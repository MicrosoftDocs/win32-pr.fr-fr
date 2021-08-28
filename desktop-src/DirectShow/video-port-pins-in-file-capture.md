---
description: Broches de port vidéo dans la capture de fichiers
ms.assetid: 0fa6d88e-3c64-487f-b007-8c65bf47211d
title: Broches de port vidéo dans la capture de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab348c7e378f4130b43eef45f2cf4ddd079b0e85a77397b767cadddde5a7d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049379"
---
# <a name="video-port-pins-in-file-capture"></a>Broches de port vidéo dans la capture de fichiers

Si le périphérique de capture a un port vidéo, le code pin du port vidéo doit être connecté à un convertisseur vidéo, même si vous souhaitez uniquement effectuer une capture dans un fichier.

si vous appelez [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) avec la valeur **broche \_ catégorie \_ capturer** et que l’appareil a une broche de port vidéo, le générateur de Graph de CAPTURE connecte automatiquement la broche de port vidéo au filtre de [Mixer de recouvrement](overlay-mixer-filter.md) et connecte le Mixer de recouvrement au convertisseur vidéo. le générateur de Graph de Capture masque la fenêtre vidéo en appelant [**IVideoWindow ::p \_ ut ut**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) avec la valeur **OAFALSE**. si l’application appelle ensuite **RenderStream** avec la version préliminaire de la **\_ \_ catégorie PIN**, les appels de Graph Builder de Capture **placent \_ autoshow** avec la valeur **OATRUE**, afin d’afficher la fenêtre vidéo.

après avoir appelé **RenderStream** avec **la \_ \_ CAPTURE de catégorie PIN**, vous pouvez vérifier s’il a ajouté le convertisseur vidéo en interrogeant le gestionnaire de Graph pour l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Capture vidéo dans un fichier](capturing-video-to-a-file.md)
</dt> </dl>

 

 



