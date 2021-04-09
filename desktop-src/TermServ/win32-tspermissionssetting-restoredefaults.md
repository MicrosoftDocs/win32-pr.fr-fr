---
title: Méthode RestoreDefaults de la classe Win32_TSPermissionsSetting (Netfw. h)
description: Restaure les valeurs de jeu d’autorisations par défaut pour le terminal.
ms.assetid: bdd01290-7c7c-4355-85dc-ade51b2abd94
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RestoreDefaults
- Services Bureau à distance de la méthode RestoreDefaults, classe Win32_TSPermissionsSetting
- Win32_TSPermissionsSetting de la classe Services Bureau à distance, méthode RestoreDefaults
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.RestoreDefaults
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 073a8f8267ab9e7f7cbd50f15f4f3f20594d2e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843389"
---
# <a name="restoredefaults-method-of-the-win32_tspermissionssetting-class"></a>Méthode RestoreDefaults de la \_ classe Win32 TSPermissionsSetting

La méthode **RestoreDefaults** restaure les valeurs de jeu d’autorisations par défaut pour le terminal.

## <a name="syntax"></a>Syntaxe


```mof
uint32 RestoreDefaults();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une réussite en cas de réussite, sinon échec.

## <a name="remarks"></a>Notes

Les autorisations par défaut sont les suivantes :

-   Les comptes administrateurs, système et Bureau à distance Assistant aide disposent de toutes les [autorisations services Bureau à distance](terminal-services-permissions.md).
-   Le compte Bureau à distance Users dispose de l’autorisation Logon, Connect, Query information et Send message.
-   Les comptes service local et service réseau disposent des informations de requête et de l’autorisation Envoyer un message.

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| En-tête<br/>                   | <dl> <dt>Netfw. h</dt> </dl>      |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSPermissionsSetting Win32**](win32-tspermissionssetting.md)
</dt> </dl>

 

