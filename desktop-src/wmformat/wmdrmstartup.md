---
title: WMDRMStartup, fonction (wmdrmsdk. h)
description: la fonction WMDRMStartup initialise les ressources utilisées par les api étendues du Client Media DRM Windows.
ms.assetid: 2fd26bcc-8106-4356-933a-d4cf3536f4fb
keywords:
- WMDRMStartup fonction Windows Media format
topic_type:
- apiref
api_name:
- WMDRMStartup
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c194a8c060ad1626fde796510c25c83e3e163dafffe9c17df17a7dcec890be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928740"
---
# <a name="wmdrmstartup-function"></a>WMDRMStartup fonction)

la fonction **WMDRMStartup** initialise les ressources utilisées par les api étendues du Client Media DRM Windows.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE WMDRMStartup(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Remarques

Pour chaque appel de cette fonction, vous devez appeler [**WMDRMShutdown**](wmdrmshutdown.md) pour libérer les ressources utilisées.

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

 

 





