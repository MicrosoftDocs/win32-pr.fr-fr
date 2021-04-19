---
title: Utilisation des icônes
description: Cette section fournit des exemples de code qui montrent comment effectuer des tâches liées aux icônes.
ms.assetid: 5021d59a-7aae-4ddc-be66-9abdc75ad316
keywords:
- ressources, icônes
- icônes, création
- icônes, affichage
- icônes, partager des ressources
- création d’icônes
- afficher les icônes
- ressources de l’icône de partage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e93f831e3411985ecfb9f841ade750acd4a61b
ms.sourcegitcommit: 8755905962e156f29203705d09d6df8b7d0e2fca
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "106541795"
---
# <a name="using-icons"></a><span data-ttu-id="b41b5-110">Utilisation des icônes</span><span class="sxs-lookup"><span data-stu-id="b41b5-110">Using Icons</span></span>

<span data-ttu-id="b41b5-111">Les rubriques suivantes décrivent comment effectuer certaines tâches liées aux icônes :</span><span class="sxs-lookup"><span data-stu-id="b41b5-111">The following topics describe how to perform certain tasks related to icons:</span></span>

-   [<span data-ttu-id="b41b5-112">Création d’une icône</span><span class="sxs-lookup"><span data-stu-id="b41b5-112">Creating an Icon</span></span>](#creating-an-icon)
-   [<span data-ttu-id="b41b5-113">Affichage d’une icône</span><span class="sxs-lookup"><span data-stu-id="b41b5-113">Displaying an Icon</span></span>](#displaying-an-icon)
-   [<span data-ttu-id="b41b5-114">Ressources de l’icône de partage</span><span class="sxs-lookup"><span data-stu-id="b41b5-114">Sharing Icon Resources</span></span>](#sharing-icon-resources)

## <a name="creating-an-icon"></a><span data-ttu-id="b41b5-115">Création d’une icône</span><span class="sxs-lookup"><span data-stu-id="b41b5-115">Creating an Icon</span></span>

<span data-ttu-id="b41b5-116">Pour utiliser une icône, votre application doit obtenir un handle vers l’icône.</span><span class="sxs-lookup"><span data-stu-id="b41b5-116">To use an icon, your application must get a handle to the icon.</span></span> <span data-ttu-id="b41b5-117">L’exemple suivant montre comment créer deux descripteurs d’icône différents : un pour l’icône de question standard et un pour une icône personnalisée incluse en tant que ressource dans le fichier de définition de ressources de l’application.</span><span class="sxs-lookup"><span data-stu-id="b41b5-117">The following example shows how to create two different icon handles: one for the standard question icon and one for a custom icon included as a resource in the application's resource-definition file.</span></span>


```
HICON hIcon1;   // icon handle 
HICON hIcon2;   // icon handle 
 
// Create a standard question icon. 
 
hIcon1 = LoadIcon(NULL, IDI_QUESTION); 
 
// Create a custom icon based on a resource. 
 
hIcon2 = LoadIcon(hinst, MAKEINTRESOURCE(460)); 
 
// Create a custom icon at run time.
 
```



<span data-ttu-id="b41b5-118">Une application doit implémenter des icônes personnalisées en tant que ressources et doit utiliser la fonction [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) ou [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) , au lieu de créer les icônes au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="b41b5-118">An application should implement custom icons as resources and should use the [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) or [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) function, rather than create the icons at run-time.</span></span> <span data-ttu-id="b41b5-119">Cette approche évite la dépendance des appareils, simplifie la localisation et permet aux applications de partager des bitmaps d’icône.</span><span class="sxs-lookup"><span data-stu-id="b41b5-119">This approach avoids device dependence, simplifies localization, and enables applications to share icon bitmaps.</span></span> <span data-ttu-id="b41b5-120">Toutefois, l’exemple suivant utilise [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) pour créer une icône personnalisée au moment de l’exécution, en fonction des masques de bits de bitmap. Il est inclus pour illustrer la façon dont le système interprète les masques de pixels de l’icône.</span><span class="sxs-lookup"><span data-stu-id="b41b5-120">However, the following example uses [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) to create a custom icon at run-time, based on bitmap bitmasks; it is included to illustrate how the system interprets icon bitmap bitmasks.</span></span>


```
HICON hIcon3;      // icon handle 
 
// Yang icon AND bitmask 
 
BYTE ANDmaskIcon[] = {0xFF, 0xFF, 0xFF, 0xFF,   // line 1 
                      0xFF, 0xFF, 0xC3, 0xFF,   // line 2 
                      0xFF, 0xFF, 0x00, 0xFF,   // line 3 
                      0xFF, 0xFE, 0x00, 0x7F,   // line 4 
 
                      0xFF, 0xFC, 0x00, 0x1F,   // line 5 
                      0xFF, 0xF8, 0x00, 0x0F,   // line 6 
                      0xFF, 0xF8, 0x00, 0x0F,   // line 7 
                      0xFF, 0xF0, 0x00, 0x07,   // line 8 
 
                      0xFF, 0xF0, 0x00, 0x03,   // line 9 
                      0xFF, 0xE0, 0x00, 0x03,   // line 10 
                      0xFF, 0xE0, 0x00, 0x01,   // line 11 
                      0xFF, 0xE0, 0x00, 0x01,   // line 12 
 
                      0xFF, 0xF0, 0x00, 0x01,   // line 13 
                      0xFF, 0xF0, 0x00, 0x00,   // line 14 
                      0xFF, 0xF8, 0x00, 0x00,   // line 15 
                      0xFF, 0xFC, 0x00, 0x00,   // line 16 
 
                      0xFF, 0xFF, 0x00, 0x00,   // line 17 
                      0xFF, 0xFF, 0x80, 0x00,   // line 18 
                      0xFF, 0xFF, 0xE0, 0x00,   // line 19 
                      0xFF, 0xFF, 0xE0, 0x01,   // line 20 
 
                      0xFF, 0xFF, 0xF0, 0x01,   // line 21 
                      0xFF, 0xFF, 0xF0, 0x01,   // line 22 
                      0xFF, 0xFF, 0xF0, 0x03,   // line 23 
                      0xFF, 0xFF, 0xE0, 0x03,   // line 24 
 
                      0xFF, 0xFF, 0xE0, 0x07,   // line 25 
                      0xFF, 0xFF, 0xC0, 0x0F,   // line 26 
                      0xFF, 0xFF, 0xC0, 0x0F,   // line 27 
                      0xFF, 0xFF, 0x80, 0x1F,   // line 28 
 
                      0xFF, 0xFF, 0x00, 0x7F,   // line 29 
                      0xFF, 0xFC, 0x00, 0xFF,   // line 30 
                      0xFF, 0xF8, 0x03, 0xFF,   // line 31 
                      0xFF, 0xFC, 0x3F, 0xFF};  // line 32 
 
// Yang icon XOR bitmask 
 
BYTE XORmaskIcon[] = {0x00, 0x00, 0x00, 0x00,   // line 1 
                      0x00, 0x00, 0x00, 0x00,   // line 2 
                      0x00, 0x00, 0x00, 0x00,   // line 3 
                      0x00, 0x00, 0x00, 0x00,   // line 4 
 
                      0x00, 0x00, 0x00, 0x00,   // line 5 
                      0x00, 0x00, 0x00, 0x00,   // line 6 
                      0x00, 0x00, 0x00, 0x00,   // line 7 
                      0x00, 0x00, 0x38, 0x00,   // line 8 
 
                      0x00, 0x00, 0x7C, 0x00,   // line 9 
                      0x00, 0x00, 0x7C, 0x00,   // line 10 
                      0x00, 0x00, 0x7C, 0x00,   // line 11 
                      0x00, 0x00, 0x38, 0x00,   // line 12 
 
                      0x00, 0x00, 0x00, 0x00,   // line 13 
                      0x00, 0x00, 0x00, 0x00,   // line 14 
                      0x00, 0x00, 0x00, 0x00,   // line 15 
                      0x00, 0x00, 0x00, 0x00,   // line 16 
 
                      0x00, 0x00, 0x00, 0x00,   // line 17 
                      0x00, 0x00, 0x00, 0x00,   // line 18 
                      0x00, 0x00, 0x00, 0x00,   // line 19 
                      0x00, 0x00, 0x00, 0x00,   // line 20 
 
                      0x00, 0x00, 0x00, 0x00,   // line 21 
                      0x00, 0x00, 0x00, 0x00,   // line 22 
                      0x00, 0x00, 0x00, 0x00,   // line 23 
                      0x00, 0x00, 0x00, 0x00,   // line 24 
 
                      0x00, 0x00, 0x00, 0x00,   // line 25 
                      0x00, 0x00, 0x00, 0x00,   // line 26 
                      0x00, 0x00, 0x00, 0x00,   // line 27 
                      0x00, 0x00, 0x00, 0x00,   // line 28 
 
                      0x00, 0x00, 0x00, 0x00,   // line 29 
                      0x00, 0x00, 0x00, 0x00,   // line 30 
                      0x00, 0x00, 0x00, 0x00,   // line 31 
                      0x00, 0x00, 0x00, 0x00};  // line 32 
 
hIcon3 = CreateIcon(hinst,    // application instance  
             32,              // icon width 
             32,              // icon height 
             1,               // number of XOR planes 
             1,               // number of bits per pixel 
             ANDmaskIcon,     // AND bitmask  
             XORmaskIcon);    // XOR bitmask 
              
```



<span data-ttu-id="b41b5-121">Pour créer l’icône, [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) applique la table de vérité suivante aux masques de et et XOR.</span><span class="sxs-lookup"><span data-stu-id="b41b5-121">To create the icon, [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) applies the following truth table to the AND and XOR bitmasks.</span></span>



| <span data-ttu-id="b41b5-122">ET masque de masque</span><span class="sxs-lookup"><span data-stu-id="b41b5-122">AND bitmask</span></span> | <span data-ttu-id="b41b5-123">Masque de masque XOR</span><span class="sxs-lookup"><span data-stu-id="b41b5-123">XOR bitmask</span></span> | <span data-ttu-id="b41b5-124">Afficher</span><span class="sxs-lookup"><span data-stu-id="b41b5-124">Display</span></span>        |
|-------------|-------------|----------------|
| <span data-ttu-id="b41b5-125">0</span><span class="sxs-lookup"><span data-stu-id="b41b5-125">0</span></span>           | <span data-ttu-id="b41b5-126">0</span><span class="sxs-lookup"><span data-stu-id="b41b5-126">0</span></span>           | <span data-ttu-id="b41b5-127">Noir</span><span class="sxs-lookup"><span data-stu-id="b41b5-127">Black</span></span>          |
| <span data-ttu-id="b41b5-128">0</span><span class="sxs-lookup"><span data-stu-id="b41b5-128">0</span></span>           | <span data-ttu-id="b41b5-129">1</span><span class="sxs-lookup"><span data-stu-id="b41b5-129">1</span></span>           | <span data-ttu-id="b41b5-130">Blancs</span><span class="sxs-lookup"><span data-stu-id="b41b5-130">White</span></span>          |
| <span data-ttu-id="b41b5-131">1</span><span class="sxs-lookup"><span data-stu-id="b41b5-131">1</span></span>           | <span data-ttu-id="b41b5-132">0</span><span class="sxs-lookup"><span data-stu-id="b41b5-132">0</span></span>           | <span data-ttu-id="b41b5-133">Screen</span><span class="sxs-lookup"><span data-stu-id="b41b5-133">Screen</span></span>         |
| <span data-ttu-id="b41b5-134">1</span><span class="sxs-lookup"><span data-stu-id="b41b5-134">1</span></span>           | <span data-ttu-id="b41b5-135">1</span><span class="sxs-lookup"><span data-stu-id="b41b5-135">1</span></span>           | <span data-ttu-id="b41b5-136">Écran inversé</span><span class="sxs-lookup"><span data-stu-id="b41b5-136">Reverse screen</span></span> |



 

<span data-ttu-id="b41b5-137">Avant de fermer, votre application doit utiliser [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) pour détruire toute icône qu’elle a créée à l’aide de [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect).</span><span class="sxs-lookup"><span data-stu-id="b41b5-137">Before closing, your application must use [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) to destroy any icon it created by using [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect).</span></span> <span data-ttu-id="b41b5-138">Il n’est pas nécessaire de détruire les icônes créées par d’autres fonctions.</span><span class="sxs-lookup"><span data-stu-id="b41b5-138">It is not necessary to destroy icons created by other functions.</span></span>

## <a name="displaying-an-icon"></a><span data-ttu-id="b41b5-139">Affichage d’une icône</span><span class="sxs-lookup"><span data-stu-id="b41b5-139">Displaying an Icon</span></span>

<span data-ttu-id="b41b5-140">Votre application peut charger et créer des icônes à afficher dans la zone cliente de l’application ou dans les fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="b41b5-140">Your application can load and create icons to display in the application's client area or child windows.</span></span> <span data-ttu-id="b41b5-141">L’exemple suivant montre comment dessiner une icône dans la zone cliente de la fenêtre dont le contexte de périphérique (DC) est identifié par le paramètre *HDC* .</span><span class="sxs-lookup"><span data-stu-id="b41b5-141">The following example demonstrates how to draw an icon in the client area of the window whose device context (DC) is identified by the *hdc* parameter.</span></span>


```
HICON hIcon1;   // icon handle  
HDC hdc;        // handle to display context 
 
DrawIcon(hdc, 10, 20, hIcon1); 
```



<span data-ttu-id="b41b5-142">Le système affiche automatiquement la ou les icônes de classe d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b41b5-142">The system automatically displays the class icon(s) for a window.</span></span> <span data-ttu-id="b41b5-143">Votre application peut assigner des icônes de classe lors de l’inscription d’une classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b41b5-143">Your application can assign class icons while registering a window class.</span></span> <span data-ttu-id="b41b5-144">Votre application peut remplacer une icône de classe à l’aide de la fonction [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) .</span><span class="sxs-lookup"><span data-stu-id="b41b5-144">Your application can replace a class icon by using the [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) function.</span></span> <span data-ttu-id="b41b5-145">Cette fonction modifie les paramètres de fenêtre par défaut pour toutes les fenêtres d’une classe donnée.</span><span class="sxs-lookup"><span data-stu-id="b41b5-145">This function changes the default window settings for all windows of a given class.</span></span> <span data-ttu-id="b41b5-146">L’exemple suivant remplace une icône de classe par l’icône dont l’identificateur de ressource est 480.</span><span class="sxs-lookup"><span data-stu-id="b41b5-146">The following example replaces a class icon with the icon whose resource identifier is 480.</span></span>


```
HINSTANCE hinst;            // handle to current instance 
HWND hwnd;                  // main window handle  
 
// Change the icon for hwnd's window class. 
 
SetClassLong(hwnd,          // window handle 
    GCL_HICON,              // changes icon 
    (LONG) LoadIcon(hinst, MAKEINTRESOURCE(480))
   ); 
```



<span data-ttu-id="b41b5-147">Pour plus d’informations sur les classes de fenêtre, consultez [classes de fenêtre](/windows/desktop/winmsg/window-classes).</span><span class="sxs-lookup"><span data-stu-id="b41b5-147">For more information about window classes, see [Window Classes](/windows/desktop/winmsg/window-classes).</span></span>

## <a name="sharing-icon-resources"></a><span data-ttu-id="b41b5-148">Ressources de l’icône de partage</span><span class="sxs-lookup"><span data-stu-id="b41b5-148">Sharing Icon Resources</span></span>

<span data-ttu-id="b41b5-149">Le code suivant utilise les fonctions [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex), [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon)et [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex), ainsi que plusieurs des fonctions de ressource, pour créer un handle d’icône basé sur les données d’icône d’un autre fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="b41b5-149">The following code uses the functions [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex), [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon), and [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex), and several of the resource functions, to create an icon handle based on icon data from another executable file.</span></span> <span data-ttu-id="b41b5-150">Il affiche ensuite l’icône dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b41b5-150">Then, it displays the icon in a window.</span></span>

<span data-ttu-id="b41b5-151">**Avertissement de sécurité :** L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut compromettre la sécurité de votre application en chargeant la dll incorrecte.</span><span class="sxs-lookup"><span data-stu-id="b41b5-151">**Security Warning:** Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="b41b5-152">Reportez-vous à la documentation de **LoadLibrary** pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="b41b5-152">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>


```
HICON hIcon1;       // icon handle 
HINSTANCE hExe;     // handle to loaded .EXE file 
HRSRC hResource;    // handle to FindResource  
HRSRC hMem;         // handle to LoadResource 
BYTE *lpResource;   // pointer to resource data  
int nID;            // ID of resource that best fits current screen 
 
HDC hdc;        // handle to display context 
 
// Load the file from which to copy the icon. 
// Note: LoadLibrary should have a fully explicit path.
//
hExe = LoadLibrary("myapp.exe");
if (hExe == NULL)
{
    //Error loading module -- fail as securely as possible
    return;
}
 
 
// Find the icon directory whose identifier is 440. 
 
hResource = FindResource(hExe, 
    MAKEINTRESOURCE(440), 
    RT_GROUP_ICON); 
 
// Load and lock the icon directory. 
 
hMem = LoadResource(hExe, hResource); 
 
lpResource = LockResource(hMem); 
 
// Get the identifier of the icon that is most appropriate 
// for the video display. 
 
nID = LookupIconIdFromDirectoryEx((PBYTE) lpResource, TRUE, 
    CXICON, CYICON, LR_DEFAULTCOLOR); 
 
// Find the bits for the nID icon. 
 
hResource = FindResource(hExe, 
    MAKEINTRESOURCE(nID), 
    MAKEINTRESOURCE(RT_ICON)); 
 
// Load and lock the icon. 
 
hMem = LoadResource(hExe, hResource); 
 
lpResource = LockResource(hMem); 
 
// Create a handle to the icon. 
 
hIcon1 = CreateIconFromResourceEx((PBYTE) lpResource, 
    SizeofResource(hExe, hResource), TRUE, 0x00030000, 
    CXICON, CYICON, LR_DEFAULTCOLOR); 
 
// Draw the icon in the client area. 
 
DrawIcon(hdc, 10, 20, hIcon1); 
```



 

 
