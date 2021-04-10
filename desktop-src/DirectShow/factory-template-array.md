---
description: Tableau de modèles de fabrique
ms.assetid: 310afccd-42a6-426e-b455-7bf98062bf36
title: Tableau de modèles de fabrique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645f2c8d05f37ab64142747755d6a0e7727f4b11
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109899"
---
# <a name="factory-template-array"></a><span data-ttu-id="08e00-103">Tableau de modèles de fabrique</span><span class="sxs-lookup"><span data-stu-id="08e00-103">Factory Template Array</span></span>

<span data-ttu-id="08e00-104">Le modèle Factory contient les variables membres publiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="08e00-104">The factory template contains the following public member variables:</span></span>

``` syntax
const WCHAR *              m_Name;                // Name
const CLSID *              m_ClsID;               // CLSID
LPFNNewCOMObject           m_lpfnNew;             // Function to create an instance
                                                  //   of the component
LPFNInitRoutine            m_lpfnInit;            // Initialization function (optional)
const AMOVIESETUP_FILTER * m_pAMovieSetup_Filter; // Set-up information (for filters)
```

<span data-ttu-id="08e00-105">Les deux pointeurs de fonction, [**m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md) et [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md), utilisent les définitions de type suivantes :</span><span class="sxs-lookup"><span data-stu-id="08e00-105">The two function pointers, [**m\_lpfnNew**](cfactorytemplate-m-lpfnnew.md) and [**m\_lpfnInit**](cfactorytemplate-m-lpfninit.md), use the following type definitions:</span></span>

``` syntax
typedef CUnknown *(CALLBACK *LPFNNewCOMObject)(LPUNKNOWN pUnkOuter, HRESULT *phr);
typedef void (CALLBACK *LPFNInitRoutine)(BOOL bLoading, const CLSID *rclsid);
```

<span data-ttu-id="08e00-106">La première est la fonction d’instanciation du composant.</span><span class="sxs-lookup"><span data-stu-id="08e00-106">The first is the instantiation function for the component.</span></span> <span data-ttu-id="08e00-107">La seconde est une fonction d’initialisation facultative.</span><span class="sxs-lookup"><span data-stu-id="08e00-107">The second is an optional initialization function.</span></span> <span data-ttu-id="08e00-108">Si vous fournissez une fonction d’initialisation, elle est appelée depuis l’intérieur de la fonction de point d’entrée DLL.</span><span class="sxs-lookup"><span data-stu-id="08e00-108">If you provide an initialization function, it is called from inside the DLL entry-point function.</span></span> <span data-ttu-id="08e00-109">(La fonction de point d’entrée DLL est présentée plus loin dans cet article.)</span><span class="sxs-lookup"><span data-stu-id="08e00-109">(The DLL entry-point function is discussed later in this article.)</span></span>

<span data-ttu-id="08e00-110">Supposons que vous créez une DLL qui contient un composant nommé CMyComponent, qui hérite de [**CUnknown**](cunknown.md).</span><span class="sxs-lookup"><span data-stu-id="08e00-110">Suppose you are creating a DLL that contains a component named CMyComponent, which inherits from [**CUnknown**](cunknown.md).</span></span> <span data-ttu-id="08e00-111">Vous devez fournir les éléments suivants dans votre DLL :</span><span class="sxs-lookup"><span data-stu-id="08e00-111">You must provide the following items in your DLL:</span></span>

-   <span data-ttu-id="08e00-112">La fonction d’initialisation, une méthode publique qui retourne une nouvelle instance de CMyComponent.</span><span class="sxs-lookup"><span data-stu-id="08e00-112">The initialization function, a public method that returns a new instance of CMyComponent.</span></span>
-   <span data-ttu-id="08e00-113">Tableau global de modèles de fabrique, appelés *\_ modèles g.*</span><span class="sxs-lookup"><span data-stu-id="08e00-113">A global array of factory templates, named *g\_Templates.*</span></span> <span data-ttu-id="08e00-114">Ce tableau contient le modèle de fabrique pour CMyComponent.</span><span class="sxs-lookup"><span data-stu-id="08e00-114">This array contains the factory template for CMyComponent.</span></span>
-   <span data-ttu-id="08e00-115">Une variable globale nommée *g \_ cTemplates* qui spécifie la taille du tableau.</span><span class="sxs-lookup"><span data-stu-id="08e00-115">A global variable named *g\_cTemplates* that specifies the size of the array.</span></span>

<span data-ttu-id="08e00-116">L’exemple suivant montre comment déclarer ces éléments :</span><span class="sxs-lookup"><span data-stu-id="08e00-116">The following example shows how to declare these items:</span></span>


```C++
// Public method that returns a new instance. 
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = new CMyComponent(NAME("My Component"), pUnk, pHr );
    if (pNewObject == NULL) {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 

CFactoryTemplate g_Templates[1] = 
{
    { 
      L"My Component",                // Name
      &CLSID_MyComponent,             // CLSID
      CMyComponent::CreateInstance,   // Method to create an instance of MyComponent
      NULL,                           // Initialization function
      NULL                            // Set-up information (for filters)
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);    
```



<span data-ttu-id="08e00-117">La `CreateInstance` méthode appelle le constructeur de classe et retourne un pointeur vers la nouvelle instance de classe.</span><span class="sxs-lookup"><span data-stu-id="08e00-117">The `CreateInstance` method calls the class constructor and returns a pointer to the new class instance.</span></span> <span data-ttu-id="08e00-118">Le paramètre *punk* est un pointeur vers l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="08e00-118">The parameter *pUnk* is a pointer to the aggregating [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="08e00-119">Vous pouvez simplement passer ce paramètre au constructeur de classe.</span><span class="sxs-lookup"><span data-stu-id="08e00-119">You can simply pass this parameter to the class constructor.</span></span> <span data-ttu-id="08e00-120">Le paramètre *pHr* est un pointeur vers une valeur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="08e00-120">The parameter *pHr* is a pointer to an HRESULT value.</span></span> <span data-ttu-id="08e00-121">Le constructeur de classe affecte à ce paramètre une valeur appropriée, mais si le constructeur échoue, définissez la valeur sur E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="08e00-121">The class constructor sets this to an appropriate value, but if the constructor fails, set the value to E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="08e00-122">La macro [**Name**](name.md) génère une chaîne dans les versions Debug, mais résout la **valeur null** dans les builds de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="08e00-122">The [**NAME**](name.md) macro generates a string in debug builds but resolves to **NULL** in retail builds.</span></span> <span data-ttu-id="08e00-123">Il est utilisé dans cet exemple pour attribuer au composant un nom qui apparaît dans les journaux de débogage, mais n’occupe pas la mémoire dans la version finale.</span><span class="sxs-lookup"><span data-stu-id="08e00-123">It is used in this example to give the component a name that appears in debug logs but does not occupy memory in the final version.</span></span>

<span data-ttu-id="08e00-124">La `CreateInstance` méthode peut avoir n’importe quel nom, car la fabrique de classe fait référence au pointeur de fonction dans le modèle de fabrique.</span><span class="sxs-lookup"><span data-stu-id="08e00-124">The `CreateInstance` method can have any name, because the class factory refers to the function pointer in the factory template.</span></span> <span data-ttu-id="08e00-125">Toutefois, *les \_ modèles g* et *g \_ cTemplates* sont des variables globales que la fabrique de classes s’attend à trouver. elles doivent donc avoir exactement ces noms.</span><span class="sxs-lookup"><span data-stu-id="08e00-125">However, *g\_Templates* and *g\_cTemplates* are global variables that the class factory expects to find, so they must have exactly those names.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08e00-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="08e00-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08e00-127">Comment créer une DLL de filtre DirectShow</span><span class="sxs-lookup"><span data-stu-id="08e00-127">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 
