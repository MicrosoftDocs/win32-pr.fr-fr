---
description: La méthode StillOff reprend la lecture, en annulant le mode toujours.
ms.assetid: 62091aad-8a78-4543-a844-a4227aed81df
title: Méthode StillOff
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cf63409cb435e0e72cb9ebcb856df7956270dc92931366f575c1fb02df9315a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050209"
---
# <a name="stilloff-method"></a>Méthode StillOff

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `StillOff` méthode reprend la lecture, en annulant le mode toujours.

``` syntax
MSWebDVD.StillOff()
```

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Le [navigateur DVD](dvd-navigator-filter.md) passe en mode toujours lorsqu’il rencontre une image toujours créée sur le disque. Il indique à votre application d’envoyer un \_ DVD ce \_ toujours \_ sur l’événement. Le mode toujours est différent du navigateur DVD qui se trouve dans un état suspendu en raison d’une opération utilisateur. `StillOff`L’appel de reprend la lecture en mode toujours, mais ne redémarre pas le navigateur DVD lorsqu’il est dans un état suspendu.

 

 



