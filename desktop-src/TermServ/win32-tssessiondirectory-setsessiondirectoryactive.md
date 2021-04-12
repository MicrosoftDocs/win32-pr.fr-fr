---
title: Méthode SetSessionDirectoryActive de la classe Win32_TSSessionDirectory
description: La méthode SetSessionDirectoryActive définit la propriété SessionDirectoryActive.
ms.assetid: b2175d1a-b62f-4bdf-9122-76e85233fba4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetSessionDirectoryActive
- Services Bureau à distance de la méthode SetSessionDirectoryActive, classe Win32_TSSessionDirectory
- Win32_TSSessionDirectory de la classe Services Bureau à distance, méthode SetSessionDirectoryActive
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca8709028ee90db549c7cdeb053b04dc88b52ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384440"
---
# <a name="setsessiondirectoryactive-method-of-the-win32_tssessiondirectory-class"></a>Méthode SetSessionDirectoryActive de la \_ classe Win32 TSSessionDirectory

La méthode **SetSessionDirectoryActive** définit la propriété **SessionDirectoryActive** .

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetSessionDirectoryActive(
  [in] uint32 SessionDirectoryActive
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SessionDirectoryActive* \[ dans\]
</dt> <dd>

Type : **UInt32**

Indicateur de désactivation ou d’activation du service d’annuaire de sessions.

<dt>

<span id="0"></span>

<span id="0"></span>**entre**


</dt> <dd>

Désactivez le service d’annuaire de sessions.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Activez le service d’annuaire de sessions.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) . La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.

## <a name="remarks"></a>Notes

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSSessionDirectory Win32**](win32-tssessiondirectory.md)
</dt> </dl>

 

