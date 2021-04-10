---
title: Surveillance des connexions et des déconnexions de session
description: Pour inscrire une application avec Services Bureau à distance, stockez le nom de l’application de serveur de canal virtuel dans le registre en ajoutant une sous-clé.
ms.assetid: 8524cb7a-a930-431a-bc5f-b0793781de15
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e819b13594ecec14a2b425560152cadedd4e9122
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031344"
---
# <a name="monitoring-session-connections-and-disconnections"></a>Surveillance des connexions et des déconnexions de session

Pour une application de service, telle qu’une application de serveur de canal virtuel, pour surveiller les connexions et les déconnexions de session, vous devez l’inscrire auprès de Services Bureau à distance. Pour inscrire l’application auprès de Services Bureau à distance, stockez le nom de l’application de serveur de canal virtuel dans le registre en ajoutant une sous-clé sous l’emplacement suivant :

**HKEY \_ \_** \\  \\  \\  \\  \\ **Compléments** TerminalServer du contrôle CurrentControlSet du système de l’ordinateur local

La sous-clé peut avoir n’importe quel nom. Elle doit avoir une valeur **reg \_ SZ** , **Name**, qui contient le nom symbolique de l’application.

``` syntax
Name = AddinName
```

La longueur maximale de la sous-clé et de la valeur de **Name** est de 99 caractères.

La sous-clé doit également avoir une valeur **reg \_ DWORD** qui indique le type d’application serveur.

``` syntax
Type = AddinType
```

*AddinType* doit avoir la valeur suivante.



| Valeur | Signification                               |
|-------|---------------------------------------|
| 3     | Application en mode utilisateur, espace de session. |



 

L’inscription de l’application de service prend effet uniquement dans les sessions créées après l’inscription.

Pour chaque application de service inscrite, Services Bureau à distance signale un ensemble d’objets d’événement lorsqu’un client se connecte ou se déconnecte de la session. Chaque plug-in de canal virtuel doit s’inscrire et créer les événements de notification en appelant [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa). Les noms de ces objets d’événement respectent le format suivant.

``` syntax
AddinName-Reconnect

AddinName-Disconnect
```

*AddInName* est la chaîne spécifiée dans la valeur **Name** de la sous-clé de Registre sous laquelle l’application serveur est inscrite. La création de ces événements dans une session entraîne leur création dans un répertoire d’événements par session spécial. Le répertoire des événements fournit une sécurité supplémentaire en empêchant les applications d’autres sessions de modifier l’état de ces événements.

Pour contrôler si les événements de reconnexion et de déconnexion sont reçus sur le serveur, vous pouvez placer l’indicateur **RemoteControlPersistent** dans le Registre sous la clé suivante :

**HKEY \_ Système d' \_ ordinateur local** \\  \\  \\ **contrôle** CurrentControlSet \\ **TerminalServer** \\ **AddIns** \\ *AddInName*

L’indicateur active ou désactive les événements de reconnexion et de déconnexion lorsqu’une session cliente démarre ou s’arrête. La syntaxe de la valeur **reg \_ DWORD** est la suivante.

``` syntax
RemoteControlPersistent = flag
```

La valeur de *Flag* peut être un ou zéro. Zéro est la valeur par défaut. Si la valeur est définie sur un, l’application de service n’est pas avertie si la session cliente est démarrée ou arrêtée. Si la valeur est zéro, un événement de reconnexion est signalé au démarrage de la session cliente et un événement de déconnexion est signalé lorsque la session cliente s’arrête.

Le format de nom d’objet d’événement précédent est toujours pris en charge dans Windows Server 2008 pour des raisons de compatibilité descendante. Nous vous recommandons d’utiliser le format Windows Server 2008 plus récent, car il est plus sécurisé.

Le format d’événement précédent est le suivant.

``` syntax
Global\AddinName-SessionId-Reconnect
 
Global\AddinName-SessionId-Disconnect
```

*AddInName* est la chaîne spécifiée dans la valeur **Name** de la sous-clé de Registre sous laquelle l’application serveur est inscrite. *SessionID* est l’identificateur de session d’une session cliente.

 

 