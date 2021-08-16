---
description: Les assemblys côte à côte sont utilisés avec les types de manifestes et de fichiers de configuration suivants. Les manifestes et les configurations sont des fichiers XML.
ms.assetid: 8b969a8f-586c-4556-87be-92db6c61e8ce
title: Référence des fichiers manifeste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87636a8a4e5398cf9bb274d5ea8b9e7620104989322a20138a162ca45d9caf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142062"
---
# <a name="manifest-files-reference"></a>Référence des fichiers manifeste

Les assemblys côte à côte sont utilisés avec les types de manifestes et de fichiers de configuration suivants. Les manifestes et les configurations sont des fichiers XML.



| Manifeste                                                               | Description                                                                                                                                                                                                   |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Manifestes d’assembly](assembly-manifests.md)                           | Décrit les noms, les versions, les ressources et les dépendances d’assembly des assemblys côte à côte.                                                                                                               |
| [Manifestes d’application](application-manifests.md)                     | Décrit les noms et les versions des assemblys partagés côte à côte auxquels l’application doit se lier au moment de l’exécution et peut également contenir des métadonnées pour les assemblys côte à côte privés utilisés par l’application. |
| [Fichiers de configuration de l’application](application-configuration-files.md) | Redirige les versions d’assembly des dépendances d’assembly à l’aide de la [configuration par application](per-application-configuration.md).                                                                            |
| [Publisher Fichiers de configuration](publisher-configuration-files.md)     | Redirige les versions d’assembly des dépendances d’assembly sur la base de chaque assembly à l’aide d’une [configuration d’éditeur](publisher-configuration.md).                                                              |



 

Pour obtenir la liste du schéma de fichier manifeste, consultez [schéma de fichier manifeste](manifest-file-schema.md).

Pour obtenir la liste du schéma de fichier de configuration de l’application, consultez [schéma du fichier de configuration](application-configuration-file-schema.md)de l’application.

pour obtenir la liste du schéma du fichier de configuration du serveur de publication, consultez [Publisher schéma du fichier de configuration](publisher-configuration-file-schema.md).

d’autres technologies étendent le format utilisé par les manifestes de contrôle de version et de configuration Windows. Les développeurs doivent se référer à la documentation spécifique à la technologie utilisée pour obtenir des informations sur le format du manifeste. Par exemple :

-   [ClickOnce](/visualstudio/deployment/clickonce-reference?view=vs-2015)
-   [Common Language Runtime](/dotnet/standard/clr)
-   [Contrôle de compte d'utilisateur (UAC)](/previous-versions/bb756929(v=msdn.10))

 

 
