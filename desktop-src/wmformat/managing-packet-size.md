---
title: Gestion de la taille des paquets
description: Gestion de la taille des paquets
ms.assetid: 75ccda39-255a-4213-824e-1ca778a741dc
keywords:
- Windows Media Format SDK, gestion des tailles de paquets
- Windows Media Format SDK, tailles de paquets
- profils, tailles de paquets
- profils, gestion des tailles de paquets
- paquets, tailles
- paquets, interface IWMPacketSize
- IWMPacketSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e5bb0720d54338a754838e3d44c4479e55af9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234606"
---
# <a name="managing-packet-size"></a>Gestion de la taille des paquets

Le writer est conçu pour gérer la taille des paquets en interne. Toutefois, vous pouvez avoir des exigences spécifiques pour votre application qui appellent un contrôle manuel sur la taille des paquets dans les fichiers ASF que vous écrivez. le kit de développement logiciel (SDK) Windows Media Format fournit deux interfaces, [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) et [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) , qui vous permettent de contrôler la taille maximale et la taille minimale des paquets.

Les deux interfaces de taille de paquet sont exposées dans l’objet de profil. Ils sont également disponibles pour l’objet lecteur. Comme avec d’autres interfaces liées aux profils, le lecteur peut accéder uniquement aux méthodes de lecture.

La taille des paquets a un impact sur les performances. En général, plus la taille du paquet est faible, plus les données sont fragmentées dans un fichier. Plus un fichier est fragmenté, moins il sera efficace de le reconstruire. Dans un scénario de diffusion en continu, ce n’est peut-être pas une considération importante, car le processus de lecture d’un fichier à partir d’une source Internet est généralement inefficace. Toutefois, lorsque vous traitez un fichier localement, cela peut être une considération.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)
</dt> <dt>

[**Interface IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)
</dt> <dt>

[**Utilisation des profils**](working-with-profiles.md)
</dt> </dl>

 

 




