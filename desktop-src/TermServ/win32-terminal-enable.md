---
title: Activer la méthode de la classe Win32_Terminal
description: La méthode Enable désactive ou active le terminal.
ms.assetid: f249563b-6fa0-413c-9fc7-01dd16d5c561
ms.tgt_platform: multiple
keywords:
- Activer la méthode Services Bureau à distance
- Activer la Services Bureau à distance de méthode, classe Win32_Terminal
- Win32_Terminal de la classe Services Bureau à distance, Enable, méthode
topic_type:
- apiref
api_name:
- Win32_Terminal.Enable
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afedef572c65f249c48da850172bb9fc4d222c19
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856810"
---
# <a name="enable-method-of-the-win32_terminal-class"></a>Activer la méthode de la \_ classe de terminal Win32

La méthode **Enable** désactive ou active le terminal.

## <a name="syntax"></a>Syntaxe


```mof
uint32 Enable(
  [in] uint32 fEnableTerminal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fEnableTerminal* \[ dans\]
</dt> <dd>

Indicateur qui désactive ou active le terminal.

<dt>

<span id="0"></span>

<span id="0"></span>**entre**


</dt> <dd>

Le terminal est désactivé.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Le terminal est activé.

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

[**\_Terminal Win32**](win32-terminal.md)
</dt> </dl>

 

