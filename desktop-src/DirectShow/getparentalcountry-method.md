---
description: La méthode DVDAdm. GetParentalCountry récupère le pays ou la région parente qui a été enregistré pour la dernière fois dans le registre.
ms.assetid: 947c5e2a-dfd5-4900-87d4-0ec967b99a22
title: Méthode GetParentalCountry (segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6fcee63fd3cad64498d95ca74e81a9f02804a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535313"
---
# <a name="getparentalcountry-method"></a>Méthode GetParentalCountry

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DVDAdm.GetParentalCountry` méthode récupère le pays ou la région parente qui a été enregistrée dans le registre.

``` syntax
[ iParentalCountry = ] DVD.DVDAdm.GetParentalCountry()
```

## <a name="return-value"></a>Valeur renvoyée

Retourne un entier indiquant le code de pays/région par défaut stocké dans le registre.

## <a name="remarks"></a>Notes

Le pays ou la région parente que cette méthode récupère n’est pas nécessairement le même pays ou la même région actuellement stockée dans l’objet MSWebDVD.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Segment. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objet MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




