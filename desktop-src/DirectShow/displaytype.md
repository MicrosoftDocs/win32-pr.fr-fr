---
description: La fonction DisplayType envoie des informations sur un type de média à l’emplacement de sortie de débogage. Ignoré dans les builds de vente au détail.
ms.assetid: 63a88508-dff8-4869-97e5-0f75f4a9dca0
title: Fonction DisplayType (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DisplayType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3d83bbe7a24463fc4cfaed4ace3adec9d6fcf7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999656"
---
# <a name="displaytype-function"></a>DisplayType, fonction

La `DisplayType` fonction envoie des informations sur un type de média à l’emplacement de sortie de débogage. Ignoré dans les builds de vente au détail.

## <a name="syntax"></a>Syntaxe


```C++
void DisplayType(
         LPTSTR        label,
   const AM_MEDIA_TYPE *pmtIn
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*label* 
</dt> <dd>

Chaîne qui contient un message à afficher avec les informations sur le type de média.

</dd> <dt>

*pmtIn* 
</dt> <dd>

ointer à la structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui contient le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette fonction génère plusieurs messages de trace des journaux \_ . Au niveau de la journalisation 2 ou supérieur, la fonction affiche le type, le sous-type et le type de format principaux, ainsi que les données du bloc de format. Au niveau de la journalisation 5 ou supérieur, la fonction affiche des informations supplémentaires, telles que les rectangles source et cible pour les types vidéo.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxdebug. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de sortie de débogage](debug-output-functions.md)
</dt> </dl>

 

 




