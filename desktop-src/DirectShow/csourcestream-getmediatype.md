---
description: La méthode GetMediaType récupère un type de média par défaut. Cette méthode utilise les paramètres *iPosition* et *pMediaType* .
ms.assetid: c5c5f498-a9a3-4ce7-8cf5-941397aa649d
title: Méthode CSourceStream. GetMediaType (source. h)-paramètres iPosition et pMediaType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb3095e366a03d94616d45eda441fec78d2ccbf7d58f8e74890a42902bae6fc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073253"
---
# <a name="csourcestreamgetmediatype-method-sourceh---iposition-and-pmediatype-parameters"></a>Méthode CSourceStream. GetMediaType (source. h)-paramètres iPosition et pMediaType

La méthode **GetMediaType** récupère un type de média par défaut.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*iPosition* 
</dt> <dd>

Valeur d’index de base zéro.

</dd> <dt>

*pMediaType* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui reçoit le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                            | Description                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Réussite.<br/>              |
| <dl> <dt>**VFW \_ S \_ n’a \_ plus d' \_ éléments**</dt> </dl> | Index hors limites.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Index inférieur à zéro.<br/> |
| <dl> <dt>**E \_ inattendu**</dt> </dl>           | Erreur inattendue.<br/>     |



 

## <a name="remarks"></a>Remarques

Il existe deux versions de cette méthode. Une version remplace la méthode [**CBasePin :: GetMediaType**](cbasepin-getmediatype.md) et prend une valeur d’index en tant que paramètre. L’autre version est conçue pour récupérer un type de média unique, de sorte qu’il n’y ait pas de paramètre d’index.

La méthode à paramètre unique retourne E \_ inattendue. La méthode à deux paramètres vérifie que le paramètre *iPosition* est égal à zéro, puis appelle la version à un seul paramètre. Selon le nombre de types de médias pris en charge par le pin, vous devez remplacer l’une des méthodes suivantes :

-   Si le code PIN ne prend en charge qu’un seul type de média, remplacez la version à paramètre unique. Renseignez le type de média que le code confidentiel prend en charge.
-   Si le code PIN prend en charge plusieurs types de média, remplacez la version à deux paramètres. Substituez également la méthode [**CSourceStream :: CheckMediaType**](csourcestream-checkmediatype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête  | Source. h (inclure Flux. h)                                                                                    |
| Bibliothèque | Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




