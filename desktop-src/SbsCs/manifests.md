---
description: Les manifestes sont des fichiers XML qui accompagnent et décrivent des assemblys côte à côte ou des applications isolées.
ms.assetid: 53c4c2e6-fff9-4506-b7e0-d091d2ec9883
title: Manifestes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2536e518f39791b400b9e99002b9575f4428d64d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011351"
---
# <a name="manifests"></a>Manifestes

Les manifestes sont des fichiers XML qui accompagnent et décrivent des assemblys côte à côte ou des applications isolées. Manifeste l’identification de l’assembly de façon unique par le biais de l’élément **assemblyIdentity** de l’assembly. Ils contiennent des informations utilisées pour la liaison et l’activation, telles que les classes COM, les interfaces et les bibliothèques de types, qui ont traditionnellement été stockées dans le registre. les manifestes spécifient également les fichiers qui composent l’assembly et peuvent inclure des classes Windows si l’auteur de l’assembly souhaite qu’elles soient gérées par version. Les assemblys côte à côte ne sont pas inscrits sur le système, mais sont disponibles pour les applications et autres assemblys sur le système qui spécifient des dépendances dans les fichiers manifestes.

Les fichiers manifeste permettent aux administrateurs et aux applications de gérer les versions d’assembly côte à côte après le déploiement. Un manifeste doit être associé à chaque assembly côte à côte. l’installation de Windows XP installe les [assemblys côte à côte Microsoft pris en charge](supported-microsoft-side-by-side-assemblies.md) avec leurs manifestes. Si vous développez vos propres assemblys côte à côte, vous devez également installer des fichiers manifeste. Pour plus d’informations, consultez [installation des assemblys côte à côte](installing-side-by-side-assemblies.md) et [référence des fichiers manifeste](manifest-files-reference.md).

Les manifestes et les fichiers de configuration ne sont pas localisés.

Les types de manifestes suivants sont utilisés avec les assemblys côte à côte :

-   Les [manifestes d’assembly](assembly-manifests.md) décrivent des assemblys côte à côte. Ils sont utilisés pour gérer les noms, les versions, les ressources et les assemblys dépendants des assemblys côte à côte. Les manifestes des [assemblys partagés](/windows/desktop/Msi/shared-assemblies) sont stockés dans le dossier WinSxS du système. Les manifestes d’assembly privés sont stockés en tant que ressource dans la DLL ou dans le dossier de l’application
-   Les [manifestes d’application](application-manifests.md) décrivent les [applications isolées](isolated-applications.md). Ils sont utilisés pour gérer les noms et les versions des assemblys partagés côte à côte auxquels l’application doit se lier au moment de l’exécution. Les manifestes d’application sont copiés dans le même dossier que le fichier exécutable de l’application ou inclus en tant que ressource dans le fichier exécutable de l’application.
-   Les [fichiers de configuration](application-configuration-files.md)de l’application sont des manifestes utilisés pour remplacer et rediriger les versions des assemblys dépendants utilisés par les applications et les assemblys côte à côte.
-   [Publisher fichiers de Configuration](publisher-configuration-files.md), sont des manifestes utilisés pour rediriger la version d’un assembly côte à côte vers une autre version compatible. La version vers laquelle l’assembly est redirigé doit avoir les mêmes valeurs majeures. minor que la version d’origine.

 

 
