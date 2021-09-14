---
title: Polices et texte (OpenGL)
description: l’implémentation de OpenGL par Microsoft dans Windows prend en charge les graphiques GDI dans une fenêtre OpenGL à mémoire tampon unique.
ms.assetid: 25a45e1a-6c1e-416b-8993-daeefc1100f3
keywords:
- OpenGL sur Windows, polices
- OpenGL sur Windows, texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fba4ffe996bd88a6285f615ddacb31e57fc311
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011511"
---
# <a name="fonts-and-text-opengl"></a>Polices et texte (OpenGL)

l’implémentation de OpenGL par Microsoft dans Windows prend en charge les graphiques GDI dans une fenêtre OpenGL à mémoire tampon unique. Elle ne prend pas en charge les graphiques GDI dans une fenêtre OpenGL à double mémoire tampon. Par conséquent, vous pouvez appeler uniquement les fonctions de texte et de police GDI standard pour dessiner du texte dans une fenêtre OpenGL à une seule mise en mémoire tampon ; vous ne pouvez pas appeler ces fonctions pour dessiner du texte dans une fenêtre OpenGL à deux mémoires tampons.

Il existe une solution de contournement pour cette restriction sur du texte dans les fenêtres à deux mémoires tampons : créez des listes d’affichage OpenGL pour les images bitmap de caractères, puis exécutez ces listes d’affichage pour dessiner des caractères. Ce processus comporte trois étapes principales :

1.  Sélectionnez une police pour un contexte de périphérique, en définissant les propriétés de la police comme vous le souhaitez.
2.  Créer un ensemble de listes d’affichage bitmap en fonction des glyphes dans la police du contexte de périphérique, une liste d’affichage pour chaque glyphe que l’application dessinera.
3.  Dessinez chaque glyphe dans une chaîne, à l’aide de ces listes d’affichage bitmap.

Pour créer les listes d’affichage, appelez les fonctions [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) et [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) . Pour dessiner des caractères dans une chaîne à l’aide de ces listes d’affichage, appelez [**glCallLists**](glcalllists.md).

Pour créer des applications faciles à localiser et utilisant des ressources avec parcimonie, la création et le stockage de ces listes d’affichage d’image de glyphe doivent être gérés avec précaution. De nombreux langages, contrairement à l’anglais, possèdent des alphabets dont les codes de caractères sont compris dans un ensemble de valeurs relativement volumineux.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions de police et de texte](font-and-text-functions.md)
</dt> </dl>

 

 




