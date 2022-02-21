# hse_hw1_meth
[Ссылка на Google Colab](https://colab.research.google.com/drive/1-bdNvxyVB3YTh-oHj4Ngpq06lbSNfjNM?usp=sharing)

### №1 FastQC
У ICM процент GC нуклеотидов в два раза меньше чем у РНК. 
RNA            |  ICM
:-------------------------:|:-------------------------:
![](https://github.com/ruanmik/hse_hw1_meth/blob/main/images/rna_fastqc.png)|![](https://github.com/ruanmik/hse_hw1_meth/blob/main/images/ICM_fast.png)

Видим, что у ICM к концу секвенирования падает Quality Score. 
RNA            |  ICM
:-------------------------:|:-------------------------:
![](https://github.com/ruanmik/hse_hw1_meth/blob/main/images/rna_fastqc1.png)|![](https://github.com/ruanmik/hse_hw1_meth/blob/main/images/icm_fast1.png)

Видим, что у ICM большоое количество тимина(45%) и малое содержание цитозина(5%).
RNA            |  ICM
:-------------------------:|:-------------------------:
![](https://github.com/ruanmik/hse_hw1_meth/blob/main/images/rna_fastqc2.png)|![](https://github.com/ruanmik/hse_hw1_meth/blob/main/images/icm_fast2.png)

Распределение сильно отличается от теоретического, наблюдаем 2 пика - на 20% и 70%
RNA            |  ICM
:-------------------------:|:-------------------------:
![](https://github.com/ruanmik/hse_hw1_meth/blob/main/images/rna_fastqc4.png)|![](https://github.com/ruanmik/hse_hw1_meth/blob/main/images/icm_fast4.png)
---
### №2 Число ридов и дупликаций

Образец | Число ридов на участке 11347700-11367700 | Число ридов на участке 40185800-40195800 | Количество дупликаций
:-------------------------:|:-------------------------:|:-------------------------:|:-------------------------:
8 cell | 1090 | 2744 | 81.69%
Epiblast | 2328 | 8935 | 97.08%
ICM | 1456 | 5060 | 90.92%

bash скрипт для дедупликации
`! ls *_bismark_bt2_pe.bam | xargs -P 3 -tI{} deduplicate_bismark --bam --paired -o s_{} {}`

---
### №3 M-bias

[8 Cell]()
![](https://github.com/ruanmik/hse_hw1_meth/blob/main/images/8cel.png)
[ICM]()
![](https://github.com/ruanmik/hse_hw1_meth/blob/main/images/icm.png)
[Epiblast]()
![](https://github.com/ruanmik/hse_hw1_meth/blob/main/images/epiblast.png)
