Imports System.Windows.Forms.VisualStyles.VisualStyleElement

Public Class Form1
    Private Sub btPrint_Click(sender As Object, e As EventArgs) Handles btPrint.Click
        '//cetak info
        rtbinfo.Text = "NIM" + vbTab + vbTab + ": " + tbNim.Text + vbCrLf &
                       "Nama" + vbTab + vbTab + ": " + tbNama.Text + vbCrLf &
                       "Alamat" + vbTab + vbTab + ": " + rtbAlamat.Text

        '//gender check
        If rbLaki.Checked = True Then
            rtbinfo.Text += vbCrLf + "jenis kelamin" + vbTab + ": " + rbLaki.Text
        ElseIf rbPerempuan.Checked = True Then
            rtbinfo.Text += vbCrLf + "jenis kelamin" + vbTab + ": " + rbPerempuan.Text
        End If

        '//tempat tanggal lahir
        Dim umur As Integer = Date.Now.Year - dtpTgllhr.Value.Year

        If Date.Now.Month > dtpTgllhr.Value.Month Then
            umur -= 1
        End If

        If Date.Now.Date <> dtpTgllhr.Value.Date And umur >= 1 Then
            rtbinfo.Text += vbCrLf + "tempat tanggal lahir" + vbTab + ": " + tbTemptlhr.Text + ", " + dtpTgllhr.Value.ToString("dd MMMM yyyy", New Globalization.CultureInfo("id-ID"))
            rtbinfo.Text += vbCrLf + "umur" + vbTab + vbTab + ": " + umur.ToString + " tahun"
        ElseIf Date.Now.Date <> dtpTgllhr.Value.Date And umur < 1 Then
            rtbinfo.Text += vbCrLf + "tempat tanggal lahir" + vbTab + ": " + tbTemptlhr.Text + ", " + dtpTgllhr.Value.ToString("dd MMMM yyyy", New Globalization.CultureInfo("id-ID"))
            rtbinfo.Text += vbCrLf + "umur" + vbTab + vbTab + ": <1 tahun"
        ElseIf Date.Now.Date = dtpTgllhr.Value.Date Then
            MessageBox.Show("tanggal lahir sama dengan tanggal sekarang!", "error!", MessageBoxButtons.OKCancel, MessageBoxIcon.Error)
        End If

        '//beasiswa status
        If cbDaftardgn.SelectedItem IsNot Nothing Then
            rtbinfo.Text += vbCrLf + "status pendaftar" + vbTab + ": " + cbDaftardgn.SelectedItem.ToString
        End If

        '//prog studi
        If cbProdi.SelectedItem IsNot Nothing Then
            rtbinfo.Text += vbCrLf + "Program Studi" + vbTab + ": " + cbProdi.SelectedItem.ToString
        End If

        '//jurusan
        If cbJurusan.SelectedItem IsNot Nothing Then
            rtbinfo.Text += vbCrLf + "Jurusan" + vbTab + vbTab + ": " + cbJurusan.SelectedItem.ToString
        End If

        '//matkul
        If clbMatkul.CheckedItems.Count > 0 Then
            rtbinfo.Text += vbCrLf + "mata kuliah yang di ambil" + vbCrLf + vbTab + vbTab + ": "
            For Each chckbox As Object In clbMatkul.CheckedItems
                rtbinfo.Text += chckbox.ToString + ", "
            Next
            'deleting coma from last item
            rtbinfo.Text = rtbinfo.Text.Trim().Remove(rtbinfo.TextLength - 2)
        End If

        '//semester status
        If cbSmt.SelectedItem IsNot Nothing Then
            rtbinfo.Text += vbCrLf + "semester" + vbTab + vbTab + ": " + cbSmt.SelectedItem.ToString + " - "
            If rbSmtA.Checked = True Then
                rtbinfo.Text += rbSmtA.Text
            ElseIf rbSmtB.Checked = True Then
                rtbinfo.Text += rbSmtB.Text
            ElseIf rbSmtC.Checked = True Then
                rtbinfo.Text += rbSmtC.Text
            End If

        End If

        '//tahun masuk
        rtbinfo.Text += vbCrLf + "tahun masuk" + vbTab + ": " + dtpTahunmsk.Value.Date.Year.ToString

        '//status mahasiswa (aktif / tidak)
        If cbStatusMhs.SelectedItem IsNot Nothing Then
            rtbinfo.Text += vbCrLf + "Status Mahasiswa" + vbTab + ": " + cbStatusMhs.SelectedItem.ToString
        End If

        '//riwayat studi

        '//if else statement
        'If cbStudi.SelectedItem IsNot Nothing Then
        'If cbStudi.SelectedItem = "lainnya..." Then
        'rtbinfo.Text += vbCrLf + "riwayat" + vbTab + vbTab + ": " + tbStudi.Text
        'Else
        'rtbinfo.Text += vbCrLf + "Riwayat" + vbTab + vbTab + ": " + cbStudi.SelectedItem.ToString
        'End If
        'End If

        'switch-case statement
        If cbStudi.SelectedItem IsNot Nothing Then
            Select Case cbStudi.SelectedItem
                Case "lainnya..."
                    rtbinfo.Text += vbCrLf + "riwayat" + vbTab + vbTab + ": " + tbStudi.Text
                Case Else
                    rtbinfo.Text += vbCrLf + "Riwayat" + vbTab + vbTab + ": " + cbStudi.SelectedItem.ToString()
            End Select
        End If

        '//email
        rtbinfo.Text += vbCrLf + "Email" + vbTab + vbTab + ": " + tbEmail.Text

        '//pekerjaan
        rtbinfo.Text += vbCrLf + "Pekerjaan" + vbTab + ": " + tbstspekerja.Text

        '//alamt kampus
        rtbinfo.Text += vbCrLf + "Alamat kampus" + vbTab + ": " + rtbalmtkmps.Text

        '//checkbox UKM
        If clbUkm.CheckedItems.Count > 0 Then
            rtbinfo.Text += vbCrLf + "UKM yang di ikuti" + vbTab + ": "
            For Each cekbok As Object In clbUkm.CheckedItems
                rtbinfo.Text += cekbok.ToString + ", "
            Next
            'deleting coma from last item
            rtbinfo.Text = rtbinfo.Text.Trim().Remove(rtbinfo.TextLength - 2)
        End If

        '//kelas
        'If rbSmtA.Checked = True Then
        'rtbinfo.Text += vbCrLf + "kelas" + vbTab + vbTab + ": " + rbSmtA.Text
        'ElseIf rbSmtB.Checked = True Then
        'rtbinfo.Text += vbCrLf + "kelas" + vbTab + vbTab + ": " + rbSmtB.Text
        'ElseIf rbSmtC.Checked = True Then
        'rtbinfo.Text += vbCrLf + "kelas" + vbTab + vbTab + ": " + rbSmtC.Text
        'End If




    End Sub
    'import gambar with clicking textbox
    Private Sub tbLinkpth_Click(sender As Object, e As EventArgs) Handles tbLinkpth.Click
        'pUserpict.ImageLocation = "C:\Users\Nitro AN715-51\Pictures\Untitled-1-01.png"
        'pUserpict.Image = Image.FromFile("C:\Users\Nitro AN715-51\Pictures\Untitled-1-01.png")
        'OpenFileDialog1.ShowDialog()
        'pbProfil.ImageLocation = OpenFileDialog1.FileName
        If OpenFileDialog1.ShowDialog() = DialogResult.OK Then
            '// Ambil path gambar yang dipilih
            Dim imagePath As String = OpenFileDialog1.FileName

            '// Tampilkan path gambar di TextBox
            tbLinkpth.Text = imagePath

            '// Tampilkan gambar di PictureBox
            pbProfil.Image = Image.FromFile(imagePath)
        End If
    End Sub

    '//using button on right textbox
    Private Sub btImport_Click(sender As Object, e As EventArgs) Handles btImport.Click
        'pUserpict.ImageLocation = "C:\Users\Nitro AN715-51\Pictures\Untitled-1-01.png"
        'pUserpict.Image = Image.FromFile("C:\Users\Nitro AN715-51\Pictures\Untitled-1-01.png")
        'OpenFileDialog1.ShowDialog()
        'pbProfil.ImageLocation = OpenFileDialog1.FileName

        '//dialog filter image
        OpenFileDialog1.Filter = "gambar | *.jpg;*jpeg;*.png;*.bmp"

        If OpenFileDialog1.ShowDialog() = DialogResult.OK Then
            ' Ambil path gambar yang dipilih
            Dim imagePath As String = OpenFileDialog1.FileName

            ' Tampilkan path gambar di TextBox
            tbLinkpth.Text = imagePath

            ' Tampilkan gambar di PictureBox
            pbProfil.Image = Image.FromFile(imagePath)
        End If
    End Sub

    Private Sub pUserpict_Click(sender As Object, e As EventArgs) Handles pbProfil.Click
        pbProfil.ImageLocation = ""
    End Sub
    '//system process to web KIPK
    Private Sub LinkLkipk_LinkClicked(sender As Object, e As System.Object) Handles LinkLkipk.LinkClicked
        System.Diagnostics.Process.Start(e.Link.LinkData.ToString())
    End Sub

    Private Sub Form1_Load(sender As Object, e As EventArgs) Handles MyBase.Load
        'link KIPK info throw to web
        LinkLkipk.Text = "info lebih lanjut KIPK"
        LinkLkipk.Links.Add(0, 22, "https://kip-kuliah.kemdikbud.go.id/")
    End Sub

    '//activate or deactivate textbox studi
    Private Sub cbStudi_changeIndex(sender As Object, e As EventArgs) Handles cbStudi.SelectedIndexChanged
        Select Case cbStudi.SelectedItem
            Case "lainnya..."
                tbStudi.Enabled = True
            Case Else
                tbStudi.Enabled = False
        End Select
    End Sub
End Class
