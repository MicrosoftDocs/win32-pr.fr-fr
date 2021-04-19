---
title: Énumération d’objets dans une collection
description: Énumération d’objets dans une collection
ms.assetid: 664e4d99-48ed-4948-b816-e92ad1ca3ece
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f3c543e01f3c8f154628c6e204aff53c6ad210
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509057"
---
# <a name="enumerating-objects-in-a-collection"></a><span data-ttu-id="ea262-103">Énumération d’objets dans une collection</span><span class="sxs-lookup"><span data-stu-id="ea262-103">Enumerating Objects in a Collection</span></span>

> [!Note]  
> <span data-ttu-id="ea262-104">Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ea262-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="ea262-105">Le contenu de cette rubrique s’applique à IAS et à NPS.</span><span class="sxs-lookup"><span data-stu-id="ea262-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="ea262-106">Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.</span><span class="sxs-lookup"><span data-stu-id="ea262-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="ea262-107">Le code suivant énumère les protocoles de la collection de protocoles NPS.</span><span class="sxs-lookup"><span data-stu-id="ea262-107">The following code enumerates the protocols in the NPS protocols collection.</span></span>


```C++
   HRESULT hr;

   //
   // Retrieve the protocols collection object
   //
   _variant_t vtIASProtocolsCollection;
   hr = pSdo->GetProperty(
      PROPERTY_IAS_PROTOCOLS_COLLECTION,
      &vtIASProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Retrieve the ISdoCollection interface 
   // for the object.
   //
   CComPtr<ISdoCollection> pIASProtocolsCollection;
   hr = vtIASProtocolsCollection.pdispVal->QueryInterface(
      __uuidof(ISdoCollection), 
      (void **) &pIASProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Retrieve the enumeration interface, IEnumVARIANT
   //
   CComPtr<IUnknown> pUnknownProtocol;
   hr = pIASProtocolsCollection->get__NewEnum(&pUnknownProtocol);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<IEnumVARIANT> pEnumProtocols;
   hr = pUnknownProtocol->QueryInterface(
      __uuidof(IEnumVARIANT), 
      (void **) &pEnumProtocols
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Retrieve the first protocol from the collection
   //
   DWORD      dwRetrieved = 1;
   _variant_t vtProtocol;
   hr = pEnumProtocols->Next(1, &vtProtocol, &dwRetrieved);
   if (FAILED(hr))
   {
      return hr;
   }

   while (hr != S_FALSE) {
      // 
      // Retrieve the name of the protocol
      //
      CComPtr<ISdo> pLocalSdo;
      hr = vtProtocol.pdispVal->QueryInterface(
         __uuidof(ISdo), 
         (void**)&pLocalSdo
      );
      if (FAILED(hr))
      {
         return hr;
      }

      _variant_t vtName;
      hr = pLocalSdo->GetProperty(PROPERTY_SDO_NAME, &vtName);
      if (FAILED(hr))
      {
         return hr;
      }

      vtProtocol.Clear();
      vtName.Clear();

      //
      // Retrieve the next protocol from the collection
      //
      dwRetrieved = 1;
      hr = pEnumProtocols->Next(1, &vtProtocol, &dwRetrieved);
      if (FAILED(hr))
      {
         return hr;
      }
   }

```



## <a name="remarks"></a><span data-ttu-id="ea262-108">Notes</span><span class="sxs-lookup"><span data-stu-id="ea262-108">Remarks</span></span>

<span data-ttu-id="ea262-109">Les variables vtName et vtProtocol sont de type [ \_ Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)).</span><span class="sxs-lookup"><span data-stu-id="ea262-109">The vtName and vtProtocol variables are of type [\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)).</span></span> <span data-ttu-id="ea262-110">Un objet [ \_ Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)) encapsule, ou encadre, le type de données **Variant** .</span><span class="sxs-lookup"><span data-stu-id="ea262-110">A [\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)) object encapsulates, or encloses, the **VARIANT** data type.</span></span> <span data-ttu-id="ea262-111">La classe gère l’allocation et la désallocation des ressources et effectue des appels de fonction vers [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) et [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) , selon le cas.</span><span class="sxs-lookup"><span data-stu-id="ea262-111">The class manages resource allocation and deallocation, and makes function calls to [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) and [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) as appropriate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea262-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ea262-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ea262-113">[\_variante \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="ea262-113">[\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span></span>
</dt> <dt>

[<span data-ttu-id="ea262-114">Ajout d’un client</span><span class="sxs-lookup"><span data-stu-id="ea262-114">Adding a Client</span></span>](/windows/desktop/Nps/sdo-adding-a-client)
</dt> <dt>

[<span data-ttu-id="ea262-115">**IASCOMMONPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="ea262-115">**IASCOMMONPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties)
</dt> <dt>

[<span data-ttu-id="ea262-116">**IEnumVARIANT**</span><span class="sxs-lookup"><span data-stu-id="ea262-116">**IEnumVARIANT**</span></span>](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)
</dt> <dt>

[<span data-ttu-id="ea262-117">**ISdo :: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="ea262-117">**ISdo::GetProperty**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[<span data-ttu-id="ea262-118">Récupération d’un service SDO</span><span class="sxs-lookup"><span data-stu-id="ea262-118">Retrieving a Service SDO</span></span>](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[<span data-ttu-id="ea262-119">**VariantClear**</span><span class="sxs-lookup"><span data-stu-id="ea262-119">**VariantClear**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[<span data-ttu-id="ea262-120">**VariantInit**</span><span class="sxs-lookup"><span data-stu-id="ea262-120">**VariantInit**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[<span data-ttu-id="ea262-121">**DIFFÉRENT**</span><span class="sxs-lookup"><span data-stu-id="ea262-121">**VARIANT**</span></span>](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 