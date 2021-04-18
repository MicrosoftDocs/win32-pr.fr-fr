---
description: La méthode DVDAdm. SaveParentalCountry enregistre le nouveau pays ou la nouvelle région parente de l’application dans le registre.
ms.assetid: 2185ad7d-c7c1-4d8b-82e7-5ed5fffaff26
title: Méthode SaveParentalCountry (segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ca47a6ca10f25298b4eb10fdcf532c8d764b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532881"
---
# <a name="saveparentalcountry-method"></a>Méthode SaveParentalCountry

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DVDAdm.SaveParentalCountry` méthode enregistre le nouveau pays ou la nouvelle région parente de l’application dans le registre.

``` syntax
DVD.DVDAdm.SaveParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*
</dt> <dd>

Spécifie le pays ou la région parente sous la forme d’un entier.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Spécifie le nom d’utilisateur sous forme de chaîne. (Actuellement ignoré.)

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Spécifie le mot de passe sous forme de chaîne.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Cette méthode permet à un utilisateur qui connaît le mot de passe actuel d’enregistrer un nouveau paramètre de pays/région parental dans le registre. Comme avec toutes les méthodes de **MSDVDAdm**, cette méthode n’affecte pas le niveau actuel dans le lecteur ; il modifie uniquement le paramètre du Registre, de sorte que la prochaine fois que l’objet MSWebDVD est créé, il s’ouvre avec le nouveau pays/région. Pour modifier le pays ou la région parente dans le lecteur, appelez [**SelectParentalCountry**](selectparentalcountry-method.md), qui ne modifie pas le paramètre de registre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Segment. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SaveParentalLevel**](saveparentallevel-method.md)
</dt> <dt>

[Objet MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




