---
title: Méthode RemoveLicensesWithIdCount de la classe Win32_TSLicenseKeyPack
description: Supprime le nombre spécifié de licences Services Bureau à distance du jeu de clés spécifié.
ms.assetid: 36228659-7BE7-490A-A00C-A99FA66BFEB8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RemoveLicensesWithIdCount
- Services Bureau à distance de la méthode RemoveLicensesWithIdCount, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode RemoveLicensesWithIdCount
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.RemoveLicensesWithIdCount
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b2de1d1e0bfeed538e400436f8a88cd25ac563
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032450"
---
# <a name="removelicenseswithidcount-method-of-the-win32_tslicensekeypack-class"></a>Méthode RemoveLicensesWithIdCount de la \_ classe Win32 TSLicenseKeyPack

Supprime le nombre spécifié de licences Services Bureau à distance du jeu de clés spécifié.

## <a name="syntax"></a>Syntaxe


```mof
uint32 RemoveLicensesWithIdCount(
  [in] uint32 KeyPackId,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*KeyPackId* \[ dans\]
</dt> <dd>

Identificateur du module de clé qui contient les licences à supprimer.

</dd> <dt>

*LicenseCount* \[ dans\]
</dt> <dd>

Nombre de licences à désinstaller.

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

 

 





