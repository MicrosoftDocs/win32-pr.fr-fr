---
description: Crée une arborescence hiérarchique d’objets IWiaItem2 pour un appareil WIA (Windows Image Acquisition) 2,0.
ms.assetid: df7f3cc2-da0a-4238-b280-89c72107753c
title: 'IWiaDevMgr2 :: CreateDevice, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.CreateDevice
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a548a0ef43c2621b77c4ed10acde393af21d596d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865253"
---
# <a name="iwiadevmgr2createdevice-method"></a>IWiaDevMgr2 :: CreateDevice, méthode

Crée une arborescence hiérarchique d’objets [**IWiaItem2**](-wia-iwiaitem2.md) pour un appareil WIA (Windows Image Acquisition) 2,0.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateDevice(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrDeviceID,
  [out] IWiaItem2 **ppWiaItem2Root
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Actuellement inutilisé. Doit être défini sur zéro (0).

</dd> <dt>

*bstrDeviceID* \[ dans\]
</dt> <dd>

Type : **BSTR**

Spécifie l’identificateur unique de l’appareil WIA 2,0.

</dd> <dt>

*ppWiaItem2Root* \[ à\]
</dt> <dd>

Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Reçoit l’adresse d’un pointeur vers l’interface [**IWiaItem2**](-wia-iwiaitem2.md) de l’élément racine de l’arborescence hiérarchique pour l’appareil WIA 2,0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Les applications utilisent la méthode **IWiaDevMgr2 :: CreateDevice** pour créer un objet appareil pour les appareils WIA 2,0 spécifiés par le paramètre bstrDeviceID. Quand elle retourne, la méthode **IWiaDevMgr2 :: CreateDevice** stocke l’adresse d’un pointeur dans le paramètre *ppWiaItem2Root*, qui pointe vers l’élément racine de l’arborescence des objets [**IWiaItem2**](-wia-iwiaitem2.md) créés par **IWiaDevMgr2 :: CreateDevice**. Les applications peuvent utiliser cette arborescence d’objets pour contrôler et récupérer des données à partir de l’appareil WIA 2,0.

Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs qu’elles reçoivent via le paramètre *ppWiaItem2Root* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
