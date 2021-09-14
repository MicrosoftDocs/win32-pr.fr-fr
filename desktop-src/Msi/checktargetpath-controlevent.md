---
description: Cet événement indique au programme d’installation qu’il doit vérifier que le chemin d’accès sélectionné est valide. Si le chemin d’accès n’est pas valide, cet événement bloque tout autre ControlEvents associé au contrôle.
ms.assetid: b7c1de6e-5738-4ecb-a033-9379d79dddb9
title: CheckTargetPath ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49301dbe1fcc6becc1bc757a0fe487061e1dcdbd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092249"
---
# <a name="checktargetpath-controlevent"></a>CheckTargetPath ControlEvent,

Cet événement indique au programme d’installation qu’il doit vérifier que le chemin d’accès sélectionné est valide. Si le chemin d’accès n’est pas valide, cet événement bloque tout autre ControlEvents associé au contrôle.

Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md)ou un [contrôle SelectionTree](selectiontree-control.md). Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Nom de la propriété contenant le chemin d’accès. Si la propriété est indirecte, le nom de la propriété est placé entre crochets.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Ce ControlEvent, n’effectue pas d’action sur les abonnés.

## <a name="typical-use"></a>Utilisation courante

Un contrôle [PUSHBUTTON](pushbutton-control.md) sur une boîte de dialogue de navigation est lié à cet événement dans la table [ControlEvent,](controlevent-table.md) pour vérifier le chemin d’accès sélectionné avant de revenir à la boîte de dialogue de sélection.

 

 



