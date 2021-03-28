---
description: IContextMenu est la plus puissante, mais également l’interface la plus compliquée à implémenter.
ms.assetid: F0C1D60E-7A5A-4609-9136-F4E535E9F6F1
title: Comment implémenter l’interface IContextMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f251b9a64c3f401239eeb7c88286c016f399cc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951939"
---
# <a name="how-to-implement-the-icontextmenu-interface"></a><span data-ttu-id="c2d96-103">Comment implémenter l’interface IContextMenu</span><span class="sxs-lookup"><span data-stu-id="c2d96-103">How to Implement the IContextMenu Interface</span></span>

<span data-ttu-id="c2d96-104">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) est la plus puissante, mais également l’interface la plus compliquée à implémenter.</span><span class="sxs-lookup"><span data-stu-id="c2d96-104">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated interface to implement.</span></span> <span data-ttu-id="c2d96-105">Nous vous recommandons vivement d’implémenter un verbe à l’aide de l’une des méthodes Verb statiques.</span><span class="sxs-lookup"><span data-stu-id="c2d96-105">We strongly recommend that you implement a verb by using one of the static verb methods.</span></span> <span data-ttu-id="c2d96-106">Pour plus d’informations, consultez [choix d’une méthode de menu contextuel statique ou dynamique](shortcut-choose-method.md).</span><span class="sxs-lookup"><span data-stu-id="c2d96-106">For more information, see [Choosing a Static or Dynamic Shortcut Menu Method](shortcut-choose-method.md).</span></span> <span data-ttu-id="c2d96-107">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) a trois méthodes, [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring), [**commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)et [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), qui sont décrites ici en détail.</span><span class="sxs-lookup"><span data-stu-id="c2d96-107">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) has three methods, [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring), [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand), and [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), which are discussed here in detail.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c2d96-108">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="c2d96-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c2d96-109">Technologies</span><span class="sxs-lookup"><span data-stu-id="c2d96-109">Technologies</span></span>

-   <span data-ttu-id="c2d96-110">C++</span><span class="sxs-lookup"><span data-stu-id="c2d96-110">C++</span></span>

### <a name="prerequisites"></a><span data-ttu-id="c2d96-111">Prérequis</span><span class="sxs-lookup"><span data-stu-id="c2d96-111">Prerequisites</span></span>

-   <span data-ttu-id="c2d96-112">Verbe statique</span><span class="sxs-lookup"><span data-stu-id="c2d96-112">Static Verb</span></span>
-   <span data-ttu-id="c2d96-113">Menu contextuel</span><span class="sxs-lookup"><span data-stu-id="c2d96-113">Shortcut Menu</span></span>

## <a name="instructions"></a><span data-ttu-id="c2d96-114">Instructions</span><span class="sxs-lookup"><span data-stu-id="c2d96-114">Instructions</span></span>

### <a name="icontextmenugetcommandstring-method"></a><span data-ttu-id="c2d96-115">IContextMenu :: GetCommandString, méthode</span><span class="sxs-lookup"><span data-stu-id="c2d96-115">IContextMenu::GetCommandString Method</span></span>

<span data-ttu-id="c2d96-116">La méthode [**IContextMenu :: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) du gestionnaire est utilisée pour retourner le nom canonique d’un verbe.</span><span class="sxs-lookup"><span data-stu-id="c2d96-116">The handler's [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) method is used to return the canonical name for a verb.</span></span> <span data-ttu-id="c2d96-117">Cette méthode est facultative.</span><span class="sxs-lookup"><span data-stu-id="c2d96-117">This method is optional.</span></span> <span data-ttu-id="c2d96-118">Dans Windows XP et les versions antérieures de Windows, lorsque l’Explorateur Windows a une barre d’État, cette méthode est utilisée pour récupérer le texte d’aide qui s’affiche dans la barre d’État pour un élément de menu.</span><span class="sxs-lookup"><span data-stu-id="c2d96-118">In Windows XP and earlier versions of Windows, when Windows Explorer has a Status bar, this method is used to retrieve the help text that is displayed in the Status bar for a menu item.</span></span>

<span data-ttu-id="c2d96-119">Le paramètre *idCmd* contient le décalage de l’identificateur de la commande qui a été définie lors de l’appel de [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="c2d96-119">The *idCmd* parameter holds the identifier offset of the command that was defined when [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) was called.</span></span> <span data-ttu-id="c2d96-120">Si une chaîne d’aide est demandée, *uFlags* est défini sur **GC \_ HELPTEXTW**.</span><span class="sxs-lookup"><span data-stu-id="c2d96-120">If a help string is requested, *uFlags* will be set to **GCS\_HELPTEXTW**.</span></span> <span data-ttu-id="c2d96-121">Copiez la chaîne d’aide dans la mémoire tampon *pszName* , en la convertissant en **PWSTR**.</span><span class="sxs-lookup"><span data-stu-id="c2d96-121">Copy the help string to the *pszName* buffer, casting it to a **PWSTR**.</span></span> <span data-ttu-id="c2d96-122">La chaîne de verbe est demandée en affectant à *uFlags* la valeur **GC \_ VERBW**.</span><span class="sxs-lookup"><span data-stu-id="c2d96-122">The verb string is requested by setting *uFlags* to **GCS\_VERBW**.</span></span> <span data-ttu-id="c2d96-123">Copiez la chaîne appropriée dans *pszName*, tout comme avec la chaîne d’aide.</span><span class="sxs-lookup"><span data-stu-id="c2d96-123">Copy the appropriate string to *pszName*, just as with the help string.</span></span> <span data-ttu-id="c2d96-124">Les indicateurs **GC \_ Validate** et **GC \_ VALIDATEW** ne sont pas utilisés par les gestionnaires de menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="c2d96-124">The **GCS\_VALIDATEA** and **GCS\_VALIDATEW** flags are not used by shortcut menu handlers.</span></span>

<span data-ttu-id="c2d96-125">L’exemple suivant illustre une implémentation simple de [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) qui correspond à l’exemple [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) fourni dans la section de la [méthode IContextMenu :: QueryContextMenu](shortcut-menu-using-dynamic-verbs.md) de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="c2d96-125">The following example shows a simple implementation of [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) that corresponds to the [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) example given in the [IContextMenu::QueryContextMenu Method](shortcut-menu-using-dynamic-verbs.md) section of this topic.</span></span> <span data-ttu-id="c2d96-126">Étant donné que le gestionnaire ajoute un seul élément de menu, il n’existe qu’un seul jeu de chaînes qui peut être retourné.</span><span class="sxs-lookup"><span data-stu-id="c2d96-126">Because the handler adds only one menu item, there is only one set of strings that can be returned.</span></span> <span data-ttu-id="c2d96-127">La méthode teste si *idCmd* est valide et, si c’est le cas, retourne la chaîne demandée.</span><span class="sxs-lookup"><span data-stu-id="c2d96-127">The method tests whether *idCmd* is valid and, if it is, returns the requested string.</span></span>

<span data-ttu-id="c2d96-128">La fonction [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) est utilisée pour copier la chaîne demandée dans *pszName* afin de garantir que la chaîne copiée ne dépasse pas la taille de la mémoire tampon spécifiée par *cchName*.</span><span class="sxs-lookup"><span data-stu-id="c2d96-128">The [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) function is used to copy the requested string to *pszName* to ensure that the copied string does not exceed the size of the buffer specified by *cchName*.</span></span> <span data-ttu-id="c2d96-129">Cet exemple implémente la prise en charge uniquement des valeurs Unicode de *uFlags*, car seules celles-ci ont été utilisées dans l’Explorateur Windows depuis Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c2d96-129">This example implements support only for the Unicode values of *uFlags*, because only those have been used in Windows Explorer since Windows 2000.</span></span>


```
IFACEMETHODIMP CMenuExtension::GetCommandString(UINT idCommand, 
                                                UINT uFlags, 
                                                UINT *pReserved, 
                                                PSTR pszName, 
                                                UINT cchName)
{
    HRESULT hr = E_INVALIDARG;

    if (idCommand == IDM_DISPLAY)
    {
        switch (uFlags)
        {
            case GCS_HELPTEXTW:
                // Only useful for pre-Vista versions of Windows that 
                // have a Status bar.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"Display File Name");
                break; 

            case GCS_VERBW:
                // GCS_VERBW is an optional feature that enables a caller
                // to discover the canonical name for the verb that is passed in
                // through idCommand.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"DisplayFileName");
                break; 
        }
    }
    return hr;
}
```



### <a name="icontextmenuinvokecommand-method"></a><span data-ttu-id="c2d96-130">IContextMenu :: commande InvokeCommand, méthode</span><span class="sxs-lookup"><span data-stu-id="c2d96-130">IContextMenu::InvokeCommand Method</span></span>

<span data-ttu-id="c2d96-131">Cette méthode est appelée lorsqu’un utilisateur clique sur un élément de menu pour indiquer au gestionnaire d’exécuter la commande associée.</span><span class="sxs-lookup"><span data-stu-id="c2d96-131">This method is called when a user clicks a menu item to tell the handler to run the associated command.</span></span> <span data-ttu-id="c2d96-132">Le paramètre *Pici* pointe vers une structure qui contient les informations requises pour exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="c2d96-132">The *pici* parameter points to a structure that contains the information required to run the command.</span></span>

<span data-ttu-id="c2d96-133">Bien que *Pici* soit déclaré dans shlobj. h comme une structure [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) , dans la pratique, il pointe souvent vers une structure [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) .</span><span class="sxs-lookup"><span data-stu-id="c2d96-133">Although *pici* is declared in Shlobj.h as a [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) structure, in practice it often points to a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure.</span></span> <span data-ttu-id="c2d96-134">Cette structure est une version étendue de **CMINVOKECOMMANDINFO** et a plusieurs membres supplémentaires qui permettent de passer des chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="c2d96-134">This structure is an extended version of **CMINVOKECOMMANDINFO** and has several additional members that make it possible to pass Unicode strings.</span></span>

<span data-ttu-id="c2d96-135">Vérifiez le membre **cbSize** de *Pici* pour déterminer la structure qui a été transmise.</span><span class="sxs-lookup"><span data-stu-id="c2d96-135">Check the **cbSize** member of *pici* to determine which structure was passed in.</span></span> <span data-ttu-id="c2d96-136">S’il s’agit d’une structure [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) et que l’indicateur **\_ \_ Unicode de masque Cmic** est défini pour le membre **fmask** , castez *Pici* en **CMINVOKECOMMANDINFOEX**.</span><span class="sxs-lookup"><span data-stu-id="c2d96-136">If it is a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure and the **fMask** member has the **CMIC\_MASK\_UNICODE** flag set, cast *pici* to **CMINVOKECOMMANDINFOEX**.</span></span> <span data-ttu-id="c2d96-137">Cela permet à votre application d’utiliser les informations Unicode contenues dans les cinq derniers membres de la structure.</span><span class="sxs-lookup"><span data-stu-id="c2d96-137">This enables your application to use the Unicode information that is contained in the last five members of the structure.</span></span>

<span data-ttu-id="c2d96-138">Le membre **lpVerb** ou **lpVerbW** de la structure est utilisé pour identifier la commande à exécuter.</span><span class="sxs-lookup"><span data-stu-id="c2d96-138">The structure's **lpVerb** or **lpVerbW** member is used to identify the command to be executed.</span></span> <span data-ttu-id="c2d96-139">Les commandes sont identifiées de l’une des deux manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="c2d96-139">Commands are identified in one of the following two ways:</span></span>

-   <span data-ttu-id="c2d96-140">Par la chaîne du verbe de la commande</span><span class="sxs-lookup"><span data-stu-id="c2d96-140">By the command's verb string</span></span>
-   <span data-ttu-id="c2d96-141">Par le décalage de l’identificateur de la commande</span><span class="sxs-lookup"><span data-stu-id="c2d96-141">By the command's identifier offset</span></span>

<span data-ttu-id="c2d96-142">Pour faire la distinction entre ces deux cas, vérifiez le mot de poids fort de **lpVerb** pour le cas ANSI ou **lpVerbW** pour la casse Unicode.</span><span class="sxs-lookup"><span data-stu-id="c2d96-142">To distinguish between these two cases, check the high-order word of **lpVerb** for the ANSI case or **lpVerbW** for the Unicode case.</span></span> <span data-ttu-id="c2d96-143">Si le mot de poids fort est différent de zéro, **lpVerb** ou **lpVerbW** contient une chaîne de verbe.</span><span class="sxs-lookup"><span data-stu-id="c2d96-143">If the high-order word is nonzero, **lpVerb** or **lpVerbW** holds a verb string.</span></span> <span data-ttu-id="c2d96-144">Si le mot de poids fort est égal à zéro, le décalage de la commande se trouve dans le mot de poids faible de **lpVerb**.</span><span class="sxs-lookup"><span data-stu-id="c2d96-144">If the high-order word is zero, the command offset is in the low-order word of **lpVerb**.</span></span>

<span data-ttu-id="c2d96-145">L’exemple suivant illustre une implémentation simple de [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) qui correspond aux exemples [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) et [**IContextMenu :: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) fournis avant et après cette section.</span><span class="sxs-lookup"><span data-stu-id="c2d96-145">The following example shows a simple implementation of [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) that corresponds to the [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) and [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) examples given before and after this section.</span></span> <span data-ttu-id="c2d96-146">La méthode détermine d’abord la structure qui est passée.</span><span class="sxs-lookup"><span data-stu-id="c2d96-146">The method first determines which structure is being passed in.</span></span> <span data-ttu-id="c2d96-147">Elle détermine ensuite si la commande est identifiée par son décalage ou son verbe.</span><span class="sxs-lookup"><span data-stu-id="c2d96-147">It then determines whether the command is identified by its offset or its verb.</span></span> <span data-ttu-id="c2d96-148">Si **lpVerb** ou **lpVerbW** contient un verbe ou un offset valide, la méthode affiche une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="c2d96-148">If **lpVerb** or **lpVerbW** holds a valid verb or offset, the method displays a message box.</span></span>


```
STDMETHODIMP CShellExtension::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    BOOL fEx = FALSE;
    BOOL fUnicode = FALSE;

    if(lpcmi->cbSize == sizeof(CMINVOKECOMMANDINFOEX))
    {
        fEx = TRUE;
        if((lpcmi->fMask & CMIC_MASK_UNICODE))
        {
            fUnicode = TRUE;
        }
    }

    if( !fUnicode && HIWORD(lpcmi->lpVerb))
    {
        if(StrCmpIA(lpcmi->lpVerb, m_pszVerb))
        {
            return E_FAIL;
        }
    }

    else if( fUnicode && HIWORD(((CMINVOKECOMMANDINFOEX *) lpcmi)->lpVerbW))
    {
        if(StrCmpIW(((CMINVOKECOMMANDINFOEX *)lpcmi)->lpVerbW, m_pwszVerb))
        {
            return E_FAIL;
        }
    }

    else if(LOWORD(lpcmi->lpVerb) != IDM_DISPLAY)
    {
        return E_FAIL;
    }

    else
    {
        MessageBox(lpcmi->hwnd,
                   "The File Name",
                   "File Name",
                   MB_OK|MB_ICONINFORMATION);
    }

    return S_OK;
}
```



### <a name="icontextmenuquerycontextmenu-method"></a><span data-ttu-id="c2d96-149">IContextMenu :: QueryContextMenu, méthode</span><span class="sxs-lookup"><span data-stu-id="c2d96-149">IContextMenu::QueryContextMenu Method</span></span>

<span data-ttu-id="c2d96-150">L’interpréteur de commandes appelle [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) pour permettre au gestionnaire de menu contextuel d’ajouter ses éléments de menu au menu.</span><span class="sxs-lookup"><span data-stu-id="c2d96-150">The Shell calls [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) to enable the shortcut menu handler to add its menu items to the menu.</span></span> <span data-ttu-id="c2d96-151">Il passe le handle **HMENU** dans le paramètre *HMENU* .</span><span class="sxs-lookup"><span data-stu-id="c2d96-151">It passes in the **HMENU** handle in the *hmenu* parameter.</span></span> <span data-ttu-id="c2d96-152">Le paramètre *indexMenu* est défini sur l’index à utiliser pour le premier élément de menu à ajouter.</span><span class="sxs-lookup"><span data-stu-id="c2d96-152">The *indexMenu* parameter is set to the index to be used for the first menu item that is to be added.</span></span>

<span data-ttu-id="c2d96-153">Tous les éléments de menu ajoutés par le gestionnaire doivent avoir des identificateurs qui se trouvent entre les valeurs des paramètres *idCmdFirst* et *idCmdLast* .</span><span class="sxs-lookup"><span data-stu-id="c2d96-153">Any menu items that are added by the handler must have identifiers that fall between the values in the *idCmdFirst* and *idCmdLast* parameters.</span></span> <span data-ttu-id="c2d96-154">En règle générale, le premier identificateur de commande est défini sur *idCmdFirst*, qui est incrémenté d’une unité (1) pour chaque commande supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="c2d96-154">Typically, the first command identifier is set to *idCmdFirst*, which is incremented by one (1) for each additional command.</span></span> <span data-ttu-id="c2d96-155">Cette pratique vous permet d’éviter de dépasser les *idCmdLast* et d’optimiser le nombre d’identificateurs disponibles au cas où l’interpréteur de commandes appellera plus d’un gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="c2d96-155">This practice helps you to avoid exceeding *idCmdLast* and maximizes the number of available identifiers in case the Shell calls more than one handler.</span></span>

<span data-ttu-id="c2d96-156">Le *décalage de commande* d’un identificateur d’élément correspond à la différence entre l’identificateur et la valeur dans *idCmdFirst*.</span><span class="sxs-lookup"><span data-stu-id="c2d96-156">An item identifier's *command offset* is the difference between the identifier and the value in *idCmdFirst*.</span></span> <span data-ttu-id="c2d96-157">Stockez le décalage de chaque élément que votre gestionnaire ajoute au menu contextuel, car l’interpréteur de commandes peut utiliser le décalage pour identifier l’élément s’il appelle ensuite [**IContextMenu :: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) ou [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span><span class="sxs-lookup"><span data-stu-id="c2d96-157">Store the offset of each item that your handler adds to the shortcut menu, because the Shell might use the offset to identify the item if it subsequently calls [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) or [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span>

<span data-ttu-id="c2d96-158">Vous devez également assigner un [verbe](launch.md) à chaque commande que vous ajoutez.</span><span class="sxs-lookup"><span data-stu-id="c2d96-158">You should also assign a [verb](launch.md) to each command that you add.</span></span> <span data-ttu-id="c2d96-159">Un verbe est une chaîne qui peut être utilisée à la place de l’offset pour identifier la commande lorsque [**commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) est appelé.</span><span class="sxs-lookup"><span data-stu-id="c2d96-159">A verb is a string that can be used instead of the offset to identify the command when [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) is called.</span></span> <span data-ttu-id="c2d96-160">Il est également utilisé par des fonctions telles que [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) pour exécuter des commandes de menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="c2d96-160">It is also used by functions such as [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to execute shortcut menu commands.</span></span>

<span data-ttu-id="c2d96-161">Il existe trois indicateurs qui peuvent être transmis via le paramètre *uFlags* qui sont pertinents pour les gestionnaires de menus contextuels.</span><span class="sxs-lookup"><span data-stu-id="c2d96-161">There are three flags that can be passed in through the *uFlags* parameter that are relevant to shortcut menu handlers.</span></span> <span data-ttu-id="c2d96-162">Ils sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c2d96-162">They are described in the following table.</span></span>



| <span data-ttu-id="c2d96-163">Indicateur</span><span class="sxs-lookup"><span data-stu-id="c2d96-163">Flag</span></span>             | <span data-ttu-id="c2d96-164">Description</span><span class="sxs-lookup"><span data-stu-id="c2d96-164">Description</span></span>                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2d96-165">CMF \_ DEFAULTONLY</span><span class="sxs-lookup"><span data-stu-id="c2d96-165">CMF\_DEFAULTONLY</span></span> | <span data-ttu-id="c2d96-166">L’utilisateur a sélectionné la commande par défaut, généralement en double-cliquant sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="c2d96-166">The user has selected the default command, usually by double-clicking the object.</span></span> <span data-ttu-id="c2d96-167">[**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) doit retourner le contrôle à l’interpréteur de commandes sans modifier le menu.</span><span class="sxs-lookup"><span data-stu-id="c2d96-167">[**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) should return control to the Shell without modifying the menu.</span></span> |
| <span data-ttu-id="c2d96-168">CMF \_ NOdéfaut</span><span class="sxs-lookup"><span data-stu-id="c2d96-168">CMF\_NODEFAULT</span></span>   | <span data-ttu-id="c2d96-169">Aucun élément dans le menu ne doit être l’élément par défaut.</span><span class="sxs-lookup"><span data-stu-id="c2d96-169">No item in the menu should be the default item.</span></span> <span data-ttu-id="c2d96-170">La méthode doit ajouter ses commandes au menu.</span><span class="sxs-lookup"><span data-stu-id="c2d96-170">The method should add its commands to the menu.</span></span>                                                                                                                          |
| <span data-ttu-id="c2d96-171">CMF \_ normal</span><span class="sxs-lookup"><span data-stu-id="c2d96-171">CMF\_NORMAL</span></span>      | <span data-ttu-id="c2d96-172">Le menu contextuel s’affiche normalement.</span><span class="sxs-lookup"><span data-stu-id="c2d96-172">The shortcut menu will be displayed normally.</span></span> <span data-ttu-id="c2d96-173">La méthode doit ajouter ses commandes au menu.</span><span class="sxs-lookup"><span data-stu-id="c2d96-173">The method should add its commands to the menu.</span></span>                                                                                                                            |



 

<span data-ttu-id="c2d96-174">Utilisez [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) ou [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) pour ajouter des éléments de menu à la liste.</span><span class="sxs-lookup"><span data-stu-id="c2d96-174">Use either [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) or [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) to add menu items to the list.</span></span> <span data-ttu-id="c2d96-175">Ensuite, retournez une valeur **HRESULT** avec la gravité définie sur gravité \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="c2d96-175">Then return an **HRESULT** value with the severity set to SEVERITY\_SUCCESS.</span></span> <span data-ttu-id="c2d96-176">Définissez la valeur de code sur le décalage de l’identificateur de commande le plus grand qui a été assigné, plus un (1).</span><span class="sxs-lookup"><span data-stu-id="c2d96-176">Set the code value to the offset of the largest command identifier that was assigned, plus one (1).</span></span> <span data-ttu-id="c2d96-177">Par exemple, supposons que *idCmdFirst* a la valeur 5 et que vous ajoutez trois éléments au menu avec des identificateurs de commande 5, 7 et 8.</span><span class="sxs-lookup"><span data-stu-id="c2d96-177">For example, assume that *idCmdFirst* is set to 5 and you add three items to the menu with command identifiers of 5, 7, and 8.</span></span> <span data-ttu-id="c2d96-178">La valeur de retour doit correspondre à \_ HRESULT (gravité \_ réussie, 0,8 + 1).</span><span class="sxs-lookup"><span data-stu-id="c2d96-178">The return value should be MAKE\_HRESULT(SEVERITY\_SUCCESS, 0, 8 + 1).</span></span>

<span data-ttu-id="c2d96-179">L’exemple suivant illustre une implémentation simple de [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) qui insère une seule commande.</span><span class="sxs-lookup"><span data-stu-id="c2d96-179">The following example shows a simple implementation of [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) that inserts a single command.</span></span> <span data-ttu-id="c2d96-180">Le décalage de l’identificateur de la commande est l' \_ affichage IDM, qui est défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="c2d96-180">The identifier offset for the command is IDM\_DISPLAY, which is set to zero.</span></span> <span data-ttu-id="c2d96-181">Les variables **m \_ pszVerb** et **m \_ pwszVerb** sont des variables privées utilisées pour stocker la chaîne de verbe indépendante du langage associée à la fois dans les formats ANSI et Unicode.</span><span class="sxs-lookup"><span data-stu-id="c2d96-181">The **m\_pszVerb** and **m\_pwszVerb** variables are private variables that are used to store the associated language-independent verb string in both ANSI and Unicode formats.</span></span>


```
#define IDM_DISPLAY 0

STDMETHODIMP CMenuExtension::QueryContextMenu(HMENU hMenu,
                                              UINT indexMenu,
                                              UINT idCmdFirst,
                                              UINT idCmdLast,
                                              UINT uFlags)
{
    HRESULT hr;
    
    if(!(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu(hMenu, 
                   indexMenu, 
                   MF_STRING | MF_BYPOSITION, 
                   idCmdFirst + IDM_DISPLAY, 
                   "&Display File Name");

    
        
        hr = StringCbCopyA(m_pszVerb, sizeof(m_pszVerb), "display");
        hr = StringCbCopyW(m_pwszVerb, sizeof(m_pwszVerb), L"display");

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_DISPLAY + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));}
```



## <a name="remarks"></a><span data-ttu-id="c2d96-182">Notes</span><span class="sxs-lookup"><span data-stu-id="c2d96-182">Remarks</span></span>

<span data-ttu-id="c2d96-183">Pour d’autres tâches d’implémentation de verbe, consultez [création de gestionnaires de menu contextuel](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="c2d96-183">For other verb implementation tasks, see [Creating Shortcut Menu Handlers](context-menu-handlers.md).</span></span>

 

 
