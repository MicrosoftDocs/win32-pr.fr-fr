---
title: Comment personnaliser les barres d’outils
description: la plupart des applications basées sur les Windows utilisent des contrôles de barre d’outils pour fournir aux utilisateurs un accès pratique aux fonctionnalités du programme.
ms.assetid: 0CE2988E-D887-433B-BFB2-5F3442E8E1B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f098880676fc0404df2a68694dc80b8601c21926d94ff594029321bafb1528a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929543"
---
# <a name="how-to-customize-toolbars"></a>Comment personnaliser les barres d’outils

la plupart des applications basées sur les Windows utilisent des contrôles de barre d’outils pour fournir aux utilisateurs un accès pratique aux fonctionnalités du programme. Toutefois, les barres d’outils statiques présentent quelques lacunes, par exemple un espace trop faible pour afficher efficacement tous les outils disponibles. La solution à ce problème consiste à rendre les barres d’outils de votre application personnalisables. Ensuite, les utilisateurs peuvent choisir d’afficher uniquement les outils dont ils ont besoin, et ils peuvent les organiser d’une manière adaptée à leur mode de traitement personnel.

> [!Note]  
> Les barres d’outils des boîtes de dialogue ne peuvent pas être personnalisées.

 

Pour activer la personnalisation, incluez l’indicateur de style de contrôles communs [**CCS \_ ajustables**](common-control-styles.md) lors de la création du contrôle de barre d’outils. Il existe deux approches de base pour la personnalisation :

-   La boîte de dialogue Personnalisation. Cette boîte de dialogue fournie par le système est l’approche la plus simple. Il fournit aux utilisateurs une interface utilisateur graphique qui leur permet d’ajouter, de supprimer ou de déplacer des icônes.
-   Glisser-déplacer des outils. L’implémentation de la fonctionnalité glisser-déplacer permet aux utilisateurs de déplacer des outils vers un autre emplacement de la barre d’outils ou de les supprimer en les faisant glisser en dehors de la barre d’outils. Il fournit aux utilisateurs un moyen simple et rapide d’organiser leur barre d’outils, mais ne les autorise pas à ajouter des outils.

Vous pouvez implémenter l’une ou l’autre approche, ou les deux, selon les besoins de l’application. Aucune de ces deux approches de la personnalisation ne fournit un mécanisme intégré, tel qu’un bouton Annuler ou annuler, pour ramener la barre d’outils à son état précédent. Vous devez utiliser explicitement l’API de contrôle ToolBar pour stocker l’état de prépersonnalisation de la barre d’outils. Si nécessaire, vous pouvez utiliser ces informations stockées ultérieurement pour rétablir l’état d’origine de la barre d’outils.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="customization-dialog-box"></a>Boîte de dialogue Personnalisation

La boîte de dialogue Personnalisation est fournie par le contrôle ToolBar pour offrir aux utilisateurs un moyen simple d’ajouter, de déplacer ou de supprimer des outils. Les utilisateurs peuvent le lancer en double-cliquant sur la barre d’outils. Les applications peuvent lancer la boîte de dialogue de personnalisation par programmation en envoyant au contrôle de barre d’outils un message de [**\_ personnalisation to**](tb-customize.md) .

L’illustration suivante montre un exemple de la boîte de dialogue Personnalisation de la barre d’outils.

![capture d’écran d’une fenêtre avec une barre d’outils à trois éléments et une boîte de dialogue avec des listes des boutons disponibles et de la barre d’outils actuelle](images/tb-customdlg.png)

Les outils de la zone de liste située à droite sont ceux qui se trouvent actuellement dans la barre d’outils. Au départ, cette liste contient les outils que vous spécifiez lors de la création de la barre d’outils. La zone de liste située à gauche contient les outils qui peuvent être ajoutés à la barre d’outils. Votre application est chargée de remplir cette liste (à l’exception du séparateur, qui apparaît automatiquement).

Le contrôle ToolBar informe votre application qu’elle lance une boîte de dialogue de personnalisation en envoyant sa fenêtre parente un code de notification [TBN \_ BEGINADJUST](tbn-beginadjust.md) suivi d’un code de notification [TBN \_ INITCUSTOMIZE](tbn-initcustomize.md) . Dans la plupart des cas, l’application n’a pas besoin de répondre à ces codes de notification. Toutefois, si vous ne souhaitez pas que la boîte de dialogue Personnaliser la barre d’outils affiche un bouton aide, gérez TBN \_ INITCUSTOMIZE en retournant TBNRF \_ HIDEHELP.

Le contrôle ToolBar collecte ensuite les informations dont il a besoin pour initialiser la boîte de dialogue en envoyant trois séries de codes de notification, dans l’ordre suivant :

-   Un code de notification [TBN \_ QUERYINSERT](tbn-queryinsert.md) pour chaque bouton de la barre d’outils pour déterminer où les boutons peuvent être insérés. Retourne **false** pour empêcher l’insertion d’un bouton à gauche du bouton spécifié dans le message de notification. Si vous renvoyez la **valeur false** à tous les \_ codes de notification TBN QUERYINSERT, la boîte de dialogue ne s’affichera pas.
-   Un code de notification [TBN \_ QUERYDELETE](tbn-querydelete.md) pour chaque outil qui se trouve actuellement dans la barre d’outils. Retourne la **valeur true** si un outil peut être supprimé ou **false** dans le cas contraire.
-   Une série de codes de notification [ \_ GETBUTTONINFO TBN](tbn-getbuttoninfo.md) pour renseigner la liste des boutons disponibles. Pour ajouter un bouton à la liste, remplissez la structure [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) qui est transmise avec le code de notification et renvoyez **true**. Si vous n’avez plus d’outils à ajouter, retournez la **valeur false**. Notez que vous pouvez retourner des informations pour les boutons qui se trouvent déjà dans la barre d’outils ; Ces boutons ne sont pas ajoutés à la liste.

La boîte de dialogue est ensuite affichée et l’utilisateur peut commencer à personnaliser la barre d’outils.

Quand la boîte de dialogue est ouverte, votre application peut recevoir un grand nombre de codes de notification, en fonction des actions de l’utilisateur :

-   [TBN \_ QUERYINSERT](tbn-queryinsert.md). L’utilisateur a modifié l’emplacement d’un outil sur la barre d’outils ou a ajouté un outil. Retourne **false** pour empêcher l’insertion de l’outil à cet emplacement.
-   [TBN \_ DELETINGBUTTON](tbn-deletingbutton.md). L’utilisateur est sur le paragraphe de supprimer un outil de la barre d’outils.
-   [TBN \_ CUSTHELP](tbn-custhelp.md). L’utilisateur a cliqué sur le bouton aide.
-   [TBN \_ TOOLBARCHANGE](tbn-toolbarchange.md). L’utilisateur a ajouté, déplacé ou supprimé un outil.
-   [TBN \_ Réinitialisez](tbn-reset.md). L’utilisateur a cliqué sur le bouton Réinitialiser.

Une fois la boîte de dialogue détruite, votre application reçoit un code de notification [TBN \_ ENDADJUST](tbn-endadjust.md) .

L’exemple de code suivant montre une façon d’implémenter la personnalisation de la barre d’outils.


```C++
// The buttons are stored in an array of TBBUTTON structures. 
//
// Constants such as STD_FILENEW are identifiers for the 
// built-in bitmaps that have already been assigned as the toolbar's 
// image list.
//
// Constants such as IDM_NEW are application-defined command identifiers.

TBBUTTON allButtons[] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"New" },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Open"},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Save"},
        { MAKELONG(STD_CUT,      ImageListID), IDM_CUT,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Cut" },
        { MAKELONG(STD_COPY,     ImageListID), IDM_COPY,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Copy"},
        { MAKELONG(STD_PASTE,    ImageListID), IDM_PASTE, TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Paste"}
    };

// The following appears in the window's message handler.

case WM_NOTIFY: 
    {
        switch (((LPNMHDR)lParam)->code) 
        {
        
        case TBN_GETBUTTONINFO:  
            {
                LPTBNOTIFY lpTbNotify = (LPTBNOTIFY)lParam;

                // Pass the next button from the array. There is no need to filter out buttons
                // that are already used—they will be ignored.
                
                int buttonCount = sizeof(allButtons) / sizeof(TBBUTTON);
                
                if (lpTbNotify->iItem < buttonCount)
                {
                    lpTbNotify->tbButton = allButtons[lpTbNotify->iItem];
                    return TRUE;
                }
                
                else
                
                {
                    return FALSE;  // No more buttons.
                }
            }
            
            break;

            case TBN_QUERYINSERT:
            
            case TBN_QUERYDELETE:
                return TRUE; 
        }
    }
```



### <a name="dragging-and-dropping-tools"></a>Glisser-déplacer des outils

Les utilisateurs peuvent également réorganiser les boutons d’une barre d’outils en appuyant sur la touche Maj et en faisant glisser le bouton vers un autre emplacement. Le processus de glisser-déplacer est géré automatiquement par le contrôle ToolBar. Elle affiche une image fantôme du bouton au fur et à mesure de son déplacement, puis réorganise la barre d’outils après qu’elle a été supprimée. Les utilisateurs ne peuvent pas ajouter de boutons de cette manière, mais ils peuvent supprimer un bouton en le supprimant de la barre d’outils.

Bien que le contrôle ToolBar effectue normalement cette opération automatiquement, il envoie également votre application deux codes de notification : [TBN \_ QUERYDELETE](tbn-querydelete.md) et [TBN \_ QUERYINSERT](tbn-queryinsert.md). Pour contrôler le processus de glisser-déplacer, gérez ces codes de notification comme suit :

-   Le code de notification [TBN \_ QUERYDELETE](tbn-querydelete.md) est envoyé dès que l’utilisateur tente de déplacer le bouton, avant l’affichage du bouton fantôme. Retourne **false** pour empêcher le déplacement du bouton. Si vous renvoyez la **valeur true**, l’utilisateur sera en mesure de déplacer l’outil ou de le supprimer en le supprimant de la barre d’outils. Si un outil peut être déplacé, il peut être supprimé. Toutefois, si l’utilisateur supprime un outil, le contrôle de barre d’outils envoie à votre application un code de notification [TBN \_ DELETINGBUTTON](tbn-deletingbutton.md) , auquel vous pouvez choisir de réinsérer le bouton à son emplacement d’origine, annulant ainsi la suppression.
-   Le code de notification [TBN \_ QUERYINSERT](tbn-queryinsert.md) est envoyé lorsque l’utilisateur tente de déposer le bouton dans la barre d’outils. Pour éviter que le bouton déplacé à gauche du bouton spécifié dans la notification, retourne **false**. Ce code de notification n’est pas envoyé si l’utilisateur dépose l’outil en dehors de la barre d’outils.

Si l’utilisateur tente de faire glisser un bouton sans également appuyer sur la touche Maj, le contrôle ToolBar ne gère pas l’opération de glisser-déplacer. Toutefois, il enverra à votre application un code de notification [TBN \_ BEGINDRAG](tbn-begindrag.md) pour indiquer le début d’une opération glisser et un code de notification [TBN \_ ENDDRAG](tbn-enddrag.md) pour indiquer la fin. Si vous souhaitez activer cette forme de glisser-déplacer, votre application doit gérer ces codes de notification, fournir l’interface utilisateur nécessaire et modifier la barre d’outils pour refléter les modifications apportées.

### <a name="saving-and-restoring-toolbars"></a>Enregistrement et restauration des barres d’outils

Dans le processus de personnalisation d’une barre d’outils, votre application peut avoir besoin d’enregistrer des informations pour vous permettre de restaurer la barre d’outils à son état d’origine. Pour lancer l’enregistrement ou la restauration d’un état de barre d’outils, envoyez au contrôle de barre d’outils un message [**\_ SAVERESTORE to**](tb-saverestore.md) avec *lParam* défini sur **true**. La valeur *lParam* de ce message spécifie si vous demandez une opération d’enregistrement ou de restauration. Une fois le message envoyé, il existe deux façons de gérer l’opération d’enregistrement et de restauration :

-   Avec les contrôles communs [version 4,72](common-control-versions.md) et antérieures, vous devez implémenter un gestionnaire [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md) . Le contrôle ToolBar envoie ce code de notification pour demander des informations sur chaque bouton lors de sa restauration.
-   La version 5,80 comprend une option d’enregistrement/de restauration. Au début du processus, lorsque chaque bouton est enregistré ou restauré, votre application reçoit un code de notification [TBN \_ Save](tbn-save.md) ou [TBN \_ Restore](tbn-restore.md) . Pour utiliser cette option, vous devez implémenter des gestionnaires de notification pour fournir la bitmap et les informations d’État nécessaires à l’enregistrement ou à la restauration de l’état de la barre d’outils.

Les États de barre d’outils sont enregistrés dans un flux de données qui comprend des blocs de données définies par l’interpréteur de commandes avec des blocs de données définies par l’application. Un bloc de données de chaque type est stocké pour chaque bouton, ainsi qu’un bloc facultatif de données globales que les applications peuvent placer au début du flux. Pendant le processus d’enregistrement, votre gestionnaire d' [ \_ enregistrement TBN](tbn-save.md) ajoute les blocs définis par l’application au flux de données. Pendant le processus de restauration, le gestionnaire de [ \_ restauration TBN](tbn-restore.md) lit chaque bloc et donne à l’interpréteur de commandes les informations dont il a besoin pour reconstruire la barre d’outils.

### <a name="how-to-handle-a-tbn_save-notification"></a>Comment gérer une notification d' \_ enregistrement TBN

Le premier code de notification d' [ \_ enregistrement TBN](tbn-save.md) est envoyé au début du processus d’enregistrement. Avant l’enregistrement des boutons, les membres de la structure [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) sont définis comme indiqué dans le tableau suivant.



| Membre       | Paramètre                                                                                                                                                                                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **iItem**    | –1                                                                                                                                                                                                                                                                                                                                                 |
| **cbData**   | Quantité de mémoire nécessaire pour les données définies par l’interpréteur de commandes.                                                                                                                                                                                                                                                                                                |
| **cButtons** | Nombre de boutons.                                                                                                                                                                                                                                                                                                                             |
| **pData**    | Quantité de mémoire calculée nécessaire pour les données définies par l’application. En règle générale, vous incluez des données globales, ainsi que des données pour chaque bouton. Ajoutez cette valeur à **cbData** et allouez suffisamment de mémoire à **pData** pour la conserver.                                                                                                                      |
| **pCurrent** | Premier octet inutilisé dans le flux de données. Si vous n’avez pas besoin d’informations globales sur la barre d’outils, définissez **pCurrent**  =  **pData** de manière à ce qu’il pointe vers le début du flux de données. Si vous avez besoin d’informations de barre d’outils globales, stockez-les sur **pData**, puis définissez **pCurrent** au début de la partie inutilisée du flux de données avant de retourner. |



 

Si vous souhaitez ajouter des informations globales sur la barre d’outils, placez-la au début du flux de données. Avancez les **pCurrent** à la fin des données globales afin qu’elles pointent vers le début de la partie inutilisée du flux de données, et retournent.

Une fois que vous avez retourné, l’interpréteur de commandes démarre l’enregistrement des informations du bouton. Elle ajoute les données définies par l’interpréteur de commandes pour le premier bouton à **pCurrent** , puis avance **pCurrent** au début de la partie inutilisée.

Une fois chaque bouton enregistré, un code de notification d' [ \_ enregistrement TBN](tbn-save.md) est envoyé et [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) est retourné avec les membres définis comme suit.



| Membre                       | Paramètre                                                                                                                                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **iItem**                    | Index de base zéro du numéro du bouton.                                                                                                                                                                                                                           |
| **pCurrent**                 | Pointeur vers le premier octet inutilisé dans le flux de données. Si vous souhaitez stocker des informations supplémentaires sur le bouton, stockez-le à l’emplacement désigné par **pCurrent** et mettez à jour **pCurrent** pour pointer vers la première partie inutilisée du flux de données. |
| [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) | Structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) qui décrit le bouton enregistré.                                                                                                                                                                              |



 

Lorsque vous recevez le code de notification, vous devez extraire toutes les informations spécifiques au bouton dont vous avez besoin à partir de [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton). N’oubliez pas que lorsque vous ajoutez un bouton, vous pouvez utiliser le membre **dwData** de **TBBUTTON** pour stocker des données spécifiques à l’application. Chargez vos données dans le flux de données sur **pCurrent**. Avancez les **pCurrent** à la fin de vos données, en pointant à nouveau sur le début de la partie inutilisée du flux et retournez.

L’interpréteur de commandes passe ensuite au bouton suivant, ajoute ses informations à **pData**, avance **PCurrent**, charge [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)et envoie un autre code de notification d' [ \_ enregistrement TBN](tbn-save.md) . Ce processus se poursuit jusqu’à ce que tous les boutons soient enregistrés.

### <a name="restoring-saved-toolbars"></a>Restauration des barres d’outils enregistrées

Le processus de restauration inverse fondamentalement le processus d’enregistrement. Au début, votre application recevra un code de notification de [ \_ restauration TBN](tbn-restore.md) avec le membre **iItem** de la structure [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) définie sur – 1. Le membre **cbData** est défini sur la taille de **pData** et **cButtons** est défini sur le nombre de boutons.

Votre gestionnaire de notification doit extraire les informations globales qui ont été placées au début de **pData** pendant l’enregistrement, et avancer **pCurrent** au début du premier bloc de données définies par l’interpréteur de commandes. Définissez **cBytesPerRecord** sur la taille des blocs de données que vous avez utilisés pour enregistrer les données du bouton. Définissez **cButtons** sur le nombre de boutons et retournez.

Le [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) suivant est pour le premier bouton. Le membre **pCurrent** pointe vers le début de votre premier bloc de données de bouton, et **iItem** est défini sur l’index de bouton. Extrayez ces données et avancez **pCurrent**. Charger les données dans [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)et retourner. Pour omettre un bouton à partir de la barre d’outils restaurée, définissez le membre **idCommand** de **TBBUTTON** sur zéro. L’interpréteur de commandes répète le processus pour les boutons restants. En plus des messages [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) et **NMTBRESTORE** , vous pouvez également utiliser des messages tels que [TBN \_ Reset](tbn-reset.md) pour enregistrer et restaurer une barre d’outils.

L’exemple de code suivant enregistre une barre d’outils avant qu’elle ne soit personnalisée et la restaure si l’application reçoit un message de [ \_ réinitialisation TBN](tbn-reset.md) .


```C++
int               i;
LPNMHDR           lpnmhdr;
static int        nResetCount;
static LPTBBUTTON lpSaveButtons;
LPARAM            lParam;

switch( lpnmhdr->code)
{
    case TBN_BEGINADJUST: // Begin customizing the toolbar.
    {
        LPTBNOTIFY  lpTB = (LPTBNOTIFY)lparam;
       
        // Allocate memory for the button information.
        
        nResetCount   = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        lpSaveButtons = (LPTBBUTTON)GlobalAlloc(GPTR, sizeof(TBBUTTON) * nResetCount);
      
        // In case the user presses reset, save the current configuration 
        // so the original toolbar can be restored.
        
        for(i = 0; i < nResetCount; i++)
        {
            SendMessage(lpTB->hdr.hwndFrom, 
                        TB_GETBUTTON, i, 
                        (LPARAM)(lpSaveButtons + i));
        }
    }
    
    return TRUE;
   
    case TBN_RESET:
    {
        LPTBNOTIFY lpTB = (LPTBNOTIFY)lparam;
        
        int nCount, i;
    
        // Remove all of the existing buttons, starting with the last one.
        
        nCount = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        
        for(i = nCount - 1; i >= 0; i--)
        {
            SendMessage(lpTB->hdr.hwndFrom, TB_DELETEBUTTON, i, 0);
        }
      
        SendMessage(lpTB->hdr.hwndFrom,      // Restore the saved buttons.
                    TB_ADDBUTTONS, 
                    (WPARAM)nResetCount, 
                    (LPARAM)lpSaveButtons);
    }
    
    return TRUE;
   
    case TBN_ENDADJUST:                // Free up the memory you allocated.
        GlobalFree((HGLOBAL)lpSaveButtons);
        
        return TRUE;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles ToolBar](using-toolbar-controls.md)
</dt> <dt>

[**Valeurs d’index d’image du bouton standard de la barre d’outils**](toolbar-standard-button-image-index-values.md)
</dt> <dt>

[Windows démonstration des contrôles communs (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




