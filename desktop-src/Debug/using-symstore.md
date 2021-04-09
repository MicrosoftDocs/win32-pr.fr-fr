---
description: SymStore (symstore.exe) est un outil permettant de créer des magasins de symboles. Il est inclus dans le package outils de débogage pour Windows.
ms.assetid: fe8a96e9-e780-4e96-98ef-c5128515ee6c
title: Utilisation de SymStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a87b5c527717d78adb9202fd1eddd54d1f44c02
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110710"
---
# <a name="using-symstore"></a>Utilisation de SymStore

SymStore (symstore.exe) est un outil permettant de créer des magasins de symboles. Il est inclus dans le package [outils de débogage pour Windows](https://www.microsoft.com/?ref=go) .

SymStore stocke les symboles dans un format qui permet au débogueur de rechercher les symboles en fonction de l’horodatage et de la taille de l’image (pour un fichier. dbg ou exécutable), ou de la signature et de l’âge (pour un fichier. pdb). L’avantage du magasin de symboles par rapport au format de stockage de symboles traditionnel est que tous les symboles peuvent être stockés ou référencés sur le même serveur et récupérés par le débogueur sans connaissance préalable du produit contenant le symbole correspondant.

Notez que plusieurs versions des fichiers de symboles. pdb (par exemple, les versions publique et privée) ne peuvent pas être stockées sur le même serveur, car elles contiennent chacune les mêmes signature et âge.

## <a name="symstore-transactions"></a>Transactions SymStore

Chaque appel à SymStore est enregistré en tant que transaction. Il existe deux types de transactions : ajouter et supprimer.

Lorsque le magasin de symboles est créé, un répertoire nommé « 000admin » est créé sous la racine du serveur. Le répertoire 000admin contient un fichier pour chaque transaction, ainsi que les fichiers journaux Server.txt et History.txt. Le fichier Server.txt contient une liste de toutes les transactions qui se trouvent actuellement sur le serveur. Le fichier History.txt contient un historique chronologique de toutes les transactions.

Chaque fois que SymStore stocke ou supprime des fichiers de symboles, un nouveau numéro de transaction est créé. Ensuite, un fichier, dont le nom est ce numéro de transaction, est créé dans 000admin. Ce fichier contient une liste de tous les fichiers ou pointeurs qui ont été ajoutés au magasin de symboles au cours de cette transaction. Si une transaction est supprimée, SymStore lit son fichier de transactions pour déterminer les fichiers et les pointeurs à supprimer.

Les options **Add** et **del** spécifient si une transaction d’ajout ou de suppression doit être effectuée. L’inclusion de l’option **/p** avec une opération Add spécifie qu’un pointeur doit être ajouté ; l’omission de l’option **/p** spécifie que le fichier de symboles réel doit être ajouté.

Il est également possible de créer le magasin de symboles en deux étapes distinctes. Dans la première étape, vous utilisez SymStore avec l’option **/x** pour créer un fichier d’index. Dans la deuxième étape, vous utilisez SymStore avec l’option **/y** pour créer le magasin de fichiers ou de pointeurs à partir des informations contenues dans le fichier d’index.

Il peut s’agir d’une technique utile pour diverses raisons. Par exemple, cela permet de recréer facilement le magasin de symboles si le magasin est perdu, tant que le fichier d’index existe toujours. Ou peut-être que l’ordinateur contenant les fichiers de symboles dispose d’une connexion réseau lente à l’ordinateur sur lequel le magasin de symboles sera créé. Dans ce cas, vous pouvez créer le fichier d’index sur le même ordinateur que les fichiers de symboles, transférer le fichier d’index sur le deuxième ordinateur, puis créer le magasin sur le deuxième ordinateur.

Pour obtenir la liste complète de tous les paramètres SymStore, consultez [options de SymStore Command-Line](symstore-command-line-options.md).

> [!Note]  
> SymStore ne prend pas en charge les transactions simultanées de plusieurs utilisateurs. Il est recommandé qu’un utilisateur soit désigné « administrateur » du magasin de symboles et qu’il soit responsable de toutes les transactions **Add** et **del** .

 

## <a name="transaction-examples"></a>Exemples de transactions

Voici deux exemples de SymStore ajout de pointeurs de symboles pour la build 3790 de Windows Server 2003 à \\ \\ SampleDir \\ symsrv :

``` syntax
symstore add /r /p /f \\BuildServer\BuildShare\3790free\symbols\*.*
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 free"
   /c "Sample add"
symstore add /r /p /f \\BuildServer\BuildShare\3790Chk\symbols\*.* 
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 checked"
   /c "Sample add"
```

Dans l’exemple suivant, SymStore ajoute les fichiers de symboles réels pour un projet d’application dans les \\ \\ \\ emplacements AppServer largeapp \\ à \\ \\ TestDir \\ symsrv :

``` syntax
symstore add /r /f \\largeapp\appserver\bins\*.* /s \\testdir\symsrv 
   /t "Large Application" /v "Build 432" /c "Sample add"
```

Voici un exemple d’utilisation d’un fichier d’index. Tout d’abord, SymStore crée un fichier d’index basé sur la collection de fichiers de symboles dans les \\ \\ \\ emplacements AppServer largeapp \\ \\ . Dans ce cas, le fichier d’index est placé sur un troisième ordinateur, \\ \\ hubserver \\ hubshare. Vous utilisez l’option **/g** pour spécifier que le préfixe de fichier « \\ \\ largeapp \\ AppServer » peut changer à l’avenir :

``` syntax
symstore add /r /p /g \\largeapp\appserver /f 
   \\largeapp\appserver\bins\*.* 
   /x \\hubserver\hubshare\myindex.txt
```

Supposons à présent que vous déplaciez tous les fichiers de symboles de la machine \\ \\ largeapp AppServer et que vous les \\ Placez sur \\ \\ myarchive \\ AppServer. Vous pouvez ensuite créer le magasin de symboles lui-même à partir du fichier d’index \\ \\ hubserver \\ hubshare \\myindex.txt comme suit :

``` syntax
symstore add /y \\hubserver\hubshare\myindex.txt 
   /g \\myarchive\appserver /s \\sampledir\symsrv /p 
   /t "Large Application" /v "Build 432" /c "Sample Add from Index"
```

Enfin, voici un exemple de SymStore de suppression d’un fichier ajouté par une transaction précédente. Consultez la section suivante pour obtenir une explication sur la façon de déterminer l’ID de transaction (dans ce cas, 0000000096).

``` syntax
symstore del /i 0000000096 /s \\sampledir\symsrv
```

## <a name="compressed-files"></a>Fichiers compressés

SymStore peut être utilisé avec des fichiers compressés de deux manières différentes.

1.  Utilisez SymStore avec l’option **/p** pour stocker des pointeurs vers les fichiers de symboles. Une fois SymStore terminé, compressez les fichiers auxquels les pointeurs font référence.
2.  Utilisez SymStore avec l’option **/x** pour créer un fichier d’index. Une fois SymStore terminé, compressez les fichiers listés dans le fichier d’index. Utilisez ensuite SymStore avec l’option **/y** (et, si vous le souhaitez, l’option **/p** ) pour stocker les fichiers ou les pointeurs vers les fichiers dans le magasin de symboles. (SymStore n’a pas besoin de décompresser les fichiers pour effectuer cette opération.)

Votre serveur de symboles est chargé de décompresser les fichiers lorsqu’ils sont nécessaires.

Si vous utilisez SymSrv en tant que serveur de symboles, toute compression doit être effectuée à l’aide de l’outil compress.exe qui est distribué avec le kit de développement logiciel (SDK) Microsoft Windows. Les fichiers compressés doivent avoir un trait de soulignement comme dernier caractère dans leurs extensions de fichier (par exemple, Module1. PD \_ ou Module2. db \_ ). Pour plus d’informations, consultez [utilisation de symsrv](using-symsrv.md).

## <a name="the-servertxt-and-historytxt-files"></a>Fichiers server.txt et history.txt

Lorsqu’une transaction est ajoutée, plusieurs éléments d’information sont ajoutés à server.txt et history.txt pour la future capacité de recherche. Voici un exemple de ligne dans server.txt et history.txt pour une transaction Add :

``` syntax
0000000096,add,ptr,10/09/99,00:08:32,Windows XP,x86 fre 1.156c-RTM-2,Added from \\mybuilds\symbols,
```

Il s’agit d’une ligne séparée par des virgules. Les champs sont définis comme suit.



| Champ      | Description                                                                         |
|------------|-------------------------------------------------------------------------------------|
| 0000000096 | Numéro d’identification de la transaction, tel qu’il a été créé par SymStore.                                      |
| add        | Type de transaction. Ce champ peut avoir la valeur **Add** ou **del**.                   |
| ptr        | Indique si des fichiers ou des pointeurs ont été ajoutés. Ce champ peut être un **fichier** ou un **ptr**. |
| 10/09/99   | Date à laquelle la transaction s’est produite.                                                     |
| 00:08:32   | Heure de début de la transaction.                                                      |
| Windows XP | Produit.                                                                            |
| fre x86    | Version (facultatif).                                                                 |
| Ajouté à partir de | Commentaire (facultatif)                                                                  |
| Inutilisé     | (Réservé pour une utilisation ultérieure.)                                                           |



 

Voici quelques exemples de lignes du fichier de transaction 0000000096. Chaque ligne enregistre le répertoire et l’emplacement du fichier ou du pointeur qui a été ajouté au répertoire.

``` syntax
canon800.dbg\35d9fd51b000,\\mybuilds\symbols\sp4\dll\canon800.dbg
canonlbp.dbg\35d9fd521c000,\\mybuilds\symbols\sp4\dll\canonlbp.dbg
certadm.dbg\352bf2f48000,\\mybuilds\symbols\sp4\dll\certadm.dbg
certcli.dbg\352bf2f1b000,\\mybuilds\symbols\sp4\dll\certcli.dbg
certcrpt.dbg\352bf04911000,\\mybuilds\symbols\sp4\dll\certcrpt.dbg
certenc.dbg\352bf2f7f000,\\mybuilds\symbols\sp4\dll\certenc.dbg
```

Si vous utilisez une transaction **del** pour annuler l' **Ajout** de transactions d’origine, ces lignes sont supprimées de server.txt, et la ligne suivante est ajoutée à history.txt :

``` syntax
0000000105,del,0000000096
```

Les champs de la transaction de suppression sont définis comme suit.



| Champ      | Description                                                       |
|------------|-------------------------------------------------------------------|
| 0000000105 | Numéro d’identification de la transaction, tel qu’il a été créé par SymStore.                    |
| del        | Type de transaction. Ce champ peut avoir la valeur **Add** ou **del**. |
| 0000000096 | Transaction qui a été supprimée.                                     |



 

## <a name="symbol-storage-format"></a>Format de stockage des symboles

SymStore utilise le système de fichiers lui-même en tant que base de données. Il crée une grande arborescence de répertoires, avec des noms de répertoires basés sur des horodatages de fichier de symboles, des signatures, de l’âge et d’autres données.

Par exemple, après l’ajout de plusieurs fichiers ACPI. dbg différents au serveur, les répertoires peuvent se présenter comme suit :

``` syntax
Directory of \\mybuilds\symsrv\acpi.dbg
10/06/1999  05:46p      <DIR>          .
10/06/1999  05:46p      <DIR>          ..
10/04/1999  01:54p      <DIR>          37cdb03962040
10/04/1999  01:49p      <DIR>          37cdb04027740
10/04/1999  12:56p      <DIR>          37e3eb1c62060
10/04/1999  12:51p      <DIR>          37e3ebcc27760
10/04/1999  12:45p      <DIR>          37ed151662060
10/04/1999  12:39p      <DIR>          37ed15dd27760
10/04/1999  11:33a      <DIR>          37f03ce962020
10/04/1999  11:21a      <DIR>          37f03cf7277c0
10/06/1999  05:38p      <DIR>          37fa7f00277e0
10/06/1999  05:46p      <DIR>          37fa7f01620a0
```

Dans cet exemple, le chemin de recherche du fichier de symboles ACPI. dbg peut se présenter comme suit : \\ \\ mybuilds \\ symsrv \\ ACPI. dbg \\ 37cdb03962040.

Trois fichiers peuvent se trouver dans le répertoire de recherche :

1.  Si le fichier a été stocké, ACPI. dbg y figure.
2.  Si un pointeur était stocké, un fichier appelé file. PTR existe et contient le chemin d’accès au fichier de symboles réel.
3.  Un fichier appelé refs. PTR, qui contient une liste de tous les emplacements actuels pour ACPI. dbg avec cet horodatage et la taille de l’image qui sont actuellement ajoutés au magasin de symboles.

L’affichage de la liste de répertoires de \\ \\ mybuilds \\ symsrv \\ ACPI. dbg \\ 37cdb03962040 donne ce qui suit :

``` syntax
10/04/1999  01:54p                  52 file.ptr
10/04/1999  01:54p                  67 refs.ptr
```

Le fichier file. PTR contient la chaîne de texte « \\ \\ mybuilds \\ Symbols \\ x86 \\ 2128. chk \\ Symbols \\ sys \\ ACPI. dbg ». Étant donné qu’il n’y a aucun fichier nommé ACPI. dbg dans ce répertoire, le débogueur essaiera de trouver le fichier dans \\ \\ mybuilds \\ Symbols \\ x86 \\ 2128. chk \\ Symbols \\ sys \\ ACPI. dbg.

Le contenu de refs. PTR est utilisé uniquement par SymStore, et non par le débogueur. Ce fichier contient un enregistrement de toutes les transactions qui ont eu lieu dans ce répertoire. Un exemple de ligne de refs. PTR peut être :

``` syntax
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\sys\acpi.dbg
```

Cela montre qu’un pointeur vers \\ \\ mybuilds \\ Symbols \\ x86 \\ 2128. chk \\ Symbols \\ sys \\ ACPI. dbg a été ajouté avec la transaction « 0000000026 ».

Certains fichiers de symboles restent constants par le biais de différents produits ou builds, ou d’un produit particulier. Le fichier Msvcrt. pdb en est un exemple. La réalisation d’un répertoire de \\ \\ mybuilds \\ symsrv \\ Msvcrt. pdb montre que seules deux versions de Msvcrt. pdb ont été ajoutées au serveur de symboles :

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb
10/06/1999  05:37p      <DIR>          .
10/06/1999  05:37p      <DIR>          ..
10/04/1999  11:19a      <DIR>          37a8f40e2
10/06/1999  05:37p      <DIR>          37f2c2272
```

Toutefois, le fait de faire d’un répertoire de \\ \\ mybuilds \\ symsrv \\ Msvcrt. pdb \\ 37a8f40e2 montre que refs. PTR a plusieurs pointeurs dans celui-ci.

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb\37a8f40e2
10/05/1999  02:50p              54     file.ptr
10/05/1999  02:50p           2,039     refs.ptr
```

Le contenu de \\ \\ mybuilds \\ symsrv \\ Msvcrt. pdb \\ 37a8f40e2 \\ refs. PTR est le suivant :

``` syntax
0000000001,ptr,\\mybuilds\symbols\x86\2137\symbols\dll\msvcrt.pdb
0000000002,ptr,\\mybuilds\symbols\x86\2137.chk\symbols\dll\msvcrt.pdb
0000000003,ptr,\\mybuilds\symbols\x86\2138\symbols\dll\msvcrt.pdb
0000000004,ptr,\\mybuilds\symbols\x86\2138.chk\symbols\dll\msvcrt.pdb
0000000005,ptr,\\mybuilds\symbols\x86\2139\symbols\dll\msvcrt.pdb
0000000006,ptr,\\mybuilds\symbols\x86\2139.chk\symbols\dll\msvcrt.pdb
0000000007,ptr,\\mybuilds\symbols\x86\2140\symbols\dll\msvcrt.pdb
0000000008,ptr,\\mybuilds\symbols\x86\2140.chk\symbols\dll\msvcrt.pdb
0000000009,ptr,\\mybuilds\symbols\x86\2136\symbols\dll\msvcrt.pdb
0000000010,ptr,\\mybuilds\symbols\x86\2136.chk\symbols\dll\msvcrt.pdb
0000000011,ptr,\\mybuilds\symbols\x86\2135\symbols\dll\msvcrt.pdb
0000000012,ptr,\\mybuilds\symbols\x86\2135.chk\symbols\dll\msvcrt.pdb
0000000013,ptr,\\mybuilds\symbols\x86\2134\symbols\dll\msvcrt.pdb
0000000014,ptr,\\mybuilds\symbols\x86\2134.chk\symbols\dll\msvcrt.pdb
0000000015,ptr,\\mybuilds\symbols\x86\2133\symbols\dll\msvcrt.pdb
0000000016,ptr,\\mybuilds\symbols\x86\2133.chk\symbols\dll\msvcrt.pdb
0000000017,ptr,\\mybuilds\symbols\x86\2132\symbols\dll\msvcrt.pdb
0000000018,ptr,\\mybuilds\symbols\x86\2132.chk\symbols\dll\msvcrt.pdb
0000000019,ptr,\\mybuilds\symbols\x86\2131\symbols\dll\msvcrt.pdb
0000000020,ptr,\\mybuilds\symbols\x86\2131.chk\symbols\dll\msvcrt.pdb
0000000021,ptr,\\mybuilds\symbols\x86\2130\symbols\dll\msvcrt.pdb
0000000022,ptr,\\mybuilds\symbols\x86\2130.chk\symbols\dll\msvcrt.pdb
0000000023,ptr,\\mybuilds\symbols\x86\2129\symbols\dll\msvcrt.pdb
0000000024,ptr,\\mybuilds\symbols\x86\2129.chk\symbols\dll\msvcrt.pdb
0000000025,ptr,\\mybuilds\symbols\x86\2128\symbols\dll\msvcrt.pdb
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\dll\msvcrt.pdb
0000000027,ptr,\\mybuilds\symbols\x86\2141\symbols\dll\msvcrt.pdb
0000000028,ptr,\\mybuilds\symbols\x86\2141.chk\symbols\dll\msvcrt.pdb
0000000029,ptr,\\mybuilds\symbols\x86\2142\symbols\dll\msvcrt.pdb
0000000030,ptr,\\mybuilds\symbols\x86\2142.chk\symbols\dll\msvcrt.pdb
```

Cela indique que le même fichier Msvcrt. pdb a été utilisé pour plusieurs générations de symboles stockées sur \\ \\ mybuilds \\ symsrv.

Voici un exemple de répertoire contenant un mélange d’ajouts de fichiers et de pointeurs :

``` syntax
Directory of E:\symsrv\dbghelp.dbg\38039ff439000
10/12/1999  01:54p         141,232     dbghelp.dbg
10/13/1999  04:57p              49     file.ptr
10/13/1999  04:57p             306     refs.ptr
```

Dans ce cas, refs. PTR a le contenu suivant :

``` syntax
0000000043,file,e:\binaries\symbols\retail\dll\dbghelp.dbg
0000000044,file,f:\binaries\symbols\retail\dll\dbghelp.dbg
0000000045,file,g:\binaries\symbols\retail\dll\dbghelp.dbg
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

Ainsi, les transactions 43, 44 et 45 ont ajouté le même fichier au serveur, et les transactions 46 et 47 ont ajouté des pointeurs. Si les transactions 43, 44 et 45 sont supprimées, le fichier dbghelp. dbg sera supprimé du répertoire. Le répertoire présente ensuite le contenu suivant :

``` syntax
Directory of e:\symsrv\dbghelp.dbg\38039ff439000
10/13/1999  05:01p                   49 file.ptr
10/13/1999  05:01p                 130 refs.ptr
```

Désormais, file. PTR contient « \\ \\ sampledir2 \\ bin \\ Symbols \\ Retail \\ dll \\ dbghelp. dbg » et refs. PTR contient

``` syntax
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

Chaque fois que l’entrée finale dans refs. PTR est un pointeur, le fichier. PTR existe et contient le chemin d’accès au fichier associé. Chaque fois que l’entrée finale dans refs. PTR est un fichier, aucun fichier. PTR n’existe dans ce répertoire. Par conséquent, toute opération de suppression qui supprime l’entrée finale dans refs. PTR peut entraîner la création, la suppression ou la modification de fichier. ptr.

 

 



