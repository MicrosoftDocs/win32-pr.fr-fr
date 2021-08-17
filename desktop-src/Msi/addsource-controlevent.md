---
description: Cet événement notifie le programme d’installation, tout en conservant l’exécution de la boîte de dialogue actuelle, qu’une fonctionnalité ou toutes les fonctionnalités doivent être exécutées à partir de la source.
ms.assetid: fd8d6433-87cc-4544-9f4f-57a90e5f2ea5
title: AddSource ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0adff72ac14376c7084d6c3c005a77b2891019947cd22e8d73e58bfa09ad64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145952"
---
# <a name="addsource-controlevent"></a>AddSource ControlEvent,

Cet événement notifie le programme d’installation, tout en conservant l’exécution de la boîte de dialogue actuelle, qu’une fonctionnalité ou toutes les fonctionnalités doivent être exécutées à partir de la source. Cet événement peut être publié par un contrôle de [bouton](pushbutton-control.md)de commande, un [contrôle de case à cocher](checkbox-control.md)ou un [contrôle SelectionTree](selectiontree-control.md). Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Chaîne, soit le nom de la fonctionnalité, soit « ALL ».

## <a name="action-on-subscribers"></a>Action sur les abonnés

Ce ControlEvent, n’effectue pas d’action sur les abonnés.

## <a name="typical-use"></a>Utilisation courante

Un contrôle [PUSHBUTTON](pushbutton-control.md) sur une boîte de dialogue modale est lié à cet événement et utilisé pour notifier le programme d’installation sans arrêter la boîte de dialogue.

 

 



