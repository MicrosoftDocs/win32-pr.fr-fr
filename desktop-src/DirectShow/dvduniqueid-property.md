---
description: La propriété DVDUniqueID récupère un numéro généré par le système qui identifie de façon unique le disque actuel.
ms.assetid: 8ea6dd4d-6998-4212-8874-9c6cd93a1db3
title: Propriété DVDUniqueID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23138f348ef1ec71f1506c8892532bd42f1c807d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324908"
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

## <a name="remarks"></a>Notes

Cette propriété est en lecture seule sans valeur par défaut. Le numéro d’identificateur (ID) n’est pas absolument unique, mais il est unique dans tous les cas pratiques. L’ID s’applique à toutes les copies répliquées d’un disque. En d’autres termes, toutes les copies d’un film spécifique ont le même ID. L’ID est basé sur les tailles de fichier, les dates et d’autres informations, et non sur la valeur BCA.

 

 



