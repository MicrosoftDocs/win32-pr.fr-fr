---
title: Encodage à vitesse de transmission variable (VBR)
description: Encodage à vitesse de transmission variable (VBR)
ms.assetid: d3fe0cc6-64d7-44ce-8bb4-dd2eed021345
keywords:
- Windows Media Format SDK, VBR Encoding
- Windows Media Format SDK, VBR (variable bit rate)
- Windows Media Format SDK, codage VBR basé sur la qualité
- Windows Media Format SDK, encodage VBR non restreint
- Windows Media Format SDK, encodage VBR restreint
- codecs, encodage VBR
- codecs, débit binaire variable (VBR)
- codecs, encodage VBR basé sur la qualité
- codecs, encodage VBR non restreint
- codecs, encodage VBR restreint
- Vitesse de transmission variable (VBR), à propos de
- VBR (vitesse de transmission variable), à propos de
- codage VBR basé sur la qualité, à propos de
- encodage VBR non restreint, à propos de
- encodage VBR restreint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b24a32b693cc4801f95695cc2d6e5f9ffa400c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512469"
---
# <a name="variable-bit-rate-vbr-encoding"></a>Encodage à vitesse de transmission variable (VBR)

L’encodage VBR (variable binaire rate) est une alternative à l’encodage à débit binaire constant (CBR) et est pris en charge par certains codecs. Lorsque l’encodage CBR s’efforce de maintenir la vitesse de transmission du média encodé, le VBR s’efforce d’obtenir la meilleure qualité possible du média encodé.

La qualité du contenu encodé est déterminée par la quantité de données perdues quand le contenu est compressé et décompressé. De nombreux facteurs affectent la perte de données dans le processus de compression mais, en général, plus les données d'origine sont complexes, plus le taux de compression est élevé et plus la perte de détails est importante dans le processus de compression.

Il existe trois types d’encodage VBR : basés sur la qualité, sans contrainte et contraint.

## <a name="quality-based-vbr-encoding"></a>Codage VBR basé sur la qualité

Le premier type d’encodage VBR est basé sur la qualité, qui utilise une passe d’encodage. L’encodage VBR basé sur la qualité vous permet de spécifier un niveau de qualité pour un flux multimédia numérique au lieu d’une vitesse de transmission. Le codec encodera ensuite le contenu afin que tous les échantillons soient de qualité comparable.

Le principal avantage de l’encodage VBR basé sur la qualité est que la qualité est cohérente dans un fichier et d’un fichier à l’autre. Par exemple, vous pouvez écrire un programme pour copier des chansons depuis des fichiers CD vers des fichiers ASF sur un ordinateur. Dans ce cas, la qualité cohérente est probablement plus importante pour l’expérience de l’utilisateur final que la cohérence de la taille des fichiers. L’utilisation de l’encodage VBR basé sur la qualité garantit que toutes les chansons copiées sont de la même qualité.

L’inconvénient de l’encodage VBR basé sur la qualité est qu’il n’existe aucun moyen de connaître les exigences de taille ou de bande passante des médias encodés avant l’encodage. Cela peut rendre les fichiers codés en fonction du VBR de qualité inappropriés pour les cas où la mémoire ou la bande passante est limitée, comme les lecteurs multimédias portables ou les connexions Internet à faible bande passante.

En général, l’encodage VBR basé sur la qualité est bien adapté à la lecture locale ou aux connexions réseau à bande passante élevée. Dans ce cas, la qualité cohérente offre une meilleure expérience utilisateur.

## <a name="unconstrained-vbr-encoding"></a>Encodage VBR sans contrainte

L’encodage VBR sans contrainte utilise deux passes d’encodage. Lorsque vous utilisez l’encodage VBR non restreint, vous spécifiez une vitesse de transmission pour le flux, comme vous le feriez avec l’encodage CBR. Toutefois, le codec utilise cette valeur uniquement comme la vitesse de transmission moyenne pour le flux et l’encodage afin que la qualité soit aussi élevée que possible tout en conservant la moyenne. La vitesse de transmission réelle à n’importe quel point dans le flux encodé peut varier considérablement de la valeur moyenne.

Vous ne définissez pas une fenêtre tampon pour l’encodage VBR sans contrainte comme vous le feriez pour un flux encodé CBR. Au lieu de cela, le codec calcule la taille de la fenêtre de mémoire tampon requise en fonction des exigences des exemples encodés.

L’avantage d’un encodage VBR non restreint est que le flux compressé a la qualité la plus élevée possible tout en restant dans une bande passante moyenne prévisible.

## <a name="constrained-vbr-encoding"></a>Encodage VBR restreint

L’encodage VBR contraint est identique à l’encodage VBR non restreint, sauf que vous spécifiez une vitesse de transmission maximale et une fenêtre de mémoire tampon maximale dans le profil. Le codec utilise ensuite les valeurs maximales pour déterminer comment compresser les données. Si vous définissez des valeurs maximales suffisamment élevées, l’encodage VBR contraint produira le même flux encodé comme un encodage VBR non restreint.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Choix d’une méthode d’encodage**](choosing-an-encoding-method.md)
</dt> <dt>

[**Fonctionnalités du codec**](codec-features.md)
</dt> <dt>

[**Configuration de flux**](configuring-streams.md)
</dt> <dt>

[**Configuration de flux VBR**](configuring-vbr-streams.md)
</dt> <dt>

[**Encodage à débit binaire constant (CBR)**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**Encodage en deux passes**](two-pass-encoding.md)
</dt> <dt>

[**Utilisation de l’encodage Two-Pass**](using-two-pass-encoding.md)
</dt> </dl>

 

 




