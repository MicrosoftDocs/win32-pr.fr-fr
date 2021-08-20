---
title: Méthode SetAllowTSConnections de la classe Win32_TerminalServiceSetting
description: La méthode SetAllowTSConnections autorise ou refuse les nouvelles connexions Bureau à distance. Cette méthode modifie la propriété AllowTSConnections de la classe en conséquence.
ms.assetid: 6cbaea62-ced0-4788-99fb-5b36816b80a1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetAllowTSConnections
- Services Bureau à distance de la méthode SetAllowTSConnections, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode SetAllowTSConnections
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetAllowTSConnections
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63f8e9be06a19599f578089fa979d7fd93a7bf457fcadf033ed0ab56fea4947f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127025"
---
# <a name="setallowtsconnections-method-of-the-win32_terminalservicesetting-class"></a>Méthode SetAllowTSConnections de la \_ classe Win32 TerminalServiceSetting

La méthode **SetAllowTSConnections** autorise ou refuse les nouvelles connexions Bureau à distance. Cette méthode modifie la propriété **AllowTSConnections** de la classe en conséquence.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetAllowTSConnections(
  [in] uint32 AllowTSConnections,
  [in] uint32 ModifyFirewallException
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AllowTSConnections* \[ dans\]
</dt> <dd>

Spécifie si les nouvelles connexions Bureau à distance sont autorisées. Il doit s’agir de l’une des valeurs suivantes.

<dt>

<span id="0"></span>

<span id="0"></span>**entre**


</dt> <dd>

Les nouvelles connexions ne sont pas autorisées. Si le paramètre *ModifyFirewallException* est 1, l’exception de pare-feu Bureau à distance est désactivée.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Les nouvelles connexions sont autorisées. Si le paramètre *ModifyFirewallException* est 1, l’exception de pare-feu Bureau à distance est activée.

</dd> </dl> </dd> <dt>

*ModifyFirewallException* \[ dans\]
</dt> <dd>

Spécifie si le paramètre d’exception de pare-feu pour Bureau à distance sera modifié à l’état spécifié par le paramètre *AllowTSConnections* . Il doit s’agir de l’une des valeurs suivantes.

<dt>

<span id="0"></span>

<span id="0"></span>**entre**


</dt> <dd>

Ne modifiez pas le paramètre d’exception de pare-feu.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Modifiez le paramètre d’exception de pare-feu.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une réussite en cas de réussite ; Sinon, retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) . La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.

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

 

