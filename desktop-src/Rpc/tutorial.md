---
title: Didacticiel
description: Ce didacticiel vous guide tout au long des étapes nécessaires à la création d’une application distribuée simple, à un seul client et à un seul serveur à partir d’une application autonome existante.
ms.assetid: afdfa037-58c0-4dcf-aa27-6839db0515e6
keywords:
- RPC appel de procédure distante, didacticiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c19b0d8ec3b3eb55cf29ccfd87eca43775c2ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011400"
---
# <a name="tutorial"></a>Didacticiel

Ce didacticiel vous guide tout au long des étapes nécessaires à la création d’une application distribuée simple, à un seul client et à un seul serveur à partir d’une application autonome existante. Ces étapes sont les suivantes :

-   Créer des fichiers de définition d’interface et de configuration d’application.
-   Utilisez le compilateur MIDL pour générer des stubs client et serveur en langage C à partir de ces fichiers.
-   Écrire une application cliente qui gère sa connexion au serveur.
-   Écrivez une application serveur qui contient les procédures distantes réelles.
-   Compilez et liez ces fichiers à la bibliothèque Runtime RPC pour produire l’application distribuée.

L’application cliente transmet une chaîne de caractères au serveur dans un appel de procédure distante, et le serveur imprime la chaîne « Hello, World » à sa sortie standard.

Les fichiers sources complets de cet exemple d’application, avec du code supplémentaire pour gérer l’entrée de la ligne de commande et pour sortir les différents messages d’état de l’utilisateur, se trouvent dans le \\ répertoire RPC Hello du kit de développement logiciel (SDK) de la plateforme.

Cette section présente la discussion dans les rubriques suivantes :

-   [Application autonome](the-standalone-application.md)
-   [Définition de l’interface](defining-the-interface.md)
-   [Génération de l’UUID](generating-the-uuid.md)
-   [Fichier IDL](the-idl-file.md)
-   [Fichier ACF](the-acf-file.md)
-   [Génération des fichiers stub](generating-the-stub-files.md)
-   [L’application cliente](the-client-application.md)
-   [Application serveur](the-server-application.md)
-   [Arrêt de l’application serveur](stopping-the-server-application.md)
-   [Compilation et liaison](compiling-and-linking.md)
-   [Exécution de l'application](running-the-application.md)

 

 




