---
description: La propriété CurrentSubpictureStream définit ou récupère le flux de sous-image en cours.
ms.assetid: 66473c87-ddfe-4555-89ad-90e210a75694
title: Propriété CurrentSubpictureStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56e9c4af677180d4893ef56a9d2bff1fb034971969e2e64d648d53e19d0814a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821944"
---
# <a name="currentsubpicturestream-property"></a>Propriété CurrentSubpictureStream

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `CurrentSubpictureStream` propriété définit ou récupère le flux de sous-image en cours.

``` syntax
[ iSPStream = ] MSWebDVD.CurrentSubpictureStream
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant le flux.

## <a name="remarks"></a>Remarques

Les valeurs possibles de cette propriété sont les suivantes :



| Valeur   | Description              |
|---------|--------------------------|
| de 0 à 31 | Flux de sous-image    |
| 63      | Flux muet faible-débit |



 

Cette propriété est en lecture/écriture sans valeur par défaut. Avant de définir un nouveau flux de sous-image, appelez [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md) pour vérifier que le flux est disponible.

La définition de cette propriété entraîne le basculement de la propriété [**SubpictureOn**](subpictureon-property.md) sur **true**.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SubpictureOn**](subpictureon-property.md)
</dt> <dt>

[**SubpictureStreamsAvailable**](subpicturestreamsavailable-property.md)
</dt> </dl>

 

 



