---
description: La méthode IsSubpictureStreamEnabled récupère une valeur indiquant si le flux de sous-image spécifié est activé dans le titre actuel.
ms.assetid: c6436f77-ca94-464f-9336-f485f5d5d199
title: Méthode IsSubpictureStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 818b4ff18dac87ea3346a1a503764b2e5e9cd02a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007523"
---
# <a name="issubpicturestreamenabled-method"></a>Méthode IsSubpictureStreamEnabled

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `IsSubpictureStreamEnabled` méthode récupère une valeur indiquant si le flux de sous-image spécifié est activé dans le titre actuel.

``` syntax
[ bEnabled = ] MSWebDVD.IsSubpictureStreamEnabled(iStream)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Spécifie le flux de sous-image sous la forme d’un entier.



| Valeur   | Description              |
|---------|--------------------------|
| de 0 à 31 | flux de sous-image        |
| 63      | flux muet faible-débit |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur booléenne indiquant si le flux audio spécifié est disponible dans le titre actuel. True signifie qu’il est disponible.

## <a name="remarks"></a>Notes

Bien qu’un disque puisse contenir jusqu’à 32 flux de sous-image, chaque flux n’est pas nécessairement disponible pour chaque titre. Vérifiez toujours qu’un flux est disponible pour un titre avant de définir la propriété [**CurrentSubpictureStream**](currentsubpicturestream-property.md) .

 

 



