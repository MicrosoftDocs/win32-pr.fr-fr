---
title: Écriture d’une image Flux
description: Écriture d’une image Flux
ms.assetid: 3a017bdd-9723-4b7f-b5e1-22838c0ba4ff
keywords:
- ASF (Advanced Systems Format), écriture de flux d’images
- ASF (format de systèmes avancés), écrire des flux d’images
- ASF (Advanced Systems Format), flux d’images
- ASF (format des systèmes avancés), flux d’images
- flux d’images, écriture
- flux, écrire des flux d’images
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6061af2ff43cbeb3fe688b6533eee044036df029bdb7f7305af305c8d45084
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006299"
---
# <a name="writing-image-streams"></a>Écriture d’une image Flux

Les entrées d’un flux d’image doivent être des images bitmap au format RVB. L’enregistreur coordonne la compression des exemples d’images d’entrée à l’aide du format JPEG. Avant de commencer à écrire un fichier contenant un flux d’image, vous devez définir une qualité d’image pour l’entrée, à l’aide du \_ paramètre g wszJPEGCompressionQuality. Utilisez [**IWMWriterAdvanced2 :: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) pour définir la qualité sur une valeur **DWORD** comprise entre 1 et 100. Les valeurs basses représentent un taux de compression élevé au détriment de la qualité, tandis que les valeurs élevées produisent des images de haute qualité qui nécessitent davantage d’espace.

Les flux d’image requièrent souvent des mémoires tampons plus volumineuses que les flux vidéo ordinaires. La taille exacte requise dépend du type d’image et de la qualité de l’image, entre autres facteurs. Utilisez la version d’évaluation et l’erreur pour déterminer la taille appropriée pour les images que vous souhaitez traiter.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Image Flux**](image-streams.md)
</dt> <dt>

[**pour définir les Paramètres d’entrée**](to-set-input-settings.md)
</dt> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> </dl>

 

 




