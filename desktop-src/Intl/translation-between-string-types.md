---
description: Les fonctions énumérées dans le tableau suivant traduisent les chaînes de caractères d’un type de chaîne en un autre.
ms.assetid: 26802339-6291-4767-b468-68a9e8e95774
title: Conversion entre types chaîne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877721f2d8ce3852011786e487598e3fd068c9eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524259"
---
# <a name="translation-between-string-types"></a>Conversion entre types chaîne

Les fonctions énumérées dans le tableau suivant traduisent les chaînes de caractères d’un type de chaîne en un autre.



| Fonction                                           | Description                                             |
|----------------------------------------------------|---------------------------------------------------------|
| [**FoldString devant**](/windows/win32/api/stringapiset/nf-stringapiset-foldstringw)                   | Convertit une chaîne de caractères en une autre.             |
| [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                 | Mappe une chaîne de caractères par paramètres régionaux.                      |
| [**ToUnicode**](/windows/win32/api/winuser/nf-winuser-tounicode)              | Traduit un code de touche virtuelle en un caractère Unicode. |
| [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) | Mappe une chaîne multioctet à une chaîne Unicode.            |
| [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) | Mappe une chaîne Unicode à une chaîne multioctet.            |



 

Les fonctions [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) et [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) sont particulièrement utiles pour les applications qui prennent en charge plusieurs types de chaînes. ANSI C définit également les fonctions de conversion **wcstombs** et **mbstowcs**, mais elles peuvent uniquement être converties vers et à partir du jeu de caractères pris en charge par la bibliothèque C standard.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Unicode dans l'API Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
