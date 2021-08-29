---
description: Le programme d’installation est averti par le biais de cet événement lorsqu’une fonctionnalité ou toutes les fonctionnalités sont sélectionnées en vue de leur suppression tout en conservant l’exécution de la boîte de dialogue actuelle.
ms.assetid: dabe44f7-97dd-4037-80e5-f289bab6d4b3
title: Supprimer ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59a22ab4fc321ceaf661aed1ba37970806beb8afe87e90ee9dbc59fa52e8fae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821379"
---
# <a name="remove-controlevent"></a>Supprimer ControlEvent,

Le programme d’installation est averti par le biais de cet événement lorsqu’une fonctionnalité ou toutes les fonctionnalités sont sélectionnées en vue de leur suppression tout en conservant l’exécution de la boîte de dialogue actuelle.

Cet événement peut être publié par un contrôle de [bouton](pushbutton-control.md)de commande, un [contrôle de case à cocher](checkbox-control.md)ou un [contrôle SelectionTree](selectiontree-control.md). Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Chaîne qui est le nom de la fonctionnalité ou « ALL ».

## <a name="action-on-subscribers"></a>Action sur les abonnés

Ce ControlEvent, n’effectue pas d’action sur les abonnés.

## <a name="action-by-publisher-when-subscriber-activated"></a>Action par Publisher lors de l’activation de l’abonné

Le programme d’installation conserve la boîte de dialogue actuelle en cours d’exécution et notifie le programme d’installation.

## <a name="typical-use"></a>Utilisation courante

Contrôle [PUSHBUTTON](pushbutton-control.md) sur une boîte de dialogue modale liée à cet événement.

 

 



