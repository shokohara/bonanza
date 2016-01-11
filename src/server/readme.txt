----------------------------------------------------------------------
         Bonanza 6.0 - Scripts for Cluster Parallelizatoin
                                              Kunihito Hoki, May 2011
----------------------------------------------------------------------


1. Legal Notices
-----------------

This program is protected by copyrights. Without a specific 
permission, any means of commercial applications are prohibited.
Furthermore, this program is distributed without any warranty.
Within these limits, you can use, redistribute, and/or modify it.


2. �g����
------------------

���̃f�B���N�g���ɂ�2011�N5���ɊJ�Â��ꂽ��21�񐢊E�R���s���[�^�����I�茠�� Bonanza ���g�p�����T�[�o�X�N���v�g�Q���W�J����܂��BTCP/IP �\�P�b�g�ʐM���\�ȃN���X�^�[���œ��삵�܂��B

- majority_server.pl

���������c���s�� Perl �X�N���v�g�BCSA �΋ǃT�[�o�̃N���C�A���g�Ƃ��ē��삵�܂��Bbonanza �� parallel_server.pl �����̃T�[�o�X�N���v�g�̃N���C�A���g�ł��B���s��� run-server.sh �Ɏ�����Ă��܂��B

--client_port        �N���C�A���g�Ƃ̒ʐM�ڑ��̂��߂� listen ����|�[�g�ԍ�
--client_num         �΋ǊJ�n�ɕK�v�ȃN���C�A���g��
--csa_host           CSA �΋ǃT�[�o�̃z�X�g��
--csa_port           CSA �΋ǃT�[�o�̃|�[�g�ԍ�
--csa_id             CSA �΋ǃT�[�o�ɕ񍐂��閼�O
--csa_pw             CSA �΋ǃT�[�o�ɕ񍐂���p�X���[�h
--sec_limit          �������ԁi�b�j
--sec_limit_up       �������Ԃ��؂�Ă���̕b�ǂ�
--time_response      �\�z�����ʐM�x�� (�b)
--time_stable_min    ���Ղɂ�����v�l�؂�グ���s���Œ᎞�� (�b)
--final_as_confident final �M���� confident ��������t���O�B

����͂�����Q�O�P�O�̍��c�T�[�o����ɍ��ꂽ���̂ł��B�d�C�ʐM��w�ɓ��������C�m�i���j�̏������l�A������w��w�@�������������Ȃ̋��q�m�K�������瑽���̃o�O���|�[�g�����������܂����B���肪�Ƃ��������܂��B�܂��A���c�@�̌����𐄐i���Ă����������d�C�ʐM��w�ɓ��B�u�����ƎВc�@�l��񏈗��w��Ɋ��ӂ��܂��B



- parallel_server.pl

���[�g���񉻒T�����s�� Perl �X�N���v�g�B���������c�T�[�o (majority_server.pl) �̃N���C�A���g�Ƃ��ē��삵�܂��Bbonanza �����̃T�[�o�X�N���v�g�̃N���C�A���g�ł��B���s��� run-parallel.sh �Ɏ�����Ă��܂��B���������c�T�[�o�Ƃ͈قȂ�A�N���C�A���g�Ƃ̒ʐM���ؒf���ꂽ�ꍇ�ɂ͓�����I�����܂��B

--client_port        �N���C�A���g�Ƃ̒ʐM�ڑ��̂��߂� listen ����|�[�g�ԍ�
--client_num         �΋ǊJ�n�ɕK�v�ȃN���C�A���g��
--server_host        ���c�T�[�o�̃z�X�g��
--server_port        ���c�T�[�o�̃|�[�g�ԍ�
--server_id          ���c�T�[�o�ɕ񍐂���N���C�A���g��
--split_nodes        ����T���O�ɍs�����O�T���̃m�[�h��



- dfpn_server.pl

DFPN �l�����T���̃T�[�o�v���O�����BDFPN �l�����T�����s�����[�J�� bonanza ���� dfpn connect �R�}���h�ŁA�l�����T���̌��ʂ𗘗p����N���C�A���g�� bonanza ���� dfpn_client �R�}���h�Őڑ����܂��B�N���C�A���g���烋�[�g�ǖʂ��󂯎��A���̋ǖʂƂ��̑S�q�ǖʂ����[�J�ɓ����A���ʂ��N���C�A���g�ɕ񍐂��܂��B�d���̗D�揇�ʂ͂P. ���[�g�A2. �őP��ɂ��ڍs����q�ǖʁA3. ���̑��S�q�ǖʂł��B���[�J�[�ƃN���C�A���g�̐��͕������邱�Ƃ�z�肵�Ă��܂��B�N���C�A���g���قȂ�ǖʂ����[�g�Ƃ��Ďv�l���Ă��Ă����������삵�܂��B

--client_port        �N���C�A���g�⃏�[�J�Ƃ̒ʐM�ڑ��̂��߂� listen ����
                     �|�[�g�ԍ�
