---
title: Méthode InstallAgreementLicenseKeyPack de la classe Win32_TSLicenseKeyPack
description: Installe un jeu de clés de licence Services Bureau à distance acheté par le biais d’un contrat de licence et se connecte automatiquement via Internet pour valider la licence du Pack de clés.
ms.assetid: 70a0aac3-2709-47ba-bf6a-549393c4c115
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode InstallAgreementLicenseKeyPack
- Services Bureau à distance de la méthode InstallAgreementLicenseKeyPack, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode InstallAgreementLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f62105d2210e08bd62b53fa05d723177383e777261f4b21885c4375b30b9599
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118852959"
---
# <a name="installagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Méthode InstallAgreementLicenseKeyPack de la \_ classe Win32 TSLicenseKeyPack

Installe un jeu de clés de licence Services Bureau à distance acheté par le biais d’un contrat de licence et se connecte automatiquement via Internet pour valider la licence du Pack de clés.

## <a name="syntax"></a>Syntaxe


```mof
uint32 InstallAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a>Paramètres

*AgreementType* \[ dans\]

Type de contrat.

| Valeur | Description |
|-------|-------------|
| 0 | Le jeu de clés de licence provient d’un contrat de licence en volume sélectionné (pour les clients disposant de 250 ordinateurs ou plus). Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé. |
| 1 | le jeu de clés de licence provient d’un contrat de licence en volume Enterprise pour les clients disposant de 250 ou plus d’ordinateurs. Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé. |
| 2 | Le jeu de clés de licence provient d’un contrat de licence en volume campus pour un établissement d’enseignement supérieur. Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé. |
| 3 | Le jeu de clés de licence provient d’un contrat de licence en volume scolaire pour les institutions primaires et secondaires. Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé. |
| 4 | Le jeu de clés de licence provient d’un contrat de licence de fournisseur de services pour les fournisseurs de services de licence pour les logiciels Microsoft sur une base mensuelle. Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé. |
| 5 | Le jeu de clés de licence provient d’un autre contrat de licence, par exemple Open Value, une licence Open sur plusieurs années et une licence Open Subscription. Le paramètre *sAgreementNumber* est le numéro de contrat fourni avec les informations de votre programme. |

*sAgreementNumber* \[ dans\]

Numéro de contrat ou numéro d’inscription. Le paramètre *sAgreementNumber* est une chaîne numérique à sept chiffres sans trait d’Union.

*ProductVersion* \[ dans\]

Version du produit.

| Valeur | Description |
|-------|-------------|
| 0 | Non pris en charge |
| 1 | Non pris en charge |
| 2 | Windows server 2008/Windows server 2008 R2 |
| 4 | Windows Server 2012/Windows Server 2012 R2 |
| 5 | Windows Server 2016 |
| 6 | Windows Server 2019 |

*ProductType* \[ dans\]

Type de produit.

| Valeur | Description |
|-------|-------------|
| 0 | Le type de produit du jeu de clés de licence Services Bureau à distance est par périphérique. Par conséquent, chaque appareil qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence. |
| 1 | Le type de produit du jeu de clés de licence Services Bureau à distance est par utilisateur. Par conséquent, chaque utilisateur qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence. |
| 2 | Ce type de produit n’est pas valide. |

*LicenseCount* \[ dans\]

Nombre de licences à installer.

*KeyPackId* \[ à\]

Reçoit l’identificateur du module de clé.

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarques

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Conditions requises

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

 

