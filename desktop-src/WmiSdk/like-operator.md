---
description: L’opérateur LIKE détermine si une chaîne de caractères correspond à un modèle spécifié.
ms.assetid: 6cafe696-891d-4b17-8802-4b872f76fc78
ms.tgt_platform: multiple
title: LIKE, opérateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e5df500091fac8b15bcdcb448b7a97fc00dc62807ba854757e447f07e6f4e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317868"
---
# <a name="like-operator"></a>LIKE, opérateur

L’opérateur LIKE détermine si une chaîne de caractères correspond à un modèle spécifié. Le modèle spécifié peut contenir exactement les caractères à faire correspondre, ou il peut contenir des caractères méta. En effet, l’opérateur LIKE met en correspondance les sous-chaînes à l’aide des caractères génériques figurant dans le tableau suivant.



| Caractère       | Description                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[ \]           | N’importe quel caractère dans la plage spécifiée ( \[ a-f \] ) ou Set ( \[ abcdef \] ).                                                                                                                 |
| ^               | N’importe quel caractère ne figurant pas dans la plage ( \[ ^ a-f \] ) ou défini ( \[ ^ abcdef \] .)                                                                                                                     |
| %               | Toute chaîne de 0 (zéro) ou plusieurs caractères. L’exemple suivant recherche toutes les instances où « Win » est trouvé n’importe où dans le nom de la classe : `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"` |
| \_ (trait de soulignement) | N’importe quel caractère. Tout trait de soulignement littéral utilisé dans la chaîne de requête doit être placé dans une séquence d’échappement en le plaçant à l’intérieur de \[ \] (crochets).                                                             |



 

Par exemple, le code PowerShell suivant récupère toutes les instances de la classe **Win32 \_ OperatingSystem** dont la propriété **Name** commence par **FirstName**:

`Get-WmiObject win32_computerSystem -filter "Name LIKE 'FirstName%'"`

Étant donné que le trait de soulignement est un caractère méta, si la cible de la requête a un trait de soulignement, les \[ \] caractères d’échappement «» doivent l’entourer. Par exemple, vous pouvez interroger toutes les classes qui ont un double trait de soulignement dans le nom.

Pour rechercher toutes les classes avec un trait de soulignement double dans le nom, vous devez échapper les deux traits de soulignement avec \[ \] (crochets), par exemple :

`SELECT * FROM meta_class WHERE __CLASS LIKE "%[_][_]%"`

Vous pouvez nier une instruction LIKE à l’aide de NOT ; pour ce faire, veillez à placer le non directement devant le nom du champ. Par exemple :

`  Get-WmiObject -computerName "." -query 'Select * FROM Win32_Printer WHERE Local="TRUE"      AND Network ="False" AND DriverName LIKE "%HP%"      AND NOT PortName LIKE "%10.%" AND NOT PortName LIKE "%\\%"'`

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Opérateurs WQL](wql-operators.md)
</dt> </dl>

 

 



