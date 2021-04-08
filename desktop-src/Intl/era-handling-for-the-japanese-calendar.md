---
description: Gestion d’ères pour le calendrier japonais
ms.assetid: a1dabf7c-6521-492e-bdc0-27cfb07cfc20
title: Gestion d’ères pour le calendrier japonais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eba757745bf0d90d119c821772c7fc23f3f8694b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867926"
---
# <a name="era-handling-for-the-japanese-calendar"></a>Gestion d’ères pour le calendrier japonais

De nombreux calendriers ont des ères, comme AD/BC ou CE/BCE. Dans le calendrier japonais, les années sont décrites par nengō, une combinaison du numéro d’année et du nom de l’ère. Par exemple, 2009 est Heisei 21. Dans le passé, les noms des ères Japonais changent fréquemment, mais à présent, la modification du japonais ne change que sur la succession du impérial. Windows et Microsoft .NET ont pris en charge historiquement les quatre ères modernes dans le cadre de cette stratégie : Meiji, Taishō, Shōwa et Heisei.

Avec Windows 7, Windows Server 2008 R2 et le .NET Framework 4, Microsoft reconnaît que des ères supplémentaires peuvent être ajoutées à l’avenir. Sur ces versions de Windows, les données de l’ère sont stockées dans le Registre sous la clé :<dl> HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ contrôler \\ les \\ calendriers nls \\ japonais \\ ères  
</dl>

Si nécessaire, des ères supplémentaires peuvent être ajoutées à cette clé par le biais du processus de Windows Update normal. Cette clé peut être affichée à l’aide de l’éditeur du Registre (Regedit.exe). Voici un exemple de la clé et des valeurs fournies dans Windows 7 :

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"1868 01 01"="明治_明_Meiji_M"
"1912 07 30"="大正_大_Taisho_T"
"1926 12 25"="昭和_昭_Showa_S"
"1989 01 08"="平成_平_Heisei_H"
```

Le nom de chaque valeur d’ère correspond à la date de début de l’ère dans le calendrier grégorien. La valeur contient le nom de l’ère en japonais, le nom abrégé en japonais, le nom en anglais et un nom abrégé en anglais :<dl> « YYYY MM JJ » = « JE \_ AJE \_ EE \_ AEE »  
</dl>where

-   « YYYY MM JJ » est la date grégorienne du début de l’ère dans l’année, le mois, le formulaire de jour où Year est 4 chiffres, Day est 2 chiffres et month est également 2 chiffres. Un espace sépare chaque partie de la date.
-   « JE suis » est le nom japonais de l’ère et est suivi d’un trait de soulignement.
-   « AJE » est le nom abrégé de l’ère, en japonais, et est suivi d’un trait de soulignement.
-   « EE » est le nom anglais de l’ère japonaise et est suivi d’un trait de soulignement.
-   « AEE » est le nom anglais abrégé de l’ère japonaise.

L’un des points à prendre en compte pour les développeurs d’applications est la possibilité que des ères supplémentaires soient ajoutées par Windows Update ou d’autres moyens. Dans ce cas, l’application peut rencontrer plus que les quatre ères attendues pour le calendrier japonais. À des fins de test, les testeurs peuvent ajouter une ère supplémentaire au registre ; Toutefois, cela doit être limité aux ordinateurs de test uniquement, car il affecte le comportement de l’ordinateur entier.

Voici un exemple d’une telle clé qui peut être utilisée pour le test. Cette modification peut être effectuée à l’aide de l’éditeur du Registre. (Il s’agit d’un exemple pour une utilisation de test uniquement et n’est pas destiné à prédire les ajouts ultérieurs.)

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"2020 09 01"="仮名_仮_Test Era_X"
```

Notez que cela affecte uniquement les ordinateurs qui exécutent Windows 7 et versions ultérieures ou .NET Framework 4 et versions ultérieures. Les développeurs d’applications sont encouragés à tester leurs applications avec des ères de test supplémentaires pour s’assurer que leurs applications continuent de fonctionner si des ères supplémentaires sont ajoutées à une date ultérieure.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Récupération des informations de date et d’heure](retrieving-time-and-date-information.md)
</dt> <dt>

[Identificateurs de calendrier](calendar-identifiers.md)
</dt> </dl>

 

 



