---
description: 'Il existe deux types de pinceaux : logique et physique.'
ms.assetid: 2e15376d-6b4c-41c5-aef8-0dbb91b81505
title: À propos des pinceaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c825892748b317807377bff12675ea04d2d2535
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114250"
---
# <a name="about-brushes"></a>À propos des pinceaux

Il existe deux types de pinceaux : logique et physique. Un *pinceau logique* est une description de la bitmap idéale qu’une application utilise pour peindre des formes. Un *pinceau physique* est le bitmap réel créé par un pilote de périphérique en fonction de la définition du pinceau logique d’une application. Pour plus d’informations sur les bitmaps, consultez [bitmaps](bitmaps.md).

Quand une application appelle l’une des fonctions qui crée un pinceau, elle récupère un handle qui identifie un pinceau logique. Lorsque l’application transmet ce descripteur à la fonction [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) , le pilote de périphérique pour l’affichage ou l’imprimante correspondante crée le pinceau physique.

Les rubriques suivantes décrivent les pinceaux :

-   [Origine du pinceau](brush-origin.md)
-   [Types Brush logiques](logical-brush-types.md)
-   [Transfert de bloc de modèle](pattern-block-transfer.md)
-   [Fonctions de brosse compatibles ICM](icm-enabled-brush-functions.md)

 

 



