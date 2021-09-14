---
description: L’action RemoveShortcuts gère la suppression d’un raccourci publié dont la fonctionnalité est sélectionnée pour la désinstallation ou un raccourci non publié dont le composant est sélectionné pour la désinstallation. Pour plus d’informations, consultez le tableau des raccourcis.
ms.assetid: 897e8a13-d9c5-4f98-8785-c0f053a11f3d
title: Action RemoveShortcuts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151f5fac6733e61b7ba27320a5e79c522abcc3e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195371"
---
# <a name="removeshortcuts-action"></a>Action RemoveShortcuts

L’action RemoveShortcuts gère la suppression d’un raccourci publié dont la fonctionnalité est sélectionnée pour la désinstallation ou un raccourci non publié dont le composant est sélectionné pour la désinstallation. Pour plus d’informations, consultez le [tableau des raccourcis](shortcut-table.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action RemoveShortcuts doit précéder l’action [CreateShortcuts](createshortcuts-action.md) .

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action      |
|-------|---------------------------------|
| \[1\] | Identificateur du raccourci supprimé. |



 

 

 



