---
title: Comment utiliser les opérations du presse-papiers RichEdit
description: Une application peut coller le contenu du presse-papiers dans un contrôle RichEdit en utilisant le format de presse-papiers le mieux disponible ou un format de presse-papiers spécifique.
ms.assetid: 1FEFFD95-839B-4A26-A26E-B8429D5FF4C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a46432054956914b484c9faeeeda78f2a18e132
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115357"
---
# <a name="how-to-use-rich-edit-clipboard-operations"></a>Comment utiliser les opérations du presse-papiers RichEdit

Une application peut coller le contenu du presse-papiers dans un contrôle RichEdit en utilisant le format de presse-papiers le mieux disponible ou un format de presse-papiers spécifique. Vous pouvez également déterminer si un contrôle RichEdit peut coller un format de presse-papiers.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="use-a-rich-edit-clipboard-operation"></a>Utilisation d’une opération RichEdit dans le presse-papiers

Comme avec un contrôle d’édition, vous pouvez copier ou couper le contenu de la sélection actuelle à l’aide du message de [**\_ copie WM**](/windows/desktop/dataxchg/wm-copy) ou de [**\_ Cut**](/windows/desktop/dataxchg/wm-cut) . De même, vous pouvez coller le contenu du presse-papiers dans un contrôle RichEdit en utilisant le message [**WM \_ Paste**](/windows/desktop/dataxchg/wm-paste) . Le contrôle colle le premier format disponible qu’il reconnaît, ce qui est vraisemblablement le format le plus descriptif.

Pour coller un format de presse-papiers spécifique, vous pouvez utiliser le message [**\_ PASTESPECIAL em**](em-pastespecial.md) . Ce message est utile pour les applications avec une commande **Collage spécial** qui permet à l’utilisateur de sélectionner le format du presse-papiers. Vous pouvez utiliser le message de la [**\_ CANPASTE em**](em-canpaste.md) pour déterminer si un format donné est reconnu par le contrôle.

Vous pouvez également utiliser le message de la [**\_ CANPASTE em**](em-canpaste.md) pour déterminer si un format de presse-papiers disponible est reconnu par un contrôle RichEdit. Ce message est utile lors du traitement du message [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) . Une application peut activer ou griser sa commande de **Collage** , selon que le contrôle peut coller n’importe quel format disponible.

Les contrôles RichEdit inscrivent deux formats de presse-papiers :

-   Format de texte enrichi
-   Format de texte enrichi sans objets
-   Texte et objets RichEdit

Une application peut inscrire ces formats à l’aide de la fonction [**RegisterClipboardFormat**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) , en spécifiant les \_ valeurs CF RTF, CF \_ RTFNOOBJS et CF \_ RETEXTOBJ.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de contrôles RichEdit](using-rich-edit-controls.md)
</dt> <dt>

[Windows démonstration des contrôles communs (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 