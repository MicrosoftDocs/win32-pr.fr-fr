---
title: Méthode IBasicDevice RemoteStreamingUrls
description: Retourne un vecteur d’URL de diffusion en continu à distance.
ms.assetid: 19B4475F-A7E4-4DC4-9C88-68D91D023AF4
keywords:
- API de diffusion multimédia en continu de méthode RemoteStreamingUrls
- API de diffusion multimédia en continu de méthode RemoteStreamingUrls, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode RemoteStreamingUrls
topic_type:
- apiref
api_name:
- IBasicDevice.RemoteStreamingUrls
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90d98d908cb582c0c2885a9b24a0a525f1e719c82bdffe20e74597ca5fc262a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972328"
---
# <a name="ibasicdeviceremotestreamingurls-method"></a>IBasicDevice :: RemoteStreamingUrls, méthode

Retourne un vecteur d’URL de diffusion en continu à distance.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RemoteStreamingUrls(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit une collection énumérable de pointeurs vers des URL de diffusion en continu distantes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





