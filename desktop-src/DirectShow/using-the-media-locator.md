---
description: Utilisation du localisateur de média
ms.assetid: 07840a37-7065-41e8-aee5-855c9f89fb77
title: Utilisation du localisateur de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce934b06d92c0bec66d9260a485516d3acaf5a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857374"
---
# <a name="using-the-media-locator"></a>Utilisation du localisateur de média

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Le localisateur de média est un objet d’assistance qui vérifie les noms de fichiers et recherche les fichiers manquants dans les répertoires locaux ou réseau. Le détecteur de média conserve un cache de chemins d’accès aux répertoires dans lesquels il a trouvé des fichiers dans les recherches précédentes. Pour localiser un fichier, il effectue une recherche dans les répertoires de son cache. En cas d’échec, le détecteur de média peut afficher une boîte de dialogue Ouvrir un fichier pour permettre à l’utilisateur de localiser un fichier manuellement. En supposant que l’utilisateur trouve le fichier, le localisateur de média ajoute le nouveau répertoire à son cache. Le localisateur de média expose l’interface [**IMediaLocator**](imedialocator.md) .

En règle générale, votre application ne crée pas directement une instance du localisateur de média. Au lieu de cela, la chronologie et le moteur de rendu fournissent les méthodes suivantes pour valider les noms de fichiers à l’aide du détecteur de média.

-   Pour valider des noms de fichiers dans la chronologie, appelez [**IAMTimeline :: ValidateSourceNames**](iamtimeline-validatesourcenames.md). Si vous le souhaitez, cette méthode met également à jour les objets sources avec les noms de fichiers corrects.
-   Pour valider des noms de fichiers lors du rendu du projet, appelez [**IRenderEngine :: SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md).

Les deux méthodes prennent des indicateurs qui contrôlent le comportement du localisateur de média. Par exemple, vous pouvez limiter la recherche aux répertoires locaux.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des sources](working-with-sources.md)
</dt> </dl>

 

 



