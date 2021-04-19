---
description: Compare deux jetons d’accès et détermine s’ils sont équivalents par rapport à un appel à la fonction AccessCheck.
ms.assetid: 3a07ddc6-9748-4f96-a597-2af6b4282e56
title: NtCompareTokens, fonction (Ntseapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtCompareTokens
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: d4d0f35bff8fa65e0e09be32a55281b5118f244c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524609"
---
# <a name="ntcomparetokens-function"></a>NtCompareTokens fonction)

La fonction **NtCompareTokens** compare deux [*jetons d’accès*](/windows/desktop/SecGloss/a-gly) et détermine s’ils sont équivalents par rapport à un appel à la fonction [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) .

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS NTAPI NtCompareTokens(
  _In_  HANDLE   FirstTokenHandle,
  _In_  HANDLE   SecondTokenHandle,
  _Out_ PBOOLEAN Equal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FirstTokenHandle* \[ dans\]
</dt> <dd>

Handle vers le premier jeton d’accès à comparer. Le jeton doit être ouvert pour l’accès à la **\_ requête de jeton** .

</dd> <dt>

*SecondTokenHandle* \[ dans\]
</dt> <dd>

Handle vers le deuxième jeton d’accès à comparer. Le jeton doit être ouvert pour l’accès à la **\_ requête de jeton** .

</dd> <dt>

*Égal* \[ à à\]
</dt> <dd>

Pointeur vers une variable qui reçoit une valeur qui indique si les jetons représentés par les paramètres *FirstTokenHandle* et *SecondTokenHandle* sont équivalents.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la fonction retourne l’état \_ Success.

Si la fonction échoue, elle retourne un code d’erreur **NTSTATUS** .

## <a name="remarks"></a>Notes

Deux jetons de contrôle d’accès sont considérés comme équivalents si toutes les conditions suivantes sont remplies :

-   Chaque [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) qui est présent dans l’un des jetons est également présent dans l’autre jeton.
-   Aucun ou les deux jetons ne sont limités.
-   Si les deux jetons sont restreints, chaque SID qui est limité dans un jeton est également limité dans l’autre jeton.
-   Chaque privilège présent dans l’un des deux jetons est également présent dans l’autre jeton.

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Ntseapi. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

