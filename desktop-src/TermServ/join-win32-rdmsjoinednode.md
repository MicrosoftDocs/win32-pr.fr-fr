---
title: Méthode Join de la classe Win32_RDMSJoinedNode
description: Ajoute un nœud à Bureau à distance Management Services (RDMS).
ms.assetid: 7451d12a-ace2-4564-bf6d-fb0169be967f
ms.tgt_platform: multiple
keywords:
- Méthode Join Services Bureau à distance
- Méthode Join Services Bureau à distance, classe Win32_RDMSJoinedNode
- Services Bureau à distance de la classe Win32_RDMSJoinedNode, méthode Join
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Join
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587e68758971453e8c4e307ccb37ce6cede262f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384155"
---
# <a name="join-method-of-the-win32_rdmsjoinednode-class"></a>Méthode Join de la \_ classe RDMSJoinedNode Win32

Ajoute un nœud à Bureau à distance Management Services (RDMS).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Join(
  [in] string NodeFQDN,
  [in] string NodeSID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NodeFQDN* \[ dans\]
</dt> <dd>

Nom de domaine complet du nœud.

</dd> <dt>

*NodeSID* \[ dans\]
</dt> <dd>

Identificateur de sécurité (SID) du nœud.

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

[**\_RDMSJoinedNode Win32**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





