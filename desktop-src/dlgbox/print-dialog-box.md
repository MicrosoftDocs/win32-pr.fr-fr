---
title: Boîte de dialogue Imprimer
description: La boîte de dialogue Imprimer permet à l’utilisateur de sélectionner des options pour un travail d’impression particulier.
ms.assetid: 34f69b25-8a89-4322-af4c-a80b85a4a973
keywords:
- Windows Interface utilisateur, entrée utilisateur
- Windows Interface utilisateur, bibliothèque de boîtes de dialogue communes
- entrée utilisateur, bibliothèque de boîtes de dialogue communes
- capture de l’entrée utilisateur, bibliothèque de boîtes de dialogue communes
- Bibliothèque de boîtes de dialogue communes
- boîtes de dialogue communes
- Boîte de dialogue Imprimer
- Boîte de dialogue Configuration de l’impression
- personnalisation de la boîte de dialogue Imprimer
- boîtes de dialogue prédéfinies
- boîtes de dialogue, imprimer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0afd8cfa31a83f664e859cd93acc9d28543b7ab00dcb8f130fdbac329cd1429e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117720915"
---
# <a name="print-dialog-box"></a>Boîte de dialogue Imprimer

La boîte de dialogue **Imprimer** permet à l’utilisateur de sélectionner des options pour un travail d’impression particulier. Par exemple, l’utilisateur peut spécifier l’imprimante à utiliser, la plage de pages à imprimer et le nombre de copies.

Vous pouvez utiliser la fonction [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) pour afficher une [feuille de propriétés d’impression](print-property-sheet.md), qui contient une page **générale** contenant des contrôles similaires à ceux de la boîte de dialogue **Imprimer** . La feuille de propriétés peut également contenir des pages de propriétés supplémentaires spécifiques à l’application et spécifiques au pilote, à la suite de la page **général** .

Vous créez et affichez une boîte de dialogue **Imprimer** en initialisant une structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) et en transmettant la structure à la fonction [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) .

L’illustration suivante montre une boîte de dialogue **Imprimer** standard.

![boîte de dialogue Imprimer](images/printdialogboxxp.png)

Si l’utilisateur clique sur le bouton **OK** , [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) retourne **true** et utilise la structure [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) pour retourner des informations sur les sélections de l’utilisateur. Par exemple, les membres **hDevMode** et **hDevNames** retournent généralement des handles de mémoire globaux pour les structures et [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) . Vous pouvez utiliser les informations de ces structures pour créer un contexte de périphérique ou un contexte d’informations pour l’imprimante sélectionnée.

Si l’utilisateur annule la boîte de dialogue **Imprimer** ou si une erreur se produit, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) retourne la **valeur false**. Vous pouvez déterminer la cause d’une erreur en utilisant la fonction [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) pour récupérer la valeur d’erreur étendue.

La boîte de dialogue **Imprimer** comprend un groupe d' **étendues** de cases d’option qui indiquent si l’utilisateur souhaite imprimer toutes les pages, une plage de pages ou uniquement le texte sélectionné. Avant d’appeler [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)), vous pouvez définir l’un des indicateurs **PD \_ ALLPAGES**, **PD \_ Selection** ou **PD \_ PAGENUMS** pour indiquer quel bouton est initialement sélectionné. Quand **PrintDlg** retourne la **valeur true**, la fonction définit l’un de ces indicateurs pour indiquer les sélections de l’utilisateur. Si **PD \_ PAGENUMS** est défini, les membres **nFromPage** et **nToPage** de la structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) contiennent les pages de début et de fin spécifiées par l’utilisateur. Pour désactiver la case **d'** option **pages** et les contrôles associés from et **to** Edit, définissez l’indicateur **PD \_ NOPAGENUMS** . Pour désactiver la case d’option **sélection** , définissez l’indicateur **PD \_ noselect** .

La boîte de dialogue comprend un contrôle d’édition dans lequel l’utilisateur peut taper le nombre de copies à imprimer. Si le membre **hDevMode** de la structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) est non **null**, le membre **dmCopies** de la structure spécifie la valeur initiale pour ce contrôle d’édition. Si **hDevMode** a la valeur **null**, le membre **nCopies** de la structure **PRINTDLG** spécifie la valeur initiale. Quand [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) retourne, **nCopies** indique généralement le nombre de copies spécifiées par l’utilisateur. Toutefois, si vous définissez l' **indicateur \_ PD USEDEVMODECOPIESANDCOLLATE** lors de la création de la boîte de dialogue, **nCopies** a toujours la valeur 1 au retour et le membre **dmCopies** de [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) indique le nombre de copies à imprimer.

La case à cocher **assembler** indique si l’utilisateur souhaite reclasser les pages si plusieurs copies sont imprimées. L’indicateur de **\_ classement PD** est défini si la case à cocher **assembler** est activée. Si votre application ne prend pas en charge plusieurs copies ou un classement simulé, définissez l’indicateur **PD \_ USEDEVMODECOPIESANDCOLLATE** dans le membre **Flags** de la structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . Cela désactive la case à cocher **assembler** et le **nombre de copies du contrôle d'** édition, sauf si le pilote d’imprimante prend en charge plusieurs copies et classement.

La case à cocher **Imprimer dans un fichier** indique si l’utilisateur souhaite envoyer la sortie vers un fichier plutôt que vers une imprimante. Vous pouvez définir l’indicateur **PD \_ PRINTTOFILE** pour que la case à cocher soit initialement sélectionnée. Pour masquer la case à cocher, définissez l’indicateur **PD \_ HIDEPRINTTOFILE** . Pour le désactiver, définissez l’indicateur **PD \_ DISABLEPRINTTOFILE** . Si l’utilisateur sélectionne l’option **Imprimer dans un fichier** , [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) définit l’indicateur **PD \_ PRINTTOFILE** et retourne « file : » à l’offset indiqué par le membre **wOutputOffset** de la structure [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) . Quand vous appelez la fonction pour démarrer l’opération d’impression, spécifiez la chaîne « FILE : » dans le membre **lpszOutput** de la structure. Si vous spécifiez cette chaîne, le sous-système d’impression interroge l’utilisateur sur le nom du fichier de sortie.

Par défaut, la boîte de dialogue **Imprimer** affiche initialement des informations sur l’imprimante par défaut actuelle. Pour afficher les informations d’une autre imprimante installée, initialisez une et une structure [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) et attribuez le descripteur de mémoire globale à la structure aux membres **hDevMode** et **hDevNames** . Le nom de l’appareil que vous spécifiez dans le membre **dmDeviceName** de la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) et dans le membre **wDriverOffset** de la structure **DEVNAMES** doit identifier un périphérique d’impression qui est également indiqué dans la \[ \] section périphériques du fichier Win.ini. Si l’appareil n’est pas listé, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) renvoie une erreur.

Vous pouvez demander à [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) de créer un contexte de périphérique ou un contexte d’informations pour l’imprimante en définissant l’indicateur de **\_ retour** **PD \_ RETURNDC** ou PD dans le membre **Flags** de la structure [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . La fonction retourne un handle vers le contexte de périphérique ou le contexte d’information dans le membre **HDC** . Si vous utilisez l’indicateur **PD \_ RETURNDC** , vous pouvez utiliser le contexte de périphérique pour générer la sortie de l’imprimante.

Pour récupérer des informations sur l’imprimante par défaut sans afficher la boîte de dialogue **Imprimer** , définissez l’indicateur **PD \_ RETURNDEFAULT** . Dans ce cas, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) retourne immédiatement après avoir défini les membres **hDevMode** et **hDevNames** sur Handles pour les structures contenant les informations.

Par défaut, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) affiche des boîtes de message lorsque des erreurs se produisent. Par exemple, la fonction affiche un message d’erreur si aucune imprimante n’est installée. Pour empêcher la fonction d’afficher ces messages d’avertissement, définissez l’indicateur **PD \_ nowarning** .

Les rubriques suivantes sont présentées dans cette section.

-   [Personnalisation de la boîte de dialogue Imprimer](#customizing-the-print-dialog-box)
-   [Boîte de dialogue Configuration de l’impression](#print-setup-dialog-box)

## <a name="customizing-the-print-dialog-box"></a>Personnalisation de la boîte de dialogue Imprimer

Vous pouvez fournir un modèle personnalisé pour la boîte de dialogue **Imprimer** , par exemple, si vous souhaitez inclure des contrôles supplémentaires propres à votre application. La fonction [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) utilise votre modèle personnalisé à la place du modèle par défaut.

Pour fournir un modèle personnalisé pour la boîte de dialogue **Imprimer** :

1.  Créez le modèle personnalisé en modifiant le modèle par défaut spécifié dans le fichier Prnsetup. dlg. Les identificateurs de contrôle utilisés dans le modèle de boîte de dialogue d' **impression** par défaut sont définis dans le fichier Dlgs. h.
2.  Utilisez la structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) pour activer le modèle comme suit :
    -   Si votre modèle personnalisé est une ressource d’une application ou d’une bibliothèque de liens dynamiques, définissez l’indicateur **PD \_ ENABLEPRINTTEMPLATE** dans le membre **Flags** . Utilisez les membres **HINSTANCE** et **lpPrintTemplateName** de la structure pour identifier le nom du module et de la ressource.

        Ou

    -   Si votre modèle personnalisé est déjà en mémoire, définissez l’indicateur **PD \_ ENABLEPRINTTEMPLATEHANDLE** . Utilisez le membre **hPrintTemplate** pour identifier l’objet mémoire qui contient le modèle.

Vous pouvez fournir une procédure de hook [**PrintHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc) pour la boîte de dialogue **Imprimer** . La procédure de raccordement peut traiter les messages envoyés à la boîte de dialogue. Il peut également envoyer des messages à la boîte de dialogue. Si vous utilisez un modèle personnalisé pour définir des contrôles supplémentaires, vous devez fournir une procédure de raccordement pour traiter l’entrée de vos contrôles.

Pour activer une procédure de Hook pour la boîte de dialogue **Imprimer** :

1.  Définissez l’indicateur **PD \_ ENABLEPRINTHOOK** dans le membre **Flags** de la structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .
2.  Spécifiez l’adresse de la procédure de raccordement dans le membre **lpfnPrintHook** .

Après le traitement du message [**WM \_ INITDIALOG**](wm-initdialog.md) , la procédure de la boîte de dialogue envoie un message **WM \_ INITDIALOG** à la procédure de Hook. Le paramètre *lParam* de ce message est un pointeur vers la structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) utilisée pour initialiser la boîte de dialogue.

## <a name="print-setup-dialog-box"></a>Boîte de dialogue Configuration de l’impression

Vous pouvez créer et afficher une boîte de dialogue de configuration de l' **impression** en définissant l’indicateur **PD \_ PRINTSETUP** dans un appel à la fonction [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) . Toutefois, la boîte de dialogue Configuration de l' **impression** a été remplacée par la boîte de dialogue **mise en page** et ne doit pas être utilisée dans les nouvelles applications.

Les indicateurs suivants s’appliquent uniquement à la boîte de dialogue Configuration de l' **impression** :

-   **PD \_ ENABLESETUPHOOK**
-   **PD \_ ENABLESETUPTEMPLATE**
-   **PD \_ ENABLESETUPTEMPLATEHANDLE**

 

 