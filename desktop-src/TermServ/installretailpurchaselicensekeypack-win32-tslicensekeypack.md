---
title: Méthode InstallRetailPurchaseLicenseKeyPack de la classe Win32_TSLicenseKeyPack
description: Installe un jeu de clés de licence Services Bureau à distance acheté par le biais d’un canal de vente au détail.
ms.assetid: cd33c785-7aa1-4e30-8155-4176b6f4c037
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode InstallRetailPurchaseLicenseKeyPack
- Services Bureau à distance de la méthode InstallRetailPurchaseLicenseKeyPack, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode InstallRetailPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 427107e6d581c839ee83767c7c95426e13d16a392b7764924997c01785b85d46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129590"
---
# <a name="installretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Méthode InstallRetailPurchaseLicenseKeyPack de la \_ classe Win32 TSLicenseKeyPack

Installe un jeu de clés de licence Services Bureau à distance acheté par le biais d’un canal de vente au détail.

## <a name="syntax"></a>Syntaxe


```mof
uint32 InstallRetailPurchaseLicenseKeyPack(
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

## <a name="remarks"></a>Remarques

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

