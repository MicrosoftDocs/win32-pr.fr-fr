---
title: Pour utiliser IVTC (inverse telecine)
description: Pour utiliser IVTC (inverse telecine)
ms.assetid: 7752d1ac-34b1-446a-a69c-29463c9e10f7
keywords:
- Windows Media Format SDK, inversement Telecine
- Windows Media Format SDK, Telecine
- ASF (Advanced Systems Format), inversement
- ASF (format avancé des systèmes), inversement
- ASF (Advanced Systems Format), télécinéma
- ASF (format avancé des systèmes), télécinéma
- inverser Telecine
- télécinéma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17d4f4e3ae34c2a9efcaa4fe8e5ce7256474404
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225836"
---
# <a name="to-use-inverse-telecine"></a>Pour utiliser IVTC (inverse telecine)

Telecine est le processus de conversion d’un film, qui compte 24 images par seconde, en vidéo, qui contient 60 champs (demi-frames) par seconde. Ce processus place les images de chaque image de film dans plusieurs champs vidéo.

Quand vous encodez numériquement une vidéo qui a été créée à partir d’un film à l’aide de Telecine, le processus de compression peut entraîner des artefacts de mouvement et d’autres dégradations de qualité. pour éviter d’affecter la qualité de la sortie numérique, le codec Windows Media Video 9 prend en charge l’inverse de telecine. Lorsque vous utilisez l’inverse telecine, le codec reconstruit les 24 images d’origine par seconde à partir de la vidéo d’entrée avant de coder le contenu.

Pour utiliser l’inverse telecine, vous devez :

-   Utilisez un profil avec un flux vidéo défini sur 24 images par seconde.
-   Connaître la configuration de champ de la vidéo d’entrée.

Pour utiliser l’inverse telecine pour une entrée au writer, procédez comme suit.

1.  Configurez le writer comme d’habitude. Pour plus d’informations, consultez [écriture de fichiers ASF](writing-asf-files.md).
2.  Avant de commencer à écrire des exemples, obtenez un pointeur vers l’interface [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) en appelant **IWMWriter :: QueryInterface**.
3.  Identifiez le flux à reconstruire en appelant [**IWMWriterAdvanced2 :: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) pour le numéro d’entrée souhaité. Pass g \_ wszDeinterlaceMode comme paramètre et WM \_ DM \_ désentrelace \_ INVERSETELECINE comme valeur.
4.  Appelez à nouveau **SetInputSetting** pour définir g \_ wszInitialPatternForInverseTelecine.
5.  Écrivez le fichier comme d’habitude.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Rubriques avancées**](advanced-topics.md)
</dt> <dt>

[**Interface IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Interface IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)
</dt> </dl>

 

 




