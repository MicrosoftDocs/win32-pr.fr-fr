---
description: Les instructions suivantes expliquent comment créer vos propres assemblys côte à côte COM ou Win32.
ms.assetid: e10fe92c-bce8-420e-a84c-2748e929eb1b
title: Instructions pour la création d’assemblys côte à côte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19054f0c48f74a373f0ce502cb6b52374db5ded00fcde3c284fad2609ba21e5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885249"
---
# <a name="guidelines-for-creating-side-by-side-assemblies"></a>Instructions pour la création d’assemblys côte à côte

Les instructions suivantes expliquent comment créer vos propres assemblys côte à côte COM ou Win32. Vous n’aurez peut-être pas besoin de créer vos propres assemblys côte à côte si les fonctionnalités nécessaires sont fournies par l’un des [assemblys Microsoft côte à côte pris en charge](supported-microsoft-side-by-side-assemblies.md). Dans ce cas, utilisez les assemblys fournis par Microsoft et suivez les procédures d’utilisation des assemblys côte à côte dans [à l’aide d’applications isolées et d’assemblys côte à côte](using-isolated-applications-and-side-by-side-assemblies.md).

Tout d’abord, déterminez si votre composant fait un candidat approprié pour un assembly côte à côte. Pour plus d’informations, consultez [si vous fournissez un composant partagé en tant qu’assembly côte à côte ?](should-you-provide-a-shared-component-as-a-side-by-side-assembly.md)

Pour créer un assembly côte à côte, suivez les instructions suivantes :

-   Choisissez les ressources à inclure dans l’assembly. N’oubliez pas qu’un assembly se compose d’un ou de plusieurs fichiers qui sont toujours fournis aux applications et aux clients ensemble. L’assembly sert d’unité fondamentale pour l’affectation de noms, la liaison, le contrôle de version, le déploiement et la [configuration par défaut](default-configuration.md). En règle générale, si vous savez si deux ressources appartiennent au même assembly, il est recommandé de les créer dans des assemblys distincts. En général, un assembly côte à côte se compose d’une seule DLL.
-   Créez un [manifeste](manifests.md) d’assembly pour l’assembly. Le manifeste doit décrire l’objet COM ou les bibliothèques de types dans l’assembly. Pour plus d’informations sur ce qui doit être créé dans un manifeste d’assembly, consultez [manifestes d’assembly](assembly-manifests.md).
-   Évaluer l’utilisation des objets quand plusieurs versions de votre assembly sont exécutées sur le système. déterminez si les différentes versions de l’assembly nécessitent des structures de données distinctes, telles que les fichiers mappés en mémoire, les canaux nommés, les messages et les classes inscrits Windows, la mémoire partagée, les sémaphores, les mutex et les pilotes matériels. Toutes les structures de données utilisées dans les versions d’assembly doivent être des versions à compatibilité descendante. Déterminez les structures de données qui peuvent être utilisées dans les différentes versions et les structures de données qui doivent être privées pour une version. Déterminez si les structures de données partagées nécessitent des objets de synchronisation distincts, tels que des sémaphores et des mutex.
-   Créez votre DLL pour fonctionner correctement en tant qu’assembly côte à côte en adhérant aux instructions de [création d’une dll pour un assembly côte à côte](authoring-a-dll-for-a-side-by-side-assembly.md).
-   Créez un ensemble de fichiers d’en-tête et de fonctions d’assistance pour fournir un moyen simple aux clés de registre de version contenant l’état de l’assembly. Les assemblys enregistrent généralement leurs paramètres d’État dans les clés de registre. Les paramètres du Registre doivent être écrits sur la base d’une version individuelle pour isoler plusieurs versions d’assembly qui peuvent être exécutées en même temps. Concevez votre assembly côte à côte et votre DLL pour stocker et gérer correctement l’état de l’assembly pendant les scénarios de partage côte à côte. suivez les instructions fournies dans [état de création Stockage pour les assemblys côte à côte](authoring-state-storage-for-side-by-side-assemblies.md).
-   Les développeurs d’applications qui utilisent des [assemblys privés](/windows/desktop/Msi/private-assemblies) doivent sécuriser le répertoire de l’application. si l’application est installée à l’aide de la [Windows Installer](../msi/windows-installer-portal.md), le répertoire de l’application peut être sécurisé à l’aide de la table LockPermissions. En règle générale, le système dispose d’un accès en lecture, écriture et exécution aux assemblys privés. tous les autres processus sont fournis uniquement pour l’accès en lecture et en lecture.
-   Testez l’assembly à l’aide de scénarios avec partage côte à côte pour vous assurer qu’il s’agit d’un assembly côte à côte valide. L’installation réussie de l’assembly n’est pas suffisante pour garantir qu’il fonctionnera comme prévu.
-   Adoptez une méthode pour numéroter les mises à jour de votre assembly. Chaque assembly est associé à un numéro de version en quatre parties. De gauche à droite, les parties principale, secondaire, de build et de révision sont séparées par des points. Modifiez le numéro principal ou secondaire d’un assembly pour une version qui n’est pas compatible avec les versions antérieures. Modifiez uniquement les composants de build et de révision pour les modifications à compatibilité descendante de l’assembly. Par exemple, un développeur peut adopter une méthode de numérotation dans laquelle tout 1.0.0. \* les numéros de version font référence aux versions de mise à jour de la version de l’assembly 1.0.0.0.

 

 
