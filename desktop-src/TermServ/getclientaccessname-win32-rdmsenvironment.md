---
title: Méthode GetClientAccessName de la classe Win32_RDMSEnvironment
description: Récupère le nom de l’enregistrement de ressource (RR) du système de noms de domaine (DNS) de l’environnement des services de gestion de Bureau à distance (RDMS).
ms.assetid: 16f9d00d-a398-4a73-a641-ac552ba6a9d3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetClientAccessName
- Services Bureau à distance de la méthode GetClientAccessName, classe Win32_RDMSEnvironment
- Win32_RDMSEnvironment de la classe Services Bureau à distance, méthode GetClientAccessName
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54662cf1f27c53f3bf69398a203bfdfce1e53c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008638"
---
# <a name="getclientaccessname-method-of-the-win32_rdmsenvironment-class"></a>Méthode GetClientAccessName de la \_ classe Win32 RDMSEnvironment

Récupère le nom de l’enregistrement de ressource (RR) du système de noms de domaine (DNS) de l’environnement des services de gestion de Bureau à distance (RDMS).

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetClientAccessName(
  [out] string ClientAccessName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ClientAccessName* \[ à\]
</dt> <dd>

Reçoit le nom de l’enregistrement de ressource récupéré.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

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

 

 





