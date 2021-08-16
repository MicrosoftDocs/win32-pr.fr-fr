---
title: Police, boîte de dialogue
description: La boîte de dialogue police permet à l’utilisateur de choisir des attributs pour une police logique, tels que la famille de polices et le style de police associé, la taille du point, les effets (souligné, barré et couleur du texte), ainsi qu’un script (ou jeu de caractères).
ms.assetid: e8a996aa-4e34-45d0-a325-9c20b1a6ce07
keywords:
- Windows Interface utilisateur, entrée utilisateur
- Windows Interface utilisateur, bibliothèque de boîtes de dialogue communes
- entrée utilisateur, bibliothèque de boîtes de dialogue communes
- capture de l’entrée utilisateur, bibliothèque de boîtes de dialogue communes
- Bibliothèque de boîtes de dialogue communes
- boîtes de dialogue communes
- Police (boîte de dialogue)
- boîte de dialogue Personnalisation de la police
- indicateurs, boîte de dialogue police
- indicateurs d’initialisation
- boîtes de dialogue prédéfinies
- boîtes de dialogue, police
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8544fcb60e499a360f60d1701863a11138d3f16fb06a770a9a2763800d908e12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785885"
---
# <a name="font-dialog-box"></a>Police, boîte de dialogue

La boîte de dialogue **police** permet à l’utilisateur de choisir des attributs pour une police logique, tels que la famille de polices et le style de police associé, la taille du point, les effets (souligné, barré et couleur du texte), ainsi qu’un script (ou jeu de caractères).

Vous créez et affichez une boîte de dialogue de **police** en initialisant une structure [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) et en transmettant la structure à la fonction [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) .

La capture d’écran suivante montre une boîte de dialogue **police** standard.

![capture d’écran montrant la boîte de dialogue police](images/fontdialogboxxp.png)

Si l’utilisateur clique sur le bouton **OK** , la fonction [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) retourne la **valeur true** et définit les informations sur la sélection de l’utilisateur dans la structure [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) .

Si l’utilisateur annule la boîte de dialogue **police** ou si une erreur se produit, [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) retourne la **valeur false** et le contenu de la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) n’est pas défini. Vous pouvez déterminer la cause d’une erreur en utilisant la fonction [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) pour récupérer la valeur d’erreur étendue.

Les rubriques suivantes sont présentées dans cette section.

-   [Indicateurs d’initialisation de la boîte de dialogue police](#font-dialog-box-initialization-flags)
-   [Personnalisation de la boîte de dialogue police sur les versions antérieures de Windows](#customizing-the-font-dialog-box-on-earlier-versions-of-windows)
-   [personnalisation de la boîte de dialogue police sur Windows 7](#customizing-the-font-dialog-box-on-windows-7)

## <a name="font-dialog-box-initialization-flags"></a>Indicateurs d’initialisation de la boîte de dialogue police

Avant d’appeler [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), le membre **Flags** de la structure [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) doit spécifier **CF \_ SCREENFONTS**, **CF \_ PRINTERFONTS**, ou **CF \_ both**, pour indiquer si la boîte de dialogue doit répertorier les polices d’écran, les polices d’imprimante ou les deux. Si vous spécifiez **CF \_ PRINTERFONTS** ou **CF \_ both**, le membre **HDC** de la structure **CHOOSEFONT** doit spécifier un handle vers un contexte de périphérique pour l’imprimante.

Si les **\_ deux** indicateurs **CF \_ PRINTERFONTS** ou CF sont définis, l’étiquette Description du type de police apparaît en bas de la boîte de dialogue **police** .

à partir de Windows 7, les indicateurs **cf \_ PRINTERFONTS**, **cf \_ SCREENFONTS**, **cf \_** et **cf \_ WYSIWYG** ne sont plus utilisés par la fonction [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) pour l’énumération des polices. ils sont obsolètes dans Windows 7. Toutefois, l’indicateur **CF \_ PRINTERFONTS** conserve une fonction : pour afficher l’étiquette de description du type de police au bas de la boîte de dialogue **police** .

Vous pouvez utiliser le membre **Flags** pour activer ou désactiver certains des contrôles de boîte de dialogue de **police** , et vous pouvez utiliser le membre **Flags** conjointement avec d’autres membres [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) pour contrôler les valeurs initiales de certains contrôles.

**Pour afficher les contrôles qui permettent à l’utilisateur de sélectionner les options de barré, de soulignement et de couleur :**

-   Définissez l’indicateur d' **\_ effets CF** . Vous pouvez utiliser le membre **rgbColors** de la structure [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) pour spécifier une couleur de police initiale.

**Pour spécifier les valeurs initiales des contrôles de boîte de dialogue police, style de police, taille, barré et souligné :**

1.  Pour spécifier les valeurs initiales des contrôles de boîte de dialogue police, style de police, taille, barré et souligné :
2.  Définissez l' **indicateur CF \_ INITTOLOGFONTSTRUCT** dans le membre **Flags** , ainsi que les membres de la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) vers laquelle pointe **lpLogFont**, pour spécifier les valeurs initiales des attributs de police.
3.  Vous pouvez également utiliser les **indicateurs \_ CF NOFACESEL**, **CF \_ NOSTYLESEL** et **CF \_ NOSIZESEL** pour empêcher la boîte de dialogue **police** d’afficher les valeurs initiales des contrôles correspondants. Cela est utile lorsque vous travaillez avec une sélection de texte qui a plusieurs polices, styles ou tailles de point. Ces valeurs seront également définies dans **Flags** lorsque [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) retourne, si l’utilisateur n’a pas sélectionné de valeur correspondante.

**Pour initialiser le contrôle de style de police à un nom de style spécifié**

-   Définissez l’indicateur **CF \_ USESTYLE** et utilisez le membre **lpszStyle** pour spécifier le nom du style.

> [!Note]  
> Pour globaliser votre application, spécifiez le style à l’aide des membres **lfWeight** et **lfItalic** de la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) vers laquelle pointe **lpLogFont**. Le nom du style peut changer en fonction de la langue de l’interface utilisateur système.

 

**Pour afficher le bouton appliquer**

-   Définissez l’indicateur **CF \_ apply** et fournissez une procédure de raccordement pour traiter les messages de [**\_ commande WM**](/windows/desktop/menurc/wm-command) pour le bouton **apply** . La procédure de hook peut envoyer le message [**WM \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md) à la boîte de dialogue pour récupérer l’adresse de la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) qui contient les sélections actuelles de la police.

**Pour afficher le bouton aide**

-   Définissez l’indicateur **CF \_ SHOWHELP** . Le membre **hwndOwner** doit identifier la fenêtre pour recevoir le message enregistré [**HELPMSGSTRING**](helpmsgstring.md) lorsque l’utilisateur clique sur le bouton **aide** .

**Pour limiter les polices affichées dans la boîte de dialogue**

-   Définissez n’importe quelle combinaison des indicateurs **CF \_ TTONLY**, cf **\_ FIXEDPITCHONLY**, cf **\_ NOVECTORFONTS**, **CF \_ NOVERTFONTS**, **CF \_ SCALABLEONLY** et **CF \_ WYSIWYG** . Vous pouvez également limiter les styles disponibles que la boîte de dialogue affiche pour certaines polices à l’aide de la valeur **CF \_ nosimulations** .

à partir de Windows 7, la liste des polices affichée dans la boîte de dialogue est restreinte en fonction des polices affichées par l’utilisateur. Pour supprimer la restriction, définissez l’indicateur **CF \_ INACTIVEFONTS** .

**Pour limiter les noms de polices, les styles et les tailles de point que l’utilisateur peut spécifier**

1.  Définissez l’indicateur **CF \_ FORCEFONTEXIST** pour limiter l’utilisateur à spécifier uniquement des noms de polices, des styles et des tailles de points valides dans la boîte de dialogue.
2.  Définissez l’indicateur de **\_ limitation CF** pour limiter l’utilisateur à spécifier des tailles de points dans la plage spécifiée par les membres **nSizeMin** et **nSizeMax** .

**Pour limiter ou désactiver la zone de liste déroulante scripts**

-   Définissez l' **indicateur CF \_ NOSCRIPTSEL** pour désactiver la zone de liste déroulante **scripts** , ou définissez l’indicateur **CF \_ SELECTSCRIPT** pour restreindre les sélections de la zone de liste déroulante **scripts** à un jeu de caractères spécifié.

## <a name="customizing-the-font-dialog-box-on-earlier-versions-of-windows"></a>Personnalisation de la boîte de dialogue police sur les versions antérieures de Windows

Vous pouvez fournir un modèle personnalisé pour la boîte de dialogue **police** , par exemple, si vous souhaitez inclure des contrôles supplémentaires propres à votre application. La fonction [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) utilise votre modèle personnalisé à la place du modèle par défaut.

**Pour fournir un modèle personnalisé pour la boîte de dialogue police**

1.  Créez le modèle personnalisé en modifiant le modèle par défaut spécifié dans le fichier font. dlg. Les identificateurs de contrôle utilisés dans le modèle de boîte de dialogue de police par défaut sont définis dans le fichier Dlgs. h.
2.  Utilisez la structure [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) pour activer le modèle comme suit :
    -   Si votre modèle personnalisé est une ressource d’une application ou d’une bibliothèque de liens dynamiques, définissez l’indicateur **CF \_ ENABLETEMPLATE** dans le membre **Flags** . Utilisez les membres **HINSTANCE** et **lpTemplateName** de la structure pour identifier le nom du module et de la ressource.
    -   Si votre modèle personnalisé est déjà en mémoire, définissez l’indicateur **CF \_ ENABLETEMPLATEHANDLE** . Utilisez le membre **HINSTANCE** pour identifier l’objet mémoire qui contient le modèle.

Vous pouvez fournir une procédure de hook [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) pour la boîte de dialogue **police** . La procédure de hook peut traiter les messages envoyés à la boîte de dialogue et envoyer des messages à la boîte de dialogue. Si vous utilisez un modèle personnalisé pour définir des contrôles supplémentaires, vous devez fournir une procédure de raccordement pour traiter l’entrée de vos contrôles.

**Pour activer une procédure de Hook pour la boîte de dialogue police**

1.  Définissez l’indicateur **CF \_ ENABLEHOOK** dans le membre **Flags** de la structure [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) .
2.  Spécifiez l’adresse de la procédure de raccordement dans le membre **lpfnHook** .

Après le traitement du message [**WM \_ INITDIALOG**](wm-initdialog.md) , la procédure de la boîte de dialogue envoie un message **WM \_ INITDIALOG** à la procédure de Hook. Le paramètre *lParam* de ce message est un pointeur vers la structure [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) qui est utilisée pour initialiser la boîte de dialogue.

La procédure de hook peut envoyer les messages [**WM \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md), [**WM \_ CHOOSEFONT \_ SETLOGFONT**](wm-choosefont-setlogfont.md)et [**WM \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md) à la boîte de dialogue pour récupérer et définir les valeurs et les indicateurs actuels de la boîte de dialogue.

## <a name="customizing-the-font-dialog-box-on-windows-7"></a>personnalisation de la boîte de dialogue police sur Windows 7

la capture d’écran suivante montre une boîte de dialogue **police** standard dans Windows 7.

![capture d’écran montrant la zone dialob de la police](images/fontdialogboxwin7.png)

dans les versions antérieures de Windows, le fichier de modèle font. dlg contient un modèle ChooseFont par défaut. le fichier de modèle font. dlg sur Windows 7 contient deux modèles par défaut : le modèle par défaut des versions antérieures Windows et le Windows nouveau modèle ChooseFont 7. par conséquent, lorsque vous personnalisez la boîte de dialogue **police** sur Windows 7, vous devez prendre en compte les problèmes suivants.

1.  utilisez le nouveau modèle lorsque vous créez des modèles personnalisés pour les applications qui s’exécutent sur Windows 7. Ce nouveau modèle contient un contrôle de lien sur lequel l’utilisateur peut cliquer pour ouvrir la fenêtre **du panneau de configuration polices** , comme illustré dans la capture d’écran suivante.

    ![capture d’écran montrant le panneau de configuration de la police dans Windows 7](images/fontcontrolpanelforwin7.png)

2.  Pour utiliser ce contrôle de lien, votre application appelante doit utiliser le COMCTL32.DLL version 6 ou ultérieure. Dans le cas contraire, la fonction [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) retourne une erreur lorsqu’elle tente de créer le contrôle de lien dans votre modèle personnalisé. Pour déterminer si ce contrôle est activé, compilez votre application appelante sur COMCTL32.DLL version 6,0. Pour plus d’informations, consultez [activation de styles visuels avec des contrôles communs](/previous-versions//ms649781(v=vs.85)).
3.  Si votre application utilise COMCTL32.DLL version 5,0 ou une version antérieure, vous devez effectuer les opérations suivantes lorsque vous créez un modèle personnalisé :

    -   Spécifiez le contrôle en tant que **bouton** de commande. Le contrôle utilisé pour lancer le **panneau de configuration des polices** s’affiche sous la forme d’un bouton plutôt que sous forme de lien.
    -   Remplacez le texte suivant dans la police. DLG :

        `CONTROL         "<A>Show more fonts</A>", IDC_MANAGE_LINK, "SysLink", WS_TABSTOP, 7, 199, 227, 9`

        avec le texte suivant :

        `PUSHBUTTON      "S&how more fonts", IDC_MANAGE_LINK, 7, 199, 74, 14 , WS_TABSTOP`

    -   pour vous assurer que votre application utilise un modèle personnalisé, vous devez spécifier un modèle personnalisé avec l’indicateur **CF \_ ENABLETEMPLATE** , créer un modèle personnalisé basé sur le modèle Windows 7 ChooseFont, puis activer éventuellement une procédure de raccordement.

        si vous activez une procédure de hook sans créer de modèle personnalisé, le modèle ChooseFont par défaut pour les versions antérieures de Windows sera chargé.

> [!Note]  
> Vous devez spécifier le type de contrôle **Control** ou **PUSHBUTTON** dans votre nouveau modèle, en fonction de la version de COMMCTL.DLL par rapport à laquelle votre application est compilée. notez également que Windows 7 fonctionnalités spécifiques, telles que l’affichage WYSIWYG des listes de polices et des familles étendues, ne sont pas disponibles lorsque vos applications s’exécutent sur des versions antérieures du système d’exploitation Windows.

 

 

 