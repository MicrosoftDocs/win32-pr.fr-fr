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
ms.openlocfilehash: a87a780798885e86b515a8d111797af304a58f13c962ecab7f7862dfb1790411
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117656129"
---
# <a name="choosing-an-encoding-method"></a>Choix d’une méthode d’encodage

certains codecs, comme le codec Windows Media Video 9, prennent en charge plusieurs méthodes d’encodage. La méthode d’encodage que vous choisissez pour un flux dépend de la façon dont le flux doit être remis. Le tableau suivant décrit quand utiliser les différentes méthodes d’encodage.



| Méthode de codage                | Description                                                                                                                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vitesse de transmission constante en 1 passe (CBR) | La seule option pour la diffusion en continu en direct. Encode une vitesse de transmission prévisible et fournit la qualité la plus faible de toutes les méthodes d’encodage.                                                                    |
| 2-pass CBR                     | Utilisez pour les fichiers qui seront diffusés en continu sur un réseau vers un lecteur client, mais qui ne sont pas diffusés à partir d’une source active. Encode une vitesse de transmission prévisible, mais avec une qualité supérieure à 1-pass CBR. |
| Vitesse de transmission variable (VBR) de passe 1 | Utilisez lorsque vous devez spécifier la qualité de la sortie encodée. Offre la qualité la plus cohérente de toutes les méthodes d’encodage. À utiliser uniquement pour les fichiers locaux ou pour le téléchargement.                        |
| 2-pass VBR – sans contrainte     | Utilisez lorsque vous devez spécifier une bande passante, mais que des fluctuations autour de la bande passante spécifiée sont acceptables. Pour les fichiers locaux ou uniquement pour le téléchargement.                                                    |
| 2-passer le VBR-restreint       | Utilisez dans les mêmes conditions que sans contrainte, mais lorsque vous devez spécifier un taux de bits momentané maximal. Pour les fichiers locaux ou uniquement pour le téléchargement.                                                |



 

le tableau suivant répertorie les méthodes d’encodage prises en charge par les codecs fournis avec le kit de développement logiciel (SDK) de Format multimédia Windows.



| Codec                                  | CBR | 2-pass CBR | MODE VBR | 2-passer le VBR |
|----------------------------------------|-----|------------|-----|------------|
| Windows Media Video 9                  | X   | X          | X   | X          |
| Windows Média audio 9 et versions ultérieures        | X   | X          | X   | X          |
| Windows Écran Media Video 9           | X   |            | X   |            |
| Windows Media Audio 9 voix            | X   |            |     |            |
| Windows Professional multimédia audio       | X   | X          | X   | X          |
| Windows Média audio sans perte           |     |            | X   |            |
| Windows Media Video 9 image et versions ultérieures  | X   |            | X   |            |
| Windows Profil Media Video 9 Advanced | X   | X          | X   | X          |



 

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

 

 




