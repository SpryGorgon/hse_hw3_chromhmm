## Гистоновые метки и эпигенетические состояния

### Клеточная линия: HSMMtube

### Список гистоновых меток:
| Гистоновая метка |          Файл          |
|------------------|------------------------|
|      H2AFZ       |   H2azStdAlnRep1.bam   | 
|     H3K27ac      | H3k27acStdAlnRep1.bam  |
|   H3K36me3       | H3k36me3StdAlnRep1.bam	|
| H3K4me1          | H3k4me1StdAlnRep1.bam	|
| H3K4me2          | H3k4me2StdAlnRep1.bam	|
| H3K4me3          | H3k4me3StdAlnRep1.bam	|
| H3K79me2         | H3k79me2StdAlnRep1.bam	|
| H3K9ac           | H3k9acStdAlnRep1.bam	  |
| H4K20me1         | H4k20me1StdAlnRep1.bam	|
| CTCF             | CtcfStdAlnRep1.bam	    |

### Контроль: ControlStdAlnRep1.bam


### Эпигенетические состояния:
| Номер состояния | Гистоновые метки | Название |
|-----------------|------------------|----------|
|   1   | H2AFZ, H3K4me1, H3K4me2 | Strong enhancer | 
|   2   | H3K27ac, H3K9ac, H3K4me1, H3K4me2 | Strong enhancer |
|   3   | H2AFZ, H3K4me2, H3K4me3, H3K9ac | Active Promoter |
|   4   | H3K79me2, H3K4me2 | Transcribed |
|   5   | H3K79me2, H4K20me1 | Transcribed |
|   6   | H3K79me2 | Weak transcribed |
|   7   | H3K36me3 | Weak transcribed	|
|   8   | - | Heterochromatin; low signal |
|   9   | - | Heterochromatin; low signal |
|   10  | CTCF | Insulator |

## [Отчёт ChromHMM](./ChromHMM_Results/webpage_10.html)

![image](https://user-images.githubusercontent.com/52814490/230118102-8ece6e74-fc6c-463b-b355-b47dfb398092.png)
![image](https://user-images.githubusercontent.com/52814490/230118133-97b7e463-ea21-4345-aaf0-c21741e505b4.png)
![image](https://user-images.githubusercontent.com/52814490/230118170-78e0cc05-ddc6-427b-b835-d72aaf15adbe.png)
![image](https://user-images.githubusercontent.com/52814490/230118199-94c34b9f-5ec7-4c22-b9ec-4c1dc8ec1d7a.png)
![image](https://user-images.githubusercontent.com/52814490/230118233-105b05c1-1c31-4965-b341-5724b9e18fe9.png)

## Участки генома в UCSC GenomeBrowser
![image](https://user-images.githubusercontent.com/52814490/230119281-5ed1df21-b34c-499d-afe1-a56f43817fdb.png)
![image](https://user-images.githubusercontent.com/52814490/230119492-41296ea6-8800-412a-bc51-7ea7f0a886d5.png)

## Список запущенных команд:
Бинаризация профилей из ChiP-seq экспериментов:

```
!java -mx5000M -jar /content/ChromHMM/ChromHMM.jar BinarizeBam -b 200  /content/ChromHMM/CHROMSIZES/hg19.txt /content/ cellmarkfiletable.txt   binarizedData
```

Запуск ChromHMM

```
!java -mx5000M -jar /content/ChromHMM/ChromHMM.jar LearnModel -p 0 binarizedData ChromHMM_Results 10 hg19
```

## Результат бонусного задания

![image](https://user-images.githubusercontent.com/52814490/230126414-ddad3433-4a47-4e09-a6af-50dd056b674b.png)
