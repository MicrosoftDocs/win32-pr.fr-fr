---
description: L’action InstallServices inscrit un service pour le système. Cette action interroge la table ServiceInstall.
ms.assetid: bb394cdb-1310-44fb-b7e1-2ffbb976d438
title: Action InstallServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e37ea0a80050d6e9ab624ff878a352f96bbc0854fd64d6a1f563f277f1ea6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787019"
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

## <a name="remarks"></a>Remarques

Cette action nécessite que l’utilisateur soit un administrateur ou qu’il dispose de privilèges élevés avec l’autorisation d’installer des services ou que l’application fasse partie d’une installation gérée.

 

 



