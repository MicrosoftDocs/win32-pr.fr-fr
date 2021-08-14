---
description: Vérifie que le profil utilisateur en ligne est chargé.
ms.assetid: 4391664E-44D0-461D-84FF-E2B2410511BC
title: OnProfileLoaded, fonction (Lsaidprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnProfileLoaded
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: 6a8ed0d96ab7c9c63f9574472cac0daedba54e42beec244271efcc309c04dd95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921143"
---
# <a name="onprofileloaded-function"></a>OnProfileLoaded fonction)

Vérifie que le profil utilisateur en ligne est chargé.

## <a name="syntax"></a>Syntaxe


```C++
SEC_ENTRY OnProfileLoaded(
  _In_ PVOID   ProviderHandle,
  _In_ HANDLE  UserToken,
  _In_ BOOLEAN Loaded
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ProviderHandle* \[ dans\]
</dt> <dd>

Handle du fournisseur.

</dd> <dt>

*UserToken* \[ dans\]
</dt> <dd>

Jeton de l’utilisateur dont le profil est chargé ou déchargé.

</dd> <dt>

*Chargé* \[ dans\]
</dt> <dd>

**True** si le profil a été chargé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la fonction retourne l’état \_ Success.

Si la fonction échoue, la fonction retourne un code d’erreur différent de zéro qui est une erreur spécifique au fournisseur à des fins de diagnostic.

## <a name="remarks"></a>Remarques

Cette fonction est appelée chaque fois que la fonction [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) est appelée. Elle n’est pas synchronisée avec **LoadUserProfile**; autrement dit, **LoadUserProfile** peut avoir retourné et le profil a peut-être été déchargé au moment où la fonction a été appelée. Cette fonction peut être appelée plusieurs fois, même lorsque le profil a été chargé. Le fournisseur d’identité ne doit pas supposer qu’un appel à cette fonction avec *Loaded* égal à true sera suivi d’un appel avec *Loaded* égal à false.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Lsaidprov. h</dt> </dl> |



 

 
