---
title: Méthode SetActiveServer de la classe Win32_RDMSEnvironment
description: Définit le nom de domaine complet de l’environnement des services de gestion de Bureau à distance (RDMS) sur le nœud actuel.
ms.assetid: ed7b71cf-c3a4-4d2f-856a-31332f94fac9
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetActiveServer
- Services Bureau à distance de la méthode SetActiveServer, classe Win32_RDMSEnvironment
- Win32_RDMSEnvironment de la classe Services Bureau à distance, méthode SetActiveServer
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f11b378b15e271200c730691c3654fd10e80f3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324481"
---
# <a name="setactiveserver-method-of-the-win32_rdmsenvironment-class"></a>Méthode SetActiveServer de la \_ classe Win32 RDMSEnvironment

Définit le nom de domaine complet de l’environnement des services de gestion de Bureau à distance (RDMS) sur le nœud actuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetActiveServer();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.

## <a name="requirements"></a>Spécifications



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

 

 





