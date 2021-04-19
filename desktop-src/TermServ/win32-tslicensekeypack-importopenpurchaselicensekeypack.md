---
title: Méthode ImportOpenPurchaseLicenseKeyPack de la classe Win32_TSLicenseKeyPack
description: Importations, à partir d’un autre serveur de licences Bureau à distance, un jeu de clés de licence Open License Services Bureau à distance.
ms.assetid: FE1923FF-5292-4080-AB51-88B8A6B2322C
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ImportOpenPurchaseLicenseKeyPack
- Services Bureau à distance de la méthode ImportOpenPurchaseLicenseKeyPack, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode ImportOpenPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 944bb1ce63150caece2cbc247af24542fde2d4f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509945"
---
# <a name="importopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Méthode ImportOpenPurchaseLicenseKeyPack de la \_ classe Win32 TSLicenseKeyPack

Importations, à partir d’un autre serveur de licences Bureau à distance, un jeu de clés de licence Open License Services Bureau à distance.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ImportOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sLicenseNumber* \[ dans\]
</dt> <dd>

chaîne numérique de 8 caractères fournie avec le jeu de clés de licence. Le paramètre *sLicenseNumber* ne peut pas contenir de traits d’Union.

</dd> <dt>

*sAuthorizationNumber* \[ dans\]
</dt> <dd>

chaîne alphanumérique de 15 caractères fournie avec la clé de licence. Le paramètre *sAuthorizationNumber* ne peut pas contenir de traits d’Union.

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

Nombre de licences à importer

</dd> <dt>

*sSourceLSName* \[ dans\]
</dt> <dd>

Nom du serveur de licences Bureau à distance source. Il s’agit du nom unique complet ou de l’adresse IP du serveur.

</dd> <dt>

*sSourceLSProductId* \[ dans\]
</dt> <dd>

Identificateur du serveur de licences Bureau à distance. Est une chaîne alphanumérique de 35 caractères qui ne peut pas contenir de traits d’Union.

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

 

 





