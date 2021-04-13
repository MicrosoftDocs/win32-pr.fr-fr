---
title: Méthode GetActiveServer de la classe Win32_RDMSEnvironment
description: Récupère le nom de domaine complet (FQDN) de l’environnement Bureau à distance Management Services (RDMS).
ms.assetid: 87e25d11-de1d-41d1-974d-2871dde444b5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetActiveServer
- Services Bureau à distance de la méthode GetActiveServer, classe Win32_RDMSEnvironment
- Win32_RDMSEnvironment de la classe Services Bureau à distance, méthode GetActiveServer
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4265315e3ed2de87e564adab87c023401bbd55e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465802"
---
# <a name="getactiveserver-method-of-the-win32_rdmsenvironment-class"></a>Méthode GetActiveServer de la \_ classe Win32 RDMSEnvironment

Récupère le nom de domaine complet (FQDN) de l’environnement Bureau à distance Management Services (RDMS).

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetActiveServer(
  [out] string ServerName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom du serveur* \[ à\]
</dt> <dd>

Reçoit le nom de domaine complet récupéré.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                              |
| Espace de noms<br/>                | Racine \\ cimv2 cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_RDMSEnvironment Win32**](win32-rdmsenvironment.md)
</dt> </dl>

 

 





