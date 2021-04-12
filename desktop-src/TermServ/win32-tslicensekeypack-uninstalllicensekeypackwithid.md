---
title: Méthode UninstallLicenseKeyPackWithId de la classe Win32_TSLicenseKeyPack
description: Désinstalle le jeu de clés de licence Services Bureau à distance avec l’identificateur de package de clés spécifié.
ms.assetid: ECB622AB-FAB4-4C5D-A007-E3ABA8E1D3E7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode UninstallLicenseKeyPackWithId
- Services Bureau à distance de la méthode UninstallLicenseKeyPackWithId, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode UninstallLicenseKeyPackWithId
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.UninstallLicenseKeyPackWithId
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583c7d56f5aacde57a1b683e988646e7e30b62d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464478"
---
# <a name="uninstalllicensekeypackwithid-method-of-the-win32_tslicensekeypack-class"></a>Méthode UninstallLicenseKeyPackWithId de la \_ classe Win32 TSLicenseKeyPack

Désinstalle le jeu de clés de licence Services Bureau à distance avec l’identificateur de package de clés spécifié.

## <a name="syntax"></a>Syntaxe


```mof
uint32 UninstallLicenseKeyPackWithId(
  [in] uint32 KeyPackId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*KeyPackId* \[ dans\]
</dt> <dd>

Identificateur du Pack de clés à désinstaller.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                            |
| Espace de noms<br/>                | Racine\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSLicenseKeyPack Win32**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





