---
description: La clé de Registre EUDC contient une ou plusieurs sous-clés contenant des valeurs définissant les polices associées aux caractères définis par l’utilisateur (EUDCs) pour une page de codes donnée.
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: EUDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a7509364545d9de01d4480a58d4e6af8043c30fa8f74db0fdbaf24e252e298
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082989"
---
# <a name="eudc"></a>EUDC

La clé de Registre EUDC contient une ou plusieurs sous-clés contenant des valeurs définissant les polices associées aux [caractères définis par l’utilisateur (EUDCs)](end-user-defined-characters.md) pour une page de codes donnée. Il a l’emplacement de Registre suivant :

HKEY \_ Current \_ User \\ EUDC

Le format est le suivant :

EUDC SystemDefaultEUDCFont = TrueTypeEUDCFontFileName TrueTypeFontTypeface = TrueTypeEUDCFontFileName

où :



| Valeur                         | Description                                                                                                                                         |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| SystemDefaultEUDCFont    | Nom prédéfini utilisé pour définir la police par défaut du système. Il n’existe aucune police EUDC par défaut du système, sauf si cette entrée est explicitement spécifiée.     |
| TrueTypeFontTypeface     | Nom défini par l’utilisateur associé à une police TrueType non-EUDC.                                                                              |
| TrueTypeEUDCFontFileName | Chaîne composée du nom de fichier d’un fichier de police EUDC distinct. Ce fichier identifie une police à associer à TrueTypeFontTypeface. |



 

L’exemple suivant illustre la clé EUDC pour la page de codes 932.


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



L’exemple suivant définit la police EUDC par défaut du système sur EUDC. ttf et associe les polices EUDC distinctes Mineudc. ttf et Goteudc. ttf aux noms de police MS Mincho et MS Gothic, respectivement.


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



lorsque la Windows page de codes (système ACP) associée à la langue des programmes non-Unicode correspond à la sous-clé, le sous-système GDI recherche les paires de valeurs de la sous-clé pour obtenir des informations d’affichage sur le caractère. Il recherche d’abord un nom correspondant à la police actuelle. S’il n’y en a aucun, il examine la valeur SystemDefaultEUDCFont. Si aucune valeur n’est définie, GDI traite le caractère comme non défini.

notez que le texte lui-même n’a pas besoin d’être dans la page de codes Windows. par exemple, supposons que la page de codes possède l’identificateur 1252, la page de codes Windows par défaut pour l’anglais. Une application transmet le point de code Unicode unique U + E000, dans la zone d’utilisation privée Unicode (PUA), à [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext). Dans ce cas, GDI examine les valeurs de Registre inférieures à 1252 pour obtenir les informations de police pour les propriétés d’affichage de caractères.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Entrées de Registre EUDC](eudc-registry-entries.md)
</dt> <dt>

[EUDCCodeRange](eudccoderange.md)
</dt> </dl>

 

 
