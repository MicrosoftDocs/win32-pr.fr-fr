---
description: Création de packages d’installation pour les applications COM+
ms.assetid: 3ef7b280-b521-4cd2-9906-013c9dfe16ab
title: Création de packages d’installation pour les applications COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ec34852ab405d965fa1ad8f8fb5892616d1347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516177"
---
# <a name="creating-installation-packages-for-com-applications"></a>Création de packages d’installation pour les applications COM+

Vous pouvez utiliser l’outil d’administration Services de composants ou la bibliothèque d’administration COM+ pour créer des packages d’installation pour les applications COM+ et les proxys d’application.

COM+ génère des packages d’installation Windows Installer, qui, dans un seul fichier, contiennent tous les éléments nécessaires pour installer une application COM+ sur un autre ordinateur.

Lors de l’exportation d’une application COM+, l’outil d’administration Services de composants détermine l’ensemble des classes, des composants et des attributs de l’application, ainsi que des attributs de niveau application. À partir de ces informations, l’outil d’administration Services de composants génère un seul fichier. msi, qui contient les éléments suivants :

-   Windows Installer des tables avec des informations d’inscription COM (pour plus d’informations, consultez la documentation de Windows Installer).
-   Fichier. apl contenant les attributs de l’application. (Il s’agit d’un fichier interne ; le format de ce fichier n’est pas documenté.)
-   Bibliothèques de types et dll qui décrivent les interfaces implémentées par les classes de l’application COM+.

En plus du fichier. msi, l’outil d’administration Services de composants génère un fichier cabinet (. cab). Ce fichier encapsule le fichier. msi, ce qui permet au développeur de déployer l’application COM+ à l’aide de Microsoft Internet Explorer.

> [!Note]  
> Lors de l’exportation d’une application COM+, l’outil d’administration Services de composants conditionne uniquement les parties COM+ standard de l’application. Il n’effectue pas de package, par exemple, les fichiers de données ou DLL dépendants. Les fichiers DLL dépendants doivent d’abord être installés sur un ordinateur avant l’installation de l’application COM+. Vous pouvez également utiliser l’outil de création de Windows Installer pour ajouter ces fichiers dépendants au fichier. msi généré par l’outil d’administration Services de composants. (Pour plus d’informations, consultez la documentation Windows Installer.)

 

## <a name="installing-com-applications-on-other-computers"></a>Installation d’applications COM+ sur d’autres ordinateurs

Le fichier Windows Installer (. msi) généré par l’outil d’administration Services de composants peut être utilisé pour installer l’application COM+ sur un autre ordinateur. Le fichier. msi contenant une application COM+ ne peut être installé que sur les ordinateurs qui prennent en charge les services COM+. Pour obtenir des procédures détaillées sur le déploiement d’applications COM+, voir la rubrique relative à l’installation des applications COM+ dans l’aide de l’administration des services de composants.

À moins que le fichier. msi ne soit modifié à l’aide d’un outil de création de Windows Installer, les applications COM+ installées à l’aide de la Windows Installer s’affichent dans le panneau de configuration Ajout/suppression de programmes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Déploiement de proxys d’application](deploying-application-proxies.md)
</dt> <dt>

[Le catalogue COM+](the-com--catalog.md)
</dt> </dl>

 

 



