---
title: Comment redimensionner automatiquement les contrôles RichEdit
description: Une application peut redimensionner un contrôle RichEdit en fonction des besoins afin qu’elle ait toujours la même taille que son contenu.
ms.assetid: CCAFC039-AC9E-4BC4-ABE1-8C56FA9DD3F5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee9ead05c4c04526a9290dc115f7a2fa7741397
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031948"
---
# <a name="how-to-automatically-resize-rich-edit-controls"></a>Comment redimensionner automatiquement les contrôles RichEdit

Une application peut redimensionner un contrôle RichEdit en fonction des besoins afin qu’elle ait toujours la même taille que son contenu. Un contrôle Rich Edit prend en charge cette fonctionnalité dite « sans *bas* » en envoyant à sa fenêtre parente un code de notification en [ \_ REQUESTRESIZE](en-requestresize.md) chaque fois que la taille du contenu du contrôle change.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions

### <a name="automatically-resize-a-rich-edit-control"></a>Redimensionner automatiquement un contrôle RichEdit

Lors du traitement du code de notification en [ \_ REQUESTRESIZE](en-requestresize.md) , une application doit redimensionner le contrôle avec les dimensions de la structure [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) spécifiée. Une application peut également déplacer toutes les informations qui se trouvent près du contrôle afin de s’adapter aux changements de hauteur du contrôle. Pour redimensionner le contrôle, vous pouvez utiliser la fonction [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) .

Vous pouvez forcer un contrôle RichEdit sans fin pour envoyer un code de notification en [ \_ REQUESTRESIZE](en-requestresize.md) à l’aide du message [**em \_ REQUESTRESIZE**](em-requestresize.md) . Ce message peut être utile lors du traitement du message de [**\_ taille WM**](/windows/desktop/winmsg/wm-size) .

## <a name="remarks"></a>Notes

Pour recevoir les codes de notification en [ \_ REQUESTRESIZE](en-requestresize.md) , vous devez activer la notification à l’aide du message [em \_ SETEVENTMASK](em-seteventmask.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de contrôles RichEdit](using-rich-edit-controls.md)
</dt> <dt>

[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 