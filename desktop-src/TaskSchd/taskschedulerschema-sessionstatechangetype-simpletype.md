---
title: Type simple sessionStateChangeType
description: Définit des valeurs pour le type de Terminal Server changement d’état de session que vous pouvez utiliser pour déclencher le démarrage d’une tâche.
ms.assetid: 56e19ec0-ea6c-4434-ab9d-a1069108920f
keywords:
- Planificateur de tâches de type simple sessionStateChangeType
topic_type:
- apiref
api_name:
- sessionStateChangeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a77fb563b59ccd8d63d38c6c85f16ff74ac404b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466415"
---
# <a name="sessionstatechangetype-simple-type"></a>Type simple sessionStateChangeType

Définit des valeurs pour le type de Terminal Server changement d’état de session que vous pouvez utiliser pour déclencher le démarrage d’une tâche.

``` syntax
<xs:simpleType name="sessionStateChangeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="ConsoleConnect"
         />
        <xs:enumeration
            value="ConsoleDisconnect"
         />
        <xs:enumeration
            value="RemoteConnect"
         />
        <xs:enumeration
            value="RemoteDisconnect"
         />
        <xs:enumeration
            value="SessionLock"
         />
        <xs:enumeration
            value="SessionUnlock"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valeurs d’énumération

Le type simple **sessionStateChangeType** définit les valeurs suivantes.



| Valeur             | Description                                                                                                                                                                                       |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ConsoleConnect    | Modification de l’état de la connexion à la console Terminal Server. Par exemple, lorsque vous vous connectez à une session utilisateur sur l’ordinateur local en basculant les utilisateurs sur l’ordinateur. <br/>                            |
| ConsoleDisconnect | Modification de l’état de déconnexion de la console Terminal Server. Par exemple, lorsque vous vous déconnectez à une session utilisateur sur l’ordinateur local en basculant les utilisateurs sur l’ordinateur. <br/>                      |
| RemoteConnect     | Terminal Server modification de l’état de la connexion à distance. Par exemple, lorsqu’un utilisateur se connecte à une session utilisateur à l’aide du programme Connexion Bureau à distance à partir d’un ordinateur distant. <br/>            |
| RemoteDisconnect  | Terminal Server modification de l’état de la déconnexion distante. Par exemple, lorsqu’un utilisateur se déconnecte d’une session utilisateur lors de l’utilisation du programme Connexion Bureau à distance à partir d’un ordinateur distant. <br/> |
| SessionLock       | Terminal Server modification de l’état verrouillé de la session. Par exemple, ce changement d’État provoque l’exécution de la tâche lorsque l’ordinateur est verrouillé. <br/>                                                       |
| SessionUnlock     | Modification de l’état de déverrouillage de la session Terminal Server. Par exemple, ce changement d’État provoque l’exécution de la tâche lorsque l’ordinateur est déverrouillé.<br/>                                                    |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





