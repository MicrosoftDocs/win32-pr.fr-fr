---
description: La méthode DVDAdm. SaveParentalLevel enregistre un nouveau niveau parental par défaut dans le registre.
ms.assetid: 8ad22098-acbd-41fd-9224-829b3cc5f8ae
title: Méthode SaveParentalLevel (segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d30d26264dff077de391b6b513f7e9ab5048c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537094"
---
# <a name="saveparentallevel-method"></a>Méthode SaveParentalLevel

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La méthode **DVDAdm. SaveParentalLevel** enregistre un nouveau niveau parental par défaut dans le registre.

``` syntax
DVD.DVDAdm.SaveParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*
</dt> <dd>

Spécifie le niveau parental comme valeur anInteger comprise entre 1 et 8.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Spécifie le nom d’utilisateur sous forme de chaîne. (Actuellement ignoré.)

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Spécifie le mot de passe sous forme de chaîne.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Cette méthode permet à un utilisateur qui connaît le mot de passe actuel d’enregistrer un nouveau paramètre de niveau parental dans le registre. Comme avec toutes les méthodes de **MSDVDAdm**, cette méthode n’affecte pas le niveau actuel dans le lecteur ; il modifie uniquement le paramètre du Registre, de sorte que la prochaine fois que l’objet MSWebDVD est démarré, il s’ouvre avec le nouveau niveau. Spécifiez-1 pour désactiver la gestion parentale. Pour modifier le niveau parental dans le lecteur, appelez [**SelectParentalLevel**](selectparentallevel-method.md), qui ne modifie pas le paramètre de registre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Segment. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objet MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




