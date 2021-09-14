---
title: À propos des feuilles de propriétés
description: Une feuille de propriétés est une fenêtre qui permet à l’utilisateur d’afficher et de modifier les propriétés d’un élément.
ms.assetid: 93676a64-7980-48cd-8615-23b14a118e1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3256959b588e2109740033692c0c528889fc939f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117561"
---
# <a name="about-property-sheets"></a>À propos des feuilles de propriétés

Une *feuille de propriétés* est une fenêtre qui permet à l’utilisateur d’afficher et de modifier les propriétés d’un élément. Par exemple, une application de feuille de calcul peut utiliser une feuille de propriétés pour permettre à l’utilisateur de définir les propriétés de police et de bordure d’une cellule ou pour afficher et définir les propriétés d’un périphérique, tel qu’un lecteur de disque, une imprimante ou une souris.

Cette section décrit les rubriques suivantes.

-   [Notions de base de la feuille de propriétés](#property-sheet-basics)
-   [Boîtes de dialogue de la feuille de propriétés](#property-sheet-dialog-boxes)
-   [Pages](#pages)
-   [Création de la feuille de propriétés](#property-sheet-creation)
-   [Ajout et suppression de pages](#adding-and-removing-pages)
-   [Titre et étiquettes de page de la feuille de propriétés](#property-sheet-title-and-page-labels)
-   [Activation de page](#page-activation)
-   [Bouton aide](#help-button)
    -   [Suppression du bouton d’aide barre de légende](#removing-the-caption-bar-help-button)
-   [Boutons OK, annuler et appliquer](#ok-cancel-and-apply-buttons)
-   [Assistants](#wizards)

## <a name="property-sheet-basics"></a>Notions de base de la feuille de propriétés

Pour implémenter les feuilles de propriétés dans votre application, incluez le fichier d’en-tête Prsht. h dans votre projet. Prsht. h contient tous les identificateurs utilisés avec les feuilles de propriétés.

Une feuille de propriétés contient une ou plusieurs fenêtres enfants qui se chevauchent, appelées pages, chacune contenant des fenêtres de contrôle pour la définition d’un groupe de propriétés associées. Par exemple, une page peut contenir les contrôles permettant de définir les propriétés de police d’un élément, notamment le style de type, la taille du point, la couleur, etc. Chaque page comporte un onglet que l’utilisateur peut sélectionner pour amener la page au premier plan de la feuille de propriétés. Par exemple, l' Date-Time application du panneau de configuration affiche la feuille de propriétés suivante.

![capture d’écran d’une feuille de propriétés avec deux onglets, l’un d’entre eux montrant une horloge et un contrôle calendrier mensuel](images/propsheet1.png)

Une feuille de propriétés standard avec plusieurs pages avec onglets permet à l’utilisateur d’accéder de manière aléatoire à toutes les propriétés. S’il est plus approprié d’avoir des propriétés définies en séquence, vous pouvez utiliser un [Assistant](#wizards).

## <a name="property-sheet-dialog-boxes"></a>Boîtes de dialogue de la feuille de propriétés

Une feuille de propriétés et les pages qu’elle contient sont en fait des boîtes de dialogue. La feuille de propriétés est une boîte de dialogue définie par le système qui gère les pages et fournit un conteneur commun pour eux. Une boîte de dialogue de feuille de propriétés peut être modale ou non modale. Il comprend un cadre, une barre de titre et quatre boutons : **OK**, **Annuler**, **appliquer** et (éventuellement) de **l’aide**. Les procédures de la boîte de dialogue pour les pages reçoivent des codes de notification sous la forme de messages [**WM \_ Notify**](wm-notify.md) quand l’utilisateur clique sur les boutons.

> [!NOTE]  
> Toutes les informations contenues dans cette section ne s’appliquent pas aux assistants, qui ont une apparence et un comportement légèrement différents. Par exemple, les assistants ont un ensemble différent de boutons et aucun onglet. Pour plus d’informations, consultez [création d’assistants](wizards.md).

Chaque page d’une feuille de propriétés est une boîte de dialogue non modale définie par l’application qui gère les fenêtres de contrôle utilisées pour afficher et modifier les propriétés d’un élément. Vous fournissez le modèle de boîte de dialogue utilisé pour créer chaque page, ainsi que la procédure de boîte de dialogue qui gère les contrôles et définit les propriétés de l’élément correspondant.

Une feuille de propriétés envoie des codes de notification à la procédure de boîte de dialogue pour une page lorsque la page obtient ou perd l’activation et lorsque l’utilisateur clique sur le bouton **OK**, **Annuler**, **appliquer** ou **aide** . Les notifications sont envoyées sous la forme de messages de [**\_ notification WM**](wm-notify.md) . Le paramètre *lParam* est l’adresse d’une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui comprend le handle de fenêtre dans la boîte de dialogue feuille de propriétés.

Certains codes de notification requièrent qu’une page retourne la **valeur true** ou **false** en réponse au message [**WM \_ Notify**](wm-notify.md) . Pour ce faire, la page doit utiliser la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) pour affecter la valeur **true** ou **false** à la valeur **\_ MSGRESULT** de la boîte de dialogue de la page.

## <a name="pages"></a>Pages

une feuille de propriétés doit contenir au moins une page, mais elle ne peut pas contenir plus de valeurs que la valeur de **MAXPROPPAGES** , comme défini dans les fichiers d’en-tête Windows. Chaque page a un index de base zéro que la feuille de propriétés attribue en fonction de l’ordre dans lequel la page est ajoutée à la feuille de propriétés. Les index sont utilisés dans les messages que vous envoyez à la feuille de propriétés.

Une page de propriétés peut contenir une boîte de dialogue imbriquée. Si c’est le cas, vous devez inclure le style [**WS \_ ex \_ CONTROLPARENT**](/windows/desktop/winmsg/extended-window-styles) pour la boîte de dialogue de niveau supérieur et appeler la fonction [**IsDialogMessage**](/windows/desktop/api/winuser/nf-winuser-isdialogmessagea) avec le descripteur de la boîte de dialogue parente. Cela permet de s’assurer que l’utilisateur peut utiliser des mnémoniques et les touches de navigation de la boîte de dialogue pour déplacer le focus sur les contrôles de la boîte de dialogue imbriquée.

Chaque page comporte une icône et une étiquette correspondantes. La feuille de propriétés crée un onglet pour chaque page et affiche l’icône et l’étiquette dans l’onglet. Toutes les pages de feuille de propriétés sont censées utiliser une police qui n’est pas en gras. Pour vous assurer que la police n’est pas en gras, spécifiez le style **DS \_ 3DLOOK** dans le modèle de boîte de dialogue.

La procédure de boîte de dialogue pour une page ne doit pas appeler la fonction [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) . Cela entraînera la suppression de la feuille de propriétés entière, pas seulement de la page.

La taille minimale d’une page de feuille de propriétés est 212 unités de boîte de dialogue horizontalement et 114 unités de boîte de dialogue verticalement. Si une boîte de dialogue de page est plus petite, la page est agrandie jusqu’à ce qu’elle atteigne la taille minimale. Le fichier d’en-tête Prsht. h contient trois ensembles de tailles recommandées pour les pages de feuille de propriétés, comme indiqué dans le tableau suivant.

|  Taille                |   Description                                                   |
|----------------------|-----------------------------------------------------------------|
| **PROP \_ SM \_ CXDLG**  | Largeur, en unités de boîte de dialogue, d’une petite page de feuille de propriétés.         |
| **PROP \_ SM \_ CYDLG**  | Hauteur, en unités de boîte de dialogue, d’une petite page de feuille de propriétés.        |
| **PROP \_ med \_ CXDLG** | Largeur, en unités de boîte de dialogue, d’une page de feuille de propriétés de taille moyenne.  |
| **PROP \_ med \_ CYDLG** | Hauteur, en unités de boîte de dialogue, d’une page de feuille de propriétés de taille moyenne. |
| **PROP \_ LG \_ CXDLG**  | Largeur, en unités de boîte de dialogue, d’une grande page de feuille de propriétés.         |
| **PROP \_ LG \_ CYDLG**  | Hauteur, en unités de boîte de dialogue, d’une grande page de feuille de propriétés.        |

l’utilisation de ces tailles recommandées permet de garantir la cohérence visuelle entre votre application et d’autres applications Microsoft Windows.

dans l’éditeur de ressources Microsoft Visual Studio, vous pouvez créer une page de la taille appropriée dans la boîte de dialogue **ajouter une ressource** . Développez le nœud de la boîte de dialogue et sélectionnez **IDD \_ PropPage \_ large**, **IDD \_ PropPage \_ Medium** ou **IDD \_ PropPage \_ Small**.

La feuille de propriétés est automatiquement dimensionnée pour s’adapter à la plus grande page.

## <a name="property-sheet-creation"></a>Création de la feuille de propriétés

Avant de créer une feuille de propriétés, vous devez définir une ou plusieurs pages. Cela implique de remplir une structure [**PROPSHEETPAGE**](pss-propsheetpage.md) avec des informations sur la page (icône, étiquette, modèle de boîte de dialogue, procédure de boîte de dialogue, etc.), puis en spécifiant l’adresse de la structure dans un appel à la fonction [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) . La fonction retourne un handle vers le type HPROPSHEETPAGE qui identifie de façon unique la page.

Pour créer une feuille de propriétés, vous spécifiez l’adresse d’une structure [**PROPSHEETHEADER**](pss-propsheetheader.md) dans un appel à la fonction [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) . La structure définit l’icône et le titre de la feuille de propriétés et comprend également l’adresse d’un tableau de handles HPROPSHEETPAGE que vous obtenez à l’aide de [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea). Quand **feuille** crée la feuille de propriétés, il comprend les pages identifiées dans le tableau. Les pages s’affichent dans la feuille de propriétés dans l’ordre dans lequel elles sont contenues dans le tableau.

Une autre façon d’assigner des pages à une feuille de propriétés consiste à spécifier un tableau de structures [**PROPSHEETPAGE**](pss-propsheetpage.md) au lieu d’un tableau de handles **HPROPSHEETPAGE** . Dans ce cas, [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) crée des handles pour les pages avant de les ajouter à la feuille de propriétés.

Lorsqu’une page est créée, sa procédure de boîte de dialogue reçoit un message [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) . Le paramètre *lParam* du message est un pointeur vers une copie de la structure [**PROPSHEETPAGE**](pss-propsheetpage.md) qui est définie lors de la création de la page. En particulier, quand une page est créée, le membre **lParam** de la structure peut être utilisé pour passer des informations définies par l’application à la procédure de boîte de dialogue. À l’exception du membre **lParam** , cette structure doit être traitée en lecture seule. Toute modification autre que **lParam** aura des conséquences imprévisibles.

Lorsque le système passe par la suite une copie de la structure [**PROPSHEETPAGE**](pss-propsheetpage.md) de la page à votre application, il utilise le même pointeur. Toutes les modifications apportées à la structure seront transmises. Étant donné que le membre **lParam** est ignoré par le système, il peut être modifié pour envoyer des informations à d’autres parties de votre application. Vous pouvez, par exemple, utiliser **lParam** pour transmettre des informations à la fonction de rappel [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) de la page.

[**Feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) définit automatiquement la taille et la position initiale d’une feuille de propriétés. La position est basée sur la position de la fenêtre propriétaire, et la taille est basée sur la plus grande page spécifiée dans le tableau de pages lors de la création de la feuille de propriétés. Si vous souhaitez que les pages correspondent à la largeur des quatre boutons au bas de la feuille de propriétés, définissez la largeur de la page la plus large sur 190 unités de boîte de dialogue.

La taille d’une feuille de propriétés est calculée à partir des propriétés *Width* et *Height* du modèle de boîte de dialogue dans le fichier de ressources. Pour plus d’informations, consultez ressource de [**boîte de dialogue**](/windows/desktop/menurc/dialog-resource) ou [**ressource DIALOGEX**](/windows/desktop/menurc/dialogex-resource) . Notez, toutefois, que pour des raisons de compatibilité, les dimensions sont calculées par rapport à la police MS Shell Dlg et non à la police utilisée par la page. Si vous concevez une page qui utilise une autre police, vous pouvez utiliser l’une des suggestions suivantes.

-   Ajustez les dimensions du modèle de boîte de dialogue pour compenser la différence de taille entre la police MS Shell Dlg et la police réellement utilisée par la page. Par exemple, si vous choisissez une police qui est deux fois plus large que MS Shell Dlg, définissez la propriété Width du modèle de boîte de dialogue sur deux fois l’utilisation normale.
-   Utilisez un modèle [**DIALOGEX**](/windows/desktop/menurc/dialogex-resource) et définissez le style de boîte de dialogue **\_ SHELLFONT DS** . Dans ce cas, le gestionnaire de feuille de propriétés interprète les dimensions du modèle de boîte de dialogue par rapport à la police utilisée par le modèle de boîte de dialogue.

## <a name="adding-and-removing-pages"></a>Ajout et suppression de pages

Après la création d’une feuille de propriétés, une application peut ajouter une page à la fin de l’ensemble de pages existant en envoyant un message de la [**\_ ADDPAGE PSM**](psm-addpage.md) . Pour insérer une page entre des pages existantes, envoyez un message [**PropSheet \_ InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) . Notez que la taille de la feuille de propriétés ne peut pas être modifiée une fois qu’elle a été créée. Les pages ajoutées ou insérées ne doivent pas être supérieures à la plus grande page actuellement dans la feuille de propriétés. Pour supprimer une page, envoyez un message [**PSM \_ REMOVEPAGE**](psm-removepage.md) .

Lorsque vous définissez une page, vous pouvez spécifier l’adresse d’une fonction de rappel [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) que la feuille de propriétés appelle lors de la création ou de la suppression de la page. L’utilisation de *PropSheetPageProc* vous donne la possibilité d’effectuer des opérations d’initialisation et de nettoyage pour des pages individuelles.

> [!NOTE]  
> Un certain nombre de messages et un appel de fonction se produisent pendant que la feuille de propriétés manipule la liste de pages. Pendant cette action, toute tentative de modification de la liste de pages aura des résultats imprévisibles. n’ajoutez pas, n’insérez pas ou ne supprimez pas de pages dans votre implémentation de [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka), ou pendant la gestion des notifications et des messages d’Windows suivants.
>
> -   [PSN \_ appliquer](psn-apply.md)
> -   [PSN \_ KILLACTIVE](psn-killactive.md)
> -   [\_réinitialisation PSN](psn-reset.md)
> -   [PSN \_](psn-setactive.md)
> -   [PSN \_ WIZBACK](psn-wizback.md)
> -   [PSN \_ WIZNEXT](psn-wiznext.md)
> -   [**\_INITDIALOG WM**](/windows/desktop/dlgbox/wm-initdialog)
> -   [**\_destructeur WM**](/windows/desktop/winmsg/wm-destroy)

si vous avez besoin de modifier une page de feuille de propriétés alors que vous gérez l’un de ces messages ou que [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) est en cours d’exécution, publiez un message de Windows privé. Votre application ne recevra pas ce message avant que le gestionnaire de feuille de propriétés ait terminé ses tâches. à ce stade, il est possible de modifier la liste des pages en toute sécurité.

Lorsqu’une feuille de propriétés est détruite, elle détruit automatiquement toutes les pages qui y ont été ajoutées. Les pages sont détruites dans l’ordre inverse de celles spécifiées dans le tableau utilisé pour créer les pages. Pour détruire une page qui a été créée par la fonction [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) mais qui n’a pas été ajoutée à la feuille de propriétés, utilisez la fonction [**DestroyPropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-destroypropertysheetpage) .

## <a name="property-sheet-title-and-page-labels"></a>Titre et étiquettes de page de la feuille de propriétés

Vous spécifiez le titre d’une feuille de propriétés dans la structure [**PROPSHEETHEADER**](pss-propsheetheader.md) utilisée pour créer la feuille de propriétés. Si le membre **dwFlags** inclut la valeur **PSH \_ PROPTITLE** , la feuille de propriétés ajoute le suffixe "Properties" ou le préfixe "Properties for", en fonction de la version. Vous pouvez modifier le titre après la création d’une feuille de propriétés à l’aide du message [**PSM \_ SETTITLE**](psm-settitle.md) . Dans un Assistant Aero, ce message peut être utilisé pour modifier le titre d’une page intérieure de manière dynamique.

Par défaut, une feuille de propriétés utilise la chaîne de nom spécifiée dans le modèle de boîte de dialogue en tant qu’étiquette d’une page. Vous pouvez remplacer la chaîne de nom en incluant la valeur **PSP \_ USETITLE** dans le membre **DwFlags** de la structure [**PROPSHEETPAGE**](pss-propsheetpage.md) qui définit la page. Quand **PSP \_ USETITLE** est spécifié, le membre **pszTitle** doit contenir l’adresse de la chaîne d’étiquette pour la page.

## <a name="page-activation"></a>Activation de page

Une feuille de propriétés ne peut avoir qu’une seule page active à la fois. La page qui a l’activation est au premier plan de la pile de pages qui se chevauche. L’utilisateur active une page en sélectionnant son onglet. une application active une page à l’aide du message [**PSM \_ SETCURSEL**](psm-setcursel.md) .

La feuille de propriétés envoie le code de notification [PSN \_ KILLACTIVE](psn-killactive.md) à la page qui va perdre l’activation. En réponse, la page doit valider toutes les modifications apportées par l’utilisateur à la page. Si la page requiert une entrée d’utilisateur supplémentaire avant de perdre l’activation, utilisez la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) pour définir la valeur de la **\_ MSGRESULT au DWL** de la page sur **true**. En outre, la page doit afficher une boîte de message qui décrit le problème et fournit l’action recommandée. Affectez la valeur **false** à **DWL \_ MSGRESULT** lorsqu’il est possible de perdre l’activation.

Avant que la page qui obtient l’activation ne soit visible, la feuille de propriétés envoie le code de notification [ \_ SetActive PSN](psn-setactive.md) à la page. La page doit répondre en initialisant ses fenêtres de contrôle.

## <a name="help-button"></a>Bouton aide

Les feuilles de propriétés peuvent afficher deux boutons d’aide : un bouton d’aide de feuille de propriétés qui s’affiche en bas du cadre, à côté des boutons **OK** / **Annuler** l' / **application** et un bouton de barre de légende standard qui fournit de l’aide contextuelle.

Le bouton aide de la feuille de propriétés est facultatif et peut être activé sur une page par page. Pour afficher le bouton d’aide de la feuille de propriétés pour une ou plusieurs pages :

-   Définissez l' **indicateur \_ HasHelp PSH** dans le membre **DwFlags** de la structure [**PROPSHEETHEADER**](pss-propsheetheader.md) de la feuille de propriétés.
-   Pour chaque page qui affiche un bouton aide, définissez l’indicateur **de \_ HasHelp HasHelp** dans le membre **DwFlags** de la structure [**PROPSHEETPAGE**](pss-propsheetpage.md) de la page.

Quand l’utilisateur clique sur le bouton aide, la page active reçoit un code de notification [ \_ d’aide PSN](psn-help.md) . La page doit répondre en affichant des informations d’aide, généralement en appelant la fonction [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) .

### <a name="removing-the-caption-bar-help-button"></a>Suppression du bouton d’aide barre de légende

Le bouton aide de la barre de légende s’affiche par défaut, afin que l’aide contextuelle soit toujours disponible pour les boutons OK/Annuler/appliquer. Toutefois, ce bouton peut être supprimé, si nécessaire. Pour supprimer le bouton d’aide de la barre de légende d’une feuille de propriétés :

-   Pour les versions des contrôles communs antérieures à la [version 5,80](common-control-versions.md), vous devez implémenter une fonction de rappel de la [**feuille de propriétés**](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback).
-   Pour la [version 5,80](common-control-versions.md) et les versions ultérieures des contrôles communs, vous pouvez simplement définir l' \_ indicateur PSH NOCONTEXTHELP dans le membre **DwFlags** de la structure [**PROPSHEETHEADER**](pss-propsheetheader.md) de la feuille de propriétés. Toutefois, si vous avez besoin d’une compatibilité descendante avec les versions de contrôle courantes antérieures, vous devez implémenter la fonction de rappel.

Pour implémenter une fonction de rappel de feuille de propriétés qui supprime le bouton d’aide barre de légende :

-   Définissez l’indicateur **PSH \_ USECALLBACK** dans le membre **DwFlags** de la structure [**PROPSHEETHEADER**](pss-propsheetheader.md) de la feuille de propriétés.
-   Définissez le membre **pfnCallBack** de la structure [**PROPSHEETHEADER**](pss-propsheetheader.md) pour qu’il pointe vers la fonction de rappel.
-   Implémentez la fonction de rappel. Lorsque cette fonction reçoit le message de **\_ précréation PSCB** , elle reçoit également un pointeur vers le modèle de boîte de dialogue de la feuille de propriétés. Supprimez le style **DS \_ CONTEXTHELP** de ce modèle.

L’exemple suivant montre comment implémenter une telle fonction de rappel :

```cpp
int CALLBACK RemoveContextHelpProc(HWND hwnd, UINT message, LPARAM lParam)
{
    switch (message) 
    {
    case PSCB_PRECREATE:
        // Remove the DS_CONTEXTHELP style from the
        // dialog box template
        if (((LPDLGTEMPLATEEX)lParam)->signature ==    
           0xFFFF)
           {
            ((LPDLGTEMPLATEEX)lParam)->style 
            &= ~DS_CONTEXTHELP;
        }
        else {
            ((LPDLGTEMPLATE)lParam)->style 
            &= ~DS_CONTEXTHELP;
        }
        return TRUE;
    }
    return TRUE;
}
```

Si la structure [**DLGTEMPLATEEX**](/windows/desktop/dlgbox/dlgtemplateex) n’est pas définie, incluez la déclaration suivante :

```cpp
#include <pshpack1.h>

typedef struct DLGTEMPLATEEX
{
    WORD dlgVer;
    WORD signature;
    DWORD helpID;
    DWORD exStyle;
    DWORD style;
    WORD cDlgItems;
    short x;
    short y;
    short cx;
    short cy;
} DLGTEMPLATEEX, *LPDLGTEMPLATEEX;

#include <poppack.h>
```

## <a name="ok-cancel-and-apply-buttons"></a>Boutons OK, annuler et appliquer

Les boutons **OK** et **appliquer** sont similaires. dirigent les pages d’une feuille de propriétés pour valider et appliquer les modifications de propriété apportées par l’utilisateur. La seule différence est que le fait de cliquer sur le bouton **OK** entraîne la destruction de la feuille de propriétés après l’application des modifications.

Quand l’utilisateur clique sur le bouton **OK** ou **appliquer** , la feuille de propriétés envoie une notification [PSN \_ KILLACTIVE](psn-killactive.md) à la page active, ce qui lui donne la possibilité de valider les modifications de l’utilisateur. Si les modifications sont valides, la page doit appeler la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec la valeur **DWL \_ MSGRESULT** définie sur **false**. Si les modifications de l’utilisateur ne sont pas valides, la page doit définir la propriété **DWL \_ MSGRESULT** sur **true** et afficher une boîte de dialogue qui informe l’utilisateur du problème. La page reste active jusqu’à ce qu’elle affecte à **\_ MSGRESULT** la **valeur false** en réponse à un \_ message PSN KILLACTIVE.

Une fois qu’une page répond à une notification [PSN \_ KILLACTIVE](psn-killactive.md) en affectant à la propriété **DWL \_ MSGRESULT** la **valeur false**, la feuille de propriétés envoie une notification d' [ \_ application PSN](psn-apply.md) à chaque page. Quand une page reçoit cette notification, elle doit appliquer les nouvelles propriétés à l’élément correspondant. Pour indiquer à la feuille de propriétés que les modifications sont valides pour la page, appelez [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec **DWL \_ MSGRESULT** défini sur **PSNRET \_ NOERROR**. Si les modifications ne sont pas valides pour la page, retournez une erreur. Cela empêche la modification de la feuille de propriétés et retourne le focus sur la page qui a reçu la \_ notification d’application PSN ou sur la page qui avait le focus lorsque le bouton **appliquer** était enfoncé. Pour retourner une erreur et indiquer la page qui recevra le focus, définissez la valeur de l' **\_ MSGRESULT** au point de contrôle DWL sur l’une des valeurs suivantes.

-   **PSNRET \_ NON valide**. La feuille de propriétés ne sera pas détruite et le focus sera renvoyé à cette page.
-   **PSNRET \_ \_NOCHANGEPAGE non valide**. La feuille de propriétés ne sera pas détruite et le focus sera retourné à la page qui avait le focus lorsque le bouton était enfoncé.

Une application peut utiliser le message d’application [**PSM \_**](psm-apply.md) pour simuler la sélection du bouton **appliquer** .

Le bouton **appliquer** est initialement désactivé lorsqu’une page devient active, ce qui indique qu’il n’y a pas encore de modification de propriété à appliquer. Lorsque la page reçoit une entrée via l’un de ses contrôles indiquant que l’utilisateur a modifié une propriété, la page doit envoyer le message [**PSM \_ modifié**](psm-changed.md) à la feuille de propriétés. Le message entraîne l’activation du bouton **appliquer** par la feuille de propriétés. Si l’utilisateur clique ensuite sur le bouton **appliquer** ou **Annuler** , la page doit réinitialiser ses contrôles, puis envoyer le message [**PSM non \_ modifié**](psm-unchanged.md) pour désactiver à nouveau le bouton **appliquer** .

Parfois, le bouton **appliquer** entraîne une modification d’une page dans une feuille de propriétés, et la modification ne peut pas être annulée. Dans ce cas, la page doit envoyer le [**message \_ CANCELTOCLOSE PSM**](psm-canceltoclose.md) à la feuille de propriétés. Le message amène la feuille de propriétés à remplacer le texte du bouton **OK** par « Close », ce qui indique que les modifications appliquées ne peuvent pas être annulées.

parfois, une page apporte une modification à la configuration système qui nécessite le redémarrage de Windows ou le système redémarré pour que la modification puisse prendre effet. Une fois cette modification apportée, une page doit envoyer le message [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) ou [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md) à la feuille de propriétés. Ces messages font en sorte que la fonction [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) retourne la valeur **ID \_ PSRESTARTWINDOWS** ou **ID \_ PSREBOOTSYSTEM** après la destruction de la feuille de propriétés.

Quand un utilisateur clique sur le bouton **Annuler** , la feuille de propriétés envoie le code de notification de [ \_ réinitialisation PSN](psn-reset.md) à toutes les pages, indiquant que la feuille de propriétés va être détruite. Une page doit utiliser la notification pour effectuer des opérations de nettoyage.

## <a name="wizards"></a>Assistants

Un Assistant est un type spécial de feuille de propriétés. Les assistants sont conçus pour présenter les pages une à la fois dans une séquence contrôlée par l’application. Au lieu de sélectionner à partir d’un groupe de pages en cliquant sur un onglet, les utilisateurs naviguent vers l’avant et vers l’arrière dans la séquence, une page à la fois, en cliquant sur les boutons. Par exemple, la capture d’écran suivante montre la page d’accueil de l’Assistant Ajout de matériel :

![capture d’écran de la page d’accueil d’un Assistant](images/wizard97.png)

la capture d’écran suivante montre la première page d’un assistant Aero, le nouveau style introduit dans Windows Vista.

![capture d’écran de la première page d’un Assistant Aero](images/wizardaero.png)

Pour une présentation complète des assistants, consultez [création d’assistants](wizards.md) .
