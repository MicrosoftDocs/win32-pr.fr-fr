---
title: Classe Win32_TSVirtualDesktopServerSettings
description: Contient les informations de configuration d’un serveur de serveur hôte de virtualisation des services Bureau à distance (hôte de virtualisation des services Bureau à distance).
ms.assetid: 749018aa-a8aa-433e-985b-40b44ef8aa7f
ms.tgt_platform: multiple
keywords:
- Win32_TSVirtualDesktopServerSettings de la classe Services Bureau à distance
- Win32_TSVirtualDesktopServerSettings de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSVirtualDesktopServerSettings
- Win32_TSVirtualDesktopServerSettings.SessionBrokerName
- Win32_TSVirtualDesktopServerSettings.PolicySourceSessionBrokerName
- Win32_TSVirtualDesktopServerSettings.Concurrency
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f40e7d51ee0c92e50afca023629bb92de9f506b3e47ee9e520aa16c09640375b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137462"
---
# <a name="win32_tsvirtualdesktopserversettings-class"></a>\_Classe TSVirtualDesktopServerSettings Win32

Contient les informations de configuration d’un serveur de serveur hôte de virtualisation des services Bureau à distance (hôte de virtualisation des services Bureau à distance).

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[singleton, dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVirtualDesktopServerSettings
{
  string SessionBrokerName;
  sint32 PolicySourceSessionBrokerName;
  uint32 Concurrency;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSVirtualDesktopServerSettings** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSVirtualDesktopServerSettings** a ces propriétés.

<dl> <dt>

**Concurrency**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Nombre maximal de demandes de configuration simultanées autorisées pour ce serveur de bureau virtuel.

</dd> <dt>

**PolicySourceSessionBrokerName**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la valeur est 0, cela indique que la propriété **SessionBrokerName** est configurée par le serveur. Si la valeur est 1, cela indique que la propriété **SessionBrokerName** est configurée par une stratégie de groupe.

</dd> <dt>

**SessionBrokerName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Nom unique du service session Broker pour le serveur hôte de virtualisation des services Bureau à distance.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                             |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

 





