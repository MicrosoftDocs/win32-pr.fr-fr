---
description: Obtient les propriétés de la vue.
title: 'IShellFolderViewType :: GetViewTypeProperties, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetViewTypeProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 82be6bd5-a46c-48b3-a1f0-a92b9454c35e
ms.openlocfilehash: f4368edf6eae3e6892a3d81147401e061548f6e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972335"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a>IShellFolderViewType :: GetViewTypeProperties, méthode

Obtient les propriétés de la vue.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetViewTypeProperties(
  [in]  PCUITEMID_CHILD pidl,
  [out] DWORD           *pdwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PIDL* \[ dans\]
</dt> <dd>

Type : **\_ enfant PCUITEMID**

PIDL.

</dd> <dt>

*pdwFlags* \[ à\]
</dt> <dd>

Type : **DWORD \** _

Pointeur vers une variable entière non signée qui reçoit les propriétés de la vue, qui indiquent la marche à suivre lorsque la vue est sélectionnée. Les indicateurs peuvent être n’importe quelle combinaison des valeurs suivantes.

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>_ *SFVTFLAG \_ Notify \_ Create** (0x00000001)


</dt> <dd>

Créer un élément d’affichage s’il n’y est pas.

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG \_ NOTIFIer le \_ Resort** (0x00000002)


</dt> <dd>

Réinsérez PIDL et retriez.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




