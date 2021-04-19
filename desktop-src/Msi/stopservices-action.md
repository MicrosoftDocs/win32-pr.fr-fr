---
description: L’action StopServices arrête les services système. Cette action interroge la table ServiceControl.
ms.assetid: 1ad01205-f8b6-400f-be1d-c00a5b71ccfd
title: Action StopServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb271b99c434a1ac54ab9744697b991e9e1fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534385"
---
# <a name="stopservices-action"></a>Action StopServices

L’action StopServices arrête les services système. Cette action interroge la [table ServiceControl](servicecontrol-table.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

Les actions des services doivent être utilisées dans l’ordre suivant :

-   StopServices
-   [DeleteServices](deleteservices-action.md)

L’une des actions suivantes :

-   [InstallFiles](installfiles-action.md)
-   [RemoveFiles](removefiles-action.md)
-   [DuplicateFiles](duplicatefiles-action.md)
-   [MoveFiles](movefiles-action.md)
-   [PatchFiles](patchfiles-action.md)
-   [RemoveDuplicateFiles](removeduplicatefiles-action.md)
-   [InstallServices](installservices-action.md)
-   [StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action |
|-------|----------------------------|
| \[1\] | Nom complet du service.      |
| \[2\] | Nom du service              |



 

## <a name="remarks"></a>Notes

Cette action nécessite que l’utilisateur soit un administrateur ou qu’il dispose de privilèges élevés avec l’autorisation de contrôler les services ou que l’application fasse partie d’une installation gérée.

 

 



