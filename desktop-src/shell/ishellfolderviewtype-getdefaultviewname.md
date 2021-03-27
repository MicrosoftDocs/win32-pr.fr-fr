---
description: Obtient le nom de la vue par défaut. Appelez GetDisplayNameOf pour récupérer les noms des autres vues.
title: 'IShellFolderViewType :: GetDefaultViewName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetDefaultViewName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 99229d13-40dc-4750-81a7-48a2f608b778
ms.openlocfilehash: 239fcd80bcfc0b29287f8e16aeef3efb8ae032c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972342"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a>IShellFolderViewType :: GetDefaultViewName, méthode

Obtient le nom de la vue par défaut. Appelez [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) pour récupérer les noms des autres vues.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDefaultViewName(
  [in]  DWORD  uFlags,
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*uFlags* \[ dans\]
</dt> <dd>

Type : **DWORD**

Indicateurs facultatifs ; doit être défini sur 0.

</dd> <dt>

*ppwszName* \[ à\]
</dt> <dd>

Tapez : **LPWStr \** _

Adresse d’un pointeur de chaîne qui reçoit le nom de vue par défaut. La mémoire pour la chaîne est allouée avec [_ *SHStrDup* *](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




