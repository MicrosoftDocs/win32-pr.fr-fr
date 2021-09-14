---
title: Méthode GetTSLanaIds de la classe Win32_TerminalServiceSetting
description: Obtient les ID de carte réseau local NetBIOS (LANA) et les descriptions des cartes réseau Services Bureau à distance.
ms.assetid: 3f42e5da-c52b-4500-8cd0-52088dca544a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetTSLanaIds
- Services Bureau à distance de la méthode GetTSLanaIds, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode GetTSLanaIds
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTSLanaIds
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a66d2b2357df7e6d7ccc2cb8a774ba34c50cb46
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324670"
---
# <a name="gettslanaids-method-of-the-win32_terminalservicesetting-class"></a>Méthode GetTSLanaIds de la \_ classe Win32 TerminalServiceSetting

La méthode **GetTSLanaIds** obtient les ID de carte réseau locale NetBIOS et les descriptions des cartes réseau services Bureau à distance.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetTSLanaIds(
  [out] uint32 LanaIdList[],
  [out] string LanaIdDescriptions[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*LanaIdList* \[ à\]
</dt> <dd>

Tableau de numéros LANA.

</dd> <dt>

*LanaIdDescriptions* \[ à\]
</dt> <dd>

Tableau de descriptions de LANA correspondant au tableau *LanaIdList* .

</dd> </dl>

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

 

