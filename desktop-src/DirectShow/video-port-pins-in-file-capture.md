---
description: Broches de port vidéo dans la capture de fichiers
ms.assetid: 0fa6d88e-3c64-487f-b007-8c65bf47211d
title: Broches de port vidéo dans la capture de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2361c5a7cdaa7640ece9724000963f39f3f77ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520420"
---
# <a name="video-port-pins-in-file-capture"></a>Broches de port vidéo dans la capture de fichiers

Si le périphérique de capture a un port vidéo, le code pin du port vidéo doit être connecté à un convertisseur vidéo, même si vous souhaitez uniquement effectuer une capture dans un fichier.

Si vous appelez [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) avec la valeur **broche \_ catégorie \_ capturer** et que l’appareil a une broche de port vidéo, le générateur de graphiques de capture connecte automatiquement la broche de port vidéo au filtre de [mixage de superposition](overlay-mixer-filter.md) et connecte le mélangeur de superposition au convertisseur vidéo. Le générateur de graphiques de capture masque la fenêtre vidéo en appelant [**IVideoWindow ::p ut \_ automatique**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) avec la valeur **OAFALSE**. Si l’application appelle ensuite **RenderStream** avec la version préliminaire de la **\_ catégorie \_ pin**, le générateur de graphiques de capture appelle la fonction d' **\_ affichage** automatique avec la valeur **OATRUE**, afin d’afficher la fenêtre vidéo.

Après avoir appelé **RenderStream** avec **la \_ \_ capture de catégorie pin**, vous pouvez vérifier s’il a ajouté le convertisseur vidéo en interrogeant le gestionnaire du graphique de filtre pour l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Capture vidéo dans un fichier](capturing-video-to-a-file.md)
</dt> </dl>

 

 



