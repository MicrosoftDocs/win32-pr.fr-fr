---
title: PxeProviderShutdown fonction de rappel
description: Appelé pour arrêter le fournisseur.
ms.assetid: 436d7428-18f9-4b73-b346-79c9a0738c31
keywords:
- Fonction de rappel PxeProviderShutdown des services de déploiement Windows
topic_type:
- apiref
api_name:
- PxeProviderShutdown
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17698c5fa1f6ce6bd5443d0244ebc6ce6082ec33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509103"
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
| Serveur minimal pris en charge<br/> | Windows Server 2008, Windows Server 2003 avec les \[ applications de bureau SP2 uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions du serveur des services de déploiement Windows](windows-deployment-services-server-functions.md)
</dt> <dt>

[*PxeProviderInitialize*](pxeproviderinitialize.md)
</dt> <dt>

[**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

 





