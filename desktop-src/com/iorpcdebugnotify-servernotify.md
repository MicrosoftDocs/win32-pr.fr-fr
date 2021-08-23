---
title: Méthode IOrpcDebugNotify ServerNotify
description: Informe le serveur d’une demande de débogueur entrant du client.
ms.assetid: 6c868b9e-f25b-4d27-80ff-697d0c005b8d
keywords:
- Méthode ServerNotify COM
- Méthode ServerNotify COM, interface IOrpcDebugNotify
- Interface IOrpcDebugNotify COM, méthode ServerNotify
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ServerNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff0faac4ee4e5fa691088afa9de8871a8bf9382ce3da629b3fc14dd9d932ab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048097"
---
# <a name="iorpcdebugnotifyservernotify-method"></a>IOrpcDebugNotify :: ServerNotify, méthode

Informe le serveur d’une demande de débogueur entrant du client.

> [!Note]  
> une bibliothèque d’importation contenant la fonction **ServerNotify** n’est pas incluse dans le kit de développement logiciel (SDK) Microsoft Windows. Une application peut utiliser les fonctions [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) pour récupérer un pointeur de fonction vers [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) à partir de oleaut.dll et fournir cette fonction par le biais de l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

 

## <a name="syntax"></a>Syntaxe


```C++
void ServerNotify(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpOrpcDebugAll* 
</dt> <dd>

Pointeur vers une structure [**ORPC \_ dbg \_ All**](orpc-dbg-all.md) qui contient des informations spécifiques à la notification que le système RPC com transmet au débogueur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                     |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>N/A</dt> </dl> |
| MIDL<br/>                      | <dl> <dt>N/A</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ORPC \_ init \_ args**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

