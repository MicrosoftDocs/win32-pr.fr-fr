---
description: Quand l’utilisateur clique avec le bouton droit sur un membre d’un type de fichier pour afficher la feuille de propriétés propriétés, l’interpréteur de commandes appelle les gestionnaires de feuille de propriétés qui sont inscrits pour le type de fichier. Chaque gestionnaire peut ajouter une page personnalisée à la feuille de propriétés par défaut.
title: Comment inscrire et implémenter un gestionnaire de feuille de propriétés pour un type de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77cf54886f7819fa910da23393c6db488ddfee72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991556"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-file-type"></a><span data-ttu-id="1ebab-104">Comment inscrire et implémenter un gestionnaire de feuille de propriétés pour un type de fichier</span><span class="sxs-lookup"><span data-stu-id="1ebab-104">How to Register and Implement a Property Sheet Handler for a File Type</span></span>

<span data-ttu-id="1ebab-105">Quand l’utilisateur clique avec le bouton droit sur un membre d’un type de fichier pour afficher la feuille de propriétés propriétés, l’interpréteur de commandes appelle les gestionnaires de feuille de propriétés qui sont inscrits pour le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="1ebab-105">When the user right-clicks a member of a file type to display the Properties property sheet, the Shell calls the property sheet handlers that are registered for the file type.</span></span> <span data-ttu-id="1ebab-106">Chaque gestionnaire peut ajouter une page personnalisée à la feuille de propriétés par défaut.</span><span class="sxs-lookup"><span data-stu-id="1ebab-106">Each handler can add one custom page to the default property sheet.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="1ebab-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="1ebab-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1ebab-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="1ebab-108">Technologies</span></span>

-   <span data-ttu-id="1ebab-109">Shell</span><span class="sxs-lookup"><span data-stu-id="1ebab-109">Shell</span></span>

### <a name="prerequisites"></a><span data-ttu-id="1ebab-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="1ebab-110">Prerequisites</span></span>

-   <span data-ttu-id="1ebab-111">Compréhension des menus contextuels</span><span class="sxs-lookup"><span data-stu-id="1ebab-111">An understanding of shortcut menus</span></span>

## <a name="instructions"></a><span data-ttu-id="1ebab-112">Instructions</span><span class="sxs-lookup"><span data-stu-id="1ebab-112">Instructions</span></span>

### <a name="step-1-registering-a-property-sheet-handler-for-a-file-type"></a><span data-ttu-id="1ebab-113">Étape 1 : inscription d’un gestionnaire de feuille de propriétés pour un type de fichier</span><span class="sxs-lookup"><span data-stu-id="1ebab-113">Step 1: Registering a Property Sheet Handler for a File Type</span></span>

<span data-ttu-id="1ebab-114">En plus de l’inscription du modèle COM (Component Object Model) normal, ajoutez une sous-clé **PropertySheetHandlers** à la sous-clé **shellex** de la clé ProgID de l’application associée au type de fichier.</span><span class="sxs-lookup"><span data-stu-id="1ebab-114">In addition to normal Component Object Model (COM) registration, add a **PropertySheetHandlers** subkey to the **shellex** subkey of the ProgID key of the application associated with the file type.</span></span> <span data-ttu-id="1ebab-115">Créez une sous-clé de **PropertySheetHandlers** avec le nom du gestionnaire et définissez la valeur par défaut sur la forme de chaîne du GUID de l’identificateur de classe (CLSID) du gestionnaire de feuilles de propriétés.</span><span class="sxs-lookup"><span data-stu-id="1ebab-115">Create a subkey of **PropertySheetHandlers** with the handler's name, and set the default value to the string form of the property sheet handler's class identifier (CLSID) GUID.</span></span>

<span data-ttu-id="1ebab-116">Pour ajouter plusieurs pages à la feuille de propriétés, inscrivez un gestionnaire pour chaque page.</span><span class="sxs-lookup"><span data-stu-id="1ebab-116">To add more than one page to the property sheet, register a handler for each page.</span></span> <span data-ttu-id="1ebab-117">Le nombre maximal de pages qu’une feuille de propriétés peut prendre en charge est 32.</span><span class="sxs-lookup"><span data-stu-id="1ebab-117">The maximum number of pages that a property sheet can support is 32.</span></span> <span data-ttu-id="1ebab-118">Pour inscrire plusieurs gestionnaires, créez une clé sous la clé **shellex** pour chaque gestionnaire, avec la valeur par défaut définie sur le GUID CLSID du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="1ebab-118">To register multiple handlers, create a key under the **shellex** key for each handler, with the default value set to the handler's CLSID GUID.</span></span> <span data-ttu-id="1ebab-119">Il n’est pas nécessaire de créer un objet distinct pour chaque gestionnaire, ce qui signifie que plusieurs gestionnaires peuvent tous avoir la même valeur GUID.</span><span class="sxs-lookup"><span data-stu-id="1ebab-119">It is not necessary to create a distinct object for each handler, which means that multiple handlers can all have the same GUID value.</span></span> <span data-ttu-id="1ebab-120">Les pages s’affichent dans l’ordre dans lequel leurs clés sont répertoriées sous **shellex**.</span><span class="sxs-lookup"><span data-stu-id="1ebab-120">The pages will be displayed in the order that their keys are listed under **shellex**.</span></span>

<span data-ttu-id="1ebab-121">L’exemple suivant illustre une entrée de Registre qui active deux gestionnaires d’extension de feuille de propriétés pour un exemple de type de fichier. MYP.</span><span class="sxs-lookup"><span data-stu-id="1ebab-121">The following example illustrates a registry entry that enables two property sheet extension handlers for an example .myp file type.</span></span> <span data-ttu-id="1ebab-122">Dans cet exemple, un objet distinct est utilisé pour chaque page, mais un seul objet peut également être utilisé pour les deux.</span><span class="sxs-lookup"><span data-stu-id="1ebab-122">In this example, a separate object is used for each page, but a single object could also be used for both.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {Page 1 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet1.dll
            ThreadingModel = Apartment
      {Page 2 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet2.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         PropertySheetHandlers
            MyPropSheet1
               (Default) = {Page1 Property Sheet Handler CLSID GUID}
            MyPropSheet2
               (Default) = {Page2 Property Sheet Handler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-file-type"></a><span data-ttu-id="1ebab-123">Étape 2 : implémentation d’un gestionnaire de feuille de propriétés pour un type de fichier</span><span class="sxs-lookup"><span data-stu-id="1ebab-123">Step 2: Implementing a Property Sheet Handler for a File Type</span></span>

<span data-ttu-id="1ebab-124">En plus de l’implémentation générale décrite dans [Comment fonctionnent les gestionnaires de feuille de propriétés](propsheet-handlers.md), un gestionnaire de feuille de propriétés pour un type de fichier doit également avoir une implémentation appropriée de l’interface [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) .</span><span class="sxs-lookup"><span data-stu-id="1ebab-124">In addition to the general implementation discussed in [How Property Sheet Handlers Work](propsheet-handlers.md), a property sheet handler for a file type must also have an appropriate implementation of the [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) interface.</span></span> <span data-ttu-id="1ebab-125">Seule la méthode [**IShellPropSheetExt :: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) a besoin d’une implémentation qui n’est pas un jeton.</span><span class="sxs-lookup"><span data-stu-id="1ebab-125">Only the [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) method needs a nontoken implementation.</span></span> <span data-ttu-id="1ebab-126">L’interpréteur de commandes n’appelle pas [**IShellPropSheetExt :: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage).</span><span class="sxs-lookup"><span data-stu-id="1ebab-126">The Shell does not call [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage).</span></span>

<span data-ttu-id="1ebab-127">La méthode [**IShellPropSheetExt :: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) permet à un gestionnaire de feuilles de propriétés d’ajouter une page à une feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="1ebab-127">The [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) method allows a property sheet handler to add a page to a property sheet.</span></span> <span data-ttu-id="1ebab-128">La méthode a deux paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1ebab-128">The method has two input parameters.</span></span> <span data-ttu-id="1ebab-129">Le premier, *lpfnAddPage*, est un pointeur vers une fonction de rappel [*AddPropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) qui est utilisé pour fournir l’interpréteur de commandes avec les informations nécessaires pour ajouter la page à la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="1ebab-129">The first, *lpfnAddPage*, is a pointer to an [*AddPropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) callback function that is used to provide the Shell with the information needed to add the page to the property sheet.</span></span> <span data-ttu-id="1ebab-130">La seconde, *lParam*, est une valeur définie par l’interpréteur de commandes qui n’est pas traitée par le gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="1ebab-130">The second, *lParam*, is a Shell-defined value that is not processed by the handler.</span></span> <span data-ttu-id="1ebab-131">Il est simplement renvoyé à l’interpréteur de commandes lorsque la fonction de rappel est appelée.</span><span class="sxs-lookup"><span data-stu-id="1ebab-131">It is simply passed back to the Shell when the callback function is called.</span></span>

<span data-ttu-id="1ebab-132">La procédure générale pour l’implémentation de [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) est la suivante.</span><span class="sxs-lookup"><span data-stu-id="1ebab-132">The general procedure for implementing [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) is as follows.</span></span>

<span data-ttu-id="1ebab-133">**Implémentation de la méthode AddPages**</span><span class="sxs-lookup"><span data-stu-id="1ebab-133">**Implementing the AddPages Method**</span></span>

1.  <span data-ttu-id="1ebab-134">Assignez des valeurs appropriées aux membres d’une structure [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) .</span><span class="sxs-lookup"><span data-stu-id="1ebab-134">Assign appropriate values to the members of a [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) structure.</span></span> <span data-ttu-id="1ebab-135">En particulier :</span><span class="sxs-lookup"><span data-stu-id="1ebab-135">In particular:</span></span>
    -   <span data-ttu-id="1ebab-136">Assignez la variable qui contient le décompte de références du gestionnaire au membre **pcRefParent** .</span><span class="sxs-lookup"><span data-stu-id="1ebab-136">Assign the variable that holds the handler's reference count to the **pcRefParent** member.</span></span> <span data-ttu-id="1ebab-137">Cette pratique empêche l’objet gestionnaire d’être déchargé pendant que la feuille de propriétés est toujours affichée.</span><span class="sxs-lookup"><span data-stu-id="1ebab-137">This practice prevents the handler object from being unloaded while the property sheet is still being displayed.</span></span>
    -   <span data-ttu-id="1ebab-138">Vous pouvez également implémenter une fonction de rappel [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) et assigner son pointeur à un membre **pfnCallback** .</span><span class="sxs-lookup"><span data-stu-id="1ebab-138">You can also implement a [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) callback function and assign its pointer to a **pfnCallback** member.</span></span> <span data-ttu-id="1ebab-139">Cette fonction est appelée lorsque la page est créée et lorsqu’elle est sur le lieu d’être détruite.</span><span class="sxs-lookup"><span data-stu-id="1ebab-139">This function is called when the page is created and when it is about to be destroyed.</span></span>
2.  <span data-ttu-id="1ebab-140">Créez le handle HPAGE de la page en passant la structure [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) à la fonction [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) .</span><span class="sxs-lookup"><span data-stu-id="1ebab-140">Create the page's HPAGE handle by passing the [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) structure to the [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) function.</span></span>
3.  <span data-ttu-id="1ebab-141">Appelez la fonction vers laquelle pointe *lpfnAddPage*.</span><span class="sxs-lookup"><span data-stu-id="1ebab-141">Call the function that is pointed to by *lpfnAddPage*.</span></span> <span data-ttu-id="1ebab-142">Définissez son premier paramètre sur le handle HPAGE créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="1ebab-142">Set its first parameter to the HPAGE handle that was created in the previous step.</span></span> <span data-ttu-id="1ebab-143">Affectez à son deuxième paramètre la valeur *lParam* qui a été transmise à [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) par l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="1ebab-143">Set its second parameter to the *lParam* value that was passed in to [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) by the Shell.</span></span>
4.  <span data-ttu-id="1ebab-144">Tous les messages associés à la page sont transmis à la procédure de boîte de dialogue qui a été assignée au membre **pfnDlgProc** de la structure [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) .</span><span class="sxs-lookup"><span data-stu-id="1ebab-144">Any messages associated with the page will be passed to the dialog box procedure that was assigned to the **pfnDlgProc** member of the [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) structure.</span></span>
5.  <span data-ttu-id="1ebab-145">Si vous avez affecté une fonction de rappel [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) à **pfnCallback**, elle est appelée lorsque la page va être détruite.</span><span class="sxs-lookup"><span data-stu-id="1ebab-145">If you assigned a [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) callback function to **pfnCallback**, it will be called when the page is about to be destroyed.</span></span> <span data-ttu-id="1ebab-146">Votre gestionnaire peut ensuite effectuer les opérations de nettoyage nécessaires, telles que la libération des références qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="1ebab-146">Your handler can then perform any needed cleanup operations, such as releasing any references that it holds.</span></span>

<span data-ttu-id="1ebab-147">L’exemple de code suivant illustre une implémentation simple de [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) .</span><span class="sxs-lookup"><span data-stu-id="1ebab-147">The following code sample illustrates a simple [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) implementation.</span></span>


```C++
STDMETHODIMP CShellPropSheetExt::AddPages(LPFNADDPROPSHEETPAGE, lpfnAddPage, LPARAM lParam)
{
    PROPSHEETPAGE  psp;
    HPROPSHEETPAGE hPage;

    psp.dwSize        = sizeof(psp);
    psp.dwFlags       = PSP_USEREFPARENT | PSP_USETITLE | PSP_USECALLBACK;
    psp.hInstance     = g_hInst;
    psp.pszTemplate   = MAKEINTRESOURCE(IDD_PAGEDLG);
    psp.hIcon         = 0;
    psp.pszTitle      = TEXT("Extension Page");
    psp.pfnDlgProc    = (DLGPROC)PageDlgProc;
    psp.pcRefParent   = &g_DllRefCount;
    psp.pfnCallback   = PageCallbackProc;
    psp.lParam        = (LPARAM)this;

    hPage = CreatePropertySheetPage(&psp);
            
    if(hPage) 
    {
        if(lpfnAddPage(hPage, lParam))
        {
            this->AddRef();
            return S_OK;
        }
        else
        {
            DestroyPropertySheetPage(hPage);
        }
    }
    else
    {
        return E_OUTOFMEMORY;
    }
    return E_FAIL;
}
```



<span data-ttu-id="1ebab-148">La variable **g \_ HINST** est le handle d’instance de la dll et IDD \_ PAGEDLG est l’ID de ressource du modèle de boîte de dialogue de la page.</span><span class="sxs-lookup"><span data-stu-id="1ebab-148">The **g\_hInst** variable is the instance handle to the DLL, and IDD\_PAGEDLG is the resource ID of the page's dialog box template.</span></span> <span data-ttu-id="1ebab-149">La fonction **PageDlgProc** est la procédure de boîte de dialogue qui gère les messages de la page.</span><span class="sxs-lookup"><span data-stu-id="1ebab-149">The **PageDlgProc** function is the dialog box procedure that handles the page's messages.</span></span> <span data-ttu-id="1ebab-150">La variable **g \_ DllRefCount** contient le nombre de références de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1ebab-150">The **g\_DllRefCount** variable holds the object's reference count.</span></span> <span data-ttu-id="1ebab-151">La méthode [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) appelle [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) pour incrémenter le nombre.</span><span class="sxs-lookup"><span data-stu-id="1ebab-151">The [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) method calls [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) to increment the count.</span></span> <span data-ttu-id="1ebab-152">Toutefois, le décompte de références est libéré par la fonction de rappel, **PageCallbackProc**, lorsque la page va être détruite.</span><span class="sxs-lookup"><span data-stu-id="1ebab-152">However, the reference count is released by the callback function, **PageCallbackProc**, when the page is about to be destroyed.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ebab-153">Notes</span><span class="sxs-lookup"><span data-stu-id="1ebab-153">Remarks</span></span>

<span data-ttu-id="1ebab-154">Pour obtenir une présentation générale de l’inscription des gestionnaires d’extensions de Shell, consultez [création de gestionnaires d’extensions de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="1ebab-154">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ebab-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1ebab-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ebab-156">**IShellPropSheetExt**</span><span class="sxs-lookup"><span data-stu-id="1ebab-156">**IShellPropSheetExt**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
</dt> </dl>

 

 
