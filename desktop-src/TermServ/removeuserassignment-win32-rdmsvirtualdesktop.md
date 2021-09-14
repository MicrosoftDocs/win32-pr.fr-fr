---
title: Méthode RemoveUserAssignment de la classe Win32_RDMSVirtualDesktop
description: Supprime l’affectation d’utilisateur du bureau virtuel.
ms.assetid: 7ebb34b4-94f6-4a00-87a9-44ad28d103cb
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RemoveUserAssignment
- Services Bureau à distance de la méthode RemoveUserAssignment, classe Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop de la classe Services Bureau à distance, méthode RemoveUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.RemoveUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01675c777603f0eab2d22c0136b1ef6cc3522b7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324537"
---
# <a name="removeuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>Méthode RemoveUserAssignment de la \_ classe Win32 RDMSVirtualDesktop

Supprime l’affectation d’utilisateur du bureau virtuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 RemoveUserAssignment(
  [in] string VMName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Vmname* \[ dans\]
</dt> <dd>

Nom de la machine virtuelle du bureau virtuel.

</dd> </dl>

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

[**\_RDMSVirtualDesktop Win32**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





