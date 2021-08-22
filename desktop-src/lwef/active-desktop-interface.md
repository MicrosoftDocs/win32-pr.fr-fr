---
title: Utilisation de l’objet Active Desktop
description: cet article contient des informations sur l’objet ActiveDesktop qui fait partie de l’API Windows Shell. Cet objet, via son interface IActiveDesktop, vous permet d’ajouter, de supprimer et de modifier des éléments sur le bureau.
ms.assetid: 68d72b0f-f5e9-4fff-bb13-4c60d1dd7009
keywords:
- Objet ActiveDesktop
- Active Desktop
- énumération, éléments du Bureau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6daf1b5fbc73286619f07c8af76fbbce53bcaa8962cc88cf20f5af74bbdec82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610659"
---
# <a name="using-the-active-desktop-object"></a>Utilisation de l’objet Active Desktop

\[cette fonctionnalité est prise en charge uniquement sous Windows XP ou version antérieure. \]

cet article contient des informations sur l’objet **ActiveDesktop** qui fait partie de l’API Windows Shell. Cet objet, via son interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , vous permet d’ajouter, de supprimer et de modifier des éléments sur le bureau.

## <a name="overview-of-the-active-desktop-interface"></a>Vue d’ensemble de l’interface Active Desktop

-   [Accès à Active Desktop](#accessing-the-active-desktop)
-   [Ajout d’un élément de bureau](#adding-a-desktop-item)
-   [Énumération des éléments du Bureau](#enumerating-the-desktop-items)

Active Desktop est une fonctionnalité introduite dans Microsoft Internet Explorer 4,0 qui vous permet d’inclure des documents et des éléments HTML (tels que des contrôles Microsoft ActiveX et des applets Java) directement sur votre bureau. l’interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , qui fait partie de l’API Windows Shell, est utilisée pour ajouter, supprimer et modifier des éléments sur le bureau par programmation. Vous pouvez également ajouter des éléments Active Desktop à l’aide d’un fichier CDF (Channel Definition Format).

### <a name="accessing-the-active-desktop"></a>Accès à Active Desktop

Pour accéder à Active Desktop, une application cliente doit créer une instance de l’objet ActiveDesktop (CLSID \_ ActiveDesktop) avec la fonction [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) et récupérer un pointeur vers l’interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) de l’objet.

L’exemple suivant montre comment récupérer un pointeur vers l’interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) .


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

//Insert code to call the IActiveDesktop methods

// Call the Release method
pActiveDesktop->Release();
```



### <a name="adding-a-desktop-item"></a>Ajout d’un élément de bureau

Il existe trois méthodes que vous pouvez utiliser pour ajouter un élément de bureau : [**IActiveDesktop :: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem), [**IActiveDesktop :: AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui)et [**IActiveDesktop :: AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl). Chaque élément de bureau ajouté à Active Desktop doit avoir une URL source différente.

Les méthodes [**IActiveDesktop :: AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui) et [**IActiveDesktop :: AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl) fournissent toutes les deux la possibilité d’afficher les différentes interfaces utilisateur qui peuvent être affichées avant l’ajout d’un élément de bureau à Active Desktop. Les interfaces vérifient si les utilisateurs souhaitent ajouter l’élément de bureau à leur bureau actif. Les interfaces informent également les utilisateurs de tous les risques de sécurité qui sont garantis par les paramètres de la zone de sécurité URL et demandent aux utilisateurs s’ils souhaitent créer un abonnement pour cet élément de bureau. Les deux méthodes fournissent également un moyen de supprimer les interfaces utilisateur. La méthode [**IActiveDesktop :: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) requiert un appel à [**IActiveDesktop :: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) afin de mettre à jour le registre. Pour **IActiveDesktop :: AddDesktopItemWithUI**, l’application cliente doit immédiatement libérer l' [**interface IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , puis utiliser la fonction [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour récupérer une interface vers une instance de l’objet **ActiveDesktop** qui comprend l’élément Desktop nouvellement ajouté.

La méthode [**IActiveDesktop :: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) ajoute l’élément de bureau spécifié au bureau actif sans interface utilisateur, sauf si les paramètres de la zone de sécurité de l’URL l’empêchent. Si les paramètres de la zone de sécurité URL n’autorisent pas l’ajout de l’élément de bureau sans inviter l’utilisateur, la méthode échoue. **IActiveDesktop :: AddDesktopItem** nécessite également un appel à [**IActiveDesktop :: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) pour mettre à jour le registre.

L’exemple suivant montre comment ajouter un élément de bureau avec la méthode [**IActiveDesktop :: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) .


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

// Initialize the COMPONENT structure
compDesktopItem.dwSize = sizeof(COMPONENT);

// Insert code that adds the information about the desktop item 
// to the COMPONENT structure

// Add the desktop item
pActiveDesktop->AddDesktopItem(&compDesktopItem,0);

// Save the changes to the registry
pActiveDesktop->ApplyChanges(AD_APPLY_ALL);
```



### <a name="enumerating-the-desktop-items"></a>Énumération des éléments du Bureau

Pour énumérer les éléments du Bureau actuellement installés sur le bureau actif, l’application cliente doit récupérer le nombre total d’éléments de bureau installés à l’aide de la méthode [**IActiveDesktop :: GetDesktopItemCount**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount) , puis créer une boucle qui récupère la structure du [**composant**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component) pour chaque élément du Bureau en appelant la méthode [**IActiveDesktop :: GetDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem) à l’aide de l’index de l’élément de bureau.

L’exemple suivant illustre une façon d’énumérer les éléments du bureau.


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;
int intCount;
int intIndex = 0;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

pActiveDesktop->GetDesktopItemCount(&intCount,0);

compDesktopItem.dwSize = sizeof(COMPONENT);

while(intIndex<=(intCount-1))
{
    //get the COMPONENT structure for the current desktop item
    pActiveDesktop->GetDesktopItem(intIndex, &compDesktopItem,0);

    //Insert code that processes the structure

    //Increment the index
    intIndex++;

    //Insert code to clean-up structure for next component
}

// Call the Release method
pActiveDesktop->Release();
```



 

 