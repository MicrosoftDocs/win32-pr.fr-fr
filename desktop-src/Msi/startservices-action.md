---
description: L’action StartServices démarre les services système. Cette action interroge la table ServiceControl.
ms.assetid: 53791b1c-5fd5-45d8-817b-098566ab4f9c
title: Action StartServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100ff7b927eb4bc157530cebe9767ef7a434d92f0b72f9e6c799b02a2969f5b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627529"
---
# <a name="startservices-action"></a>Action StartServices

L’action StartServices démarre les services système. Cette action interroge la [table ServiceControl](servicecontrol-table.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

Les actions des services doivent être utilisées dans l’ordre suivant :

-   [StopServices](stopservices-action.md)
-   [DeleteServices](deleteservices-action.md)

L’une des actions suivantes :

-   [InstallFiles](installfiles-action.md)
-   [RemoveFiles](removefiles-action.md)
-   [DuplicateFiles](duplicatefiles-action.md)
-   [MoveFiles](movefiles-action.md)
-   [PatchFiles](patchfiles-action.md)
-   [RemoveDuplicateFiles](removeduplicatefiles-action.md)
-   [InstallServices](installservices-action.md)
-   StartServices

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action |
|-------|----------------------------|
| \[1\] | Nom complet du service.      |
| \[2\] | Nom du service              |



 

## <a name="remarks"></a>Remarques

Cette action nécessite que l’utilisateur soit un administrateur ou qu’il dispose de privilèges élevés avec l’autorisation de contrôler les services ou que l’application fasse partie d’une installation gérée.

 

 



