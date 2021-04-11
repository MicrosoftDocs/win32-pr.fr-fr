---
title: MirrorIcon fonction)
description: Inverse (met en miroir) les icônes afin qu’elles s’affichent correctement sur un contexte de périphérique en miroir.
ms.assetid: bca87037-1789-466b-9be0-914966fdad31
keywords:
- Contrôles Windows de la fonction MirrorIcon
topic_type:
- apiref
api_name:
- MirrorIcon
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02f180d509464b63e5ec73c5fb74e4d70386bdea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032489"
---
# <a name="mirroricon-function"></a>MirrorIcon fonction)

\[**MirrorIcon** est disponible via Windows XP avec Service Pack 2 (SP2). Il peut être modifié ou non disponible dans les versions ultérieures.\]

Inverse (met en miroir) les icônes afin qu’elles s’affichent correctement sur un contexte de périphérique en miroir.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI MirrorIcon(
  _Inout_opt_ HICON *phIconSmall,
  _Inout_opt_ HICON *phIconLarge
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*phIconSmall* \[ in, out, facultatif\]
</dt> <dd>

Type : **[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _

Pointeur vers le handle d’icône qui fait référence à une petite version d’une icône.

</dd> <dt>

_phIconLarge * \[ in, out, facultatif\]
</dt> <dd>

Type : **[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _

Pointeur vers le handle d’icône qui fait référence à une grande version d’une icône.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *[**bool**](/windows/desktop/WinProg/windows-data-types)**

**True** en cas de réussite ; Sinon, **false**.

## <a name="remarks"></a>Notes

**MirrorIcon** n’est pas exporté par nom ou déclaré dans un fichier d’en-tête public. Pour l’utiliser, vous devez utiliser [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et demander l’ordinal 414 de ComCtl32.dll pour obtenir un pointeur de fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (version 5,81 ou ultérieure)</dt> </dl> |



 

