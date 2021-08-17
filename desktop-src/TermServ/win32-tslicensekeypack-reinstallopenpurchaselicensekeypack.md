---
title: Méthode ReinstallOpenPurchaseLicenseKeyPack de la classe Win32_TSLicenseKeyPack
description: Réinstalle un jeu de clés de licence Open License Services Bureau à distance.
ms.assetid: 3E70711E-284A-466E-A733-1219F5E0B741
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ReinstallOpenPurchaseLicenseKeyPack
- Services Bureau à distance de la méthode ReinstallOpenPurchaseLicenseKeyPack, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode ReinstallOpenPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6519e6eedc187b6db2ee93a776843b0f305430df7ae55e4356ebce4de5ad31d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137822"
---
# <a name="reinstallopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Méthode ReinstallOpenPurchaseLicenseKeyPack de la \_ classe Win32 TSLicenseKeyPack

Réinstalle un jeu de clés de licence Open License Services Bureau à distance.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ReinstallOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
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

 

 





