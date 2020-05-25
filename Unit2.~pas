unit Unit2;

interface

uses
  Windows, Messages, SysUtils, Variants, Classes, Graphics, Controls, Forms,
  Dialogs, StdCtrls, ExtCtrls;

type
  TForm2 = class(TForm)
    Label1: TLabel;
    Edit1: TEdit;
    Label2: TLabel;
    Edit2: TEdit;
    Label3: TLabel;
    Edit3: TEdit;
    Label4: TLabel;
    Edit4: TEdit;
    Button1: TButton;
    Button2: TButton;
    Button3: TButton;
    Button4: TButton;
    RadioGroup1: TRadioGroup;
    Label5: TLabel;
    RadioButton1: TRadioButton;
    RadioButton2: TRadioButton;
    RadioButton3: TRadioButton;
    Edit5: TEdit;
    Label6: TLabel;
    OpenDialog1: TOpenDialog;
    Button5: TButton;
    procedure Button1Click(Sender: TObject);
    procedure FormCreate(Sender: TObject);
    procedure Button2Click(Sender: TObject);
    procedure Button3Click(Sender: TObject);
    procedure FormClose(Sender: TObject; var Action: TCloseAction);
    procedure Button4Click(Sender: TObject);
    procedure Button5Click(Sender: TObject);
  private
    { Private declarations }
  public
    { Public declarations }
  end;

var
  Form2: TForm2;
  myFile : TextFile;

implementation

uses Unit1;

{$R *.dfm}


procedure TForm2.Button1Click(Sender: TObject);
begin
  Append(myFile);
  WriteLn(myFile, edit1.text);
  if edit5.Text = '' then
  WriteLn(myFile, '.')
  else
  WriteLn(myFile,'"',edit5.text,'"');
  CloseFile(myFile);
  //1
  Append(myFile);
  WriteLn(myFile, edit2.text);
  CloseFile(myFile);

  if radiobutton1.Checked = true then
     begin
     Append(myFile);
  WriteLn(myFile, ',1');
  CloseFile(myFile);
  end else begin
  Append(myFile);
  WriteLn(myFile, ',0');
  CloseFile(myFile);
  end;
  //2
  Append(myFile);
  WriteLn(myFile, edit3.text);
  CloseFile(myFile);

  if radiobutton2.Checked = true then
     begin
     Append(myFile);
  WriteLn(myFile, ',1');
  CloseFile(myFile);
  end else begin
  Append(myFile);
  WriteLn(myFile, ',0');
  CloseFile(myFile);
  end;
  //3
  Append(myFile);
  WriteLn(myFile, edit4.text);
  CloseFile(myFile);

  if radiobutton3.Checked = true then
     begin
     Append(myFile);
  WriteLn(myFile, '.1');
  CloseFile(myFile);
  end else begin
  Append(myFile);
  WriteLn(myFile, '.0');
  CloseFile(myFile);
  end;

end;

procedure TForm2.FormCreate(Sender: TObject);
begin
 AssignFile(myFile, 'Test.txt');
  ReWrite(myFile);
end;

procedure TForm2.Button2Click(Sender: TObject);
begin
edit1.Text:='';
edit2.Text:='';
edit3.Text:='';
edit4.Text:='';
edit5.Text:='';
radiobutton1.Checked:=false;
radiobutton2.Checked:=false;
radiobutton3.Checked:=false;
end;

procedure TForm2.Button3Click(Sender: TObject);
begin
form1.close;
end;

procedure TForm2.FormClose(Sender: TObject; var Action: TCloseAction);
begin
form1.Close;
end;

procedure TForm2.Button4Click(Sender: TObject);
var
 FullProgPath: PChar;
begin
 FullProgPath:=PChar(Application.ExeName);
 WinExec(FullProgPath,SW_SHOW);
 Application.Terminate;
end;

procedure TForm2.Button5Click(Sender: TObject);
begin
if OpenDialog1.Execute then edit5.Text:=opendialog1.FileName;
end;

end.
