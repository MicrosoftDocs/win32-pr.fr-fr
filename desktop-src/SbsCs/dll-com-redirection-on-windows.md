---
description: La redirection DLL/COM est une stratégie d’isolation d’application utilisée par les administrateurs d’entreprise sur Windows XP.
ms.assetid: 5bbb0bee-d457-4dfa-93a0-82537fe11f2d
title: Redirection DLL/COM sur Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e356c7b4cc6e5616a03eba60439c7478d65e626a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867269"
---
# <a name="dllcom-redirection-on-windows"></a>Redirection DLL/COM sur Windows

La redirection DLL/COM est une stratégie d’isolation d’application utilisée par les administrateurs d’entreprise sur Windows XP.

* * Windows Server 2008, Windows Vista, Windows Server 2003 et Windows XP avec SP2 : * * l’utilisation de stratégies de redirection DLL/COM n’est pas recommandée, car les applications isolées qui utilisent des manifestes et des [assemblys côte à côte](about-side-by-side-assemblies-.md) peuvent être plus faciles à mettre à jour et à traiter. La présence d’un fichier. local est ignorée si un manifeste est présent. La stratégie de redirection DLL/COM à l’aide des fichiers. local fonctionne si l’application n’a pas de manifeste.

La redirection DLL/COM lie une application à une version locale d’un composant. Les fichiers du composant local peuvent être conservés séparément de la version du système du composant à un emplacement privé pour l’application. La version du système du composant est inscrite globalement et disponible pour toutes les autres applications qui y sont liées. La version locale du composant est réservée à l’utilisation exclusive de l’application. Si nécessaire, les fichiers de composants utilisés par l’application peuvent être chargés en mémoire en même temps que les fichiers de composants du système.

La redirection DLL/COM est activée en installant un fichier spécial avec une copie du fichier de composant local dans le même répertoire que le fichier exécutable de l’application. Le fichier spécial est un fichier vide nommé d’après le nom de fichier de l’exécutable de l’application et ajouté avec. local. Par exemple, pour activer la redirection DLL/COM pour une application nommée MyApp, la version locale du composant et un fichier vide nommé Myapp.exe. local doivent être copiés dans le dossier contenant Myapp.exe. Cela permet de lier l’application à la version locale du composant plutôt qu’à la version globale partagée du composant.

Quand une application charge un fichier de composant, tel qu’un fichier DLL ou. ocx, Windows commence par la recherche dans le dossier où le fichier. local et exécutable de l’application est installé. S’il est trouvé, l’application utilise ce fichier de composant quel que soit le chemin de recherche de répertoire défini dans l’application ou le registre. S’il est introuvable, le fichier composant dans le chemin de recherche défini est utilisé.

L’utilitaire d’installation doit effectuer les opérations suivantes pour installer l’application à l’aide de la redirection DLL/COM :

-   Un fichier. local vide doit être copié dans le même dossier que le fichier exécutable de l’application.
-   Tous les composants, DLL et fichiers. ocx utilisés par l’application doivent être copiés dans le même dossier que le fichier exécutable de l’application.
-   Les composants COM isolés doivent être inscrits auprès de Windows afin que les différentes versions de l’assembly n’entrent pas en conflit les unes avec les autres lorsqu’elles sont chargées en mémoire en même temps. Le processus d’inscription requiert que, bien que l’implémentation du composant puisse changer d’une version à l’autre, certaines métadonnées COM telles que le CLSID, le ProgID, la bibliothèque de types et le modèle de thread ne peuvent pas.
-   Si l’application est installée à l’aide de la Windows Installer, le répertoire de l’application peut être sécurisé à l’aide de la table LockPermissions. En règle générale, le système reçoit un accès en lecture, écriture et exécution ; tous les autres processus sont fournis uniquement pour l’accès en lecture et en lecture.

 

 



