---
title: Utilisation des informations sur les mots et les sauts de ligne
description: Un contrôle Rich Edit appelle une fonction appelée procédure d’interruption de mot pour rechercher des sauts entre les mots et pour déterminer où elle peut couper les lignes.
ms.assetid: DDCE9814-0D39-494C-953A-FB6A98100EEA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feb90064e455bfeb8ee126e6107d75ef29b3a4f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115321"
---
# <a name="how-to-use-word-and-line-break-information"></a>Utilisation des informations sur les mots et les sauts de ligne

Un contrôle Rich Edit appelle une fonction appelée procédure d’interruption de mot pour rechercher des sauts entre les mots et pour déterminer où elle peut couper les lignes. Le contrôle utilise ces informations lors de l’exécution d’opérations de retour automatique à la ligne et lors du traitement des combinaisons de touches CTRL + Flèche gauche et CTRL + Flèche droite. Une application peut envoyer des messages à un contrôle Rich Edit pour remplacer la procédure de césure par défaut, pour récupérer des informations de césure de mots et pour déterminer la ligne sur laquelle se trouve un caractère donné.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="use-word-and-line-break-information"></a>Utiliser les informations sur les mots et les sauts de ligne

Les procédures de césure de mots pour les contrôles RichEdit sont similaires à celles des contrôles d’édition, mais elles ont des fonctionnalités supplémentaires : les procédures d’arrêt de mot pour les deux types de contrôles peuvent déterminer si un caractère est un délimiteur et peut Rechercher l’arrêt de mot le plus proche avant ou après la position spécifiée. Un délimiteur est un caractère qui marque la fin d’un mot, tel qu’un espace. En règle générale, dans un contrôle d’édition, un saut de mot se produit uniquement après les délimiteurs. Toutefois, différentes règles s’appliquent à la plupart des langues asiatiques.

Les procédures de césure de mots pour les contrôles RichEdit regroupent également des caractères dans des classes de caractères, chacune identifiée par une valeur comprise entre 0x00 et 0x0F. Des arrêts se produisent après des délimiteurs ou entre des caractères de classes différentes. Par conséquent, une procédure de césure lexicale avec des classes différentes pour les caractères alphanumériques et de ponctuation trouvera deux césures de mots dans la chaîne « Win.doc » (avant et après le point).

La classe d’un caractère peut être combinée avec zéro, un ou plusieurs indicateurs de césure lexicale pour former une valeur 8 bits. Lors de l’exécution d’opérations de retour automatique à la ligne, un contrôle RichEdit utilise des indicateurs de césure lexicale pour déterminer où il peut couper les lignes. La modification riche utilise les indicateurs de césure de mots suivants.



| Indicateur            | Description                                                                                                                       |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| WBF \_ BREAKAFTER | Les lignes peuvent être brisées après le caractère.                                                                                          |
| WBF \_ BREAKLINE  | Le caractère est un délimiteur. Les délimiteurs marquent les extrémités des mots. Les lignes peuvent être rompues après les délimiteurs.                            |
| WBF \_ ISWHITE    | Le caractère est un espace blanc. Les espaces blancs de fin ne sont pas inclus dans la longueur d’une ligne lors de l’encapsulation. |



 

La \_ valeur WBF BREAKAFTER est utilisée pour permettre l’encapsulation après un caractère qui ne marque pas la fin d’un mot, tel qu’un trait d’Union.

Vous pouvez remplacer la procédure de césure par défaut d’un contrôle RichEdit par votre propre procédure à l’aide du message [**em \_ SETWORDBREAKPROC**](em-setwordbreakproc.md) . Pour plus d’informations sur les procédures de césure de mots, consultez la description de la fonction [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) .

> [!Note]  
> Ce remplacement n’est pas recommandé pour Microsoft Rich Edit 2,0 et versions ultérieures, en raison de la complexité de la césure des mots multilingues.

 

Pour Microsoft Rich Edit 1,0, vous pouvez utiliser le message [**em \_ SETWORDBREAKPROCEX**](em-setwordbreakprocex.md) pour remplacer la procédure de coupure de mots étendue par défaut par une fonction [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) . Cette fonction fournit des informations supplémentaires sur le texte, telles que le jeu de caractères. Vous pouvez utiliser le message [**em \_ GETWORDBREAKPROCEX**](em-getwordbreakprocex.md) pour récupérer l’adresse de la procédure d’arrêt de mot étendu en cours. Notez que Microsoft Rich Edit 2,0 et versions ultérieures ne prennent pas en charge *EditWordBreakProcEx*, **em \_ GETWORDBREAKPROCEX** et **em \_ SETWORDBREAKPROCEX**.

Vous pouvez utiliser le message [**em \_ FINDWORDBREAK**](em-findwordbreak.md) pour rechercher les césures de mots ou pour déterminer les indicateurs de classe et de césure de mots d’un caractère. À son tour, le contrôle appelle sa procédure de césure lexicale pour récupérer les informations demandées.

Pour déterminer la ligne sur laquelle se trouve un caractère donné, vous pouvez utiliser le message [**em \_ EXLINEFROMCHAR**](em-exlinefromchar.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de contrôles RichEdit](using-rich-edit-controls.md)
</dt> <dt>

[Windows démonstration des contrôles communs (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 