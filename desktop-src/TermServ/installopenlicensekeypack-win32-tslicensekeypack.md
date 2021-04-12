---
title: Méthode InstallOpenLicenseKeyPack de la classe Win32_TSLicenseKeyPack
description: Installe un jeu de clés de licence Open License Services Bureau à distance.
ms.assetid: be50e25c-cda3-408b-934b-51ce343f3271
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode InstallOpenLicenseKeyPack
- Services Bureau à distance de la méthode InstallOpenLicenseKeyPack, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode InstallOpenLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallOpenLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7335f25d3118c14f8cd0d27f72fd6a8d4cf1e0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464794"
---
# <a name="installopenlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Méthode InstallOpenLicenseKeyPack de la \_ classe Win32 TSLicenseKeyPack

Installe un jeu de clés de licence Open License Services Bureau à distance.

## <a name="syntax"></a>Syntaxe


```mof
uint32 InstallOpenLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a>Paramètres

*sLicenseNumber* \[ dans\]

chaîne numérique de 8 caractères fournie avec le jeu de clés de licence. Le paramètre *sLicenseNumber* ne peut pas contenir de traits d’Union.

*sAuthorizationNumber* \[ dans\]

chaîne alphanumérique de 15 caractères fournie avec la clé de licence. Le paramètre *sAuthorizationNumber* ne peut pas contenir de traits d’Union.

*ProductVersion* \[ dans\]

Version du produit.

| Valeur | Description |
|-------|-------------|
| 0 | Non pris en charge |
| 1 | Non pris en charge |
| 2 | Windows Server 2008/Windows Server 2008 R2 |
| 4 | Windows Server 2012/Windows Server 2012 R2 |
| 5 | Windows Server 2016 |
| 6 | Windows Server 2019 |

*ProductType* \[ dans\]
</dt> <dd>

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

## <a name="remarks"></a>Notes

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

