---
description: La méthode GetDVDTextNumberOfStrings récupère le nombre de chaînes de texte disponibles pour la langue spécifiée.
ms.assetid: 84d2b5b7-b474-48a4-9058-ea9da8109398
title: Méthode GetDVDTextNumberOfStrings
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5be6818d447ad244ec59be029f21119ef89024477edc7811de94372c3825fa25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537049"
---
# <a name="getdvdtextnumberofstrings-method"></a>Méthode GetDVDTextNumberOfStrings

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `GetDVDTextNumberOfStrings` méthode récupère le nombre de chaînes de texte disponibles pour la langue spécifiée.

``` syntax
[ iStrings = ] MSWebDVD.GetDVDTextNumberOfStrings(iLangIndex)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*
</dt> <dd>

Spécifie la langue sous la forme d’un entier. La valeur doit être comprise entre zéro et une valeur inférieure à la valeur retournée par [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière spécifiant le nombre de chaînes contenues dans le disque dans la langue spécifiée.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objet MSWebDVD](mswebdvd-object.md)
</dt> </dl>

 

 



