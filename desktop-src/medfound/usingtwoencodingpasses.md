---
description: l’encodage en deux passes peut être utilisé pour le débit binaire constant (CBR) et pour l’encodage VBR (variable bit rate) avec certains codecs de média Windows.
ms.assetid: eec5085c-9441-496a-8127-cf5d2686d917
title: Utilisation de l’encodage Two-Pass (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993af0015452db410b5a9f2c13233566fc17a3a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313622"
---
# <a name="using-two-pass-encoding-microsoft-media-foundation"></a>Utilisation de l’encodage Two-Pass (Microsoft Media Foundation)

l’encodage en deux passes peut être utilisé pour le débit binaire constant (CBR) et pour l’encodage VBR (variable bit rate) avec certains codecs de média Windows. Vous pouvez trouver le nombre maximal de passes d’encodage pris en charge par un codec en extrayant la propriété [MFPKEY \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md) . Aucun des codecs ne prend en charge plus de deux passes. configurez le DMO pour qu’il utilise deux passes en affectant à la propriété [ \_ PASSESUSED MFPKEY](mfpkey-passesusedproperty.md) la valeur 2.

fournissez les exemples DMO un à la fois, comme vous le feriez dans un mode à passage unique. Lorsque vous traitez les exemples d’entrée pour votre passe de prétraitement, les appels à [**IMediaObject ::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) ou [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) renverront la **\_ valeur S false** pour indiquer qu’aucune sortie n’est produite.

À la fin de la première passe (après le premier traitement de la dernière entrée), vous devez définir la propriété [MFPKEY \_ ENDOFPASS](mfpkey-endofpassproperty.md) pour informer le codec que l’entrée suivante traitée est la première entrée de la deuxième passe. Aucune valeur n’est requise pour cette propriété. vous devez donc utiliser une structure **Variant** vide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Codecs Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 
