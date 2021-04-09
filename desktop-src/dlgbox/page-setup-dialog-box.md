---
title: Boîte de dialogue Mise en page
description: Affiche une boîte de dialogue modale qui permet à l’utilisateur de choisir des paramètres qui incluent le type de papier, la source de papier, l’orientation de page et la largeur des marges de page.
ms.assetid: debde0a0-07d4-46ed-a936-e517eab1852d
keywords:
- Interface utilisateur Windows, entrée utilisateur
- Interface utilisateur Windows, bibliothèque de boîtes de dialogue communes
- entrée utilisateur, bibliothèque de boîtes de dialogue communes
- capture de l’entrée utilisateur, bibliothèque de boîtes de dialogue communes
- Bibliothèque de boîtes de dialogue communes
- boîtes de dialogue communes
- Mise en page (boîte de dialogue)
- personnalisation de la boîte de dialogue mise en page
- raccordements, boîte de dialogue mise en page
- boîtes de dialogue prédéfinies
- boîtes de dialogue, mise en page
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b9a8f7f30a8313017dc3a124cdccb7d00c872b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102300"
---
# <a name="page-setup-dialog-box"></a>Boîte de dialogue Mise en page

Affiche une boîte de dialogue modale qui permet à l’utilisateur de définir les attributs suivants de la page imprimée :

-   Le type de papier (enveloppe, légal, lettre, etc.)
-   Source de papier (alimentation manuelle, alimentation de tracteur, chargeur de feuille, etc.)
-   Orientation de la page (portrait ou paysage)
-   Largeur des marges de la page

Vous créez et affichez une boîte de dialogue **mise en page** en initialisant une structure [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) et en transmettant la structure à la fonction [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) . Toutefois, les attributs présentés dans la boîte de dialogue varient selon les capacités de l’imprimante. L’illustration suivante montre une boîte de dialogue de **mise en page** classique.

![mise en page, boîte de dialogue](images/pagesetupdialogboxxp.png)

Si l’utilisateur clique sur le bouton **OK** , [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) retourne **true** après avoir défini différents membres dans la structure [**PageSetupDlg**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) pour spécifier les sélections de l’utilisateur. Les membres **ptPaperSize** et **rtMargin** contiennent les valeurs spécifiées par l’utilisateur. Les membres **hDevMode** et **hDevNames** contiennent des descripteurs de mémoire globaux pour les structures [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) et [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) . Ces structures contiennent des informations de page supplémentaires ainsi que des informations sur l’imprimante. Vous pouvez utiliser ces informations pour préparer la sortie à envoyer à l’imprimante sélectionnée.

Si l’utilisateur annule la boîte de dialogue **mise en page** ou si une erreur se produit, [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) retourne **false**. Pour déterminer la cause de l’erreur, appelez la fonction [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) pour récupérer la valeur d’erreur étendue.

Cette section décrit les rubriques suivantes.

-   [Initialisation de la boîte de dialogue mise en page](#initializing-the-page-setup-dialog-box)
-   [Personnalisation de la boîte de dialogue mise en page](#customizing-the-page-setup-dialog-box)
-   [Personnalisation de l’exemple de page](#customizing-the-sample-page)

## <a name="initializing-the-page-setup-dialog-box"></a>Initialisation de la boîte de dialogue mise en page

Par défaut, la boîte de dialogue **mise en page** affiche des informations sur l’imprimante par défaut actuelle. Pour indiquer à la boîte de dialogue d’afficher des informations sur une imprimante spécifique, définissez les membres d’une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) ou [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) et affectez les descripteurs de mémoire globaux de ces structures au membre correspondant dans [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga). Si vous spécifiez le nom d’une imprimante qui n’est pas installée actuellement, la boîte de dialogue affiche un message d’erreur. Pour empêcher la boîte de dialogue d’afficher des messages d’erreur, utilisez la valeur **PSD \_ nowarning** . Pour récupérer des informations sur l’imprimante par défaut sans afficher la boîte de dialogue **mise en page** , utilisez la valeur **PSD \_ RETURNDEFAULT** .

Si le système de mesure par défaut est pouces, la boîte de dialogue utilise des millièmes de pouce comme unité de mesure par défaut. Si le système de mesure par défaut est métrique, la boîte de dialogue utilise des centièmes de millimètres comme unité de mesure par défaut. Pour remplacer l’unité de mesure par défaut, définissez l' **indicateur \_ PSD INHUNDREDTHSOFMILLIMETERS** ou **PSD \_ INTHOUSANDTHSOFINCHES** dans le membre **Flags** de la structure [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) .

Par défaut, les valeurs initiales des marges sont d’un pouce. Si vous définissez l’indicateur de **\_ marges PSD** , la boîte de dialogue affiche les valeurs de marge initiale spécifiées dans le membre **rtMargin** . Les valeurs minimales par défaut que l’utilisateur peut spécifier pour les marges sont les marges minimales autorisées par l’imprimante. Si vous définissez l’indicateur **PSD \_ MINMARGINS** , la boîte de dialogue applique les marges minimales spécifiées dans le membre **rtMinMargin** .

Pour empêcher les utilisateurs de sélectionner certaines options, définissez une combinaison des indicateurs suivants pour désactiver les contrôles correspondants.



| Indicateur                        | Signification                                                                  |
|-----------------------------|--------------------------------------------------------------------------|
| **\_DISABLEMARGINS PSD**     | Désactive les contrôles d’édition dans lesquels l’utilisateur entre les paramètres de marge. |
| **\_DISABLEORIENTATION PSD** | Désactive les cases d’option **portrait** et **paysage** .               |
| **\_DISABLEPAPER PSD**       | Désactive les contrôles permettant de sélectionner le format de papier et la source de papier.     |
| **\_DISABLEPRINTER PSD**     | Désactive le bouton **imprimante** .                                         |



 

## <a name="customizing-the-page-setup-dialog-box"></a>Personnalisation de la boîte de dialogue mise en page

Vous pouvez fournir un modèle personnalisé pour la boîte de dialogue **mise en page** , par exemple, si vous souhaitez inclure des contrôles supplémentaires propres à votre application. La fonction [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) utilise votre modèle personnalisé à la place du modèle par défaut.

**Pour fournir un modèle personnalisé pour la boîte de dialogue mise en page**

1.  Créez le modèle personnalisé en modifiant le modèle par défaut spécifié dans le fichier Prnsetup. dlg. Les identificateurs de contrôle utilisés dans le modèle de boîte de dialogue de **mise en page** par défaut sont définis dans le fichier Dlgs. h.
2.  Utilisez la structure [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) pour activer le modèle comme suit :
    -   -   Si votre modèle personnalisé est une ressource d’une application ou d’une bibliothèque de liens dynamiques, définissez l’indicateur **PSD \_ ENABLEPAGESETUPTEMPLATE** dans le membre **Flags** . Utilisez les membres **HINSTANCE** et **lpPageSetupTemplateName** de la structure pour identifier le nom du module et de la ressource.

            Ou

        -   Si votre modèle personnalisé est déjà en mémoire, définissez l’indicateur **PSD \_ ENABLEPAGESETUPTEMPLATEHANDLE** . Utilisez le membre **hPageSetupTemplate** pour identifier l’objet mémoire qui contient le modèle.

Pour filtrer les messages envoyés à la procédure de la boîte de dialogue, vous pouvez fournir une procédure de hook [**PageSetupHook**](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook) . Si vous utilisez un modèle personnalisé pour définir des contrôles supplémentaires, vous devez fournir une procédure de hook **PageSetupHook** pour traiter l’entrée de vos contrôles. En outre, vous pouvez fournir une procédure de hook [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) pour personnaliser le contenu de l’exemple de page affiché dans la boîte de dialogue **mise en page** . Pour plus d’informations sur la procédure de hook **PagePaintHook** , consultez [Personnalisation de la page d’exemple](#customizing-the-sample-page).

**Pour activer une procédure de hook PageSetupHook**

1.  Définissez l’indicateur **PSD \_ ENABLEPAGESETUPHOOK** dans le membre **Flags** de la structure [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) .
2.  Spécifiez l’adresse de la procédure de raccordement dans le membre **lpfnPageSetupHook** .

Après le traitement du message [**WM \_ INITDIALOG**](wm-initdialog.md) , la procédure de la boîte de dialogue envoie un message **WM \_ INITDIALOG** à la procédure de hook [**PageSetupHook**](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook) . Le paramètre *lParam* de ce message est un pointeur vers la structure [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) utilisée pour initialiser la boîte de dialogue.

## <a name="customizing-the-sample-page"></a>Personnalisation de l’exemple de page

La boîte de dialogue **mise en page** comprend une image d’un exemple de page qui montre comment les sélections de l’utilisateur affectent l’apparence de la sortie imprimée. L’image se compose d’un rectangle qui représente le type de papier ou d’enveloppe sélectionné, avec un rectangle en pointillé représentant les marges actuelles et des caractères partiels (texte grec) pour afficher l’aspect du texte sur la page imprimée.

Quand vous appelez la fonction [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , vous pouvez fournir une procédure de hook [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) pour personnaliser l’apparence de la page d’exemple.

**Pour activer une procédure de hook PagePaintHook**

1.  Définissez l’indicateur **PSD \_ ENABLEPAGEPAINTHOOK** dans le membre **Flags** de la structure [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) .
2.  Spécifiez l’adresse de la procédure de raccordement dans le membre **lpfnPagePaintHook** .

Chaque fois que la boîte de dialogue est sur le le contenu de la page d’exemple, la procédure de raccordement reçoit les messages suivants dans l’ordre dans lequel ils sont répertoriés.



| Message                                                  | Signification                                                                                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_PAGESETUPDLG WM \_**](wm-psd-pagesetupdlg.md)     | La boîte de dialogue vous permet de dessiner la page de l’exemple. La procédure de raccordement peut utiliser ce message pour préparer le contenu de la page d’exemple.     |
| [**\_FULLPAGERECT WM \_**](wm-psd-fullpagerect.md)     | La boîte de dialogue vous permet de dessiner la page de l’exemple. Ce message spécifie le rectangle englobant de la page d’exemple.                               |
| [**\_MINMARGINRECT WM \_**](wm-psd-minmarginrect.md)   | La boîte de dialogue vous permet de dessiner la page de l’exemple. Ce message spécifie le rectangle de marge.                                                    |
| [**\_MARGINRECT WM \_**](wm-psd-marginrect.md)         | La boîte de dialogue est sur le sujet de dessiner le rectangle de marge.                                                                                            |
| [**\_GREEKTEXTRECT WM \_**](wm-psd-greektextrect.md)   | La boîte de dialogue vous permet de dessiner le texte grec à l’intérieur du rectangle de marge.                                                                      |
| [**\_ENVSTAMPRECT WM \_**](wm-psd-envstamprect.md)     | La boîte de dialogue est sur le dessin du rectangle d’enveloppe d’une page d’exemple d’enveloppe. Ce message est envoyé uniquement pour les enveloppes.             |
| [**\_YAFULLPAGERECT WM \_**](wm-psd-yafullpagerect.md) | La boîte de dialogue vous permet de dessiner la partie adresse de retour d’une page d’exemple d’enveloppe. Ce message est envoyé pour les enveloppes et autres formats de papier. |



 

Si la procédure de raccordement retourne la **valeur true** pour l’un des trois premiers messages d’une séquence de dessin ([**WM \_ PSD \_ PAGESETUPDLG**](wm-psd-pagesetupdlg.md), [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)ou [**WM \_ PSD \_ MINMARGINRECT**](wm-psd-minmarginrect.md)), la boîte de dialogue n’envoie plus de messages et ne dessine pas dans la page d’exemple tant que le système n’a pas besoin de redessiner la page d’exemple. Si la procédure de hook retourne la **valeur false** pour les trois messages, la boîte de dialogue envoie les messages restants de la séquence de dessin.

Si la procédure de raccordement retourne la **valeur true** pour l’un des messages restants dans une séquence de dessin, la boîte de dialogue ne dessine pas la partie correspondante de la page d’exemple. Si la procédure de raccordement retourne la **valeur false** pour l’un de ces messages, la boîte de dialogue crée cette partie de la page d’exemple.

Pour empêcher la boîte de dialogue de dessiner le contenu de la page d’exemple, vous pouvez définir l’indicateur **PSD \_ DISABLEPAGEPAINTING** . Cet indicateur n’affecte pas votre procédure de hook [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) , qui reçoit toujours tous **\_ les messages \_ \* WM** et peut dessiner le contenu de la page d’exemple.

 

 