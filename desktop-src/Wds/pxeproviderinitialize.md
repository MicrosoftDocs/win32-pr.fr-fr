---
title: PxeProviderInitialize fonction de rappel
description: Exportation à partir d’une bibliothèque de liens dynamiques (DLL) de fournisseur qui initialise le fournisseur et la prépare à recevoir des demandes du client.
ms.assetid: 433b051c-9fde-4589-92e2-58d3774826ac
keywords:
- Fonction de rappel PxeProviderInitialize des services de déploiement Windows
topic_type:
- apiref
api_name:
- PxeProviderInitialize
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b8d8fed4c1cc91c2090b957894b4f6641adad32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509356"
---
# <a name="pxeproviderinitialize-callback-function"></a>PxeProviderInitialize fonction de rappel

Exportation à partir d’une bibliothèque de liens dynamiques (DLL) de fournisseur qui initialise le fournisseur et la prépare à recevoir des demandes du client. Les fournisseurs sont requis pour exporter la fonction *PxeProviderInitialize* . Tous les rappels du fournisseur doivent être inscrits avec un appel à la fonction [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) pendant le traitement de *PxeProviderInitialize*. Au retour de cette fonction, le fournisseur doit être entièrement initialisé et prêt à traiter les demandes des clients.

## <a name="syntax"></a>Syntaxe


```C++
DWORD PXEAPI PxeProviderInitialize(
  _In_ HANDLE hProvider,
  _In_ HKEY   hProviderKey
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hProvider* \[ dans\]
</dt> <dd>

Handle de l’instance du fournisseur. Ce descripteur doit être stocké par le fournisseur et utilisé dans les appels suivants. Ce handle est valide jusqu’à ce que la fonction de rappel [*PxeProviderShutdown*](pxeprovidershutdown.md) soit appelée.

</dd> <dt>

*hProviderKey* \[ dans\]
</dt> <dd>

Handle d’une clé de Registre dans laquelle les informations de configuration du fournisseur doivent être stockées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’initialisation du fournisseur réussit, le rappel doit retourner **la \_ réussite** de l’erreur. En cas d’échec, un code d’erreur approprié doit être retourné.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008, Windows Server 2003 avec les \[ applications de bureau SP2 uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions du serveur des services de déploiement Windows](windows-deployment-services-server-functions.md)
</dt> <dt>

[*PxeProviderShutdown*](pxeprovidershutdown.md)
</dt> </dl>

 

 





