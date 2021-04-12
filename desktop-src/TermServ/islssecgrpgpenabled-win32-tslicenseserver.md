---
title: Méthode IsLSSecGrpGPEnabled de la classe Win32_TSLicenseServer
description: Récupère si le groupe de sécurité \ 0034 ; du serveur de licences \ 0034 ; le paramètre de stratégie de groupe est activé sur le serveur de licences Bureau à distance.
ms.assetid: 715b619b-f082-4fed-ac4c-70d5e286e37c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode IsLSSecGrpGPEnabled
- Services Bureau à distance de la méthode IsLSSecGrpGPEnabled, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode IsLSSecGrpGPEnabled
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSSecGrpGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f3d7ec9de3d98849f9680f1b2a87bf5b22922a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104302"
---
# <a name="islssecgrpgpenabled-method-of-the-win32_tslicenseserver-class"></a>Méthode IsLSSecGrpGPEnabled de la \_ classe Win32 TSLicenseServer

Récupère si le paramètre de stratégie de groupe « Groupe de sécurité du serveur de licences » est activé sur le serveur de licences Bureau à distance.

## <a name="syntax"></a>Syntaxe


```mof
uint32 IsLSSecGrpGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Activé* \[ à\]
</dt> <dd>

Valeur booléenne qui indique si le paramètre de stratégie « Groupe de sécurité du serveur de licences » est activé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Notes

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

Le paramètre de stratégie « Groupe de sécurité du serveur de licences » vous permet de spécifier les serveurs Bureau à distance hôte de session Bureau à distance qui sont autorisés à contacter le serveur de licences pour obtenir des licences d’accès client Services Bureau à distance (CAL RDS). Si le paramètre de stratégie est activé sur le serveur de licences, le serveur ne répondra aux demandes de licences d’accès client aux services Bureau à distance des serveurs hôtes de session Bureau à distance dont les comptes d’ordinateur sont membres du groupe local ordinateurs Terminal Server sur le serveur de licences.

Le paramètre de stratégie se trouve dans le nœud suivant de l’éditeur d’une stratégie de groupe locale :

Configuration de l’ordinateur \\ modèles d’administration \\ composants Windows \\ Gestionnaire de \\ licences TS TS

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

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

