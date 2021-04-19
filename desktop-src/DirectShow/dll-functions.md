---
description: Cette rubrique explique comment implémenter un composant en tant que bibliothèque de liens dynamiques (DLL) dans Microsoft DirectShow.
ms.assetid: cb935c26-2dc9-4ab3-810d-b63f1018a62a
title: Fonctions DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b6d1b15df86cf3d7a2eb81080ec02b02a868f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106544537"
---
# <a name="dll-functions"></a><span data-ttu-id="3b3ee-103">Fonctions DLL</span><span class="sxs-lookup"><span data-stu-id="3b3ee-103">DLL Functions</span></span>

<span data-ttu-id="3b3ee-104">Cette rubrique explique comment implémenter un composant en tant que bibliothèque de liens dynamiques (DLL) dans Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3b3ee-104">This topic describes how to implement a component as a dynamic-link library (DLL) in Microsoft DirectShow.</span></span>

<span data-ttu-id="3b3ee-105">Une DLL doit implémenter les fonctions suivantes pour qu’elle puisse être inscrite, désinscrite et chargée en mémoire.</span><span class="sxs-lookup"><span data-stu-id="3b3ee-105">A DLL must implement the following functions so that it can be registered, unregistered, and loaded into memory.</span></span>

-   <span data-ttu-id="3b3ee-106">[*DllMain*](/windows/desktop/Dlls/dllmain): point d’entrée de la dll.</span><span class="sxs-lookup"><span data-stu-id="3b3ee-106">[*DllMain*](/windows/desktop/Dlls/dllmain): The DLL entry point.</span></span> <span data-ttu-id="3b3ee-107">Le nom *DllMain* est un espace réservé pour le nom de la fonction définie par la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="3b3ee-107">The name *DllMain* is a placeholder for the library-defined function name.</span></span> <span data-ttu-id="3b3ee-108">L’implémentation DirectShow utilise le nom **DllEntryPoint**.</span><span class="sxs-lookup"><span data-stu-id="3b3ee-108">The DirectShow implementation uses the name **DllEntryPoint**.</span></span> <span data-ttu-id="3b3ee-109">Pour plus d’informations, consultez le kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="3b3ee-109">For more information, see the Platform SDK.</span></span>
-   <span data-ttu-id="3b3ee-110">[**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject): crée une instance de fabrique de classe.</span><span class="sxs-lookup"><span data-stu-id="3b3ee-110">[**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject): Creates a class factory instance.</span></span> <span data-ttu-id="3b3ee-111">Décrit dans les sections précédentes.</span><span class="sxs-lookup"><span data-stu-id="3b3ee-111">Described in the previous sections.</span></span>
-   <span data-ttu-id="3b3ee-112">[**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow): interroge si la dll peut être déchargée en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="3b3ee-112">[**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow): Queries whether the DLL can safely be unloaded.</span></span>
-   <span data-ttu-id="3b3ee-113">[**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver): crée des entrées de Registre pour la dll.</span><span class="sxs-lookup"><span data-stu-id="3b3ee-113">[**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver): Creates registry entries for the DLL.</span></span>
-   <span data-ttu-id="3b3ee-114">[**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver): supprime les entrées de Registre pour la dll.</span><span class="sxs-lookup"><span data-stu-id="3b3ee-114">[**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver): Removes registry entries for the DLL.</span></span>

<span data-ttu-id="3b3ee-115">Parmi celles-ci, les trois premières sont implémentées par DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3b3ee-115">Of these, the first three are implemented by DirectShow.</span></span> <span data-ttu-id="3b3ee-116">Si votre modèle de fabrique fournit une fonction d’initialisation dans la variable membre [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md) , cette fonction est appelée depuis l’intérieur de la fonction de point d’entrée de la dll.</span><span class="sxs-lookup"><span data-stu-id="3b3ee-116">If your factory template provides an initialization function in the [**m\_lpfnInit**](cfactorytemplate-m-lpfninit.md) member variable, that function is called from inside the DLL entry-point function.</span></span> <span data-ttu-id="3b3ee-117">Pour plus d’informations sur le moment où le système appelle la fonction de point d’entrée DLL, consultez [*DllMain*](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="3b3ee-117">For more information on when the system calls the DLL entry-point function, see [*DllMain*](/windows/desktop/Dlls/dllmain).</span></span>

<span data-ttu-id="3b3ee-118">Vous devez implémenter [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) et [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver), mais DirectShow fournit une fonction nommée [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) qui effectue les tâches nécessaires.</span><span class="sxs-lookup"><span data-stu-id="3b3ee-118">You must implement [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver), but DirectShow provides a function named [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) that does the necessary work.</span></span> <span data-ttu-id="3b3ee-119">Votre composant peut simplement encapsuler cette fonction, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="3b3ee-119">Your component can simply wrap this function, as shown in the following example:</span></span>


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}

STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



<span data-ttu-id="3b3ee-120">Toutefois, dans [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) et [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) , vous pouvez personnaliser le processus d’inscription en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="3b3ee-120">However, within [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) you can customize the registration process as needed.</span></span> <span data-ttu-id="3b3ee-121">Si votre DLL contient un filtre, vous devrez peut-être effectuer des tâches supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="3b3ee-121">If your DLL contains a filter, you might need to do some additional work.</span></span> <span data-ttu-id="3b3ee-122">Pour plus d’informations, consultez [comment inscrire des filtres DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="3b3ee-122">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

<span data-ttu-id="3b3ee-123">Dans votre fichier de définition de module (. def), exportez toutes les fonctions DLL à l’exception de la fonction de point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3b3ee-123">In your module-definition (.def) file, export all the DLL functions except for the entry-point function.</span></span> <span data-ttu-id="3b3ee-124">Voici un exemple de fichier. def :</span><span class="sxs-lookup"><span data-stu-id="3b3ee-124">The following is an example .def file:</span></span>


```C++
EXPORTS
    DllGetClassObject PRIVATE
    DllCanUnloadNow PRIVATE
    DllRegisterServer PRIVATE
    DllUnregisterServer PRIVATE
```



<span data-ttu-id="3b3ee-125">Vous pouvez inscrire la DLL à l’aide de l’utilitaire Regsvr32.exe.</span><span class="sxs-lookup"><span data-stu-id="3b3ee-125">You can register the DLL using the Regsvr32.exe utility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b3ee-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3b3ee-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b3ee-127">Comment créer une DLL de filtre DirectShow</span><span class="sxs-lookup"><span data-stu-id="3b3ee-127">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 
