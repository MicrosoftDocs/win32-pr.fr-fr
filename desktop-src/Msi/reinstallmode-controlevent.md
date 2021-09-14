---
description: Permet à l’auteur de spécifier le ou les modes de validation lors d’une réinstallation, et Pendant l’exécution de la boîte de dialogue active.
ms.assetid: d7cd41c6-c019-49d6-b593-a1d31c8f5a81
title: ReinstallMode ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ff5ff662b2880a3f4ab0fb79738b49cdeeccd3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009669"
---
# <a name="reinstallmode-controlevent"></a>ReinstallMode ControlEvent,

Le ReinstallMode ControlEventallows l’auteur pour spécifier le ou les modes de validation lors d’une réinstallation, et Pendant l’exécution de la boîte de dialogue active.

Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md) ou un [contrôle SelectionTree](selectiontree-control.md). Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md)et nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une [*interface utilisateur réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez niveaux de l' [interface utilisateur](user-interface-levels.md).

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Chaîne. Pour obtenir la liste des valeurs possibles, consultez [**REINSTALLMODE**](reinstallmode.md) , propriété.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Ce ControlEvent, n’effectue pas d’action sur les abonnés.

## <a name="typical-use"></a>Utilisation courante

Cet événement est lié à un contrôle [PUSHBUTTON](pushbutton-control.md) dans une boîte de dialogue modale. Le même contrôle [PUSHBUTTON](pushbutton-control.md) doit également être lié à un ControlEvent, de [réinstallation](reinstall-controlevent.md) .

 

 



