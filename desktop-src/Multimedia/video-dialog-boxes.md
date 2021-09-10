---
title: Boîtes de dialogue vidéo
description: Boîtes de dialogue vidéo
ms.assetid: 65f0d8de-c782-4d91-b38e-b36445f07af3
keywords:
- Message WM_CAP_DLG_VIDEOSOURCE
- capDlgVideoSource macro)
- Message WM_CAP_DLG_VIDEOFORMAT
- capDlgVideoFormat macro)
- Message WM_CAP_DLG_VIDEODISPLAY
- capDlgVideoDisplay macro)
- Message WM_CAP_DLG_VIDEOCOMPRESSION
- capDlgVideoCompression macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046fbb6cedbf86fd4ad7262c7685b10a5ff7b003
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369396"
---
# <a name="video-dialog-boxes"></a>Boîtes de dialogue vidéo

Chaque pilote de capture peut fournir jusqu’à quatre boîtes de dialogue pour contrôler les aspects du processus de numérisation et de capture vidéo, et pour définir des attributs de compression utilisés pour réduire la taille des données vidéo. Le contenu de ces boîtes de dialogue est défini par le pilote de capture vidéo.

La boîte de dialogue source vidéo contrôle la sélection des canaux d’entrée vidéo et des paramètres affectant l’image vidéo en cours de numérisation dans la mémoire tampon de trame. Cette boîte de dialogue énumère les types de signaux qui connectent la source vidéo à la carte de capture (généralement les entrées SVHS et composite) et fournit des contrôles pour modifier la teinte, le contraste ou la saturation. Si la boîte de dialogue est prise en charge par un pilote de capture vidéo, vous pouvez l’afficher et la mettre à jour à l’aide du message [**WM \_ Cap \_ DLG \_ VIDEOSOURCE**](wm-cap-dlg-videosource.md) (ou de la macro [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) ).

La boîte de dialogue Format vidéo contrôle la sélection des dimensions de l’image numérisée et de la profondeur de l’image, ainsi que des options de compression de la vidéo capturée. Si la boîte de dialogue est prise en charge par un pilote de capture vidéo, vous pouvez l’afficher et la mettre à jour à l’aide du message [**WM \_ Cap \_ DLG \_ VIDEOFORMAT**](wm-cap-dlg-videoformat.md) (ou de la macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) ).

La boîte de dialogue affichage vidéo contrôle l’apparence de la vidéo sur le moniteur pendant la capture. Les contrôles de cette boîte de dialogue n’ont aucun effet sur les données numérisées de la vidéo, mais elles peuvent affecter la présentation du signal numérisé. Par exemple, les appareils de capture qui prennent en charge la superposition peuvent permettre de modifier la teinte et la saturation, la couleur de la clé ou l’alignement de la superposition. Si la boîte de dialogue est prise en charge par un pilote de capture vidéo, vous pouvez l’afficher et la mettre à jour à l’aide du message [**WM \_ Cap \_ DLG \_ VIDEODISPLAY**](wm-cap-dlg-videodisplay.md) (ou de la macro [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) ).

La boîte de dialogue compression vidéo contrôle les attributs de compression vidéo postérieurs à la capture. Si la boîte de dialogue est prise en charge par un pilote de capture vidéo, vous pouvez l’afficher et la mettre à jour à l’aide du message [**WM \_ Cap \_ DLG \_ VIDEOCOMPRESSION**](wm-cap-dlg-videocompression.md) (ou de la macro [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) ).

 

 




