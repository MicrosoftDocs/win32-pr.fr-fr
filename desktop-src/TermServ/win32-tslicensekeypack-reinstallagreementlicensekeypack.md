---
title: Méthode ReinstallAgreementLicenseKeyPack de la classe Win32_TSLicenseKeyPack
description: Réinstalle un jeu de clés de licence Services Bureau à distance acheté par le biais d’un contrat de licence et se connecte automatiquement via Internet pour valider la licence du Pack de clés.
ms.assetid: BC3C966B-E6CE-45E2-BC1D-2439B75D4C3C
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ReinstallAgreementLicenseKeyPack
- Services Bureau à distance de la méthode ReinstallAgreementLicenseKeyPack, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode ReinstallAgreementLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15894ec80819cf39c7eaee45eb6f943e6fd8930618154be62e6a15969b597190
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513879"
---
# <a name="reinstallagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Méthode ReinstallAgreementLicenseKeyPack de la \_ classe Win32 TSLicenseKeyPack

Réinstalle un jeu de clés de licence Services Bureau à distance acheté par le biais d’un contrat de licence et se connecte automatiquement via Internet pour valider la licence du Pack de clés.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ReinstallAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AgreementType* \[ dans\]
</dt> <dd>

Type de contrat.

<dt>

0
</dt> <dd>

Le jeu de clés de licence provient d’un contrat de licence en volume sélectionné (pour les clients disposant de 250 ordinateurs ou plus). Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé.

</dd> <dt>

1
</dt> <dd>

le jeu de clés de licence provient d’un contrat de licence en volume Enterprise pour les clients disposant de 250 ou plus d’ordinateurs. Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé.

</dd> <dt>

2
</dt> <dd>

Le jeu de clés de licence provient d’un contrat de licence en volume campus pour un établissement d’enseignement supérieur. Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé.

</dd> <dt>

3
</dt> <dd>

Le jeu de clés de licence provient d’un contrat de licence en volume scolaire pour les institutions primaires et secondaires. Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé.

</dd> <dt>

4
</dt> <dd>

Le jeu de clés de licence provient d’un contrat de licence de fournisseur de services pour les fournisseurs de services de licence pour les logiciels Microsoft sur une base mensuelle. Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé.

</dd> <dt>

5
</dt> <dd>

Le jeu de clés de licence provient d’un autre contrat de licence, par exemple Open Value, une licence Open sur plusieurs années et une licence Open Subscription. Le paramètre *sAgreementNumber* est le numéro de contrat fourni avec les informations de votre programme.

</dd> </dl> </dd> <dt>

*sAgreementNumber* \[ dans\]
</dt> <dd>

Numéro de contrat ou numéro d’inscription. Le paramètre *sAgreementNumber* est une chaîne numérique à sept chiffres sans trait d’Union.

</dd> <dt>

*ProductVersion* \[ dans\]
</dt> <dd>

Version du produit.

<dt>

0
</dt> <dd>

Non pris en charge.

</dd> <dt>

1
</dt> <dd>

Non pris en charge.

</dd> <dt>

2
</dt> <dd>

Windows Server 2008

</dd> </dl> </dd> <dt>

*ProductType* \[ dans\]
</dt> <dd>

Type de produit.

<dt>

0
</dt> <dd>

Le type de produit du jeu de clés de licence Services Bureau à distance est par périphérique. Par conséquent, chaque appareil qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence.

</dd> <dt>

1
</dt> <dd>

Le type de produit du jeu de clés de licence Services Bureau à distance est par utilisateur. Par conséquent, chaque utilisateur qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence.

</dd> <dt>

2
</dt> <dd>

Ce type de produit n’est pas valide.

</dd> </dl> </dd> <dt>

*LicenseCount* \[ dans\]
</dt> <dd>

Nombre de licences à installer.

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

 

 





