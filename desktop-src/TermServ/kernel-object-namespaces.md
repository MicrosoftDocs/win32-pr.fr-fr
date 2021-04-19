---
title: Espaces de noms d’objets de noyau
description: Services Bureau à distance utilise plusieurs espaces de noms pour les objets de noyau ; un espace de noms global est principalement utilisé par les services dans les applications client/serveur.
ms.assetid: 771e0bbf-bd73-4e87-aa1e-945c1287b517
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20680a32c8b35e3fa2f1ab15c732683d424550f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510901"
---
# <a name="kernel-object-namespaces"></a>Espaces de noms d’objets de noyau

Un serveur de Services Bureau à distance possède plusieurs espaces de noms pour les objets de noyau nommés suivants : événements, sémaphores, mutex, minuteries prédéfinies, objets de mappage de fichiers et objets de traitement. Il existe un espace de noms global utilisé principalement par les services dans les applications client/serveur. En outre, chaque session client dispose d’un espace de noms distinct pour ces objets, comme dans Windows Vista.

Les espaces de noms de session client distincts permettent à plusieurs clients d’exécuter les mêmes applications sans interférer entre eux. Pour les processus démarrés dans le cadre d’une session cliente, le système utilise l’espace de noms de session par défaut. Toutefois, ces processus peuvent utiliser l’espace de noms global en ajoutant le \\ préfixe « global » au nom de l’objet. Par exemple, le code suivant appelle [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) et crée un objet d’événement nommé CSAPP dans l’espace de noms global :

> [!Note]  
> L’espace de noms global n’est pas disponible pour les applications du Windows Store.

 

`CreateEvent( NULL, FALSE, FALSE, "Global\\CSAPP" );`

Les applications de service dans un environnement de Services Bureau à distance utilisent l’espace de noms global par défaut.

La session zéro est utilisée uniquement pour les services d’hébergement, et il n’existe aucune session de console, contrairement aux versions précédentes de Windows.

L’espace de noms global permet aux processus sur plusieurs sessions clientes de communiquer avec une application de service. Par exemple, une application client/serveur peut utiliser un objet mutex pour la synchronisation. Le module de serveur peut créer l’objet mutex dans l’espace de noms global. Ensuite, une session cliente peut utiliser le \\ préfixe « global » pour ouvrir l’objet Mutex.

L’espace de noms global est également utilisé pour les applications qui utilisent des objets nommés pour détecter qu’une instance de l’application est déjà en cours d’exécution dans le système pour toutes les sessions. Cet objet nommé doit être créé ou ouvert dans l’espace de noms global au lieu de l’espace de noms par session. Le cas le plus courant de l’exécution de l’application une fois par session est pris en charge par défaut, car l’objet nommé est créé dans un espace de noms par session.

Outre le préfixe « global \\ », les processus clients peuvent utiliser le \\ préfixe « local » pour créer explicitement un objet dans leur espace de noms de session. Ces mots clés respectent la casse.

Le \\ préfixe « session » est réservé à l’utilisation du système et vous ne devez pas l’utiliser dans les noms des objets du noyau.

Le changement rapide d’utilisateur est implémenté à l’aide de sessions de Services Bureau à distance. Le premier utilisateur qui se connecte utilise la session un, le prochain utilisateur à se connecter utilise la session deux, et ainsi de suite. Les noms d’objets de noyau doivent respecter les instructions indiquées pour Services Bureau à distance afin que les applications puissent prendre en charge plusieurs utilisateurs.

La création d’un objet de mappage de fichier dans l’espace de noms global, à l’aide de [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga), à partir d’une session autre que la session zéro est une opération privilégiée. Pour cette raison, [SeCreateGlobalPrivilege](/windows/desktop/SecAuthZ/authorization-constants) doit être activé pour qu’une application exécutée dans une session de serveur de l’hôte de session Bureau à distance arbitraire Bureau à distance soit activée afin de pouvoir créer un objet de mappage de fichiers dans l’espace de noms global. La vérification des privilèges est limitée à la création d’objets de mappage de fichiers et ne s’applique pas à l’ouverture de ceux qui existent déjà. Par exemple, si un service ou le système crée un objet de mappage de fichiers, tout processus en cours d’exécution dans une session peut accéder à cet objet de mappage de fichiers, à condition que l’utilisateur dispose de l’accès nécessaire.

 

 