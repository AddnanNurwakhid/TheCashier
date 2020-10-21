# TheCashier

Aplikasi untuk kemudahan kasir untuk menginputkan barang atau jasa yang dibeli dan menjumlahkan total harganya.

fitur
1.  3 textbox untuk penginputan nama item, jumlah, dan harga
2.  1 combobox berisi jenis item
3.  1 button untuk penginputan
4.  1 listbox tempat item yang diinput akan ditampilkan
5.  2 label untuk menampilkan total harga dari seluruh transaksi

Single Responsibility
Ada pada kodingan dalam calculator.cs dimana berisi intruksi pada aplikasi untuk menambahkan item yang diinput lalu memproses penambahan dan menampilkan total pada listbox

        public void AddItem(Item item)
        {
            this.listItem.Add(item);
            this.total += item.getSubtotal();
        }
        
Class item berisi tentang penginisialisasian untuk input dari jendela agar bisa diterima dan dikirim ke class calculator untuk diproses dan ditampilkan
contoh berikut

        public MainWindow()
        {
            InitializeComponent();
            calculator = new Calculator();
            listBox.ItemsSource = calculator.getListItem();
        }

Pada MainWindow() diatas adalah penginisialisasian untuk calculator mengambil dari Class Calculator untuk menampilkan listBox yang ada didalamnya.
