---
description: Cet événement est publié par le contrôle ScrollableText pour permettre à l’utilisateur d’imprimer le contenu de ce contrôle.
ms.assetid: 8cb91b21-f6db-4f49-827d-1ec739ff4f45
title: MsiPrint ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0dd876f1a98e68c6ad61c7c122e1b51fa9c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868645"
---
# <a name="msiprint-controlevent"></a>MsiPrint ControlEvent,

Cet événement est publié par le [contrôle ScrollableText](scrollabletext-control.md) pour permettre à l’utilisateur d’imprimer le contenu de ce contrôle.

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge. Ce ControlEvent, est disponible à partir de Windows Installer 5,0.

Cet événement doit être souscrit par un [contrôle PUSHBUTTON](pushbutton-control.md) situé dans la même boîte de dialogue que le [contrôle ScrollableText](scrollabletext-control.md). TheMsiPrint ControlEvent, doit être créé dans la [table ControlEvent,](controlevent-table.md).

## <a name="published-by"></a>Publié par

[ScrollableText](scrollabletext-control.md)

## <a name="argument"></a>Argument

Ce ControlEvent, n’utilise pas d’argument.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Ce ControlEvent, n’effectue pas d’action sur les abonnés.

## <a name="typical-use"></a>Utilisation courante

Un contrôle [PUSHBUTTON](pushbutton-control.md) dans la même boîte de dialogue que le [contrôle ScrollableText](scrollabletext-control.md) peut être utilisé pour afficher une boîte de dialogue modale permettant à l’utilisateur d’imprimer le contenu du contrôle ScrollableText.

 

 



