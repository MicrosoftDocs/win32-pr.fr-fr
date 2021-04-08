---
description: Crée un énumérateur d’informations de propriété pour chaque périphérique WIA (Windows Image Acquisition) 2,0 disponible.
ms.assetid: e37b73d5-5192-46e4-bb1c-bd1ef41f1d6c
title: 'IWiaDevMgr2 :: EnumDeviceInfo, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.EnumDeviceInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: bd9e9281b625f4cec5377537d82a304045b95a3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752837"
---
# <a name="iwiadevmgr2enumdeviceinfo-method"></a>IWiaDevMgr2 :: EnumDeviceInfo, méthode

Crée un énumérateur d’informations de propriété pour chaque périphérique WIA (Windows Image Acquisition) 2,0 disponible.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EnumDeviceInfo(
  [in]          LONG              lFlags,
  [out, retval] IEnumWIA_DEV_INFO **ppIEnum
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Spécifie le type d’appareils WIA 2,0 à énumérer.

<dt>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**WIA \_ DevInfo \_ enum \_ local**


</dt> <dd>

Seuls les appareils de scanneur actifs connectés localement sont énumérés.

</dd> <dt>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**WIA \_ DevInfo \_ enum \_ All**


</dt> <dd>

Tous les appareils sont énumérés, à la fois localement et à distance, y compris les appareils inactifs (déconnectés) et les appareils traditionnels de ICT uniquement.

</dd> </dl> </dd> <dt>

*ppIEnum* \[ out, retval\]
</dt> <dd>

Type : **[ **IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***

Reçoit l’adresse d’un pointeur vers l’interface [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

La méthode **IWiaDevMgr2 :: EnumDeviceInfo** crée un objet énumérateur qui prend en charge l’interface d' [**\_ \_ informations de développement IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) . La méthode stocke un pointeur vers l’interface **IEnumWIA \_ dev \_ info** dans le paramètre *ppIEnum*. Les applications peuvent utiliser le pointeur d’interface **IEnumWIA \_ dev \_ info** pour énumérer les propriétés de chaque appareil WIA 2,0 attaché à l’ordinateur de l’utilisateur.

Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIEnum* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
