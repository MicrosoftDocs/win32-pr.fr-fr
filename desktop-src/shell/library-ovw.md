---
description: Windows 7 présente des bibliothèques qui fournissent aux utilisateurs une vue unique et cohérente de leurs fichiers, même lorsque ces fichiers sont stockés dans des emplacements différents.
title: Windows Bibliotheque
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 19DA68B2-FCB6-443d-A3CD-0BF2F429B149
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 18134654d477caaca250c114d79659d4cc617b7955ee32d527a2f8f001bbacd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049312"
---
# <a name="windows-libraries"></a>Windows Bibliotheque

Windows 7 présente des bibliothèques qui fournissent aux utilisateurs une vue unique et cohérente de leurs fichiers, même lorsque ces fichiers sont stockés dans des emplacements différents. Les bibliothèques peuvent être configurées et organisées par un utilisateur et une bibliothèque peut contenir des dossiers qui se trouvent sur l’ordinateur de l’utilisateur et également des dossiers qui ont été partagés sur un réseau. Les bibliothèques présentent une vue plus simple du système de stockage sous-jacent car, pour l’utilisateur, les fichiers et les dossiers d’une bibliothèque s’affichent dans une seule vue, quel que soit l’emplacement où ils sont stockés physiquement.

les développeurs qui écrivent de nouveaux programmes dans Windows 7 sont encouragés à utiliser des bibliothèques comme moyen permettant aux utilisateurs d’interagir avec les fichiers utilisés par le programme. l’utilisation de bibliothèques dans votre programme offre aux utilisateurs une expérience plus propre, plus simple et plus cohérente dans Windows 7.

Les développeurs doivent également examiner leurs programmes existants et les mettre à jour si nécessaire, pour travailler avec des bibliothèques. Étant donné que les bibliothèques ne font pas partie du système de fichiers, les API basées sur le système de fichiers n’ont pas accès aux bibliothèques que l’utilisateur a pu configurer.

Les programmes qui permettent actuellement aux utilisateurs de stocker leur contenu dans différents dossiers ou sur des ordinateurs différents tireront le meilleur parti lorsqu’ils ajoutent la prise en charge de bibliothèque. Les bibliothèques simplifient la gestion du contenu dans divers emplacements de stockage pour le développeur et l’utilisateur.

Ce guide décrit en détail les bibliothèques, la façon dont les programmes peuvent être utilisés pour travailler avec les bibliothèques, ainsi que certains des moyens dont dispose un programme pour améliorer l’expérience de l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des bibliothèques](library-leverage-to-manage-folders.md)
</dt> <dt>

[Utilisation de bibliothèques dans votre programme](library-be-library-aware.md)
</dt> <dt>

[**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Liens de Shell](./links.md)
</dt> <dt>

[Dossiers connus](known-folders.md)
</dt> <dt>

[Schéma de description de la bibliothèque](library-schema-entry.md)
</dt> </dl>

 

 
