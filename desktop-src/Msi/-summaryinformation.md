---
description: La \_ table SummaryInformation est une table spéciale utilisée avec le flux d’informations de synthèse. Vous pouvez obtenir ou définir le flux d’informations de synthèse d’une base de données Windows Installer en exportant ou en important un fichier d’archive de texte nommé \_ SummaryInformation. IDT.
ms.assetid: b1b42e03-7a05-46d4-9c42-b87906535adb
title: _SummaryInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803b89223db8b6fc8074336109221a8300f7c1ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519662"
---
# <a name="_summaryinformation"></a>\_SummaryInformation

La \_ table SummaryInformation est une table spéciale utilisée avec le [flux d’informations de synthèse](summary-information-stream.md). Vous pouvez obtenir ou définir le flux d’informations de synthèse d’une base de données Windows Installer en exportant ou en important un [fichier d’archive de texte](text-archive-files.md) nommé \_ SummaryInformation. IDT.

Le fichier. IDT d’une table SummaryInformation exportée \_ a le format suivant.

-   La première ligne contient les noms de colonnes de table séparés par des tabulations : PropertyId et value. Pour obtenir la liste des propriétés et de leurs ID (PID), consultez la rubrique [Propriétés du flux d’informations de synthèse](summary-information-stream-property-set.md) .
-   La deuxième ligne contient les définitions de colonne séparées par des tabulations. Les définitions de colonne sont spécifiées de la même façon que dans le [format de fichier d’archive](archive-file-format.md)Basic. IDT. La colonne PropertyId peut être un entier Short non Nullable. La colonne valeur peut être une chaîne non Nullable de 255 caractères de long.
-   La troisième ligne est le nom de la table et le nom de la colonne de clé primaire, séparés par des tabulations : \_ SummaryInformation et PropertyId.
-   Les lignes restantes dans le fichier représentent le PID et la valeur associée, séparés par des tabulations. La date et l’heure dans \_ SummaryInformation sont au format suivant : aaaa/mm/jj hh :: mm :: SS. Par exemple, 1999/03/22 15:25:45.

Voici un exemple de [flux d’informations résumées](summary-information-stream.md) d’une base de données au format. IDT.

``` syntax
PropertyId   Value
i2  l255
_SummaryInformation PropertyId
1   1252
2   Installation Database
3   Internal Quick Test
4   Microsoft Corporation
5   Installer,MSI,Database
6   Installer Internal Release Quick Test
7   Intel;1033
9   {00000002-0001-0000-0000-624474736554}
12  1999/06/21
14  110
15  1
18  Windows Installer
```

Lorsque vous utilisez [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) ou la méthode [Import](database-import.md) de l’objet [**Database**](database-object.md) pour importer une table d’archive de texte nommée \_ SummaryInformation dans une base de données du programme d’installation, vous écrivez le flux « 05SummaryInformation » dans la base de données.

 

 



