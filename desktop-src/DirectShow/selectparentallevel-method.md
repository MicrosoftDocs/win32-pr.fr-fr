---
description: La méthode SelectParentalLevel définit le niveau parental spécifié pour la lecture suivante.
ms.assetid: ffd1e204-6ed2-4190-8635-9f3866d38099
title: Méthode SelectParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb00172b8e61f353c45981af628eb396bca7a7df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521271"
---
# <a name="selectparentallevel-method"></a>Méthode SelectParentalLevel

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `SelectParentalLevel` méthode définit le niveau parental spécifié pour la lecture suivante.

``` syntax
MSWebDVD.SelectParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*
</dt> <dd>

Spécifie le niveau de gestion parental sous la forme d’un entier. Pour activer la gestion parentale, le paramètre *iLevel* doit être compris entre 1 et 8. Pour désactiver la gestion parentale, affectez la valeur-1 à *iLevel* .

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Spécifie l’utilisateur actuel en tant que chaîne. (Actuellement ignoré.)

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Spécifie le mot de passe actuellement stocké dans le Registre sous forme de chaîne.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Cette méthode définit le niveau d’accès dans l’objet MSWebDVD, qui détermine le contenu que l’utilisateur peut relire. Les niveaux plus élevés peuvent lire du contenu de niveau inférieur, mais les niveaux inférieurs ne peuvent pas lire du contenu de niveau supérieur. La signification exacte des huit niveaux de gestion parentale des DVD varie en fonction du pays ou de la région. Au États-Unis et au Canada, les niveaux sont mappés aux catégories d’évaluation MPAA (motion image Association of America). La gestion du contrôle parental dans le navigateur DVD est désactivée par défaut.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> <dt>

[**NotifyParentalLevelChange**](notifyparentallevelchange-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**AcceptParentalLevelChange**](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



