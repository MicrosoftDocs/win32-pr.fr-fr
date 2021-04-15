---
title: Utilisation de l’objet Active Desktop
description: Cet article contient des informations sur l’objet ActiveDesktop qui fait partie de l’API du shell Windows. Cet objet, via son interface IActiveDesktop, vous permet d’ajouter, de supprimer et de modifier des éléments sur le bureau.
ms.assetid: 68d72b0f-f5e9-4fff-bb13-4c60d1dd7009
keywords:
- Objet ActiveDesktop
- Active Desktop
- énumération, éléments du Bureau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e61a4a9145386fc4c84a454aa79558b8d5df79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462990"
---
# <a name="using-the-active-desktop-object"></a><span data-ttu-id="f790a-107">Utilisation de l’objet Active Desktop</span><span class="sxs-lookup"><span data-stu-id="f790a-107">Using the Active Desktop Object</span></span>

<span data-ttu-id="f790a-108">\[Cette fonctionnalité est prise en charge uniquement sous Windows XP ou version antérieure.</span><span class="sxs-lookup"><span data-stu-id="f790a-108">\[This feature is supported only under Windows XP or earlier.</span></span> <span data-ttu-id="f790a-109">\]</span><span class="sxs-lookup"><span data-stu-id="f790a-109">\]</span></span>

<span data-ttu-id="f790a-110">Cet article contient des informations sur l’objet **ActiveDesktop** qui fait partie de l’API du shell Windows.</span><span class="sxs-lookup"><span data-stu-id="f790a-110">This article contains information on the **ActiveDesktop** object that is part of the Windows Shell API.</span></span> <span data-ttu-id="f790a-111">Cet objet, via son interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , vous permet d’ajouter, de supprimer et de modifier des éléments sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="f790a-111">This object, through its [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface, enables you to add, remove, and change items on the desktop.</span></span>

## <a name="overview-of-the-active-desktop-interface"></a><span data-ttu-id="f790a-112">Vue d’ensemble de l’interface Active Desktop</span><span class="sxs-lookup"><span data-stu-id="f790a-112">Overview of the Active Desktop Interface</span></span>

-   [<span data-ttu-id="f790a-113">Accès à Active Desktop</span><span class="sxs-lookup"><span data-stu-id="f790a-113">Accessing the Active Desktop</span></span>](#accessing-the-active-desktop)
-   [<span data-ttu-id="f790a-114">Ajout d’un élément de bureau</span><span class="sxs-lookup"><span data-stu-id="f790a-114">Adding a Desktop Item</span></span>](#adding-a-desktop-item)
-   [<span data-ttu-id="f790a-115">Énumération des éléments du Bureau</span><span class="sxs-lookup"><span data-stu-id="f790a-115">Enumerating the Desktop Items</span></span>](#enumerating-the-desktop-items)

<span data-ttu-id="f790a-116">Active Desktop est une fonctionnalité introduite dans Microsoft Internet Explorer 4,0 qui vous permet d’inclure des documents et des éléments HTML (tels que des contrôles Microsoft ActiveX et des applets Java) directement sur votre bureau.</span><span class="sxs-lookup"><span data-stu-id="f790a-116">The Active Desktop is a feature introduced with Microsoft Internet Explorer 4.0 that enables you to include HTML documents and items (such as Microsoft ActiveX Controls and Java applets) directly to your desktop.</span></span> <span data-ttu-id="f790a-117">L’interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , qui fait partie de l’API Windows Shell, est utilisée pour ajouter, supprimer et modifier des éléments sur le bureau par programmation.</span><span class="sxs-lookup"><span data-stu-id="f790a-117">The [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface, which is part of the Windows Shell API, is used to programmatically add, remove, and modify the items on the desktop.</span></span> <span data-ttu-id="f790a-118">Vous pouvez également ajouter des éléments Active Desktop à l’aide d’un fichier CDF (Channel Definition Format).</span><span class="sxs-lookup"><span data-stu-id="f790a-118">Active Desktop items can also be added using a Channel Definition Format (CDF) file.</span></span>

### <a name="accessing-the-active-desktop"></a><span data-ttu-id="f790a-119">Accès à Active Desktop</span><span class="sxs-lookup"><span data-stu-id="f790a-119">Accessing the Active Desktop</span></span>

<span data-ttu-id="f790a-120">Pour accéder à Active Desktop, une application cliente doit créer une instance de l’objet ActiveDesktop (CLSID \_ ActiveDesktop) avec la fonction [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) et récupérer un pointeur vers l’interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f790a-120">To access the Active Desktop, a client application would need to create an instance of the ActiveDesktop object (CLSID\_ActiveDesktop) with the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function and retrieve a pointer to the object's [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface.</span></span>

<span data-ttu-id="f790a-121">L’exemple suivant montre comment récupérer un pointeur vers l’interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) .</span><span class="sxs-lookup"><span data-stu-id="f790a-121">The following sample shows how to retrieve a pointer to the [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface.</span></span>


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



### <a name="adding-a-desktop-item"></a><span data-ttu-id="f790a-122">Ajout d’un élément de bureau</span><span class="sxs-lookup"><span data-stu-id="f790a-122">Adding a Desktop Item</span></span>

<span data-ttu-id="f790a-123">Il existe trois méthodes que vous pouvez utiliser pour ajouter un élément de bureau : [**IActiveDesktop :: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem), [**IActiveDesktop :: AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui)et [**IActiveDesktop :: AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl).</span><span class="sxs-lookup"><span data-stu-id="f790a-123">There are three methods you can use to add a desktop item: [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem), [**IActiveDesktop::AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui), and [**IActiveDesktop::AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl).</span></span> <span data-ttu-id="f790a-124">Chaque élément de bureau ajouté à Active Desktop doit avoir une URL source différente.</span><span class="sxs-lookup"><span data-stu-id="f790a-124">Each desktop item added to the Active Desktop must have a different source URL.</span></span>

<span data-ttu-id="f790a-125">Les méthodes [**IActiveDesktop :: AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui) et [**IActiveDesktop :: AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl) fournissent toutes les deux la possibilité d’afficher les différentes interfaces utilisateur qui peuvent être affichées avant l’ajout d’un élément de bureau à Active Desktop.</span><span class="sxs-lookup"><span data-stu-id="f790a-125">The [**IActiveDesktop::AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui) and [**IActiveDesktop::AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl) methods both provide the option to display the various user interfaces that can be displayed before adding a desktop item to the Active Desktop.</span></span> <span data-ttu-id="f790a-126">Les interfaces vérifient si les utilisateurs souhaitent ajouter l’élément de bureau à leur bureau actif.</span><span class="sxs-lookup"><span data-stu-id="f790a-126">The interfaces verify whether users want to add the desktop item to their Active Desktop.</span></span> <span data-ttu-id="f790a-127">Les interfaces informent également les utilisateurs de tous les risques de sécurité qui sont garantis par les paramètres de la zone de sécurité URL et demandent aux utilisateurs s’ils souhaitent créer un abonnement pour cet élément de bureau.</span><span class="sxs-lookup"><span data-stu-id="f790a-127">The interfaces also notify users of any security risks that are warranted by the URL security zone settings, and they ask users if they would like to create a subscription for this desktop item.</span></span> <span data-ttu-id="f790a-128">Les deux méthodes fournissent également un moyen de supprimer les interfaces utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f790a-128">Both methods also provide a way of suppressing the user interfaces.</span></span> <span data-ttu-id="f790a-129">La méthode [**IActiveDesktop :: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) requiert un appel à [**IActiveDesktop :: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) afin de mettre à jour le registre.</span><span class="sxs-lookup"><span data-stu-id="f790a-129">The [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) method requires a call to [**IActiveDesktop::ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) in order to update the registry.</span></span> <span data-ttu-id="f790a-130">Pour **IActiveDesktop :: AddDesktopItemWithUI**, l’application cliente doit immédiatement libérer l' [**interface IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , puis utiliser la fonction [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour récupérer une interface vers une instance de l’objet **ActiveDesktop** qui comprend l’élément Desktop nouvellement ajouté.</span><span class="sxs-lookup"><span data-stu-id="f790a-130">For the **IActiveDesktop::AddDesktopItemWithUI**, the client application must immediately release the [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface and then use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function to retrieve an interface to an instance of the **ActiveDesktop** object that includes the newly added desktop item.</span></span>

<span data-ttu-id="f790a-131">La méthode [**IActiveDesktop :: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) ajoute l’élément de bureau spécifié au bureau actif sans interface utilisateur, sauf si les paramètres de la zone de sécurité de l’URL l’empêchent.</span><span class="sxs-lookup"><span data-stu-id="f790a-131">The [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) method adds the specified desktop item to the Active Desktop without any user interface, unless the URL security zone settings prevent it.</span></span> <span data-ttu-id="f790a-132">Si les paramètres de la zone de sécurité URL n’autorisent pas l’ajout de l’élément de bureau sans inviter l’utilisateur, la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="f790a-132">If the URL security zone settings do not allow the desktop item to be added without prompting the user, the method fails.</span></span> <span data-ttu-id="f790a-133">**IActiveDesktop :: AddDesktopItem** nécessite également un appel à [**IActiveDesktop :: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) pour mettre à jour le registre.</span><span class="sxs-lookup"><span data-stu-id="f790a-133">**IActiveDesktop::AddDesktopItem** also requires a call to [**IActiveDesktop::ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) in order to update the registry.</span></span>

<span data-ttu-id="f790a-134">L’exemple suivant montre comment ajouter un élément de bureau avec la méthode [**IActiveDesktop :: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) .</span><span class="sxs-lookup"><span data-stu-id="f790a-134">The following sample demonstrates how to add a desktop item with the [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) method.</span></span>


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



### <a name="enumerating-the-desktop-items"></a><span data-ttu-id="f790a-135">Énumération des éléments du Bureau</span><span class="sxs-lookup"><span data-stu-id="f790a-135">Enumerating the Desktop Items</span></span>

<span data-ttu-id="f790a-136">Pour énumérer les éléments du Bureau actuellement installés sur le bureau actif, l’application cliente doit récupérer le nombre total d’éléments de bureau installés à l’aide de la méthode [**IActiveDesktop :: GetDesktopItemCount**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount) , puis créer une boucle qui récupère la structure du [**composant**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component) pour chaque élément du Bureau en appelant la méthode [**IActiveDesktop :: GetDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem) à l’aide de l’index de l’élément de bureau.</span><span class="sxs-lookup"><span data-stu-id="f790a-136">To enumerate the desktop items currently installed on the Active Desktop, the client application needs to retrieve the total number of desktop items installed using the [**IActiveDesktop::GetDesktopItemCount**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount) method and then creating a loop that retrieves the [**COMPONENT**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component) structure for each desktop item by calling the [**IActiveDesktop::GetDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem) method using the desktop item index.</span></span>

<span data-ttu-id="f790a-137">L’exemple suivant illustre une façon d’énumérer les éléments du bureau.</span><span class="sxs-lookup"><span data-stu-id="f790a-137">The following sample demonstrates one way to enumerate the desktop items.</span></span>


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



 

 