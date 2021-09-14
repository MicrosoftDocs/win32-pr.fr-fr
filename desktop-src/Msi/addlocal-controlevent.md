---
description: Cet événement notifie le programme d’installation, tout en conservant l’exécution de la boîte de dialogue actuelle, qu’une fonctionnalité ou toutes les fonctionnalités doivent être exécutées localement.
ms.assetid: 074f347e-37d3-4365-a25d-caa0392a0dbc
title: AddLocal ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 112975d31e341c06a21609b173b9682283e71610
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092805"
---
# <a name="addlocal-controlevent"></a>AddLocal ControlEvent,

Cet événement notifie le programme d’installation, tout en conservant l’exécution de la boîte de dialogue actuelle, qu’une fonctionnalité ou toutes les fonctionnalités doivent être exécutées localement. Cet événement peut être publié par un contrôle de [bouton](pushbutton-control.md)de commande, un [contrôle de case à cocher](checkbox-control.md)ou un [contrôle SelectionTree](selectiontree-control.md). Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Chaîne, soit le nom de la fonctionnalité, soit « ALL ».

## <a name="action-on-subscribers"></a>Action sur les abonnés

Ce ControlEvent, n’effectue pas d’action sur les abonnés.

## <a name="typical-use"></a>Utilisation courante

Un contrôle [PUSHBUTTON](pushbutton-control.md) sur une boîte de dialogue modale est lié à cet événement et utilisé pour notifier le programme d’installation sans arrêter la boîte de dialogue.

 

 



