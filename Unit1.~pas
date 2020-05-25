unit Unit1;

interface

uses
  Windows, Messages, SysUtils, Variants, Classes, Graphics, Controls, Forms,
  Dialogs, StdCtrls;

type
  TForm1 = class(TForm)
    Edit1: TEdit;
    Label1: TLabel;
    Label2: TLabel;
    Edit2: TEdit;
    Button1: TButton;
    Edit3: TEdit;
    Edit4: TEdit;
    Edit5: TEdit;
    Edit6: TEdit;
    Edit7: TEdit;
    Edit8: TEdit;
    Label3: TLabel;
    Edit9: TEdit;
    Label4: TLabel;
    procedure Button1Click(Sender: TObject);
  private
    { Private declarations }
  public
    { Public declarations }
  end;

var
  Form1: TForm1;

implementation

uses Unit2;

{$R *.dfm}

procedure TForm1.Button1Click(Sender: TObject);
begin
Append(myFile);
WriteLn(myFile, edit1.text);
WriteLn(myFile, edit2.text);
WriteLn(myFile, 'Вы должны из предложенных нескольких вариантов ответов выбрать правильный.');
WriteLn(myFile, '.');
WriteLn(myFile, edit4.text);
WriteLn(myFile, edit3.text);
WriteLn(myFile, edit6.text);
WriteLn(myFile, edit5.text);
WriteLn(myFile, edit8.text);
WriteLn(myFile, edit7.text);
WriteLn(myFile, edit9.text);
WriteLn(myFile, edit7.text);
WriteLn(myFile, '.');
CloseFile(myFile);
form2.show;
form1.Hide;
end;

end.
