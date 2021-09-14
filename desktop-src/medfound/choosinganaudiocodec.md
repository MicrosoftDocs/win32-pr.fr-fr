---
description: Choix d’un codec audio
ms.assetid: 37f3582c-c718-42ae-b887-d7d31ee853e9
title: Choix d’un codec audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b16dc0c6e65356f7d7e74b85b0671c2b41369
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127236364"
---
# <a name="choosing-an-audio-codec-microsoft-media-foundation"></a>Choix d’un codec audio (Microsoft Media Foundation)

l' [**encodeur Windows Media Audio**](windowsmediaaudioencoder.md) fournit trois catégories d’encodage Audio, comme indiqué dans le tableau suivant.



| Category                         | Objectif                                                    |
|----------------------------------|------------------------------------------------------------|
| Windows Media audio standard     | Compression de l’audio à usage général.                      |
| Windows Professional multimédia audio | Compression des données audio multicanaux et haute définition.       |
| Windows Média audio sans perte     | Compression de l’audio sans perdre les données d’origine. |



 

La catégorie standard fournit un codage audio à usage général adapté à un large éventail de scénarios de lecture. Par exemple, il peut compresser l’audio sur un faible taux de diffusion en continu sur un réseau avec une bande passante limitée, ou pour le rendu sur des appareils mobiles. À l’autre extrémité de l’échelle, elle peut produire du contenu audio compressé pour une lecture de haute qualité. L’accent est mis sur la musique des algorithmes d’encodage standard, mais ils conviennent également à d’autres contenus audio complexes. La catégorie standard doit être votre valeur par défaut pour le contenu audio. les catégories Professional et sans perte doivent être utilisées pour répondre à des besoins spécifiques.

un encodeur distinct, le [**Windows Media Voice encoder**](windowsmediaaudiovoiceencoder.md), assure la compression de la parole.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’audio](workingwithaudio.md)
</dt> </dl>

 

 



