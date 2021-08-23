---
description: La méthode GetMediaType récupère un type de média par défaut.
ms.assetid: 85605885-adb5-4f13-91af-48bf74684eca
title: Méthode CSourceStream. GetMediaType (source. h)-paramètre pMediaType
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
ms.openlocfilehash: 2850d08726337f1ff43ad09319aea8b0af95d107ad9dad9c0f89ce94474c7261
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073193"
---
# <a name="csourcestreamgetmediatype-method-sourceh"></a>Méthode CSourceStream. GetMediaType (source. h)

La `GetMediaType` méthode récupère un type de média par défaut.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT GetMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

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
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




