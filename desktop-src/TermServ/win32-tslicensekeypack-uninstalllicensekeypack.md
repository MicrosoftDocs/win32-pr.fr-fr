---
title: Méthode UninstallLicenseKeyPack de la classe Win32_TSLicenseKeyPack
description: Désinstalle un jeu de clés de licence Services Bureau à distance.
ms.assetid: AF429AD7-C0DB-40AC-A4C6-591699FBF7E7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode UninstallLicenseKeyPack
- Services Bureau à distance de la méthode UninstallLicenseKeyPack, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode UninstallLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.UninstallLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64754ea9ef2a32676b36821cf20c4f6871396415
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383955"
---
# <a name="uninstalllicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Méthode UninstallLicenseKeyPack de la \_ classe Win32 TSLicenseKeyPack

Désinstalle un jeu de clés de licence Services Bureau à distance.

## <a name="syntax"></a>Syntaxe


```mof
uint32 UninstallLicenseKeyPack(
  [in] unit32 ProductVersion,
  [in] unit32 ProductType,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ProductVersion* \[ dans\]
</dt> <dd>

Identificateur de la version du produit pour le Services Bureau à distance le jeu de clés de licence.

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

Type de produit du jeu de clés de licence Services Bureau à distance.

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

 

 





