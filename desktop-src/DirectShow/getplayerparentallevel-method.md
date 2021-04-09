---
description: Le GetPlayerParentalLevel récupère le niveau de gestion parental défini dans l’objet MSWebDVD.
ms.assetid: 451e0891-4e5d-4a01-94b8-290f5a804ff1
title: Méthode GetPlayerParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bac51e776a45e0d1fa748fc995240292474e902
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108499"
---
# <a name="getplayerparentallevel-method"></a>Méthode GetPlayerParentalLevel

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

Le `GetPlayerParentalLevel` récupère le niveau de gestion parental défini dans l’objet **mswebdvd** .

``` syntax
[ iLevel = ] MSWebDVD.GetPlayerParentalLevel()
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière spécifiant le niveau parental actuel dans le navigateur DVD, ou-1 si la gestion parentale est désactivée.

## <a name="remarks"></a>Notes

Une application de lecteur est chargée d’appliquer les contrôles de contrôle parental. Le niveau parental du joueur est une valeur définie par une application qui peut être utilisée pour indiquer le niveau parental le plus élevé que l’utilisateur actuel peut afficher. Lorsque le navigateur DVD rencontre un nouveau niveau parental, utilisez cette méthode pour déterminer si le nouveau niveau est supérieur au niveau défini par l’application via [**SelectParentalLevel**](selectparentallevel-method.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> </dl>

 

 



