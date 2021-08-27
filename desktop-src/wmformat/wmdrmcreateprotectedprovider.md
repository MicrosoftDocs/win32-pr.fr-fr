---
title: WMDRMCreateProtectedProvider, fonction (wmdrmsdk. h)
description: la fonction WMDRMCreateProtectedProvider crée une fabrique de classes qui peut créer les autres objets du Windows les api étendues du Client DRM Media.
ms.assetid: 0882062f-48a2-43bc-8853-a8a3d6bc2f52
keywords:
- WMDRMCreateProtectedProvider fonction Windows Media format
topic_type:
- apiref
api_name:
- WMDRMCreateProtectedProvider
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4b5d71ff1deed01cc10d7342286b443b9f64b1a1c192af575a599a2fc8d8c9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026927"
---
# <a name="wmdrmcreateprotectedprovider-function"></a>WMDRMCreateProtectedProvider fonction)

la fonction **WMDRMCreateProtectedProvider** crée une fabrique de classes qui peut créer les autres objets du Windows les api étendues du Client DRM Media. Cette fonction requiert une bibliothèque de stubs de la part de Microsoft et crée des objets qui prennent en charge les fonctionnalités DRM protégées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProtectedProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppDRMProvider* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’interface [**IWMDRMProvider**](iwmdrmprovider.md) de l’objet nouvellement créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions**](drm-functions.md)
</dt> <dt>

[**WMDRMCreateProvider**](wmdrmcreateprovider.md)
</dt> </dl>

 

 





