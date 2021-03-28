---
description: Les fonctions suivantes sont utilisées avec les polices Microsoft OpenType incorporées.
ms.assetid: 8f47d7a5-db45-4a41-8af2-9fc6b373a531
title: Fonctions d’incorporation de police
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ece5b413be5489bf51df38fd92b6f3167823506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991240"
---
# <a name="font-embedding-functions"></a>Fonctions d’incorporation de police

Les fonctions suivantes sont utilisées avec les polices Microsoft OpenType incorporées.



| Fonction                                                                   | Description                                                                                                                                              |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*\_ALLOCPROC PCP*](/windows/desktop/api/FontSub/nc-fontsub-cfp_allocproc)                                      | Fonction d’allocation de mémoire fournie par l’application pour CreateFontPackage et MergeFontPackage.                                                              |
| [*\_FREEPROC PCP*](/windows/desktop/api/FontSub/nc-fontsub-cfp_freeproc)                                        | Fonction de désallocation de mémoire fournie par l’application pour CreateFontPackage et MergeFontPackage.                                                            |
| [*\_REALLOCPROC PCP*](/windows/desktop/api/FontSub/nc-fontsub-cfp_reallocproc)                                  | Fonction de réallocation de mémoire fournie par l’application pour CreateFontPackage et MergeFontPackage.                                                            |
| [**CreateFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-createfontpackage)                             | Crée une version plus compacte d’une police TrueType spécifiée, afin de la passer à une imprimante. La police obtenue peut être sous-ensemble, compressée ou les deux. |
| [**MergeFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-mergefontpackage)                               | Fusionne les polices de sous-ensemble créées par CreateFontPackage.                                                                                                        |
| [*READEMBEDPROC*](/previous-versions//dd162894(v=vs.85))                                       | Fonction de rappel fournie par le client pour lire le contenu du flux à partir d’une mémoire tampon.                                                                                 |
| [**TTCharToUnicode**](/windows/desktop/api/T2embapi/nf-t2embapi-ttchartounicode)                                 | Convertit un tableau de valeurs de code de type caractère 8 bits en valeurs Unicode 16 bits.                                                                               |
| [**TTDeleteEmbeddedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttdeleteembeddedfont)                       | Libère la mémoire utilisée par une police incorporée.                                                                                                                |
| [**TTEmbedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfont)                                         | Crée une structure de police contenant une police à caractères larges (16 bits) de sous-ensemble, en utilisant un contexte de périphérique comme source d’informations d’incorporation de polices.           |
| [**TTEmbedFontEx**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontex)                                     | Crée une structure de police contenant la police du caractère UCS-4 (32-bit) du sous-ensemble de caractères, à l’aide d’un contexte de périphérique comme source d’informations d’incorporation de polices.        |
| [**TTEmbedFontFromFileA**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontfromfilea)                       | Crée une structure de police contenant une police à caractères larges (16 bits) de sous-ensemble, à l’aide d’un fichier comme source d’informations d’incorporation de polices.                     |
| [**TTEnableEmbeddingForFacename**](/windows/desktop/api/T2embapi/nf-t2embapi-ttenableembeddingforfacename)       | Ajoute ou supprime des FaceNames dans la liste d’exclusion de caractères.                                                                                              |
| [**TTGetEmbeddedFontInfo**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetembeddedfontinfo)                     | Récupère des informations sur une police incorporée.                                                                                                            |
| [**TTGetEmbeddingType**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetembeddingtype)                           | Retourne les privilèges d’incorporation d’une police.                                                                                                                  |
| [**TTGetNewFontName**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetnewfontname)                               | Crée un nouveau nom pour une police incorporée installée.                                                                                                       |
| [**TTIsEmbeddingEnabled**](/windows/desktop/api/T2embapi/nf-t2embapi-ttisembeddingenabled)                       | Détermine si la liste d’exclusion de police contient une police spécifiée.                                                                                     |
| [**TTIsEmbeddingEnabledForFacename**](/windows/desktop/api/T2embapi/nf-t2embapi-ttisembeddingenabledforfacename) | Détermine si l’incorporation est activée pour une police spécifiée.                                                                                            |
| [**TTLoadEmbeddedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttloadembeddedfont)                           | Lit la police incorporée dans le flux de document et l’installe. Permet également à un client de restreindre davantage les privilèges d’incorporation de la police.             |
| [**TTRunValidationTests**](/windows/desktop/api/T2embapi/nf-t2embapi-ttrunvalidationtests)                       | Valide une partie ou toutes les données de glyphe d’une police à caractères larges (16 bits), dans la plage de tailles spécifiée.                                                         |
| [**TTRunValidationTestsEx**](/windows/desktop/api/T2embapi/nf-t2embapi-ttrunvalidationtestsex)                   | Version UCS-4 de TTRunValidationTests.                                                                                                                   |
| [*WRITEEMBEDPROC*](/previous-versions//dd145225(v=vs.85))                                     | Fonction de rappel fournie par le client pour écrire le contenu du flux dans une mémoire tampon.                                                                                  |



 

 

 
