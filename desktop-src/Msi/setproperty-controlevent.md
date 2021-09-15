---
description: 'La syntaxe de l’événement SetProperty est différente de celle d’autres ControlEvents à la place du nom de l’événement 1 place la propriété entre crochets : \[ nom de la propriété \_ \] .'
ms.assetid: a8e80d14-8d62-4398-9e53-9a0119a62d70
title: ControlEvent, SetProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59326ddd9f576b4871de7c232318ffcdcdb4fb36
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238625"
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

 

 



