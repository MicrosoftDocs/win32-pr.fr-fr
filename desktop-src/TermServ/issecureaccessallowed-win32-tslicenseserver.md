---
title: Méthode IsSecureAccessAllowed de la classe Win32_TSLicenseServer
description: Récupère une valeur indiquant si un serveur hôte de session Bureau à distance (hôte de session Bureau à distance) est autorisé à demander des licences d’accès client Services Bureau à distance (RDS \ 160 ; Cal) à partir du serveur de licences Bureau à distance.
ms.assetid: b9124808-79be-4b94-b12b-f093d5e8195a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode IsSecureAccessAllowed
- Services Bureau à distance de la méthode IsSecureAccessAllowed, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode IsSecureAccessAllowed
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsSecureAccessAllowed
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6109eb363459432d50d54eb8521f0f23bb54a0836c82f92af20a5b83b64f1d86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351359"
---
# <a name="issecureaccessallowed-method-of-the-win32_tslicenseserver-class"></a>Méthode IsSecureAccessAllowed de la \_ classe Win32 TSLicenseServer

Récupère une valeur qui détermine si un serveur hôte de session Bureau à distance (hôte de session Bureau à distance) est autorisé à demander Services Bureau à distance des licences d’accès client (CAL RDS) à partir du serveur de licences Bureau à distance.

## <a name="syntax"></a>Syntaxe


```mof
uint32 IsSecureAccessAllowed(
  [in]  string  tsname,
  [out] boolean Allowed
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*tsname* \[ dans\]
</dt> <dd>

Nom du serveur hôte de session Bureau à distance.

</dd> <dt>

*Autorisé* \[ à\]
</dt> <dd>

Valeur booléenne qui indique si le serveur hôte de session Bureau à distance est autorisé à demander des licences d’accès client aux services Bureau à distance à partir du serveur de licences.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarques

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

La valeur retournée est basée sur le paramètre de stratégie de groupe « Groupe de sécurité du serveur de licences » et l’appartenance au groupe local ordinateurs Terminal Server sur le serveur de licences Bureau à distance.

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

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> <dt>

[**IsLSSecGrpGPEnabled**](islssecgrpgpenabled-win32-tslicenseserver.md)
</dt> </dl>

 

