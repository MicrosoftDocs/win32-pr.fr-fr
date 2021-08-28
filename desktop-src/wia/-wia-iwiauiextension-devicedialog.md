---
description: IWiaUIExtension ::D méthode eviceDialog-fournit une interface utilisateur personnalisée qui remplace l’interface utilisateur système par défaut.
ms.assetid: 5dbcacde-5bbe-459d-804f-5ce7eb1cd8d8
title: IWiaUIExtension ::D méthode eviceDialog (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: a06ac5428743c31bae22c6d106ee927791739295754b15ac9764045c3aeeffab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813869"
---
# <a name="iwiauiextensiondevicedialog-method"></a>IWiaUIExtension ::D méthode eviceDialog

Fournit une interface utilisateur personnalisée qui remplace l’interface utilisateur système par défaut.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA *pDeviceDialogData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDeviceDialogData* \[ dans\]
</dt> <dd>

Type : **PDEVICEDIALOGDATA \***

Pointe vers une structure [**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) qui contient toutes les données nécessaires pour implémenter la boîte de dialogue de l’appareil.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si la méthode est réussie, elle retourne la valeur \_ OK. Si l’utilisateur annule la boîte de dialogue, la méthode retourne S \_ false. Si la méthode n’est pas implémentée, elle retourne E \_ NOTIMPL. Si la méthode échoue, elle retourne un code d’erreur COM standard.

## <a name="remarks"></a>Remarques

Si vous implémentez l’interface [**IWiaUIExtension**](-wia-iwiauiextension.md) et que vous ne souhaitez pas remplacer l’interface utilisateur système, cette méthode doit encore être implémentée, mais elle ne doit rien faire d’autre que retourner E \_ NOTIMPL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




