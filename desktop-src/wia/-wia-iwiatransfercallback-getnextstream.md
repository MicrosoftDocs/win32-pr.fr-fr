---
description: Obtient un nouveau flux pour l’élément spécifié.
ms.assetid: fe25843c-2051-42fe-8737-eea39f6aeab9
title: 'IWiaTransferCallback :: GetNextStream, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.GetNextStream
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: fb2e92c9cade1dfd48efc3051b617997bf8473e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514628"
---
# <a name="iwiatransfercallbackgetnextstream-method"></a><span data-ttu-id="d862d-103">IWiaTransferCallback :: GetNextStream, méthode</span><span class="sxs-lookup"><span data-stu-id="d862d-103">IWiaTransferCallback::GetNextStream method</span></span>

<span data-ttu-id="d862d-104">Obtient un nouveau flux pour l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="d862d-104">Gets a new stream for the specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="d862d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d862d-105">Syntax</span></span>


```C++
HRESULT GetNextStream(
  [in]  LONG    lFlags,
  [in]  BSTR    bstrItemName,
  [in]  BSTR    bstrFullItemName,
  [out] IStream **ppDestination
);
```



## <a name="parameters"></a><span data-ttu-id="d862d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d862d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d862d-107">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d862d-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d862d-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="d862d-108">Type: **LONG**</span></span>

<span data-ttu-id="d862d-109">Actuellement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d862d-109">Currently unused.</span></span> <span data-ttu-id="d862d-110">Doit être défini sur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="d862d-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="d862d-111">*bstrItemName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d862d-111">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d862d-112">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d862d-112">Type: **BSTR**</span></span>

<span data-ttu-id="d862d-113">Spécifie le nom de l’élément pour lequel créer un flux.</span><span class="sxs-lookup"><span data-stu-id="d862d-113">Specifies the name of the item to create stream for.</span></span>

</dd> <dt>

<span data-ttu-id="d862d-114">*bstrFullItemName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d862d-114">*bstrFullItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d862d-115">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d862d-115">Type: **BSTR**</span></span>

<span data-ttu-id="d862d-116">Spécifie le nom complet de l’élément pour lequel créer un flux.</span><span class="sxs-lookup"><span data-stu-id="d862d-116">Specifies the full name of the item to create stream for.</span></span>

</dd> <dt>

<span data-ttu-id="d862d-117">*ppDestination* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d862d-117">*ppDestination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d862d-118">Type : **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\*\***</span><span class="sxs-lookup"><span data-stu-id="d862d-118">Type: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\*\***</span></span>

<span data-ttu-id="d862d-119">Reçoit l’adresse d’un pointeur vers le nouvel objet [IStream](/windows/win32/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="d862d-119">Receives the address of a pointer to the new [IStream](/windows/win32/api/objidl/nn-objidl-istream) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d862d-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d862d-120">Return value</span></span>

<span data-ttu-id="d862d-121">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d862d-121">Type: **HRESULT**</span></span>

<span data-ttu-id="d862d-122">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d862d-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d862d-123">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d862d-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d862d-124">Notes</span><span class="sxs-lookup"><span data-stu-id="d862d-124">Remarks</span></span>

<span data-ttu-id="d862d-125">Lorsque cette méthode est implémentée par un filtre de traitement d’image, le minipilote WIA (Windows Image Acquisition) 2,0 l’appelle lors de l’acquisition d’images pour récupérer le flux de destination à partir du client.</span><span class="sxs-lookup"><span data-stu-id="d862d-125">When this method is implemented by an image processing filter, the Windows Image Acquisition (WIA) 2.0 minidriver calls it during image acquisition to get the destination stream from the client.</span></span>

<span data-ttu-id="d862d-126">**IWiaTransferCallback :: GetNextStream** d’un filtre doit déléguer à la méthode de rappel de l’application.</span><span class="sxs-lookup"><span data-stu-id="d862d-126">A filter's **IWiaTransferCallback::GetNextStream** must delegate to the application's callback method.</span></span> <span data-ttu-id="d862d-127">Le filtre utilise le flux retourné par l’implémentation **IWiaTransferCallback :: GetNextStream** du rappel d’application pour créer son propre flux qu’il transmet au service WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="d862d-127">The filter uses the stream returned by the application callback's **IWiaTransferCallback::GetNextStream** implementation to create its own stream that it passes back to the WIA 2.0 service.</span></span> <span data-ttu-id="d862d-128">Le filtrage est effectué lorsque le flux du filtre appelle la méthode [IStream :: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) .</span><span class="sxs-lookup"><span data-stu-id="d862d-128">The filtering is done when the filter's stream calls the [IStream::Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) method.</span></span>

<span data-ttu-id="d862d-129">Le flux du filtre ne peut pas faire d’hypothèses sur le nombre d’octets qui y sont écrits à chaque écriture, car les données d’image non filtrées peuvent provenir du composant WIA 2,0 Preview et non du pilote.</span><span class="sxs-lookup"><span data-stu-id="d862d-129">The filter's stream cannot make any assumptions on the number of bytes that are written to it on each write, since the unfiltered image data may come from the WIA 2.0 Preview Component rather than the driver.</span></span> <span data-ttu-id="d862d-130">Le composant d’aperçu WIA 2,0 écrit toujours l’intégralité des données d’image non filtrées dans le flux du filtre une seule fois, ce qui signifie que le flux du filtre a une source en écriture.</span><span class="sxs-lookup"><span data-stu-id="d862d-130">The WIA 2.0 Preview Component always writes the whole unfiltered image data into the filter's stream only once, which means that the filter's stream has one source writing into it.</span></span> <span data-ttu-id="d862d-131">Si le pilote et le composant d’aperçu écrivent dans le flux du filtre, le flux du filtre ne peut pas supposer, par exemple, qu’il recevra l’en-tête complet la première fois que [IStream :: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) est appelé, alors que son pilote correspondant écrit toujours les données d’en-tête en premier dans une écriture.</span><span class="sxs-lookup"><span data-stu-id="d862d-131">If both the driver and the preview component write into the filter's stream, the filter's stream cannot assume, for example, that it will receive the full header the first time [IStream::Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) is called although its corresponding driver always writes the header data first in one write.</span></span> <span data-ttu-id="d862d-132">Elle ne peut pas non plus supposer qu’une écriture suivante ne contient qu’une seule ligne de numérisation.</span><span class="sxs-lookup"><span data-stu-id="d862d-132">Nor can it assume that a subsequent write contains exactly one scan line.</span></span> <span data-ttu-id="d862d-133">Le flux de filtrage peut donc avoir à compter le nombre d’octets écrits pour déterminer, par exemple, où les données de l’image démarrent.</span><span class="sxs-lookup"><span data-stu-id="d862d-133">So the filtering stream may have to count the number of bytes written to it to determine, for example, where the image data starts.</span></span>

<span data-ttu-id="d862d-134">L’implémentation **IWiaTransferCallback :: GetNextStream** du filtre de traitement d’image doit lire les propriétés nécessaires à son traitement d’image à partir de l’élément pour lequel l’image est acquise.</span><span class="sxs-lookup"><span data-stu-id="d862d-134">The image processing filter's **IWiaTransferCallback::GetNextStream** implementation should read the properties needed for its image processing from the item for which the image is being acquired.</span></span> <span data-ttu-id="d862d-135">Le filtre ne lit pas les propriétés directement à partir du *pWiaItem2* passé dans [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span><span class="sxs-lookup"><span data-stu-id="d862d-135">The filter does not read the properties directly from the *pWiaItem2* passed into [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span></span> <span data-ttu-id="d862d-136">Au lieu de cela, le filtre doit appeler [**FindItemByName**](-wia-iwiaitem2-finditembyname.md) sur cet élément WIA 2,0 pour obtenir l’élément WIA 2,0 réel.</span><span class="sxs-lookup"><span data-stu-id="d862d-136">Instead the filter must call [**FindItemByName**](-wia-iwiaitem2-finditembyname.md) on this WIA 2.0 item to obtain the actual WIA 2.0 item.</span></span> <span data-ttu-id="d862d-137">Cela est dû au fait que l’image en cours d’acquisition peut être un élément enfant de *pWiaItem2*.</span><span class="sxs-lookup"><span data-stu-id="d862d-137">The reason for this is that the image being acquired may actually be a child item of *pWiaItem2*.</span></span> <span data-ttu-id="d862d-138">Par exemple, lors d’une acquisition de dossiers, le filtre utilise *pWiaItem2* pour obtenir les éléments enfants de *pWiaItem2* dans **IWiaTransferCallback :: GetNextStream** (lors d’une acquisition de dossier, le pilote retourne les images représentées par les éléments enfants de *pWiaItem2*).</span><span class="sxs-lookup"><span data-stu-id="d862d-138">For example, during a folder acquisition the filter uses *pWiaItem2* to obtain *pWiaItem2*'s child items in **IWiaTransferCallback::GetNextStream** (during a folder acquisition the driver returns the images represented by the child items of *pWiaItem2*).</span></span> <span data-ttu-id="d862d-139">Il en va de même lorsque le composant WIA 2,0 Preview appelle le filtre de traitement d’image en passant un élément enfant WIA de l' 2,0 acquisition d’images.</span><span class="sxs-lookup"><span data-stu-id="d862d-139">The same is true when the WIA 2.0 Preview Component calls into the image processing filter passing a child WIA 2.0 item.</span></span>

## <a name="requirements"></a><span data-ttu-id="d862d-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d862d-140">Requirements</span></span>



| <span data-ttu-id="d862d-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d862d-141">Requirement</span></span> | <span data-ttu-id="d862d-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="d862d-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d862d-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d862d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d862d-144">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d862d-144">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d862d-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d862d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d862d-146">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d862d-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d862d-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="d862d-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="d862d-148"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="d862d-148"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="d862d-149">MIDL</span><span class="sxs-lookup"><span data-stu-id="d862d-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d862d-150"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d862d-150"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="d862d-151">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d862d-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="d862d-152"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d862d-152"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
