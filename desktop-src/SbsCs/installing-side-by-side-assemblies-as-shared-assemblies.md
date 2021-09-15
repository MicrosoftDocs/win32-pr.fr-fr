---
description: La procédure suivante décrit comment installer des assemblys côte à côte en tant qu’assemblys partagés.
ms.assetid: 272ad1b8-9ea2-4af8-ba0d-c59f4db027e6
title: Installation d’assemblys côte à côte en tant qu’assemblys partagés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4e796fb371a299f508945371fea926c5d56a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237966"
---
# <a name="installing-side-by-side-assemblies-as-shared-assemblies"></a>Installation d’assemblys côte à côte en tant qu’assemblys partagés

La procédure suivante décrit comment installer des [assemblys côte à côte](about-side-by-side-assemblies-.md) en tant qu' [assemblys partagés](/windows/desktop/Msi/shared-assemblies).

**Pour installer un assembly côte à côte en tant qu’assembly partagé**

1.  Signez et créez un catalogue pour les fichiers de l’assembly.

    Les fichiers doivent être signés pour être installés en tant qu’assemblys côte à côte. Pour plus d’informations, consultez [création de fichiers et catalogues signés](creating-signed-files-and-catalogs.md).

2.  vous devez installer des assemblys côte à côte partagés en tant que composants d’un package de Windows Installer. Il peut s’agir du même package d’installation que celui utilisé pour installer ou mettre à jour votre application. Si l’assembly partagé est fourni dans le cadre de plusieurs applications, vous devez fournir un module de fusion qui peut être incorporé dans les packages d’installation de ces applications et créer un catalogue pour les fichiers de l’assembly.

    Windows Le programme d’installation 2,0 ou une version ultérieure est requis pour installer des assemblys. pour plus d’informations, consultez le kit de développement logiciel (SDK) [Windows Installer](../msi/windows-installer-portal.md) et les sections [Installation des assemblys Win32](../msi/installation-of-win32-assemblies.md).

 

 
