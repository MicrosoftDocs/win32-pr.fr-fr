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
# <a name="retrieving-a-collection"></a>Récupération d’une collection

> [!Note]  
> Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008. Le contenu de cette rubrique s’applique à IAS et à NPS. Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.

 

Le code suivant récupère la collection de clients pour le serveur NPS.


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



## <a name="remarks"></a>Notes

La variable pSdoServiceControl contient un pointeur vers un objet de données serveur pour NPS. Pour plus d’informations, consultez la rubrique [récupération d’un service SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo).

La variable vtClientsCollection est de type [ \_ Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)). Un \_ \_ objet variant t encapsule, ou encadre, le type de données [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) . La classe gère l’allocation et la désallocation des ressources et effectue des appels de fonction vers [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) et [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) , selon le cas.

Après l’appel à « pSdo->GetProperty () », la variable vtProtocolsCollection spécifie un objet. Le membre **pdispVal** de vtProtocolsCollection contient un pointeur vers l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pour l’objet.

L’exemple de code ci-dessus peut être adapté pour récupérer d’autres collections NPS, par exemple les collections de gestionnaires de demandes NPS. Valeurs énumérées du type énumération [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) qui correspondent aux collections NPS disponibles.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[\_variante \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))
</dt> <dt>

[**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> <dt>

[**ISdo :: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[Récupération d’un service SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[**DIFFÉRENT**](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 