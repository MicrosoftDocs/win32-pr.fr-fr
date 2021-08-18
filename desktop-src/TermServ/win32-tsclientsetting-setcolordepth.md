---
title: Méthode SetColorDepth de la classe Win32_TSClientSetting
description: La méthode SetColorDepth définit la propriété ColorDepth pour la classe.
ms.assetid: 1ab8ac41-cbbf-4077-b91e-692856ccba42
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetColorDepth
- Services Bureau à distance de la méthode SetColorDepth, classe Win32_TSClientSetting
- Win32_TSClientSetting de la classe Services Bureau à distance, méthode SetColorDepth
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepth
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2c7f31ef04fdfb9dcbfee5e1ca3dcec1386a7dbd0c20824b00bdfe41ac6d48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999859"
---
# <a name="setcolordepth-method-of-the-win32_tsclientsetting-class"></a>Méthode SetColorDepth de la \_ classe Win32 TSClientSetting

La méthode **SetColorDepth** définit la propriété **ColorDepth** pour la classe.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetColorDepth(
  [in] uint32 ColorDepth
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ColorDepth* \[ dans\]
</dt> <dd>

Nouvelle valeur de la propriété **ColorDepth** .

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

8 bits par pixel

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

15 bits par pixel

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**1,3**


</dt> <dd>

16 bits par pixel

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

24 bits par pixel

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5,5**


</dt> <dd>

32 bits par pixel

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

[**\_TSClientSetting Win32**](win32-tsclientsetting.md)
</dt> </dl>

 

