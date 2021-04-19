---
title: Méthode disjointe de la classe Win32_RDMSJoinedNode
description: Supprime un nœud de Bureau à distance services de gestion (RDMS).
ms.assetid: 37c462f4-a19d-4b85-8fac-2735deb7c04f
ms.tgt_platform: multiple
keywords:
- Méthode disjoin Services Bureau à distance
- Méthode disjoin Services Bureau à distance, classe Win32_RDMSJoinedNode
- Win32_RDMSJoinedNode de la classe Services Bureau à distance, méthode disjoin
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Unjoin
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234f7cc3ad8a797fff51661528f4545ed9fea3a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511567"
---
# <a name="unjoin-method-of-the-win32_rdmsjoinednode-class"></a>Méthode disjointe de la \_ classe RDMSJoinedNode Win32

Supprime un nœud de Bureau à distance services de gestion (RDMS).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Unjoin();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

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

 

 





