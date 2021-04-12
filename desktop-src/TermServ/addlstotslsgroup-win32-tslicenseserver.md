---
title: Méthode AddLStoTSLSGroup de la classe Win32_TSLicenseServer
description: Ajoute le Bureau à distance serveur de licences au groupe serveurs de licences Connexion Bureau à distance Broker (RD Connection Broker) sur un contrôleur de domaine dans le même domaine que le serveur de licences Bureau à distance.
ms.assetid: 65c6b7cf-324a-44f1-8dfc-40e35ed45d4f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AddLStoTSLSGroup
- Services Bureau à distance de la méthode AddLStoTSLSGroup, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode AddLStoTSLSGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.AddLStoTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53934f6682d1a23f99916588aa4eac3b18526c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384339"
---
# <a name="addlstotslsgroup-method-of-the-win32_tslicenseserver-class"></a>Méthode AddLStoTSLSGroup de la \_ classe Win32 TSLicenseServer

Ajoute le Bureau à distance serveur de licences au groupe serveurs de licences Connexion Bureau à distance Broker (RD Connection Broker) sur un contrôleur de domaine dans le même domaine que le serveur de licences Bureau à distance.

## <a name="syntax"></a>Syntaxe


```mof
uint32 AddLStoTSLSGroup();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Notes

Vous devez être membre du groupe Admins du domaine pour appeler cette méthode.

Le serveur de licences doit être membre du groupe Bureau à distance les serveurs de licences si le serveur est configuré pour utiliser l’étendue de la découverte du domaine ou de la forêt.

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
</dt> <dt>

[**IsLSinTSLSGroup**](islsintslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 

