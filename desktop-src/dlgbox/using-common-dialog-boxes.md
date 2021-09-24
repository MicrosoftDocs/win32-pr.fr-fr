---
title: Utilisation des boîtes de dialogue communes
description: Cette section traite des tâches qui appellent des boîtes de dialogue communes.
ms.assetid: ba038bc1-fb5c-4576-be80-7eae7339ba05
keywords:
- Bibliothèque de boîtes de dialogue communes, tâches
- boîtes de dialogue communes, utilisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d5652c87ab3a8549513f70512e17b344d99a3e2
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128521266"
---
# <a name="using-common-dialog-boxes"></a>Utilisation des boîtes de dialogue communes

Cette section traite des tâches qui appellent des boîtes de dialogue courantes :

-   [Choisir une couleur](#choosing-a-color)
-   [Choix d’une police](#choosing-a-font)
-   [Ouverture d’un fichier](#opening-a-file)
-   [Affichage de la boîte de dialogue Imprimer](#displaying-the-print-dialog-box)
-   [Utilisation de la feuille de propriétés d’impression](#using-the-print-property-sheet)
-   [Configuration de la page imprimée](#setting-up-the-printed-page)
-   [Recherche de texte](#finding-text)

## <a name="choosing-a-color"></a>Choisir une couleur

Cette rubrique décrit un exemple de code qui affiche une boîte de dialogue de **couleur** qui permet à un utilisateur de sélectionner une couleur. L’exemple de code initialise d’abord une structure [**les ChooseColor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) , puis appelle la fonction [**les ChooseColor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) pour afficher la boîte de dialogue. Si la fonction retourne la **valeur true**, ce qui indique que l’utilisateur a sélectionné une couleur, l’exemple de code utilise la couleur sélectionnée pour créer un pinceau plein.

Cet exemple utilise la structure [**les ChooseColor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) pour initialiser la boîte de dialogue comme suit :

-   Initialise le membre **lpCustColors** avec un pointeur vers un tableau statique de valeurs. Les couleurs du tableau sont initialement noires, mais le tableau statique conserve les couleurs personnalisées créées par l’utilisateur pour les appels [**les ChooseColor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) suivants.
-   Définit l' **indicateur \_ RGBINIT CC** et initialise le membre **rgbResult** pour spécifier la couleur qui est initialement sélectionnée quand la boîte de dialogue s’ouvre. S’il n’est pas spécifié, la sélection initiale est noire. L’exemple utilise la variable statique *rgbCurrent* pour conserver la valeur sélectionnée entre les appels à [**les ChooseColor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)).
-   Définit l' **indicateur \_ FULLOPEN CC** pour que l’extension de couleurs personnalisées de la boîte de dialogue s’affiche toujours.


```
CHOOSECOLOR cc;                 // common dialog box structure 
static COLORREF acrCustClr[16]; // array of custom colors 
HWND hwnd;                      // owner window
HBRUSH hbrush;                  // brush handle
static DWORD rgbCurrent;        // initial color selection

// Initialize CHOOSECOLOR 
ZeroMemory(&cc, sizeof(cc));
cc.lStructSize = sizeof(cc);
cc.hwndOwner = hwnd;
cc.lpCustColors = (LPDWORD) acrCustClr;
cc.rgbResult = rgbCurrent;
cc.Flags = CC_FULLOPEN | CC_RGBINIT;
 
if (ChooseColor(&cc)==TRUE) 
{
    hbrush = CreateSolidBrush(cc.rgbResult);
    rgbCurrent = cc.rgbResult; 
}
```



## <a name="choosing-a-font"></a>Choix d’une police

Cette rubrique décrit un exemple de code qui affiche une boîte de dialogue de **police** pour permettre à un utilisateur de choisir les attributs d’une police. L’exemple de code initialise d’abord une structure [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) , puis appelle la fonction [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) pour afficher la boîte de dialogue.

Cet exemple définit l’indicateur **CF \_ SCREENFONTS** pour spécifier que la boîte de dialogue doit afficher uniquement les polices d’écran. Elle définit l’indicateur d' **\_ effets CF** pour afficher les contrôles qui permettent à l’utilisateur de sélectionner des options de barré, de soulignement et de couleur.

Si [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) retourne la **valeur true**, ce qui indique que l’utilisateur a cliqué sur le bouton **OK** , la structure [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) contient des informations qui décrivent les attributs de police et de police sélectionnés par l’utilisateur, y compris les membres de la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) vers laquelle pointe le membre **lpLogFont** . Le membre **rgbColors** contient la couleur de texte sélectionnée. L’exemple de code utilise ces informations pour définir la police et la couleur du texte pour le contexte de périphérique associé à la fenêtre propriétaire.


```
HWND hwnd;                // owner window
HDC hdc;                  // display device context of owner window

CHOOSEFONT cf;            // common dialog box structure
static LOGFONT lf;        // logical font structure
static DWORD rgbCurrent;  // current text color
HFONT hfont, hfontPrev;
DWORD rgbPrev;

// Initialize CHOOSEFONT
ZeroMemory(&cf, sizeof(cf));
cf.lStructSize = sizeof (cf);
cf.hwndOwner = hwnd;
cf.lpLogFont = &lf;
cf.rgbColors = rgbCurrent;
cf.Flags = CF_SCREENFONTS | CF_EFFECTS;

if (ChooseFont(&cf)==TRUE)
{
    hfont = CreateFontIndirect(cf.lpLogFont);
    hfontPrev = SelectObject(hdc, hfont);
    rgbCurrent= cf.rgbColors;
    rgbPrev = SetTextColor(hdc, rgbCurrent);
 .
 .
 .
}
```



## <a name="opening-a-file"></a>Ouverture d’un fichier

> [!Note]  
> à partir de Windows Vista, la boîte de dialogue de fichier commune a été remplacée par la boîte de dialogue d’élément commune lorsqu’elle est utilisée pour ouvrir un fichier. Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de l’API de la boîte de dialogue de fichier commune. Pour plus d’informations, consultez [boîte de dialogue élément commun](../shell/common-file-dialog.md).

Cette rubrique décrit un exemple de code qui affiche une boîte de dialogue **ouvrir** pour permettre à un utilisateur de spécifier le lecteur, le répertoire et le nom d’un fichier à ouvrir. L’exemple de code initialise d’abord une structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) , puis appelle la fonction [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) pour afficher la boîte de dialogue.

Dans cet exemple, le membre **lpstrFilter** est un pointeur vers une mémoire tampon qui spécifie deux filtres de nom de fichier que l’utilisateur peut sélectionner pour limiter les noms de fichiers affichés. La mémoire tampon contient un tableau de chaînes se terminant par deux valeurs NULL dans lequel chaque paire de chaînes spécifie un filtre. Le membre **nFilterIndex** spécifie que le premier modèle est utilisé lors de la création de la boîte de dialogue.

Cet exemple définit les indicateurs **OFN \_ PATHMUSTEXIST** et **OFN \_ FILEMUSTEXIST** dans le membre **Flags** . Ces indicateurs forcent la boîte de dialogue à vérifier, avant de retourner, que le chemin d’accès et le nom de fichier spécifiés par l’utilisateur existent réellement.

La fonction [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) retourne la **valeur true** si l’utilisateur clique sur le bouton **OK** et que le chemin d’accès et le nom de fichier spécifiés existent. Dans ce cas, la mémoire tampon vers laquelle pointe le membre **lpstrFile** contient le chemin d’accès et le nom de fichier. L’exemple de code utilise ces informations dans un appel à la fonction pour ouvrir le fichier.

Bien que cet exemple ne configure pas l’indicateur **OFN \_ Explorer** , il affiche toujours la boîte de dialogue d' **ouverture** de style Explorer par défaut. Toutefois, si vous souhaitez fournir une procédure de raccordement ou un modèle personnalisé et que vous souhaitez l’interface utilisateur de l’Explorateur, vous devez définir l’indicateur **OFN \_ Explorer** .

> [!Note]  
> Dans le langage de programmation C, une chaîne entre guillemets se termine par un caractère null.

 


```
OPENFILENAME ofn;       // common dialog box structure
char szFile[260];       // buffer for file name
HWND hwnd;              // owner window
HANDLE hf;              // file handle

// Initialize OPENFILENAME
ZeroMemory(&ofn, sizeof(ofn));
ofn.lStructSize = sizeof(ofn);
ofn.hwndOwner = hwnd;
ofn.lpstrFile = szFile;
// Set lpstrFile[0] to '\0' so that GetOpenFileName does not 
// use the contents of szFile to initialize itself.
ofn.lpstrFile[0] = '\0';
ofn.nMaxFile = sizeof(szFile);
ofn.lpstrFilter = "All\0*.*\0Text\0*.TXT\0";
ofn.nFilterIndex = 1;
ofn.lpstrFileTitle = NULL;
ofn.nMaxFileTitle = 0;
ofn.lpstrInitialDir = NULL;
ofn.Flags = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;

// Display the Open dialog box. 

if (GetOpenFileName(&ofn)==TRUE) 
    hf = CreateFile(ofn.lpstrFile, 
                    GENERIC_READ,
                    0,
                    (LPSECURITY_ATTRIBUTES) NULL,
                    OPEN_EXISTING,
                    FILE_ATTRIBUTE_NORMAL,
                    (HANDLE) NULL);
```



## <a name="displaying-the-print-dialog-box"></a>Affichage de la boîte de dialogue Imprimer

Cette rubrique décrit un exemple de code qui affiche une boîte de dialogue **Imprimer** afin qu’un utilisateur puisse sélectionner des options pour l’impression d’un document. L’exemple de code initialise d’abord une structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) , puis appelle la fonction [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) pour afficher la boîte de dialogue.

Cet exemple définit l’indicateur **PD \_ RETURNDC** dans le membre **Flags** de la structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) retourne alors un handle de contexte de périphérique à l’imprimante sélectionnée dans le membre **HDC** . Vous pouvez utiliser le descripteur pour afficher la sortie sur l’imprimante.

En entrée, l’exemple de code définit les membres **hDevMode** et **HDevNames** sur la **valeur null**. Si la fonction retourne la **valeur true**, ces membres retournent des handles aux structures [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) qui contiennent l’entrée utilisateur et des informations sur l’imprimante. Vous pouvez utiliser ces informations pour préparer la sortie à envoyer à l’imprimante sélectionnée.


```
PRINTDLG pd;
HWND hwnd;

// Initialize PRINTDLG
ZeroMemory(&pd, sizeof(pd));
pd.lStructSize = sizeof(pd);
pd.hwndOwner   = hwnd;
pd.hDevMode    = NULL;     // Don't forget to free or store hDevMode.
pd.hDevNames   = NULL;     // Don't forget to free or store hDevNames.
pd.Flags       = PD_USEDEVMODECOPIESANDCOLLATE | PD_RETURNDC; 
pd.nCopies     = 1;
pd.nFromPage   = 0xFFFF; 
pd.nToPage     = 0xFFFF; 
pd.nMinPage    = 1; 
pd.nMaxPage    = 0xFFFF; 

if (PrintDlg(&pd)==TRUE) 
{
    // GDI calls to render output. 

    // Delete DC when done.
    DeleteDC(pd.hDC);
}
```



## <a name="using-the-print-property-sheet"></a>Utilisation de la feuille de propriétés d’impression

Cette rubrique décrit un exemple de code qui affiche une feuille de propriétés d' **impression** afin qu’un utilisateur puisse sélectionner des options pour l’impression d’un document. L’exemple de code initialise d’abord une structure [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) , puis appelle la fonction [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) pour afficher la feuille de propriétés.

L’exemple de code définit l’indicateur **PD \_ RETURNDC** dans le membre **Flags** de la structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . La fonction [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) retourne alors un handle de contexte de périphérique à l’imprimante sélectionnée dans le membre **HDC** .

En entrée, l’exemple de code définit les membres **hDevMode** et **HDevNames** sur la **valeur null**. Si la fonction retourne la valeur **\_ OK**, ces membres retournent des handles aux structures [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) contenant l’entrée utilisateur et des informations sur l’imprimante. Vous pouvez utiliser ces informations pour préparer la sortie à envoyer à l’imprimante sélectionnée.

Une fois l’opération d’impression terminée, l’exemple de code libère les mémoires tampons [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames)et [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) et appelle la fonction [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) pour supprimer le contexte de périphérique.


```
// hWnd is the window that owns the property sheet.
HRESULT DisplayPrintPropertySheet(HWND hWnd)
{
    HRESULT hResult;
    PRINTDLGEX pdx = {0};
    LPPRINTPAGERANGE pPageRanges = NULL;

    // Allocate an array of PRINTPAGERANGE structures.
    pPageRanges = (LPPRINTPAGERANGE) GlobalAlloc(GPTR, 10 * sizeof(PRINTPAGERANGE));
    if (!pPageRanges)
        return E_OUTOFMEMORY;

    //  Initialize the PRINTDLGEX structure.
    pdx.lStructSize = sizeof(PRINTDLGEX);
    pdx.hwndOwner = hWnd;
    pdx.hDevMode = NULL;
    pdx.hDevNames = NULL;
    pdx.hDC = NULL;
    pdx.Flags = PD_RETURNDC | PD_COLLATE;
    pdx.Flags2 = 0;
    pdx.ExclusionFlags = 0;
    pdx.nPageRanges = 0;
    pdx.nMaxPageRanges = 10;
    pdx.lpPageRanges = pPageRanges;
    pdx.nMinPage = 1;
    pdx.nMaxPage = 1000;
    pdx.nCopies = 1;
    pdx.hInstance = 0;
    pdx.lpPrintTemplateName = NULL;
    pdx.lpCallback = NULL;
    pdx.nPropertyPages = 0;
    pdx.lphPropertyPages = NULL;
    pdx.nStartPage = START_PAGE_GENERAL;
    pdx.dwResultAction = 0;
    
    //  Invoke the Print property sheet.
    
    hResult = PrintDlgEx(&pdx);

    if ((hResult == S_OK) && pdx.dwResultAction == PD_RESULT_PRINT) 
    {
        // User clicked the Print button, so use the DC and other information returned in the 
        // PRINTDLGEX structure to print the document.
    }

    if (pdx.hDevMode != NULL) 
        GlobalFree(pdx.hDevMode); 
    if (pdx.hDevNames != NULL) 
        GlobalFree(pdx.hDevNames); 
    if (pdx.lpPageRanges != NULL)
        GlobalFree(pPageRanges);

    if (pdx.hDC != NULL) 
        DeleteDC(pdx.hDC);

    return hResult;
}
```



## <a name="setting-up-the-printed-page"></a>Configuration de la page imprimée

Cette rubrique décrit un exemple de code qui affiche une boîte de dialogue **mise en page** pour permettre à un utilisateur de sélectionner les attributs de la page imprimée, tels que le type de papier, la source de papier, l’orientation de page et les marges de page. L’exemple de code initialise d’abord une structure [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) , puis appelle la fonction [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) pour afficher la boîte de dialogue.

Cet exemple définit l’indicateur **PSD \_ Margins** dans le membre **Flags** et utilise le membre **rtMargin** pour spécifier les valeurs de marge initiales. Il définit l’indicateur **PSD \_ INTHOUSANDTHSOFINCHES** pour s’assurer que la boîte de dialogue exprime les dimensions de marge en millièmes de pouce.

En entrée, l’exemple de code définit les membres **hDevMode** et **HDevNames** sur la **valeur null**. Si la fonction retourne la **valeur true**, la fonction utilise ces membres pour retourner les descripteurs aux structures [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) contenant l’entrée utilisateur et les informations relatives à l’imprimante. Vous pouvez utiliser ces informations pour préparer la sortie à envoyer à l’imprimante sélectionnée.

L’exemple suivant permet également une procédure de hook [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) pour personnaliser le dessin du contenu de la page d’exemple.


```
PAGESETUPDLG psd;    // common dialog box structure
HWND hwnd;           // owner window

// Initialize PAGESETUPDLG
ZeroMemory(&psd, sizeof(psd));
psd.lStructSize = sizeof(psd);
psd.hwndOwner   = hwnd;
psd.hDevMode    = NULL; // Don't forget to free or store hDevMode.
psd.hDevNames   = NULL; // Don't forget to free or store hDevNames.
psd.Flags       = PSD_INTHOUSANDTHSOFINCHES | PSD_MARGINS | 
                  PSD_ENABLEPAGEPAINTHOOK; 
psd.rtMargin.top = 1000;
psd.rtMargin.left = 1250;
psd.rtMargin.right = 1250;
psd.rtMargin.bottom = 1000;
psd.lpfnPagePaintHook = PaintHook;

if (PageSetupDlg(&psd)==TRUE)
{
    // check paper size and margin values here.
}
```



L’exemple suivant montre un exemple de procédure de hook [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) qui dessine le rectangle de marge dans l’exemple de zone de page :


```
BOOL CALLBACK PaintHook(HWND hwndDlg, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    LPRECT lprc; 
    COLORREF crMargRect; 
    HDC hdc, hdcOld; 
 
    switch (uMsg) 
    { 
        // Draw the margin rectangle. 
        case WM_PSD_MARGINRECT: 
            hdc = (HDC) wParam; 
            lprc = (LPRECT) lParam; 
 
            // Get the system highlight color. 
            crMargRect = GetSysColor(COLOR_HIGHLIGHT); 
 
            // Create a dash-dot pen of the system highlight color and 
            // select it into the DC of the sample page. 
            hdcOld = SelectObject(hdc, CreatePen(PS_DASHDOT, .5, crMargRect)); 
 
            // Draw the margin rectangle. 
            Rectangle(hdc, lprc->left, lprc->top, lprc->right, lprc->bottom); 
 
            // Restore the previous pen to the DC. 
            SelectObject(hdc, hdcOld); 
            return TRUE; 
 
        default: 
            return FALSE; 
    } 
    return TRUE; 
}
```



## <a name="finding-text"></a>Recherche de texte

Cette rubrique décrit un exemple de code qui affiche et gère une boîte de dialogue **Rechercher** afin que l’utilisateur puisse spécifier les paramètres d’une opération de recherche. La boîte de dialogue envoie des messages à la procédure de fenêtre pour que vous puissiez effectuer l’opération de recherche.

Le code permettant d’afficher et de gérer une boîte de dialogue **remplacer** est similaire, à ceci près qu’elle utilise la fonction [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) pour afficher la boîte de dialogue. La boîte de dialogue **remplacer** envoie également des messages en réponse à un clic de l’utilisateur sur les boutons **remplacer** et **remplacer tout** .

Pour utiliser la boîte de dialogue **Rechercher** ou **remplacer** , vous devez effectuer trois tâches distinctes :

1.  Obtient un identificateur de message pour le message [**FINDMSGSTRING**](findmsgstring.md) Registered.
2.  Affichez la boîte de dialogue.
3.  Traitez les messages [**FINDMSGSTRING**](findmsgstring.md) lorsque la boîte de dialogue est ouverte.

Lorsque vous initialisez votre application, appelez la fonction [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) pour obtenir un identificateur de message pour le message [**FINDMSGSTRING**](findmsgstring.md) Registered.


```
UINT uFindReplaceMsg;  // message identifier for FINDMSGSTRING 

uFindReplaceMsg = RegisterWindowMessage(FINDMSGSTRING);
```



Pour afficher une boîte de dialogue **Rechercher** , commencez par initialiser une structure [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) , puis appelez la fonction [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) . Notez que la structure **FINDREPLACE** et la mémoire tampon de la chaîne de recherche doivent être des variables globales ou statiques afin qu’elles ne soient pas hors de portée avant la fermeture de la boîte de dialogue. Vous devez définir le membre **hwndOwner** pour qu’il spécifie la fenêtre qui reçoit les messages enregistrés. Une fois que vous avez créé la boîte de dialogue, vous pouvez la déplacer ou la manipuler à l’aide du handle retourné.


```
FINDREPLACE fr;       // common dialog box structure
HWND hwnd;            // owner window
CHAR szFindWhat[80];  // buffer receiving string
HWND hdlg = NULL;     // handle to Find dialog box

// Initialize FINDREPLACE
ZeroMemory(&fr, sizeof(fr));
fr.lStructSize = sizeof(fr);
fr.hwndOwner = hwnd;
fr.lpstrFindWhat = szFindWhat;
fr.wFindWhatLen = 80;
fr.Flags = 0;

hdlg = FindText(&fr);
```



Quand la boîte de dialogue est ouverte, votre boucle de messages principale doit inclure un appel à la fonction [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) . Transmettez un handle à la boîte de dialogue en tant que paramètre dans l’appel **IsDialogMessage** . Cela permet de s’assurer que la boîte de dialogue traite correctement les messages de clavier.

Pour surveiller les messages envoyés à partir de la boîte de dialogue, votre procédure de fenêtre doit vérifier le message [**FINDMSGSTRING**](findmsgstring.md) Registered et traiter les valeurs passées dans la structure [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) comme dans l’exemple suivant.


```
LPFINDREPLACE lpfr;

if (message == uFindReplaceMsg)
{ 
    // Get pointer to FINDREPLACE structure from lParam.
    lpfr = (LPFINDREPLACE)lParam;

    // If the FR_DIALOGTERM flag is set, 
    // invalidate the handle that identifies the dialog box. 
    if (lpfr->Flags & FR_DIALOGTERM)
    { 
        hdlg = NULL; 
        return 0; 
    } 

    // If the FR_FINDNEXT flag is set, 
    // call the application-defined search routine
    // to search for the requested string. 
    if (lpfr->Flags & FR_FINDNEXT) 
    {
        SearchFile(lpfr->lpstrFindWhat,
                   (BOOL) (lpfr->Flags & FR_DOWN), 
                   (BOOL) (lpfr->Flags & FR_MATCHCASE)); 
    }

    return 0; 
}
```
