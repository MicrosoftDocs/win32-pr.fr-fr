---
description: L’action RemoveShortcuts gère la suppression d’un raccourci publié dont la fonctionnalité est sélectionnée pour la désinstallation ou un raccourci non publié dont le composant est sélectionné pour la désinstallation. Pour plus d’informations, consultez le tableau des raccourcis.
ms.assetid: 897e8a13-d9c5-4f98-8785-c0f053a11f3d
title: Action RemoveShortcuts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f01c16845b260502ecd286649c2bf246e86d7247c40f14d840e29f9676004c48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128959"
---
# <a name="removeshortcuts-action"></a>Action RemoveShortcuts

L’action RemoveShortcuts gère la suppression d’un raccourci publié dont la fonctionnalité est sélectionnée pour la désinstallation ou un raccourci non publié dont le composant est sélectionné pour la désinstallation. Pour plus d’informations, consultez le [tableau des raccourcis](shortcut-table.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action RemoveShortcuts doit précéder l’action [CreateShortcuts](createshortcuts-action.md) .

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action      |
|-------|---------------------------------|
| \[1\] | Identificateur du raccourci supprimé. |



 

 

 



