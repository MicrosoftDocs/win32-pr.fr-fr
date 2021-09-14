---
title: Comment utiliser la liaison de police dans les contrôles RichEdit
description: Microsoft Rich Edit 3,0 affecte un jeu de caractères aux caractères de texte brut en fonction de leur contexte.
ms.assetid: 975B9C33-6766-4FF1-A93E-2169C140CEE9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea17c2f8e0e8c1b57611839a5bbf992f9af6bf65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115369"
---
# <a name="how-to-use-font-binding-in-rich-edit-controls"></a>Comment utiliser la liaison de police dans les contrôles RichEdit

Microsoft Rich Edit 3,0 affecte un jeu de caractères aux caractères de texte brut en fonction de leur contexte. Quelques exemples :

-   Les caractères grecs sont affectés au **\_ jeu** de caractères grec.
-   Les symboles Hangul sont affectés d’un **\_ jeu** de caractères Hangul.
-   Des caractères chinois sont affectés au **\_ jeu** de caractères SHIFTJIS si des caractères Kana sont trouvés à proximité, ou un **\_ jeu** de caractères GB2312 si aucun Kana n’est trouvé à proximité.
-   Les caractères ANSI non neutres sont assignés à un **\_ jeu** de caractères ANSI dans n’importe quel événement.

> [!Note]  
> Le contrôle Rich Edit utilise Unicode en interne, ce qui signifie que cette utilisation des jeux de caractères diffère de celle d’origine utilisée dans les spécifications de police. Mais la structure [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) a un emplacement bien défini pour le jeu de caractères.

 

Les caractères neutres comme les espaces et les chiffres reçoivent un jeu de caractères en fonction de leur contexte. Par exemple, un espace entouré de caractères du même jeu de caractères obtient ce jeu de caractères. Les caractères neutres et les chiffres utilisés pour le texte bidirectionnel reçoivent des jeux de caractères d’une manière basée sur l’algorithme bidirectionnel Unicode.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="use-font-binding-in-a-rich-edit-control"></a>Utiliser la liaison de police dans un contrôle RichEdit

Une fois les jeux de caractères affectés, Rich Edit analyse le texte du point d’insertion vers l’avant et vers l’arrière pour trouver les polices les plus proches qui ont été utilisées pour les jeux de caractères. Si aucune police n’est trouvée pour un jeu de caractères, la modification riche utilise la police choisie par le client pour ce jeu de caractères. Si le client n’a pas spécifié de police pour le jeu de caractères, la modification complète utilise la police par défaut pour ce jeu de caractères. Si le client souhaite une autre police, le client peut toujours le modifier, mais cette approche fonctionnera la plupart du temps. Les choix de polices par défaut actuels sont basés sur le tableau suivant. Notez que les polices par défaut sont définies par processus, et qu’il existe des listes distinctes pour l’utilisation de l’interface utilisateur et pour l’utilisation de l’interface utilisateur.



| Langage                    | Nom de police de l’interface utilisateur  | Taille de police de l’interface utilisateur | nom de police non-IU | taille de police n’appartenant pas à l’interface utilisateur |
|-----------------------------|---------------|--------------|------------------|------------------|
| Occidental, CE, ME, vietnamien | Tahoma        | 8            | Arial            | 10               |
| Japonais                    | MS UI Gothic  | 9            | MS P Gothic      | 10               |
| Coréen                      | Gulim         | 9            | Gulim            | 9                |
| Chinois simplifié          | SimSun        | 9            | SimSun           | 10               |
| Chinois traditionnel         | PMingLiU      | 9            | PMingLiU         | 9                |
| Thaï                        | MS sans serif | 8            | Tahoma           | 14               |
| symboles                     | Wingdings     | 8            | Wingdings        | 10               |
| Dévanâgarî                  | Mangal        | 8            | Mangal           | 10               |
| Tamoul                       | Latha         | 8            | Latha            | 10               |
| Géorgien, arménien          | Arial Unicode | 8            | Arial Unicode    | 10               |



 

Par conséquent, dans la table de liaison de police par défaut (les entrées ont un jeu de caractères, un nom de police et une taille), la modification riche permet \_ à ANSI charset de correspondre à plusieurs jeux de caractères, tandis que le jeu de caractères approprié correspond à d’autres polices sur une base un-à-un. Plus précisément, la modification riche utilise le jeu de caractères ANSI à \_ chaque fois qu’aucune autre solution n’est trouvée. Vous serez en mesure de spécifier une granularité plus fine que celle-ci. par exemple, affectez un jeu de caractères arabe spécifique \_ pour les exécutions arabes, une police grecque spécifique pour les exécutions grecques, et ainsi de suite. Cette granularité plus fine sera également utilisée si une police avec le marqueur de jeu de caractères souhaité est trouvée dans le document avant la zone qui est liée aux polices.

Notez que la modification enrichie ne gère pas actuellement un glyphe manquant dans une police qui prétend prendre en charge un jeu de caractères mais qui est incomplète. Au moment de l’affichage dans un script complexe, la modification complète fait qu’il manque un glyphe de ce type, mais n’entraîne pas l’utilisation d’une nouvelle police par le magasin de stockage. En règle générale, la liaison de police sous-jacente du système d’exploitation effectue cette opération.

## <a name="remarks"></a>Notes

**Édition enrichie 4,1 :** Pour définir la police par défaut d’un script, [**appelez em \_ SETCHARFORMAT**](em-setcharformat.md) avec [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a), en spécifiant des valeurs pour les membres **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** et **LCID** . En outre, pour obtenir la police par défaut pour une page de codes spécifique, appelez [**em \_ GETCHARFORMAT**](em-getcharformat.md) avec **CHARFORMAT2**, en spécifiant des valeurs pour les membres **bCharSet** et **LCID** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de contrôles RichEdit](using-rich-edit-controls.md)
</dt> <dt>

[Windows démonstration des contrôles communs (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




