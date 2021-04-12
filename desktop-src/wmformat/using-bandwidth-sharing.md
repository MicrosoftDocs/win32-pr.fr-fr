---
title: Utilisation du partage de bande passante
description: Utilisation du partage de bande passante
ms.assetid: 1df61a3a-d34a-447e-a7ee-d5d409e7c4fa
keywords:
- Windows Media Format SDK, partage de bande passante
- partage de bande passante, à propos de
- profils, partage de bande passante
- flux, partage de bande passante
- partage de bande passante, interface IWMProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298c690b484a8b4b5990aacd5d525867da8923c0
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104381699"
---
# <a name="using-bandwidth-sharing"></a>Utilisation du partage de bande passante

Vous pouvez utiliser des objets de partage de bande passante pour spécifier que certains flux, lorsqu’ils sont combinés, n’utilisent pas plus de bande passante que ce qui est spécifié. Les informations contenues dans un objet de partage de bande passante ne sont pas générées ou vérifiées par le writer et ne sont utilisées par le lecteur pour rien.

Lorsqu’un fichier écrit qui possède des informations de partage de bande passante dans son profil, les données sont stockées dans sa section d’en-tête. Vous pouvez utiliser l’interface [**IWMProfile**](iwmprofile.md) dans le lecteur pour vérifier les informations de partage de bande passante lors de la lecture du fichier.

Chaque objet de partage de bande passante est défini par deux paramètres. Tout d’abord, la bande passante, telle que définie par une bande passante et une fenêtre de mémoire tampon. Le deuxième paramètre est un type de partage de bande passante, qui peut être exclusif ou partiel. Le partage de bande passante exclusive signifie que les flux constitutifs sont lus l’un après l’autre, tandis que partial signifie que les flux sont remis simultanément.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMProfile**](iwmprofile.md)
</dt> <dt>

[**IWMProfile3::AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing)
</dt> <dt>

[**IWMProfile3::CreateNewBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing)
</dt> <dt>

[**IWMProfile3::GetBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)
</dt> <dt>

[**IWMProfile3::GetBandwidthSharingCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharingcount)
</dt> <dt>

[**Utilisation des profils**](working-with-profiles.md)
</dt> </dl>

 

 




