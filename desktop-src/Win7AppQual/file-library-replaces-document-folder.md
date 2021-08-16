---
description: La bibliothèque de fichiers remplace le dossier de documents
ms.assetid: 80b97bfc-4212-4401-a4a9-d96e2f39be60
title: La bibliothèque de fichiers remplace le dossier de documents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e8d08b176ebf4b5801a73695ea03f60a38eeb5a1ca51e1d90d9119dae5fcaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329669"
---
# <a name="file-library-replaces-document-folder"></a>La bibliothèque de fichiers remplace le dossier de documents

## <a name="affected-platforms"></a>Plateformes affectées

**Clients** -Windows 7  
**serveurs** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impact sur les fonctionnalités

**Gravité** -moyenne  
**Fréquence** -élevée  











## <a name="description"></a>Description

Les bibliothèques fournissent une expérience de type dossier centralisé pour le stockage des fichiers, la recherche et l’accès à plusieurs emplacements, à la fois locaux et distants.

Les emplacements par défaut utilisés par les boîtes de dialogue de fichier courantes (par exemple, ouvrir et enregistrer) ont été modifiés depuis le dossier de documents vers la bibliothèque de documents. L’interface utilisateur est inchangée, mais l’utilisateur peut désormais afficher, parcourir et rechercher la bibliothèque à l’aide de plusieurs vues de la structure. Les fichiers sont enregistrés dans l’emplacement d’enregistrement par défaut de la bibliothèque, sauf si l’utilisateur modifie l’emplacement d’enregistrement par défaut ou choisit un autre dossier.

Les développeurs peuvent créer leurs propres bibliothèques ou ajouter des emplacements à des bibliothèques existantes à l’aide de l’interface IShellLibrary. Les utilisateurs peuvent rechercher des bibliothèques à l’aide du système de dossiers connu (par exemple, FOLDERID \_ DocumentsLibrary).

## <a name="manifestation-of-impact"></a>Manifeste de l’impact

La bibliothèque est elle-même un fichier et non un dossier. Par conséquent, les manipulations de chemin d’accès peuvent entraîner des erreurs en raison de la tentative de concaténation des fichiers par l’application pour les fichiers.

## <a name="solution"></a>Solution

Lorsque vous utilisez IFileDialog, vous devez utiliser la méthode GetResult au lieu de la combinaison de GetFolder et GetFilename, comme vous le feriez dans les versions précédentes du système d’exploitation. Utilisez les API de l’interpréteur de commandes dans la mesure du possible pour interagir avec et manipuler des éléments dans l’espace de noms Shell (par exemple, IShellItem).

## <a name="leveraging-feature-capabilities"></a>Exploitation des fonctionnalités de fonctionnalités

Si vous souhaitez créer vos propres bibliothèques ou ajouter des emplacements à des bibliothèques existantes, vous devez utiliser l’API IShellLibrary. Les bibliothèques sont elles-mêmes des dossiers Shell, ce qui vous permet de les énumérer comme n’importe quel autre dossier shell.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilité, performances, fiabilité et test d’utilisabilité

À l’aide de la boîte de dialogue fichier commun, vous pouvez vous assurer que les utilisateurs peuvent enregistrer directement dans leurs bibliothèques.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   **bibliothèques de Windows :**https://msdn.microsoft.com/library/dd758096(VS.85).aspx
-   **Maintien de la synchronisation avec une bibliothèque :**https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync

 

 



