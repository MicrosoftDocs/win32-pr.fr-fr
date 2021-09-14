---
title: Méthode GetVirtualDesktopDetails de la classe Win32_RDMSVirtualDesktop
description: Récupère les informations supplémentaires sur le bureau virtuel.
ms.assetid: 487e3a02-4306-4639-a44e-5b9519163a67
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetVirtualDesktopDetails
- Services Bureau à distance de la méthode GetVirtualDesktopDetails, classe Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop de la classe Services Bureau à distance, méthode GetVirtualDesktopDetails
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopDetails
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7382a7ea10b3e557cd7317bdf1ddb0c4bcea55d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324660"
---
# <a name="getvirtualdesktopdetails-method-of-the-win32_rdmsvirtualdesktop-class"></a>Méthode GetVirtualDesktopDetails de la \_ classe Win32 RDMSVirtualDesktop

Récupère les informations supplémentaires sur le bureau virtuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetVirtualDesktopDetails(
  [out] uint32  RAMSizeInMB,
  [out] boolean RemoteFXEnabled,
  [out] string  OSVersion
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RAMSizeInMB* \[ à\]
</dt> <dd>

Reçoit la quantité de mémoire vive (RAM) affectée au bureau virtuel, en octets.

</dd> <dt>

*RemoteFXEnabled* \[ à\]
</dt> <dd>

reçoit une valeur qui indique si RemoteFX est activé sur le bureau virtuel. **TRUE** si RemoteFX est activé ; Sinon, **false**.

</dd> <dt>

*OSVersion* \[ à\]
</dt> <dd>

Reçoit la version du système d’exploitation du bureau virtuel.

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

 

 





