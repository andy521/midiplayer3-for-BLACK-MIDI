Free Pascal midiplayer3 for Black MIDI by ax_pokl
=============

Release and Source Code
-------------
* Latest version: http://www.axpokl.com/midiplayer3.zip
* Source code: https://github.com/axpokl/midiplayer3-for-BLACK-MIDI

How to Play
-------------
* Drag and drop files into the window to play
* Command line: midiplayer.exe filename.mid [-M]
* Support MIDI(.mid) and RMID(.rmi) file

Mouse Control
-------------
* MLeft                	Seek/Keyboard
* MRight               	Pause
* MWheel               	Volume

Key Control
-------------
* L/R                  	Seek                   	[Default=1s,Ctrl=5s,Shift=30s]
* Space                	Pause
* UP/DN                	Volumn                 	[0%-200%]
* +/-                  	Speed                  	[0%-1600%][Default=10%,Ctrl=3%,Shift=1%]
* [/]                  	Chord
* Shift+[/]            	����
* PGUP/PGDN            	Prev/Next
* Home/End             	First/Last
* F1                   	Help
* F2                   	Reset File
* Ctrl+F2              	Reset All
* F3                   	Reset Hardware
* Ctrl+F3              	Switch MIDI Device/Synthesizer
* Shift+F3             	Switch Long Message or Stream
* Ctrl+Shift+F3        	On/Off ignore same notes
* F4                   	Reset Bar 
* Ctrl+F4              	Auto Reset Bar
* Shift+F4             	Record Video
* F5/F6                	Set FPS                	[5-480][Default=120]
* Ctrl+F5/F6           	Set short MIDI event buffer
* ShiftF5/F6           	Set minimum MIDI event volume
* Ctrl+Shift+F5/F6     	Set max note buffer
* F7/F8                	Set Bar Size           	[0%-1000%][Default=10%,Ctrl=3%,Shift=1%]
* Ctrl+Shift+F7/F8     	Set keyboard note buffer
* F9                   	Set Bar Color          	[0=Chord,1=Track/Channel(With Black Key),2=Track/Channel]
* F11                  	Set Key Text           	[0=Number,1=Note,2=Blank]
* Ctrl+F11             	Set Information Text
* Shift+F11            	Set Messure/Chord line
* F12                  	Set Loop Mode          	[S=Single,A=All,N=None]

Reset or Uninstall the midiplayer3
-------------
* Run this Command to reset midiplayer3: REG DELETE HKCU\Software\ax_midi_player /f
* You can also delete the registry key HKCU\Software\ax_midi_player by regedit.exe manually
* If you are able to run midiplayer3, you can also press Ctrl+F2 to reset all the settings

Memory instead of File
-------------
* Midiplayer3 needs to load MIDI file information before playing. There are 3 ways to force midiplayer3 use memory
* 1: Set 2nd command line parameter to -M
* 2: Run Command: REG ADD HKCU\Software\ax_midi_player /v fbi /t REG_DWORD /d 1 /f
* 3: Create File "FORCE_MEMORY"
* Otherwise midiplayer3 creates 3 temporary files in %temp% folder to store the information

MIDI software synthesizer and MIDI Long Message
-------------
* It is recommended to use VirtualMIDISynth or OmniMIDI as MIDI output device
* The Synthesizer need to supports midiOutLongMsg Windows API function for long MIDI event as MIDI output
* The Microsoft GS Wavetable Synth or other MIDI output device may not support long MIDI event
* If your output device does not support long MIDI event, please increase the short MIDI event buffer by pressing Ctrl+F6
* You can also reduce the short MIDI event buffer to have better MIDI output performance by pressing Ctrl+F5

Change Channel Color
-------------
* You can change the Track/Channel color by changing the content of file "CHANNEL_COLOR"
* Each line represent a color which has a Hue value from 0-255. E.g. 0=Red, 85=Green and 170=Blue.
* The Track/Channel will sort by it's note count, then use the color in order
* The color will repeat if there is less color in the file defined than Track/Channel number

Record Video
-------------
* You will need to create file "RECORD_VIDEO" and changing the content it before record
* Three lines need to write: the complete path of the output file, frame rate and video quality
* You can record video by pressing Shift+F4, midiplayer3 will reset bar before record


ax_pokl ���� Free Pascal ������MIDI������ midiplayer3
=============

���°汾��Դ����
-------------
* ���°汾: http://www.axpokl.com/midiplayer3.zip
* Դ����: https://github.com/axpokl/midiplayer3-for-BLACK-MIDI

��β���
-------------
* ���ļ���ק�������ڲ���
* �����в��ţ�midiplayer.exe filename.mid [-M]
* ֧��MIDI(.mid)��RMID(.rmi)�ļ�

������
-------------
* ������             	��λ/���ټ���
* ����Ҽ�             	��ͣ
* ��껬��             	����

���̿���
-------------
* ��/��                	��λ                   	[Ĭ��=1��,Ctrl=5��,Shift=30��]
* �ո�                 	��ͣ
* ��/��                	����                   	[0%-200%]
* +/-                  	�ٶ�                   	[0%-1600%][Ĭ��=10%,Ctrl=3%,Shift=1%]
* [/]                  	����
* Shift+[/]            	����
* PGUP/PGDN            	ǰһ��/��һ��
* Home/End             	��һ��/���һ��
* F1                   	����
* F2                   	�����ļ�����
* Ctrl+F2              	�ָ���ʼ����
* F3                   	Ӳ������
* Ctrl+F3              	�л�MIDI�豸/�ϳ���
* Shift+F3             	�л�MIDI����Ϣ�������
* Ctrl+Shift+F3        	��/�غ�����ͬ����
* F4                   	������Ⱦ����
* Ctrl+F4              	�Զ�������Ⱦ����
* Shift+F4             	¼����Ƶ
* F5/F6                	����FPS                	[5-480][Ĭ��=120]
* Ctrl+F5/F6           	���ö�MIDI�¼�������
* ShiftF5/F6           	������СMIDI�¼�����
* Ctrl+Shift+F5/F6     	�����������������
* F7/F8                	���û�����С           	[0%-1000%][Ĭ��=10%,Ctrl=3%,Shift=1%]
* Ctrl+Shift+F7/F8     	���ø��ټ�������������
* F9                   	���û�����ɫ           	[0=����,1=����/����(�кڼ�),2=����/����]
* F11                  	������������           	[0=����,1=����,2=��]
* Ctrl+F11             	������Ϣ����
* Shift+F11            	����С��/������
* F12                  	����ѭ��ģʽ           	[S=����ѭ��,A=ȫ��ѭ��,N=��ѭ��]

������û�ж��midiplayer3
-------------
* ���д�����������midiplayer3��REG DELETE HKCU\Software\ax_midi_player / f
* ��Ҳ����ͨ��regedit.exe�ֶ�ɾ��ע�����HKCU\Software\ax_midi_player
* ������ܹ�����midiplayer3����Ҳ���԰�Ctrl+F2������������

ʹ���ڴ�����ļ�
-------------
* midiplayer3�ڲ���֮ǰ��Ҫ����MIDI�ļ���Ϣ����3�ַ�������ǿ��midiplayer3ʹ���ڴ�
* 1�����ڶ��������в�������Ϊ-M
* 2���������REG ADD HKCU\Software\ax_midi_player /v fbi /t REG_DWORD /d 1 /f
* 3�������ļ���FORCE_MEMORY��
* ����midiplayer3����%temp%�ļ����д���3����ʱ�ļ����洢��Ϣ

MIDI����ϳ�����MIDI����Ϣ���
-------------
* ����ʹ��VirtualMIDISynth��OmniMIDI��ΪMIDI����豸
* �ϳ�����Ҫ֧��midiOutLongMsg Windows API������ΪMIDI����ĳ�MIDI�¼�
* Microsoft GS Wavetable Synth������MIDI����豸���ܲ�֧�ֳ�MIDI�¼�
* �����������豸��֧�ֳ�MIDI�¼����밴Ctrl+F6���Ӷ�MIDI�¼�������
* ��������ͨ����Ctrl+F5���̶�MIDI�¼��������Ի�ø��õ�MIDI�������

����������ɫ
-------------
* ������ͨ�������ļ���CHANNEL_COLOR������������������/������ɫ
* ÿһ�д���һ����ɫ����ɫ��ֵΪ0-255�� ���磺0 =��ɫ��85 =��ɫ��170 =��ɫ
* ����/����������������������Ȼ��˳��ʹ����ɫ
* ����ļ��ж������ɫ��������/Ƶ����ţ�����ɫ���ظ�

¼����Ƶ
-------------
* ����Ҫ�����ļ���RECORD_VIDEO������¼��֮ǰ����������
* ��Ҫд���������ݣ�����ļ�������·����֡�ʺ���Ƶ����
* �����԰�Shift+F4¼����Ƶ��midiplayer3����¼��ǰ���û���
