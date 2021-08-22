---
description: La méthode GetTitleParentalLevels récupère les niveaux de gestion parental pour le titre spécifié.
ms.assetid: 076808d7-6cb6-4d81-b26d-c7945db298f2
title: Méthode GetTitleParentalLevels
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88ef462767c280f5e6f1c58679a78ee876e58042dce632f30711c198b4ca574a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536669"
---
# <a name="gettitleparentallevels-method"></a>Méthode GetTitleParentalLevels

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `GetTitleParentalLevels` méthode récupère les niveaux de gestion parental pour le titre spécifié.

``` syntax
[ iLevels = ] MSWebDVD.GetTitleParentalLevels(iTitle)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Spécifie le titre sous la forme d’un entier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière dont les bits indiquent les niveaux de gestion du contrôle parental (PML) qui sont définis dans le titre spécifié.

## <a name="remarks"></a>Remarques

Un titre peut avoir des chapitres, voire des segments courts, qui ont un PML différent de la PML globale pour le titre. Utilisez cette méthode pour déterminer tous les PMLs qui seront rencontrés lors de la diffusion d’un titre spécifié. L’entier retourné est un jeu d’indicateurs binaires définis comme indiqué dans le tableau ci-dessous. Effectuez une opération and au niveau du bit sur *iLevels* et chaque valeur possible. Si l’opération retourne la **valeur true**, cela signifie que PML sera rencontré à un moment donné dans ce titre.



| Valeur  | Description          |
|--------|----------------------|
| 0x100  | Niveau parental du DVD 1 |
| 0x200  | Niveau parental de DVD 2 |
| 0x400  | Niveau parental de DVD 3 |
| 0x800  | Niveau parental de DVD 4 |
| 0x1000 | Niveau parental de DVD 5 |
| 0x2000 | Niveau parental de DVD 6 |
| 0x4000 | Niveau parental de DVD 7 |
| 0x8000 | Niveau parental de DVD 8 |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> </dl>

 

 



