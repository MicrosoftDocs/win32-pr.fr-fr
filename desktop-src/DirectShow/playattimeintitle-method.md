---
description: La méthode PlayAtTimeInTitle démarre la lecture à l’heure spécifiée dans le titre spécifié.
ms.assetid: 82726885-8393-409b-b8a1-29a8e9e9ac65
title: Méthode PlayAtTimeInTitle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c40373b4327b6df5fc341ca392c223d464a70a8b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998989"
---
# <a name="playattimeintitle-method"></a>Méthode PlayAtTimeInTitle

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `PlayAtTimeInTitle` méthode démarre la lecture à l’heure spécifiée dans le titre spécifié.

``` syntax
MSWebDVD.PlayAtTimeInTitle(sTime, iTitle)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="sTime"></span><span id="stime"></span><span id="STIME"></span>*sTime*
</dt> <dd>

Spécifie l’heure de début de la lecture sous forme de chaîne. La chaîne doit être au format « hh : mm : SS : FF » (en spécifiant les heures, les minutes, les secondes, les frames).

</dd> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Spécifie l’index du titre sous la forme d’un entier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CurrentTitle**](currenttitle-property.md)
</dt> <dt>

[**PlayAtTime**](playattime-method.md)
</dt> <dt>

[**TitlesAvailable**](titlesavailable-property.md)
</dt> </dl>

 

 



