---
description: Reconnexion de votre entrée pour garantir des types de sortie spécifiques
ms.assetid: c83d002e-59bf-4d03-9917-e39ceab9a4ce
title: Reconnexion de votre entrée pour garantir des types de sortie spécifiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d74d6914989231542ddfea9f97e93ce860d34eb4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392516"
---
# <a name="reconnecting-your-input-to-ensure-specific-output-types"></a><span data-ttu-id="973ea-103">Reconnexion de votre entrée pour garantir des types de sortie spécifiques</span><span class="sxs-lookup"><span data-stu-id="973ea-103">Reconnecting Your Input to Ensure Specific Output Types</span></span>

<span data-ttu-id="973ea-104">Les filtres implémentent la méthode [**IAMStreamConfig :: SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) pour définir le format audio ou vidéo avant que les broches du filtre soient connectées.</span><span class="sxs-lookup"><span data-stu-id="973ea-104">Filters implement the [**IAMStreamConfig::SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) method to set the audio or video format before the filter's pins are connected.</span></span> <span data-ttu-id="973ea-105">Si votre code confidentiel de sortie est déjà connecté et que vous pouvez fournir un nouveau type, reconnectez votre code confidentiel, mais uniquement si l’autre filtre peut accepter le nouveau type.</span><span class="sxs-lookup"><span data-stu-id="973ea-105">If your output pin is already connected and you can provide a new type, then reconnect your pin, but only if the other filter can accept the new type.</span></span> <span data-ttu-id="973ea-106">Si l’autre filtre ne peut pas accepter le type de média, échouez l’appel à **SetFormat** et laissez votre connexion seule.</span><span class="sxs-lookup"><span data-stu-id="973ea-106">If the other filter cannot accept the media type, fail the call to **SetFormat** and leave your connection alone.</span></span>

<span data-ttu-id="973ea-107">Un filtre de transformation ne peut pas avoir de types de sortie préférés, sauf si leur broche d’entrée est connectée.</span><span class="sxs-lookup"><span data-stu-id="973ea-107">A transform filter may not have any preferred output types unless their input pin is connected.</span></span> <span data-ttu-id="973ea-108">Dans ce cas, les méthodes **SetFormat** et [**IAMStreamConfig :: GETSTREAMCAPS**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) doivent retourner VFW \_ E \_ non \_ connecté jusqu’à ce que la broche d’entrée soit connectée.</span><span class="sxs-lookup"><span data-stu-id="973ea-108">In that case, the **SetFormat** and [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) methods should return VFW\_E\_NOT\_CONNECTED until the input pin is connected.</span></span> <span data-ttu-id="973ea-109">Dans le cas contraire, ces méthodes peuvent fonctionner comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="973ea-109">Otherwise, these methods can function as usual.</span></span>

<span data-ttu-id="973ea-110">Dans certains cas, il est utile de reconnecter les broches quand vous offrez un format sur une connexion établie.</span><span class="sxs-lookup"><span data-stu-id="973ea-110">In certain cases it is useful to reconnect pins when you are offering a format on an established connection.</span></span> <span data-ttu-id="973ea-111">Par exemple, supposez qu’un filtre peut compresser une vidéo RGB de 24 bits dans le format X, et qu’il peut compresser une vidéo RGB 8 bits dans le format Y. La broche de sortie peut effectuer l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="973ea-111">For example, suppose that a filter can compress 24-bit RGB video into format X, and that it can compress 8-bit RGB video into format Y. The output pin can do either of the following:</span></span>

-   <span data-ttu-id="973ea-112">Offrez toujours X et Y dans **GetStreamCaps** et acceptez toujours x et y dans **SetFormat**.</span><span class="sxs-lookup"><span data-stu-id="973ea-112">Always offer both X and Y in **GetStreamCaps**, and always accept both X and Y in **SetFormat**.</span></span>
-   <span data-ttu-id="973ea-113">Offre et accepte uniquement le format X si le type d’entrée est une couleur RVB de 24 bits.</span><span class="sxs-lookup"><span data-stu-id="973ea-113">Offer and accept just format X if the input type is 24-bit RGB.</span></span> <span data-ttu-id="973ea-114">Offre et accepte uniquement le format Y si le type d’entrée est de type RGB 8 bits.</span><span class="sxs-lookup"><span data-stu-id="973ea-114">Offer and accept just format Y if the input type 8-bit RGB.</span></span> <span data-ttu-id="973ea-115">Les deux méthodes échouent si la broche d’entrée n’est pas connectée.</span><span class="sxs-lookup"><span data-stu-id="973ea-115">Fail both methods if the input pin is not connected.</span></span>

<span data-ttu-id="973ea-116">Dans les deux cas, vous aurez besoin d’un code de reconnexion qui ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="973ea-116">In either case, you will need some reconnecting code that looks like this:</span></span>


```C++
HRESULT MyOutputPin::CheckMediaType(const CMediaType *pmtOut)
{
    // Fail if the input pin is not connected.
    if (!m_pFilter->m_pInput->IsConnected()) {
        return VFW_E_NOT_CONNECTED;
    }

    // (Not shown: Reject any media types that you know in advance your 
    // filter cannot use. Check the major type and subtype GUIDs.)

    // (Not shown: If SetFormat was previously called, check whether
    // pmtOut exactly matches the format that was specified in SetFormat.
    // Return S_OK if they match, or VFW_E_INVALIDMEDIATYPE otherwise.)
   
    // Now do the normal check for this media type.
    HRESULT hr;
    hr = m_pFilter->CheckTransform(
        &m_pFilter->m_pInput->CurrentMediaType(),  // The input type.
        pmtOut  // The proposed output type.
    );
    if (hr == S_OK)
    {
        // This format is compatible with the current input type.
        return S_OK;
    }
 
    // This format is not compatible with the current input type. 
    // Maybe we can reconnect the input pin with a new input type.
    
    // Enumerate the upstream filter's preferred output types, and 
    // see if one of them will work.
    CMediaType *pmtEnum;
    BOOL fFound = FALSE;
    IEnumMediaTypes *pEnum;
    hr = m_pFilter->m_pInput->GetConnected()->EnumMediaTypes(&pEnum);
    if (hr != S_OK)
    {
        return E_FAIL;
    }
    while (hr = pEnum->Next(1, (AM_MEDIA_TYPE **)&pmtEnum, NULL), hr == S_OK)
    {
        // Check this input type against the proposed output type.
        hr = m_pFilter->CheckTransform(pmtEnum, pmtOut);
        if (hr != S_OK) 
        {
            DeleteMediaType(pmtEnum);
            continue; // Try the next one.
        }

        // This input type is a possible candidate. But, we have to make
        // sure that the upstream filter can switch to this type. 
        hr = m_pFilter->m_pInput->GetConnected()->QueryAccept(pmtEnum);
        if (hr != S_OK) 
        {
            // The upstream filter will not switch to this type.
            DeleteMediaType(pmtEnum);
            continue; // Try the next one.
        }
        fFound = TRUE;
        DeleteMediaType(pmtEnum);
        break;
    }
    pEnum->Release();

    if (fFound)
    {
        // This output type is OK, but if we are asked to use it, we will
        // need to reconnect our input pin. (See SetFormat, below.)
        return S_OK;
    }
    else
    {
        return VFW_E_INVALIDMEDIATYPE;
    }
}

HRESULT MyOutputPin::SetFormat(AM_MEDIA_TYPE *pmt)
{
    CheckPointer(pmt, E_POINTER);
    HRESULT hr;

    // Hold the filter state lock, to make sure that streaming isn't 
    // in the middle of starting or stopping:
    CAutoLock cObjectLock(&m_pFilter->m_csFilter);

    // Cannot set the format unless the filter is stopped.
    if (m_pFilter->m_State != State_Stopped)
    {
        return VFW_E_NOT_STOPPED;
    }

    // The set of possible output formats depends on the input format,
    // so if the input pin is not connected, return a failure code.
    if (!m_pFilter->m_pInput->IsConnected())
    {
        return VFW_E_NOT_CONNECTED;
    }

    // If the pin is already using this format, there's nothing to do.
    if (IsConnected() && CurrentMediaType() == *pmt)
    {
        return S_OK;
    }

    // See if this media type is acceptable.
    if ((hr = CheckMediaType((CMediaType *)pmt)) != S_OK) 
    {
        return hr;
    }

    // If we're connected to a downstream filter, we have to make
    // sure that the downstream filter accepts this media type.
    if (IsConnected()) 
    {
        hr = GetConnected()->QueryAccept(pmt);
        if (hr != S_OK)
        {
            return VFW_E_INVALIDMEDIATYPE;
        }
    }

    // Now make a note that from now on, this is the only format allowed,
    // and refuse anything but this in the CheckMediaType code above.

    // Changing the format means reconnecting if necessary.
    if (IsConnected())
    {
        m_pFilter->m_pGraph->Reconnect(this);
    }

    return NOERROR;
}


// Override CTransformFilter::SetMediaType to reconnect the input pin. 
// This method is called immediately after the media type is set on a pin.
HRESULT MyFilter::SetMediaType(
    PIN_DIRECTION direction, 
    const CMediaType *pmt
)
{
    HRESULT hr;
    if (direction == PINDIR_OUTPUT) 
    {
        // Before we set the output type, we might need to reconnect 
        // the input pin with a new type.
        if (m_pInput && m_pInput->IsConnected()) 
        {
            // Check if the current input type is compatible.
            hr = CheckTransform(
                    &m_pInput->CurrentMediaType(),
                    &m_pOutput->CurrentMediaType());
            if (SUCCEEDED(hr))
            {
                return S_OK;
            }
            // Otherwise, we need to reconnect the input pin.
            // Note: The CheckMediaType method has already called 
            // QueryAccept on the upstream filter. 
            hr = m_pGraph->Reconnect(m_pInput);
            return hr;
        }
    }
    return S_OK;
}
```



 

 



