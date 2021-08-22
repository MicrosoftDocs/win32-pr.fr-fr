---
title: PxeProviderInitialize fonction de rappel
description: Exportation à partir d’une bibliothèque de liens dynamiques (DLL) de fournisseur qui initialise le fournisseur et la prépare à recevoir des demandes du client.
ms.assetid: 433b051c-9fde-4589-92e2-58d3774826ac
keywords:
- fonction de rappel PxeProviderInitialize Windows les Services de déploiement
topic_type:
- apiref
api_name:
- PxeProviderInitialize
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6eb7ba32049dc3ef70085a489b499d90b92ec6155323b650df0e2b2f839bbdf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098659"
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
| Serveur minimal pris en charge<br/> | Windows serveur 2008, Windows server 2003 avec les \[ applications de bureau SP2 uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Windows Fonctions du serveur des services de déploiement](windows-deployment-services-server-functions.md)
</dt> <dt>

[*PxeProviderShutdown*](pxeprovidershutdown.md)
</dt> </dl>

 

 





