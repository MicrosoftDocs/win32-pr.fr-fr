---
title: Comment utiliser les codes de notification de contrôle RichEdit
description: La fenêtre parente d’un contrôle RichEdit peut traiter les codes de notification pour surveiller les événements qui affectent le contrôle. Les contrôles RichEdit prennent en charge tous les codes de notification utilisés avec les contrôles d’édition, ainsi que plusieurs autres.
ms.assetid: E045EADE-CB37-492A-85EC-6CF236677F08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68e510bf7c5abe6109862a01d8926c8956736f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115361"
---
# <a name="how-to-use-rich-edit-control-notification-codes"></a>Comment utiliser les codes de notification de contrôle RichEdit

La fenêtre parente d’un contrôle RichEdit peut traiter les codes de notification pour surveiller les événements qui affectent le contrôle. Les contrôles RichEdit prennent en charge tous les codes de notification utilisés avec les contrôles d’édition, ainsi que plusieurs autres.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="use-a-rich-edit-control-notification-code"></a>Utiliser un code de notification Rich Edit Control

Vous pouvez déterminer les codes de notification qu’un contrôle RichEdit envoie à sa fenêtre parente en définissant son masque d’événement. Pour définir le masque d’événement pour un contrôle RichEdit, utilisez le message [**em \_ SETEVENTMASK**](em-seteventmask.md) . Vous pouvez récupérer le masque d’événement actuel d’un contrôle RichEdit à l’aide du message [**em \_ GETEVENTMASK**](em-geteventmask.md) . Pour obtenir la liste des indicateurs de masque d’événement, consultez [indicateurs de masque d’événement de contrôle RichEdit](rich-edit-control-event-mask-flags.md).

La fenêtre parente d’un contrôle RichEdit peut filtrer toutes les entrées du clavier et de la souris dans le contrôle en traitant le code de notification en [ \_ msgfilter](en-msgfilter.md) . La fenêtre parente peut empêcher le traitement du message clavier ou de la souris, ou peut modifier le message en modifiant la structure [**msgfilter**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) spécifiée.

Une application peut traiter le code de notification en [ \_ protégé](en-protected.md) pour détecter quand l’utilisateur tente de modifier du texte protégé. Pour marquer une plage de texte comme protégée, vous pouvez définir l’effet de caractère protégé.

Vous pouvez autoriser l’utilisateur à déposer des fichiers dans un contrôle Rich Edit en traitant le code de notification en [ \_ DROPFILES](en-dropfiles.md) . La structure [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) spécifiée contient des informations sur les fichiers en cours de suppression.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de contrôles RichEdit](using-rich-edit-controls.md)
</dt> <dt>

[Windows démonstration des contrôles communs (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




