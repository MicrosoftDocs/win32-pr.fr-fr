---
description: Création du fichier de ressources de la langue de base
ms.assetid: 770e1f4b-5258-4b6b-afa4-5c19743daaaa
title: Création du fichier de ressources de la langue de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96d566625025c105e123e0e2edf9f4f20721274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035126"
---
# <a name="creating-the-base-language-resource-file"></a>Création du fichier de ressources de la langue de base

Les ressources pour les éléments d’interface utilisateur sont définies pour le langage de base pris en charge par l’application, par exemple l’anglais (États-Unis). Un fichier de ressources Win32 PE est un exemple de fichier. RC créé à l’aide du compilateur RC. Pour plus d’informations sur la création de fichiers. RC, consultez [à propos des fichiers de ressources](../menurc/about-resource-files.md).

Si vous utilisez un fichier. RC pour les ressources linguistiques de base, vous avez la possibilité d’utiliser un fichier de configuration de ressources pour une représentation XML des données de configuration de ressource. Pour créer ce fichier, consultez [préparation d’un fichier de configuration de ressource](preparing-a-resource-configuration-file.md).

Vous pouvez également utiliser un fichier PE non Win32 pour définir les ressources linguistiques de base. Par exemple, vous pouvez utiliser un fichier. XML ou. txt à cet effet.

> [!Note]  
> Quand vous définissez des ressources de langue de base à l’aide d’un fichier PE non Win32, vous ne pouvez pas utiliser le compilateur RC pour la définition de ressource. Au lieu de cela, vous définissez votre propre format de ressource, et votre application doit fournir ses propres fonctionnalités pour rechercher et charger les ressources requises.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Préparation des ressources](preparing-resources.md)
</dt> <dt>

[Préparation d’un fichier de configuration de ressource](preparing-a-resource-configuration-file.md)
</dt> </dl>

 

 
