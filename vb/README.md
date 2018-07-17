```vb
Sub matching()
    Dim hida As Long
    Dim migi As Long
    Dim ws1 As Worksheet
    Dim ws2 As Worksheet
    
    Set ws1 = ThisWorkbook.Worksheets("sample6")
    
    Workbooks.Open Filename:=ThisWorkbook.Path & "\user1.xlsx"
    
    Set ws2 = ActiveWorkbook.Worksheets("sample")
    
    For hida = 2 To 6
        For migi = 2 To 7
            If ws1.Range("A" & hida).Value = ws2.Range("A" & migi).Value And _
            ws1.Range("B" & hida).Value = ws2.Range("B" & migi).Value And _
            ws1.Range("C" & hida).Value = ws2.Range("C" & migi).Value Then
                ws1.Range("E" & hida).Value = "OK"
                Exit For
            End If
        Next
    Next
    
    For hida = 2 To 6
        If ws1.Range("E" & hida).Value = "" Then
            ws1.Range("E" & hida).Interior.Color = vbYellow
        Else
            ws1.Range("E" & hida).Interior.Color = xlNone
        End If
    Next
End Sub
```