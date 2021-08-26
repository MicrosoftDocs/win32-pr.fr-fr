---
title: Handles de contexte
description: Il arrive parfois que les applications distribuées requièrent que le programme serveur gère les informations d’État entre les appels des clients.
ms.assetid: 91732a75-0a3a-44bd-9db9-c11be6fd2d70
keywords:
- Appel de procédure distante RPC, décrit, handles de contexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73fb49a2e4c09ec818777389194df98e0d7b8bcac618d05ff7b519aefe5eb28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073419"
---
# <a name="context-handles"></a>Handles de contexte

Il arrive parfois que les applications distribuées requièrent que le programme serveur gère les informations d’État entre les appels des clients. Les programmes serveur qui desservent plusieurs clients à la fois doivent conserver les informations d’état de chaque client. Étant donné que le client et le serveur utilisent des espaces d’adressage différents sur des ordinateurs différents et qu’ils ne s’approuvent pas nécessairement l’un l’autre, les approches courantes du partage de données ne fonctionnent pas souvent. Par exemple, le client et le serveur ne peuvent pas conserver les informations d’État sur leur session à distance dans les variables globales, car ils ne partagent pas le même espace d’adressage global. Il est difficile de conserver les informations dans un fichier partagé, car elles s’exécutent sur des ordinateurs différents. Une approche simpliste peut consister à expédier tout l’État au client et à faire en sorte que le client le retourne lors de l’appel suivant, mais cette approche présente des défauts : le serveur n’approuve pas nécessairement le client pour retourner l’état correct, et l’État peut être implicitement lié à un autre État sur le serveur, tel que des handles de fichiers ou des sockets ouverts

Microsoft RPC fournit un mécanisme puissant et sécurisé appelé descripteurs de contexte pour conserver l’état associé à un client donné sur un serveur. Les informations d’État sont appelées le contexte du serveur. Les clients peuvent obtenir un handle de contexte pour identifier le contexte du serveur pour leurs sessions RPC individuelles.

Par exemple, chaque client dans une application distribuée peut faire en sorte que le programme serveur crée et met à jour un fichier de données pour sa session RPC. Le serveur peut utiliser son descripteur de fichier pour le fichier de données de chaque client comme handle de contexte. Chaque fois qu’un client demande des opérations sur le fichier de données que le serveur crée pour celui-ci, le client passe le descripteur de contexte au serveur. Le client n’obtient pas réellement le descripteur de fichier lui-même ; elle obtient un jeton opaque que l’heure d’exécution RPC du serveur peut associer de manière unique au descripteur de fichier. Étant donné que le descripteur de contexte est véritablement un descripteur de fichier, le handle de contexte n’est utile que dans l’espace d’adressage du serveur. Toutefois, le programme client peut utiliser le handle de contexte pour indiquer au serveur sur quel fichier effectuer les mises à jour.

D’autres données peuvent également être des handles de contexte. Par exemple, un client et un serveur peuvent utiliser un numéro d’enregistrement d’un enregistrement de base de données comme descripteur de fichier. Si le client a besoin d’effectuer un certain nombre de mises à jour sur un enregistrement particulier, il peut obtenir le numéro d’enregistrement en tant que descripteur de contexte. Elle transmet le numéro d’enregistrement au serveur chaque fois qu’elle appelle une procédure distante pour mettre à jour l’enregistrement de la base de données.

Le plus souvent, un handle de contexte pointe vers un bloc de mémoire sur le serveur sur lequel le serveur conserve diverses informations de gestion.

Cette section présente des informations sur la définition et l’utilisation des handles de contexte. La discussion est présentée dans les rubriques suivantes :

-   [Développement d’interface à l’aide de handles de contexte](interface-development-using-context-handles.md)
-   [Développement de serveurs à l’aide de handles de contexte](server-development-using-context-handles.md)
-   [Développement de clients à l’aide de handles de contexte](client-development-using-context-handles.md)
-   [Routine d’exécution du contexte de serveur](server-context-run-down-routine.md)
-   [Réinitialisation du contexte client](client-context-reset.md)
-   [Clients multithread et handles de contexte](multithreaded-clients-and-context-handles.md)

 

 




