---
title: Méthode IOrpcDebugNotify ClientNotify
description: Informe le client d’une demande de débogueur sortant au serveur.
ms.assetid: a41e3eaa-6d1f-46bf-9103-f83e45b2cd90
keywords:
- Méthode ClientNotify COM
- Méthode ClientNotify COM, interface IOrpcDebugNotify
- Interface IOrpcDebugNotify COM, méthode ClientNotify
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e788a51e278df09715aaf9d4993ac5724ed65b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855513"
---
# <a name="iorpcdebugnotifyclientnotify-method"></a>IOrpcDebugNotify :: ClientNotify, méthode

Informe le client d’une demande de débogueur sortant au serveur.

> [!Note]  
> une bibliothèque d’importation contenant la fonction **ClientNotify** n’est pas incluse dans le kit de développement logiciel (SDK) Microsoft Windows. Une application peut utiliser les fonctions [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) pour récupérer un pointeur de fonction vers [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) à partir de oleaut.dll et fournir cette fonction par le biais de l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

 

## <a name="syntax"></a>Syntaxe


```C++
void ClientNotify(
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

 

