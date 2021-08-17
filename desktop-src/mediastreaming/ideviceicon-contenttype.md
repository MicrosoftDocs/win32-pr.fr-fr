---
title: IDeviceIcon, méthode ContentType
description: Récupère le type de contenu de l’icône.
ms.assetid: 01928A98-B7D0-4523-9259-81FEB33F052E
keywords:
- API de diffusion multimédia en continu de la méthode ContentType
- Méthode ContentType API de diffusion multimédia en continu, interface IDeviceIcon
- API de diffusion multimédia en continu de l’interface IDeviceIcon, méthode ContentType
topic_type:
- apiref
api_name:
- IDeviceIcon.ContentType
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8fb9cb639381b60bb59965d12ce3f0545daf6d2725cde69d3dea3dee589f8f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461742"
---
# <a name="ideviceiconcontenttype-method"></a>IDeviceIcon :: ContentType, méthode

Récupère le type de contenu de l’icône.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ContentType(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit un pointeur vers le type de contenu de l’icône.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

