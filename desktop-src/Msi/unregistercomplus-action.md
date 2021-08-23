---
description: L’action UnregisterComPlus supprime les applications COM+ du Registre.
ms.assetid: bcedc436-a048-487e-9a84-e766da57a0b3
title: Action UnregisterComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc3ed5e8e4afd853294e7f5832662e9aaf1eb122d3573e7c384115c86d994588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499849"
---
# <a name="unregistercomplus-action"></a>Action UnregisterComPlus

L’action UnregisterComPlus supprime les applications COM+ du Registre.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action [RegisterComPlus](registercomplus-action.md) doit suivre l' [action InstallFiles](installfiles-action.md) et l’action UnregisterComPlus.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                                    |
|-------|---------------------------------------------------------------|
| \[1\] | Identificateur d’application de l’application COM+ en cours de suppression. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Action RegisterComPlus](registercomplus-action.md)
</dt> <dt>

[Table ComPlus](complus-table.md)
</dt> <dt>

[installation d’une Application COM+ avec la Windows Installer](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



