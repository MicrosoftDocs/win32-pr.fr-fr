---
description: Cet événement est publié par le contrôle ScrollableText pour permettre à l’utilisateur d’imprimer le contenu de ce contrôle.
ms.assetid: 8cb91b21-f6db-4f49-827d-1ec739ff4f45
title: MsiPrint ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbd2107e4930e7d2d410846f656f25143926f8675f354976d866b2ee5d547b0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519779"
---
# <a name="msiprint-controlevent"></a>MsiPrint ControlEvent,

Cet événement est publié par le [contrôle ScrollableText](scrollabletext-control.md) pour permettre à l’utilisateur d’imprimer le contenu de ce contrôle.

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge. ce controlevent, est disponible à partir de Windows Installer 5,0.

Cet événement doit être souscrit par un [contrôle PUSHBUTTON](pushbutton-control.md) situé dans la même boîte de dialogue que le [contrôle ScrollableText](scrollabletext-control.md). TheMsiPrint ControlEvent, doit être créé dans la [table ControlEvent,](controlevent-table.md).

## <a name="published-by"></a>Publié par

[ScrollableText](scrollabletext-control.md)

## <a name="argument"></a>Argument

Ce ControlEvent, n’utilise pas d’argument.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Ce ControlEvent, n’effectue pas d’action sur les abonnés.

## <a name="typical-use"></a>Utilisation courante

Un contrôle [PUSHBUTTON](pushbutton-control.md) dans la même boîte de dialogue que le [contrôle ScrollableText](scrollabletext-control.md) peut être utilisé pour afficher une boîte de dialogue modale permettant à l’utilisateur d’imprimer le contenu du contrôle ScrollableText.

 

 



