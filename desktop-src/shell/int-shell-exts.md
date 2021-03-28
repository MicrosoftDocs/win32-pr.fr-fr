---
description: La majeure partie de l’implémentation d’un objet de gestionnaire d’extensions de Shell est dictée par son type. Toutefois, il existe des éléments communs. Cette rubrique décrit les aspects de l’implémentation qui sont partagés par tous les gestionnaires d’extensions de Shell.
ms.assetid: ce21ca0f-157c-4f69-bcf9-dc259c3bac80
title: Initialisation des gestionnaires d’extensions de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6a27b6273c5e342dc4caf545fb3593cdad66261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973762"
---
# <a name="initializing-shell-extension-handlers"></a><span data-ttu-id="dffb5-105">Initialisation des gestionnaires d’extensions de Shell</span><span class="sxs-lookup"><span data-stu-id="dffb5-105">Initializing Shell Extension Handlers</span></span>

<span data-ttu-id="dffb5-106">La majeure partie de l’implémentation d’un objet de gestionnaire d’extensions de Shell est dictée par son type.</span><span class="sxs-lookup"><span data-stu-id="dffb5-106">Much of the implementation of a Shell extension handler object is dictated by its type.</span></span> <span data-ttu-id="dffb5-107">Toutefois, il existe des éléments communs.</span><span class="sxs-lookup"><span data-stu-id="dffb5-107">There are, however, some common elements.</span></span> <span data-ttu-id="dffb5-108">Cette rubrique décrit les aspects de l’implémentation qui sont partagés par tous les gestionnaires d’extensions de Shell.</span><span class="sxs-lookup"><span data-stu-id="dffb5-108">This topic discusses those aspects of implementation that are shared by all Shell extension handlers.</span></span>

<span data-ttu-id="dffb5-109">Tous les gestionnaires d’extensions de Shell sont des objets COM (Component Object Model) in-process.</span><span class="sxs-lookup"><span data-stu-id="dffb5-109">All Shell extension handlers are in-process Component Object Model (COM) objects.</span></span> <span data-ttu-id="dffb5-110">Ils doivent recevoir un GUID et être inscrits comme décrit dans [inscription des gestionnaires d’extensions de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="dffb5-110">They must be assigned a GUID and registered as described in [Registering Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="dffb5-111">Elles sont implémentées en tant que dll et doivent exporter les fonctions standard suivantes :</span><span class="sxs-lookup"><span data-stu-id="dffb5-111">They are implemented as DLLs and must export the following standard functions:</span></span>

-   <span data-ttu-id="dffb5-112">[**DllMain**](../dlls/dllmain.md).</span><span class="sxs-lookup"><span data-stu-id="dffb5-112">[**DllMain**](../dlls/dllmain.md).</span></span> <span data-ttu-id="dffb5-113">Point d’entrée standard de la DLL.</span><span class="sxs-lookup"><span data-stu-id="dffb5-113">The standard entry point to the DLL.</span></span>
-   <span data-ttu-id="dffb5-114">[**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject).</span><span class="sxs-lookup"><span data-stu-id="dffb5-114">[**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject).</span></span> <span data-ttu-id="dffb5-115">Expose la fabrique de classe de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dffb5-115">Exposes the object's class factory.</span></span>
-   <span data-ttu-id="dffb5-116">[**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow).</span><span class="sxs-lookup"><span data-stu-id="dffb5-116">[**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow).</span></span> <span data-ttu-id="dffb5-117">COM appelle cette fonction pour déterminer si l’objet dessert des clients.</span><span class="sxs-lookup"><span data-stu-id="dffb5-117">COM calls this function to determine whether the object is serving any clients.</span></span> <span data-ttu-id="dffb5-118">Si ce n’est pas le cas, le système peut décharger la DLL et libérer la mémoire associée.</span><span class="sxs-lookup"><span data-stu-id="dffb5-118">If not, the system can unload the DLL and free the associated memory.</span></span>

<span data-ttu-id="dffb5-119">Comme tous les objets COM, les gestionnaires d’extensions de Shell doivent implémenter une interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) et une [fabrique de classe](../com/implementing-iclassfactory.md).</span><span class="sxs-lookup"><span data-stu-id="dffb5-119">Like all COM objects, Shell extension handlers must implement an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface and a [class factory](../com/implementing-iclassfactory.md).</span></span> <span data-ttu-id="dffb5-120">La plupart d’entre eux doivent également implémenter une interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) ou [**ISHELLEXTINIT**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) dans Windows XP ou une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="dffb5-120">Most must also implement either an [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) or [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface in Windows XP or earlier.</span></span> <span data-ttu-id="dffb5-121">Ils ont été remplacés par [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) et [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dffb5-121">These were replaced by [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) and [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) in Windows Vista.</span></span> <span data-ttu-id="dffb5-122">L’interpréteur de commandes utilise ces interfaces pour initialiser le gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="dffb5-122">The Shell uses these interfaces to initialize the handler.</span></span>

<span data-ttu-id="dffb5-123">L’interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) doit être implémentée par les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="dffb5-123">The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface must be implemented by the following:</span></span>

-   <span data-ttu-id="dffb5-124">Gestionnaires d’icônes</span><span class="sxs-lookup"><span data-stu-id="dffb5-124">Icon handlers</span></span>
-   <span data-ttu-id="dffb5-125">Gestionnaires de données</span><span class="sxs-lookup"><span data-stu-id="dffb5-125">Data handlers</span></span>
-   <span data-ttu-id="dffb5-126">Gestionnaires de suppression</span><span class="sxs-lookup"><span data-stu-id="dffb5-126">Drop handlers</span></span>

<span data-ttu-id="dffb5-127">L’interface [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) doit être implémentée par les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="dffb5-127">The [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface must be implemented by the following:</span></span>

-   <span data-ttu-id="dffb5-128">Gestionnaires de menus contextuels</span><span class="sxs-lookup"><span data-stu-id="dffb5-128">Shortcut menu handlers</span></span>
-   <span data-ttu-id="dffb5-129">Gestionnaires de glisser-déplacer</span><span class="sxs-lookup"><span data-stu-id="dffb5-129">Drag-and-drop handlers</span></span>
-   <span data-ttu-id="dffb5-130">Gestionnaires de feuille de propriétés</span><span class="sxs-lookup"><span data-stu-id="dffb5-130">Property sheet handlers</span></span>

<span data-ttu-id="dffb5-131">Les sujets suivants sont abordés dans le reste de cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="dffb5-131">The following subjects are discussed in the remainder of this topic:</span></span>

-   [<span data-ttu-id="dffb5-132">Implémentation de IPersistFile</span><span class="sxs-lookup"><span data-stu-id="dffb5-132">Implementing IPersistFile</span></span>](#implementing-ipersistfile)
-   [<span data-ttu-id="dffb5-133">Implémentation de IShellExtInit</span><span class="sxs-lookup"><span data-stu-id="dffb5-133">Implementing IShellExtInit</span></span>](#implementing-ishellextinit)
-   [<span data-ttu-id="dffb5-134">Personnalisation de l’info-bulle</span><span class="sxs-lookup"><span data-stu-id="dffb5-134">Infotip Customization</span></span>](#infotip-customization)
-   [<span data-ttu-id="dffb5-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dffb5-135">Related topics</span></span>](#related-topics)

## <a name="implementing-ipersistfile"></a><span data-ttu-id="dffb5-136">Implémentation de IPersistFile</span><span class="sxs-lookup"><span data-stu-id="dffb5-136">Implementing IPersistFile</span></span>

<span data-ttu-id="dffb5-137">L’interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) est conçue pour permettre le chargement d’un objet à partir de ou son enregistrement dans un fichier sur disque.</span><span class="sxs-lookup"><span data-stu-id="dffb5-137">The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is designed to permit an object to be loaded from or saved to a disk file.</span></span> <span data-ttu-id="dffb5-138">Il a six méthodes en plus de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), cinq propres et la méthode [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) qu’il hérite de l’interface [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist).</span><span class="sxs-lookup"><span data-stu-id="dffb5-138">It has six methods in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), five of its own, and the [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) method that it inherits from [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist).</span></span> <span data-ttu-id="dffb5-139">Avec les extensions de Shell, **IPersist** est utilisé uniquement pour initialiser un objet de gestionnaire d’extensions de Shell.</span><span class="sxs-lookup"><span data-stu-id="dffb5-139">With Shell extensions, **IPersist** is used only to initialize a Shell extension handler object.</span></span> <span data-ttu-id="dffb5-140">Étant donné qu’il n’est généralement pas nécessaire de lire ou d’écrire sur le disque, seules les méthodes **GetClassID** et [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) requièrent une implémentation sans jeton.</span><span class="sxs-lookup"><span data-stu-id="dffb5-140">Because there is typically no need to read from or write to the disk, only the **GetClassID** and [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) methods require a nontoken implementation.</span></span>

<span data-ttu-id="dffb5-141">L’interpréteur de commandes appelle d’abord [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) , et la fonction retourne l’identificateur de classe (CLSID) de l’objet de gestionnaire d’extensions.</span><span class="sxs-lookup"><span data-stu-id="dffb5-141">The Shell calls [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) first, and the function returns the class identifier (CLSID) of the extension handler object.</span></span> <span data-ttu-id="dffb5-142">L’interpréteur de commandes appelle ensuite la [**charge**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) et passe deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="dffb5-142">The Shell then calls [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) and passes in two values.</span></span> <span data-ttu-id="dffb5-143">La première, *pszFile*, est une chaîne Unicode avec le nom du fichier ou du dossier sur lequel l’interpréteur de commandes va fonctionner.</span><span class="sxs-lookup"><span data-stu-id="dffb5-143">The first, *pszFile*, is a Unicode string with the name of the file or folder that Shell is about to operate on.</span></span> <span data-ttu-id="dffb5-144">Le deuxième est *dwMode*, qui indique le mode d’accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="dffb5-144">The second is *dwMode*, which indicates the file access mode.</span></span> <span data-ttu-id="dffb5-145">Étant donné qu’il n’est normalement pas nécessaire d’accéder aux fichiers, *dwMode* est généralement égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="dffb5-145">Because there is normally no need to access files, *dwMode* is typically zero.</span></span> <span data-ttu-id="dffb5-146">La méthode stocke ces valeurs en fonction des besoins pour une référence ultérieure.</span><span class="sxs-lookup"><span data-stu-id="dffb5-146">The method stores these values as needed for later reference.</span></span>

<span data-ttu-id="dffb5-147">Le fragment de code suivant illustre la façon dont un gestionnaire d’extensions de Shell standard implémente les méthodes [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) et [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) .</span><span class="sxs-lookup"><span data-stu-id="dffb5-147">The following code fragment illustrates how a typical Shell extension handler implements the [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) and [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) methods.</span></span> <span data-ttu-id="dffb5-148">Il est conçu pour gérer ANSI ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="dffb5-148">It is designed to handle either ANSI or Unicode.</span></span> <span data-ttu-id="dffb5-149">CLSID \_ SampleExtHandler est le GUID de l’objet de gestionnaire d’extensions et CSampleShellExtension est le nom de la classe utilisée pour implémenter l’interface.</span><span class="sxs-lookup"><span data-stu-id="dffb5-149">CLSID\_SampleExtHandler is the extension handler object's GUID, and CSampleShellExtension is the name of the class used to implement the interface.</span></span> <span data-ttu-id="dffb5-150">Les variables **m \_ szFileName** et **m \_ dwMode** sont des variables privées utilisées pour stocker le nom et les indicateurs d’accès du fichier.</span><span class="sxs-lookup"><span data-stu-id="dffb5-150">The **m\_szFileName** and **m\_dwMode** variables are private variables that are used to store the file's name and access flags.</span></span>


```C++
class CSampleShellExtension : public IPersistFile
{
    // Method declarations not included

    private:
    WCHAR m_szFileName[MAX_PATH];    // The file name
    DWORD m_dwMode;                  // The file access mode
}

IFACEMETHODIMP CSampleShellExtension::GetClassID(__out CLSID *pCLSID)
{
    *pCLSID = CLSID_SampleExtHandler;
}

IFACEMETHODIMP CSampleShellExtension::Load(PCWSTR pszFile, DWORD dwMode)
{
    m_dwMode = dwMode;
    return StringCchCopy(m_szFileName, ARRAYSIZE(m_szFileName), pszFile); 
}

// The implementation sample is continued in the next section.
```



## <a name="implementing-ishellextinit"></a><span data-ttu-id="dffb5-151">Implémentation de IShellExtInit</span><span class="sxs-lookup"><span data-stu-id="dffb5-151">Implementing IShellExtInit</span></span>

<span data-ttu-id="dffb5-152">L’interface [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) n’a qu’une seule méthode, [**IShellExtInit :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), en plus de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="dffb5-152">The [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface has only one method, [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="dffb5-153">La méthode a trois paramètres que l’interpréteur de commandes peut utiliser pour passer divers types d’informations.</span><span class="sxs-lookup"><span data-stu-id="dffb5-153">The method has three parameters that the Shell can use to pass in various types of information.</span></span> <span data-ttu-id="dffb5-154">Les valeurs transmises dépendent du type de gestionnaire, tandis que d’autres peuvent avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="dffb5-154">The values passed in depend on the type of handler, and some can be set to **NULL**.</span></span>

-   <span data-ttu-id="dffb5-155">*pidlFolder* contient le pointeur d’un dossier vers une liste d’identificateurs d’éléments (PIDL).</span><span class="sxs-lookup"><span data-stu-id="dffb5-155">*pidlFolder* holds a folder's pointer to an item identifier list (PIDL).</span></span> <span data-ttu-id="dffb5-156">Il s’agit d’un PIDL absolu.</span><span class="sxs-lookup"><span data-stu-id="dffb5-156">This is an absolute PIDL.</span></span> <span data-ttu-id="dffb5-157">Pour les extensions de feuille de propriétés, cette valeur est **null**.</span><span class="sxs-lookup"><span data-stu-id="dffb5-157">For property sheet extensions, this value is **NULL**.</span></span> <span data-ttu-id="dffb5-158">Pour les extensions de menu contextuel, il s’agit de l’PIDL du dossier qui contient l’élément dont le menu contextuel est affiché.</span><span class="sxs-lookup"><span data-stu-id="dffb5-158">For shortcut menu extensions, it is the PIDL of the folder that contains the item whose shortcut menu is being displayed.</span></span> <span data-ttu-id="dffb5-159">Pour les gestionnaires de glisser-déplacer non par défaut, il s’agit de l’PIDL du dossier cible.</span><span class="sxs-lookup"><span data-stu-id="dffb5-159">For nondefault drag-and-drop handlers, it is the PIDL of the target folder.</span></span>
-   <span data-ttu-id="dffb5-160">*pDataObject* contient un pointeur vers l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) d’un objet de données.</span><span class="sxs-lookup"><span data-stu-id="dffb5-160">*pDataObject* holds a pointer to a data object's [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) interface.</span></span> <span data-ttu-id="dffb5-161">L’objet de données contient un ou plusieurs noms de fichiers au format [CF \_ HDROP](dragdrop.md) .</span><span class="sxs-lookup"><span data-stu-id="dffb5-161">The data object holds one or more file names in [CF\_HDROP](dragdrop.md) format.</span></span>
-   <span data-ttu-id="dffb5-162">*hRegKey* contient une clé de Registre pour l’objet de fichier ou le type de dossier.</span><span class="sxs-lookup"><span data-stu-id="dffb5-162">*hRegKey* holds a registry key for the file object or folder type.</span></span>

<span data-ttu-id="dffb5-163">La méthode [**IShellExtInit :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) stocke le nom de fichier, le pointeur [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) et la clé de Registre nécessaires pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="dffb5-163">The [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method stores the file name, [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer, and registry key as needed for later use.</span></span> <span data-ttu-id="dffb5-164">Le fragment de code suivant illustre une implémentation de **IShellExtInit :: Initialize**.</span><span class="sxs-lookup"><span data-stu-id="dffb5-164">The following code fragment illustrates an implementation of **IShellExtInit::Initialize**.</span></span> <span data-ttu-id="dffb5-165">Pour plus de simplicité, cet exemple suppose que l’objet de données ne contient qu’un seul fichier.</span><span class="sxs-lookup"><span data-stu-id="dffb5-165">For simplicity, this example assumes that the data object contains only a single file.</span></span> <span data-ttu-id="dffb5-166">En général, l’objet de données peut contenir plusieurs fichiers, chacun d’entre eux devant être extrait.</span><span class="sxs-lookup"><span data-stu-id="dffb5-166">In general, the data object might contain multiple files, each of which will need to be extracted.</span></span>


```C++
// This code continues the CSampleShellExtension sample shown in the
// "Implementing IPersistFile" section above.

class CSampleShellExtension : public IShellExtInit
{
    // Method declarations not included
    
    private:
    // IDList of the folder for extensions invoked on the folder, such as 
    // background context menu handlers or nondefault drag-and-drop handlers. 
    PIDLIST_ABSOLUTE m_pidlFolder;
    
    // The data object contains an expression of the items that the handler is 
    // being initialized for. Use SHCreateShellItemArrayFromDataObject to 
    // convert this object to an array of items. Use SHGetItemFromObject if you
    // are only interested in a single Shell item. If you need a file system
    // path, use IShellItem::GetDisplayName(SIGDN_FILESYSPATH, ...).
    IDataObject *m_pdtobj;
    
    // For context menu handlers, the registry key provides access to verb 
    // instance data that might be stored there. This is a rare feature to use 
    // so most extensions do not need this variable.
    HKEY m_hRegKey;             
}
    
// This method must be very efficient. Do not do any unnecessary work here.
// Use Initialize to acquire resources that will be used later.

IFACEMETHODIMP CSampleShellExtension::Initialize(__in_opt PCIDLIST_ABSOLUTE pidlFolder,
                                                 __in_opt IDataObject *pDataObject, 
                                                 __in_opt HKEY hRegKey) 
{ 
    // In some cases, handlers are initialized multiple times. Therefore, 
    // clear any previous state here.
    CoTaskMemFree(m_pidlFolder);
    m_pidlFolder = NULL;
    
    if (m_pdtobj)
    { 
        m_pdtobj->Release(); 
    }
    
    if (m_hRegKey)
    {
        RegCloseKey(m_hRegKey);
        m_hRegKey = NULL;
    }
    
    // Capture the inputs for use later.
    HRESULT hr = S_OK;
    
    if (pidlFolder)
    {
        m_pidlFolder = ILClone(pidlFolder);   // Make a copy to use later.
        hr = m_pidlFolder ? S_OK : E_OUTOFMEMORY;
    }
    
    if (SUCCEEDED(hr))
    {
        // If a data object pointer was passed into the method, save it and
        // extract the file name. 
        if (pDataObject) 
        { 
            m_pdtobj = pDataObject; 
            m_pdtobj->AddRef(); 
        }
    
        // It is uncommon to use the registry handle, but if you need it,
        // duplicate it now.
        if (hRegKey)
        {
            LSTATUS const result = RegOpenKeyEx(hRegKey, NULL, 0, KEY_READ, &m_hRegKey); 
            hr = HRESULT_FROM_WIN32(result);
        }
    }
    
    return hr;
}
```



## <a name="infotip-customization"></a><span data-ttu-id="dffb5-167">Personnalisation de l’info-bulle</span><span class="sxs-lookup"><span data-stu-id="dffb5-167">Infotip Customization</span></span>

<span data-ttu-id="dffb5-168">Il existe deux façons de personnaliser info-bulles.</span><span class="sxs-lookup"><span data-stu-id="dffb5-168">There are two ways to customize infotips.</span></span> <span data-ttu-id="dffb5-169">L’une des méthodes consiste à implémenter un objet qui prend en charge [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) , puis à inscrire l’objet sous la sous-clé appropriée dans le registre (voir ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="dffb5-169">One way is to implement an object that supports [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) and then register the object under the proper subkey in the registry (see below).</span></span> <span data-ttu-id="dffb5-170">Vous pouvez également spécifier une chaîne fixe ou une liste de certaines propriétés de fichier à afficher.</span><span class="sxs-lookup"><span data-stu-id="dffb5-170">Alternatively, you can specify either a fixed string or a list of certain file properties to be displayed.</span></span>

<span data-ttu-id="dffb5-171">Pour afficher une chaîne fixe pour une extension d’espace de noms, créez une sous-clé appelée **info-bulle** sous la clé CLSID de votre extension d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="dffb5-171">To display a fixed string for a namespace extension, create a subkey called **InfoTip** beneath the CLSID key of your namespace extension.</span></span> <span data-ttu-id="dffb5-172">Définissez les données de cette sous-clé pour qu’elles soient la chaîne que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="dffb5-172">Set the data of that subkey to be the string you want to be displayed.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

<span data-ttu-id="dffb5-173">Pour afficher une chaîne fixe pour un type de fichier, créez une sous-clé appelée **info-bulle** sous la clé **ProgID** du type de fichier pour lequel vous souhaitez fournir des info-bulles.</span><span class="sxs-lookup"><span data-stu-id="dffb5-173">To display a fixed string for a file type, create a subkey called **InfoTip** beneath the **ProgID** key of the file type for which you want to supply infotips.</span></span> <span data-ttu-id="dffb5-174">Définissez les données de cette sous-clé pour qu’elles soient la chaîne que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="dffb5-174">Set the data of that subkey to be the string you want to be displayed.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = InfoTip string for all files of this type
```

<span data-ttu-id="dffb5-175">Si vous souhaitez que l’interpréteur de commandes affiche certaines propriétés de fichier dans l’info-bulle pour un type de fichier spécifique, créez une sous-clé appelée **info-bulle** sous la clé **ProgID** de ce type de fichier.</span><span class="sxs-lookup"><span data-stu-id="dffb5-175">If you want the Shell to show certain file properties in the infotip for a specific file type, create a subkey called **InfoTip** beneath the **ProgID** key of that file type.</span></span> <span data-ttu-id="dffb5-176">Définissez les données de cette sous-clé comme une liste délimitée par des points-virgules de noms de propriété canoniques ou {fmtid}, paires PID où *propName* est un nom de propriété canonique et *{fmtid}, PID* est une [**paire fmtid/PID**](./objects.md).</span><span class="sxs-lookup"><span data-stu-id="dffb5-176">Set the data of that subkey to be a semicolon-delineated list of canonical property names or {fmtid}, pid pairs where *propname* is a canonical property name and *{fmtid},pid* is a [**FMTID/PID pair**](./objects.md).</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = propname;propname;{fmtid},pid;{fmtid},pid
```

<span data-ttu-id="dffb5-177">Les noms de propriétés suivants peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="dffb5-177">The following property names can be used.</span></span>



| <span data-ttu-id="dffb5-178">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="dffb5-178">Property Name</span></span>    | <span data-ttu-id="dffb5-179">Description</span><span class="sxs-lookup"><span data-stu-id="dffb5-179">Description</span></span>                   | <span data-ttu-id="dffb5-180">Récupéré à partir de</span><span class="sxs-lookup"><span data-stu-id="dffb5-180">Retrieved From</span></span>                                                                            |
|------------------|-------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="dffb5-181">Auteur</span><span class="sxs-lookup"><span data-stu-id="dffb5-181">Author</span></span>           | <span data-ttu-id="dffb5-182">Auteur du document</span><span class="sxs-lookup"><span data-stu-id="dffb5-182">Author of the document</span></span>        | [<span data-ttu-id="dffb5-183">**\_auteur PIDSI**</span><span class="sxs-lookup"><span data-stu-id="dffb5-183">**PIDSI\_AUTHOR**</span></span>](../stg/the-summary-information-property-set.md)                             |
| <span data-ttu-id="dffb5-184">Intitulé</span><span class="sxs-lookup"><span data-stu-id="dffb5-184">Title</span></span>            | <span data-ttu-id="dffb5-185">Titre du document</span><span class="sxs-lookup"><span data-stu-id="dffb5-185">Title of the document</span></span>         | [<span data-ttu-id="dffb5-186">**\_titre PIDSI**</span><span class="sxs-lookup"><span data-stu-id="dffb5-186">**PIDSI\_TITLE**</span></span>](../stg/the-summary-information-property-set.md)                              |
| <span data-ttu-id="dffb5-187">Objet</span><span class="sxs-lookup"><span data-stu-id="dffb5-187">Subject</span></span>          | <span data-ttu-id="dffb5-188">Résumé de l’objet</span><span class="sxs-lookup"><span data-stu-id="dffb5-188">Subject summary</span></span>               | [<span data-ttu-id="dffb5-189">**PIDSI \_ objet**</span><span class="sxs-lookup"><span data-stu-id="dffb5-189">**PIDSI\_SUBJECT**</span></span>](../stg/the-summary-information-property-set.md)                            |
| <span data-ttu-id="dffb5-190">Commentaire</span><span class="sxs-lookup"><span data-stu-id="dffb5-190">Comment</span></span>          | <span data-ttu-id="dffb5-191">Commentaires sur le document</span><span class="sxs-lookup"><span data-stu-id="dffb5-191">Document comments</span></span>             | <span data-ttu-id="dffb5-192">[**PIDSI \_**](../stg/the-summary-information-property-set.md) Propriétés d’un commentaire ou d’un dossier/lecteur</span><span class="sxs-lookup"><span data-stu-id="dffb5-192">[**PIDSI\_COMMENT**](../stg/the-summary-information-property-set.md) or folder/drive properties</span></span> |
| <span data-ttu-id="dffb5-193">PageCount</span><span class="sxs-lookup"><span data-stu-id="dffb5-193">PageCount</span></span>        | <span data-ttu-id="dffb5-194">Nombre de pages</span><span class="sxs-lookup"><span data-stu-id="dffb5-194">Number of pages</span></span>               | [<span data-ttu-id="dffb5-195">**PIDSI \_ PageCount**</span><span class="sxs-lookup"><span data-stu-id="dffb5-195">**PIDSI\_PAGECOUNT**</span></span>](../stg/the-summary-information-property-set.md)                          |
| <span data-ttu-id="dffb5-196">Nom</span><span class="sxs-lookup"><span data-stu-id="dffb5-196">Name</span></span>             | <span data-ttu-id="dffb5-197">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="dffb5-197">Friendly name</span></span>                 | <span data-ttu-id="dffb5-198">Affichage des dossiers standard</span><span class="sxs-lookup"><span data-stu-id="dffb5-198">Standard folder view</span></span>                                                                      |
| <span data-ttu-id="dffb5-199">OriginalLocation</span><span class="sxs-lookup"><span data-stu-id="dffb5-199">OriginalLocation</span></span> | <span data-ttu-id="dffb5-200">Emplacement du fichier d’origine</span><span class="sxs-lookup"><span data-stu-id="dffb5-200">Location of original file</span></span>     | <span data-ttu-id="dffb5-201">Dossier porte-documents et dossier Corbeille</span><span class="sxs-lookup"><span data-stu-id="dffb5-201">Briefcase folder and Recycle Bin folder</span></span>                                                   |
| <span data-ttu-id="dffb5-202">DateDeleted</span><span class="sxs-lookup"><span data-stu-id="dffb5-202">DateDeleted</span></span>      | <span data-ttu-id="dffb5-203">Date de suppression du fichier</span><span class="sxs-lookup"><span data-stu-id="dffb5-203">Date file was deleted</span></span>         | <span data-ttu-id="dffb5-204">Dossier Corbeille</span><span class="sxs-lookup"><span data-stu-id="dffb5-204">Recycle Bin folder</span></span>                                                                        |
| <span data-ttu-id="dffb5-205">Type</span><span class="sxs-lookup"><span data-stu-id="dffb5-205">Type</span></span>             | <span data-ttu-id="dffb5-206">Type de fichier</span><span class="sxs-lookup"><span data-stu-id="dffb5-206">Type of file</span></span>                  | <span data-ttu-id="dffb5-207">Mode Détails du dossier standard</span><span class="sxs-lookup"><span data-stu-id="dffb5-207">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="dffb5-208">Taille</span><span class="sxs-lookup"><span data-stu-id="dffb5-208">Size</span></span>             | <span data-ttu-id="dffb5-209">Taille du fichier</span><span class="sxs-lookup"><span data-stu-id="dffb5-209">Size of file</span></span>                  | <span data-ttu-id="dffb5-210">Mode Détails du dossier standard</span><span class="sxs-lookup"><span data-stu-id="dffb5-210">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="dffb5-211">SyncCopyIn</span><span class="sxs-lookup"><span data-stu-id="dffb5-211">SyncCopyIn</span></span>       | <span data-ttu-id="dffb5-212">Identique à OriginalLocation</span><span class="sxs-lookup"><span data-stu-id="dffb5-212">Same as OriginalLocation</span></span>      | <span data-ttu-id="dffb5-213">Identique à OriginalLocation</span><span class="sxs-lookup"><span data-stu-id="dffb5-213">Same as OriginalLocation</span></span>                                                                  |
| <span data-ttu-id="dffb5-214">Modifié le</span><span class="sxs-lookup"><span data-stu-id="dffb5-214">Modified</span></span>         | <span data-ttu-id="dffb5-215">Date de dernière modification</span><span class="sxs-lookup"><span data-stu-id="dffb5-215">Date last modified</span></span>            | <span data-ttu-id="dffb5-216">Mode Détails du dossier standard</span><span class="sxs-lookup"><span data-stu-id="dffb5-216">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="dffb5-217">Date de création</span><span class="sxs-lookup"><span data-stu-id="dffb5-217">Created</span></span>          | <span data-ttu-id="dffb5-218">Date de création</span><span class="sxs-lookup"><span data-stu-id="dffb5-218">Date created</span></span>                  | <span data-ttu-id="dffb5-219">Mode Détails du dossier standard</span><span class="sxs-lookup"><span data-stu-id="dffb5-219">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="dffb5-220">Atteint</span><span class="sxs-lookup"><span data-stu-id="dffb5-220">Accessed</span></span>         | <span data-ttu-id="dffb5-221">Date du dernier accès</span><span class="sxs-lookup"><span data-stu-id="dffb5-221">Date last accessed</span></span>            | <span data-ttu-id="dffb5-222">Mode Détails du dossier standard</span><span class="sxs-lookup"><span data-stu-id="dffb5-222">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="dffb5-223">Indossier</span><span class="sxs-lookup"><span data-stu-id="dffb5-223">InFolder</span></span>         | <span data-ttu-id="dffb5-224">Répertoire contenant le fichier</span><span class="sxs-lookup"><span data-stu-id="dffb5-224">Directory containing the file</span></span> | <span data-ttu-id="dffb5-225">Résultats de la recherche de documents</span><span class="sxs-lookup"><span data-stu-id="dffb5-225">Document search results</span></span>                                                                   |
| <span data-ttu-id="dffb5-226">Rank</span><span class="sxs-lookup"><span data-stu-id="dffb5-226">Rank</span></span>             | <span data-ttu-id="dffb5-227">Qualité de la recherche de correspondance</span><span class="sxs-lookup"><span data-stu-id="dffb5-227">Quality of search match</span></span>       | <span data-ttu-id="dffb5-228">Résultats de la recherche de documents</span><span class="sxs-lookup"><span data-stu-id="dffb5-228">Document search results</span></span>                                                                   |
| <span data-ttu-id="dffb5-229">FreeSpace</span><span class="sxs-lookup"><span data-stu-id="dffb5-229">FreeSpace</span></span>        | <span data-ttu-id="dffb5-230">Espace de stockage disponible</span><span class="sxs-lookup"><span data-stu-id="dffb5-230">Available storage space</span></span>       | <span data-ttu-id="dffb5-231">Lecteurs de disque</span><span class="sxs-lookup"><span data-stu-id="dffb5-231">Disk drives</span></span>                                                                               |
| <span data-ttu-id="dffb5-232">NumberOfVisits</span><span class="sxs-lookup"><span data-stu-id="dffb5-232">NumberOfVisits</span></span>   | <span data-ttu-id="dffb5-233">Nombre de visites</span><span class="sxs-lookup"><span data-stu-id="dffb5-233">Number of visits</span></span>              | <span data-ttu-id="dffb5-234">Dossier Favoris</span><span class="sxs-lookup"><span data-stu-id="dffb5-234">Favorites folder</span></span>                                                                          |
| <span data-ttu-id="dffb5-235">Attributs</span><span class="sxs-lookup"><span data-stu-id="dffb5-235">Attributes</span></span>       | <span data-ttu-id="dffb5-236">Attributs de fichier</span><span class="sxs-lookup"><span data-stu-id="dffb5-236">File Attributes</span></span>               | <span data-ttu-id="dffb5-237">Mode Détails du dossier standard</span><span class="sxs-lookup"><span data-stu-id="dffb5-237">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="dffb5-238">Company</span><span class="sxs-lookup"><span data-stu-id="dffb5-238">Company</span></span>          | <span data-ttu-id="dffb5-239">Nom de la société</span><span class="sxs-lookup"><span data-stu-id="dffb5-239">Company name</span></span>                  | [<span data-ttu-id="dffb5-240">**\_entreprise PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="dffb5-240">**PIDDSI\_COMPANY**</span></span>](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| <span data-ttu-id="dffb5-241">Category</span><span class="sxs-lookup"><span data-stu-id="dffb5-241">Category</span></span>         | <span data-ttu-id="dffb5-242">Catégorie de document</span><span class="sxs-lookup"><span data-stu-id="dffb5-242">Document category</span></span>             | [<span data-ttu-id="dffb5-243">**\_catégorie PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="dffb5-243">**PIDDSI\_CATEGORY**</span></span>](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| <span data-ttu-id="dffb5-244">copyright</span><span class="sxs-lookup"><span data-stu-id="dffb5-244">Copyright</span></span>        | <span data-ttu-id="dffb5-245">Copyright du support</span><span class="sxs-lookup"><span data-stu-id="dffb5-245">Media copyright</span></span>               | [<span data-ttu-id="dffb5-246">**\_Copyright PIDMSI**</span><span class="sxs-lookup"><span data-stu-id="dffb5-246">**PIDMSI\_COPYRIGHT**</span></span>](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md) |
| <span data-ttu-id="dffb5-247">HTMLInfoTipFile</span><span class="sxs-lookup"><span data-stu-id="dffb5-247">HTMLInfoTipFile</span></span>  | <span data-ttu-id="dffb5-248">Fichier info-bulle HTML</span><span class="sxs-lookup"><span data-stu-id="dffb5-248">HTML InfoTip file</span></span>             | <span data-ttu-id="dffb5-249">Fichier Desktop.ini pour le dossier</span><span class="sxs-lookup"><span data-stu-id="dffb5-249">Desktop.ini file for folder</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="dffb5-250">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dffb5-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dffb5-251">Inscription des gestionnaires d’extensions de Shell</span><span class="sxs-lookup"><span data-stu-id="dffb5-251">Registering Shell Extension Handlers</span></span>](reg-shell-exts.md)
</dt> </dl>

 

 
