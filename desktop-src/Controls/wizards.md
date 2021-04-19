---
title: Comment créer des assistants
description: Un Assistant est un type de feuille de propriétés qui offre un moyen simple et puissant pour guider les utilisateurs dans une procédure.
ms.assetid: f8def159-0a68-4d7f-9840-c7b6b906ed08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fedd35bd0454e0d78ddbe74d832543e58d0a8fc7
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "106529645"
---
# <a name="how-to-create-wizards"></a>Comment créer des assistants

Un Assistant est un type de feuille de propriétés qui offre un moyen simple et puissant pour guider les utilisateurs dans une procédure.

Les assistants sont l’une des clés permettant de simplifier l’expérience utilisateur. Elles vous permettent d’effectuer une opération complexe, telle que la configuration d’une application, et de la décomposer en une série d’étapes simples. À chaque étape du processus, vous pouvez fournir une explication de ce qui est nécessaire et afficher les contrôles qui permettent à l’utilisateur d’effectuer des sélections et d’entrer du texte.

Un Assistant est en fait un type de feuille de propriétés. Une feuille de propriétés est essentiellement un conteneur pour une collection de *pages*, où chaque page est une boîte de dialogue distincte. Tandis que les feuilles de propriétés standard permettent à l’utilisateur d’accéder à n’importe quelle page à tout moment, les assistants présentent des pages en séquence. Au lieu de tabulations, les boutons permettent de naviguer vers l’avant et vers l’arrière. L’ordre dans lequel les pages sont affichées est contrôlé par l’application et peut être modifié en fonction de l’entrée de l’utilisateur.

Il existe deux principaux styles d’Assistant : l’ancien style Wizard97 et le style Aero introduit dans Windows Vista. Pour obtenir des illustrations, consultez [à propos des feuilles de propriétés](property-sheets.md). (Un troisième style, utilisant uniquement PSH \_ L’Assistant ou \_ l' \_ indicateur Lite de l’Assistant PSH présente une séquence simple de feuilles de propriétés sans en-tête ni filigrane.)

> [!Note]  
> Un « filigrane » dans le contexte des assistants est une image bitmap qui apparaît dans la marge de gauche de certaines pages.

 

La description de la majeure partie de ce document suppose que vous implémentiez un Assistant pour un système avec la [version 5,80](common-control-versions.md) ou ultérieure des contrôles communs. Si vous tentez d’utiliser le style Wizard97 avec des versions antérieures des contrôles communs, votre application peut se compiler, mais elle ne s’affichera pas correctement. Pour plus d’informations sur la création d’un Assistant compatible Wizard97 sur des systèmes antérieurs, consultez la section assistants à compatibilité descendante, plus loin dans cette rubrique.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions

### <a name="wizard-implementation"></a>Implémentation de l’Assistant

L’implémentation d’un Assistant est semblable à l’implémentation d’une feuille de propriétés régulière. Au niveau le plus simple, il est important de définir l’un des indicateurs ou combinaisons suivants dans la structure [**PROPSHEETHEADER**](pss-propsheetheader.md) qui définit la feuille de propriétés.



| Indicateur                           | Style                                                                                                                                                 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Assistant PSH                    | Assistant simple sans en-tête ni bitmap.                                                                                                           |
| \_Assistant PSH \_ Lite              | Similaire à l' \_ Assistant PSH, avec quelques différences mineures d’apparence ; par exemple, le séparateur au-dessus des boutons est défini sur la largeur totale de la fenêtre. |
| PSH \_ WIZARD97                  | Un Assistant Wizard97 avec des en-têtes (facultatifs), des bitmaps d’en-tête et des filigranes.                                                                            |
| \_Assistant PSH \| PSH \_ AEROWIZARD | Assistant Aero. Les assistants Aero n’utilisent pas les filigranes ni les bitmaps d’en-tête. Ils requièrent le modèle STA (Single-Threaded Apartment).                         |



 

La procédure de base pour l’implémentation d’un Assistant est la suivante :

1.  Créez un modèle de boîte de dialogue pour chaque page.
2.  Définissez les pages en créant une structure [**PROPSHEETPAGE**](pss-propsheetpage.md) pour chaque page. Cette structure définit la page et contient des pointeurs vers le modèle de boîte de dialogue et toutes les bitmaps ou autres ressources.
3.  Transmettez la structure [**PROPSHEETPAGE**](pss-propsheetpage.md) créée à l’étape précédente à la fonction [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) pour créer le descripteur HPROPSHEETPAGE de la page.
4.  Définissez l’Assistant en créant une structure [**PROPSHEETHEADER**](pss-propsheetheader.md) pour celui-ci.
5.  Transmettez la structure [**PROPSHEETHEADER**](pss-propsheetheader.md) à la fonction [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) pour afficher l’Assistant.
6.  Implémentez des procédures de boîte de dialogue pour chaque page pour gérer les messages de notification à partir des contrôles de la page et des boutons de l’Assistant et pour traiter d’autres messages Windows.

### <a name="create-the-dialog-box-templates"></a>Créer les modèles de boîte de dialogue

Il existe deux types de base de page de l’Assistant : extérieur et intérieur. Les pages externes sont l’introduction (Bienvenue) et les pages de saisie semi-automatique. Toutes les autres sont des pages intérieures.

**Modèles de boîte de dialogue page externe**

La disposition de base des pages d’introduction et de fin est identique. L’illustration suivante montre un exemple de page d’introduction Wizard97, avec un filigrane d’espace réservé.

![capture d’écran montrant une page d’Assistant avec un graphique à gauche, le titre et le corps du texte à droite, et les boutons précédent, suivant et annuler en bas](images/wiz97exterior.png)

Pour les pages extérieures Wizard97, le modèle de boîte de dialogue est 317x193 Units Dialog units. Il remplit tout l’Assistant, à l’exception de la légende et de la bande en bas qui contient les boutons **précédent**, **suivant** et **Annuler** . La partie gauche du modèle, qui est réservée à une image bitmap « filigrane », ne doit pas contenir de contrôles. Le filigrane est spécifié dans la structure [**PROPSHEETHEADER**](pss-propsheetheader.md) de l’Assistant et est ajouté automatiquement à la page. Vous devez lui accorder de l’espace lors de la conception du modèle de ressource.

Lorsque vous créez la bitmap de filigrane, gardez à l’esprit que la taille de la boîte de dialogue peut augmenter si, par exemple, l’utilisateur choisit une police système volumineuse. Les différentes langues ont également tendance à avoir des mesures de police différentes. Lorsque la page s’agrandit, la zone réservée pour le filigrane est proportionnellement plus grande. Toutefois, vous ne pouvez pas modifier la bitmap de filigrane, ni la bitmap étirée pour remplir la plus grande zone. Au lieu de cela, la bitmap reste dans sa taille d’origine, dans la partie supérieure gauche de la zone réservée. La partie de la zone réservée la plus grande qui n’est pas couverte par le filigrane est remplie automatiquement avec la couleur du pixel supérieur gauche de la bitmap.

Si vous avez besoin de bitmaps de filigranes de taille différente pour différentes métriques de police, deux solutions possibles sont les suivantes :

-   Récupérez les métriques de police avant de créer l’Assistant et spécifiez une bitmap de filigrane de taille appropriée.
-   Ne spécifiez pas de bitmap de filigrane lors de la création de l’Assistant. Wizard97 laisse la zone de filigrane vide. Dessinez ensuite une bitmap de taille appropriée sur la zone réservée pour le filigrane.

Vous pouvez placer des contrôles dans la zone à droite du filigrane comme vous le feriez pour une boîte de dialogue normale. La couleur d’arrière-plan de cette zone est déterminée par le système et ne nécessite aucune action de votre part. En général, vous placez deux contrôles statiques dans cette zone. La partie supérieure contient le titre et utilise une grande police en gras (12 points Verdana en gras pour Wizard97). L’autre, qui est un texte explicatif, utilise la police de la boîte de dialogue standard.

La principale différence entre les pages d’introduction et de fin est les boutons de l’Assistant et le texte des contrôles statiques. Les pages d’introduction ont normalement un bouton **suivant** et un bouton **précédent** , avec uniquement le bouton **suivant** activé. Le bouton **précédent** est activé pour les pages de saisie semi-automatique et le bouton **suivant** est remplacé par un bouton **Terminer** .

> [!Note]  
> Dans les assistants Aero, le bouton **précédent** est remplacé par un bouton fléché dans la barre de légende.

 

Vous pouvez modifier le texte du bouton **Terminer** en envoyant un message [**\_ SETFINISHTEXT PSM**](psm-setfinishtext.md) à l’Assistant. Par défaut, le bouton **Terminer** n’inclut pas d’accélérateur clavier. Pour définir une touche d’accès rapide, incluez une esperluette dans la chaîne de texte que vous transmettez à PSM \_ SETFINISHTEXT. Par exemple, « &Finish » définit « F » comme touche d’accès rapide.

**Pages intérieures, modèles de boîte de dialogue**

Les pages intérieures ont une apparence quelque peu différente de celle des pages extérieures. L’illustration suivante montre un exemple de page Wizard97 Interior, avec un bitmap d’en-tête d’espace réservé.

![capture d’écran d’une page d’Assistant avec texte du titre et du sous-titre et un graphique en haut, texte au milieu et boutons en bas](images/wiz97interior.png)

La zone d’en-tête en haut de la page est gérée par la feuille de propriétés, de sorte qu’elle n’est pas incluse dans le modèle. Le contenu de l’en-tête est spécifié dans la structure [**PROPSHEETPAGE**](pss-propsheetpage.md) de la page et la structure [**PROPSHEETHEADER**](pss-propsheetheader.md) de l’Assistant. Étant donné que la page intérieure doit tenir entre l’en-tête et les boutons, le modèle de boîte de dialogue Wizard97 est 317x143 unités de boîte de dialogue, un peu plus petit que le modèle pour les pages externes.

L’illustration suivante montre un Assistant Aero créé à partir du même modèle.

![capture d’écran qui diffère de la précédente en ayant une zone de titre en haut, et uniquement les boutons suivant et annuler en bas](images/wizardaerointerior.png)

### <a name="define-the-wizard-pages"></a>Définir les pages de l’Assistant

Une fois que vous avez créé les modèles de boîte de dialogue et les ressources associées, telles que les bitmaps et les tables de chaînes, vous pouvez créer les pages de feuille de propriétés. La procédure est similaire à celle des feuilles de propriétés standard. Tout d’abord, renseignez les membres appropriés d’une structure [**PROPSHEETPAGE**](pss-propsheetpage.md) . (Certains membres sont spécifiques aux assistants.) Appelez ensuite la fonction [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) pour créer le descripteur HPROPSHEETPAGE de la page.

Les indicateurs suivants relatifs à l’Assistant peuvent être définis dans le membre **dwFlags** de la structure [**PROPSHEETPAGE**](pss-propsheetpage.md) .



| Indicateur                   | Description                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| \_HIDEHEADER PSP        | Définissez cet indicateur pour les pages extérieures dans Wizard97. L’en-tête n’est pas affiché et un filigrane peut être affiché.                                |
| \_USEHEADERTITLE PSP    | Définissez cet indicateur pour les pages intérieures pour placer un titre dans la zone d’en-tête dans Wizard97 ou en haut de la zone cliente dans un Assistant Aero. |
| \_USEHEADERSUBTITLE PSP | Définissez cet indicateur pour les pages intérieures pour placer un sous-titre dans la zone d’en-tête dans Wizard97.                                                  |



 

Si vous avez défini PSP \_ USEHEADERTITLE ou PSP \_ USEHEADERSUBTITLE, assignez le titre et le texte du sous-titre aux membres **pszHeaderTitle** et **pszHeaderSubtitle** , respectivement. Lorsque vous assignez des chaînes de texte à des membres des structures [**PROPSHEETPAGE**](pss-propsheetpage.md) et [**PROPSHEETHEADER**](pss-propsheetheader.md) , vous pouvez assigner un pointeur de chaîne ou utiliser la macro **MAKEINTRESOURCE** pour assigner une valeur à partir d’une ressource de type chaîne. La ressource de type chaîne est chargée à partir du module spécifié dans le membre **HINSTANCE** de la structure **PROPSHEETHEADER** de l’Assistant.

Quand vous appelez [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) pour créer une page, assignez le résultat à un élément d’un tableau de handles HPROPSHEETPAGE. Ce tableau est utilisé lors de la création de la feuille de propriétés. L’index de tableau du descripteur d’une page détermine l’ordre par défaut dans lequel il est affiché. Une fois que vous avez créé le descripteur HPROPSHEETPAGE d’une page, vous pouvez réutiliser la même structure [**PROPSHEETPAGE**](pss-propsheetpage.md) pour créer la page suivante en assignant de nouvelles valeurs aux membres appropriés.

Une autre façon de créer des pages consiste à utiliser des structures [**PROPSHEETPAGE**](pss-propsheetpage.md) distinctes pour chaque page et à créer un tableau de structures. Ce tableau est utilisé à la place d’un tableau de handles HPROPSHEETPAGE lors de la création de la feuille de propriétés. L’utilisation de structures **PROPSHEETPAGE** distinctes évite d’avoir à appeler [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) , mais utilise davantage de mémoire. Dans le cas contraire, il n’y a pas de différence significative entre les deux approches.

L’exemple suivant définit une page Wizard97 intérieure en assignant des valeurs à une structure [**PROPSHEETPAGE**](pss-propsheetpage.md) . Dans cet exemple, le titre, le sous-titre et le modèle de boîte de dialogue de la page sont tous identifiés par leur ID de ressource. La fonction [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) est ensuite appelée pour créer le descripteur HPROPSHEETPAGE de la page. Étant donné qu’il s’agit de la deuxième page à afficher, la poignée est assignée au tableau de descripteurs, *ahpsp*, avec un index de 1.


```C++
// g_hInstance is the global HINSTANCE of the application.
// IntPage1DlgProc is the dialog procedure for this page.
// ahpsp is an array of HPROPSHEETPAGE handles.

PROPSHEETPAGE psp = { sizeof(psp) };

psp.hInstance         = g_hInstance;
psp.dwFlags           = PSP_USEHEADERTITLE | PSP_USEHEADERSUBTITLE;
psp.lParam            = (LPARAM) &wizdata;
psp.pszHeaderTitle    = MAKEINTRESOURCE(IDS_TITLE1);
psp.pszHeaderSubTitle = MAKEINTRESOURCE(IDS_SUBTITLE1);
psp.pszTemplate       = MAKEINTRESOURCE(IDD_INTERIOR1);
psp.pfnDlgProc        = IntPage1DlgProc;

ahpsp[1] = CreatePropertySheetPage(&psp);
```



### <a name="custom-page-data"></a>Données de page personnalisées

Lorsque vous créez une page, vous pouvez lui assigner des données personnalisées à l’aide du membre **lParam** de la structure [**PROPSHEETPAGE**](pss-propsheetpage.md) , généralement en lui assignant un pointeur vers une structure définie par l’utilisateur.

Lorsque la page est sélectionnée pour la première fois, sa procédure de boîte de dialogue reçoit un message [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) . La valeur *lParam* du message pointe vers une copie de la structure [**PROPSHEETPAGE**](pss-propsheetpage.md) de la page, à partir de laquelle vous pouvez récupérer les données personnalisées. Vous pouvez ensuite stocker ces données pour les utiliser dans les messages suivants à l’aide de [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) avec GWL \_ UserData comme paramètre d’index. Plusieurs pages peuvent avoir un pointeur vers les mêmes données et toute modification apportée aux données d’une page est disponible pour les autres pages de leurs procédures de dialogue.

### <a name="define-the-wizard-property-sheet"></a>Définir la feuille de propriétés de l’Assistant

Comme avec les feuilles de propriétés ordinaires, vous définissez la feuille de propriétés de l’Assistant en remplissant les membres d’une structure [**PROPSHEETHEADER**](pss-propsheetheader.md) . Cette structure vous permet de spécifier les pages qui composent l’Assistant et l’ordre par défaut dans lequel elles sont affichées, ainsi que plusieurs paramètres associés. Vous lancez ensuite l’Assistant en appelant la fonction [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) .

Dans le style Wizard97, le membre **pszCaption** de la structure [**PROPSHEETHEADER**](pss-propsheetheader.md) est ignoré. Au lieu de cela, l’Assistant affiche la légende qui est spécifiée dans le modèle de boîte de dialogue de la page active. Si le modèle ne possède pas de légende, la légende de la page précédente s’affiche. Ainsi, pour afficher la même légende dans toutes les pages, spécifiez la légende dans le modèle pour la page d’introduction.

Dans le style de l’Assistant Aero, la légende de la boîte de dialogue est extraite de **pszCaption**.

Si vous avez créé un tableau de handles HPROPSHEETPAGE pour vos pages, assignez le tableau au membre **phpage** . Si vous avez créé un tableau de structures [**PROPSHEETPAGE**](pss-propsheetpage.md) à la place, assignez le tableau au membre **PPSP** et définissez l' \_ indicateur PROPSHEETPAGE PSH dans le membre **dwFlags** .

L’exemple suivant affecte des valeurs à *PSH*, à une structure [**PROPSHEETHEADER**](pss-propsheetheader.md) , et appelle la fonction [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) pour lancer l’Assistant. L’Assistant de style Wizard97 contient à la fois des graphiques en filigrane et en-tête, spécifiés par leur ID de ressource. Le tableau *ahpsp* contient tous les handles HPROPSHEETPAGE et définit l’ordre par défaut dans lequel ils sont affichés.


```C++
// g_hInstance is the global HINSTANCE of the application.
// ahpsp is an array of HPROPSHEETPAGE handles.

PROPSHEETHEADER psh = { sizeof(psh) };

psh.hInstance      = g_hInstance;
psh.hwndParent     = NULL;
psh.phpage         = ahpsp;
psh.dwFlags        = PSH_WIZARD97 | PSH_WATERMARK | PSH_HEADER;
psh.pszbmWatermark = MAKEINTRESOURCE(IDB_WATERMARK);
psh.pszbmHeader    = MAKEINTRESOURCE(IDB_BANNER);
psh.nStartPage     = 0;
psh.nPages         = 4;

PropertySheet(&psh);
```



### <a name="the-dialog-box-procedure"></a>La procédure de la boîte de dialogue

Chaque page de l’Assistant a besoin d’une procédure de boîte de dialogue pour traiter les messages Windows, en particulier les notifications de ses contrôles et de l’Assistant. Les trois messages que presque tous les assistants doivent pouvoir gérer sont [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog), [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy)et [**WM \_ Notify**](wm-notify.md).

Le message [**WM \_ Notify**](wm-notify.md) est reçu avant l’affichage de la page et l’utilisateur clique sur l’un des boutons de l’Assistant. Le paramètre *lParam* du message est un pointeur vers une structure d’en-tête [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) . L’ID de la notification est contenu dans le membre de **code** de la structure. Les quatre notifications que la plupart des assistants doivent gérer sont les suivantes.



| Code                                | Description                                 |
|-------------------------------------|---------------------------------------------|
| [PSN \_](psn-setactive.md) | Envoyé avant l’affichage de la page.          |
| [PSN \_ WIZBACK](psn-wizback.md)     | Envoyé lorsque l’utilisateur clique sur le bouton **précédent** .   |
| [PSN \_ WIZNEXT](psn-wiznext.md)     | Envoyé lorsque l’utilisateur clique sur le bouton **suivant** .   |
| [PSN \_ WIZFINISH](psn-wizfinish.md) | Envoyé lorsque l’utilisateur clique sur le bouton **Terminer** . |



 

### <a name="handle-wm_initdialog-and-wm_destroy"></a>Gérer WM \_ INITDIALOG et WM \_ Destroy

Quand une page est sur le point d’être affichée pour la première fois, la procédure de la boîte de dialogue reçoit un message [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) . La gestion de ce message permet à l’Assistant d’effectuer toutes les tâches d’initialisation nécessaires, telles que le stockage de données personnalisées ou la définition de polices.

Lorsque la feuille de propriétés est détruite, vous recevez un message [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) . L’Assistant est automatiquement détruit par le système, mais le traitement de ce message vous permet d’effectuer les nettoyages nécessaires.

### <a name="handle-psn_setactive"></a>Gérer PSN \_ SEtactive

Le [code \_ de notification PSN](psn-setactive.md) est envoyé chaque fois qu’une page est sur le point d’être affichée. La première fois qu’une page est visitée, PSN \_ SEtactive suit le message [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) . Si la page est revisitée par la suite, elle reçoit uniquement une \_ notification SEtactive PSN. Cette notification est généralement gérée pour initialiser les données de la page et activer les boutons appropriés.

Par défaut, l’Assistant affiche les boutons **précédent**, **suivant** et **Annuler** , avec tous les boutons activés. Pour désactiver un bouton ou afficher la **fin** au lieu de la **prochaine**, vous devez envoyer un message [**\_ SETWIZBUTTONS PSM**](psm-setwizbuttons.md) . Une fois que ce message a été envoyé, l’état des boutons est conservé jusqu’à ce qu’il soit modifié par un autre message **\_ SETWIZBUTTONS PSM** , même si une nouvelle page est sélectionnée. En règle générale, tous les gestionnaires [PSN \_ setacteurs](psn-setactive.md) envoient ce message pour s’assurer que chaque page a l’état de bouton correct.

Vous pouvez modifier l’état du bouton avec ce message à tout moment. Par exemple, vous souhaiterez peut-être désactiver initialement le bouton **suivant** . Une fois qu’un utilisateur a entré toutes les informations nécessaires, vous pouvez envoyer un autre message [**\_ SETWIZBUTTONS PSM**](psm-setwizbuttons.md) pour activer le bouton **suivant** et permettre à l’utilisateur de passer à la page suivante.

Le fragment de code suivant utilise la macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) pour activer les boutons **précédent** et **suivant** sur une page intérieure avant qu’elle ne soit affichée.


```C++
case WM_NOTIFY :
    {
        LPNMHDR pnmh = (LPNMHDR)lParam;
        
        switch(pnmh->code)
        {
        
        ...
        
        case PSN_SETACTIVE :
        
            ...
            
            // This is an interior page.
            PropSheet_SetWizButtons(hwnd, PSWIZB_NEXT | PSWIZB_BACK);
            
            ...
        }
    ...
    
    }
```



### <a name="handle-psn_wiznext-psnwizback-and-psn_wizfinish"></a>Gérer PSN \_ WIZNEXT, PSNWIZBACK et PSN \_ WIZFINISH

Quand vous cliquez sur un bouton **suivant** ou **précédent** , vous recevez un code de notification [PSN \_ WIZNEXT](psn-wiznext.md) ou [PSN \_ WIZBACK](psn-wizback.md) . Par défaut, l’Assistant passe automatiquement à la page suivante ou précédente dans l’ordre défini lors de la création de la feuille de propriétés. Une raison courante pour gérer ces notifications est d’empêcher l’utilisateur de changer de page ou de remplacer l’ordre des pages par défaut.

Pour empêcher l’utilisateur de changer de page, gérez la notification du bouton, appelez la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec la \_ valeur-1 de la propriété DWL MSGRESULT, et retournez la valeur **true**. Par exemple :


```C++
case PSN_WIZNEXT :

        ...
        
        // Do not go to the next page yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, -1);
        
        return TRUE;
        
        ...
```



Pour remplacer l’ordre standard et accéder à une page particulière, appelez [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec la \_ valeur MSGRESULT de la page DWL définie sur l’ID de ressource de la boîte de dialogue de la page, puis renvoyez **true**. Par exemple :


```C++
case PSN_WIZNEXT :

        ...
        
        // Go straight to the completion page.
        SetWindowLong(hwnd, DWL_MSGRESULT, IDD_FINISH);
        
        return TRUE;
        
        ...
```



Lorsque l’utilisateur clique sur le bouton **Terminer** ou **Annuler** , vous recevez un code de notification de [ \_ réinitialisation](psn-reset.md) [PSN \_ WIZFINISH](psn-wizfinish.md) ou PSN, respectivement. Lorsque vous cliquez sur l’un de ces boutons, l’Assistant est automatiquement détruit par le système. Toutefois, vous pouvez gérer ces notifications si vous devez effectuer des tâches de nettoyage avant la destruction de l’Assistant. Pour empêcher la destruction de l’Assistant lorsque vous recevez une \_ notification PSN WIZFINISH, appelez [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec la \_ valeur de MSGRESULT DWL définie sur **true**, puis revenez à **true**. Par exemple :


```C++
case PSN_WIZFINISH :

        ...
        
        // Not finished yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, TRUE);
        
        return TRUE;
        
        ...
```



### <a name="backward-compatible-wizards"></a>Assistants à compatibilité descendante

La section précédente suppose que vous implémentez un Assistant pour un système avec la [version 5](common-control-versions.md) ou ultérieure des contrôles communs.

Si vous écrivez un Assistant pour des systèmes avec des versions antérieures des contrôles communs, la plupart des fonctionnalités décrites dans la section précédente ne seront pas disponibles. Un certain nombre de membres des structures [**PROPSHEETHEADER**](pss-propsheetheader.md) et [**PROPSHEETPAGE**](pss-propsheetpage.md) qui sont utilisés par le style Wizard97 sont pris en charge uniquement par les contrôles communs version 5 et ultérieures. Toutefois, il est toujours possible d’implémenter un assistant à *compatibilité descendante* avec une apparence similaire à celle du style Wizard97. Pour ce faire, vous devez implémenter explicitement les éléments suivants :

-   Ajoutez le graphique en filigrane au modèle de boîte de dialogue pour vos pages d’introduction et de fin.
-   Modifiez la taille de tous vos modèles. Il n’existe pas de zone d’en-tête définie par le système distincte pour les pages intérieures.
-   Créez explicitement la zone d’en-tête de la page intérieure sur vos modèles.
-   N’utilisez pas de graphique d’en-tête, car il peut être en conflit avec le titre ou le sous-titre si l’Assistant change de taille.

Pour plus d’informations sur les assistants à compatibilité descendante, consultez Assistant à compatibilité [descendante 97](/previous-versions//ms737910(v=vs.85)).

## <a name="remarks"></a>Notes

Pour une présentation complète des problèmes de conception pour Wizard97, consultez la [spécification Wizard97](/previous-versions//ms738248(v=vs.85)), ailleurs dans le SDK Windows. Ce document contient des instructions pour des éléments tels que les dimensions des boîtes de dialogue, les dimensions et les couleurs de la bitmap et le positionnement des contrôles.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des feuilles de propriétés](using-property-sheets.md)
</dt> <dt>

[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 