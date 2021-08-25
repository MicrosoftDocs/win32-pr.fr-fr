---
title: Méthode SetLoadBalancingState de la classe Win32_TSSessionDirectory
description: Définit la valeur pour indiquer si le serveur doit participer à l’équilibrage de charge de Connexion Bureau à distance Broker (RD Connection Broker).
ms.assetid: 6368043c-1808-4757-9756-10b3800190b0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetLoadBalancingState
- Services Bureau à distance de la méthode SetLoadBalancingState, classe Win32_TSSessionDirectory
- Win32_TSSessionDirectory de la classe Services Bureau à distance, méthode SetLoadBalancingState
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetLoadBalancingState
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23d539f07c97e4e5b92152190a7bb38a8132d31a73daf08de8f140a39f67efdb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987949"
---
# <a name="setloadbalancingstate-method-of-the-win32_tssessiondirectory-class"></a>Méthode SetLoadBalancingState de la \_ classe Win32 TSSessionDirectory

Définit la valeur pour indiquer si le serveur doit participer à l’équilibrage de charge de Connexion Bureau à distance Broker (RD Connection Broker).

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetLoadBalancingState(
  [in] uint32 StateValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StateValue* \[ dans\]
</dt> <dd>

Type : **UInt32**

Indique si le serveur doit participer à l’équilibrage de charge du Service Broker pour les connexions Bureau à distance.

<dt>

0
</dt> <dd>

Le serveur ne participe pas à l’équilibrage de charge du Service Broker pour les connexions Bureau à distance.

</dd> <dt>

1
</dt> <dd>

Le serveur fera partie de l’équilibrage de charge du Service Broker pour les connexions Bureau à distance.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Le serveur doit être joint à une batterie de serveurs du Service Broker pour les connexions Bureau à distance.

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

 

