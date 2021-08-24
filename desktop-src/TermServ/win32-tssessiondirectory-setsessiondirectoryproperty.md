---
title: Méthode SetSessionDirectoryProperty de la classe Win32_TSSessionDirectory
description: Définit la propriété SessionDirectoryLocation ou la propriété SessionDirectoryClusterName de la classe.
ms.assetid: 728e1991-294f-4b80-86f8-a0c2cfd10e9c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetSessionDirectoryProperty
- Services Bureau à distance de la méthode SetSessionDirectoryProperty, classe Win32_TSSessionDirectory
- Win32_TSSessionDirectory de la classe Services Bureau à distance, méthode SetSessionDirectoryProperty
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf09cbf8e832446831a5b12ecce8cc00b61bc49b23a8ed1da7f291d6f0c3562c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769299"
---
# <a name="setsessiondirectoryproperty-method-of-the-win32_tssessiondirectory-class"></a>Méthode SetSessionDirectoryProperty de la \_ classe Win32 TSSessionDirectory

Définit la propriété **SessionDirectoryLocation** ou la propriété **SessionDirectoryClusterName** de la classe.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetSessionDirectoryProperty(
  [in] string PropertyName,
  [in] string Value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PropertyName* \[ dans\]
</dt> <dd>

Type : **chaîne**

Spécifie la propriété définie par la méthode.

<dt>

<span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>

<span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>**SessionDirectoryLocation**


</dt> <dd>

La méthode définit la propriété **SessionDirectoryLocation** .

</dd> <dt>

<span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>

<span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>**SessionDirectoryClusterName**


</dt> <dd>

La méthode définit la propriété **SessionDirectoryClusterName** .

</dd> </dl> </dd> <dt>

*Valeur* \[ dans\]
</dt> <dd>

Type : **chaîne**

Nouvelle valeur de la propriété spécifiée par le paramètre *PropertyName* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) . La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.

## <a name="remarks"></a>Remarques

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

