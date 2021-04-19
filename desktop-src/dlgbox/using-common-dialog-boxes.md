---
title: Utilisation des boîtes de dialogue communes
description: Cette section traite des tâches qui appellent des boîtes de dialogue communes.
ms.assetid: ba038bc1-fb5c-4576-be80-7eae7339ba05
keywords:
- Bibliothèque de boîtes de dialogue communes, tâches
- boîtes de dialogue communes, utilisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a973fee7c8f7cd88abad3097edfc0349cc9118c1
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/19/2020
ms.locfileid: "106538803"
---
# <a name="using-common-dialog-boxes"></a><span data-ttu-id="ab9a5-105">Utilisation des boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="ab9a5-105">Using Common Dialog Boxes</span></span>

<span data-ttu-id="ab9a5-106">Cette section traite des tâches qui appellent des boîtes de dialogue courantes :</span><span class="sxs-lookup"><span data-stu-id="ab9a5-106">This section covers tasks that invoke common dialog boxes:</span></span>

-   [<span data-ttu-id="ab9a5-107">Choisir une couleur</span><span class="sxs-lookup"><span data-stu-id="ab9a5-107">Choosing a Color</span></span>](#choosing-a-color)
-   [<span data-ttu-id="ab9a5-108">Choix d’une police</span><span class="sxs-lookup"><span data-stu-id="ab9a5-108">Choosing a Font</span></span>](#choosing-a-font)
-   [<span data-ttu-id="ab9a5-109">Ouverture d’un fichier</span><span class="sxs-lookup"><span data-stu-id="ab9a5-109">Opening a File</span></span>](#opening-a-file)
-   [<span data-ttu-id="ab9a5-110">Affichage de la boîte de dialogue Imprimer</span><span class="sxs-lookup"><span data-stu-id="ab9a5-110">Displaying the Print Dialog Box</span></span>](#displaying-the-print-dialog-box)
-   [<span data-ttu-id="ab9a5-111">Utilisation de la feuille de propriétés d’impression</span><span class="sxs-lookup"><span data-stu-id="ab9a5-111">Using the Print Property Sheet</span></span>](#using-the-print-property-sheet)
-   [<span data-ttu-id="ab9a5-112">Configuration de la page imprimée</span><span class="sxs-lookup"><span data-stu-id="ab9a5-112">Setting Up the Printed Page</span></span>](#setting-up-the-printed-page)
-   [<span data-ttu-id="ab9a5-113">Recherche de texte</span><span class="sxs-lookup"><span data-stu-id="ab9a5-113">Finding Text</span></span>](#finding-text)

## <a name="choosing-a-color"></a><span data-ttu-id="ab9a5-114">Choisir une couleur</span><span class="sxs-lookup"><span data-stu-id="ab9a5-114">Choosing a Color</span></span>

<span data-ttu-id="ab9a5-115">Cette rubrique décrit un exemple de code qui affiche une boîte de dialogue de **couleur** qui permet à un utilisateur de sélectionner une couleur.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-115">This topic describes sample code that displays a **Color** dialog box so that a user can select a color.</span></span> <span data-ttu-id="ab9a5-116">L’exemple de code initialise d’abord une structure [**les ChooseColor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) , puis appelle la fonction [**les ChooseColor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) pour afficher la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-116">The sample code first initializes a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure, and then calls the [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) function to display the dialog box.</span></span> <span data-ttu-id="ab9a5-117">Si la fonction retourne la **valeur true**, ce qui indique que l’utilisateur a sélectionné une couleur, l’exemple de code utilise la couleur sélectionnée pour créer un pinceau plein.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-117">If the function returns **TRUE**, indicating that the user selected a color, the sample code uses the selected color to create a new solid brush.</span></span>

<span data-ttu-id="ab9a5-118">Cet exemple utilise la structure [**les ChooseColor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) pour initialiser la boîte de dialogue comme suit :</span><span class="sxs-lookup"><span data-stu-id="ab9a5-118">This example uses the [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure to initialize the dialog box as follows:</span></span>

-   <span data-ttu-id="ab9a5-119">Initialise le membre **lpCustColors** avec un pointeur vers un tableau statique de valeurs.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-119">Initializes the **lpCustColors** member with a pointer to a static array of values.</span></span> <span data-ttu-id="ab9a5-120">Les couleurs du tableau sont initialement noires, mais le tableau statique conserve les couleurs personnalisées créées par l’utilisateur pour les appels [**les ChooseColor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) suivants.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-120">The colors in the array are initially black, but the static array preserves custom colors created by the user for subsequent [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) calls.</span></span>
-   <span data-ttu-id="ab9a5-121">Définit l' **indicateur \_ RGBINIT CC** et initialise le membre **rgbResult** pour spécifier la couleur qui est initialement sélectionnée quand la boîte de dialogue s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-121">Sets the **CC\_RGBINIT** flag and initializes the **rgbResult** member to specify the color that is initially selected when the dialog box opens.</span></span> <span data-ttu-id="ab9a5-122">S’il n’est pas spécifié, la sélection initiale est noire.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-122">If not specified, the initial selection is black.</span></span> <span data-ttu-id="ab9a5-123">L’exemple utilise la variable statique *rgbCurrent* pour conserver la valeur sélectionnée entre les appels à [**les ChooseColor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ab9a5-123">The example uses the *rgbCurrent* static variable to preserve the selected value between calls to [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)).</span></span>
-   <span data-ttu-id="ab9a5-124">Définit l' **indicateur \_ FULLOPEN CC** pour que l’extension de couleurs personnalisées de la boîte de dialogue s’affiche toujours.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-124">Sets the **CC\_FULLOPEN** flag so the custom colors extension of the dialog box is always displayed.</span></span>


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



## <a name="choosing-a-font"></a><span data-ttu-id="ab9a5-125">Choix d’une police</span><span class="sxs-lookup"><span data-stu-id="ab9a5-125">Choosing a Font</span></span>

<span data-ttu-id="ab9a5-126">Cette rubrique décrit un exemple de code qui affiche une boîte de dialogue de **police** pour permettre à un utilisateur de choisir les attributs d’une police.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-126">This topic describes sample code that displays a **Font** dialog box so that a user can choose the attributes of a font.</span></span> <span data-ttu-id="ab9a5-127">L’exemple de code initialise d’abord une structure [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) , puis appelle la fonction [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) pour afficher la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-127">The sample code first initializes a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure, and then calls the [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function to display the dialog box.</span></span>

<span data-ttu-id="ab9a5-128">Cet exemple définit l’indicateur **CF \_ SCREENFONTS** pour spécifier que la boîte de dialogue doit afficher uniquement les polices d’écran.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-128">This example sets the **CF\_SCREENFONTS** flag to specify that the dialog box should display only screen fonts.</span></span> <span data-ttu-id="ab9a5-129">Elle définit l’indicateur d' **\_ effets CF** pour afficher les contrôles qui permettent à l’utilisateur de sélectionner des options de barré, de soulignement et de couleur.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-129">It sets the **CF\_EFFECTS** flag to display controls that allow the user to select strikeout, underline, and color options.</span></span>

<span data-ttu-id="ab9a5-130">Si [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) retourne la **valeur true**, ce qui indique que l’utilisateur a cliqué sur le bouton **OK** , la structure [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) contient des informations qui décrivent les attributs de police et de police sélectionnés par l’utilisateur, y compris les membres de la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) vers laquelle pointe le membre **lpLogFont** .</span><span class="sxs-lookup"><span data-stu-id="ab9a5-130">If [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) returns **TRUE**, indicating that the user clicked the **OK** button, the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure contains information that describes the font and font attributes selected by the user, including the members of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure pointed to by the **lpLogFont** member.</span></span> <span data-ttu-id="ab9a5-131">Le membre **rgbColors** contient la couleur de texte sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-131">The **rgbColors** member contains the selected text color.</span></span> <span data-ttu-id="ab9a5-132">L’exemple de code utilise ces informations pour définir la police et la couleur du texte pour le contexte de périphérique associé à la fenêtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-132">The sample code uses this information to set the font and text color for the device context associated with the owner window.</span></span>


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



## <a name="opening-a-file"></a><span data-ttu-id="ab9a5-133">Ouverture d’un fichier</span><span class="sxs-lookup"><span data-stu-id="ab9a5-133">Opening a File</span></span>

> [!Note]  
> <span data-ttu-id="ab9a5-134">À compter de Windows Vista, la boîte de dialogue de fichier commune a été remplacée par la boîte de dialogue d’élément commune lorsqu’elle est utilisée pour ouvrir un fichier.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-134">Starting with Windows Vista, the Common File Dialog has been superseded by the Common Item Dialog when used to open a file.</span></span> <span data-ttu-id="ab9a5-135">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de l’API de la boîte de dialogue de fichier commune.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-135">We recommend that you use the Common Item Dialog API instead of the Common File Dialog API.</span></span> <span data-ttu-id="ab9a5-136">Pour plus d’informations, consultez [boîte de dialogue élément commun](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ab9a5-136">For more information, see [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span>

 

<span data-ttu-id="ab9a5-137">Cette rubrique décrit un exemple de code qui affiche une boîte de dialogue **ouvrir** pour permettre à un utilisateur de spécifier le lecteur, le répertoire et le nom d’un fichier à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-137">This topic describes sample code that displays an **Open** dialog box so that a user can specify the drive, directory, and name of a file to open.</span></span> <span data-ttu-id="ab9a5-138">L’exemple de code initialise d’abord une structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) , puis appelle la fonction [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) pour afficher la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-138">The sample code first initializes an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure, and then calls the [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) function to display the dialog box.</span></span>

<span data-ttu-id="ab9a5-139">Dans cet exemple, le membre **lpstrFilter** est un pointeur vers une mémoire tampon qui spécifie deux filtres de nom de fichier que l’utilisateur peut sélectionner pour limiter les noms de fichiers affichés.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-139">In this example, the **lpstrFilter** member is a pointer to a buffer that specifies two file name filters that the user can select to limit the file names that are displayed.</span></span> <span data-ttu-id="ab9a5-140">La mémoire tampon contient un tableau de chaînes se terminant par deux valeurs NULL dans lequel chaque paire de chaînes spécifie un filtre.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-140">The buffer contains a double-null terminated array of strings in which each pair of strings specifies a filter.</span></span> <span data-ttu-id="ab9a5-141">Le membre **nFilterIndex** spécifie que le premier modèle est utilisé lors de la création de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-141">The **nFilterIndex** member specifies that the first pattern is used when the dialog box is created.</span></span>

<span data-ttu-id="ab9a5-142">Cet exemple définit les indicateurs **OFN \_ PATHMUSTEXIST** et **OFN \_ FILEMUSTEXIST** dans le membre **Flags** .</span><span class="sxs-lookup"><span data-stu-id="ab9a5-142">This example sets the **OFN\_PATHMUSTEXIST** and **OFN\_FILEMUSTEXIST** flags in the **Flags** member.</span></span> <span data-ttu-id="ab9a5-143">Ces indicateurs forcent la boîte de dialogue à vérifier, avant de retourner, que le chemin d’accès et le nom de fichier spécifiés par l’utilisateur existent réellement.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-143">These flags cause the dialog box to verify, before returning, that the path and file name specified by the user actually exist.</span></span>

<span data-ttu-id="ab9a5-144">La fonction [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) retourne la **valeur true** si l’utilisateur clique sur le bouton **OK** et que le chemin d’accès et le nom de fichier spécifiés existent.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-144">The [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) function returns **TRUE** if the user clicks the **OK** button and the specified path and file name exist.</span></span> <span data-ttu-id="ab9a5-145">Dans ce cas, la mémoire tampon vers laquelle pointe le membre **lpstrFile** contient le chemin d’accès et le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-145">In this case, the buffer pointed to by the **lpstrFile** member contains the path and file name.</span></span> <span data-ttu-id="ab9a5-146">L’exemple de code utilise ces informations dans un appel à la fonction pour ouvrir le fichier.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-146">The sample code uses this information in a call to the function to open the file.</span></span>

<span data-ttu-id="ab9a5-147">Bien que cet exemple ne configure pas l’indicateur **OFN \_ Explorer** , il affiche toujours la boîte de dialogue d' **ouverture** de style Explorer par défaut.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-147">Although this example does not set the **OFN\_EXPLORER** flag, it still displays the default Explorer-style **Open** dialog box.</span></span> <span data-ttu-id="ab9a5-148">Toutefois, si vous souhaitez fournir une procédure de raccordement ou un modèle personnalisé et que vous souhaitez l’interface utilisateur de l’Explorateur, vous devez définir l’indicateur **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="ab9a5-148">However, if you want to provide a hook procedure or a custom template and you want the Explorer user interface, you must set the **OFN\_EXPLORER** flag.</span></span>

> [!Note]  
> <span data-ttu-id="ab9a5-149">Dans le langage de programmation C, une chaîne entre guillemets se termine par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-149">In the C programming language, a string enclosed in quotation marks is null-terminated.</span></span>

 


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



## <a name="displaying-the-print-dialog-box"></a><span data-ttu-id="ab9a5-150">Affichage de la boîte de dialogue Imprimer</span><span class="sxs-lookup"><span data-stu-id="ab9a5-150">Displaying the Print Dialog Box</span></span>

<span data-ttu-id="ab9a5-151">Cette rubrique décrit un exemple de code qui affiche une boîte de dialogue **Imprimer** afin qu’un utilisateur puisse sélectionner des options pour l’impression d’un document.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-151">This topic describes sample code that displays a **Print** dialog box so that a user can select options for printing a document.</span></span> <span data-ttu-id="ab9a5-152">L’exemple de code initialise d’abord une structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) , puis appelle la fonction [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) pour afficher la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-152">The sample code first initializes a [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure, and then calls the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function to display the dialog box.</span></span>

<span data-ttu-id="ab9a5-153">Cet exemple définit l’indicateur **PD \_ RETURNDC** dans le membre **Flags** de la structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="ab9a5-153">This example sets the **PD\_RETURNDC** flag in the **Flags** member of the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="ab9a5-154">[**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) retourne alors un handle de contexte de périphérique à l’imprimante sélectionnée dans le membre **HDC** .</span><span class="sxs-lookup"><span data-stu-id="ab9a5-154">This causes [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) to return a device context handle to the selected printer in the **hDC** member.</span></span> <span data-ttu-id="ab9a5-155">Vous pouvez utiliser le descripteur pour afficher la sortie sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-155">You can use the handle to render output on the printer.</span></span>

<span data-ttu-id="ab9a5-156">En entrée, l’exemple de code définit les membres **hDevMode** et **HDevNames** sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-156">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="ab9a5-157">Si la fonction retourne la **valeur true**, ces membres retournent des handles aux structures [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) qui contiennent l’entrée utilisateur et des informations sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-157">If the function returns **TRUE**, these members return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures that contain the user input and information about the printer.</span></span> <span data-ttu-id="ab9a5-158">Vous pouvez utiliser ces informations pour préparer la sortie à envoyer à l’imprimante sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-158">You can use this information to prepare the output to be sent to the selected printer.</span></span>


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



## <a name="using-the-print-property-sheet"></a><span data-ttu-id="ab9a5-159">Utilisation de la feuille de propriétés d’impression</span><span class="sxs-lookup"><span data-stu-id="ab9a5-159">Using the Print Property Sheet</span></span>

<span data-ttu-id="ab9a5-160">Cette rubrique décrit un exemple de code qui affiche une feuille de propriétés d' **impression** afin qu’un utilisateur puisse sélectionner des options pour l’impression d’un document.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-160">This topic describes sample code that displays a **Print** property sheet so that a user can select options for printing a document.</span></span> <span data-ttu-id="ab9a5-161">L’exemple de code initialise d’abord une structure [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) , puis appelle la fonction [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) pour afficher la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-161">The sample code first initializes a [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) structure, then calls the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to display the property sheet.</span></span>

<span data-ttu-id="ab9a5-162">L’exemple de code définit l’indicateur **PD \_ RETURNDC** dans le membre **Flags** de la structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="ab9a5-162">The sample code sets the **PD\_RETURNDC** flag in the **Flags** member of the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="ab9a5-163">La fonction [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) retourne alors un handle de contexte de périphérique à l’imprimante sélectionnée dans le membre **HDC** .</span><span class="sxs-lookup"><span data-stu-id="ab9a5-163">This causes the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to return a device context handle to the selected printer in the **hDC** member.</span></span>

<span data-ttu-id="ab9a5-164">En entrée, l’exemple de code définit les membres **hDevMode** et **HDevNames** sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-164">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="ab9a5-165">Si la fonction retourne la valeur **\_ OK**, ces membres retournent des handles aux structures [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) contenant l’entrée utilisateur et des informations sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-165">If the function returns **S\_OK**, these members return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures containing the user input and information about the printer.</span></span> <span data-ttu-id="ab9a5-166">Vous pouvez utiliser ces informations pour préparer la sortie à envoyer à l’imprimante sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-166">You can use this information to prepare the output to be sent to the selected printer.</span></span>

<span data-ttu-id="ab9a5-167">Une fois l’opération d’impression terminée, l’exemple de code libère les mémoires tampons [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames)et [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) et appelle la fonction [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) pour supprimer le contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-167">After the printing operation has been completed, the sample code frees the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames), and [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) buffers and calls the [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) function to delete the device context.</span></span>


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



## <a name="setting-up-the-printed-page"></a><span data-ttu-id="ab9a5-168">Configuration de la page imprimée</span><span class="sxs-lookup"><span data-stu-id="ab9a5-168">Setting Up the Printed Page</span></span>

<span data-ttu-id="ab9a5-169">Cette rubrique décrit un exemple de code qui affiche une boîte de dialogue **mise en page** pour permettre à un utilisateur de sélectionner les attributs de la page imprimée, tels que le type de papier, la source de papier, l’orientation de page et les marges de page.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-169">This topic describes sample code that displays a **Page Setup** dialog box so that a user can select the attributes of the printed page, such as the paper type, paper source, page orientation, and page margins.</span></span> <span data-ttu-id="ab9a5-170">L’exemple de code initialise d’abord une structure [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) , puis appelle la fonction [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) pour afficher la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-170">The sample code first initializes a [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure, and then calls the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function to display the dialog box.</span></span>

<span data-ttu-id="ab9a5-171">Cet exemple définit l’indicateur **PSD \_ Margins** dans le membre **Flags** et utilise le membre **rtMargin** pour spécifier les valeurs de marge initiales.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-171">This example sets the **PSD\_MARGINS** flag in the **Flags** member and uses the **rtMargin** member to specify the initial margin values.</span></span> <span data-ttu-id="ab9a5-172">Il définit l’indicateur **PSD \_ INTHOUSANDTHSOFINCHES** pour s’assurer que la boîte de dialogue exprime les dimensions de marge en millièmes de pouce.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-172">It sets the **PSD\_INTHOUSANDTHSOFINCHES** flag to ensure that the dialog box expresses margin dimensions in thousandths of an inch.</span></span>

<span data-ttu-id="ab9a5-173">En entrée, l’exemple de code définit les membres **hDevMode** et **HDevNames** sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-173">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="ab9a5-174">Si la fonction retourne la **valeur true**, la fonction utilise ces membres pour retourner les descripteurs aux structures [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) contenant l’entrée utilisateur et les informations relatives à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-174">If the function returns **TRUE**, the function uses these members to return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures containing the user input and information about the printer.</span></span> <span data-ttu-id="ab9a5-175">Vous pouvez utiliser ces informations pour préparer la sortie à envoyer à l’imprimante sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-175">You can use this information to prepare the output to be sent to the selected printer.</span></span>

<span data-ttu-id="ab9a5-176">L’exemple suivant permet également une procédure de hook [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) pour personnaliser le dessin du contenu de la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-176">The following example also enables a [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize drawing the contents of the sample page.</span></span>


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



<span data-ttu-id="ab9a5-177">L’exemple suivant montre un exemple de procédure de hook [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) qui dessine le rectangle de marge dans l’exemple de zone de page :</span><span class="sxs-lookup"><span data-stu-id="ab9a5-177">The following example shows a sample [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure that draws the margin rectangle in the sample page area:</span></span>


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



## <a name="finding-text"></a><span data-ttu-id="ab9a5-178">Recherche de texte</span><span class="sxs-lookup"><span data-stu-id="ab9a5-178">Finding Text</span></span>

<span data-ttu-id="ab9a5-179">Cette rubrique décrit un exemple de code qui affiche et gère une boîte de dialogue **Rechercher** afin que l’utilisateur puisse spécifier les paramètres d’une opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-179">This topic describes sample code that displays and manages a **Find** dialog box so that the user can specify the parameters of a search operation.</span></span> <span data-ttu-id="ab9a5-180">La boîte de dialogue envoie des messages à la procédure de fenêtre pour que vous puissiez effectuer l’opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-180">The dialog box sends messages to the window procedure so you can perform the search operation.</span></span>

<span data-ttu-id="ab9a5-181">Le code permettant d’afficher et de gérer une boîte de dialogue **remplacer** est similaire, à ceci près qu’elle utilise la fonction [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) pour afficher la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-181">The code for displaying and managing a **Replace** dialog box is similar, except that it uses the [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) function to display the dialog box.</span></span> <span data-ttu-id="ab9a5-182">La boîte de dialogue **remplacer** envoie également des messages en réponse à un clic de l’utilisateur sur les boutons **remplacer** et **remplacer tout** .</span><span class="sxs-lookup"><span data-stu-id="ab9a5-182">The **Replace** dialog box also sends messages in response to user clicks on the **Replace** and **Replace All** buttons.</span></span>

<span data-ttu-id="ab9a5-183">Pour utiliser la boîte de dialogue **Rechercher** ou **remplacer** , vous devez effectuer trois tâches distinctes :</span><span class="sxs-lookup"><span data-stu-id="ab9a5-183">To use the **Find** or **Replace** dialog box, you must perform three separate tasks:</span></span>

1.  <span data-ttu-id="ab9a5-184">Obtient un identificateur de message pour le message [**FINDMSGSTRING**](findmsgstring.md) Registered.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-184">Get a message identifier for the [**FINDMSGSTRING**](findmsgstring.md) registered message.</span></span>
2.  <span data-ttu-id="ab9a5-185">Affichez la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-185">Display the dialog box.</span></span>
3.  <span data-ttu-id="ab9a5-186">Traitez les messages [**FINDMSGSTRING**](findmsgstring.md) lorsque la boîte de dialogue est ouverte.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-186">Process [**FINDMSGSTRING**](findmsgstring.md) messages when the dialog box is open.</span></span>

<span data-ttu-id="ab9a5-187">Lorsque vous initialisez votre application, appelez la fonction [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) pour obtenir un identificateur de message pour le message [**FINDMSGSTRING**](findmsgstring.md) Registered.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-187">When you initialize your application, call the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get a message identifier for the [**FINDMSGSTRING**](findmsgstring.md) registered message.</span></span>


```
UINT uFindReplaceMsg;  // message identifier for FINDMSGSTRING 

uFindReplaceMsg = RegisterWindowMessage(FINDMSGSTRING);
```



<span data-ttu-id="ab9a5-188">Pour afficher une boîte de dialogue **Rechercher** , commencez par initialiser une structure [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) , puis appelez la fonction [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) .</span><span class="sxs-lookup"><span data-stu-id="ab9a5-188">To display a **Find** dialog box, first initialize a [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure and then call the [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) function.</span></span> <span data-ttu-id="ab9a5-189">Notez que la structure **FINDREPLACE** et la mémoire tampon de la chaîne de recherche doivent être des variables globales ou statiques afin qu’elles ne soient pas hors de portée avant la fermeture de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-189">Note that the **FINDREPLACE** structure and the buffer for the search string should be a global or static variable so that it does not go out of scope before the dialog box closes.</span></span> <span data-ttu-id="ab9a5-190">Vous devez définir le membre **hwndOwner** pour qu’il spécifie la fenêtre qui reçoit les messages enregistrés.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-190">You must set the **hwndOwner** member to specify the window that receives the registered messages.</span></span> <span data-ttu-id="ab9a5-191">Une fois que vous avez créé la boîte de dialogue, vous pouvez la déplacer ou la manipuler à l’aide du handle retourné.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-191">After you create the dialog box, you can move or manipulate it by using the returned handle.</span></span>


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



<span data-ttu-id="ab9a5-192">Quand la boîte de dialogue est ouverte, votre boucle de messages principale doit inclure un appel à la fonction [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) .</span><span class="sxs-lookup"><span data-stu-id="ab9a5-192">When the dialog box is open, your main message loop must include a call to the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function.</span></span> <span data-ttu-id="ab9a5-193">Transmettez un handle à la boîte de dialogue en tant que paramètre dans l’appel **IsDialogMessage** .</span><span class="sxs-lookup"><span data-stu-id="ab9a5-193">Pass a handle to the dialog box as a parameter in the **IsDialogMessage** call.</span></span> <span data-ttu-id="ab9a5-194">Cela permet de s’assurer que la boîte de dialogue traite correctement les messages de clavier.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-194">This ensures that the dialog box correctly processes keyboard messages.</span></span>

<span data-ttu-id="ab9a5-195">Pour surveiller les messages envoyés à partir de la boîte de dialogue, votre procédure de fenêtre doit vérifier le message [**FINDMSGSTRING**](findmsgstring.md) Registered et traiter les valeurs passées dans la structure [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) comme dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="ab9a5-195">To monitor messages sent from the dialog box, your window procedure must check for the [**FINDMSGSTRING**](findmsgstring.md) registered message and process the values passed in the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure as in the following example.</span></span>


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



 

 
