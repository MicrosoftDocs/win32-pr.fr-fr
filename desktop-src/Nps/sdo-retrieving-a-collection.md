---
title: Récupération d’une collection
description: Récupération d’une collection
ms.assetid: b9090ad5-564c-4f48-b7bd-24617d582d2e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 517acfa320069f9c94ee291e9215459d27ba25ad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941171"
---
# <a name="retrieving-a-collection"></a><span data-ttu-id="0851a-103">Récupération d’une collection</span><span class="sxs-lookup"><span data-stu-id="0851a-103">Retrieving a Collection</span></span>

> [!Note]  
> <span data-ttu-id="0851a-104">Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="0851a-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="0851a-105">Le contenu de cette rubrique s’applique à IAS et à NPS.</span><span class="sxs-lookup"><span data-stu-id="0851a-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="0851a-106">Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.</span><span class="sxs-lookup"><span data-stu-id="0851a-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="0851a-107">Le code suivant récupère la collection de clients pour le serveur NPS.</span><span class="sxs-lookup"><span data-stu-id="0851a-107">The following code retrieves the clients collection for the Network Policy Server.</span></span>


```C++
// Retrieve the clients collection 
   HRESULT hr;
   CComPtr<ISdo>  pSdo;
   hr = pSdoServiceControl->QueryInterface(
      __uuidof(ISdo),
      (void**) &pSdo
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // First Retrieve the protocols collection
   //
   _variant_t  vtProtocolsCollection;
   hr = pSdo->GetProperty(
      PROPERTY_IAS_PROTOCOLS_COLLECTION,
      &vtProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Get the ISdoCollection interface 
   // for the object.
   //
   CComPtr<ISdoCollection>  pProtocolsCollection;
   hr = vtProtocolsCollection.pdispVal->QueryInterface(
      __uuidof(ISdoCollection), 
      (void **) &pProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Then retrieve the RADIUS protocol
   //
   CComPtr<IDispatch> pRadiusDispatch;
   _variant_t  vtProtocolName = L"Microsoft Radius Protocol";
   hr = pProtocolsCollection->Item(&vtProtocolName, &pRadiusDispatch);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pRadiusSdo;
   hr = pRadiusDispatch->QueryInterface(      
      __uuidof(ISdo), 
      (void **) &pRadiusSdo
   );

   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Then retrieve the clients collection
   //
   _variant_t  vtClientsCollection;
   hr = pRadiusSdo->GetProperty(PROPERTY_RADIUS_CLIENTS_COLLECTION, &vtClientsCollection);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdoCollection> pClientsCollection;
   hr = vtClientsCollection.pdispVal->QueryInterface(      
      __uuidof(ISdoCollection), 
      (void **) &pClientsCollection
   );

   if (FAILED(hr))
   {
      return hr;
   }

```



## <a name="remarks"></a><span data-ttu-id="0851a-108">Notes</span><span class="sxs-lookup"><span data-stu-id="0851a-108">Remarks</span></span>

<span data-ttu-id="0851a-109">La variable pSdoServiceControl contient un pointeur vers un objet de données serveur pour NPS.</span><span class="sxs-lookup"><span data-stu-id="0851a-109">The pSdoServiceControl variable contains a pointer to a Server Data Object for NPS.</span></span> <span data-ttu-id="0851a-110">Pour plus d’informations, consultez la rubrique [récupération d’un service SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo).</span><span class="sxs-lookup"><span data-stu-id="0851a-110">For more information, see the topic [Retrieving a Service SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo).</span></span>

<span data-ttu-id="0851a-111">La variable vtClientsCollection est de type [ \_ Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)).</span><span class="sxs-lookup"><span data-stu-id="0851a-111">The vtClientsCollection variable is of type [\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)).</span></span> <span data-ttu-id="0851a-112">Un \_ \_ objet variant t encapsule, ou encadre, le type de données [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .</span><span class="sxs-lookup"><span data-stu-id="0851a-112">A \_variant\_t object encapsulates, or encloses, the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) data type.</span></span> <span data-ttu-id="0851a-113">La classe gère l’allocation et la désallocation des ressources et effectue des appels de fonction vers [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) et [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) , selon le cas.</span><span class="sxs-lookup"><span data-stu-id="0851a-113">The class manages resource allocation and deallocation, and makes function calls to [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) and [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) as appropriate.</span></span>

<span data-ttu-id="0851a-114">Après l’appel à « pSdo->GetProperty () », la variable vtProtocolsCollection spécifie un objet.</span><span class="sxs-lookup"><span data-stu-id="0851a-114">After the call to "pSdo->GetProperty()", the vtProtocolsCollection variable specifies an object.</span></span> <span data-ttu-id="0851a-115">Le membre **pdispVal** de vtProtocolsCollection contient un pointeur vers l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="0851a-115">The **pdispVal** member of vtProtocolsCollection contains a pointer to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface for the object.</span></span>

<span data-ttu-id="0851a-116">L’exemple de code ci-dessus peut être adapté pour récupérer d’autres collections NPS, par exemple les collections de gestionnaires de demandes NPS.</span><span class="sxs-lookup"><span data-stu-id="0851a-116">The above sample code can be adapted to retrieve other NPS collections, for example the NPS Request Handlers collections.</span></span> <span data-ttu-id="0851a-117">Valeurs énumérées du type énumération [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) qui correspondent aux collections NPS disponibles.</span><span class="sxs-lookup"><span data-stu-id="0851a-117">The [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) enumeration type enumerated values that correspond to the available NPS collections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0851a-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0851a-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0851a-119">[\_variante \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="0851a-119">[\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span></span>
</dt> <dt>

[<span data-ttu-id="0851a-120">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="0851a-120">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> <dt>

[<span data-ttu-id="0851a-121">**ISdo :: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="0851a-121">**ISdo::GetProperty**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[<span data-ttu-id="0851a-122">**ISdoCollection**</span><span class="sxs-lookup"><span data-stu-id="0851a-122">**ISdoCollection**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[<span data-ttu-id="0851a-123">Récupération d’un service SDO</span><span class="sxs-lookup"><span data-stu-id="0851a-123">Retrieving a Service SDO</span></span>](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[<span data-ttu-id="0851a-124">**VariantClear**</span><span class="sxs-lookup"><span data-stu-id="0851a-124">**VariantClear**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[<span data-ttu-id="0851a-125">**VariantInit**</span><span class="sxs-lookup"><span data-stu-id="0851a-125">**VariantInit**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[<span data-ttu-id="0851a-126">**DIFFÉRENT**</span><span class="sxs-lookup"><span data-stu-id="0851a-126">**VARIANT**</span></span>](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 