---
description: L’action RegisterComPlus inscrit des applications COM+.
ms.assetid: e42bb993-7079-4d5b-bb2e-c958e99e705e
title: Action RegisterComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb824d67e776a99f8cd05c56f73f171f436c71d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115502"
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

[Installation d’une application COM+ avec la Windows Installer](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



