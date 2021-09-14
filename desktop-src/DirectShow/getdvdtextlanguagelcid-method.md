---
description: La méthode GetDVDTextLanguageLCID récupère l’identificateur de paramètres régionaux (LCID) pour le bloc de chaîne de texte spécifié.
ms.assetid: feaa1db8-2d33-4c32-8491-f3aa5555e3d3
title: Méthode GetDVDTextLanguageLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66d21b9870982b605d9deeb1e22882a525c5616
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999124"
---
# <a name="getdvdtextlanguagelcid-method"></a>Méthode GetDVDTextLanguageLCID

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `GetDVDTextLanguageLCID` méthode récupère l’identificateur de paramètres régionaux (LCID) pour le bloc de chaîne de texte spécifié.

``` syntax
[ iLCID = ] MSWebDVD.GetDVDTextLanguageLCID(iLangIndex)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*
</dt> <dd>

Spécifie le bloc de langage de texte sur le disque sous la forme d’un entier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur LCID qui contient des informations spécifiant le langage dans lequel les chaînes sont écrites.

## <a name="remarks"></a>Notes

Les chaînes de texte supplémentaires sont stockées dans des blocs contigus sur le disque. Chaque langage possède un bloc de chaînes. Une application spécifie ces blocs par un index, qui doit être inférieur à la valeur retournée par [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objet MSWebDVD](mswebdvd-object.md)
</dt> <dt>

[**GetLangFromLangID**](getlangfromlangid-method.md)
</dt> </dl>

 

 



