---
description: Reconstruit un pointeur vers une liste d’identificateurs d’éléments (PIDL) à partir d’une représentation hiérarchique du dossier de Shell dans une représentation différente.
title: 'IShellFolderViewType :: TranslateViewPidl, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.TranslateViewPidl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b7fa6c4-3d02-44ed-b63d-80a799e4017a
ms.openlocfilehash: 75876e5088c610c1f9f02ba9374db5cea4a6023c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527310"
---
# <a name="ishellfolderviewtypetranslateviewpidl-method"></a>IShellFolderViewType :: TranslateViewPidl, méthode

Reconstruit un pointeur vers une liste d’identificateurs d’éléments (PIDL) à partir d’une représentation hiérarchique du dossier de Shell dans une représentation différente.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT TranslateViewPidl(
  [in] PCUIDLIST_RELATIVE pidl,
  [in] PCUIDLIST_RELATIVE pidlView,
  [in] PCUIDLIST_RELATIVE *ppidlOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PIDL* \[ dans\]
</dt> <dd>

Type : **PCUIDLIST \_ relatif**

Tableau d’ID d’élément par rapport au dossier racine.

</dd> <dt>

*pidlView* \[ dans\]
</dt> <dd>

Type : **PCUIDLIST \_ relatif**

PIDL spéciale de la vue.

</dd> <dt>

*ppidlOut* \[ dans\]
</dt> <dd>

Type : **PCUIDLIST \_ relatif \** _

Adresse d’une variable PIDL pour recevoir la traduction.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Lorsque vous avez terminé, vous devez libérer le PIDL retourné avec [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




