---
description: La propriété DVDUniqueID récupère un numéro généré par le système qui identifie de façon unique le disque actuel.
ms.assetid: 8ea6dd4d-6998-4212-8874-9c6cd93a1db3
title: Propriété DVDUniqueID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 488a3e76c93005a55f58e631f0b166b51f036e63857df3b2e21eed6e093e55b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652902"
---
# <a name="dvduniqueid-property"></a>Propriété DVDUniqueID

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DVDUniqueID` propriété récupère un numéro généré par le système qui identifie de façon unique le disque actuel.

``` syntax
[ iDiscID = ] MSWebDVD.DVDUniqueID
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière qui identifie de façon unique le disque actuel.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture seule sans valeur par défaut. Le numéro d’identificateur (ID) n’est pas absolument unique, mais il est unique dans tous les cas pratiques. L’ID s’applique à toutes les copies répliquées d’un disque. En d’autres termes, toutes les copies d’un film spécifique ont le même ID. L’ID est basé sur les tailles de fichier, les dates et d’autres informations, et non sur la valeur BCA.

 

 



