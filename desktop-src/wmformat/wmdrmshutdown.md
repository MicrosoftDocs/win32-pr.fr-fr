---
title: WMDRMShutdown, fonction (wmdrmsdk. h)
description: La fonction WMDRMShutdown libère les ressources utilisées par les API étendues du client Windows Media DRM.
ms.assetid: fa99a07a-2f07-464b-b7a2-e8f3110389b5
keywords:
- WMDRMShutdown fonction Windows Media format
topic_type:
- apiref
api_name:
- WMDRMShutdown
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb49049a593699a4071eefea9c5cf7c61571fc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537332"
---
# <a name="wmdrmshutdown-function"></a>WMDRMShutdown fonction)

La fonction **WMDRMShutdown** libère les ressources utilisées par les API étendues du client Windows Media DRM.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE WMDRMShutdown(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Pour éviter les fuites de mémoire, vous devez appeler cette fonction pour chaque appel de la fonction [**WMDRMStartup**](wmdrmstartup.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Wmdrmsdk.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions**](drm-functions.md)
</dt> </dl>

 

 





