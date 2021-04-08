---
title: CleanupCredentialCache fonction)
description: Implémenté par certains fournisseurs de support de sécurité (SSP) pour vider le cache des informations d’identification SSP.
ms.assetid: e60870e6-22d3-4321-abca-a5b9d2b0ce2d
keywords:
- CleanupCredentialCache fonction WinINet
topic_type:
- apiref
api_name:
- CleanupCredentialCache
api_location:
- MSNSSPC.dll
- MSAPSSPC.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53464073dd59837ba8026bbec03118055fba20cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102928"
---
# <a name="cleanupcredentialcache-function"></a>CleanupCredentialCache fonction)

La fonction **CleanupCredentialCache** est implémentée par certains fournisseurs de support de sécurité (SSP) pour vider le cache des informations d’identification SSP.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI CleanupCredentialCache(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

**True** si la fonction est réussie ; Sinon, **false**.

## <a name="remarks"></a>Notes

La fonction **CleanupCredentialCache** est implémentée par les SSP suivants :

-   MSNSSPC.dll
-   MSAPSSPC.dll

L’implémentation de **CleanupCredentialCache** par ces SSP retourne toujours **true**.

Avant de tenter d’obtenir un handle de module pour exporter **CleanupCredentialCache**, l’application doit vérifier que le fournisseur de services partagés qui a été chargé est l’un des SSP connus qui implémente la fonction **CleanupCredentialCache** .

Pour vider le cache des informations d’identification SSP, l’application doit obtenir un handle de module pour le fournisseur de services partagés en appelant la fonction [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) . Une fois le module obtenu, l’application doit exporter la fonction **CleanupCredentialCache** implémentée par le fournisseur de services partagés en appelant la fonction [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) , en passant le module retourné par **GetModuleHandle** et **CleanupCredentialCache** en tant que paramètres d’entrée.

Comme tous les autres aspects de l’API WinINet, cette fonction ne peut pas être appelée en toute sécurité à partir de DllMain ou des constructeurs et des destructeurs d’objets globaux.

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                                 |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                       |
| DLL<br/>                      | <dl> <dt>MSNSSPC.dll ; </dt> <dt>MSAPSSPC.dll</dt> </dl> |



 

