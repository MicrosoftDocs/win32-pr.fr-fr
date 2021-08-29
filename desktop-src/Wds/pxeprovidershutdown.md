---
title: PxeProviderShutdown fonction de rappel
description: Appelé pour arrêter le fournisseur.
ms.assetid: 436d7428-18f9-4b73-b346-79c9a0738c31
keywords:
- fonction de rappel PxeProviderShutdown Windows les Services de déploiement
topic_type:
- apiref
api_name:
- PxeProviderShutdown
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5efc7267a5b5e1c15d185b96419210f31981c56c887dd5a8ab7f1068eb4f20ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860789"
---
# <a name="pxeprovidershutdown-callback-function"></a>PxeProviderShutdown fonction de rappel

Appelé pour arrêter le fournisseur. Cette fonction est inscrite en appelant la fonction [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) avec le paramètre *CallbackType* défini **sur \_ \_ arrêt du rappel PXE**. Une fois cette fonction appelée, le handle *hProvider* passé à la fonction [*PxeProviderInitialize*](pxeproviderinitialize.md) n’est plus valide.

## <a name="syntax"></a>Syntaxe


```C++
DWORD PXEAPI PxeProviderShutdown(
  _In_ PVOID pContext
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pContext* \[ dans\]
</dt> <dd>

Valeur de contexte passée à la fonction [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’arrêt du fournisseur réussit, le rappel doit retourner la **\_ réussite** de l’erreur. En cas d’échec, un code d’erreur approprié doit être retourné.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                          |
| Serveur minimal pris en charge<br/> | Windows serveur 2008, Windows server 2003 avec les \[ applications de bureau SP2 uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Windows Fonctions du serveur des services de déploiement](windows-deployment-services-server-functions.md)
</dt> <dt>

[*PxeProviderInitialize*](pxeproviderinitialize.md)
</dt> <dt>

[**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

 





