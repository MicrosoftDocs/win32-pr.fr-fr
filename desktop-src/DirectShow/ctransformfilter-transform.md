---
description: La méthode de transformation transforme un exemple d’entrée pour produire un échantillon de sortie.
ms.assetid: 30ef8c0c-e834-481a-93ff-d06e6fa1ddeb
title: CTransformFilter. Transform, méthode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a03b32006aecfb79f90a5f5aefeff542c53341b205031352974341926ed8eb26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907499"
---
# <a name="ctransformfiltertransform-method"></a>CTransformFilter. Transform, méthode

La `Transform` méthode transforme un exemple d’entrée pour produire un échantillon de sortie.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT Transform(
   IMediaSample *pIn,
   IMediaSample *pOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Définis* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple d’entrée.

</dd> <dt>

*Moue* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple de sortie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La classe de base retourne E \_ inattendue.

La classe dérivée doit retourner une valeur **HRESULT** indiquant la réussite ou l’échec. Les valeurs possibles sont les suivantes :



| Code de retour                                                                             | Description                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Ne fournissez pas cet exemple.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Réussite.<br/>                    |



 

## <a name="remarks"></a>Remarques

Substituez cette méthode pour produire des données de sortie. Lit les données d’entrée de l’exemple spécifié par le paramètre *pin* et écrit les nouvelles données dans l’exemple spécifié par le paramètre *moue* .

Avant que le filtre appelle cette méthode, il copie les propriétés de l’exemple d’entrée dans l’exemple de sortie. La `Transform` méthode doit définir toutes les propriétés qui diffèrent entre les deux exemples, à l’aide des méthodes **IMediaSample** ou de l’interface [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) (si disponible).

Si le filtre ne doit pas livrer cet exemple (par exemple, pour prendre en charge le contrôle de qualité), la méthode doit retourner S \_ false.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




