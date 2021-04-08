---
title: Réexaminer les règles d’agrégation COM avec les extensions ADSI
description: Voici un bref aperçu de l’agrégation COM et des règles d’extension ADSI.
ms.assetid: 3efcdfcf-4965-4436-90b2-dc0f627c71b4
ms.tgt_platform: multiple
keywords:
- ADSI d’extensions, règles d’agrégation COM
- ADSI Aggregation COM
- Réexaminer les règles d’agrégation COM avec les extensions ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9b3e3614c4adc225883f120f8fbf362df3e646
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730260"
---
# <a name="revisiting-com-aggregation-rules-with-adsi-extensions"></a><span data-ttu-id="0c33b-106">Réexaminer les règles d’agrégation COM avec les extensions ADSI</span><span class="sxs-lookup"><span data-stu-id="0c33b-106">Revisiting COM Aggregation Rules with ADSI Extensions</span></span>

<span data-ttu-id="0c33b-107">Voici un bref aperçu de l’agrégation COM et des règles d’extension ADSI.</span><span class="sxs-lookup"><span data-stu-id="0c33b-107">The following is a brief review of COM aggregation and ADSI extension rules.</span></span>

-   <span data-ttu-id="0c33b-108">La méthode **CreateInstance** retourne un pointeur vers une interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , comme suit, qui ne délègue aucun appel de fonction à l’agrégation.</span><span class="sxs-lookup"><span data-stu-id="0c33b-108">The **CreateInstance** method returns a pointer to an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface, as follows, that does not delegate any function calls to the aggregator.</span></span>

    <span data-ttu-id="0c33b-109">La méthode [**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) retourne des pointeurs vers les interfaces qu’il prend en charge, ainsi que des erreurs pour les interfaces qu’il ne prend pas en charge.</span><span class="sxs-lookup"><span data-stu-id="0c33b-109">The [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method returns pointers to the interfaces that it supports, and errors for interfaces it does not support.</span></span>

    <span data-ttu-id="0c33b-110">La méthode [**IUnknown :: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) incrémente le décompte de références sur l’objet d’extension agrégé lui-même.</span><span class="sxs-lookup"><span data-stu-id="0c33b-110">The [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method increments the reference count on the aggregated extension object itself.</span></span>

    <span data-ttu-id="0c33b-111">La méthode [**IUnkown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) décrémente le décompte de références sur l’objet d’extension agrégé lui-même et se détruit lorsque le nombre de références est égal à 0.</span><span class="sxs-lookup"><span data-stu-id="0c33b-111">The [**IUnkown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method decrements the reference count on the aggregated extension object itself and destroys itself when the reference count is 0.</span></span>

-   <span data-ttu-id="0c33b-112">L’objet d’extension doit stocker le pointeur [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) de l’agrégateur, tel que m \_ pOuterUnknown, pendant l’implémentation de la méthode **CreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="0c33b-112">The extension object should store the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer of the aggregator, such as m\_pOuterUnknown, during the implementation of the **CreateInstance** method.</span></span>
-   <span data-ttu-id="0c33b-113">Toutes les interfaces prises en charge par l’objet d’extension, y compris [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension), doivent hériter de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), qui délègue tous les appels de fonction à l’agrégateur.</span><span class="sxs-lookup"><span data-stu-id="0c33b-113">All interfaces that the extension object supports, including [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension), should inherit from [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), which delegates all function calls back to the aggregator.</span></span>
    -   <span data-ttu-id="0c33b-114">[**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) appelle « m \_ POuterUnknown->QueryInterface »</span><span class="sxs-lookup"><span data-stu-id="0c33b-114">[**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) calls "m\_pOuterUnknown->QueryInterface"</span></span>
    -   <span data-ttu-id="0c33b-115">[**IUnknown :: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) appelle « m \_ POuterUnknown->AddRef »</span><span class="sxs-lookup"><span data-stu-id="0c33b-115">[**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) calls "m\_pOuterUnknown->AddRef"</span></span>
    -   <span data-ttu-id="0c33b-116">[**IUnkown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) appelle « m \_ POuterUnknown->Release »</span><span class="sxs-lookup"><span data-stu-id="0c33b-116">[**IUnkown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) calls "m\_pOuterUnknown->Release"</span></span>

<span data-ttu-id="0c33b-117">Les rédacteurs d’extensions peuvent choisir n’importe quelle implémentation interne qu’ils préfèrent, à condition qu’ils respectent les règles d’agrégation COM standard.</span><span class="sxs-lookup"><span data-stu-id="0c33b-117">Extension writers can choose any internal implementation they prefer as long as they obey standard COM aggregation rules.</span></span> <span data-ttu-id="0c33b-118">N’oubliez pas qu’un objet d’extension ne doit pas nécessairement fonctionner comme un objet autonome.</span><span class="sxs-lookup"><span data-stu-id="0c33b-118">Be aware that an extension object does not have to work as a standalone object.</span></span> <span data-ttu-id="0c33b-119">Les extensions sont conçues pour fonctionner en tant qu’agrégats.</span><span class="sxs-lookup"><span data-stu-id="0c33b-119">Extensions are designed to work as aggregates.</span></span> <span data-ttu-id="0c33b-120">Toutefois, une extension peut être écrite pour fonctionner à la fois comme un objet autonome et comme un agrégat.</span><span class="sxs-lookup"><span data-stu-id="0c33b-120">However, an extension can be written to work as both a standalone object and as an aggregate.</span></span>

<span data-ttu-id="0c33b-121">En plus de la prise en charge de l’agrégation COM standard, un objet d’extension peut prendre en charge [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) pour des fonctionnalités plus avancées.</span><span class="sxs-lookup"><span data-stu-id="0c33b-121">In addition to standard COM aggregation support, an extension object may support [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) for more advanced features.</span></span> <span data-ttu-id="0c33b-122">Si la liaison tardive est prise en charge, l’extension doit :</span><span class="sxs-lookup"><span data-stu-id="0c33b-122">If late binding is supported, the extension should:</span></span>

-   <span data-ttu-id="0c33b-123">Déléguez les fonctions pour [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) à l’agrégateur.</span><span class="sxs-lookup"><span data-stu-id="0c33b-123">Delegate functions for [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) back to the aggregator.</span></span>
-   <span data-ttu-id="0c33b-124">Implémentez l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) dans [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span><span class="sxs-lookup"><span data-stu-id="0c33b-124">Implement the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface in [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span>

 

 