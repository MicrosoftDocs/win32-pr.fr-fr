---
title: Méthode SetClientProperty de la classe Win32_TSClientSetting
description: La méthode SetClientProperty définit la propriété LPTPortMapping, COMPortMapping, AudioMapping, ClipboardMapping, DriveMapping ou WindowsPrinterMapping pour la classe.
ms.assetid: a8ad922f-d768-4708-9a67-c6b00580baed
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetClientProperty
- Services Bureau à distance de la méthode SetClientProperty, classe Win32_TSClientSetting
- Win32_TSClientSetting de la classe Services Bureau à distance, méthode SetClientProperty
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetClientProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89bfdfd7c7f2c4b23f76b50ab671d74541f9dbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510317"
---
# <a name="setclientproperty-method-of-the-win32_tsclientsetting-class"></a>Méthode SetClientProperty de la \_ classe Win32 TSClientSetting

La méthode **SetClientProperty** définit la **propriété LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping** ou **WindowsPrinterMapping** pour la classe.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetClientProperty(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PropertyName* \[ dans\]
</dt> <dd>

Spécifie la propriété cliente définie par la méthode.

<dt>

<span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>

<span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>**AudioMapping**


</dt> <dd>

La méthode définit la propriété **AudioMapping** .

</dd> <dt>

<span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>

<span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>**ClipboardMapping**


</dt> <dd>

La méthode définit la propriété **ClipboardMapping** .

</dd> <dt>

<span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>

<span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>**COMPortMapping**


</dt> <dd>

La méthode définit la propriété **COMPortMapping** .

</dd> <dt>

<span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>

<span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>**DriveMapping**


</dt> <dd>

La méthode définit la propriété **DriveMapping** .

</dd> <dt>

<span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>

<span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>**LPTPortMapping**


</dt> <dd>

La méthode définit la propriété **LPTPortMapping** .

</dd> <dt>

<span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>

<span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>**PNPRedirection**


</dt> <dd>

La méthode définit la propriété **PNPRedirection** .

</dd> <dt>

<span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>

<span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>**WindowsPrinterMapping**


</dt> <dd>

La méthode définit la propriété **WindowsPrinterMapping** .

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

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) . La méthode retourne une erreur si la propriété cliente spécifiée n’est pas sous contrôle de stratégie de groupe ou si le paramètre de propriété n’est pas éligible pour la substitution par le serveur.

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

[**\_TSClientSetting Win32**](win32-tsclientsetting.md)
</dt> </dl>

 

