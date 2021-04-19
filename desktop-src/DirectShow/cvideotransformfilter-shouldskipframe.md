---
description: La méthode ShouldSkipFrame détermine si le filtre doit supprimer un échantillon spécifié.
ms.assetid: 49f86f7d-28b1-443e-a238-692da96d60fb
title: Méthode CVideoTransformFilter. ShouldSkipFrame (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.ShouldSkipFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f845ac7ae52537bfadfb6c913537b32e4d44171
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528425"
---
# <a name="cvideotransformfiltershouldskipframe-method"></a>Méthode CVideoTransformFilter. ShouldSkipFrame

La `ShouldSkipFrame` méthode détermine si le filtre doit supprimer un échantillon spécifié.

## <a name="syntax"></a>Syntaxe


```C++
BOOL ShouldSkipFrame(
   IMediaSample *pIn
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Définis* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si le filtre doit supprimer cet exemple, ou **false** si le filtre doit traiter cet exemple.

## <a name="remarks"></a>Notes

Cette méthode retourne la **valeur true** si les conditions suivantes sont remplies :

-   L’exemple contient des horodatages.
-   Le temps de décodage moyen est d’au moins 25% de la durée de la trame.
-   Le convertisseur est actuellement au moins un frame en retard, comme indiqué par les messages de qualité.
-   Si vous ignorez l’image clé suivante, le frame n’arrivait pas plus d’une image tôt.

Dans le cadre de ce calcul, le filtre enregistre les informations suivantes lors du traitement des données :

-   Temps de décodage moyen au cours des 20 dernières trames (**m \_ itrAvgDecode**)
-   Nombre de trames depuis la dernière image clé (**m \_ nFramesSinceKeyFrame**)
-   Estimation du nombre de frames entre les images clés (**m \_ nKeyFramePeriod**)

Une fois que le filtre a supprimé un frame, il continue à déposer les images jusqu’à ce qu’il atteigne l’image clé suivante. Si cette méthode retourne la **valeur true**, elle envoie également un événement de modification de la [**\_ \_ qualité ce**](ec-quality-change.md) au gestionnaire de graphes de filtre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Vtrans. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CVideoTransformFilter, classe**](cvideotransformfilter.md)
</dt> </dl>

 

 




