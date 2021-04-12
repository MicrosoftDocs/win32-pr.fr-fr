---
title: Créer une méthode de la classe Win32_Terminal
description: Crée un terminal avec les paramètres par défaut qui peuvent être personnalisés à l’aide des propriétés et des méthodes des \_ classes TerminalSetting Win32.
ms.assetid: 64c90695-72d4-42be-a37a-89b54c04a78c
ms.tgt_platform: multiple
keywords:
- Créer une méthode Services Bureau à distance
- Create Method Services Bureau à distance, Win32_Terminal Class
- Win32_Terminal de la classe Services Bureau à distance, Create, méthode
topic_type:
- apiref
api_name:
- Win32_Terminal.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f1edfa22893452f81cf4695a50380842fa5c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464591"
---
# <a name="create-method-of-the-win32_terminal-class"></a>Créer une méthode de la \_ classe de terminal Win32

La méthode **Create** crée un terminal avec les paramètres par défaut qui peuvent être personnalisés à l’aide des propriétés et des méthodes des classes [**\_ TerminalSetting Win32**](win32-terminalsetting.md) . La fonction retourne zéro en cas de réussite et une erreur en cas d’échec.

## <a name="syntax"></a>Syntaxe


```mof
uint32 Create(
  [in] string NewTerminalName,
  [in] string Transport,
  [in] string TerminalProtocol
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NewTerminalName* \[ dans\]
</dt> <dd>

Nom du terminal.

</dd> <dt>

*Transport* \[ dans\]
</dt> <dd>

Transport pour le terminal. Il s’agit d’une propriété de la classe [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md) .

</dd> <dt>

*TerminalProtocol* \[ dans\]
</dt> <dd>

Protocole pour le terminal. Il s’agit d’une propriété de la classe [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

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

[**\_Terminal Win32**](win32-terminal.md)
</dt> </dl>

 

