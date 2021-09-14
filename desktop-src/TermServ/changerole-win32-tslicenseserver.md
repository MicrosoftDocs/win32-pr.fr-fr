---
title: Méthode ChangeRole de la classe Win32_TSLicenseServer
description: Modifie l’étendue de la découverte du serveur de licences Bureau à distance. L’étendue de découverte détermine les serveurs de Bureau à distance hôte de session (hôte de session Bureau à distance) sur le réseau qui peuvent détecter automatiquement le serveur de licences.
ms.assetid: 3d98fd8a-4ade-489f-8edd-5df1227f15cd
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ChangeRole
- Services Bureau à distance de la méthode ChangeRole, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode ChangeRole
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ChangeRole
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9746b856c74e9603751fe85bb861e2b6869f03a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857176"
---
# <a name="changerole-method-of-the-win32_tslicenseserver-class"></a>Méthode ChangeRole de la \_ classe Win32 TSLicenseServer

Modifie l’étendue de la découverte du serveur de licences Bureau à distance. L’étendue de découverte détermine les serveurs de Bureau à distance hôte de session (hôte de session Bureau à distance) sur le réseau qui peuvent détecter automatiquement le serveur de licences.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ChangeRole(
  [in] uint32 ServerRole
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ServerRole* \[ dans\]
</dt> <dd>

Étendue de la découverte pour le serveur de licences Bureau à distance. Vous pouvez définir l’une des valeurs suivantes.

<dt>

0
</dt> <dd>

Les serveurs hôtes de session Bureau à distance dans le même groupe de travail peuvent découvrir le serveur de licences.

</dd> <dt>

1
</dt> <dd>

Les serveurs hôtes de session Bureau à distance dans le même domaine peuvent découvrir le serveur de licences. Vous devez être connecté en tant qu’administrateur de domaine pour définir cette valeur.

</dd> <dt>

2
</dt> <dd>

Les serveurs hôtes de session Bureau à distance de plusieurs domaines de la même forêt peuvent découvrir le serveur de licences. Vous devez être connecté en tant qu’administrateur d’entreprise pour définir cette valeur.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Notes

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Spécifications



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

 

