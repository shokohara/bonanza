---------------------------------------------------------------------
    Operation instructions for Bonanza 6.0 Windows Binary
                                             Kunihito Hoki, May 2011
---------------------------------------------------------------------

src/client/ �ȉ��̃\�[�X�t�@�C�����r���h���ē���ꂽ Windows ���s�`��
bonanza.exe ���C���̃A�v���P�[�V�������痘�p������@���L���܂��D�����ŁA
���� Windows ���s�`���Ƃ́CMakefile.vs ���� /DCSASHOGI �}�N�����`��
�ăr���h���ꂽ���̂ł��D

�܂��C�q�v���Z�X�Ƃ��� bonanza.exe ���N�����ĉ������D���� csa_shogi
���w�肷��K�v������܂��D���̂����� anonymous pipe �ōs���܂��D
bonanza.exe �͍�Ɨp�t�@�C�� book.bin, hash.bin, game.csa,
restraint.dat ���Q�ƁE�������܂��D�����̃p�X�́C�q�v���Z�v���Z�X��
������ۂɎw�肳�ꂽ�J�����g�f�B���N�g���ɂȂ�܂��D

���̃t�H���_���ɂ���ȉ��̃t�@�C���� sikou.dll �̃\�[�X�t�@�C���ł��D
Visual C++ 2008 �ɂ��r���h�\�Ȃ��Ƃ��m�F���Ă��܂��D�T���v���Ƃ���
�Q�l�ɂ��ĉ������D

- Makefile
- sikou.c      
- sikou.h
- sikou.rc
- bonanza.ico


bonanza.exe �ւ̓��o�͈ꗗ�\���ȉ��ɗ񋓂��܂��D

�y���̓R�}���h�ꗗ�z
��s�P�ʂœ��͂��󂯕t���܂��D�Ō�ɕK�����s�R�[�h�����ĉ������D

�܂��Cread [filename] �R�}���h�Ŋ�����ǂݍ��ލہC�\�Ȍ�������ɂ͏�
���ǖʂ���̎w������L�q���ĉ������D���ǖʂ������ǖʂƌ��Ȃ��������ꍇ�C
�v�l���[�`���̐����ɑ΂����舵������肭�����Ȃ��ꍇ������܂��D
bonanza.exe ���������Ă�������� game.csa �ɕۑ�����Ă��܂��D

�\���ǂ݂̒��f�C�܂��͐V���������ŏ��߂���ǂݒ����������Ȃ�����p����
��R�}���h�ɂ� * ��t���܂����D��Ɋ����̕ύX�C�΋Ǐ����̕ύX���s����
�̂����̕���p�������܂��D�����̃R�}���h����͂����ꍇ�C���O�܂� CPU
���Ԃ�����������\���ǂ݂͖��ʂɂȂ�̂Œ��ӂ��Ă��������D

* mpv num [num]
  �ǂ݋؂� num �܂Ő�������D�����l�� 1�D���̒l��傫������قǎv�l
  �����͒ቺ����D�v�l���͖����C�\���ǂݒ��͓ǂݒ����D

* mpv width [num]
  �ǂ݋؂𕡐���������ہCnum �ȏ�]���_���Ⴂ�w����͍l�����Ȃ��D����
  �l�� 400 ���x�D���̒l��傫������قǎv�l�������ቺ����D�v�l���͖�
  ���C�\���ǂݒ��͓ǂݒ����D

- tlp num [num]
  ���񏈗����s���X���b�h���� num �ɐݒ�D�����l�� 1�D

- (EOF)
  bonanza.exe ���I���D�e�v���Z�X�� pipe �̃n���h��������ۂɑ�����
  �悤�ł��D

 book off
  ���Ճf�[�^�x�[�X�̎Q�Ƃ��֎~�Dbook on ����͂���܂ŗL���D

- book on
  ���Ճf�[�^�x�[�X���Q�Ɓi�����ݒ�jbook off ����͂���܂ŗL���D

- book narrow
  ���Ճf�[�^�x�[�X�̎w��̂����C�p�x�̒Ⴂ����̗p���Ȃ��Dbook wide ��
  ���͂���܂ŗL���D

- book wide
  ���Ճf�[�^�x�[�X���畝�L���w�����I�� (�����ݒ�)�Dbook narrow ���
  �͂���܂ŗL���D

- display
  bonanza.exe ���ێ�����Ֆʂ� CSA �`���ŏo�́D�v�l�E�\���ǂݒ��͏o��
  ���ʕs��D

* hash [num]
  �n�b�V���e�[�u���Ƃ��Ċm�ۂ��郁�����̈�̑傫�����w��D�傫���͑�́C
  2 �� num �悩���� 48 �o�C�g���x�C�����l�� 18�D�v�l���͖����C�\���ǂ�
  ���͓ǂݒ����D

* limit depth [num]
  �v�l���Ԃ�T���̒T����[�� [num] �Ő����D�v�l���͖����C�\���ǂݒ�
  �͓ǂݒ����Dlimit nodes [num], limit time [num] ����͂���܂ŗL���D

* limit nodes [num]
  �v�l���Ԃ�T���m�[�h�� [num] �Ő����D�v�l���͖����C�\���ǂݒ��͓ǂ�
  �����Dlimit depth [num], limit time [num] ����͂���܂ŗL���D

* limit time [num1] [num2]
  �v�l���Ԃ��������ԂŐ��� (�����ݒ�)�Dnum1 ���C�؂�Ă����� num2 �b
  �ɐݒ�D�����ݒ�� 0�� - 10�b�D�v�l���͖����C�\���ǂݒ��͓ǂݒ����D
  limit depth [num], limit node [num] ����͂���܂ŗL���D

* limit time strict
  �v�l���Ԃ��������ԂŐ��������ꍇ�C�؂�Ă�����ӂ�̕b�������� (��
  ���ݒ�)�D�v�l���͖����C�\���ǂݒ��͓ǂݒ����Dlimit time extendable
  ����͂���܂ŗL���D

* limit time extendable
  �v�l���Ԃ��������ԂŐ��������ꍇ�C���ǂ��w�肪�����肻���ȏꍇ�ɁC
  �؂�Ă�����ӂ�̕b���𒴂��Ďv�l���邱�Ƃ������D�v�l���͖����C�\
  ���ǂݒ��͓ǂݒ����Dlimit time strict ����͂���܂ŗL���D

* time remain [num1] [num2]
  �v�l���Ԃ��������ԂŐ��������ꍇ�C�������Ԃ̎c���b�P�ʂŕύX�D
  num1  ���c�莞��
  num2  ���c�莞��

* move
  ���̈����v�l���Cbonanza.exe ���ێ�������������i�߂�D�v�l���͖�
  ���C�\���ǂݒ��͓ǂݒ����D

- [move]
  �΋Ǒ���̎w���� [move] ���󂯎��C���̈����v�l�D�X�� bonanza.exe
  ���ێ�������������i�߂�D���\�������� [move] �̌`���� CSA �`��
  �̎w�肩�� +, - �����������ɂȂ�܂��D(��F7776FU, 0087FU) �v�l����
  �����D���O�܂ōs���Ă����\���ǂ݂��q�b�g�����ꍇ�C���̌��ʂ𗘗p����
  �v�l����D

* move [move]
  ���݂̊���������i�߂�D���\�������� [move] �̌`���� CSA �`����
  �w�肩�� +, - �����������ɂȂ�܂��D(��Fmove 7776FU, move 0087FU)
  �v�l���͖����C�\���ǂݒ��͓ǂݒ����D

* move restraint
  ���̈����v�l�D�A���Crestraint.dat ���ɗ��񂳂�Ă��鍇�@����w����
  ���悤�ɂ���D�t�@�C�����̕�����͈ȉ��̂悤�ɂ��ĉ������D
  -------- restraint.dat --------
2726FU(���s)
7776FU(���s)
(EOF)
  -------------------------------
  �v�l���͖����C�\���ǂݒ��͓ǂݒ����D

* new
  bonanza.exe ���ێ���������𕽎�̏�����Ԃɕ��A (�����ݒ�)�D�v�l��
  �͖����C�\���ǂݒ��f�D

- ping
  pong �̏o�͂𑣂��D

- ponder on
  �\���ǂ݋@�\�I���i�����ݒ�j�Dponder off ����͂���܂ŗL���D

* ponder off
  �\���ǂ݋@�\�I�t�D�\���ǂݒ��͒��f�Dponder on ����͂���܂ŗL��

* read [filename] t [num]
  CSA �`���̊����t�@�C����ǂށDbonanza.exe ���ێ�����������X�V�D�v�l
  ���͖����C�\���ǂݒ��͐V�����ǖʂ���ǂݒ����D
  [filename]  �t�@�C�������w��D�s���I�h "." ���w�肵���ꍇ�͌��݂̊�
              ����ǂށD
  [num]       �萔���w��D�ȗ������ꍇ�͏I�[�܂œǂށD

- resign [num]
  ��������X�R�A�̉��� num ���w��D32600 �ɐݒ肷��Ɠ������Ȃ��D����
  �ݒ�� 533�D

- s
  ���̈����ł��邾�������w������D�v�l���łȂ��ꍇ�͖����D


�y�o�́z�@�i��s�P�ʂōs���܂��D�Ō�ɕK�����s�R�[�h�����݂��܂��j

move[move]
  �v�l���ʂ̎w��D���\�������� [move] �̌`���� CSA �`���̎w�肩�� +,
  - �����������ɂȂ�܂��D(��Fmove7776FU, move0087FU)

info ponder start
  �\���ǂ݂��J�n����Ƃ��ɏo��

info ponder end
  �\���ǂ݂��I�����������ɏo�́D'info ponder start' ���o�͂���Ă���
  '[move]' �R�}���h����͂���܂ł����ۂɗ\���ǂ݂ɔ�₵�����ԁD�\��
  �ǂ݂̒��f�E�ǂݒ������s�����ꍇ�C�r���� 'info ponder end' ���o�͂�
  ���D

info[statistics]
  �v�l�����ǖʂ����Ճf�[�^�x�[�X���Ɍ��������ꍇ�ɏo�͂���铝�v���D
  (��Finfo 7776FU(86%) 2726FU(14%))

info[score] [move sequence]:...
  �v�l���ɑ�����o�͂����v�l�̓r���o�߁Dmpv num �̒l�� 2�ȏ�w�肷��
  �ƁC���� ":" �ŋ�؂��� [score] [move sequence]�@�𕡐��o�͂���D

  [score]
    �o�͂��ꂽ���_�ł� bonanza �̐���]���l
     325.99            - ���ɂƂ��ėD���ȌJ��Ԃ�
     325.98 ~  300.01  - ���ʋl��
     300.00 ~ -300.00  - �]���l�D1�_�����ꖇ���ɑ���
    -300.01 ~ -325.98  - ���ʋl��
    -325.99            - ���ɂƂ��ėD���ȌJ��Ԃ�

  [move sequence]
    �o�͂��ꂽ���_�ł� bonanza �̐���őP����DCSA �`���̎w����X�y�[
    �X�ŋ�؂��ďo��
  (��Finfo+0.43 -5142OU +2726FU -4232OU +2625FU -7162GI)

info tt [num]
  �v�l�ɔ�₵������ num ���o��

pong
  ping ���͂�^�����ۂɏo��

statsatu=[num1] cpu=[num2] nps=[num3]
  �v�l�I�����ɏo�͂���� bonanza �̃R���s���[�^�����g�p�󋵐���l�D��
  �ǖʋǂ����Ճf�[�^�x�[�X���Ō��������ꍇ�͏o�͂���܂���D
  [num1]  �n�b�V���̈�g�p�p�[�Z���e�[�W
  [num2]  CPU ���Ԑ�L�p�[�Z���e�[�W
  [num3]  ��b������̌����m�[�h�� / 1000
  (��Fstatsatu=22 cpu=98 nps=886.28)


�y��z
���o�͂̈��D[out]: �ȍ~�̍s�͏o�́C[in]: �ȍ~�̍s�͓��͂�\���D

 1 [out]: Bonanza Version 4.0.3 - The Computer Shogi Engine
 2 [in ]: book off
 3 [in ]: 5968OU
 4 [out]: info+0.47 -5142OU +7776FU -3334FU +3948GI ...
 5 [out]: info+0.26 -5142OU +7776FU -7162GI +6878OU ...
 6 [out]: info+0.47 -5142OU +7776FU -3334FU +6878OU ...
 7 [out]: info+0.15 -5142OU +7776FU -4232OU +7978GI ...
 8 [out]: statsatu=54 cpu=100 nps=461.92
 9 [out]: move5142OU
10 [out]: info tt 000:10
11 [out]: info ponder start
12 [out]: info+0.27 +7776FU -3334FU +6878OU -4232OU ...
13 [out]: info+0.27 +7776FU -3334FU +6878OU -4232OU ...
14 [out]: info+0.33 +7776FU -3334FU +2726FU -7162GI ...
15 [out]: info+0.32 +7776FU -3132GI +6878OU -4231OU ...
16 [in ]: 7776FU
17 [out]: info ponder end
18 [out]: info+0.13 -8384FU +2726FU -8485FU +2625FU ...


 1     �o�[�W�������
 2     ���Ճf�[�^�x�[�X�̎Q�Ƃ��֎~������
 3     ���̏��聣�U�����D���̎��̎w����� bonanza �Ɏv�l������
 4-  7 �]���l�C�ǂ݋ؓr���o��
 8     �R���s���[�^�����g�p�󋵐���l
 9     �v�l���ʂ̎w��
10     �v�l�ɔ�₵������
11     �\���ǂ݊J�n�̍��}
12- 15 �]���l�C�ǂ݋ؓr���o�߁D�ǂ݋ؑ���ځ��V�Z���͗\����D
16     ���̂Q��ځ��V�Z���D���̎��̎w����� bonanza �Ɏv�l������
17     �\���ǂݏI���̍��}
18     �]���l�C�ǂ݋ؓr���o��
