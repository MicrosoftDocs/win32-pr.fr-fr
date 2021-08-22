---
description: Vos applications peuvent utiliser les fonctions de l’API Uniscribe pour prendre en charge la typographie et l’affichage et la modification du texte international. Uniscribe utilise le paragraphe comme unité pour l’affichage du texte, et la fonctionnalité Uniscribe doit être utilisée pour le paragraphe entier.
ms.assetid: e1adc567-0445-4deb-8634-25653f82127c
title: Affichage de texte avec Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17caf7e7880a61bdf9afbaf6db5b60065b01d3d3960f2ed5629a007aa304b7b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949604"
---
# <a name="displaying-text-with-uniscribe"></a>Affichage de texte avec Uniscribe

Vos applications peuvent utiliser les fonctions de l’API Uniscribe pour prendre en charge la typographie et l’affichage et la modification du texte international. Uniscribe utilise le paragraphe comme unité pour l’affichage du texte, et la fonctionnalité Uniscribe doit être utilisée pour le paragraphe entier.

Lorsque vous utilisez Uniscribe pour l’affichage de texte, une application doit passer par un processus de mise en forme (« disposition »), généralement à l’aide de Uniscribe. L’application divise un paragraphe de texte en chaînes de caractères avec le même style, appelé « exécutions ». Le style est déterminé par l’implémentation particulière, mais il comprend généralement des attributs tels que la police, la taille et la couleur. Lors de la définition des exécutions, l’application peut également appliquer d’autres informations, telles que la langue et les données de paramètres régionaux, qui sont conservées pour une utilisation avec les outils lexicaux. Par exemple, une application peut traiter en tant qu’exécution distincte un passage dans un texte principalement anglais qui est rendu en français.

Une fois qu’elle a déterminé les exécutions de tous les paragraphes, l’application divise chaque paragraphe en chaînes ayant les mêmes script et direction (« items »). L’application applique les informations de l’élément pour produire des exécutions uniques dans le script et la direction et qui sont entièrement dans un seul élément (« Ranges »).

La répartition d’un élément en plages est quelque peu arbitraire, bien qu’une plage soit composée d’un ou plusieurs regroupements de caractères indivisibles définis par script consécutifs, appelés « clusters ». Pour les langues européennes, un cluster correspond généralement à un caractère de page de codes unique ou à un point de code Unicode, et se compose d’un seul [glyphe](uniscribe-glossary.md). Toutefois, dans les langages tels que le thaï, un cluster est un regroupement de glyphes et correspond à plusieurs caractères ou points de code consécutifs. Par exemple, un cluster thaï peut contenir une consonne, une voyelle et une marque de ton. Pour qu’il n’interrompe pas les clusters, l’application doit généralement utiliser les plages les plus longues qu’il peut ou utiliser ses propres informations lexicales pour s’arrêter entre des plages situées dans des endroits qui ne sont pas au milieu d’un cluster.

Lorsqu’il a identifié les clusters dans chaque plage, l’application doit déterminer la taille de chaque cluster. Elle utilise Uniscribe pour additionner les clusters afin de déterminer la taille de chaque plage. Ensuite, l’application additionne les tailles des plages jusqu’à ce qu’elles débordent une ligne, autrement dit, atteint la marge. La plage dépassant la ligne est divisée entre la ligne active et la ligne suivante. Pour chaque ligne, l’application crée une carte à partir de la position visuelle à la position logique pour chaque plage. L’application forme ensuite les points de code de chaque plage en glyphes, qu’il est possible de positionner et de restituer par la suite.

Une application n’effectue une mise en page de texte qu’une seule fois. Par la suite, il enregistre les glyphes et les positions à des fins d’affichage, ou il les génère chaque fois qu’il affiche le texte, ce qui représente un compromis entre la vitesse et la mémoire. Une application classique implémente le processus de disposition une seule fois, puis génère les glyphes et les positions chaque fois qu’il affiche le texte.

Une application qui utilise des [scripts complexes](uniscribe-glossary.md) présente les problèmes suivants avec une approche simple de la disposition et de l’affichage.

-   La largeur d’un caractère de script complexe dépend de son contexte. Il n’est pas possible d’enregistrer les largeurs dans des tables simples.
-   L’interruption entre les mots dans des scripts tels que le thaï requiert la prise en charge du dictionnaire. Par exemple, aucun caractère de séparation n’est utilisé entre les mots thaï.
-   L’arabe, l’hébreu, le persan, l’ourdou et d’autres langages de [texte bidirectionnel](uniscribe-glossary.md) nécessitent une réorganisation avant l’affichage.
-   Une certaine forme d’association de polices est souvent nécessaire pour utiliser facilement des scripts complexes.

Le fait que Uniscribe utilise le paragraphe comme unité d’affichage permet à l’application de traiter correctement ces problèmes de script complexes.

> [!Note]  
> Uniscribe doit être utilisé pour un paragraphe entier, même si les sections du paragraphe ne sont pas des scripts complexes.

 

Comme indiqué dans le tableau suivant, Uniscribe version 1,6 ou ultérieure prend en charge plusieurs fonctions qui tirent parti des balises OpenType. Elles peuvent être remplacées par les fonctions Uniscribe régulières correspondantes. En général, vos applications doivent fonctionner entièrement avec les fonctions d’un jeu ou de l’autre, et ne doivent pas essayer de « mélanger et faire correspondre » aux fonctions.



| Fonction Uniscribe normale             | Fonction OpenType équivalente                           |
|----------------------------------------|--------------------------------------------------------|
| [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) | [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype) |
| [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)     | [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)     |
| [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)     | [**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)     |



 

## <a name="lay-out-text-using-uniscribe"></a>Disposition du texte à l’aide de Uniscribe

Votre application peut utiliser les étapes suivantes pour mettre en page un paragraphe de texte avec Uniscribe. Cette procédure suppose que l’application a déjà divisé le paragraphe en exécutions.

1.  Appelez [**ScriptRecordDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptrecorddigitsubstitution) uniquement lors du démarrage ou de la réception d’un message [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) .
2.  Facultatif Appelez [**ScriptIsComplex**](/windows/desktop/api/Usp10/nf-usp10-scriptiscomplex) pour déterminer si le paragraphe requiert un traitement complexe.
3.  Facultatif Si vous utilisez Uniscribe pour gérer le texte bidirectionnel et/ou la substitution de chiffres, appelez [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) pour préparer [**le \_ contrôle de script**](/windows/win32/api/usp10/ns-usp10-script_control) et les structures d' [**\_ État de script**](/windows/win32/api/usp10/ns-usp10-script_state) comme entrées à [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize). Si vous ignorez cette étape, mais que vous avez toujours besoin d’une substitution de chiffre, substituez les chiffres nationaux pour Unicode U + 0030 à U + 0039 (chiffres européens). Pour plus d’informations sur la substitution de chiffres, consultez [Shape digits](digit-shapes.md).
4.  Appelez [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) pour diviser le paragraphe en éléments. Si vous n’utilisez pas Uniscribe pour la substitution de chiffres et que l’ordre bidirectionnel est connu, par exemple en raison de la disposition du clavier utilisée pour entrer le caractère, appelez **ScriptItemize**. Dans l’appel, fournissez des pointeurs null pour le [**\_ contrôle de script**](/windows/win32/api/usp10/ns-usp10-script_control) et les structures d' [**\_ État de script**](/windows/win32/api/usp10/ns-usp10-script_state) . Cette technique génère des éléments en utilisant uniquement le moteur de mise en forme, et les éléments peuvent être réorganisés à l’aide des informations du moteur.
    > [!Note]  
    > En règle générale, les applications qui fonctionnent uniquement avec des scripts de gauche à droite et sans substitution de chiffres doivent passer des pointeurs null pour le [**\_ contrôle de script**](/windows/win32/api/usp10/ns-usp10-script_control) et les structures d' [**\_ État de script**](/windows/win32/api/usp10/ns-usp10-script_state) .

     

5.  Fusionnez les informations d’élément avec les informations d’exécution pour produire des plages.
6.  Appelez [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) pour identifier les clusters et générer des glyphes.
7.  Si [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) retourne le code USP \_ E \_ script \_ n’est pas \_ dans \_ la police ou S \_ OK avec la sortie contenant des glyphes manquants, sélectionnez les caractères d’une autre police. Remplacez une autre police ou désactivez la mise en forme en affectant la valeur non définie au membre **escript** de la structure d' [**\_ analyse de script**](/windows/win32/api/usp10/ns-usp10-script_analysis) passée à **ScriptShape** \_ . Pour plus d’informations, consultez Utilisation de la [police de secours](using-font-fallback.md).
8.  Appelez [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) pour générer des [largeurs d’avance](uniscribe-glossary.md) et des positions x et y pour les glyphes de chaque plage consécutive. Il s’agit de la première étape pour laquelle la taille du texte est prise en compte.
9.  Additionner les tailles de plage jusqu’à ce que la ligne déborde.
10. Rompez la plage sur une limite de mot en utilisant les membres **fSoftBreak** et **fWhiteSpace** dans les attributs logiques. Pour arrêter un seul cluster de caractères en dehors de l’exécution, utilisez les informations retournées en appelant [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).
    > [!Note]  
    > Déterminez si le premier point de code d’une plage doit être un point d’arrêt de mot car le dernier caractère de la plage précédente l’exige. Par exemple, si une plage se termine par une virgule, considérez le premier caractère de la plage suivante comme un point d’arrêt de mot.

     

11. Répétez les étapes 6 à 10 pour chaque ligne du paragraphe. Toutefois, si vous rompez la dernière exécution sur la ligne, appelez [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) pour mettre en forme la partie restante de l’exécution en tant que première exécution sur la ligne suivante.

## <a name="display-text-using-uniscribe"></a>Afficher le texte à l’aide de Uniscribe

Votre application peut utiliser les étapes suivantes pour afficher un paragraphe de texte. Cette procédure suppose que l’application a déjà disposé le texte et n’a pas enregistré les glyphes et les positions du processus de disposition. Si la vitesse est un problème, l’application peut enregistrer les glyphes et les positions de la procédure de disposition et démarrer à l’étape 2 dans la procédure d’affichage.

> [!Note]  
> L’application peut omettre l’étape 2 si le texte ne contient pas de caractères de scripts de droite à gauche, ne contient pas de caractères de contrôle bidirectionnels et utilise un niveau d’incorporation de base de gauche à droite.

 

1.  Pour chaque exécution, procédez comme suit :
    1.  Si le style a changé depuis la dernière exécution, mettez à jour le handle vers le contexte de périphérique en le relâchant et en le réobtenant.
    2.  Appelez [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) pour générer des glyphes pour l’exécution.
    3.  Appelez [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) pour générer une largeur avancée et un décalage x, y pour chaque glyphe.
2.  Procédez comme suit pour établir l’ordre visuel correct des exécutions dans la ligne :
    1.  Extrayez un tableau de [niveaux d’incorporation](uniscribe-glossary.md)bidirectionnels, un par plage. Le niveau d’incorporation est donné par (élément de SCRIPT \_ ) si. ( SCRIPT \_ Analysis) a. (SCRIPT \_ STATE) s. uBidiLevel.
    2.  Transmettez ce tableau à [**ScriptLayout**](/windows/desktop/api/Usp10/nf-usp10-scriptlayout) pour générer une carte des positions visuelles à des positions logiques.
3.  Facultatif Pour justifier le texte, appelez [**ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify) ou utilisez une connaissance spécialisée du texte.
4.  Utilisez la carte Visual-to-Logical pour afficher les exécutions dans l’ordre visuel. À partir de l’extrémité gauche de la ligne, appelez [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) pour afficher l’exécution fournie par la première entrée de la carte. Pour chaque entrée suivante dans le mappage, appelez **ScriptTextOut** pour afficher l’exécution indiquée à droite de la série précédemment affichée.

    Si vous omettez l’étape 2, commencez à l’extrémité gauche de la ligne et appelez [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) pour afficher la première exécution logique, puis pour afficher chaque exécution logique à droite de l’exécution précédente.

5.  Répétez les étapes ci-dessus pour toutes les lignes du paragraphe.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 
