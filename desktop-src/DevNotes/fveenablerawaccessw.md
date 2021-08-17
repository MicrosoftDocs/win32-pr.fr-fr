---
description: Active ou désactive la lecture et l’écriture de secteurs de disque.
ms.assetid: 885e4db1-a131-4727-80ab-3be8c591b766
title: FveEnableRawAccessW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FveEnableRawAccessW
api_type:
- DllExport
api_location:
- Fveapi.dll
ms.openlocfilehash: 050983663b782d40c330092919b8fc29060cbba057a16d147b80c6ea477cbf54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956088"
---
# <a name="fveenablerawaccessw-function"></a>FveEnableRawAccessW fonction)

Active ou désactive la lecture et l’écriture de secteurs de disque.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FveEnableRawAccessW(
  _In_ PCWSTR VolumeName,
  _In_ BOOL   Enabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom_volume* \[ dans\]
</dt> <dd>

Identificateur unique du volume de disque.

</dd> <dt>

*Activé* \[ dans\]
</dt> <dd>

Si la **valeur est true**, autorise l’accès au volume brut. Si la **valeur est false**, aucun accès au volume brut n’est autorisé. Si l’accès brut a déjà été activé, mais que cette valeur est **false**, le volume est remonté et revalidés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                           | Description                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                           | La fonction a réussi.<br/>                                            |
| <dl> <dt>**S \_ FALSe**</dt> <dt>1 (0x1)</dt> </dl>                        | Enabled a la **valeur false** et le volume n’était pas déjà en mode d’accès brut.<br/> |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt> </dl> | Le volume ne peut pas être verrouillé.<br/>                                            |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Fveapi.dll</dt> </dl> |



 

 




