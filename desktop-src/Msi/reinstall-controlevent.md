---
description: Permet à l’auteur de lancer une réinstallation de certaines ou de toutes les fonctionnalités, tandis que la boîte de dialogue active est en cours d’exécution.
ms.assetid: bc667f20-3abe-4ef3-b51e-dc74da63f651
title: Réinstaller ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d2adece3f89dbe57b77f2345d1714ece64b271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527456"
---
# <a name="reinstall-controlevent"></a>Réinstaller ControlEvent,

La réinstallation ControlEventallows l’auteur pour lancer une réinstallation de certaines ou de toutes les fonctionnalités, tandis que la boîte de dialogue active est en cours d’exécution.

Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md) ou un [contrôle SelectionTree](selectiontree-control.md). Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md)et nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une [*interface utilisateur réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez niveaux de l' [interface utilisateur](user-interface-levels.md).

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Chaîne qui est le nom de la fonctionnalité ou « ALL ».

## <a name="action-on-subscribers"></a>Action sur les abonnés

Ce ControlEvent, n’effectue pas d’action sur les abonnés.

## <a name="typical-use"></a>Utilisation courante

Cet événement est lié à un contrôle [PUSHBUTTON](pushbutton-control.md) dans une boîte de dialogue modale. Le même contrôle [PUSHBUTTON](pushbutton-control.md) doit également être lié à un ControlEvent, [ReinstallMode](reinstallmode-controlevent.md) .

 

 



