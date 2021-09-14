---
description: ICE26 valide les tables de séquence dans une base de données Windows Installer.
ms.assetid: 7ea47452-3147-4d39-961d-a10eca8328c9
title: ICE26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7b110d0b15b37441170980d0fd3e96e2eb00d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021587"
---
# <a name="ice26"></a>ICE26

ICE26 vérifie que chacune des [*tables de séquence*](s-gly.md) suivantes contient les actions requises par la table et qu’elle ne contient aucune action interdite dans la table :

-   [Table AdminUISequence](adminuisequence-table.md)
-   [Table AdminExecuteSequence](adminexecutesequence-table.md)
-   [Table InstallUISequence](installuisequence-table.md)
-   [Table InstallExecuteSequence](installexecutesequence-table.md)

## <a name="result"></a>Résultats

ICE26 publie un message d’erreur si le package d’installation a une table de séquences qui n’a pas d’action requise ou qui contient une action qui n’est pas autorisée pour la table.

## <a name="example"></a>Exemple



| Erreur ICE26                                                                   | Description                                                                                                                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Action : 'action1 'est obligatoire dans la table de séquences InstallExecuteSequence.   | Une action requise est absente de la table de séquences indiquée. Consultez le template.msi ou les tables de séquence suggérées dans [à l’aide d’une table de séquences](using-a-sequence-table.md). |
| Action : 'action2 'est interdit dans la table de séquences InstallExecuteSequence. | Cette action ne peut pas figurer dans la table de séquence indiquée. Supprimez cette action de la table Sequence.                                                                             |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



