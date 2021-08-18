---
description: Le rectangle englobant de toutes les analyses est l’écran virtuel. Le bureau couvre l’écran virtuel au lieu d’un seul moniteur. L’illustration suivante montre une organisation possible de trois analyses.
ms.assetid: 3f84027d-f316-4454-92ad-2d36d10b2ec8
title: Écran virtuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5516ef0cb5d99124200ab7810e484ea79027cf832a0e8da74833bf709ce5cc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037517"
---
# <a name="the-virtual-screen"></a>Écran virtuel

Le rectangle englobant de toutes les analyses est l' *écran virtuel*. Le bureau couvre l’écran virtuel au lieu d’un seul moniteur. L’illustration suivante montre une organisation possible de trois analyses.

![Illustration montrant trois cases représentant les moniteurs organisés dans une zone représentant l’écran virtuel](images/multimon-1.png)

L' *analyse principale* contient l’origine (0,0). Il s’agit d’une compatibilité avec les applications existantes qui attendent une analyse avec une origine. Toutefois, il n’est pas nécessaire que l’analyse principale se trouve dans l’angle supérieur gauche de l’écran virtuel. Dans la figure 1, il est proche du centre. Lorsque l’analyse principale n’est pas en haut à gauche de l’écran virtuel, les parties de l’écran virtuel ont des coordonnées négatives. Étant donné que la disposition des analyses est définie par l’utilisateur, toutes les applications doivent être conçues pour fonctionner avec des coordonnées négatives. Pour plus d’informations, consultez [considérations relatives à la surveillance multiple pour les programmes plus anciens](multiple-monitor-considerations-for-older-programs.md).

Les coordonnées de l’écran virtuel sont représentées par une valeur 16 bits signée en raison des valeurs 16 bits contenues dans de nombreux messages existants. Ainsi, les limites de l’écran virtuel sont les suivantes :

``` syntax
SHORT_MIN    <= rcVirtualScreen.left   <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.right  <= SHORT_MAX
SHORT_MIN    <= rcVirtualScreen.top    <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.bottom <= SHORT_MAX
```

 

 



