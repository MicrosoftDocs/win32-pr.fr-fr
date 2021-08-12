---
title: Méthode SetServerWeight de la classe Win32_TSSessionDirectory
description: Définit la valeur du poids du serveur pour l’équilibrage de charge de Connexion Bureau à distance Broker pour les connexions Bureau à distance.
ms.assetid: 9c7563e5-bb45-495d-90b0-43170b58581e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetServerWeight
- Services Bureau à distance de la méthode SetServerWeight, classe Win32_TSSessionDirectory
- Win32_TSSessionDirectory de la classe Services Bureau à distance, méthode SetServerWeight
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetServerWeight
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d8c9af7995f2d42f02075fde8ae43f4b5f5e9a5ccb7d3fa6f4635cb9645464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604628"
---
# <a name="setserverweight-method-of-the-win32_tssessiondirectory-class"></a>Méthode SetServerWeight de la \_ classe Win32 TSSessionDirectory

Définit la valeur du poids du serveur pour l’équilibrage de charge de Connexion Bureau à distance Broker pour les connexions Bureau à distance.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetServerWeight(
  [in] uint32 ServerWeightValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ServerWeightValue* \[ dans\]
</dt> <dd>

Type : **UInt32**

Valeur de poids du serveur. La plage valide est comprise entre 1 et 10000.

</dd> </dl>

## <a name="remarks"></a>Remarques

Par défaut, dans l’interface utilisateur de Services Bureau à distance configuration, la valeur du poids du serveur est 100. Le poids du serveur est relatif. Par conséquent, si vous affectez à un serveur la valeur 100 et une valeur de 200, le serveur avec un poids relatif de 200 recevra deux fois le nombre de sessions.

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

 

