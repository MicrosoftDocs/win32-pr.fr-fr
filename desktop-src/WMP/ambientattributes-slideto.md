---
title: AmbientAttributes.slideTo
description: La méthode slideTo déplace le contrôle vers un nouvel emplacement. Le contrôle se déplace de manière non linéaire sur la période spécifiée.
ms.assetid: 06dd610b-cb58-4b60-9f4b-8929c54c3c33
keywords:
- AmbientAttributes. slideTo Lecteur Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.slideTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f199a2786adbd63313c3f500d589f9f51e2b8ca2fa8120a8fdf75021041115
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469909"
---
# <a name="ambientattributesslideto"></a>AmbientAttributes.slideTo

La méthode **slideTo** déplace le contrôle vers un nouvel emplacement. Le contrôle se déplace de manière non linéaire sur la période spécifiée.

``` syntax
        elementID.slideTo(newX, newY, moveTime)
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

<span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*
</dt> <dd>

**Nombre** (**long**) spécifiant la durée, en millisecondes, nécessaire au déplacement du contrôle vers son nouvel emplacement.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode est différente de **MoveTo**, qui crée un mouvement linéaire lors du déplacement du contrôle. Le mouvement non linéaire créé par cette méthode est un mouvement coulissant qui accélère à partir d’une vitesse nulle au début du mouvement et ralentit à zéro à la fin, en arrivant à un arrêt sans heurts.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------|
| Version<br/> | Lecteur Windows Media 11<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs ambiants**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes. Left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes. moveTo**](ambientattributes-moveto.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> </dl>

 

 





