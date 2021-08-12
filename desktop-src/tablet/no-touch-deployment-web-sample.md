---
description: Cet exemple montre comment déployer une application Tablet PC gérée sur le Web à l’aide d’un déploiement sans toucher.
ms.assetid: d226bd67-e20d-431b-b0c3-9361b00a9340
title: Exemple de déploiement Web No-Touch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d8fb9989785dc081022c2e76d8fade6d48bf521b3f27449ff5aac963706f356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449650"
---
# <a name="no-touch-deployment-web-sample"></a>Exemple de déploiement Web No-Touch

Cet exemple montre comment déployer une application Tablet PC gérée sur le Web à l’aide d’un déploiement sans toucher. Vous devez être familiarisé avec les concepts abordés dans [le déploiement sans toucher dans le .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp). Microsoft Internet Information Services (IIS) doit être installé sur votre ordinateur pour exécuter cet exemple.

## <a name="overview"></a>Vue d’ensemble

Avec le déploiement sans toucher, les applications de formulaires PCWindows-applications de bureau générées à l’aide des classes du système. Windows. l’espace de noms forms de microsoft .NET Framework et microsoft Windows XP Tablet PC Edition Kit de développement 1,7-peuvent être téléchargés, installés et exécutés directement sur les ordinateurs des utilisateurs sans aucune modification du registre ou des composants du système partagé.

Cet exemple utilise le projet d’origine pour l' [exemple de formulaire de déclaration automatique](auto-claims-form-sample.md), les revendications automatiques et fournit un projet de programme d’installation, \_ NoTouchWebe automatiquement. Une fois compilé et exécuté, le projet d’installation crée une nouvelle racine virtuelle, également appelée \_ NoTouchWeb. Le programme d’installation copie un fichier, default.htm, qui comprend un lien vers l’assembly AutoClaims.exe. Pour lancer l’application cliente enrichie, accédez à la racine virtuelle avec Microsoft Internet Explorer, puis cliquez sur le lien dans la page default.htm.

> [!Note]  
> Vous devez accéder à la racine virtuelle par le biais d’IIS (par exemple, https://localhost/AutoClaims\_NoTouchWeb/default.htm) et pas directement via le système de fichiers pour que l’application fonctionne dans le domaine d’application Internet Explorer.

 


```C++
<html>
    <head>
        <title>AutoClaims (No Touch Web)</title>
      </head>
      <body>
          <a href="AutoClaims.exe">Launch AutoClaims Sample</a>
      </body>
</html>
```



## <a name="no-touch-deployment-requirements"></a>Conditions requises pour le déploiement de No-Touch

Tous les assemblys dépendants doivent se trouver dans le chemin de recherche de l’assembly ou la racine du répertoire virtuel du site Web. Le projet de déploiement NoTouchWeb de la récupération d' \_ origine installe l’assembly et la page de référence, default.htm, dans la même racine virtuelle (NoTouchWeb de récupération \_ ).

> [!Note]  
> Les exemples Web compilés ne sont pas installés par l’option d’installation par défaut pour le kit de développement logiciel (SDK). Vous devez effectuer une installation personnalisée et sélectionner la sous-option « exemples Web précompilés » pour les installer.

 

Pour plus d’informations sur l’utilisation de l’encre sur le Web, voir [Ink on the Web](ink-on-the-web.md).

 

 