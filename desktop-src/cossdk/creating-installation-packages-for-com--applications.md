---
description: Création de packages d’installation pour les applications COM+
ms.assetid: 3ef7b280-b521-4cd2-9906-013c9dfe16ab
title: Création de packages d’installation pour les applications COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef766c222fc887742f060fa786ac6308e3d7569ca572fde216cb8055ee67a29c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991159"
---
# <a name="creating-installation-packages-for-com-applications"></a>Création de packages d’installation pour les applications COM+

Vous pouvez utiliser l’outil d’administration Services de composants ou la bibliothèque d’administration COM+ pour créer des packages d’installation pour les applications COM+ et les proxys d’application.

COM+ génère des packages d’installation Windows Installer, qui, dans un seul fichier, contiennent tous les éléments nécessaires pour installer une application COM+ sur un autre ordinateur.

Lors de l’exportation d’une application COM+, l’outil d’administration Services de composants détermine l’ensemble des classes, des composants et des attributs de l’application, ainsi que des attributs de niveau application. À partir de ces informations, l’outil d’administration Services de composants génère un seul .msi fichier, qui contient les éléments suivants :

-   Windows tables de programme d’installation avec des informations d’inscription COM (pour plus d’informations, consultez la documentation Windows Installer).
-   Fichier. apl contenant les attributs de l’application. (Il s’agit d’un fichier interne ; le format de ce fichier n’est pas documenté.)
-   Bibliothèques de types et dll qui décrivent les interfaces implémentées par les classes de l’application COM+.

Outre le fichier .msi, l’outil d’administration Services de composants génère un fichier CAB (.cab). Ce fichier encapsule le fichier .msi, ce qui permet au développeur de déployer l’application COM+ à l’aide de Microsoft Internet Explorer.

> [!Note]  
> Lors de l’exportation d’une application COM+, l’outil d’administration Services de composants conditionne uniquement les parties COM+ standard de l’application. Il n’effectue pas de package, par exemple, les fichiers de données ou DLL dépendants. Les fichiers DLL dépendants doivent d’abord être installés sur un ordinateur avant l’installation de l’application COM+. vous pouvez également utiliser l’outil de création de Windows Installer pour ajouter ces fichiers dépendants au fichier .msi généré par l’outil d’administration Services de composants. (pour plus d’informations, consultez la documentation Windows Installer.)

 

## <a name="installing-com-applications-on-other-computers"></a>Installation d’applications COM+ sur d’autres ordinateurs

le fichier Windows Installer (.msi) généré par l’outil d’administration Services de composants peut être utilisé pour installer l’application COM+ sur un autre ordinateur. Le fichier .msi contenant une application COM+ ne peut être installé que sur les ordinateurs qui prennent en charge les services COM+. Pour obtenir des procédures détaillées sur le déploiement d’applications COM+, voir la rubrique relative à l’installation des applications COM+ dans l’aide de l’administration des services de composants.

à moins que le fichier .msi ne soit modifié à l’aide d’un outil de création de Windows Installer, les applications COM+ installées à l’aide de la Windows Installer s’affichent dans le panneau de configuration ajout/suppression de programmes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Déploiement de proxys d’application](deploying-application-proxies.md)
</dt> <dt>

[Le catalogue COM+](the-com--catalog.md)
</dt> </dl>

 

 



