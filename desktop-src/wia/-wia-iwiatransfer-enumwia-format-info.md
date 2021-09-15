---
description: crée un énumérateur pour les formats de transfert pris en charge par l’appareil WIA (Windows Image Acquisition) 2,0.
ms.assetid: 70fffc7b-b500-4404-9d94-76d1828ddc8c
title: 'IWiaTransfer :: EnumWIA_FORMAT_INFO, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.EnumWIA_FORMAT_INFO
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 66f3c91d6023655daf85b2a0d726d98a685b001b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312778"
---
# <a name="iwiatransferenumwia_format_info-method"></a>IWiaTransfer :: EnumWIA \_ , \_ méthode des informations de format

crée un énumérateur pour les formats de transfert pris en charge par l’appareil WIA (Windows Image Acquisition) 2,0.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EnumWIA_FORMAT_INFO(
  [out] IEnumWIA_FORMAT_INFO **ppIEnum
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppIEnum* \[ à\]
</dt> <dd>

Type : **[ **\_ \_ informations sur le format IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***

Adresse du pointeur vers l’interface d' [**\_ \_ informations de format IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) pour l’énumérateur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur le pointeur d’interface reçu via le paramètre *ppIEnum* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
