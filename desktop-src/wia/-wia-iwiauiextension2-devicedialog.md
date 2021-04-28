---
description: IWiaUIExtension2 ::D méthode eviceDialog-fournit une interface utilisateur personnalisée qui remplace l’interface utilisateur système par défaut.
ms.assetid: 0d70392d-294a-42bf-adc5-1006f83d7e21
title: IWiaUIExtension2 ::D méthode eviceDialog (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 94e717184c936ae85ba1cf345a13b44f9bbdce4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116647"
---
# <a name="iwiauiextension2devicedialog-method"></a>IWiaUIExtension2 ::D méthode eviceDialog

Fournit une interface utilisateur personnalisée qui remplace l’interface utilisateur système par défaut.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA2 *pDeviceDialogData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDeviceDialogData* \[ dans\]
</dt> <dd>

Type : **PDEVICEDIALOGDATA2 \***

Pointe vers une structure [**DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) qui contient toutes les données nécessaires pour implémenter la boîte de dialogue de l’appareil.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **HRESULT**

Si la méthode est réussie, elle retourne la valeur \_ OK. Si l’utilisateur annule la boîte de dialogue, la méthode retourne S \_ false. Si la méthode échoue, elle retourne un code d’erreur approprié. Le tableau suivant présente certains des codes d’état de retour possibles.



| Code d'erreur    | Description                              |
|---------------|------------------------------------------|
| E \_ INVALIDARG | Le paramètre pDeviceDialogData a la **valeur null**. |
| \_NOTIMPL E    | Cette méthode n'est pas implémentée.           |



 

## <a name="remarks"></a>Notes 

Si vous implémentez l’interface [**IWiaUIExtension2**](-wia-iwiauiextension2.md) et que vous ne souhaitez pas remplacer l’interface utilisateur système, cette méthode doit encore être implémentée, mais elle ne doit rien faire d’autre que retourner E \_ NOTIMPL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




