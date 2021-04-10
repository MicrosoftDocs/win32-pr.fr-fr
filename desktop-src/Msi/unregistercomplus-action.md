---
description: L’action UnregisterComPlus supprime les applications COM+ du Registre.
ms.assetid: bcedc436-a048-487e-9a84-e766da57a0b3
title: Action UnregisterComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e32d39255229151757f7d6be0ada871f555f77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953166"
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

[Installation d’une application COM+ avec la Windows Installer](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



