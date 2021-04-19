---
title: Choix d’une méthode d’encodage
description: Choix d’une méthode d’encodage
ms.assetid: 095245a6-39eb-4228-86ac-ade94dde3695
keywords:
- profils, choix des méthodes d’encodage
- profils, méthodes d’encodage
- codecs, choix des méthodes d’encodage
- codecs, méthodes d’encodage
- profils, sélection des méthodes d’encodage
- codecs, sélection des méthodes d’encodage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54c5bd099e5aaf8b3a735594c8b87a335fc2594
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511822"
---
# <a name="choosing-an-encoding-method"></a>Choix d’une méthode d’encodage

Certains codecs, comme le codec Windows Media Video 9, prennent en charge plusieurs méthodes d’encodage. La méthode d’encodage que vous choisissez pour un flux dépend de la façon dont le flux doit être remis. Le tableau suivant décrit quand utiliser les différentes méthodes d’encodage.



| Méthode de codage                | Description                                                                                                                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vitesse de transmission constante en 1 passe (CBR) | La seule option pour la diffusion en continu en direct. Encode une vitesse de transmission prévisible et fournit la qualité la plus faible de toutes les méthodes d’encodage.                                                                    |
| 2-pass CBR                     | Utilisez pour les fichiers qui seront diffusés en continu sur un réseau vers un lecteur client, mais qui ne sont pas diffusés à partir d’une source active. Encode une vitesse de transmission prévisible, mais avec une qualité supérieure à 1-pass CBR. |
| Vitesse de transmission variable (VBR) de passe 1 | Utilisez lorsque vous devez spécifier la qualité de la sortie encodée. Offre la qualité la plus cohérente de toutes les méthodes d’encodage. À utiliser uniquement pour les fichiers locaux ou pour le téléchargement.                        |
| 2-pass VBR – sans contrainte     | Utilisez lorsque vous devez spécifier une bande passante, mais que des fluctuations autour de la bande passante spécifiée sont acceptables. Pour les fichiers locaux ou uniquement pour le téléchargement.                                                    |
| 2-passer le VBR-restreint       | Utilisez dans les mêmes conditions que sans contrainte, mais lorsque vous devez spécifier un taux de bits momentané maximal. Pour les fichiers locaux ou uniquement pour le téléchargement.                                                |



 

Le tableau suivant répertorie les méthodes d’encodage prises en charge par les codecs fournis avec le kit de développement logiciel (SDK) du format Windows Media.



| Codec                                  | CBR | 2-pass CBR | MODE VBR | 2-passer le VBR |
|----------------------------------------|-----|------------|-----|------------|
| Windows Media Video 9                  | X   | X          | X   | X          |
| Windows Media Audio 9 et versions ultérieures        | X   | X          | X   | X          |
| Écran Windows Media Video 9           | X   |            | X   |            |
| Voix Windows Media Audio 9            | X   |            |     |            |
| Windows Media Audio professionnel       | X   | X          | X   | X          |
| Windows Media Audio sans perte           |     |            | X   |            |
| Image Windows Media Video 9 et versions ultérieures  | X   |            | X   |            |
| Profil avancé Windows Media Video 9 | X   | X          | X   | X          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Conception de profils**](designing-profiles.md)
</dt> <dt>

[**Encodage à débit binaire constant (CBR)**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**Encodage en deux passes**](two-pass-encoding.md)
</dt> <dt>

[**Encodage à vitesse de transmission variable (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




