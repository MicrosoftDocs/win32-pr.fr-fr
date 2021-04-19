---
title: Méthode GetJoinedNodeCount de la classe Win32_RDMSJoinedNode
description: Obtenir le nombre de serveurs sur lesquels sont installés les rôles spécifiés.
ms.assetid: ed2ae0b5-5cbc-4c11-a2ad-065f88dd5842
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetJoinedNodeCount
- Services Bureau à distance de la méthode GetJoinedNodeCount, classe Win32_RDMSJoinedNode
- Win32_RDMSJoinedNode de la classe Services Bureau à distance, méthode GetJoinedNodeCount
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.GetJoinedNodeCount
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ecc5c388814873aa690e9af5adda5081aad4d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106533569"
---
# <a name="getjoinednodecount-method-of-the-win32_rdmsjoinednode-class"></a>Méthode GetJoinedNodeCount de la \_ classe Win32 RDMSJoinedNode

Obtenir le nombre de serveurs sur lesquels sont installés les rôles spécifiés.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetJoinedNodeCount(
  [in]  uint32 roleType,
  [out] uint32 Count
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*roleType* \[ dans\]
</dt> <dd>

Champ de type de champ qui spécifie les types de rôles.

<dt>

0
</dt> <dd>

Tous

</dd> <dt>

1
</dt> <dd>

Connexion Bureau à distance Broker (RDCB)

</dd> <dt>

2
</dt> <dd>

Hôte de session Bureau à distance (hôte de session)

</dd> <dt>

4
</dt> <dd>

Serveur hôte de virtualisation des services Bureau à distance (RDVH)

</dd> </dl> </dd> <dt>

*Nombre* \[ à\]
</dt> <dd>

En cas de réussite, retourne le nombre de serveurs sur lesquels sont installés les rôles spécifiés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.

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

[**\_RDMSJoinedNode Win32**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





