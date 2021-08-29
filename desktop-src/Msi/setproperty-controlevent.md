---
description: 'La syntaxe de l’événement SetProperty est différente de celle d’autres ControlEvents à la place du nom de l’événement 1 place la propriété entre crochets : \[ nom de la propriété \_ \] .'
ms.assetid: a8e80d14-8d62-4398-9e53-9a0119a62d70
title: ControlEvent, SetProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 850048ab550ea091fcd714835546305b81cdd001efd15e1f55f46f924b3a0308
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628609"
---
# <a name="setproperty-controlevent"></a>ControlEvent, SetProperty

La syntaxe de l’événement SetProperty est différente de celle d’autres ControlEvents à la place du nom de l’événement 1 place la propriété entre crochets : \[ nom de la propriété \_ \] . L’argument est la nouvelle valeur de la propriété. Pour annuler la propriété, l’argument doit avoir la valeur {} . Cela est nécessaire, car l’argument est une clé primaire dans la table et ne peut pas être null. L’argument sera mis en forme à l’aide de la méthode FormatText. par conséquent, l’argument peut contenir toute expression que la méthode FormatText peut gérer. Les valeurs de propriété sont évaluées au moment de l’ControlEvent,.

Cet événement peut être publié par un contrôle de [bouton](pushbutton-control.md)de commande, un [contrôle de case à cocher](checkbox-control.md)ou un [contrôle SelectionTree](selectiontree-control.md). Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Nouvelle valeur de la propriété. {} pour null.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Aucun.

## <a name="typical-use"></a>Utilisation courante

Contrôle [PUSHBUTTON](pushbutton-control.md) sur une boîte de dialogue liée à cet événement pour qu’il modifie une propriété lorsque le bouton fait l’objet d’un push.

 

 



