---
title: Méthode IOrpcDebugNotify ServerGetBufferSize
description: Récupère la taille de la mémoire tampon RPC à partir du débogueur côté serveur.
ms.assetid: 1e9ef194-c85b-4f6d-8b89-1f7ee6941189
keywords:
- Méthode ServerGetBufferSize COM
- Méthode ServerGetBufferSize COM, interface IOrpcDebugNotify
- Interface IOrpcDebugNotify COM, méthode ServerGetBufferSize
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ServerGetBufferSize
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d461670cc65f5cfcb433a52529e724a1c54bede
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855501"
---
# <a name="iorpcdebugnotifyservergetbuffersize-method"></a>IOrpcDebugNotify :: ServerGetBufferSize, méthode

Récupère la taille de la mémoire tampon RPC à partir du débogueur côté serveur.

> [!Note]  
> une bibliothèque d’importation contenant la fonction **ServerGetBufferSize** n’est pas incluse dans le kit de développement logiciel (SDK) Microsoft Windows. Une application peut utiliser les fonctions [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) pour récupérer un pointeur de fonction vers [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) à partir de oleaut.dll et fournir cette fonction par le biais de l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

 

## <a name="syntax"></a>Syntaxe


```C++
void ServerGetBufferSize(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpOrpcDebugAll* 
</dt> <dd>

Pointeur vers une structure [**ORPC \_ dbg \_ All**](orpc-dbg-all.md) qui contient des informations spécifiques à la notification que le système RPC com transmet au débogueur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Spécifications



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

 

