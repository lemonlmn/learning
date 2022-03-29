
Private dtmNext As Date
Private Type POINTAPI
    x As Long
    y As Long
End Type

Private Declare Function GetCursorPos Lib "user32" (Point As POINTAPI) As Long
Private Declare Function SetCursorPos Lib "user32" (ByVal x As Integer, ByVal y As Integer) As Long

Sub Move_Cursor()
    Dim Hold As POINTAPI
    GetCursorPos Hold
    SetCursorPos Hold.x + 30, Hold.y
    dtmNext = DateAdd("s", 120, Now)
    Application.OnTime dtmNext, "Move_Cursor"
End Sub

Sub Stop_Cursor()
    Application.OnTime dtmNext, "Move_Cursor", , False
End Sub
