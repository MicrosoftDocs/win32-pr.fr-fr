---
title: Méthode ImportLicenseKeyPackOffline de la classe Win32_TSLicenseKeyPack
description: Importations, à partir d’un autre serveur de licences Bureau à distance, un jeu de clés de licence Services Bureau à distance qui utilise un identificateur de licence reçu via Internet ou le téléphone.
ms.assetid: 69D65917-8B82-4C24-AFFA-BBE529D3883C
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ImportLicenseKeyPackOffline
- Services Bureau à distance de la méthode ImportLicenseKeyPackOffline, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode ImportLicenseKeyPackOffline
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7d5be5dc8cfd9f654c09d989149a423351689f420a52ca1756fb197260e800
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348630"
---
# <a name="importlicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a>Méthode ImportLicenseKeyPackOffline de la \_ classe Win32 TSLicenseKeyPack

Importations, à partir d’un autre serveur de licences Bureau à distance, un jeu de clés de licence Services Bureau à distance qui utilise un identificateur de licence reçu via Internet ou le téléphone.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ImportLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sLicenseKeyPackId* \[ dans\]
</dt> <dd>

Contient le code de licence de 35 caractères. Seule la chaîne de caractères alphanumériques de 35 caractères doit être indiquée comme entrée. Aucun trait d’Union ne doit être ajouté.

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

 

 





