---
description: Décrit comment initialiser un modèle d’objet XPS, qui permet à un programme de créer un document XPS.
ms.assetid: 920d940f-5ae2-4376-8c7b-0cef04f21df7
title: Initialiser un modèle d’objet XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cac44a69d171c1d38633512b0e275dcdeaea8738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318909"
---
# <a name="initialize-an-xps-om"></a><span data-ttu-id="6a784-103">Initialiser un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="6a784-103">Initialize an XPS OM</span></span>

<span data-ttu-id="6a784-104">Décrit comment initialiser un modèle d’objet XPS, qui permet à un programme de créer un document XPS.</span><span class="sxs-lookup"><span data-stu-id="6a784-104">Describes how to initialize an XPS OM, which allows a program to create an XPS document.</span></span>

<span data-ttu-id="6a784-105">Les interfaces de l’API de document XPS sont créées par une interface [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) .</span><span class="sxs-lookup"><span data-stu-id="6a784-105">The interfaces of the XPS Document API are created by an [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) interface.</span></span> <span data-ttu-id="6a784-106">Pour obtenir un pointeur vers un **IXpsOMObjectFactory** qui peut être utilisé dans votre programme, appelez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="6a784-106">To obtain a pointer to an **IXpsOMObjectFactory** that can be used in your program, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="6a784-107">Avant d’utiliser les exemples de code suivants dans votre programme, lisez l’exclusion de responsabilité dans les [tâches de programmation de document XPS courantes](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="6a784-107">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="6a784-108">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="6a784-108">Code Example</span></span>

<span data-ttu-id="6a784-109">L’exemple suivant crée la fabrique d’objet qui sera utilisée pour créer des interfaces OM XPS dans d’autres exemples.</span><span class="sxs-lookup"><span data-stu-id="6a784-109">The following example creates the object factory that will be used to create XPS OM interfaces in other examples.</span></span>


```C++
    IXpsOMObjectFactory *xpsFactory;

    HRESULT hr = S_OK;

    // Init COM for this thread if it hasn't 
    //  been initialized, yet.
    hr = CoInitializeEx(0, COINIT_MULTITHREADED);

    hr = CoCreateInstance(
        __uuidof(XpsOMObjectFactory),
        NULL, 
        CLSCTX_INPROC_SERVER,
        __uuidof(IXpsOMObjectFactory),
        reinterpret_cast<LPVOID*>(&xpsFactory));

    if (SUCCEEDED(hr))
    {
        // Make sure that you got a pointer 
        //  to the interface.

        // Use object factory...

        // ... and release when done
        xpsFactory->Release();
    }

    // Uninitialize COM when finished
    CoUninitialize();
```



## <a name="best-practices"></a><span data-ttu-id="6a784-110">Bonnes pratiques</span><span class="sxs-lookup"><span data-stu-id="6a784-110">Best Practices</span></span>

<span data-ttu-id="6a784-111">Vous pouvez rendre votre programme plus efficace en obtenant un pointeur vers une interface [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) la première fois que vous devez appeler **IXpsOMObjectFactory** pour créer une interface, puis enregistrer le pointeur pour l’utiliser dans d’autres zones du programme.</span><span class="sxs-lookup"><span data-stu-id="6a784-111">You can make your program more efficient by obtaining a pointer to an [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) interface the first time that you need to call **IXpsOMObjectFactory** to create an interface, and then saving the pointer for use in other areas of the program.</span></span> <span data-ttu-id="6a784-112">Lorsque le programme n’a plus besoin de la fabrique d’objet ou qu’il n’en a plus besoin pendant un certain temps, le pointeur peut être relâché.</span><span class="sxs-lookup"><span data-stu-id="6a784-112">When the program no longer needs the object factory, or will not need it for a while, the pointer can be released.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a784-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a784-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6a784-114">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="6a784-114">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="6a784-115">Créer un modèle d’objet XPS vide</span><span class="sxs-lookup"><span data-stu-id="6a784-115">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)
</dt> <dt>

<span data-ttu-id="6a784-116">**Utilisé dans cette section**</span><span class="sxs-lookup"><span data-stu-id="6a784-116">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="6a784-117">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="6a784-117">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="6a784-118">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="6a784-118">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

<span data-ttu-id="6a784-119">**Pour plus d’informations**</span><span class="sxs-lookup"><span data-stu-id="6a784-119">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="6a784-120">Packaging</span><span class="sxs-lookup"><span data-stu-id="6a784-120">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="6a784-121">Informations de référence sur l’API de document XPS</span><span class="sxs-lookup"><span data-stu-id="6a784-121">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="6a784-122">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="6a784-122">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
