---
description: La méthode GetBitmapBits récupère une image vidéo à l’heure du média spécifiée. Le frame retourné est toujours au format RGB 24 bits.
ms.assetid: b51df9d1-9c54-41bd-b0f8-ec290525deca
title: 'IMediaDet :: GetBitmapBits, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 95aea5281f77b32868e0f0856bc63063e4f08639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537637"
---
# <a name="imediadetgetbitmapbits-method"></a><span data-ttu-id="6ac9a-104">IMediaDet :: GetBitmapBits, méthode</span><span class="sxs-lookup"><span data-stu-id="6ac9a-104">IMediaDet::GetBitmapBits method</span></span>

> [!Note]  
> <span data-ttu-id="6ac9a-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-105">\[Deprecated.</span></span> <span data-ttu-id="6ac9a-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6ac9a-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6ac9a-107">La `GetBitmapBits` méthode récupère une image vidéo à l’heure du média spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-107">The `GetBitmapBits` method retrieves a video frame at the specified media time.</span></span> <span data-ttu-id="6ac9a-108">Le frame retourné est toujours au format RGB 24 bits.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-108">The returned frame is always in 24-bit RGB format.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ac9a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ac9a-109">Syntax</span></span>


```C++
HRESULT GetBitmapBits(
   double StreamTime,
   long   *pBufferSize,
   char   *pBuffer,
   long   Width,
   long   Height
);
```



## <a name="parameters"></a><span data-ttu-id="6ac9a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ac9a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ac9a-111">*StreamTime*</span><span class="sxs-lookup"><span data-stu-id="6ac9a-111">*StreamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="6ac9a-112">Heure à laquelle récupérer l’image vidéo, en secondes.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-112">Time at which to retrieve the video frame, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="6ac9a-113">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="6ac9a-113">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="6ac9a-114">Reçoit la taille de mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-114">Receives the required buffer size.</span></span> <span data-ttu-id="6ac9a-115">Si *pbuffer* a la **valeur null**, la variable reçoit la taille de la mémoire tampon nécessaire pour récupérer le frame.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-115">If *pBuffer* is **NULL**, the variable receives the size of the buffer needed to retrieve the frame.</span></span> <span data-ttu-id="6ac9a-116">Si *pbuffer* n’a pas la **valeur null**, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-116">If *pBuffer* is not **NULL**, this parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="6ac9a-117">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="6ac9a-117">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="6ac9a-118">Pointeur vers une mémoire tampon qui reçoit une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) suivie des bits dib.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-118">Pointer to a buffer that receives a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure followed by the DIB bits.</span></span>

</dd> <dt>

<span data-ttu-id="6ac9a-119">*Width*</span><span class="sxs-lookup"><span data-stu-id="6ac9a-119">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="6ac9a-120">Largeur de l’image vidéo, en pixels.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-120">Width of the video image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="6ac9a-121">*Height*</span><span class="sxs-lookup"><span data-stu-id="6ac9a-121">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="6ac9a-122">Hauteur de l’image vidéo, en pixels.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-122">Height of the video image, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ac9a-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6ac9a-123">Return value</span></span>

<span data-ttu-id="6ac9a-124">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6ac9a-124">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6ac9a-125">Il peut prendre les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="6ac9a-125">Possible values include the following:</span></span>



| <span data-ttu-id="6ac9a-126">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6ac9a-126">Return code</span></span>                                                                                             | <span data-ttu-id="6ac9a-127">Description</span><span class="sxs-lookup"><span data-stu-id="6ac9a-127">Description</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6ac9a-128"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6ac9a-128"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="6ac9a-129">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-129">Success.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="6ac9a-130"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="6ac9a-130"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="6ac9a-131">Impossible d’ajouter l’exemple de filtre d' [**accrochage**](sample-grabber-filter.md) au graphique.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-131">Could not add the [**Sample Grabber**](sample-grabber-filter.md) filter to the graph.</span></span><br/> |
| <dl> <span data-ttu-id="6ac9a-132"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="6ac9a-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>           | <span data-ttu-id="6ac9a-133">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-133">Insufficient memory.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="6ac9a-134"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="6ac9a-134"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="6ac9a-135">Erreur de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="6ac9a-135">**NULL** pointer error.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="6ac9a-136"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="6ac9a-136"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>            | <span data-ttu-id="6ac9a-137">Erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-137">Unexpected error.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="6ac9a-138"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="6ac9a-138"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="6ac9a-139">Type de média non valide.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-139">Invalid media type.</span></span><br/>                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="6ac9a-140">Notes</span><span class="sxs-lookup"><span data-stu-id="6ac9a-140">Remarks</span></span>

<span data-ttu-id="6ac9a-141">Avant d’appeler cette méthode, définissez le nom de fichier et le flux en appelant [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) et [**IMediaDet ::p ut \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="6ac9a-141">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="6ac9a-142">Pour déterminer la taille de la mémoire tampon requise, appelez cette méthode avec *pbuffer* égal à **null**.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-142">To determine the size of the buffer that is required, call this method with *pBuffer* equal to **NULL**.</span></span> <span data-ttu-id="6ac9a-143">La taille est retournée dans la variable vers laquelle pointe *pBufferSize*.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-143">The size is returned in the variable pointed to by *pBufferSize*.</span></span> <span data-ttu-id="6ac9a-144">Créez ensuite la mémoire tampon et rappelez la méthode, avec *pbuffer* égal à l’adresse de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-144">Then create the buffer and call the method again, with *pBuffer* equal to the address of the buffer.</span></span> <span data-ttu-id="6ac9a-145">Lorsque la méthode est retournée, la mémoire tampon contient une structure **BITMAPINFOHEADER** suivie de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-145">When the method returns, the buffer contains a **BITMAPINFOHEADER** structure followed by the bitmap.</span></span> <span data-ttu-id="6ac9a-146">La bitmap est mise à l’échelle selon les dimensions spécifiées dans les paramètres de *largeur* et de *hauteur* .</span><span class="sxs-lookup"><span data-stu-id="6ac9a-146">The bitmap is scaled to the dimensions specified in the *Width* and *Height* parameters.</span></span>

<span data-ttu-id="6ac9a-147">Cette méthode met le détecteur de média en mode de manipulation bitmap.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-147">This method puts the media detector into bitmap grab mode.</span></span> <span data-ttu-id="6ac9a-148">Une fois cette méthode appelée, les différentes méthodes d’informations de flux de **IMediaDet** ne fonctionnent pas, sauf si vous créez une nouvelle instance du détecteur de média.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-148">Once this method has been called, the various stream information methods in **IMediaDet** do not work, unless you create a new instance of the media detector.</span></span>

> [!Note]  
> <span data-ttu-id="6ac9a-149">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-149">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6ac9a-150">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6ac9a-150">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6ac9a-151">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-151">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="examples"></a><span data-ttu-id="6ac9a-152">Exemples</span><span class="sxs-lookup"><span data-stu-id="6ac9a-152">Examples</span></span>

<span data-ttu-id="6ac9a-153">Le code suivant utilise la `GetBitmapBits` méthode pour créer une image bitmap indépendante du périphérique.</span><span class="sxs-lookup"><span data-stu-id="6ac9a-153">The following code uses the `GetBitmapBits` method to create a device-independent bitmap.</span></span>


```C++
long size;
hr = pDet->GetBitmapBits(0, &size, 0, width, height);
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[size];
    if (!pBuffer)
        return E_OUTOFMEMORY;
    try {
        hr = pDet->GetBitmapBits(0, 0, pBuffer, width, height);
    }
    catch (...) {
        delete [] pBuffer;
        throw;
    }
    if (SUCCEEDED(hr))
    {
        BITMAPINFOHEADER *bmih = (BITMAPINFOHEADER*)pBuffer;
        HDC hdcDest = GetDC(0);
        
        // Find the address of the start of the image data.
        void *pData = pBuffer + sizeof(BITMAPINFOHEADER);
        
        // Note: In general a BITMAPINFOHEADER can include extra color
        // information at the end, so calculating the offset to the image
        // data is not generally correct. However, the IMediaDet interface
        // always returns an RGB-24 image with no extra color information.
        
        BITMAPINFO bmi;
        ZeroMemory(&bmi, sizeof(BITMAPINFO));
        CopyMemory(&(bmi.bmiHeader), bmih, sizeof(BITMAPINFOHEADER));
        HBITMAP hBitmap = CreateDIBitmap(hdcDest, bmih, CBM_INIT, 
            pData, &bmi, DIB_RGB_COLORS);
    }
    delete[] pBuffer;
}
```



## <a name="requirements"></a><span data-ttu-id="6ac9a-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ac9a-154">Requirements</span></span>



| <span data-ttu-id="6ac9a-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ac9a-155">Requirement</span></span> | <span data-ttu-id="6ac9a-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ac9a-156">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ac9a-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="6ac9a-157">Header</span></span><br/>  | <dl> <span data-ttu-id="6ac9a-158"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ac9a-158"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6ac9a-159">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6ac9a-159">Library</span></span><br/> | <dl> <span data-ttu-id="6ac9a-160"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ac9a-160"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ac9a-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ac9a-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ac9a-162">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="6ac9a-162">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="6ac9a-163">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="6ac9a-163">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




