---
description: crée un énumérateur qui est utilisé pour déterminer les commandes et les événements qu’un appareil WIA (Windows Image Acquisition) 2,0 prend en charge.
ms.assetid: 9efb758d-a5d6-41c7-b318-2897274ccbc0
title: 'IWiaItem2 :: EnumDeviceCapabilities, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumDeviceCapabilities
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3e771aa636b42d9cd7e4024a1684ebe3edf02eeb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522184"
---
# <a name="iwiaitem2enumdevicecapabilities-method"></a>IWiaItem2 :: EnumDeviceCapabilities, méthode

crée un énumérateur qui est utilisé pour déterminer les commandes et les événements qu’un appareil WIA (Windows Image Acquisition) 2,0 prend en charge.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EnumDeviceCapabilities(
  [in]  LONG              lFlags,
  [out] IEnumWIA_DEV_CAPS **ppIEnumWIA_DEV_CAPS
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Spécifie un indicateur qui sélectionne le type de fonctionnalités à énumérer. Il s’agit de l’une des valeurs suivantes.

<dt>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**commandes de l' \_ appareil WIA \_**


</dt> <dd>

Énumérer les commandes de l’appareil.

</dd> <dt>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**\_événements d’appareil WIA \_**


</dt> <dd>

Énumérer les événements d’appareil.

</dd> </dl> </dd> <dt>

*ppIEnumWIA \_ \_Majuscules de développement* \[\]
</dt> <dd>

Type : **[ **IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***

Reçoit un pointeur vers l’interface [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) créée par cette méthode.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Cette méthode est utilisée pour créer un objet énumérateur pour obtenir le jeu de commandes et d’événements pris en charge par un appareil WIA 2,0. Le paramètre *lFlags* est utilisé pour spécifier les genres de fonctionnalités d’appareil à énumérer. La méthode **IWiaItem2 :: EnumDeviceCapabilities** stocke l’adresse de l’interface de l’objet énumérateur dans le paramètre *ppIEnumWIA \_ dev \_ Caps* .

Cette méthode peut uniquement être appelée sur l’élément racine des objets [**IWiaItem2**](-wia-iwiaitem2.md) d’un arbre d’appareil.

Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIEnumWIA \_ dev \_ Caps* .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
