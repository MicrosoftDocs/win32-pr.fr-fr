---
description: Le contrôle InkEdit offre un moyen simple de capturer, reconnaître et afficher de l’encre.
ms.assetid: a1dfa254-cade-44c5-8fdd-74bb40849063
title: InkEdit, contrôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fa64c4452ba5d7f66cdc03a1148c02a12f3945f876d68ac240ff4473e8d50bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451320"
---
# <a name="inkedit-control"></a>InkEdit, contrôle

Le contrôle [InkEdit](inkedit-control-reference.md) offre un moyen simple de capturer, reconnaître et afficher de l’encre.

Cette implémentation du contrôle [InkEdit](inkedit-control-reference.md) est basée sur le contrôle [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) . l’implémentation managée (.NET Framework) de [InkEdit](/previous-versions/ms835842(v=msdn.10)) est basée sur le contrôle [**RichTextBox**](/previous-versions/windows/) .

L’objectif principal du contrôle [InkEdit](inkedit-control-reference.md) est de collecter l’encre, de la reconnaître et de l’afficher sous forme de texte. En outre, il prend en charge l’affichage de l’encre comme un objet incorporé avec des fonctionnalités de mise en forme du texte, telles que le gras et le soulignement.

## <a name="gestures-and-correction"></a>Mouvements et correction

[InkEdit](inkedit-control-reference.md) prend en charge les gestes suivants.



| Mouvement                                                                    | Nom du geste              | Action               |
|----------------------------------------------------------------------------|---------------------------|----------------------|
| ![geste vers le gauche](images/d8b00c0a-f450-4f71-980f-3bca1b558e4c.gif)      | Vers le gauche<br/>      | Entrez<br/>     |
| ![geste vers le long-gauche-long](images/b8cb23b5-b947-477d-922f-2ffb42756804.gif) | En baisse à gauche<br/> | Entrez<br/>     |
| ![geste vers le haut](images/02c34d24-c2d7-404f-b99a-742ba6de7f0c.gif)       | En haut à droite<br/>       | Onglet<br/>       |
| ![geste vers le haut à droite.](images/5e3522d3-2920-4a86-86ae-f29b01d93993.gif) | Up-Right-long<br/>  | Onglet<br/>       |
| ![mouvement de droite](images/864cf4e1-2619-49cf-ac96-72994232e465.jpg)          | Right<br/>          | Espace<br/>     |
| ![mouvement de gauche](images/ce60cc20-1769-428d-80de-7f47c86021fb.jpg)           | Gauche<br/>           | Retour arrière<br/> |



 

Les événements de mouvement que vous pouvez gérer contiennent des informations de mouvement, de trait et de curseur que vous pouvez utiliser pour envoyer du texte à [InkEdit](inkedit-control-reference.md) ou placer des données dans le presse-papiers.

[InkEdit](inkedit-control-reference.md) fournit également une interface utilisateur de correction qui permet aux utilisateurs d’afficher et de sélectionner parmi d’autres, d’utiliser le clavier visuel et les détecteurs de caractères/lettres/bloc.

## <a name="other-details"></a>Autres détails

[InkEdit](inkedit-control-reference.md) est conçu pour fonctionner correctement dans un scénario de formulaire pour une ligne unique, ainsi que pour la saisie et la modification de texte multiligne. L’utilisation principale prévue pour InkEdit consiste à obtenir la saisie de texte d’un utilisateur sous la forme d’une écriture manuscrite. Par défaut, l’entrée manuscrite est reconnue et le texte est inséré à la place. L’interface utilisateur par défaut pour InkEdit ressemble à celle du contrôle [**RichTextBox**](/previous-versions/windows/) , sauf lorsque l’utilisateur fixe une entrée manuscrite. Vous pouvez afficher l’encre d’origine plutôt que le texte. Toutefois, l’encre est mise à l’échelle en fonction de la taille actuelle de la police d’entrée du contrôle InkEdit et s’affiche en ligne avec un autre texte.

> [!Note]  
> Pour des raisons de sécurité, vous devez utiliser des procédures standard pour ouvrir ou fermer un fichier, diffuser en continu l’entrée/sortie et définir la propriété [**RTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) ou [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) .

 

Le contrôle [InkEdit](inkedit-control-reference.md) est défini pour reconnaître l’entrée manuscrite comme texte par défaut. Pour permettre aux utilisateurs d’ajouter de l’encre comme entrée manuscrite, affectez à la propriété [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) la valeur **InsertAsInk**.

Pour obtenir des informations de référence détaillées sur le contrôle [InkEdit](inkedit-control-reference.md) , consultez InkEdit.

> [!Note]  
> Si vous utilisez le contrôle [InkEdit](inkedit-control-reference.md) Win32 et le placez à l’intérieur d’une zone de groupe, assurez-vous que la zone a un style transparent ; dans le cas contraire, InkEdit n’est pas en mesure de collecter l’encre.

 

> [!Note]  
> Pour vous assurer que l’entrée manuscrite est correctement affichée, appelez la méthode d' [**actualisation**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh) du contrôle [InkEdit](inkedit-control-reference.md) lorsqu’elle reçoit un événement [**HScroll**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1) ou [**VScroll**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1) .

 

Les sections suivantes détaillent l’utilisation du contrôle [InkEdit](inkedit-control-reference.md) :

-   [Instanciation de InkEdit](instantiating-inkedit.md)
-   [Word et reconnaissance de caractères](word-vs--character-recognition.md)
-   [Affichage de l’encre sous forme d’encre](displaying-ink-as-ink.md)
-   [Utilisation d’InkEdit sur les versions antérieures de Windows](using-inkedit-on-earlier-versions-of-windows.md)
-   [Utilisation d’un dictionnaire d’applications avec InkEdit](using-an-application-dictionary-with-inkedit.md)

 

