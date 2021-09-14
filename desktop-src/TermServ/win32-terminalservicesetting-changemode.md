---
title: Méthode ChangeMode de la classe Win32_TerminalServiceSetting
description: La méthode ChangeMode définit le type de licence du serveur actuel de l’hôte de session Bureau à distance (hôte de session Bureau à distance).
ms.assetid: 293483ee-51ce-4cd4-ba13-6c7c02bbdbbf
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ChangeMode
- Services Bureau à distance de la méthode ChangeMode, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode ChangeMode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.ChangeMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880fcab8aa68e49c6b3c00278b90635686de6168
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919632"
---
# <a name="changemode-method-of-the-win32_terminalservicesetting-class"></a>Méthode ChangeMode de la \_ classe Win32 TerminalServiceSetting

La méthode **ChangeMode** définit le type de licence du serveur actuel de l’hôte de session Bureau à distance (hôte de session Bureau à distance).

## <a name="syntax"></a>Syntaxe


```mof
uint32 ChangeMode(
  [in] uint32 LicensingType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*LicensingType* \[ dans\]
</dt> <dd>

Type de licence à définir en fonction du mode de serveur hôte de session Bureau à distance.

<dt>

<span id="0"></span>

<span id="0"></span>**entre**


</dt> <dd>

Serveur hôte de session Bureau à distance personnel.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Bureau à distance pour l’administration.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Par appareil/par siège. Valide pour les serveurs d’applications.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Par utilisateur. Valide pour les serveurs d’applications.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Notes

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

