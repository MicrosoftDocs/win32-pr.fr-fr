---
title: Méthode IBasicDevice PresentationUrl
description: Récupère l’URL de présentation de l’appareil.
ms.assetid: F1EF1BBE-F35D-4828-B4F6-D6DEFF5A6391
keywords:
- API de diffusion multimédia en continu de méthode PresentationUrl
- API de diffusion multimédia en continu de méthode PresentationUrl, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode PresentationUrl
topic_type:
- apiref
api_name:
- IBasicDevice.PresentationUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60d5908b80e7b413ca646279a751e12ec7d9c7e6e98ae7ecff3ad1f1d9e60bd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235936"
---
# <a name="ibasicdevicepresentationurl-method"></a>IBasicDevice ::P méthode resentationUrl

Récupère l’URL de présentation de l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PresentationUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’URL de présentation de l’appareil.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





