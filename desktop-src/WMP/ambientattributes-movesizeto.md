---
title: AmbientAttributes.moveSizeTo
description: La méthode moveSizeTo déplace le contrôle et spécifie une nouvelle taille pour le contrôle dans le nouvel emplacement. Le contrôle se déplace et se redimensionne de manière animée sur la période spécifiée.
ms.assetid: 89e3bf16-a123-4fb1-8c24-bc22a978e7f6
keywords:
- AmbientAttributes. moveSizeTo Lecteur Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.moveSizeTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 936a6696dfcc99c5a181906eb970f84c7019af7905c466f09e820044f6220271
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469949"
---
# <a name="ambientattributesmovesizeto"></a>AmbientAttributes.moveSizeTo

La méthode **moveSizeTo** déplace le contrôle et spécifie une nouvelle taille pour le contrôle dans le nouvel emplacement. Le contrôle se déplace et se redimensionne de manière animée sur la période spécifiée.

``` syntax
        elementID.moveSizeTo(newX, newY, newWidth, newHeight, moveTime, fSlide)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*
</dt> <dd>

**Nombre** (**long**) spécifiant la nouvelle valeur de l’attribut de **gauche** du contrôle.

</dd> <dt>

<span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*
</dt> <dd>

**Nombre** (**long**) spécifiant la nouvelle valeur de l’attribut **Top** du contrôle.

</dd> <dt>

<span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*newWidth*
</dt> <dd>

**Nombre** (**long**) spécifiant la nouvelle valeur de l’attribut **Width** du contrôle.

</dd> <dt>

<span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*newHeight*
</dt> <dd>

**Nombre** (**long**) spécifiant la nouvelle valeur de l’attribut **Height** du contrôle.

</dd> <dt>

<span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*
</dt> <dd>

**Nombre** (**long**) spécifiant la durée, en millisecondes, nécessaire au déplacement du contrôle vers son nouvel emplacement.

</dd> <dt>

<span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*fSlide*
</dt> <dd>

**Valeur booléenne** qui spécifie le type de mouvement créé lors du déplacement du contrôle.



| Valeur | Description                                                             |
|-------|-------------------------------------------------------------------------|
| true  | Motion est non linéaire (mouvement coulissant qui accélère et ralentit). |
| false | Motion est linéaire.                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Le mouvement du contrôle peut être linéaire ou non linéaire. Le mouvement linéaire signifie que le contrôle se déplace à une vitesse constante jusqu’à son nouvel emplacement, en démarrant et en arrêt brutalement. Lorsque vous spécifiez un mouvement non linéaire, un mouvement coulissant est créé, ce qui accélère la valeur zéro au début du mouvement et ralentit vers la valeur zéro à la fin, en partant d’un arrêt lisse.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------|
| Version<br/> | Lecteur Windows Media 11<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs ambiants**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes. Height**](ambientattributes-height.md)
</dt> <dt>

[**AmbientAttributes. Left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> <dt>

[**AmbientAttributes. Width**](ambientattributes-width.md)
</dt> </dl>

 

 





