---
description: Un attribut est une paire clé/valeur, où la clé est un GUID et la valeur est un PROPVARIANT. Les attributs sont utilisés tout au long de Microsoft Media Foundation pour configurer des objets, décrire des formats multimédias, interroger des propriétés d’objet, etc.
ms.assetid: 44af5e03-5f0a-4564-b9d6-b8c935df35b2
title: Attributs dans Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e7893586aa1e966b95c1af5d04246bbb0c82ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749381"
---
# <a name="attributes-in-media-foundation"></a><span data-ttu-id="1d1f3-104">Attributs dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1d1f3-104">Attributes in Media Foundation</span></span>

<span data-ttu-id="1d1f3-105">Un attribut est une paire clé/valeur, où la clé est un GUID et la valeur est un **PROPVARIANT**.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-105">An attribute is a key/value pair, where the key is a GUID and the value is a **PROPVARIANT**.</span></span> <span data-ttu-id="1d1f3-106">Les attributs sont utilisés tout au long de Microsoft Media Foundation pour configurer des objets, décrire des formats multimédias, interroger des propriétés d’objet, etc.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-106">Attributes are used throughout Microsoft Media Foundation to configure objects, describe media formats, query object properties, and other purposes.</span></span>

<span data-ttu-id="1d1f3-107">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="1d1f3-108">Présentation des attributs</span><span class="sxs-lookup"><span data-stu-id="1d1f3-108">About Attributes</span></span>](#about-attributes)
-   [<span data-ttu-id="1d1f3-109">Sérialisation des attributs</span><span class="sxs-lookup"><span data-stu-id="1d1f3-109">Serializing Attributes</span></span>](#serializing-attributes)
-   [<span data-ttu-id="1d1f3-110">Implémentation de IMFAttributes</span><span class="sxs-lookup"><span data-stu-id="1d1f3-110">Implementing IMFAttributes</span></span>](#implementing-imfattributes)
-   [<span data-ttu-id="1d1f3-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1d1f3-111">Related topics</span></span>](#related-topics)

## <a name="about-attributes"></a><span data-ttu-id="1d1f3-112">Présentation des attributs</span><span class="sxs-lookup"><span data-stu-id="1d1f3-112">About Attributes</span></span>

<span data-ttu-id="1d1f3-113">Un attribut est une paire clé/valeur, où la clé est un GUID et la valeur est un **PROPVARIANT**.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-113">An attribute is a key/value pair, where the key is a GUID and the value is a **PROPVARIANT**.</span></span> <span data-ttu-id="1d1f3-114">Les valeurs d’attribut sont limitées aux types de données suivants :</span><span class="sxs-lookup"><span data-stu-id="1d1f3-114">Attribute values are restricted to the following data types:</span></span>

-   <span data-ttu-id="1d1f3-115">Entier non signé 32 bits (**UInt32**).</span><span class="sxs-lookup"><span data-stu-id="1d1f3-115">Unsigned 32-bit integer (**UINT32**).</span></span>
-   <span data-ttu-id="1d1f3-116">Entier non signé 64 bits (**UINT64**).</span><span class="sxs-lookup"><span data-stu-id="1d1f3-116">Unsigned 64-bit integer (**UINT64**).</span></span>
-   <span data-ttu-id="1d1f3-117">nombre à virgule flottante 64 bits.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-117">64-bit floating-point number.</span></span>
-   <span data-ttu-id="1d1f3-118">GUID (identificateur global unique).</span><span class="sxs-lookup"><span data-stu-id="1d1f3-118">GUID.</span></span>
-   <span data-ttu-id="1d1f3-119">Chaîne à caractères larges se terminant par le caractère Null.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-119">Null-terminated wide-character string.</span></span>
-   <span data-ttu-id="1d1f3-120">Tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-120">Byte array.</span></span>
-   <span data-ttu-id="1d1f3-121">Pointeur **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="1d1f3-121">**IUnknown** pointer.</span></span>

<span data-ttu-id="1d1f3-122">Ces types sont définis dans l’énumération de [**\_ \_ type d’attribut MF**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type) .</span><span class="sxs-lookup"><span data-stu-id="1d1f3-122">These types are defined in the [**MF\_ATTRIBUTE\_TYPE**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type) enumeration.</span></span> <span data-ttu-id="1d1f3-123">Pour définir ou récupérer des valeurs d’attribut, utilisez l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="1d1f3-123">To set or retrieve attribute values, use the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="1d1f3-124">Cette interface contient des méthodes de type sécurisé pour récupérer et définir des valeurs par type de données.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-124">This interface contains type-safe methods to get and set values by data type.</span></span> <span data-ttu-id="1d1f3-125">Par exemple, pour définir un entier 32 bits, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="1d1f3-125">For example, to set a 32-bit integer, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span> <span data-ttu-id="1d1f3-126">Les clés d’attribut sont uniques au sein d’un objet.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-126">Attribute keys are unique within an object.</span></span> <span data-ttu-id="1d1f3-127">Si vous définissez deux valeurs différentes avec la même clé, la deuxième valeur remplace la première.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-127">If you set two different values with the same key, the second value overwrites the first.</span></span>

<span data-ttu-id="1d1f3-128">Plusieurs interfaces Media Foundation héritent de l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="1d1f3-128">Several Media Foundation interfaces inherit the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="1d1f3-129">Les objets qui exposent cette interface ont des attributs facultatifs ou obligatoires que l’application doit définir sur l’objet, ou avoir des attributs que l’application peut récupérer.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-129">Objects that expose this interface have optional or mandatory attributes that the application should set on the object, or have attributes that the application can retrieve.</span></span> <span data-ttu-id="1d1f3-130">En outre, certaines méthodes et fonctions prennent un pointeur **IMFAttributes** comme paramètre, ce qui permet à l’application de définir des informations de configuration.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-130">Also, some methods and functions take an **IMFAttributes** pointer as a parameter, which enables the application to set configuration information.</span></span> <span data-ttu-id="1d1f3-131">L’application doit créer un magasin d’attributs pour stocker les attributs de configuration.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-131">The application must create an attribute store to hold the configuration attributes.</span></span> <span data-ttu-id="1d1f3-132">Pour créer un magasin d’attributs vide, appelez [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span><span class="sxs-lookup"><span data-stu-id="1d1f3-132">To create an empty attribute store, call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>

<span data-ttu-id="1d1f3-133">Le code suivant illustre deux fonctions.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-133">The following code shows two functions.</span></span> <span data-ttu-id="1d1f3-134">La première crée un nouveau magasin d’attributs et définit un attribut hypothétique nommé MY \_ attribute avec une valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-134">The first creates a new attribute store and sets a hypothetical attribute named MY\_ATTRIBUTE with a string value.</span></span> <span data-ttu-id="1d1f3-135">La deuxième fonction récupère la valeur de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-135">The second function retrieves the value of this attribute.</span></span>


```C++
extern const GUID MY_ATTRIBUTE;

HRESULT ShowCreateAttributeStore(IMFAttributes **ppAttributes)
{
    IMFAttributes *pAttributes = NULL;
    const UINT32 cElements = 10;  // Starting size.

    // Create the empty attribute store.
    HRESULT hr = MFCreateAttributes(&pAttributes, cElements);

    // Set the MY_ATTRIBUTE attribute with a string value.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MY_ATTRIBUTE,
            L"This is a string value"
            );
    }

    // Return the IMFAttributes pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }

    SAFE_RELEASE(pAttributes);

    return hr;
}

HRESULT ShowGetAttributes()
{
    IMFAttributes *pAttributes = NULL;
    WCHAR *pwszValue = NULL;
    UINT32 cchLength = 0;

    // Create the attribute store.
    HRESULT hr = ShowCreateAttributeStore(&pAttributes);

    // Get the attribute.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->GetAllocatedString(
            MY_ATTRIBUTE,
            &pwszValue,
            &cchLength
            );
    }

    CoTaskMemFree(pwszValue);
    SAFE_RELEASE(pAttributes);

    return hr;
}
```



<span data-ttu-id="1d1f3-136">Pour obtenir la liste complète des attributs de Media Foundation, consultez [Media Foundation attributs](media-foundation-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="1d1f3-136">For a complete list of Media Foundation attributes, see [Media Foundation Attributes](media-foundation-attributes.md).</span></span> <span data-ttu-id="1d1f3-137">Le type de données attendu pour chaque attribut est documenté ici.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-137">The expected data type for each attribute is documented there.</span></span>

## <a name="serializing-attributes"></a><span data-ttu-id="1d1f3-138">Sérialisation des attributs</span><span class="sxs-lookup"><span data-stu-id="1d1f3-138">Serializing Attributes</span></span>

<span data-ttu-id="1d1f3-139">Media Foundation a deux fonctions pour sérialiser des magasins d’attributs.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-139">Media Foundation has two functions for serializing attribute stores.</span></span> <span data-ttu-id="1d1f3-140">L’une écrit les attributs dans un tableau d’octets, l’autre les écrit dans un flux qui prend en charge l’interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="1d1f3-140">One writes the attributes to a byte array, the other writes them to a stream that supports the **IStream** interface.</span></span> <span data-ttu-id="1d1f3-141">Chaque fonction a une fonction correspondante qui charge les données.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-141">Each function has a corresponding function that loads the data.</span></span>



| <span data-ttu-id="1d1f3-142">Opération</span><span class="sxs-lookup"><span data-stu-id="1d1f3-142">Operation</span></span> | <span data-ttu-id="1d1f3-143">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="1d1f3-143">Byte Array</span></span>                                                   | <span data-ttu-id="1d1f3-144">IStream</span><span class="sxs-lookup"><span data-stu-id="1d1f3-144">IStream</span></span>                                                                        |
|-----------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="1d1f3-145">Enregistrer</span><span class="sxs-lookup"><span data-stu-id="1d1f3-145">Save</span></span>      | [<span data-ttu-id="1d1f3-146">**MFGetAttributesAsBlob**</span><span class="sxs-lookup"><span data-stu-id="1d1f3-146">**MFGetAttributesAsBlob**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob)       | [<span data-ttu-id="1d1f3-147">**MFSerializeAttributesToStream**</span><span class="sxs-lookup"><span data-stu-id="1d1f3-147">**MFSerializeAttributesToStream**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream)         |
| <span data-ttu-id="1d1f3-148">Load</span><span class="sxs-lookup"><span data-stu-id="1d1f3-148">Load</span></span>      | [<span data-ttu-id="1d1f3-149">**MFInitAttributesFromBlob**</span><span class="sxs-lookup"><span data-stu-id="1d1f3-149">**MFInitAttributesFromBlob**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfinitattributesfromblob) | [<span data-ttu-id="1d1f3-150">**MFDeserializeAttributesFromStream**</span><span class="sxs-lookup"><span data-stu-id="1d1f3-150">**MFDeserializeAttributesFromStream**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-mfdeserializeattributesfromstream) |



 

<span data-ttu-id="1d1f3-151">Pour écrire le contenu d’un magasin d’attributs dans un tableau d’octets, appelez [**MFGetAttributesAsBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob).</span><span class="sxs-lookup"><span data-stu-id="1d1f3-151">To write the contents of an attribute store into a byte array, call [**MFGetAttributesAsBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob).</span></span> <span data-ttu-id="1d1f3-152">Les attributs avec des valeurs de pointeur **IUnknown** sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-152">Attributes with **IUnknown** pointer values are ignored.</span></span> <span data-ttu-id="1d1f3-153">Pour charger les attributs dans un magasin d’attributs, appelez [**MFInitAttributesFromBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfinitattributesfromblob).</span><span class="sxs-lookup"><span data-stu-id="1d1f3-153">To load the attributes back into an attribute store, call [**MFInitAttributesFromBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfinitattributesfromblob).</span></span>

<span data-ttu-id="1d1f3-154">Pour écrire un magasin d’attributs dans un flux, appelez [**MFSerializeAttributesToStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream).</span><span class="sxs-lookup"><span data-stu-id="1d1f3-154">To write an attribute store to a stream, call [**MFSerializeAttributesToStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream).</span></span> <span data-ttu-id="1d1f3-155">Cette fonction peut marshaler des valeurs de pointeur **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="1d1f3-155">This function can marshal **IUnknown** pointer values.</span></span> <span data-ttu-id="1d1f3-156">L’appelant doit fournir un objet de flux qui implémente l’interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="1d1f3-156">The caller must provide a stream object that implements the **IStream** interface.</span></span> <span data-ttu-id="1d1f3-157">Pour charger un magasin d’attributs à partir d’un flux, appelez [**MFDeserializeAttributesFromStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfdeserializeattributesfromstream).</span><span class="sxs-lookup"><span data-stu-id="1d1f3-157">To load an attribute store from a stream, call [**MFDeserializeAttributesFromStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfdeserializeattributesfromstream).</span></span>

## <a name="implementing-imfattributes"></a><span data-ttu-id="1d1f3-158">Implémentation de IMFAttributes</span><span class="sxs-lookup"><span data-stu-id="1d1f3-158">Implementing IMFAttributes</span></span>

<span data-ttu-id="1d1f3-159">Media Foundation fournit une implémentation stockée de [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), qui est obtenue en appelant la fonction [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .</span><span class="sxs-lookup"><span data-stu-id="1d1f3-159">Media Foundation provides a stock implementation of [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), which is obtained by calling the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function.</span></span> <span data-ttu-id="1d1f3-160">Dans la plupart des cas, vous devez utiliser cette implémentation et ne pas fournir votre propre implémentation personnalisée.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-160">In most situations, you should use this implementation, and not provide your own custom implementation.</span></span>

<span data-ttu-id="1d1f3-161">Il existe une situation dans laquelle vous devrez peut-être implémenter l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) : Si vous implémentez une deuxième interface qui hérite de **IMFAttributes**.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-161">There is one situation when you might need to implement the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface: If you implement a second interface that inherits **IMFAttributes**.</span></span> <span data-ttu-id="1d1f3-162">Dans ce cas, vous devez fournir des implémentations pour les méthodes **IMFAttributes** héritées par la deuxième interface.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-162">In that case, you must provide implementations for the **IMFAttributes** methods inherited by the second interface.</span></span>

<span data-ttu-id="1d1f3-163">Dans ce cas, il est recommandé d’encapsuler l’implémentation Media Foundation existante de [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span><span class="sxs-lookup"><span data-stu-id="1d1f3-163">In this situation, it is recommended to wrap the existing Media Foundation implementation of [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span> <span data-ttu-id="1d1f3-164">Le code suivant illustre un modèle de classe qui contient un pointeur **IMFAttributes** et encapsule chaque méthode **IMFAttributes** , à l’exception des méthodes **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="1d1f3-164">The following code shows a class template that holds an **IMFAttributes** pointer and wraps every **IMFAttributes** method, except for the **IUnknown** methods.</span></span>


```C++
#include <assert.h>

// Helper class to implement IMFAttributes. 

// This is an abstract class; the derived class must implement the IUnknown 
// methods. This class is a wrapper for the standard attribute store provided 
// in Media Foundation.

// template parameter: 
// The interface you are implementing, either IMFAttributes or an interface 
// that inherits IMFAttributes, such as IMFActivate

template <class IFACE=IMFAttributes>
class CBaseAttributes : public IFACE
{
protected:
    IMFAttributes *m_pAttributes;

    // This version of the constructor does not initialize the 
    // attribute store. The derived class must call Initialize() in 
    // its own constructor.
    CBaseAttributes() : m_pAttributes(NULL)
    {
    }

    // This version of the constructor initializes the attribute 
    // store, but the derived class must pass an HRESULT parameter 
    // to the constructor.

    CBaseAttributes(HRESULT& hr, UINT32 cInitialSize = 0) : m_pAttributes(NULL)
    {
        hr = Initialize(cInitialSize);
    }

    // The next version of the constructor uses a caller-provided 
    // implementation of IMFAttributes.

    // (Sometimes you want to delegate IMFAttributes calls to some 
    // other object that implements IMFAttributes, rather than using 
    // MFCreateAttributes.)

    CBaseAttributes(HRESULT& hr, IUnknown *pUnk)
    {
        hr = Initialize(pUnk);
    }

    virtual ~CBaseAttributes()
    {
        if (m_pAttributes)
        {
            m_pAttributes->Release();
        }
    }

    // Initializes the object by creating the standard Media Foundation attribute store.
    HRESULT Initialize(UINT32 cInitialSize = 0)
    {
        if (m_pAttributes == NULL)
        {
            return MFCreateAttributes(&m_pAttributes, cInitialSize); 
        }
        else
        {
            return S_OK;
        }
    }

    // Initializes this object from a caller-provided attribute store.
    // pUnk: Pointer to an object that exposes IMFAttributes.
    HRESULT Initialize(IUnknown *pUnk)
    {
        if (m_pAttributes)
        {
            m_pAttributes->Release();
            m_pAttributes = NULL;
        }


        return pUnk->QueryInterface(IID_PPV_ARGS(&m_pAttributes));
    }

public:

    // IMFAttributes methods

    STDMETHODIMP GetItem(REFGUID guidKey, PROPVARIANT* pValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetItem(guidKey, pValue);
    }

    STDMETHODIMP GetItemType(REFGUID guidKey, MF_ATTRIBUTE_TYPE* pType)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetItemType(guidKey, pType);
    }

    STDMETHODIMP CompareItem(REFGUID guidKey, REFPROPVARIANT Value, BOOL* pbResult)
    {
        assert(m_pAttributes);
        return m_pAttributes->CompareItem(guidKey, Value, pbResult);
    }

    STDMETHODIMP Compare(
        IMFAttributes* pTheirs, 
        MF_ATTRIBUTES_MATCH_TYPE MatchType, 
        BOOL* pbResult
        )
    {
        assert(m_pAttributes);
        return m_pAttributes->Compare(pTheirs, MatchType, pbResult);
    }

    STDMETHODIMP GetUINT32(REFGUID guidKey, UINT32* punValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetUINT32(guidKey, punValue);
    }

    STDMETHODIMP GetUINT64(REFGUID guidKey, UINT64* punValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetUINT64(guidKey, punValue);
    }

    STDMETHODIMP GetDouble(REFGUID guidKey, double* pfValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetDouble(guidKey, pfValue);
    }

    STDMETHODIMP GetGUID(REFGUID guidKey, GUID* pguidValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetGUID(guidKey, pguidValue);
    }

    STDMETHODIMP GetStringLength(REFGUID guidKey, UINT32* pcchLength)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetStringLength(guidKey, pcchLength);
    }

    STDMETHODIMP GetString(REFGUID guidKey, LPWSTR pwszValue, UINT32 cchBufSize, UINT32* pcchLength)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetString(guidKey, pwszValue, cchBufSize, pcchLength);
    }

    STDMETHODIMP GetAllocatedString(REFGUID guidKey, LPWSTR* ppwszValue, UINT32* pcchLength)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetAllocatedString(guidKey, ppwszValue, pcchLength);
    }

    STDMETHODIMP GetBlobSize(REFGUID guidKey, UINT32* pcbBlobSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetBlobSize(guidKey, pcbBlobSize);
    }

    STDMETHODIMP GetBlob(REFGUID guidKey, UINT8* pBuf, UINT32 cbBufSize, UINT32* pcbBlobSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetBlob(guidKey, pBuf, cbBufSize, pcbBlobSize);
    }

    STDMETHODIMP GetAllocatedBlob(REFGUID guidKey, UINT8** ppBuf, UINT32* pcbSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetAllocatedBlob(guidKey, ppBuf, pcbSize);
    }

    STDMETHODIMP GetUnknown(REFGUID guidKey, REFIID riid, LPVOID* ppv)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetUnknown(guidKey, riid, ppv);
    }

    STDMETHODIMP SetItem(REFGUID guidKey, REFPROPVARIANT Value)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetItem(guidKey, Value);
    }

    STDMETHODIMP DeleteItem(REFGUID guidKey)
    {
        assert(m_pAttributes);
        return m_pAttributes->DeleteItem(guidKey);
    }

    STDMETHODIMP DeleteAllItems()
    {
        assert(m_pAttributes);
        return m_pAttributes->DeleteAllItems();
    }

    STDMETHODIMP SetUINT32(REFGUID guidKey, UINT32 unValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetUINT32(guidKey, unValue);
    }

    STDMETHODIMP SetUINT64(REFGUID guidKey,UINT64 unValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetUINT64(guidKey, unValue);
    }

    STDMETHODIMP SetDouble(REFGUID guidKey, double fValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetDouble(guidKey, fValue);
    }

    STDMETHODIMP SetGUID(REFGUID guidKey, REFGUID guidValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetGUID(guidKey, guidValue);
    }

    STDMETHODIMP SetString(REFGUID guidKey, LPCWSTR wszValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetString(guidKey, wszValue);
    }

    STDMETHODIMP SetBlob(REFGUID guidKey, const UINT8* pBuf, UINT32 cbBufSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetBlob(guidKey, pBuf, cbBufSize);
    }

    STDMETHODIMP SetUnknown(REFGUID guidKey, IUnknown* pUnknown)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetUnknown(guidKey, pUnknown);
    }

    STDMETHODIMP LockStore()
    {
        assert(m_pAttributes);
        return m_pAttributes->LockStore();
    }

    STDMETHODIMP UnlockStore()
    {
        assert(m_pAttributes);
        return m_pAttributes->UnlockStore();
    }

    STDMETHODIMP GetCount(UINT32* pcItems)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetCount(pcItems);
    }

    STDMETHODIMP GetItemByIndex(UINT32 unIndex, GUID* pguidKey, PROPVARIANT* pValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetItemByIndex(unIndex, pguidKey, pValue);
    }

    STDMETHODIMP CopyAllItems(IMFAttributes* pDest)
    {
        assert(m_pAttributes);
        return m_pAttributes->CopyAllItems(pDest);
    }

    // Helper functions
    
    HRESULT SerializeToStream(DWORD dwOptions, IStream* pStm)      
        // dwOptions: Flags from MF_ATTRIBUTE_SERIALIZE_OPTIONS
    {
        assert(m_pAttributes);
        return MFSerializeAttributesToStream(m_pAttributes, dwOptions, pStm);
    }

    HRESULT DeserializeFromStream(DWORD dwOptions, IStream* pStm)
    {
        assert(m_pAttributes);
        return MFDeserializeAttributesFromStream(m_pAttributes, dwOptions, pStm);
    }

    // SerializeToBlob: Stores the attributes in a byte array. 
    // 
    // ppBuf: Receives a pointer to the byte array. 
    // pcbSize: Receives the size of the byte array.
    //
    // The caller must free the array using CoTaskMemFree.
    HRESULT SerializeToBlob(UINT8 **ppBuffer, UINT32 *pcbSize)
    {
        assert(m_pAttributes);

        if (ppBuffer == NULL)
        {
            return E_POINTER;
        }
        if (pcbSize == NULL)
        {
            return E_POINTER;
        }

        *ppBuffer = NULL;
        *pcbSize = 0;

        UINT32 cbSize = 0;
        BYTE *pBuffer = NULL;

        HRESULT hr = MFGetAttributesAsBlobSize(m_pAttributes, &cbSize);

        if (FAILED(hr))
        {
            return hr;
        }

        pBuffer = (BYTE*)CoTaskMemAlloc(cbSize);
        if (pBuffer == NULL)
        {
            return E_OUTOFMEMORY;
        }

        hr = MFGetAttributesAsBlob(m_pAttributes, pBuffer, cbSize);

        if (SUCCEEDED(hr))
        {
            *ppBuffer = pBuffer;
            *pcbSize = cbSize;
        }
        else
        {
            CoTaskMemFree(pBuffer);
        }
        return hr;
    }
    
    HRESULT DeserializeFromBlob(const UINT8* pBuffer, UINT cbSize)
    {
        assert(m_pAttributes);
        return MFInitAttributesFromBlob(m_pAttributes, pBuffer, cbSize);
    }

    HRESULT GetRatio(REFGUID guidKey, UINT32* pnNumerator, UINT32* punDenominator)
    {
        assert(m_pAttributes);
        return MFGetAttributeRatio(m_pAttributes, guidKey, pnNumerator, punDenominator);
    }

    HRESULT SetRatio(REFGUID guidKey, UINT32 unNumerator, UINT32 unDenominator)
    {
        assert(m_pAttributes);
        return MFSetAttributeRatio(m_pAttributes, guidKey, unNumerator, unDenominator);
    }

    // Gets an attribute whose value represents the size of something (eg a video frame).
    HRESULT GetSize(REFGUID guidKey, UINT32* punWidth, UINT32* punHeight)
    {
        assert(m_pAttributes);
        return MFGetAttributeSize(m_pAttributes, guidKey, punWidth, punHeight);
    }

    // Sets an attribute whose value represents the size of something (eg a video frame).
    HRESULT SetSize(REFGUID guidKey, UINT32 unWidth, UINT32 unHeight)
    {
        assert(m_pAttributes);
        return MFSetAttributeSize (m_pAttributes, guidKey, unWidth, unHeight);
    }
};
```



<span data-ttu-id="1d1f3-165">Le code suivant montre comment dériver une classe à partir de ce modèle :</span><span class="sxs-lookup"><span data-stu-id="1d1f3-165">The following code shows how to derive a class from this template:</span></span>


```C++
#include <shlwapi.h>

class MyObject : public CBaseAttributes<>
{
    MyObject() : m_nRefCount(1) { }
    ~MyObject() { }

    long m_nRefCount;

public:

    // IUnknown
    STDMETHODIMP MyObject::QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(MyObject, IMFAttributes),
            { 0 },
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) MyObject::AddRef()
    {
        return InterlockedIncrement(&m_nRefCount);
    }

    STDMETHODIMP_(ULONG) MyObject::Release()
    {
        ULONG uCount = InterlockedDecrement(&m_nRefCount);
        if (uCount == 0)
        {
            delete this;
        }
        return uCount;
    }

    // Static function to create an instance of the object.

    static HRESULT CreateInstance(MyObject **ppObject)
    {
        HRESULT hr = S_OK;

        MyObject *pObject = new MyObject();
        if (pObject == NULL)
        {
            return E_OUTOFMEMORY;
        }

        // Initialize the attribute store.
        hr = pObject->Initialize();

        if (FAILED(hr))
        {
            delete pObject;
            return hr;
        }

        *ppObject = pObject;
        (*ppObject)->AddRef();

        return S_OK;
    }
};
```



<span data-ttu-id="1d1f3-166">Vous devez appeler `CBaseAttributes::Initialize` pour créer le magasin d’attributs.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-166">You must call `CBaseAttributes::Initialize` to create the attribute store.</span></span> <span data-ttu-id="1d1f3-167">Dans l’exemple précédent, cela se fait à l’intérieur d’une fonction de création statique.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-167">In the previous example, that is done inside a static creation function.</span></span>

<span data-ttu-id="1d1f3-168">L’argument template est un type interface, qui a comme valeur par défaut [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span><span class="sxs-lookup"><span data-stu-id="1d1f3-168">The template argument is an interface type, which defaults to [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span> <span data-ttu-id="1d1f3-169">Si votre objet implémente une interface qui hérite de **IMFAttributes**, telle que [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate), définissez l’argument de modèle sur le nom de l’interface dérivée.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-169">If your object implements an interface that inherits **IMFAttributes**, such as [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate), set the template argument equal to name of the derived interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d1f3-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1d1f3-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d1f3-171">Primitives de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1d1f3-171">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



