---
title: Méthode SetClientWallPaper de la classe Win32_TSEnvironmentSetting
description: La méthode SetClientWallPaper définit la propriété ClientWallPaper.
ms.assetid: 08c41df4-5a3c-4799-bb64-61f414814d0c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetClientWallPaper
- Services Bureau à distance de la méthode SetClientWallPaper, classe Win32_TSEnvironmentSetting
- Win32_TSEnvironmentSetting de la classe Services Bureau à distance, méthode SetClientWallPaper
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.SetClientWallPaper
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ae476134cf526602a059b4714cded6fd6c990e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741260"
---
# <a name="setclientwallpaper-method-of-the-win32_tsenvironmentsetting-class"></a>Méthode SetClientWallPaper de la \_ classe Win32 TSEnvironmentSetting

La méthode **SetClientWallPaper** définit la propriété **ClientWallPaper** .

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetClientWallPaper(
  [in] uint32 ClientWallPaper
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ClientWallPaper* \[ dans\]
</dt> <dd>

Indicateur de désactivation ou d’activation de la propriété **ClientWallPaper** , qui spécifie si l’image d’arrière-plan (ou de papier peint) est affichée sur le client.

<dt>

<span id="0"></span>

<span id="0"></span>**entre**


</dt> <dd>

L’image d’arrière-plan (ou de papier peint) n’est pas affichée sur le client.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

L’image d’arrière-plan (ou de papier peint) est affichée sur le client.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) . La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.

## <a name="remarks"></a>Notes

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**\_TSEnvironmentSetting Win32**](win32-tsenvironmentsetting.md)
</dt> </dl>

 

