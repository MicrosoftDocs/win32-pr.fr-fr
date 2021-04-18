---
description: La boîte de dialogue est réinitialisée. En d’autres termes, tous les contrôles de la boîte de dialogue sont appelés pour annuler les modifications apportées aux propriétés. Cet événement réinitialise toutes les valeurs de propriété en fonction de ce qu’elles étaient lors de la création de la boîte de dialogue.
ms.assetid: 6449abb8-54cb-4400-9eb2-b7e7f1564747
title: Réinitialiser ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889f1b0f984f14b7522707db4ffbd958bff9c32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526124"
---
# <a name="reset-controlevent"></a>Réinitialiser ControlEvent,

La boîte de dialogue est réinitialisée. En d’autres termes, tous les contrôles de la boîte de dialogue sont appelés pour annuler les modifications apportées aux propriétés. Cet événement réinitialise toutes les valeurs de propriété en fonction de ce qu’elles étaient lors de la création de la boîte de dialogue.

Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md)ou un [contrôle SelectionTree](selectiontree-control.md). Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

Il y a un cas, qui doit se produire rarement en pratique, qui n’est pas géré correctement par ce ControlEvent,. Si deux contrôles ou plus de la même boîte de dialogue sont liés indirectement à la même propriété et qu’au moins l’un d’eux a démarré avec une autre propriété, cette valeur de propriété sera parfois réinitialisée à sa seconde valeur.

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Aucun

## <a name="action-on-subscribers"></a>Action sur les abonnés

Aucun

## <a name="typical-use"></a>Utilisation courante

Un contrôle [PUSHBUTTON](pushbutton-control.md) dans une boîte de dialogue modale permet de réinitialiser toutes les valeurs de la boîte de dialogue et d’annuler toutes les modifications apportées à la page.

 

 



