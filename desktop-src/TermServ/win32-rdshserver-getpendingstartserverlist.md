---
title: Méthode GetPendingStartServerList de la classe Win32_RDSHServer
description: Récupère une liste de serveurs en attente de démarrage.
ms.assetid: 7af7a0e7-dc00-4e3a-8e0c-5987bd2bc3a2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetPendingStartServerList
- Services Bureau à distance de la méthode GetPendingStartServerList, classe Win32_RDSHServer
- Win32_RDSHServer de la classe Services Bureau à distance, méthode GetPendingStartServerList
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetPendingStartServerList
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99b96453b33f931b18d89f13413513d3baf82bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384756"
---
# <a name="getpendingstartserverlist-method-of-the-win32_rdshserver-class"></a>Méthode GetPendingStartServerList de la \_ classe Win32 RDSHServer

Récupère une liste de serveurs en attente de démarrage.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetPendingStartServerList(
  [in]  uint32 maxServers,
  [out] string ServerFQDNs[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*maxServers* \[ dans\]
</dt> <dd>

Nombre maximal de serveurs à retourner dans la liste.

</dd> <dt>

*ServerFQDNs* \[ à\]
</dt> <dd>

En cas de réussite, contient une collection de noms de domaine complets des serveurs en attente de démarrage.

</dd> </dl>

## <a name="remarks"></a>Notes

La liste des serveurs est réinitialisée après chaque appel, de sorte que l’appel suivant n’obtiendra pas de serveur dupliqué.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                              |
| Espace de noms<br/>                | Racine \\ cimv2 cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_RDSHServer Win32**](win32-rdshserver.md)
</dt> </dl>

 

 





