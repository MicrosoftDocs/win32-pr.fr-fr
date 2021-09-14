---
description: L’action DeleteServices arrête un service et supprime son inscription du système. Cette action interroge la table ServiceControl.
ms.assetid: c7976de9-65f4-4552-8f8c-e7a32ef4821d
title: Action DeleteServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c5fc22bbb0c11cd546f1ffbb9f3ad98e06efae3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091634"
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



 

## <a name="remarks"></a>Notes

Cette action nécessite que l’utilisateur soit un administrateur ou qu’il dispose de privilèges élevés avec l’autorisation de supprimer des services ou que l’application fasse partie d’une installation gérée.

 

 



