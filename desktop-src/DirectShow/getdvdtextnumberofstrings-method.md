---
description: La méthode GetDVDTextNumberOfStrings récupère le nombre de chaînes de texte disponibles pour la langue spécifiée.
ms.assetid: 84d2b5b7-b474-48a4-9058-ea9da8109398
title: Méthode GetDVDTextNumberOfStrings
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18c9c4fadfd28d6cddc8b9013a6e426aebe9f816
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513107"
---
# <a name="getdvdtextnumberofstrings-method"></a>Méthode GetDVDTextNumberOfStrings

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

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

 

 



