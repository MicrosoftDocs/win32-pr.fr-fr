---
title: Méthode ReinstallLicenseKeyPackOffline de la classe Win32_TSLicenseKeyPack
description: Réinstalle un jeu de clés de licence Services Bureau à distance qui utilise l’identificateur de licence reçu sur Internet ou sur le téléphone.
ms.assetid: CFDB4C3B-C7C1-4670-BC87-92727057A500
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ReinstallLicenseKeyPackOffline
- Services Bureau à distance de la méthode ReinstallLicenseKeyPackOffline, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode ReinstallLicenseKeyPackOffline
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e805521ea750c018ab2e7965e7fbfba05a92d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843181"
---
# <a name="reinstalllicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a>Méthode ReinstallLicenseKeyPackOffline de la \_ classe Win32 TSLicenseKeyPack

Réinstalle un jeu de clés de licence Services Bureau à distance qui utilise l’identificateur de licence reçu sur Internet ou sur le téléphone.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ReinstallLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sLicenseKeyPackId* \[ dans\]
</dt> <dd>

Contient le code de licence de 35 caractères. Seule la chaîne de caractères alphanumériques de 35 caractères doit être indiquée comme entrée. Aucun trait d’Union ne doit être ajouté.

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

 

 





