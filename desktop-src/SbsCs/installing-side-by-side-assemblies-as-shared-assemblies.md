---
description: La procédure suivante décrit comment installer des assemblys côte à côte en tant qu’assemblys partagés.
ms.assetid: 272ad1b8-9ea2-4af8-ba0d-c59f4db027e6
title: Installation d’assemblys côte à côte en tant qu’assemblys partagés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6348354b224e281135e72697aaa155ce69f4ccd23293f671d733e2bc1cd89dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127509"
---
# <a name="installing-side-by-side-assemblies-as-shared-assemblies"></a>Installation d’assemblys côte à côte en tant qu’assemblys partagés

La procédure suivante décrit comment installer des [assemblys côte à côte](about-side-by-side-assemblies-.md) en tant qu' [assemblys partagés](/windows/desktop/Msi/shared-assemblies).

**Pour installer un assembly côte à côte en tant qu’assembly partagé**

1.  Signez et créez un catalogue pour les fichiers de l’assembly.

    Les fichiers doivent être signés pour être installés en tant qu’assemblys côte à côte. Pour plus d’informations, consultez [création de fichiers et catalogues signés](creating-signed-files-and-catalogs.md).

2.  vous devez installer des assemblys côte à côte partagés en tant que composants d’un package de Windows Installer. Il peut s’agir du même package d’installation que celui utilisé pour installer ou mettre à jour votre application. Si l’assembly partagé est fourni dans le cadre de plusieurs applications, vous devez fournir un module de fusion qui peut être incorporé dans les packages d’installation de ces applications et créer un catalogue pour les fichiers de l’assembly.

    Windows Le programme d’installation 2,0 ou une version ultérieure est requis pour installer des assemblys. pour plus d’informations, consultez le kit de développement logiciel (SDK) [Windows Installer](../msi/windows-installer-portal.md) et les sections [Installation des assemblys Win32](../msi/installation-of-win32-assemblies.md).

 

 
