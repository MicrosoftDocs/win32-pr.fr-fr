---
title: Interface IOrpcDebugNotify
description: Fournit des fonctionnalités de débogage distant.
ms.assetid: f91987c0-2e4b-4872-8ed6-e208a23baa49
keywords:
- Interface IOrpcDebugNotify COM
- Interface IOrpcDebugNotify COM, Description
topic_type:
- apiref
api_name:
- IOrpcDebugNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4db08daf93997b2a7fa0ed383591cb5d111ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519057"
---
# <a name="iorpcdebugnotify-interface"></a>Interface IOrpcDebugNotify

Fournit des fonctionnalités de débogage distant.

## <a name="when-to-implement"></a>Quand implémenter

Implémentez cette interface pour activer le débogage à distance sur RPC.

## <a name="when-to-use"></a>Quand l’utiliser

Cette interface doit être utilisée pour le débogage distant in-process quand les exceptions logicielles ne doivent pas être utilisées pour les notifications du débogueur COM. Elle permet aux débogueurs in-process d’être avertis par des appels directs à l’aide de ces méthodes.

## <a name="members"></a>Membres

L’interface **IOrpcDebugNotify** hérite de l’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . **IOrpcDebugNotify** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IOrpcDebugNotify** possède ces méthodes.



| Méthode                                                              | Description                                                                    |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md)       | Envoie des données du débogueur client au débogueur de serveur.<br/>         |
| [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) | Récupère la taille de la mémoire tampon RPC à partir du débogueur côté client.<br/>        |
| [**ClientNotify**](iorpcdebugnotify-clientnotify.md)               | Informe le client d’une demande de débogueur sortant au serveur.<br/>   |
| [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)       | Envoie des données du débogueur de serveur au débogueur client.<br/>         |
| [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) | Récupère la taille de la mémoire tampon RPC à partir du débogueur côté serveur.<br/>        |
| [**ServerNotify**](iorpcdebugnotify-servernotify.md)               | Informe le serveur d’une demande de débogueur entrant du client.<br/> |



 

## <a name="remarks"></a>Notes

Une bibliothèque d’importation contenant l’interface **IOrpcDebugNotify** n’est pas incluse dans le kit de développement logiciel (SDK) Microsoft Windows. Une application peut utiliser les fonctions [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) pour récupérer un pointeur de fonction vers [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) à partir de oleaut.dll et fournir ces méthodes via l’interface **IOrpcDebugNotify** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                     |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>N/A</dt> </dl> |
| MIDL<br/>                      | <dl> <dt>N/A</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)
</dt> <dt>

[**ORPC \_ dbg \_ tout**](orpc-dbg-all.md)
</dt> <dt>

[**\_ \_ mémoire tampon dbg ORPC**](orpc-dbg-buffer.md)
</dt> <dt>

[**ORPC \_ init \_ args**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> </dl>

 

