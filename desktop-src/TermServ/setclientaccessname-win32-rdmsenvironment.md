---
title: Méthode SetClientAccessName de la classe Win32_RDMSEnvironment
description: Met à jour le nom de l’enregistrement de ressource DNS (Domain Name System) d’un environnement Bureau à distance Management Services (RDMS).
ms.assetid: bbce3fc1-d2c5-4874-bdd0-be27fb5981d1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetClientAccessName
- Services Bureau à distance de la méthode SetClientAccessName, classe Win32_RDMSEnvironment
- Win32_RDMSEnvironment de la classe Services Bureau à distance, méthode SetClientAccessName
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbb962a6dd1600ad0cd439f7f34772f69d91b925308e2247e1283575d8f68cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604871"
---
# <a name="setclientaccessname-method-of-the-win32_rdmsenvironment-class"></a>Méthode SetClientAccessName de la \_ classe Win32 RDMSEnvironment

Met à jour le nom de l’enregistrement de ressource DNS (Domain Name System) d’un environnement Bureau à distance Management Services (RDMS).

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetClientAccessName(
  [in] string ClientAccessName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ClientAccessName* \[ dans\]
</dt> <dd>

Nouveau nom du RR.

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

 

 





