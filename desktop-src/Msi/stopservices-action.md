---
description: L’action StopServices arrête les services système. Cette action interroge la table ServiceControl.
ms.assetid: 1ad01205-f8b6-400f-be1d-c00a5b71ccfd
title: Action StopServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fee0082d1588c3a1486b51bd4f06869374e1f6babfa71d309d65512e1ff1b0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627379"
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



 

## <a name="remarks"></a>Remarques

Cette action nécessite que l’utilisateur soit un administrateur ou qu’il dispose de privilèges élevés avec l’autorisation de contrôler les services ou que l’application fasse partie d’une installation gérée.

 

 



