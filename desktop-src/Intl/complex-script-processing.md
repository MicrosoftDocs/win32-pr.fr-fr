---
description: 'Vous trouverez ci-dessous des options pour l’affichage et le traitement associé du texte afin de prendre en charge des effets de typographie fine ou des scripts complexes : Text functionsEdit controlsRich Edit controlsUniscribe'
ms.assetid: 337bc798-e75d-4389-8fea-577eb82a0ed5
title: Traitement de script complexe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e4be6295bff949c8e29036ef3af496c673575e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542945"
---
# <a name="complex-script-processing"></a>Traitement de script complexe

Vous trouverez ci-dessous des options pour l’affichage et le traitement associé du texte afin de prendre en charge des effets de typographie fine ou des scripts complexes :

-   Fonctions de texte
-   Contrôles d’édition
-   Contrôles RichEdit
-   Uniscribe

Les options que vous choisissez dépendent des facteurs suivants :

-   Type de texte ou de scripts.
-   Le modèle d’implémentation, par exemple, la disposition du texte et la gestion du saut de ligne par l’application.
-   Mise à jour d’une application existante par rapport à la création d’une nouvelle application.

En général, une application qui effectue un traitement de script relativement simple peut choisir n’importe quelle option pour traiter des scripts complexes. Toutefois, pour un contrôle plus complet du traitement complexe des scripts, Uniscribe est recommandé.

## <a name="complex-script-processing-using-text-functions"></a>Traitement de script complexe à l’aide de fonctions de texte

Les applications qui utilisent essentiellement du texte brut, autrement dit, du texte qui utilise la même police, le même poids, la même couleur, etc., ont traditionnellement écrit du texte et des longueurs de lignes mesurées à l’aide de fonctions de texte standard, telles que [**TextOut**](/windows/win32/api/wingdi/nf-wingdi-textouta), [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)et [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa). Ces fonctions prennent en charge le traitement des scripts complexes et des effets de typographie fine. Pour plus d’informations, consultez [polices et texte](../gdi/fonts-and-text.md).

En général, la prise en charge du texte standard est transparente pour les applications qui traitent des scripts complexes. Toutefois, vous devez connaître certaines règles spécifiques à suivre pour écrire des applications qui prennent en charge la typographie fine et traiter des scripts complexes :

-   Votre application doit enregistrer des caractères dans une mémoire tampon et afficher une ligne entière de texte à la fois au lieu de, par exemple, en appelant [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) sur chaque caractère au fur et à mesure qu’elle est tapée par l’utilisateur. Ce mécanisme permet aux modules de mise en forme de texte avancés d’utiliser le contexte pour réorganiser et générer correctement les [glyphes](uniscribe-glossary.md) .
-   L’application doit utiliser [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) pour déterminer la longueur de ligne, au lieu de calculer les longueurs de ligne à partir des largeurs de caractères mises en cache, car la largeur d’un glyphe peut varier en fonction du contexte.
-   L’application doit éventuellement ajouter une prise en charge pour l’ordre de lecture de droite à gauche et l’alignement à droite.
-   La réorganisation et le traitement contextuel requis pour les scripts complexes ou la typographie fine nécessitent une augmentation significative du traitement par rapport à l’affichage de texte de base pour les scripts simples. Par conséquent, pour éviter les problèmes de performances, votre application ne doit pas traiter de grandes quantités de texte avant d’afficher les résultats et de retourner le contrôle à l’utilisateur.

## <a name="complex-script-processing-using-edit-controls"></a>Traitement de scripts complexes à l’aide de contrôles d’édition

Les contrôles d’édition Windows standard ont été étendus pour prendre en charge le texte multilingue et les scripts complexes. La prise en charge étendue comprend l’entrée et l’affichage, ainsi que le déplacement du curseur sur les clusters de caractères, par exemple, dans les scripts thaï et DÉVANÂGARÎ. Pour plus d’informations, consultez [modifier des contrôles](../controls/edit-controls.md).

## <a name="complex-script-processing-using-rich-edit-controls"></a>Traitement de scripts complexes à l’aide de contrôles RichEdit

La modification enrichie 3,0 est une collection d’interfaces de niveau supérieur qui tire parti de Uniscribe pour isoler les applications de disposition du texte de la complexité de certains scripts. L’édition enrichie est le moyen le plus simple pour les applications d’afficher des scripts complexes, même si leur objectif principal n’est pas nécessairement la disposition du texte. La modification enrichie fournit une édition rapide et polyvalente de texte enrichi Unicode et de texte brut simple. Il comprend une grande quantité de messages et d’interfaces COM, l’édition de texte, la mise en forme, le saut de ligne, la disposition de tableau simple, la disposition de texte verticale, la disposition de texte bidirectionnel, la prise en charge Indo-aryen et thaï, une interface utilisateur de modification similaire à Microsoft Word et les interfaces de modèle d’objet de texte.

Avec les interfaces RichEdit, les applications peuvent utiliser la fonction Rich Edit [**TextOut**](/windows/win32/api/wingdi/nf-wingdi-textouta) pour analyser, mettre en forme, positionner et rompre automatiquement les lignes. Pour plus d’informations, consultez [contrôles RichEdit](../controls/rich-edit-controls.md).

## <a name="complex-script-processing-using-uniscribe"></a>Traitement de scripts complexes à l’aide de Uniscribe

[Uniscribe](uniscribe.md) fournit la prise en charge la plus complète du traitement de texte impliquant des effets de typographie fine et des scripts complexes. Il prend en charge les règles complexes trouvées dans des scripts tels que l’arabe, le DÉVANÂGARÎ et le thaï. Il gère les scripts écrits de droite à gauche, tels que l’arabe et l’hébreu, et prend en charge le mélange de scripts. Uniscribe expose également les fonctionnalités de police [OpenType](opentype-font-format.md) qui peuvent être utilisées par les applications pour contrôler les effets de typographie fine. Pour plus d’informations, consultez [traitement de scripts complexes](processing-complex-scripts.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de Uniscribe](about-uniscribe.md)
</dt> <dt>

[Traitement de scripts complexes](processing-complex-scripts.md)
</dt> </dl>

 

 
