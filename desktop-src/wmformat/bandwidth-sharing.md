---
title: Partage de bande passante
description: Partage de bande passante
ms.assetid: d33f3454-d20a-4b4d-9902-dabc5b806ad6
keywords:
- Windows Media Format SDK, partage de bande passante
- ASF (Advanced Systems Format), partage de bande passante
- ASF (format de systèmes avancés), partage de bande passante
- Windows Media Format SDK, Streams
- ASF (Advanced Systems Format), flux
- ASF (format de systèmes avancés), flux
- partage de bande passante, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b01ff94e82f2ce3609a93278fef30c68e1a59445eea22f68f4b0a5d92371a19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709409"
---
# <a name="bandwidth-sharing"></a>Partage de bande passante

Vous pouvez spécifier des flux dans un fichier qui, lorsqu’ils sont utilisés ensemble, utilisent moins de bande passante que la somme des vitesses de transmission indiquées. En spécifiant le partage de bande passante dans le profil, vous précisez que vous devez lire les applications dont la bande passante disponible pour diffuser le fichier n’est pas celle qui pourrait autrement paraître.

aucun des objets du kit de développement logiciel (SDK) de Format multimédia Windows modifie leur comportement en réponse aux informations de partage de bande passante, qui sont fournies uniquement afin que la lecture des applications puisse prendre en compte pour déterminer si un fichier peut être lu avec une remise de bande passante limitée.

Le partage de bande passante est configuré avec un objet de partage de bande passante et est ajouté à un profil avant de commencer à écrire un fichier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités des fichiers ASF**](asf-file-features.md)
</dt> <dt>

[**Objet de partage de bande passante**](bandwidth-sharing-object.md)
</dt> <dt>

[**Interface IWMBandwidthSharing**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing)
</dt> <dt>

[**Interface IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)
</dt> <dt>

[**Utilisation du partage de bande passante**](using-bandwidth-sharing.md)
</dt> </dl>

 

 




