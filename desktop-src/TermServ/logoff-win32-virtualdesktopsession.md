---
title: Méthode Logoff de la classe Win32_VirtualDesktopSession (Sensevts. h)
description: Déconnecte l’utilisateur de la session de bureau virtuel.
ms.assetid: a9c90ace-324c-4eec-86e1-30ce35307e52
ms.tgt_platform: multiple
keywords:
- Méthode Logoff Services Bureau à distance
- Méthode Logoff Services Bureau à distance, classe Win32_VirtualDesktopSession
- Win32_VirtualDesktopSession de la classe Services Bureau à distance, méthode Logoff
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession.Logoff
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4582744f0d8ba9300bd620a45190ec1de4819ee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384971"
---
# <a name="logoff-method-of-the-win32_virtualdesktopsession-class"></a>Méthode Logoff de la \_ classe VirtualDesktopSession Win32

Déconnecte l’utilisateur de la session de bureau virtuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 Logoff();
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
| En-tête<br/>                   | <dl> <dt>Sensevts. h</dt> </dl>       |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_VirtualDesktopSession Win32**](win32-virtualdesktopsession.md)
</dt> </dl>

 

 





