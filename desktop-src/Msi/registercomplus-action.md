---
description: L’action RegisterComPlus inscrit des applications COM+.
ms.assetid: e42bb993-7079-4d5b-bb2e-c958e99e705e
title: Action RegisterComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046d1f40293888d3a1be48a3c55fd5082b6073828c8d5cc7d34c464556986d4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082639"
---
# <a name="registercomplus-action"></a>Action RegisterComPlus

L’action RegisterComPlus inscrit des applications COM+.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action RegisterComPlus doit suivre l' [action InstallFiles](installfiles-action.md) et l' [action UnregisterComPlus](unregistercomplus-action.md).

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action              |
|-------|-----------------------------------------|
| \[1\] | ID d’application de l’application COM+. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Table ComPlus](complus-table.md)
</dt> <dt>

[Action UnregisterComPlus](unregistercomplus-action.md)
</dt> <dt>

[installation d’une Application COM+ avec la Windows Installer](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



