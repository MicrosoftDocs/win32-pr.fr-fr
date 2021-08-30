---
title: Interpolation de frame
description: Interpolation de frame
ms.assetid: 74dbe855-361c-42ba-b21b-322ccd1c91d0
keywords:
- Windows Media Format SDK, interpolation de trame
- codecs, interpolation de trame
- interpolation de frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b10691bd2a1f3e6257810efd1e243d099cd4cfa85f0b2522369786602792614
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007009"
---
# <a name="frame-interpolation"></a>Interpolation de frame

L’interpolation de frames est le processus de création de trames vidéo intermédiaires basées sur les données dans deux images consécutives de la vidéo encodée. En effet, l’interpolation de frame augmente la [*fréquence d’images*](wmformat-glossary.md) de la vidéo encodée au moment du décodage. Vous pouvez utiliser l’interpolation de frames pour améliorer la fluidité de la lecture des flux vidéo avec des fréquences d’images faibles.

Comme il s’agit d’une fonctionnalité de décodage, elle n’implique aucune option d’encodage spéciale et n’ajoute aucune surcharge au contenu. L’interpolation de frame est spécifiée en tant que paramètre de sortie dans l’objet lecteur.

seul le codec Windows Media Video 9 prend en charge l’interpolation de trame.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités du codec**](codec-features.md)
</dt> <dt>

[**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[**Paramètres de sortie**](output-settings.md)
</dt> </dl>

 

 




