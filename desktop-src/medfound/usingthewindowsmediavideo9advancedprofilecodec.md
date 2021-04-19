---
description: Utilisation du profil avancé Windows Media Video 9
ms.assetid: 2abc0efc-dd11-4921-897c-209a26f8ba1d
title: Utilisation du profil avancé Windows Media Video 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692243117cde3b4b5f1179c5f7324d25842191b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522879"
---
# <a name="using-the-windows-media-video-9-advanced-profile"></a>Utilisation du profil avancé Windows Media Video 9

Les procédures vidéo de base décrites dans la section [utilisation de vidéos](workingwithvideo.md) s’appliquent également directement au profil avancé Windows Media Video 9. Aucune procédure spéciale n’est requise.

Le profil avancé Windows Media Video 9 est associé aux identificateurs de classe CLSID \_ CWMV9EncMediaObject et CLSID \_ CWMVDecMediaObject. La valeur FOURCC pour les types de média utilisant ce codec est « WVC1 ».

Le profil avancé Windows Media Video 9 prend en charge tous les modes d’encodage courants, ainsi que l’encodage entrelacé, le codage mixte entrelacé et progressif, les résolutions qui diffèrent de l’affichage et les fonctionnalités de réduction de plage. Une autre fonctionnalité est la possibilité de stocker des métadonnées de séquence et de frame dans le flux de bits. auparavant, cela nécessitait l’utilisation de l’API ASF et des extensions d’unité de données.

Les propriétés suivantes du profil avancé Windows Media Video 9, qui peuvent être contrôlées à l’aide des paramètres du Registre, n’ont pas de chaînes **IPropertyBag** ou **IPropertyStore** correspondantes :

-   Option DQuant.
-   Force DQuant.
-   Chevauchement forcé.
-   Méthode de coût du vecteur de mouvement.

## <a name="achieving-optimal-visual-quality"></a>Obtenir une qualité visuelle optimale

Pour la plupart des données vidéo, pour obtenir une qualité visuelle optimale à l’aide du profil avancé Windows Media Video 9, vous pouvez affecter la valeur 1 à la propriété [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) .

## <a name="about-the-previous-windows-media-video-9-advanced-profile-codecs"></a>À propos des codecs de profil avancé Windows Media Video 9 précédents

La version actuelle du codec de profil avancé Windows Media Video 9 est basée sur la norme SMPTE (The Motion image and Television Engineers) standard pour le profil avancé VC-1 (SMPTE 421M). Ce codec remplace le codec antérieur de Windows, également appelé codec de profil avancé Windows Media Video 9, identifié par le code FOURCC « WMVA ». La version précédente du codec VC-1 a été implémentée avant la finalisation de la norme de profil avancé VC-1 et n’est plus prise en charge.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la vidéo](workingwithvideo.md)
</dt> 
<dt>

[Utilisation des paramètres avancés du codec de profil avancé Windows Media Video 9](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)
</dt> </dl>

 

 



