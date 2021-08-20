---
description: L’action DeleteServices arrête un service et supprime son inscription du système. Cette action interroge la table ServiceControl.
ms.assetid: c7976de9-65f4-4552-8f8c-e7a32ef4821d
title: Action DeleteServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd00b9d077239402817bdf40dc10ee1de9bdbff4b52998742434933c3e9dd8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379115"
---
# <a name="deleteservices-action"></a>Action DeleteServices

L’action DeleteServices arrête un service et supprime son inscription du système. Cette action interroge la [table ServiceControl](servicecontrol-table.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

Les actions des services doivent être utilisées dans l’ordre suivant :

1.  [StopServices](stopservices-action.md)
2.  DeleteServices
3.  L’une des actions suivantes : les actions [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)et [RemoveDuplicateFiles](removeduplicatefiles-action.md) .
4.  [Action InstallServices](installservices-action.md)
5.  [StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action |
|-------|----------------------------|
| \[1\] | Nom complet du service.      |
| \[2\] | Nom du service              |



 

## <a name="remarks"></a>Remarques

Cette action nécessite que l’utilisateur soit un administrateur ou qu’il dispose de privilèges élevés avec l’autorisation de supprimer des services ou que l’application fasse partie d’une installation gérée.

 

 



