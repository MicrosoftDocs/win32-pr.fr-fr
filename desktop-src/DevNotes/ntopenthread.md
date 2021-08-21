---
description: Ouvre un handle vers un objet thread avec l’accès spécifié.
ms.assetid: 85148f27-cfb4-4a33-8bcc-e48d2c2e3c51
title: NtOpenThread fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenThread
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: e5f459b12d90a12b7c75aabd44d25f6fcf352aff8914e6d991471acaee400260
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079689"
---
# <a name="ntopenthread-function"></a>NtOpenThread fonction)

\[cette fonction peut être modifiée ou supprimée de Windows sans préavis. Utilisez à la place la fonction [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) .\]

Ouvre un handle vers un objet thread avec l’accès spécifié.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS NtOpenThread(
  _Out_ PHANDLE            ThreadHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes,
  _In_  PCLIENT_ID         ClientId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ThreadHandle* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le handle de l’objet thread.

</dd> <dt>

*DesiredAccess* \[ dans\]
</dt> <dd>

Type de données de [**\_ masque d’accès**](../secauthz/access-mask-format.md) qui fournit les types d’accès souhaités pour l’objet thread.

</dd> <dt>

*ObjectAttributes* \[ dans\]
</dt> <dd>

Pointeur vers une structure [d' \_ attributs d’objet](https://msdn.microsoft.com/library/aa491657.aspx) . Le membre **ObjectName** de cette structure doit avoir la valeur null.

**Windows Server 2003 et Windows XP :** Le membre **ObjectName** de cette structure peut pointer vers un nom d’objet. Si **ObjectName** n’a pas la valeur null, le paramètre *ClientID* doit avoir la valeur null.

</dd> <dt>

*ClientID* \[ dans\]
</dt> <dd>

Pointeur vers une structure **d' \_ ID client** qui identifie le thread dont le thread doit être ouvert.

**Windows Server 2003 et Windows XP :** Pointeur vers une structure **d' \_ ID client** qui identifie le thread dont le thread doit être ouvert. Ce paramètre peut être NULL. Si ce paramètre n’est pas NULL, le membre **ObjectName** de la structure vers laquelle pointe le paramètre *ObjectAttributes* doit avoir la valeur null.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un code **NTSTATUS** ou d’erreur.

Les formulaires et la signification des codes d’erreur de **NTSTATUS** sont répertoriés dans le fichier d’en-tête Ntstatus. h disponible dans le kit WDK et sont décrits dans la documentation WDK.

## <a name="remarks"></a>Remarques

Cette fonction n’a aucun fichier d’en-tête associé. La bibliothèque d’importation associée, ntdll. lib, est disponible dans le kit WDK. Vous pouvez également utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Ntdll.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
