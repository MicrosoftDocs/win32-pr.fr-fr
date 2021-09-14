---
title: Méthode InitialProgram de la classe Win32_TSEnvironmentSetting
description: La méthode InitialProgram définit les propriétés du programme de démarrage, telles que le nom, le répertoire de travail et le chemin d’accès du programme à démarrer immédiatement après l’ouverture de session sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance).
ms.assetid: e53621cf-ade8-4301-acc0-232866e88488
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode InitialProgram
- Services Bureau à distance de la méthode InitialProgram, classe Win32_TSEnvironmentSetting
- Win32_TSEnvironmentSetting de la classe Services Bureau à distance, méthode InitialProgram
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.InitialProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd41e1af990e37b8458431106bc2ec9a8489b14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122726"
---
# <a name="initialprogram-method-of-the-win32_tsenvironmentsetting-class"></a>Méthode InitialProgram de la \_ classe Win32 TSEnvironmentSetting

La méthode **InitialProgram** définit les propriétés du programme de démarrage, telles que le nom, le répertoire de travail et le chemin d’accès du programme à démarrer immédiatement après l’ouverture de session sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance).

## <a name="syntax"></a>Syntaxe


```mof
uint32 InitialProgram(
  [in] string InitialProgramPath,
  [in] string Startin
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*InitialProgramPath* \[ dans\]
</dt> <dd>

Nom et chemin d’accès du programme de démarrage.

</dd> <dt>

*Démarrer* \[ dans\]
</dt> <dd>

Chemin d’accès au répertoire de travail du programme de démarrage.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) . La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.

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

[**\_TSEnvironmentSetting Win32**](win32-tsenvironmentsetting.md)
</dt> </dl>

 

