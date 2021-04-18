---
title: Vidéo (Windows Media Player SDK)
description: Vidéo
ms.assetid: 3c654494-19b5-401e-bed8-02f7cc7d7f4e
keywords:
- Windows Media Player Mobile Skins, vidéo
- apparences, vidéo
- référence pour les enveloppes, vidéo
- vidéo dans les apparences, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3d505acec3f6917c7ed3d182c656ff5e9f29f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106512767"
---
# <a name="video-windows-media-player-sdk"></a>Vidéo (Windows Media Player SDK)

Un affichage vidéo permet à l’utilisateur d’afficher des fichiers vidéo numériques. La zone d’affichage vidéo est visible uniquement lorsque la vidéo est en mode de diffusion ou en pause. Lorsque vous concevez votre apparence, vous souhaiterez réserver de l’espace dans l’image d’arrière-plan pour contenir l’affichage vidéo. Si vous ne le faites pas, l’affichage vidéo peut se superposer sur n’importe quelle illustration visible, comme le fichier d’arrière-plan, les boutons et les trackbars, ce qui empêchera l’utilisateur d’utiliser les contrôles sur votre apparence.

La section vidéo du fichier de définition d’apparence doit commencer par cette ligne :


```C++
[ Video ]

```



Vous devez ensuite ajouter une ligne qui spécifie l’emplacement et la taille de la zone d’affichage de la vidéo dans votre apparence.


```C++
0,38,240,172

```



Vous pouvez utiliser le modèle suivant pour la section vidéo de votre fichier de définition d’apparence :


```C++
//  <Location>
//  ----------

```



Les sections suivantes fournissent des informations supplémentaires.

-   [Emplacement de la vidéo](video-location.md)
-   [Source de l’image vidéo](video-image-source.md)
-   [Taille de la vidéo](video-size.md)
-   [Exemple de section vidéo](sample-video-section.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence d’apparence**](skin-reference.md)
</dt> </dl>

 

 




