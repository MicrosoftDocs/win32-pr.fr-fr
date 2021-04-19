---
description: Paramètres du décodeur pour Windows Media Center Edition
ms.assetid: 019b063f-f215-44d8-a916-3125bee6af93
title: Paramètres du décodeur pour Windows Media Center Edition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f66b5107fa0316f6ce2547e1f5f066165ed598
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106527041"
---
# <a name="decoder-settings-for-windows-media-center-edition"></a>Paramètres du décodeur pour Windows Media Center Edition

Windows XP Media Center Edition 2005 et versions ultérieures utilise l’interface [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) pour configurer le filtre de décodeur audio pour la télévision et la lecture de DVD. Les propriétés suivantes sont prises en charge.



| Guid de propriété                   | Description                                      |
|---------------------------------|--------------------------------------------------|
| \_format de \_ sortie \_ audio CODECAPI | Configure le format de sortie audio. Consultez la section Notes. |



 

## <a name="remarks"></a>Notes

La valeur de la \_ \_ propriété format de sortie audio CODECAPI \_ est une représentation sous forme de chaîne d’un GUID, stockée en tant que valeur **BSTR** . Les GUID suivants sont définis.



| GUID                                                        | Description                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_format de \_ sortie audio CODECAPI \_ \_ PCM \_ stéréo \_ MATRIXENCODED | Le filtre audio logiciel doit effectuer le décodage logiciel et générer un flux audio stéréo, avec la matrice audio multicanal encodée sur les deux canaux.                                                   |
| \_format de \_ sortie audio CODECAPI \_ \_ PCM \_ stéréo                | Le filtre audio logiciel doit effectuer le décodage logiciel et générer un flux audio stéréo.                                                                                                                   |
| \_PCM CODECAPI \_ format de sortie audio \_ \_ SPDIF \_                 | Le filtre audio logiciel doit effectuer le décodage logiciel audio, même si la sortie physique du PC peut être une interface numérique, telle que S/PDIF.                                                      |
| \_ \_ \_ \_ flux binaire SPDIF de format de sortie audio CODECAPI \_           | Le filtre audio logiciel ne doit pas effectuer de décodage audio logiciel, mais il doit transmettre le flux de données audio numérique brut pour le traitement externe par un appareil connecté avec une liaison audio numérique, comme S/PDIF. |
| \_ \_ \_ \_ casque PCM format de sortie audio CODECAPI \_            | Le filtre audio logiciel doit effectuer le décodage logiciel audio et doit appliquer un traitement propriétaire pour optimiser le casque. La prise en charge de ce paramètre est facultative.                                     |



 

> [!Note]  
> L’interface **ICodecAPI** stocke les propriétés de codec sous forme de paires clé/valeur, où la clé est un GUID et la valeur est un type **Variant** .

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement d’encodeur et de décodeur](encoder-and-decoder-development.md)
</dt> </dl>

 

 



