---
title: Méthode SetFallbackPrintDriverType de la classe Win32_TerminalServiceSetting
description: La méthode SetFallbackPrintDriverType définit la propriété FallbackPrintDriverType de la classe.
ms.assetid: be738134-199a-41a6-b2f8-cccfa14fa02b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetFallbackPrintDriverType
- Services Bureau à distance de la méthode SetFallbackPrintDriverType, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode SetFallbackPrintDriverType
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetFallbackPrintDriverType
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d39033a34c75ea94f365ae690b1ac6fe4cd61663e9cd6db19f2cd2c232bd8c89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137862"
---
# <a name="setfallbackprintdrivertype-method-of-the-win32_terminalservicesetting-class"></a>Méthode SetFallbackPrintDriverType de la \_ classe Win32 TerminalServiceSetting

La méthode **SetFallbackPrintDriverType** définit la propriété **FallbackPrintDriverType** de la classe.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetFallbackPrintDriverType(
  [in] uint32 FallbackPrintDriverType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FallbackPrintDriverType* \[ dans\]
</dt> <dd>

Définit la propriété **FallbackPrintDriverType** qui autorise ou refuse les nouvelles connexions de services Bureau à distance.

<dt>

<span id="0"></span>

<span id="0"></span>**entre**


</dt> <dd>

Aucun pilote de secours.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Meilleure hypothèse.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Meilleure hypothèse. Si aucune correspondance n’est trouvée, vous pouvez revenir à Hewlett-Packard PCL (Printer Control Language).

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**1,3**


</dt> <dd>

Meilleure hypothèse. Si aucune correspondance n’est trouvée, basculez vers PostScript (PS).

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Meilleure hypothèse. Si aucune correspondance n’est trouvée, affichez les pilotes PS et PCL.

</dd> </dl> </dd> </dl>

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

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

