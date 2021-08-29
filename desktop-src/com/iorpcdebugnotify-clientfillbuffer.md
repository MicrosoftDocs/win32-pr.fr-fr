---
title: Méthode IOrpcDebugNotify ClientFillBuffer
description: Envoie des données du débogueur client au débogueur de serveur.
ms.assetid: d575cf34-34a2-4951-a87e-7835b2c5b7a0
keywords:
- Méthode ClientFillBuffer COM
- Méthode ClientFillBuffer COM, interface IOrpcDebugNotify
- Interface IOrpcDebugNotify COM, méthode ClientFillBuffer
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientFillBuffer
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db0063f980e500481adcd3848e7227762f81603bf71ace525745b3fa2e535d91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854289"
---
# <a name="iorpcdebugnotifyclientfillbuffer-method"></a>IOrpcDebugNotify :: ClientFillBuffer, méthode

Envoie des données du débogueur client au débogueur de serveur.

> [!Note]  
> une bibliothèque d’importation contenant la fonction **ClientFillBuffer** n’est pas incluse dans le kit de développement logiciel (SDK) Microsoft Windows. Une application peut utiliser les fonctions [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) pour récupérer un pointeur de fonction vers [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) à partir de oleaut.dll et fournir cette fonction par le biais de l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

 

## <a name="syntax"></a>Syntaxe


```C++
void ClientFillBuffer(
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

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

