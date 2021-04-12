---
title: Méthode GetUserAssignment de la classe Win32_RDMSVirtualDesktop
description: Récupère le nom d’utilisateur et le nom de domaine de l’utilisateur affecté au bureau virtuel.
ms.assetid: 1887c49d-85df-4fb4-9b40-42fb7763bf95
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetUserAssignment
- Services Bureau à distance de la méthode GetUserAssignment, classe Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop de la classe Services Bureau à distance, méthode GetUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87293a471bb4f69b3f4c57de0f964fa0daa043cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384900"
---
# <a name="getuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>Méthode GetUserAssignment de la \_ classe Win32 RDMSVirtualDesktop

Récupère le nom d’utilisateur et le nom de domaine de l’utilisateur affecté au bureau virtuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetUserAssignment(
  [out] string UserName,
  [out] string UserDomain
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom d’utilisateur* \[ à\]
</dt> <dd>

Reçoit le nom d’utilisateur.

</dd> <dt>

*UserDomain* \[ à\]
</dt> <dd>

Reçoit le nom de domaine.

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

[**\_RDMSVirtualDesktop Win32**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





