---
description: L’événement ValidateProductID affecte l’ID de produit complet à la propriété ProductID. Si la validation échoue, cet événement affiche un message d’erreur et une boîte de dialogue modale pour une entrée utilisateur de l’ID de produit.
ms.assetid: 44002cae-154a-4938-a15c-456c293e94fb
title: ValidateProductID ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ae9ae5747deb9995c2e33a5c44541793442be8844b224c28c8a91e412cb188
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786659"
---
# <a name="validateproductid-controlevent"></a>ValidateProductID ControlEvent,

L’événement ValidateProductID affecte l’ID de produit complet à la propriété [**ProductID**](productid.md) . Si la validation échoue, cet événement affiche un message d’erreur et une boîte de dialogue modale pour une entrée utilisateur de l’ID de produit.

Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md)ou un [contrôle SelectionTree](selectiontree-control.md). Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Aucun.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Aucun.

## <a name="typical-use"></a>Utilisation courante

Un contrôle [PUSHBUTTON](pushbutton-control.md) sur une boîte de dialogue modale est lié à cet événement et est utilisé pour vérifier l’entrée de l’ID de produit de l’utilisateur. Si l’entrée de l’utilisateur est valide, la boîte de dialogue suivante s’ouvre.

 

 



