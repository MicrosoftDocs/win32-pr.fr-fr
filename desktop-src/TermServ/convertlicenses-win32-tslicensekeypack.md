---
title: Méthode ConvertLicenses de la classe Win32_TSLicenseKeyPack
description: Convertit les licences dans le jeu de clés actuel.
ms.assetid: 38600144-8fa2-4f9a-b7a4-7fafc304e7cb
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ConvertLicenses
- Services Bureau à distance de la méthode ConvertLicenses, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode ConvertLicenses
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ConvertLicenses
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f37b1d9804c5f14f89a7ff6b48f5f8fcbdc60b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126853455"
---
# <a name="convertlicenses-method-of-the-win32_tslicensekeypack-class"></a>Méthode ConvertLicenses de la \_ classe Win32 TSLicenseKeyPack

Convertit les licences dans le jeu de clés actuel. Si la licence est une licence par utilisateur, elle est convertie en licence par appareil. Si la licence est une licence par appareil, elle est convertie en licence par utilisateur.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ConvertLicenses(
  [in]  uint32 Count,
  [out] uint32 KeypackID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nombre* \[ dans\]
</dt> <dd>

Nombre de licences à convertir.

</dd> <dt>

*KeypackID* \[ à\]
</dt> <dd>

Identificateur du Pack de clés résultant.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                            |
| Espace de noms<br/>                | Racine\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSLicenseKeyPack Win32**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





