---
description: utilisation du profil avancé Windows Media Video 9
ms.assetid: 2abc0efc-dd11-4921-897c-209a26f8ba1d
title: utilisation du profil avancé Windows Media Video 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692243117cde3b4b5f1179c5f7324d25842191b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313633"
---
# <a name="using-the-windows-media-video-9-advanced-profile"></a>utilisation du profil avancé Windows Media Video 9

les procédures vidéo de base décrites dans la section [utilisation de vidéos](workingwithvideo.md) s’appliquent également directement au profil avancé Windows Media Video 9. Aucune procédure spéciale n’est requise.

le profil avancé Windows Media Video 9 est associé aux identificateurs de classe clsid \_ CWMV9EncMediaObject et clsid \_ CWMVDecMediaObject. La valeur FOURCC pour les types de média utilisant ce codec est « WVC1 ».

le profil avancé Windows Media Video 9 prend en charge tous les modes d’encodage courants, ainsi que l’encodage entrelacé, le codage mixte entrelacé et progressif, les résolutions qui diffèrent de l’affichage et les fonctionnalités de réduction de plage. Une autre fonctionnalité est la possibilité de stocker des métadonnées de séquence et de frame dans le flux de bits. auparavant, cela nécessitait l’utilisation de l’API ASF et des extensions d’unité de données.

les propriétés suivantes du profil avancé Windows Media Video 9, qui peuvent être contrôlées à l’aide des paramètres du registre, n’ont pas de chaînes **IPropertyBag** ou **IPropertyStore** correspondantes :

-   Option DQuant.
-   Force DQuant.
-   Chevauchement forcé.
-   Méthode de coût du vecteur de mouvement.

## <a name="achieving-optimal-visual-quality"></a>Obtenir une qualité visuelle optimale

pour la plupart des données vidéo, pour obtenir une qualité visuelle optimale à l’aide du profil avancé Windows Media Video 9, vous pouvez affecter la valeur 1 à la propriété [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) .

## <a name="about-the-previous-windows-media-video-9-advanced-profile-codecs"></a>à propos des codecs de profil avancé Windows Media Video 9 précédents

la version actuelle du codec de profil avancé Windows Media Video 9 est basée sur la norme SMPTE (the Motion image and Television Engineers) standard pour le profil avancé VC-1 (smpte 421M). ce codec remplace le codec antérieur de Windows également appelé codec de profil avancé Windows Media Video 9 qui a été identifié par le code FOURCC « WMVA ». La version précédente du codec VC-1 a été implémentée avant la finalisation de la norme de profil avancé VC-1 et n’est plus prise en charge.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la vidéo](workingwithvideo.md)
</dt> 
<dt>

[utilisation de la Paramètres avancée du Codec du profil avancé Windows Media Video 9](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)
</dt> </dl>

 

 



