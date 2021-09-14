---
title: Audio Low-Delay
description: Audio Low-Delay
ms.assetid: f93819eb-f38a-45a0-aa1b-4e677e33daf8
keywords:
- Windows Media Format SDK, audio à faible délai
- Windows Media Format SDK, prise en charge audio
- codecs, audio à faible délai
- codecs, prise en charge audio
- audio à faible retards
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8cedd3a6bb54942f5a517c7133e993cf5b11cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234612"
---
# <a name="low-delay-audio"></a>Audio Low-Delay

L’audio à faible délai est un mode d’encodage qui produit un contenu audio compressé avec un paramètre de fenêtre de mémoire tampon plus petit que les autres modes. Cela est utile pour les flux qui doivent être basculés rapidement pendant la lecture. Le scénario classique de cette fonctionnalité est une présentation diffusée en continu qui comprend la possibilité de changer arbitrairement le contenu, par exemple en modifiant le canal d’une télévision.

Lorsque vous utilisez un format audio à faible retards, la latence du changement de contenu est considérablement réduite par rapport à d’autres formats audio. La latence est également réduite pour les diffusions en direct lorsque vous utilisez des formats à faible délai.

cette fonctionnalité est prise en charge par les codecs Professional Windows Media Audio 9,1 et Windows Media Audio 9,1. Les formats à faible délai sont disponibles uniquement pour l’encodage à vitesse binaire constante (à la fois en un passage et en deux passes).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités du codec**](codec-features.md)
</dt> </dl>

 

 




