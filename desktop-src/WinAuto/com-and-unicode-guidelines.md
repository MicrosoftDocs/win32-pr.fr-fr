---
title: Directives COM et Unicode
description: Étant donné que Microsoft Active Accessibility est basé sur le modèle COM (Component Object Model), les développeurs ont besoin d’un niveau modéré de compréhension des interfaces et des objets COM, et doivent savoir comment effectuer des tâches de base (par exemple, initialiser la bibliothèque COM).
ms.assetid: ed4bbef9-676a-4f4e-926a-044f71399c56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2312b6177891c31c0987b846f7adfc1aa08abc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512322"
---
# <a name="com-and-unicode-guidelines"></a><span data-ttu-id="a256f-103">Directives COM et Unicode</span><span class="sxs-lookup"><span data-stu-id="a256f-103">COM and Unicode Guidelines</span></span>

<span data-ttu-id="a256f-104">Étant donné que Microsoft Active Accessibility est basé sur le modèle COM (Component Object Model), les développeurs ont besoin d’un niveau modéré de compréhension des interfaces et des objets COM, et doivent savoir comment effectuer des tâches de base (par exemple, initialiser la bibliothèque COM).</span><span class="sxs-lookup"><span data-stu-id="a256f-104">Because Microsoft Active Accessibility is based on Component Object Model (COM), developers need a moderate level of understanding about COM objects and interfaces and must know how to perform basic tasks (for example, how to initialize the COM library).</span></span> <span data-ttu-id="a256f-105">Les développeurs de serveurs doivent comprendre comment concevoir des classes qui implémentent l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) et comment créer des objets accessibles.</span><span class="sxs-lookup"><span data-stu-id="a256f-105">Server developers need to understand how to design classes that implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface and how to create accessible objects.</span></span>

<span data-ttu-id="a256f-106">Vous avez également besoin d’un niveau modéré de compréhension d’Unicode pour utiliser un grand nombre des fonctions Microsoft Active Accessibility qui retournent des chaînes.</span><span class="sxs-lookup"><span data-stu-id="a256f-106">You also need a moderate level of understanding about Unicode to use many of the Microsoft Active Accessibility functions that return strings.</span></span>

<span data-ttu-id="a256f-107">Pour utiliser Microsoft Active Accessibility efficacement, vous devez comprendre les fonctions, structures, types de données et interfaces COM et Unicode suivants.</span><span class="sxs-lookup"><span data-stu-id="a256f-107">To use Microsoft Active Accessibility effectively, you should understand the following COM and Unicode functions, structures, data types, and interfaces.</span></span> <span data-ttu-id="a256f-108">Des informations limitées sur certains de ces éléments sont fournies dans cette documentation.</span><span class="sxs-lookup"><span data-stu-id="a256f-108">Limited information about some of these items is provided in this documentation.</span></span>

### <a name="functions"></a><span data-ttu-id="a256f-109">Fonctions :</span><span class="sxs-lookup"><span data-stu-id="a256f-109">Functions:</span></span>

-   [<span data-ttu-id="a256f-110">**Échec**</span><span class="sxs-lookup"><span data-stu-id="a256f-110">**OleInitialize**</span></span>](/windows/desktop/api/ole2/nf-ole2-oleinitialize)
-   <span data-ttu-id="a256f-111">[**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [ **CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)</span><span class="sxs-lookup"><span data-stu-id="a256f-111">[**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)</span></span>
-   <span data-ttu-id="a256f-112">[**IUnknown :: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) et [ **IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)</span><span class="sxs-lookup"><span data-stu-id="a256f-112">[**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)</span></span>
-   <span data-ttu-id="a256f-113">[**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) et [ **VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)</span><span class="sxs-lookup"><span data-stu-id="a256f-113">[**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) and [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)</span></span>
-   <span data-ttu-id="a256f-114">[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) et [ **WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)</span><span class="sxs-lookup"><span data-stu-id="a256f-114">[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) and [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)</span></span>
-   <span data-ttu-id="a256f-115">[**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) et [ **SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)</span><span class="sxs-lookup"><span data-stu-id="a256f-115">[**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) and [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)</span></span>

### <a name="structures-and-data-types"></a><span data-ttu-id="a256f-116">Structures et types de données :</span><span class="sxs-lookup"><span data-stu-id="a256f-116">Structures and data types:</span></span>

-   [<span data-ttu-id="a256f-117">**DIFFÉRENT**</span><span class="sxs-lookup"><span data-stu-id="a256f-117">**VARIANT**</span></span>](variant-structure.md)
-   [<span data-ttu-id="a256f-118">**SIGNÉ**</span><span class="sxs-lookup"><span data-stu-id="a256f-118">**HRESULT**</span></span>](/windows/desktop/com/structure-of-com-error-codes)
-   [<span data-ttu-id="a256f-119">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="a256f-119">**BSTR**</span></span>](/previous-versions/windows/desktop/automat/bstr)

### <a name="com-interfaces"></a><span data-ttu-id="a256f-120">Interfaces COM :</span><span class="sxs-lookup"><span data-stu-id="a256f-120">COM Interfaces:</span></span>

-   [<span data-ttu-id="a256f-121">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="a256f-121">**IUnknown**</span></span>](/windows/desktop/api/unknwn/nn-unknwn-iunknown)
-   [<span data-ttu-id="a256f-122">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="a256f-122">**IDispatch**</span></span>](idispatch-interface.md)
-   [<span data-ttu-id="a256f-123">**IEnumVARIANT**</span><span class="sxs-lookup"><span data-stu-id="a256f-123">**IEnumVARIANT**</span></span>](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant)

## <a name="in-this-section"></a><span data-ttu-id="a256f-124">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="a256f-124">In this section</span></span>

-   [<span data-ttu-id="a256f-125">Structure de variante</span><span class="sxs-lookup"><span data-stu-id="a256f-125">VARIANT Structure</span></span>](variant-structure.md)
-   [<span data-ttu-id="a256f-126">Interface IDispatch</span><span class="sxs-lookup"><span data-stu-id="a256f-126">IDispatch Interface</span></span>](idispatch-interface.md)
-   [<span data-ttu-id="a256f-127">Conversion de chaînes Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="a256f-127">Converting Unicode and ANSI Strings</span></span>](converting-unicode-and-ansi-strings.md)

 

 