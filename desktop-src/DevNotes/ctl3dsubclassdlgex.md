---
description: Sous-classe tous les contrôles dans une boîte de dialogue et dans la fenêtre de dialogue elle-même.
ms.assetid: 4d3c298b-07ba-4668-badd-dddecc389e70
title: Ctl3dSubclassDlgEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassDlgEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: aeacdf75e20e2d3521405c20b52d29a466c5fe9a063d70e5acb3c0597934ab9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162130"
---
# <a name="ctl3dsubclassdlgex-function"></a>Ctl3dSubclassDlgEx fonction)

Sous-classe tous les contrôles dans une boîte de dialogue et dans la fenêtre de dialogue elle-même.

## <a name="syntax"></a>Syntaxe


```C++
PUBLIC BOOL FAR PASCAL Ctl3dSubclassDlgEx(
   HWND  hwndDlg,
   DWORD grbit
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hwndDlg* 
</dt> <dd>

Handle de la fenêtre de boîte de dialogue.

</dd> <dt>

*grbit* 
</dt> <dd>

Types de contrôle à sous-classer. Cette valeur peut être l’une des suivantes :



| Valeur                                                                                                                                                                                                                                     | Signification                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="CTL3D_BUTTONS"></span><span id="ctl3d_buttons"></span><dl> <dt>**CTL3D \_ BOUTONS**</dt> <dt>0x0001</dt> </dl>                 | Boutons de sous-classe.<br/>                  |
| <span id="CTL3D_LISTBOXES"></span><span id="ctl3d_listboxes"></span><dl> <dt>**CTL3D \_ ZONES de liste**</dt> <dt>0x0002</dt> </dl>           | Zones de liste sous-classe.<br/>               |
| <span id="CTL3D_EDITS"></span><span id="ctl3d_edits"></span><dl> <dt>**CTL3D \_ MODIFIE**</dt> <dt>0x0004</dt> </dl>                       | Contrôles d’édition de sous-classes.<br/>            |
| <span id="CTL3D_COMBOS"></span><span id="ctl3d_combos"></span><dl> <dt>**CTL3D \_ COMBOS**</dt> <dt>0x0008</dt> </dl>                    | Zones de liste déroulante de sous-classe.<br/>              |
| <span id="CTL3D_STATICTEXTS"></span><span id="ctl3d_statictexts"></span><dl> <dt>**CTL3D \_ STATICTEXTS**</dt> <dt>0x0010</dt> </dl>     | Sous-classe les contrôles de texte statique.<br/>     |
| <span id="CTL3D_STATICFRAMES"></span><span id="ctl3d_staticframes"></span><dl> <dt>**CTL3D \_ STATICFRAMES**</dt> <dt>0x0020</dt> </dl>  | Trames statiques de sous-classe.<br/>            |
| <span id="CTL3D_ALL"></span><span id="ctl3d_all"></span><dl> <dt>**CTL3D \_ Toutes les**</dt> <dt>0xFFFF</dt> </dl>                             | Sous-classez tous les contrôles.<br/>             |
| <span id="CTL3D_NODLGWINDOW"></span><span id="ctl3d_nodlgwindow"></span><dl> <dt>**CTL3D \_ NODLGWINDOW**</dt> <dt>0x00010000</dt> </dl> | Ne sous-classez pas la fenêtre de boîte de dialogue.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si la fonction est réussie ; Sinon, elle retourne **false**.

## <a name="remarks"></a>Remarques

Cette fonction est particulièrement utile dans les applications basées sur C++.

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
