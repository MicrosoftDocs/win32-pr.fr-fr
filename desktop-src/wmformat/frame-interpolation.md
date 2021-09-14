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
ms.openlocfilehash: 5c62f95322920576eec0f10f3e4d61a279fdc4cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234671"
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

 

 




