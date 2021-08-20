---
title: Méthode RemoveTSCGroup de la classe Win32_TSLicenseServer
description: RemoveTSCGroup n’est plus disponible pour une utilisation à partir de Windows Server 2012.
ms.assetid: e5e3eca9-4990-4322-b41d-c6b6b3356272
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RemoveTSCGroup
- Services Bureau à distance de la méthode RemoveTSCGroup, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode RemoveTSCGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.RemoveTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebcd3c0eacb54a14675d2794f1c42f8e7a18cd9ea78c7f6369ef883cc3d9fad3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127504"
---
# <a name="removetscgroup-method-of-the-win32_tslicenseserver-class"></a>Méthode RemoveTSCGroup de la \_ classe Win32 TSLicenseServer

\[**RemoveTSCGroup** n’est plus disponible pour une utilisation à partir de Windows Server 2012.\]

Cette méthode n'est pas prise en charge.

**Windows server 2008 R2 et Windows server 2008 :** Supprime le Terminal Server groupe local ordinateurs du serveur de licences Bureau à distance.

## <a name="syntax"></a>Syntaxe


```mof
uint32 RemoveTSCGroup();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne **WBEM \_ E \_ non \_ pris en charge**.

**Windows server 2008 R2 et Windows server 2008 :** Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarques

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                            |
| Fin de la prise en charge des clients<br/>    | Aucun pris en charge<br/>                                                                 |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2008 R2<br/>                                                         |
| Espace de noms<br/>                | Racine\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> <dt>

[**IsTSCGroupPresent**](istscgrouppresent-win32-tslicenseserver.md)
</dt> </dl>

 

