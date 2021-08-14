---
title: Encodage Two-Pass
description: Encodage Two-Pass
ms.assetid: 354cd0a5-9a64-4171-9604-694e60b382ad
keywords:
- Windows Media Format SDK, encodage en deux passes
- Windows Media Format SDK, encodage 2 passe
- codecs, encodage en deux passes
- codecs, encodage à 2 passes
- encodage en deux passes, à propos de
- 2-encodage Pass, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cd769049b5fa3869c844e00d9ee14cfae596b197d06d414b04a544d831bbeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845337"
---
# <a name="two-pass-encoding"></a>Encodage Two-Pass

l’encodage en deux passes est une méthode d’encodage disponible avec certains codecs, comme le codec Windows Media Video 9. Lorsque vous utilisez l’encodage en deux passes, le codec traite tous les exemples du flux à deux reprises. Lors du premier passage, le codec rassemble des informations sur le contenu du flux. Lors de la deuxième passe, le codec utilise les informations collectées lors du premier passage pour optimiser le processus d’encodage du flux.

Dans le mode d’encodage à taux binaire constant, les fichiers qui sont codés en deux passes sont généralement plus efficaces que les fichiers encodés en une seule passe. Le VBR basé sur la qualité, qui est une passe, produit une qualité plus cohérente que le VBR basé sur la vitesse du bit, ce qui correspond à deux passes.

Vous ne pouvez pas utiliser un encodage en deux passes sur des flux Live.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités du codec**](codec-features.md)
</dt> <dt>

[**Utilisation de l’encodage Two-Pass**](using-two-pass-encoding.md)
</dt> </dl>

 

 




