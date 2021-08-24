---
description: Sous-classe un contrôle individuel, sauf si le contrôle s’affiche dans une boîte de dialogue.
ms.assetid: 07a2bce1-4c69-4f8d-bb24-b17351f5e771
title: Ctl3dSubclassCtl fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: f1d25bdc189ad80f1976ee76cc7f9909d099f34c8a88b83771ebf3f297c78934
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654479"
---
# <a name="ctl3dsubclassctl-function"></a>Ctl3dSubclassCtl fonction)

Sous-classe un contrôle individuel, sauf si le contrôle s’affiche dans une boîte de dialogue.

## <a name="syntax"></a>Syntaxe


```C++
BOOL Ctl3dSubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de la fenêtre de contrôle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si le contrôle est sous-classé avec succès ; Sinon, elle retourne **false**.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Ctl3dUnsubclassCtl**](ctl3dunsubclassctl.md)
</dt> </dl>

 

 
