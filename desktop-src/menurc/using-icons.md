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
ms.openlocfilehash: 03202c250502794d5f845bcc8c2ae263d919ea62
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327114"
---
# <a name="using-icons"></a>Utilisation des icônes

Les rubriques suivantes décrivent comment effectuer certaines tâches liées aux icônes :

-   [Création d’une icône](#creating-an-icon)
-   [Affichage d’une icône](#displaying-an-icon)
-   [Ressources de l’icône de partage](#sharing-icon-resources)

## <a name="creating-an-icon"></a>Création d’une icône

Pour utiliser une icône, votre application doit obtenir un handle vers l’icône. L’exemple suivant montre comment créer deux descripteurs d’icône différents : un pour l’icône de question standard et un pour une icône personnalisée incluse en tant que ressource dans le fichier de définition de ressources de l’application.


```
HICON hIcon1;   // icon handle 
HICON hIcon2;   // icon handle 
 
// Create a standard question icon. 
 
hIcon1 = LoadIcon(NULL, IDI_QUESTION); 
 
// Create a custom icon based on a resource. 
 
hIcon2 = LoadIcon(hinst, MAKEINTRESOURCE(460)); 
 
// Create a custom icon at run time.
 
```



Une application doit implémenter des icônes personnalisées en tant que ressources et doit utiliser la fonction [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) ou [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) , au lieu de créer les icônes au moment de l’exécution. Cette approche évite la dépendance des appareils, simplifie la localisation et permet aux applications de partager des bitmaps d’icône. Toutefois, l’exemple suivant utilise [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) pour créer une icône personnalisée au moment de l’exécution, en fonction des masques de bits de bitmap. Il est inclus pour illustrer la façon dont le système interprète les masques de pixels de l’icône.


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



Pour créer l’icône, [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) applique la table de vérité suivante aux masques de et et XOR.



| ET masque de masque | Masque de masque XOR | Affichage        |
|-------------|-------------|----------------|
| 0           | 0           | Noir          |
| 0           | 1           | Blancs          |
| 1           | 0           | Screen         |
| 1           | 1           | Écran inversé |



 

Avant de fermer, votre application doit utiliser [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) pour détruire toute icône qu’elle a créée à l’aide de [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect). Il n’est pas nécessaire de détruire les icônes créées par d’autres fonctions.

## <a name="displaying-an-icon"></a>Affichage d’une icône

Votre application peut charger et créer des icônes à afficher dans la zone cliente de l’application ou dans les fenêtres enfants. L’exemple suivant montre comment dessiner une icône dans la zone cliente de la fenêtre dont le contexte de périphérique (DC) est identifié par le paramètre *HDC* .


```
HICON hIcon1;   // icon handle  
HDC hdc;        // handle to display context 
 
DrawIcon(hdc, 10, 20, hIcon1); 
```



Le système affiche automatiquement la ou les icônes de classe d’une fenêtre. Votre application peut assigner des icônes de classe lors de l’inscription d’une classe de fenêtre. Votre application peut remplacer une icône de classe à l’aide de la fonction [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) . Cette fonction modifie les paramètres de fenêtre par défaut pour toutes les fenêtres d’une classe donnée. L’exemple suivant remplace une icône de classe par l’icône dont l’identificateur de ressource est 480.


```
HINSTANCE hinst;            // handle to current instance 
HWND hwnd;                  // main window handle  
 
// Change the icon for hwnd's window class. 
 
SetClassLongPtr(hwnd,          // window handle 
    GCLP_HICON,              // changes icon 
    (LONG_PTR) LoadIcon(hinst, MAKEINTRESOURCE(480))
   ); 
```



Pour plus d’informations sur les classes de fenêtre, consultez [classes de fenêtre](/windows/desktop/winmsg/window-classes).

## <a name="sharing-icon-resources"></a>Ressources de l’icône de partage

Le code suivant utilise les fonctions [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex), [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon)et [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex), ainsi que plusieurs des fonctions de ressource, pour créer un handle d’icône basé sur les données d’icône d’un autre fichier exécutable. Il affiche ensuite l’icône dans une fenêtre.

**Avertissement de sécurité :** L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut compromettre la sécurité de votre application en chargeant la dll incorrecte. Reportez-vous à la documentation de **LoadLibrary** pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Windows.


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



 

 
