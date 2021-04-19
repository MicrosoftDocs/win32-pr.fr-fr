---
title: Méthode IWMDRMLicense ResetEnumeration (wmdrmsdk. h)
description: La méthode ResetEnumeration réinitialise la liste de licences à son état d’origine. La licence active devient la première licence de la liste.
ms.assetid: cb5a31a8-ee25-44d6-81ca-746c379cb99e
keywords:
- Méthode ResetEnumeration format Windows Media
- Méthode ResetEnumeration format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, méthode ResetEnumeration
topic_type:
- apiref
api_name:
- IWMDRMLicense.ResetEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6510c05b4c974051d9902ed2d30d9cdf99956af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528704"
---
# <a name="iwmdrmlicenseresetenumeration-method"></a>IWMDRMLicense :: ResetEnumeration, méthode

La méthode **ResetEnumeration** réinitialise la liste de licences à son état d’origine. La licence active devient la première licence de la liste.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ResetEnumeration();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                | Description                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**le \_ RIV de la messagerie DRM E est \_ \_ \_ trop \_ petit**</dt> </dl> | Une liste de révocation de contenu mise à jour est nécessaire.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>                       | S_OK<br/>                         |



 

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





