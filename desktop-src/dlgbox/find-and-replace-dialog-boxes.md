---
title: Boîtes de dialogue Rechercher et remplacer
description: Affiche une boîte de dialogue non modale qui permet à l’utilisateur de spécifier une chaîne à rechercher, ainsi que les options à utiliser lors de la recherche de texte dans un document.
ms.assetid: c8c035bf-795d-42a7-abc6-168dea43e6e9
keywords:
- Windows Interface utilisateur, entrée utilisateur
- Windows Interface utilisateur, bibliothèque de boîtes de dialogue communes
- entrée utilisateur, bibliothèque de boîtes de dialogue communes
- capture de l’entrée utilisateur, bibliothèque de boîtes de dialogue communes
- Bibliothèque de boîtes de dialogue communes
- boîtes de dialogue communes
- Rechercher (boîte de dialogue)
- Remplacer (boîte de dialogue)
- personnalisation de la boîte de dialogue Rechercher
- personnalisation de la boîte de dialogue remplacer
- boîtes de dialogue prédéfinies
- boîtes de dialogue, Rechercher
- boîtes de dialogue, remplacer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59bc5da5a8780a4f08bbf4bf757e1703d8d9120fdefe9d1730e515ffc6feae40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503484"
---
# <a name="find-and-replace-dialog-boxes"></a>Boîtes de dialogue Rechercher et remplacer

Affiche une boîte de dialogue non modale qui permet à l’utilisateur de spécifier une chaîne à rechercher, ainsi que les options à utiliser lors de la recherche de texte dans un document. La boîte de dialogue **remplacer** permet à l’utilisateur de spécifier une chaîne à rechercher et une chaîne de remplacement, ainsi que des options pour contrôler l’opération.

Vous créez et affichez une boîte de dialogue **Rechercher** en initialisant une structure [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) et en passant la structure à la fonction [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) . L’illustration suivante montre une boîte de dialogue de **recherche** classique.

![Rechercher, boîte de dialogue](images/finddialogboxxp.png)

Vous créez et affichez une boîte de dialogue **remplacer** en initialisant une structure [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) et en passant la structure à la fonction [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) . L’illustration suivante montre une boîte de dialogue **remplacer** classique.

![remplacer, boîte de dialogue](images/replacedialogboxxp.png)

Contrairement à d’autres boîtes de dialogue courantes, les boîtes de dialogue **Rechercher** et **remplacer** sont non modales. Une boîte de dialogue non modale permet à l’utilisateur de basculer entre la boîte de dialogue et la fenêtre qui l’A créée. Cela est utile pour permettre à l’utilisateur de rechercher une chaîne, de basculer vers la fenêtre d’application pour travailler sur la chaîne, puis de revenir à la boîte de dialogue pour rechercher une autre chaîne sans répéter la commande nécessaire pour ouvrir la boîte de dialogue.

Si la fonction [**TexteCherché**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) ou [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) crée correctement la boîte de dialogue, elle retourne un handle vers la boîte de dialogue. Vous pouvez utiliser ce handle pour déplacer et communiquer avec la boîte de dialogue. Si la fonction ne peut pas créer la boîte de dialogue, elle retourne la **valeur null**. Vous pouvez déterminer la cause d’une erreur en appelant la fonction [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) pour récupérer la valeur d’erreur étendue.

Cette section décrit les rubriques suivantes.

-   [Message enregistré FINDMSGSTRING](#the-findmsgstring-registered-message)
-   [Personnalisation de la boîte de dialogue Rechercher ou remplacer](#customizing-the-find-or-replace-dialog-box)

## <a name="the-findmsgstring-registered-message"></a>Message enregistré FINDMSGSTRING

Avant de créer une boîte de dialogue **Rechercher** ou **remplacer** , vous devez appeler la fonction [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) pour obtenir un identificateur de message pour le message [**FINDMSGSTRING**](findmsgstring.md) Registered. Vous pouvez ensuite utiliser l’identificateur pour détecter et traiter les messages envoyés à partir de la boîte de dialogue. Quand l’utilisateur clique sur le bouton **Rechercher suivant**, **remplacer** ou **remplacer tout** dans une boîte de dialogue, la procédure de la boîte de dialogue envoie un message **FINDMSGSTRING** à la procédure de fenêtre de la fenêtre propriétaire. Lorsque vous créez la boîte de dialogue, le membre **hwndOwner** de la structure [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) identifie la fenêtre propriétaire.

Le paramètre *lParam* d’un message [**FINDMSGSTRING**](findmsgstring.md) est un pointeur vers la structure [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) que vous avez spécifiée lors de la création de la boîte de dialogue. Avant d’envoyer le message, la boîte de dialogue définit les membres de cette structure avec la dernière entrée utilisateur, y compris la chaîne à rechercher, la chaîne de remplacement (le cas échéant) et les options de l’opération de recherche et remplacement.

Dans un message [**FINDMSGSTRING**](findmsgstring.md) , le membre **Flags** de la structure [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) comprend l’un des indicateurs suivants pour indiquer l’événement à l’origine du message.



| Indicateur               | Signification                                                                                                                                                                                                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_DIALOGTERM fr** | La boîte de dialogue se ferme. Une fois que la fenêtre propriétaire a traité ce message, un descripteur de la boîte de dialogue n’est plus valide.                                                                                    |
| **FR \_ TrouverSuivant**   | L’utilisateur a cliqué sur le bouton **suivant** de la boîte de dialogue **Rechercher** ou **remplacer** . Le membre **lpstrFindWhat** spécifie la chaîne à rechercher.                                                         |
| **r \_ remplacer**    | L’utilisateur a cliqué sur le bouton **remplacer** dans une boîte de dialogue **remplacer** . Le membre **lpstrFindWhat** spécifie la chaîne à remplacer et le membre **lpstrReplaceWith** spécifie la chaîne de remplacement.     |
| **FR \_ REPLACEALL** | L’utilisateur a cliqué sur le bouton **remplacer tout** dans une boîte de dialogue **remplacer** . Le membre **lpstrFindWhat** spécifie la chaîne à remplacer et le membre **lpstrReplaceWith** spécifie la chaîne de remplacement. |



 

Pour un message **suivant** ou **remplacer tout** , le membre **indicateurs** peut inclure n’importe quelle combinaison des indicateurs suivants pour indiquer les options de recherche.



| Indicateur              | Signification                                                                                                                                                                                                                                                                                          |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FR \_**      | Si cette option est définie, le bouton **bas** des cases d’option direction est sélectionné, ce qui indique que l’utilisateur souhaite effectuer une recherche à partir de l’emplacement actuel jusqu’à la fin du document. Si **fr \_** n’est pas défini, le bouton haut est sélectionné afin que l’utilisateur souhaite effectuer **une** recherche jusqu’au début du document.       |
| **FR \_ RespecterCasse** | Si cette option est définie, la case à cocher **respecter la casse** est activée, ce qui indique que l’utilisateur veut que la recherche respecte la casse. Si **fr \_ RespecterCasse** n’est pas défini, la case à cocher est désactivée afin que la recherche ne respecte pas la casse.                                                                       |
| **\_WHOLEWORD fr** | Si cette option est définie, la case à cocher **mot entier uniquement** est activée, ce qui indique que l’utilisateur souhaite rechercher uniquement les mots entiers qui correspondent à la chaîne recherchée. Si **fr \_ WHOLEWORD** n’est pas défini, la case à cocher est désactivée. par conséquent, vous devez également rechercher les fragments de mots qui correspondent à la chaîne recherchée. |



 

## <a name="customizing-the-find-or-replace-dialog-box"></a>Personnalisation de la boîte de dialogue Rechercher ou remplacer

Pour personnaliser une boîte de dialogue **Rechercher** ou **remplacer** , vous pouvez utiliser l’une des méthodes suivantes :

-   Spécifier des valeurs dans la structure [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) lorsque vous créez la boîte de dialogue
-   Fournir un modèle personnalisé
-   Fournir une procédure de raccordement

Lorsque vous créez une boîte de dialogue **Rechercher** ou **remplacer** , vous pouvez définir des indicateurs dans le membre **Flags** de la structure [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) pour masquer ou désactiver les contrôles d’option de recherche. Par exemple, vous pouvez définir l' \_ indicateur fr NOMATCHCASE pour désactiver la case à cocher **respecter la casse** ou définir l’indicateur fr \_ HIDEMATCHCASE pour le masquer.

Vous pouvez fournir un modèle personnalisé pour une boîte de dialogue **Rechercher** ou **remplacer** , par exemple, si vous souhaitez inclure des contrôles supplémentaires propres à votre application. Les fonctions [**TexteCherché**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) et [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) utilisent votre modèle personnalisé à la place du modèle par défaut.

**Pour fournir un modèle personnalisé pour une boîte de dialogue Rechercher ou remplacer**

1.  Créez le modèle personnalisé en modifiant le modèle par défaut spécifié dans le fichier TexteCherché. dlg. Les identificateurs de contrôle utilisés dans le modèle de boîte de dialogue **Rechercher** ou **remplacer** par défaut sont définis dans le fichier Dlgs. h.
2.  Utilisez la structure [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) pour activer le modèle comme suit :
    -   -   Si votre modèle personnalisé est une ressource d’une application ou d’une bibliothèque de liens dynamiques, définissez l' \_ indicateur fr ENABLETEMPLATE dans le membre **Flags** . Utilisez les membres **HINSTANCE** et **lpTemplateName** de la structure pour identifier le nom du module et de la ressource.

            Ou

        -   Si votre modèle personnalisé est déjà en mémoire, définissez l' \_ indicateur fr ENABLETEMPLATEHANDLE. Utilisez le membre **HINSTANCE** pour identifier l’objet mémoire qui contient le modèle.

Vous pouvez fournir une procédure de hook [**FRHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc) pour une boîte de dialogue **Rechercher** ou **remplacer** . La procédure de raccordement peut traiter les messages envoyés à la boîte de dialogue. Si vous utilisez un modèle personnalisé pour définir des contrôles supplémentaires, vous devez fournir une procédure de raccordement pour traiter l’entrée de vos contrôles.

**Pour activer une procédure de Hook pour une boîte de dialogue Rechercher ou remplacer**

1.  Définissez l' \_ indicateur fr ENABLEHOOK dans le membre **Flags** de la structure [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) .
2.  Spécifiez l’adresse de la procédure de raccordement dans le membre **lpfnHook** .

Après le traitement du message [**WM \_ INITDIALOG**](wm-initdialog.md) , la procédure de la boîte de dialogue envoie un message **WM \_ INITDIALOG** à la procédure de Hook. Le paramètre *lParam* de ce message est un pointeur vers la structure [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) utilisée pour initialiser la boîte de dialogue.

Si la procédure de hook retourne la **valeur false** en réponse au message [**WM \_ INITDIALOG**](wm-initdialog.md) , la boîte de dialogue ne s’affiche pas, sauf si la procédure de raccordement l’affiche. Pour ce faire, effectuez tout d’abord toutes les autres opérations de peinture, puis appelez les fonctions [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) et [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) . Le code suivant est fourni à titre d'exemple :


```
// We've returned FALSE in response to WM_INITDIALOG. 
// We've performed any other paint operations. 
// Now we display the dialog box. 
ShowWindow(hDlg, SW_SHOWNORMAL); 
UpdateWindow(hDlg); 
```



 

 