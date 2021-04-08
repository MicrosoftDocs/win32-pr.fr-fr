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
ms.openlocfilehash: af48aabb2a64f4c4b8fbd40a3859acc82496a399
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842138"
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

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

