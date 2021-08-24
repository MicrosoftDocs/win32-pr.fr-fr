---
title: Énumération d’objets dans une collection
description: Énumération d’objets dans une collection
ms.assetid: 664e4d99-48ed-4948-b816-e92ad1ca3ece
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0399a75e9301fcdb5e88e6f30b7e0b2ef66160fa05136ed43b51fa8e80eca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742109"
---
# <a name="enumerating-objects-in-a-collection"></a>Énumération d’objets dans une collection

> [!Note]  
> le Service d’authentification Internet (IAS) a été renommé serveur nps (network Policy Server) à partir de Windows Server 2008. Le contenu de cette rubrique s’applique à IAS et à NPS. Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.

 

Le code suivant énumère les protocoles de la collection de protocoles NPS.


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



## <a name="remarks"></a>Remarques

Les variables vtName et vtProtocol sont de type [ \_ Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)). Un objet [ \_ Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)) encapsule, ou encadre, le type de données **Variant** . La classe gère l’allocation et la désallocation des ressources et effectue des appels de fonction vers [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) et [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) , selon le cas.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[\_variante \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))
</dt> <dt>

[Ajout d’un client](/windows/desktop/Nps/sdo-adding-a-client)
</dt> <dt>

[**IASCOMMONPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties)
</dt> <dt>

[**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)
</dt> <dt>

[**ISdo :: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[Récupération d’un service SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[**DIFFÉRENT**](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 