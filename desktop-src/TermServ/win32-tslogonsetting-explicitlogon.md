---
title: Méthode ExplicitLogon de la classe Win32_TSLogonSetting
description: La méthode ExplicitLogon définit les informations d’identification à utiliser pour l’authentification.
ms.assetid: cfd43396-0d66-4d5e-81c8-5c0e66422dc5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ExplicitLogon
- Services Bureau à distance de la méthode ExplicitLogon, classe Win32_TSLogonSetting
- Win32_TSLogonSetting de la classe Services Bureau à distance, méthode ExplicitLogon
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.ExplicitLogon
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7303f06967d26276c7b43e06109cd9b37d664b960946afdffbb4f6a5a7c18821
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137782"
---
# <a name="explicitlogon-method-of-the-win32_tslogonsetting-class"></a>Méthode ExplicitLogon de la \_ classe Win32 TSLogonSetting

La méthode **ExplicitLogon** définit les informations d’identification à utiliser pour l’authentification.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ExplicitLogon(
  [in] string UserName,
  [in] string Domain,
  [in] string Password
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom d’utilisateur* \[ dans\]
</dt> <dd>

Informations d’identification d’ouverture de session de nom d’utilisateur.

</dd> <dt>

*Domaine* \[ dans\]
</dt> <dd>

Informations d’identification d’ouverture de session de domaine.

</dd> <dt>

*Mot de passe* \[ dans\]
</dt> <dd>

Informations d’identification de connexion au mot de passe.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une réussite en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) . La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.

## <a name="remarks"></a>Remarques

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSLogonSetting Win32**](win32-tslogonsetting.md)
</dt> </dl>

 

