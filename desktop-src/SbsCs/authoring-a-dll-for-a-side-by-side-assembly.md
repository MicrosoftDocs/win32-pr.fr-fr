---
description: Lorsque vous créez vos propres assemblys côte à côte, suivez les instructions relatives à la création d’assemblys côte à côte.
ms.assetid: e5fc3bae-0646-4418-a8f7-369856f03cd5
title: Création de dll pour les assemblys côte à côte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb83ba1d788d82e8d4fa7ab5f657170875b5deee6921aec3013406328dc2fcf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142452"
---
# <a name="authoring-dlls-for-side-by-side-assemblies"></a>Création de dll pour les assemblys côte à côte

Lorsque vous créez vos propres assemblys côte à côte, suivez les [instructions relatives à la création d’assemblys côte à côte](guidelines-for-creating-side-by-side-assemblies.md) et créez les DLL utilisées dans l’assembly conformément aux indications suivantes :

-   Vos dll doivent être conçues de manière à ce que plusieurs versions puissent s’exécuter en même temps et dans le même processus sans interférer les unes avec les autres. Par exemple, de nombreuses applications hébergent plusieurs plug-ins qui requièrent chacun une version différente d’un composant. Le développeur doit concevoir et tester l’assembly côte à côte pour s’assurer que plusieurs versions du composant fonctionnent correctement lorsqu’elles sont exécutées en même temps dans le même processus.

-   si vous envisagez de fournir votre composant en tant que composant partagé sur des systèmes antérieurs à Windows XP, vous devez continuer à installer le composant sur ces systèmes en tant que composant partagé d’instance unique. Dans ce cas, vous devez vous assurer que votre composant est à compatibilité descendante.

-   Évaluer l’utilisation des objets quand plusieurs versions de votre assembly sont exécutées sur le système. déterminez si les différentes versions de l’assembly nécessitent des structures de données distinctes, telles que les fichiers mappés en mémoire, les canaux nommés, les messages et les classes inscrits Windows, la mémoire partagée, les sémaphores, les mutex et les pilotes matériels. Toutes les structures de données utilisées dans les versions d’assembly doivent être à compatibilité descendante. Déterminez les structures de données qui peuvent être utilisées dans les différentes versions et les structures de données qui doivent être privées pour une version. Déterminez si les structures de données partagées nécessitent des objets de synchronisation distincts, tels que des sémaphores et des mutex.

-   Certains objets, tels que les classes de fenêtre et les atomes, sont nommés de manière unique pour chaque processus. Les objets tels que les classes de fenêtre doivent être dotés d’un contrôle de version pour chaque assembly utilisant le manifeste. Pour les objets tels que les atomes, utilisez des identificateurs spécifiques à la version, sauf si vous envisagez de partager entre les versions. Si vous utilisez des identificateurs spécifiques à la version, utilisez le numéro de version en quatre parties.

-   N’incluez pas de code auto-inscrit dans une DLL. Une DLL dans un assembly côte à côte ne peut pas s’inscrire automatiquement.

-   Définissez tous les noms spécifiques à la version dans votre DLL avec des \# instructions define. Cela permet de modifier toutes les clés de Registre à partir d’un emplacement. Lorsque vous publiez une nouvelle version de votre assembly, il vous suffit de modifier cette \# instruction de définition. Par exemple :

    `#define MyRegistryKey "MyAssembly1.0.0.0"`

-   Stockez les données non persistantes dans le répertoire Temp.

-   Ne placez pas de données utilisateur dans des emplacements globaux. Conserver les données d’application séparées des données utilisateur.

-   Affectez à tous les fichiers partagés une version de fichier qui dépend du nom de l’application.

-   Affectez à tous les messages et toutes les structures de données utilisés dans les processus une version pour empêcher le partage interprocessus accidentel.

-   Votre DLL ne doit pas dépendre du partage entre les versions qui n’existent pas, telles que les sections de mémoire partagée qui ne sont pas partagées entre différentes versions de votre assembly.

-   Si vous ajoutez de nouvelles fonctionnalités qui ne suivent pas le contrat de compatibilité avec l’interface binaire de la DLL d’origine, vous devez assigner un nouveau CLSID, ProgId et nom de fichier. Les futures versions de votre assembly côte à côte sont alors requises pour utiliser ce CLSID, ce ProgId et ce nom de fichier. Cela empêche un conflit quand une version de la DLL qui n’est pas côte à côte est inscrite sur une version côte à côte.

-   Si vous réutilisez le même CLSID ou ProgId, effectuez un test pour vérifier que l’assembly est à compatibilité descendante.

-   Initialisez et définissez les paramètres par défaut de l’assembly dans le code de l’assembly. N’enregistrez pas les paramètres par défaut dans le registre.

-   Assignez des versions à toutes les structures de données.

-   votre DLL doit stocker l’état de l’assembly côte à côte, comme décrit dans la section création d’un [état Stockage pour les assemblys côte à côte](authoring-state-storage-for-side-by-side-assemblies.md).

 

 



