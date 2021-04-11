---
title: Méthode ReinstallRetailPurchaseLicenseKeyPack de la classe Win32_TSLicenseKeyPack
description: Réinstalle un jeu de clés de licence Services Bureau à distance acheté par le biais d’un canal de vente au détail.
ms.assetid: 19528726-8DEB-4D03-BFA6-647C8A612FA2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ReinstallRetailPurchaseLicenseKeyPack
- Services Bureau à distance de la méthode ReinstallRetailPurchaseLicenseKeyPack, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode ReinstallRetailPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4caa8635eaf28ad823add500883832a7fe885b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032451"
---
# <a name="reinstallretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Méthode ReinstallRetailPurchaseLicenseKeyPack de la \_ classe Win32 TSLicenseKeyPack

Réinstalle un jeu de clés de licence Services Bureau à distance acheté par le biais d’un canal de vente au détail.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ReinstallRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sLicenseCode* \[ dans\]
</dt> <dd>

Contient le code de licence de 25 caractères. Seule la chaîne de caractères alphanumériques de 25 caractères doit être indiquée comme entrée. Aucun trait d’Union ne doit être ajouté.

</dd> <dt>

*KeyPackId* \[ à\]
</dt> <dd>

Reçoit l’identificateur du module de clé.

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

 

 





