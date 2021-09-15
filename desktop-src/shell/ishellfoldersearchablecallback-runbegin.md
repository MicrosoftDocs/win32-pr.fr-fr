---
description: Indique qu’une recherche a été démarrée.
title: 'IShellFolderSearchableCallback :: RunBegin, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback.RunBegin
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6e3ae592-a0cb-4d9d-b186-241a757da5ea
ms.openlocfilehash: 953bf54ff64cf41724ce0dfabd064f9c7b980cc6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412439"
---
# <a name="ishellfoldersearchablecallbackrunbegin-method"></a>IShellFolderSearchableCallback :: RunBegin, méthode

Indique qu’une recherche a été démarrée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RunBegin(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwReserved* \[ dans\]
</dt> <dd>

Type : **DWORD**

Réservé. Doit avoir la valeur 0.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

En réponse à ce rappel, l’application peut activer le bouton **Annuler** , par exemple.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




