---
description: L’action InstallServices inscrit un service pour le système. Cette action interroge la table ServiceInstall.
ms.assetid: bb394cdb-1310-44fb-b7e1-2ffbb976d438
title: Action InstallServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5964deb08f811e391418211efc6f774261bd87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530906"
---
# <a name="installservices-action"></a>Action InstallServices

L’action InstallServices inscrit un service pour le système. Cette action interroge la [table ServiceInstall](serviceinstall-table.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action services doit être utilisée dans l’ordre suivant.

[StopServices](stopservices-action.md)

[DeleteServices](deleteservices-action.md)

L’une des actions suivantes : les actions [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)et [RemoveDuplicateFiles](removeduplicatefiles-action.md) .

InstallServices

[StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Notes

Cette action nécessite que l’utilisateur soit un administrateur ou qu’il dispose de privilèges élevés avec l’autorisation d’installer des services ou que l’application fasse partie d’une installation gérée.

 

 



