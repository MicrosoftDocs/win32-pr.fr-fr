---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 0D537FD1-AD5C-43CB-989F-4B5B7C0A1208
title: A (applications isolées et assemblys côte à côte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41a925d83cf602f5d23c7d043102927748da14a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518668"
---
# <a name="a-isolated-applications-and-side-by-side-assemblies"></a>A (applications isolées et assemblys côte à côte)

A B C [D](d-sbscs-gly.md) e F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z

<dl> <dt>

<span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**contexte d’activation**
</dt> <dd>

Structure de données en mémoire. Chaque section de cette structure contient des métadonnées pour les fonctions d’API de prise en charge côte à côte. Par exemple, une section peut contenir des données de redirection de DLL, qui sont utilisées par le chargeur de DLL, et une autre peut comporter des données de serveur COM. Ces données peuvent être utilisées pour rediriger le chargement d’une DLL vers une version spécifique, la création d’un objet COM ou la création d’une fenêtre avec une version la plus compatible pour l’application.

</dd> <dt>

<span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**configuration de l’application**
</dt> <dd>

Noms et versions des assemblys côte à côte requis pour exécuter une application. Quand une application est déployée avec un manifeste, les dépendances sur des versions spécifiques des assemblys côte à côte partagés sont définies explicitement. Par défaut, la version de l’assembly spécifiée dans le manifeste est la version utilisée lors de l’activation. La configuration globale de l’application spécifie la configuration de toutes les applications sur le système. La configuration par application peut remplacer la configuration d’application globale pour chaque application.

</dd> <dt>

<span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**manifeste de configuration de l’application**
</dt> <dd>

Fichier qui spécifie les assemblys côte à côte à utiliser par une application totalement ou partiellement isolée. Les fichiers manifeste de la configuration de l’application sont installés dans le même dossier que le fichier exécutable de l’application.

</dd> <dt>

<span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**manifeste d’application**
</dt> <dd>

Fichier qui décrit une application isolée. Il spécifie les informations requises pour exécuter l’application, y compris les dépendances sur les assemblys privés, les versions spécifiques des assemblys partagés et les métadonnées pour les assemblys privés. Le nom d’un fichier manifeste d’application est le nom de l’exécutable de l’application suivi de l’extension. manifest. Par exemple, pour MySampleApp.exe, le fichier manifeste est MySampleApp.exe. manifest.

</dd> <dt>

<span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**chargeur**
</dt> <dd>

Unité fondamentale pour l’affectation de noms, la liaison, le contrôle de version, le déploiement ou la configuration d’un bloc de code de programmation. Ces assemblys de code peuvent être placés dans des dll ou des assemblys COM. Les applications avec des fonctionnalités communes peuvent exécuter des blocs partagés de code de programmation, appelés modules ou assemblys de code. L’infrastructure pour le partage sécurisé des assemblys est appelée partage d’assembly côte à côte.

</dd> <dt>

<span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**manifeste d’assembly**
</dt> <dd>

Description d’un assembly côte à côte. Il spécifie le nom, la version, les fichiers, les ressources de l’assembly, les données de liaison pour les éléments de l’assembly et les dépendances sur d’autres assemblys côte à côte. Un fichier manifeste d’assembly peut avoir n’importe quel nom de fichier valide, à condition qu’il soit suivi par l’extension. manifest.

</dd> </dl>

 

 



