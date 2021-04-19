---
description: La méthode NotifyParentalLevelChange active ou désactive la gestion des événements pour les commandes de niveau de gestion parental temporaire.
ms.assetid: c8252cc6-a83f-4cce-ba3e-7db669eeb465
title: Méthode NotifyParentalLevelChange (segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc47b7d78af8cfdd32aa63361411e769c375ddf1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537503"
---
# <a name="notifyparentallevelchange-method"></a>Méthode NotifyParentalLevelChange

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `NotifyParentalLevelChange` méthode active ou désactive la gestion des événements pour les commandes de niveau de gestion parental temporaire.

``` syntax
MSWebDVD.NotifyParentalLevelChange(bNotify)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bNotify*
</dt> <dd>

Spécifie une valeur booléenne indiquant si l’application est notifiée ou non lorsque l’objet MSWebDVD rencontre des segments vidéo avec une évaluation plus restrictive que l’évaluation générale du disque.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Les notifications de gestion parentale sont désactivées par défaut. Cela signifie que les commandes parentales temporaires du disque sont autorisées mais ignorées et que le disque est lu sans interruption. Appelez cette méthode lors de l’initialisation de votre application si vous devez gérer les commandes de niveau de gestion parental temporaire à partir du disque. Pour désactiver la gestion parentale une fois qu’elle est activée, appelez cette méthode avec un argument ayant la valeur false. Pour plus d’informations sur la gestion parentale, consultez [**AcceptParentalLevelChange**](acceptparentallevelchange-method.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Segment. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> </dl>

 

 




