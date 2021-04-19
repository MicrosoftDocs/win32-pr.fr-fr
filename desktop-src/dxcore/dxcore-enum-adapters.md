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
# <a name="using-dxcore-to-enumerate-adapters"></a>Utilisation de DXCore pour énumérer des adaptateurs

DXCore étant une API d’énumération d’adaptateur pour les appareils DirectX, certaines de ses fonctionnalités se chevauchent avec celles de [dxgi](../direct3ddxgi/dx-graphics-dxgi.md).

DXCore permet l’exposition de nouveaux types d’appareils au mode utilisateur, tels que MCDM (Microsoft Compute Driver Model), à utiliser avec [Direct3D 12](../direct3d12/directx-12-programming-guide.md), [DirectML](../direct3d12/dml.md)et [Windows machine learning](/windows/ai/windows-ml/). DXCore, contrairement à DXGI, ne fournit aucune information sur la technologie ou les propriétés relatives à l’affichage

Dans les sections suivantes, nous allons jeter un coup d’œil sur les principales fonctionnalités de DXCore avec des exemples de code (écrits en [C++/WinRT](/windows/uwp/cpp-and-winrt-apis)). Les exemples de code ci-dessous sont extraits de la liste complète du code source que vous pouvez trouver dans la rubrique [application dxcore minimal](dxcore-source-code.md).

## <a name="create-an-adapter-factory"></a>Créer une fabrique d’adaptateurs

Vous commencez l’énumération d’adaptateur DXCore en créant un objet de fabrique d’adaptateur, représenté par l’interface [**IDXCoreAdapterFactory**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) . Pour créer une fabrique, incluez le `dxcore.h` fichier d’en-tête et appelez la fonction Free [**DXCoreCreateAdapterFactory**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) .

```cppwinrt
#include <dxcore.h>
...
winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));
```

## <a name="retrieve-an-adapter-list"></a>Récupérer une liste d’adaptateurs

Contrairement à DXGI, une fabrique d’adaptateur DXCore qui vient d’être créée ne crée pas automatiquement un instantané de l’état de l’adaptateur du système. Au lieu de cela, DXCore crée cet instantané lorsque vous récupérez explicitement un objet de liste d’adaptateurs, représenté par l’interface [**IDXCoreAdapterList**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) .

```cppwinrt
winrt::com_ptr<IDXCoreAdapterList> d3D12CoreComputeAdapters;
GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE };
winrt::check_hresult(
    adapterFactory->CreateAdapterList(_countof(attributes),
        attributes,
        d3D12CoreComputeAdapters.put()));
```

## <a name="select-an-appropriate-adapter-from-the-list"></a>Sélectionner une carte appropriée dans la liste

Cette section montre comment, à partir d’un objet de liste d’adaptateurs, vous pouvez trouver la première carte matérielle dans la liste.

La méthode [**IDXCoreAdapterList :: GetAdapterCount**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md) indique le nombre d’éléments de la liste, et [**IDXCoreAdapterList :: GetAdapter**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md) extrait un adaptateur spécifique par index.

Vous pouvez ensuite interroger les propriétés de cet adaptateur, en procédant comme suit.

- Tout d’abord, pour confirmer qu’il est valide pour récupérer la valeur d’une propriété donnée pour cet adaptateur sur cette version du système d’exploitation, vous devez appeler [**IDXCoreAdapter :: IsPropertySupported**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md). Transmettez une valeur de l’énumération [**DXCoreAdapterProperty**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) pour identifier la propriété sur laquelle vous interrogez.
- Confirmez éventuellement la taille de la valeur de la propriété avec un appel à [**IDXCoreAdapter :: GetPropertySize**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md). Pour une propriété telle que **DXCoreAdapterProperty :: IsHardware**, qui est une valeur booléenne simple, cette étape n’est pas nécessaire.
- Enfin, récupérez la valeur de la propriété en appelant [**IDXCoreAdapter :: GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md).

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

## <a name="select-the-preferred-adapter-by-sorting-an-adapter-list"></a>Sélectionner l’adaptateur par défaut en triant une liste d’adaptateurs

Vous pouvez trier une liste d’adaptateurs DXCore en appelant la méthode [IDXCoreAdapterList :: sort](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) .

L’énumération [DXCoreAdapterPreference](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md) définit des valeurs qui représentent des critères de tri. Transmettez un tableau de ces valeurs à **Trier**, puis lisez le premier adaptateur de la liste triée résultante.

Pour déterminer si un type de tri va être compris par **sort**, appelez d’abord [IDXCoreAdapterList :: IsAdapterPreferenceSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).

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

## <a name="query-and-set-adapter-state-properties"></a>Interroger et définir l’état de l’adaptateur (propriétés)

Vous pouvez récupérer et définir l’état d’un élément d’état spécifié d’un adaptateur en appelant les méthodes [**IDXCoreAdapter :: QueryState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) et [**IDXCoreAdapter :: SetState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) .

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

Dans la pratique, avant d’appeler **QueryState** et **SetState**, vous devez appeler [IsQueryStateSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) pour confirmer que l’interrogation du genre d’État est disponible pour cet adaptateur et le système d’exploitation.

## <a name="adapter-list-freshness"></a>Actualisation de la liste des adaptateurs

Si une liste d’adaptateurs devient obsolète en raison de la modification des conditions système, elle est marquée comme telle. Vous pouvez déterminer l’actualisation d’une liste d’adaptateurs en interrogeant sa méthode [**IDXCoreAdapterList :: IsStale**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) .

Plus pratique encore, vous pouvez vous abonner à des notifications pour des conditions telles que l’obsolescence. Pour ce faire, transmettez [**DXCoreNotificationType :: AdapterListStale**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) à [**IDXCoreAdapterFactory :: RegisterEventNotification**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), puis stockez en toute sécurité le cookie retourné pour une utilisation ultérieure.

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

Vous pouvez ensuite générer un nouvel objet de liste d’adaptateurs, en cours à partir de l’objet de fabrique que vous avez déjà. La gestion de ces conditions est essentielle à votre capacité à répondre en toute transparence à des événements tels que l’arrivée et la suppression d’adaptateurs (qu’il s’agisse d’un GPU ou d’un adaptateur de calcul spécialisé) et pour déplacer correctement les charges de travail en réponse.

Avant de détruire l’objet de liste d’adaptateurs, vous devez utiliser la valeur de cookie pour annuler l’inscription de cet objet dans les notifications en appelant [IDXCoreAdapterFactory :: UnregisterEventNotification](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md). Si vous ne désinscrivez pas, une exception irrécupérable est générée lorsque la situation est détectée.

```cppwinrt
HRESULT hr = factory->UnregisterEventNotification(m_eventCookie);
```

## <a name="display-information"></a>Afficher des informations

> [!NOTE]
> DXCore ne fournit pas d’informations d’affichage. Le cas échéant, vous devez utiliser la classe Windows Runtime [**DisplayMonitor**](/uwp/api/windows.devices.display.displaymonitor) pour récupérer ces informations. Le [**LUID**](/windows/win32/api/winnt/ns-winnt-luid) d’un adaptateur fournit un identificateur commun que vous pouvez utiliser pour mapper un adaptateur dxcore aux informations [**DisplayMonitor. DisplayAdapterId**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) . Pour obtenir le LUID d’un adaptateur, transmettez [**DXCoreAdapterProperty :: InstanceLuid**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) à la méthode [**IDXCoreAdapter :: GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md) .

## <a name="see-also"></a>Voir aussi

* [Application DXCore minimale](dxcore-source-code.md)
* [Référence DXCore](./dxcore-reference.md)
* [Graphiques Direct3D 12](../direct3d12/direct3d-12-graphics.md)