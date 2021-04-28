---
description: 'IWiaUIExtension :: GetDeviceIcon, méthode-obtient une icône d’appareil personnalisé.'
ms.assetid: 27763f39-80d8-4862-b045-e49c6e824c28
title: 'IWiaUIExtension :: GetDeviceIcon, méthode (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 9bfa8e87736412822c1a70f75b129aeec30af20e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116657"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a>IWiaUIExtension :: GetDeviceIcon, méthode

Obtient une icône d’appareil personnalisé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrDeviceId* \[ dans\]
</dt> <dd>

Type : **BSTR**

Spécifie l’ID d’appareil de l’appareil WIA pour lequel l’icône doit être obtenue.

</dd> <dt>

*phIcon* \[ à\]
</dt> <dd>

Type : **HICON \***

Pointe vers un emplacement de mémoire qui reçoit un handle pour l’icône de l’appareil.

</dd> <dt>

*nSize* \[ dans\]
</dt> <dd>

Type : **ULong**

Spécifie la taille d’icône souhaitée, en pixels. L’icône est supposée être carrée et nSize spécifie à la fois la largeur et la hauteur de l’icône demandée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




