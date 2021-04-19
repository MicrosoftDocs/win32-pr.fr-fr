---
title: Utilisation de DXCore pour énumérer des adaptateurs
description: Découvrez les principales fonctionnalités de DXCore avec des exemples de code, ainsi qu’une liste complète de code source d’une application DXCore minimale.
ms.localizationpriority: high
ms.topic: article
ms.date: 06/20/2019
ms.openlocfilehash: f1c21971f2daea69de1f317d1db8eceb9ec00118
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511288"
---
# <a name="using-dxcore-to-enumerate-adapters"></a><span data-ttu-id="0762a-103">Utilisation de DXCore pour énumérer des adaptateurs</span><span class="sxs-lookup"><span data-stu-id="0762a-103">Using DXCore to enumerate adapters</span></span>

<span data-ttu-id="0762a-104">DXCore étant une API d’énumération d’adaptateur pour les appareils DirectX, certaines de ses fonctionnalités se chevauchent avec celles de [dxgi](../direct3ddxgi/dx-graphics-dxgi.md).</span><span class="sxs-lookup"><span data-stu-id="0762a-104">DXCore is an adapter enumeration API for DirectX devices, so some of its facilities overlap with those of [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).</span></span>

<span data-ttu-id="0762a-105">DXCore permet l’exposition de nouveaux types d’appareils au mode utilisateur, tels que MCDM (Microsoft Compute Driver Model), à utiliser avec [Direct3D 12](../direct3d12/directx-12-programming-guide.md), [DirectML](../direct3d12/dml.md)et [Windows machine learning](/windows/ai/windows-ml/).</span><span class="sxs-lookup"><span data-stu-id="0762a-105">DXCore enables the exposure of new device types to user mode, such as MCDM (Microsoft Compute Driver Model), for use with [Direct3D 12](../direct3d12/directx-12-programming-guide.md), [DirectML](../direct3d12/dml.md), and [Windows Machine Learning](/windows/ai/windows-ml/).</span></span> <span data-ttu-id="0762a-106">DXCore, contrairement à DXGI, ne fournit aucune information sur la technologie ou les propriétés relatives à l’affichage</span><span class="sxs-lookup"><span data-stu-id="0762a-106">DXCore, unlike DXGI, does not provide any information about display-related technology or properties</span></span>

<span data-ttu-id="0762a-107">Dans les sections suivantes, nous allons jeter un coup d’œil sur les principales fonctionnalités de DXCore avec des exemples de code (écrits en [C++/WinRT](/windows/uwp/cpp-and-winrt-apis)).</span><span class="sxs-lookup"><span data-stu-id="0762a-107">In the next few sections, we'll take a look at the main features of DXCore with some code examples (written in [C++/WinRT](/windows/uwp/cpp-and-winrt-apis)).</span></span> <span data-ttu-id="0762a-108">Les exemples de code ci-dessous sont extraits de la liste complète du code source que vous pouvez trouver dans la rubrique [application dxcore minimal](dxcore-source-code.md).</span><span class="sxs-lookup"><span data-stu-id="0762a-108">The code examples shown below are extracted from the full source code listing that you can find in the topic [Minimal DXCore application](dxcore-source-code.md).</span></span>

## <a name="create-an-adapter-factory"></a><span data-ttu-id="0762a-109">Créer une fabrique d’adaptateurs</span><span class="sxs-lookup"><span data-stu-id="0762a-109">Create an adapter factory</span></span>

<span data-ttu-id="0762a-110">Vous commencez l’énumération d’adaptateur DXCore en créant un objet de fabrique d’adaptateur, représenté par l’interface [**IDXCoreAdapterFactory**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) .</span><span class="sxs-lookup"><span data-stu-id="0762a-110">You begin DXCore adapter enumeration by creating an adapter factory object, which is represented by the [**IDXCoreAdapterFactory**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) interface.</span></span> <span data-ttu-id="0762a-111">Pour créer une fabrique, incluez le `dxcore.h` fichier d’en-tête et appelez la fonction Free [**DXCoreCreateAdapterFactory**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) .</span><span class="sxs-lookup"><span data-stu-id="0762a-111">To create a factory, include the `dxcore.h` header file, and call the [**DXCoreCreateAdapterFactory**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) free function.</span></span>

```cppwinrt
#include <dxcore.h>
...
winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));
```

## <a name="retrieve-an-adapter-list"></a><span data-ttu-id="0762a-112">Récupérer une liste d’adaptateurs</span><span class="sxs-lookup"><span data-stu-id="0762a-112">Retrieve an adapter list</span></span>

<span data-ttu-id="0762a-113">Contrairement à DXGI, une fabrique d’adaptateur DXCore qui vient d’être créée ne crée pas automatiquement un instantané de l’état de l’adaptateur du système.</span><span class="sxs-lookup"><span data-stu-id="0762a-113">Unlike with DXGI, a newly-created DXCore adapter factory doesn't automatically create a snapshot of the adapter state of the system.</span></span> <span data-ttu-id="0762a-114">Au lieu de cela, DXCore crée cet instantané lorsque vous récupérez explicitement un objet de liste d’adaptateurs, représenté par l’interface [**IDXCoreAdapterList**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) .</span><span class="sxs-lookup"><span data-stu-id="0762a-114">Instead, DXCore creates that snapshot when you explicitly retrieve an adapter list object, which is represented by the [**IDXCoreAdapterList**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) interface.</span></span>

```cppwinrt
winrt::com_ptr<IDXCoreAdapterList> d3D12CoreComputeAdapters;
GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE };
winrt::check_hresult(
    adapterFactory->CreateAdapterList(_countof(attributes),
        attributes,
        d3D12CoreComputeAdapters.put()));
```

## <a name="select-an-appropriate-adapter-from-the-list"></a><span data-ttu-id="0762a-115">Sélectionner une carte appropriée dans la liste</span><span class="sxs-lookup"><span data-stu-id="0762a-115">Select an appropriate adapter from the list</span></span>

<span data-ttu-id="0762a-116">Cette section montre comment, à partir d’un objet de liste d’adaptateurs, vous pouvez trouver la première carte matérielle dans la liste.</span><span class="sxs-lookup"><span data-stu-id="0762a-116">This section demonstrates how, given an adapter list object, you could find the first hardware adapter in the list.</span></span>

<span data-ttu-id="0762a-117">La méthode [**IDXCoreAdapterList :: GetAdapterCount**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md) indique le nombre d’éléments de la liste, et [**IDXCoreAdapterList :: GetAdapter**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md) extrait un adaptateur spécifique par index.</span><span class="sxs-lookup"><span data-stu-id="0762a-117">The [**IDXCoreAdapterList::GetAdapterCount**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md) method tells you the number of elements in the list, and [**IDXCoreAdapterList::GetAdapter**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md) retrieves a specific adapter by index.</span></span>

<span data-ttu-id="0762a-118">Vous pouvez ensuite interroger les propriétés de cet adaptateur, en procédant comme suit.</span><span class="sxs-lookup"><span data-stu-id="0762a-118">You can then query the properties of that adapter, by following these steps.</span></span>

- <span data-ttu-id="0762a-119">Tout d’abord, pour confirmer qu’il est valide pour récupérer la valeur d’une propriété donnée pour cet adaptateur sur cette version du système d’exploitation, vous devez appeler [**IDXCoreAdapter :: IsPropertySupported**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md).</span><span class="sxs-lookup"><span data-stu-id="0762a-119">First, to confirm that it's valid to retrieve the value of a given property for this adapter on this operating system version, you call [**IDXCoreAdapter::IsPropertySupported**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md).</span></span> <span data-ttu-id="0762a-120">Transmettez une valeur de l’énumération [**DXCoreAdapterProperty**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) pour identifier la propriété sur laquelle vous interrogez.</span><span class="sxs-lookup"><span data-stu-id="0762a-120">Pass a value of the [**DXCoreAdapterProperty**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) enumeration to identify which property you're querying about.</span></span>
- <span data-ttu-id="0762a-121">Confirmez éventuellement la taille de la valeur de la propriété avec un appel à [**IDXCoreAdapter :: GetPropertySize**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md).</span><span class="sxs-lookup"><span data-stu-id="0762a-121">Optionally confirm the size of the property value with a call to [**IDXCoreAdapter::GetPropertySize**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md).</span></span> <span data-ttu-id="0762a-122">Pour une propriété telle que **DXCoreAdapterProperty :: IsHardware**, qui est une valeur booléenne simple, cette étape n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0762a-122">For a property such as **DXCoreAdapterProperty::IsHardware**, which is a simple Boolean, this step isn't necessary.</span></span>
- <span data-ttu-id="0762a-123">Enfin, récupérez la valeur de la propriété en appelant [**IDXCoreAdapter :: GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md).</span><span class="sxs-lookup"><span data-stu-id="0762a-123">And, finally, retrieve the property's value by calling [**IDXCoreAdapter::GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md).</span></span>

```cppwinrt
winrt::com_ptr<IDXCoreAdapter> preferredAdapter;

const uint32_t count{ d3D12CoreComputeAdapters->GetAdapterCount() };

for (uint32_t i = 0; i < count; ++i)
{
    winrt::com_ptr<IDXCoreAdapter> candidateAdapter;
    winrt::check_hresult(
        d3D12CoreComputeAdapters->GetAdapter(i, candidateAdapter.put()));

    bool isHardware{ false };
    winrt::check_hresult(candidateAdapter->GetProperty(
        DXCoreAdapterProperty::IsHardware,
        &isHardware));

    if (isHardware)
    {
        // Choose the first hardware adapter, and stop looping.
        preferredAdapter = candidateAdapter;
        break;
    }

    // Otherwise, ensure that (as long as there are *any* adapters) we'll
    // at least choose one.
    if (!preferredAdapter)
    {
        preferredAdapter = candidateAdapter;
    }
}
```

## <a name="select-the-preferred-adapter-by-sorting-an-adapter-list"></a><span data-ttu-id="0762a-124">Sélectionner l’adaptateur par défaut en triant une liste d’adaptateurs</span><span class="sxs-lookup"><span data-stu-id="0762a-124">Select the preferred adapter by sorting an adapter list</span></span>

<span data-ttu-id="0762a-125">Vous pouvez trier une liste d’adaptateurs DXCore en appelant la méthode [IDXCoreAdapterList :: sort](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) .</span><span class="sxs-lookup"><span data-stu-id="0762a-125">You can sort a DXCore adapter list by calling the [IDXCoreAdapterList::Sort](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) method.</span></span>

<span data-ttu-id="0762a-126">L’énumération [DXCoreAdapterPreference](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md) définit des valeurs qui représentent des critères de tri.</span><span class="sxs-lookup"><span data-stu-id="0762a-126">The [DXCoreAdapterPreference](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md) enumeration defines values that representing sort criteria.</span></span> <span data-ttu-id="0762a-127">Transmettez un tableau de ces valeurs à **Trier**, puis lisez le premier adaptateur de la liste triée résultante.</span><span class="sxs-lookup"><span data-stu-id="0762a-127">Pass an array of those values to **Sort**, and then read off the first adapter in the resulting sorted list.</span></span>

<span data-ttu-id="0762a-128">Pour déterminer si un type de tri va être compris par **sort**, appelez d’abord [IDXCoreAdapterList :: IsAdapterPreferenceSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span><span class="sxs-lookup"><span data-stu-id="0762a-128">To determine whether a sort type is going to be understood by **Sort**, first call [IDXCoreAdapterList::IsAdapterPreferenceSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span></span>

```cppwinrt
winrt::com_ptr<IDXCoreAdapter> TryFindHardwareHighPerformanceGraphicsAdapter()
{
    // You begin DXCore adapter enumeration by creating an adapter factory.
    winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
    winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));

    // From the factory, retrieve a list of all the Direct3D 12 Graphics adapters.
    winrt::com_ptr<IDXCoreAdapterList> d3D12GraphicsAdapters;
    GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS };
    winrt::check_hresult(
        adapterFactory->CreateAdapterList(_countof(attributes),
            attributes,
            d3D12GraphicsAdapters.put()));

    DXCoreAdapterPreference sortPreferences[]{
        DXCoreAdapterPreference::Hardware, DXCoreAdapterPreference::HighPerformance };

    // Ask the OS to sort for the highest performance hardware adapter.
    winrt::check_hresult(d3D12GraphicsAdapters->Sort(_countof(sortPreferences), sortPreferences));

    winrt::com_ptr<IDXCoreAdapter> preferredAdapter;

    if (d3D12GraphicsAdapters->GetAdapterCount() > 0)
    {
        winrt::check_hresult(d3D12GraphicsAdapters->GetAdapter(0, preferredAdapter.put()));
    }

    return preferredAdapter;
}
```

## <a name="query-and-set-adapter-state-properties"></a><span data-ttu-id="0762a-129">Interroger et définir l’état de l’adaptateur (propriétés)</span><span class="sxs-lookup"><span data-stu-id="0762a-129">Query and set adapter state (properties)</span></span>

<span data-ttu-id="0762a-130">Vous pouvez récupérer et définir l’état d’un élément d’état spécifié d’un adaptateur en appelant les méthodes [**IDXCoreAdapter :: QueryState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) et [**IDXCoreAdapter :: SetState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) .</span><span class="sxs-lookup"><span data-stu-id="0762a-130">You can retrieve and set the state of a specified state item of an adapter by calling the [**IDXCoreAdapter::QueryState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) and [**IDXCoreAdapter::SetState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) methods.</span></span>

```cppwinrt
void SetDesiredMemoryReservation(winrt::com_ptr<IDXCoreAdapter> const& adapter, uint64_t reservation)
{
    DXCoreAdapterMemoryBudgetNodeSegmentGroup nodeSegmentGroup{};
    nodeSegmentGroup.nodeIndex = 0;
    nodeSegmentGroup.segmentGroup = DXCoreSegmentGroup::Local;

    DXCoreAdapterMemoryBudget memoryBudget{};
    winrt::check_hresult(adapter->QueryState(
        DXCoreAdapterState::AdapterMemoryBudget,
        &nodeSegmentGroup,
        &memoryBudget));

    // Clamp the reservation to what's available.
    reservation = std::min<uint64_t>(reservation, memoryBudget.availableForReservation);

    winrt::check_hresult(adapter->SetState(
        DXCoreAdapterState::AdapterMemoryBudget,
        &nodeSegmentGroup,
        &reservation));
}
```

<span data-ttu-id="0762a-131">Dans la pratique, avant d’appeler **QueryState** et **SetState**, vous devez appeler [IsQueryStateSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) pour confirmer que l’interrogation du genre d’État est disponible pour cet adaptateur et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0762a-131">In practice, before calling **QueryState** and **SetState**, you should call [IsQueryStateSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>

## <a name="adapter-list-freshness"></a><span data-ttu-id="0762a-132">Actualisation de la liste des adaptateurs</span><span class="sxs-lookup"><span data-stu-id="0762a-132">Adapter list freshness</span></span>

<span data-ttu-id="0762a-133">Si une liste d’adaptateurs devient obsolète en raison de la modification des conditions système, elle est marquée comme telle.</span><span class="sxs-lookup"><span data-stu-id="0762a-133">Should an adapter list become stale due to changing system conditions, it will be marked as such.</span></span> <span data-ttu-id="0762a-134">Vous pouvez déterminer l’actualisation d’une liste d’adaptateurs en interrogeant sa méthode [**IDXCoreAdapterList :: IsStale**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) .</span><span class="sxs-lookup"><span data-stu-id="0762a-134">You can determine an adapter list's freshness by polling its [**IDXCoreAdapterList::IsStale**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) method.</span></span>

<span data-ttu-id="0762a-135">Plus pratique encore, vous pouvez vous abonner à des notifications pour des conditions telles que l’obsolescence.</span><span class="sxs-lookup"><span data-stu-id="0762a-135">More conveniently, though, you can subscribe to notifications for conditions such as staleness.</span></span> <span data-ttu-id="0762a-136">Pour ce faire, transmettez [**DXCoreNotificationType :: AdapterListStale**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) à [**IDXCoreAdapterFactory :: RegisterEventNotification**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), puis stockez en toute sécurité le cookie retourné pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="0762a-136">To do that, pass [**DXCoreNotificationType::AdapterListStale**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) to [**IDXCoreAdapterFactory::RegisterEventNotification**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), and safely store the returned cookie for use later.</span></span>

```cppwinrt
uint32_t m_eventCookie = 0;
...
winrt::check_hresult(factory->RegisterEventNotification(
    m_adapters.get(),
    DXCoreNotificationType::AdapterListStale,
    OnAdapterListStale,
    this,
    &m_eventCookie));
...
static void WINAPI OnAdapterListStale(
    DXCoreNotificationType notificationType,
    IUnknown* staleObject,
    void* context)
{
    ...
}
```

<span data-ttu-id="0762a-137">Vous pouvez ensuite générer un nouvel objet de liste d’adaptateurs, en cours à partir de l’objet de fabrique que vous avez déjà.</span><span class="sxs-lookup"><span data-stu-id="0762a-137">You can then generate a new, current, adapter list object from the factory object that you already have.</span></span> <span data-ttu-id="0762a-138">La gestion de ces conditions est essentielle à votre capacité à répondre en toute transparence à des événements tels que l’arrivée et la suppression d’adaptateurs (qu’il s’agisse d’un GPU ou d’un adaptateur de calcul spécialisé) et pour déplacer correctement les charges de travail en réponse.</span><span class="sxs-lookup"><span data-stu-id="0762a-138">Handling these conditions is critical to your ability to seamlessly respond to events such as adapter arrival and removal (whether that be a GPU, or a specialized compute adapter), and to appropriately shift workloads in response.</span></span>

<span data-ttu-id="0762a-139">Avant de détruire l’objet de liste d’adaptateurs, vous devez utiliser la valeur de cookie pour annuler l’inscription de cet objet dans les notifications en appelant [IDXCoreAdapterFactory :: UnregisterEventNotification](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md).</span><span class="sxs-lookup"><span data-stu-id="0762a-139">Before you destroy the adapter list object, you must use the cookie value to unregister that object from notifications by calling [IDXCoreAdapterFactory::UnregisterEventNotification](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md).</span></span> <span data-ttu-id="0762a-140">Si vous ne désinscrivez pas, une exception irrécupérable est générée lorsque la situation est détectée.</span><span class="sxs-lookup"><span data-stu-id="0762a-140">If you don't unregister, then a fatal exception is raised when the situation is detected.</span></span>

```cppwinrt
HRESULT hr = factory->UnregisterEventNotification(m_eventCookie);
```

## <a name="display-information"></a><span data-ttu-id="0762a-141">Afficher des informations</span><span class="sxs-lookup"><span data-stu-id="0762a-141">Display information</span></span>

> [!NOTE]
> <span data-ttu-id="0762a-142">DXCore ne fournit pas d’informations d’affichage.</span><span class="sxs-lookup"><span data-stu-id="0762a-142">DXCore doesn't itself provide any display information.</span></span> <span data-ttu-id="0762a-143">Le cas échéant, vous devez utiliser la classe Windows Runtime [**DisplayMonitor**](/uwp/api/windows.devices.display.displaymonitor) pour récupérer ces informations.</span><span class="sxs-lookup"><span data-stu-id="0762a-143">Where necessary, you should use the Windows Runtime [**DisplayMonitor**](/uwp/api/windows.devices.display.displaymonitor) class to retrieve this information.</span></span> <span data-ttu-id="0762a-144">Le [**LUID**](/windows/win32/api/winnt/ns-winnt-luid) d’un adaptateur fournit un identificateur commun que vous pouvez utiliser pour mapper un adaptateur dxcore aux informations [**DisplayMonitor. DisplayAdapterId**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) .</span><span class="sxs-lookup"><span data-stu-id="0762a-144">An adapter's [**LUID**](/windows/win32/api/winnt/ns-winnt-luid) provides a common identifier that you can use to map a DXCore adapter to [**DisplayMonitor.DisplayAdapterId**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) information.</span></span> <span data-ttu-id="0762a-145">Pour obtenir le LUID d’un adaptateur, transmettez [**DXCoreAdapterProperty :: InstanceLuid**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) à la méthode [**IDXCoreAdapter :: GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="0762a-145">To obtain an adapter's LUID, pass [**DXCoreAdapterProperty::InstanceLuid**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) to the [**IDXCoreAdapter::GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="0762a-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0762a-146">See also</span></span>

* [<span data-ttu-id="0762a-147">Application DXCore minimale</span><span class="sxs-lookup"><span data-stu-id="0762a-147">Minimal DXCore application</span></span>](dxcore-source-code.md)
* [<span data-ttu-id="0762a-148">Référence DXCore</span><span class="sxs-lookup"><span data-stu-id="0762a-148">DXCore Reference</span></span>](./dxcore-reference.md)
* [<span data-ttu-id="0762a-149">Graphiques Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="0762a-149">Direct3D 12 graphics</span></span>](../direct3d12/direct3d-12-graphics.md)