---
title: Méthode SetPolicyPropertyName de la classe Win32_TerminalServiceSetting
description: La méthode SetPolicyPropertyName définit la propriété DeleteTempFolders, UseTempFolders ou Help pour la classe.
ms.assetid: 18d9927a-b7db-46c7-90ee-00da6de06202
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetPolicyPropertyName
- Services Bureau à distance de la méthode SetPolicyPropertyName, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode SetPolicyPropertyName
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPolicyPropertyName
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f49732fa916dd3c37539dc35d6cef7a4d920d81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919600"
---
# <a name="setpolicypropertyname-method-of-the-win32_terminalservicesetting-class"></a>Méthode SetPolicyPropertyName de la \_ classe Win32 TerminalServiceSetting

La méthode **SetPolicyPropertyName** définit la propriété **DeleteTempFolders**, **UseTempFolders** ou **Help** pour la classe.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetPolicyPropertyName(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PropertyName* \[ dans\]
</dt> <dd>

Spécifie la propriété de stratégie définie par la méthode.

<dt>

<span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>

<span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>**DeleteTempFolders**


</dt> <dd>

La méthode définit la propriété **DeleteTempFolders** .

</dd> <dt>

<span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>

<span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>**UseTempFolders**


</dt> <dd>

La méthode définit la propriété **UseTempFolders** .

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>**Aide**


</dt> <dd>

La méthode définit la propriété **d’aide** .

**Remarque :**  **l’aide** n’est pas prise en charge

</dd> </dl> </dd> <dt>

*Valeur* \[ dans\]
</dt> <dd>

Valeur qui indique s’il faut activer ou désactiver la propriété spécifiée par le paramètre *PropertyName* .

<dt>

<span id="0"></span>

<span id="0"></span>**entre**


</dt> <dd>

Désactivez la propriété.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Activez la propriété.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une réussite en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) . La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.

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

 

