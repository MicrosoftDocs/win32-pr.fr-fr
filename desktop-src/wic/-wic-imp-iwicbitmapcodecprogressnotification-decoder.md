---
description: Implémentation de IWICBitmapCodecProgressNotification (décodeur)
ms.assetid: 686b0875-c7ec-45ee-bd3e-94bfd9e5dcda
title: Implémentation de IWICBitmapCodecProgressNotification (décodeur)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f05f02e77886d96d794be3f974c1eb0eed9dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534299"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-decoder"></a><span data-ttu-id="8ff6c-103">Implémentation de IWICBitmapCodecProgressNotification (décodeur)</span><span class="sxs-lookup"><span data-stu-id="8ff6c-103">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>

## <a name="iwicbitmapcodecprogressnotification"></a><span data-ttu-id="8ff6c-104">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="8ff6c-104">IWICBitmapCodecProgressNotification</span></span>

<span data-ttu-id="8ff6c-105">Lorsqu’un codec effectue une opération d’e/s telle que [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) sur une grande image, l’exécution peut prendre plusieurs secondes ou quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-105">When a codec is performing an I/O operation such as [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) on a large image, it may take several seconds or even minutes to complete.</span></span> <span data-ttu-id="8ff6c-106">Lorsque les utilisateurs finaux ne peuvent pas interrompre une opération de longue durée, ils peuvent croire que l’application a été suspendue.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-106">When end users are unable to interrupt a long-running operation, they may think the application has hung.</span></span> <span data-ttu-id="8ff6c-107">Les utilisateurs ferment souvent une application, voire redémarrent leurs ordinateurs, afin de tenter de reprendre le contrôle de leur ordinateur lorsqu’une application ne répond plus.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-107">Users will often close an application, or even restart their computers, in an attempt to regain control of their computer when an application becomes unresponsive.</span></span>

<span data-ttu-id="8ff6c-108">Cette interface permet à une application de spécifier une fonction de rappel que le codec peut appeler à des intervalles spécifiés pour notifier l’appelant de la progression de l’opération en cours.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-108">This interface enables an application to specify a callback function that the codec can call at specified intervals to notify the caller of the progress of the current operation.</span></span> <span data-ttu-id="8ff6c-109">L’application peut utiliser cette fonction de rappel pour afficher une indication de la progression dans l’interface utilisateur pour notifier l’utilisateur de l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-109">The application can use this callback function to display an indication of progress in the user interface to notify the user of the status of the operation.</span></span> <span data-ttu-id="8ff6c-110">Si un utilisateur clique sur le bouton **Annuler** de la boîte de dialogue **État d’avancement** , l’application renvoie **WINCODEC \_ Err \_ abandonnée** à partir de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-110">If a user clicks the **Cancel** button on the **Progress** dialog box, the application returns **WINCODEC\_ERR\_ABORTED** from the callback function.</span></span> <span data-ttu-id="8ff6c-111">Dans ce cas, le codec doit annuler l’opération spécifiée et propager ce **HRESULT** à l’appelant de la méthode qui exécutait l’opération.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-111">When this happens, the codec must cancel the specified operation and propagate this **HRESULT** back to the caller of the method that was performing the operation.</span></span>

<span data-ttu-id="8ff6c-112">Cette interface doit être implémentée sur votre classe de décodeur au niveau du conteneur.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-112">This interface should be implemented on your container-level decoder class.</span></span>


```C++
interface IWICBitmapCodecProgressNotification : public IUnknown
{
    HRESULT RegisterProgressNotification ( 
        PFNProgressNotification pfnProgressNotification,
        LPVOID pvData,
        DWORD dwProgressFlags );
}
```



-   [<span data-ttu-id="8ff6c-113">RegisterProgressNotification</span><span class="sxs-lookup"><span data-stu-id="8ff6c-113">RegisterProgressNotification</span></span>](#registerprogressnotification)
-   [<span data-ttu-id="8ff6c-114">PFNProgressNotification</span><span class="sxs-lookup"><span data-stu-id="8ff6c-114">PFNProgressNotification</span></span>](#pfnprogressnotification)

### <a name="registerprogressnotification"></a><span data-ttu-id="8ff6c-115">RegisterProgressNotification</span><span class="sxs-lookup"><span data-stu-id="8ff6c-115">RegisterProgressNotification</span></span>

<span data-ttu-id="8ff6c-116">[**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) est appelé par une application pour inscrire une fonction de rappel que le codec peut appeler à intervalles spécifiés.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-116">[**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) is invoked by an application to register a callback function that the codec can call at specified intervals.</span></span> <span data-ttu-id="8ff6c-117">Le premier paramètre, *pfnProgressNotification*, est un pointeur vers la fonction de rappel que le codec doit appeler à des intervalles réguliers.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-117">The first parameter, *pfnProgressNotification*, is a pointer to the callback function that the codec should call at regular intervals.</span></span>

<span data-ttu-id="8ff6c-118">Le paramètre *pvData* pointe vers un objet que l’appelant souhaite que le codec renvoie à la fonction de rappel chaque fois que la fonction de rappel est appelée.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-118">The *pvData* parameter points to some object that the caller wants the codec to pass back to the callback function whenever the callback function is invoked.</span></span> <span data-ttu-id="8ff6c-119">Cet objet peut être tout et n’a aucune importance particulière pour le codec.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-119">This object may be anything at all and has no particular significance to the codec.</span></span>

<span data-ttu-id="8ff6c-120">Le paramètre *dwProgressFlags* spécifie quand le codec doit appeler la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-120">The *dwProgressFlags* parameter specifies when the codec should call the callback function.</span></span> <span data-ttu-id="8ff6c-121">Une fonction ou peut être exécutée avec deux énumérations pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-121">An OR function can be performed with two enumerations for this parameter.</span></span> <span data-ttu-id="8ff6c-122">L’énumération [**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation) spécifie s’il faut appeler la fonction de rappel pendant le décodage (**WICProgressOperationCopyPixels**), l’encodage (**WICProgerssOperationWritePixels**) ou les deux (**WICProgressOperationAll**).</span><span class="sxs-lookup"><span data-stu-id="8ff6c-122">The [**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation) enum specifies whether to call the callback function during decoding (**WICProgressOperationCopyPixels**), encoding (**WICProgerssOperationWritePixels**), or both (**WICProgressOperationAll**).</span></span>


```C++
enum WICProgressOperation
{
   WICProgressOperationCopyPixels,
   WICProgerssOperationWritePixels,
   WICProgressOperationAll      
};
```



<span data-ttu-id="8ff6c-123">Le codec doit appeler la fonction de rappel à intervalles réguliers tout au long de l’opération, mais l’appelant peut spécifier certaines exigences.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-123">The codec should call the callback function at regular intervals throughout the operation, but the caller may specify certain requirements.</span></span> <span data-ttu-id="8ff6c-124">L’énumération [**WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification) indique à quel point de l’opération d’appeler la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-124">The [**WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification) enum indicates at which point in the operation to call the callback function.</span></span> <span data-ttu-id="8ff6c-125">Si l’appelant spécifie **WICProgressNotificationBegin**, vous devez l’appeler au début de l’opération (0,0).</span><span class="sxs-lookup"><span data-stu-id="8ff6c-125">If the caller specifies **WICProgressNotificationBegin**, you must call it at the beginning of the operation (0.0).</span></span> <span data-ttu-id="8ff6c-126">Si l’appelant ne spécifie pas cela, il est facultatif.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-126">If the caller does not specify this, it is optional.</span></span> <span data-ttu-id="8ff6c-127">De même, si l’appelant spécifie **WICProgerssNotificationEnd**, vous devez l’appeler lorsque l’opération est terminée (1,0).</span><span class="sxs-lookup"><span data-stu-id="8ff6c-127">Likewise, if the caller specifies **WICProgerssNotificationEnd**, you must call it when the operation is completed (1.0).</span></span> <span data-ttu-id="8ff6c-128">Si l’appelant spécifie **WICProgressNotificationAll**, vous devez l’appeler au début et à la fin, ainsi qu’à intervalles réguliers tout au long de l’opération.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-128">If the caller specifies **WICProgressNotificationAll**, you must call it at the beginning and end, as well as at regular intervals throughout the operation.</span></span> <span data-ttu-id="8ff6c-129">L’appelant peut également spécifier **WICProgerssNotificationFrequent**, qui indique qu’il souhaite être rappelé à intervalles fréquents, par exemple après chaque ligne d’analyse.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-129">The caller may also specify **WICProgerssNotificationFrequent**, which indicates that they want to be called back at frequent intervals, perhaps after every couple of scan lines.</span></span> <span data-ttu-id="8ff6c-130">(Un appelant utilise généralement cet indicateur uniquement pour une très grande image.) Dans le cas contraire, vous devez généralement rappeler à intervalles d’environ 10 pour cent du nombre total de lignes de numérisation à traiter.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-130">(A caller will usually use this flag only for a very large image.) Otherwise, you should usually call back at intervals of approximately 10 percent increments of the total number of scan lines to be processed.</span></span>


```C++
enum WICProgressNotification
{
   WICProgressNotificationBegin,
   WICProgerssNotificationEnd,
   WICProgerssNotificationFrequent,
   WICProgressNotificationAll
};
```



<span data-ttu-id="8ff6c-131">Une seule fonction de rappel à la fois peut être inscrite pour une instance spécifique de décodeur ou d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-131">Only one callback function at a time can be registered for a specific decoder or encoder instance.</span></span> <span data-ttu-id="8ff6c-132">Si une application appelle [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) plusieurs fois, remplacez la fonction de rappel précédemment enregistrée par la nouvelle.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-132">If an application calls [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) more than once, replace the previously registered callback function with the new one.</span></span> <span data-ttu-id="8ff6c-133">Pour annuler une inscription de rappel, un appelant affecte la valeur **null** au paramètre *pfnProgressNotification* .</span><span class="sxs-lookup"><span data-stu-id="8ff6c-133">To cancel a callback registration, a caller will set the *pfnProgressNotification* parameter to **NULL**.</span></span>

### <a name="pfnprogressnotification"></a><span data-ttu-id="8ff6c-134">PFNProgressNotification</span><span class="sxs-lookup"><span data-stu-id="8ff6c-134">PFNProgressNotification</span></span>

<span data-ttu-id="8ff6c-135">[**PFNProgressNotification**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) est la fonction de rappel avec la signature suivante.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-135">[**PFNProgressNotification**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) is the callback function with the following signature.</span></span>


```C++
typedef HRESULT (*PFNProgressNotification) ( 
   LPVOID pvData,
   ULONG uFrameNum,
   WICProgressOperation operation,
   double dblProgress );
```



<span data-ttu-id="8ff6c-136">Quand vous appelez la fonction de rappel, utilisez le paramètre *pvData* pour retourner le même *pvData* que l’application spécifié lors de l’inscription de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-136">When you invoke the callback function, use the *pvData* parameter to pass back the same *pvData* that the application specified when it registered the callback function.</span></span>

<span data-ttu-id="8ff6c-137">Le paramètre *uFrameNum* doit indiquer l’index du frame en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-137">The *uFrameNum* parameter should indicate the index of the frame that is being processed.</span></span>

<span data-ttu-id="8ff6c-138">Définissez le paramètre d’opération sur **WICProgressOperationCopyPixels** lors du décodage et **WICProgressOperationWritePixels** lors de l’encodage.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-138">Set the operation parameter to **WICProgressOperationCopyPixels** when decoding and **WICProgressOperationWritePixels** when encoding.</span></span>

<span data-ttu-id="8ff6c-139">Le paramètre *dblProgress* doit être un nombre compris entre 0,0 (le début de l’opération) et 1,0 (la fin de l’opération).</span><span class="sxs-lookup"><span data-stu-id="8ff6c-139">The *dblProgress* parameter should be a number between 0.0 (the beginning of the operation) and 1.0 (the completion of the operation).</span></span> <span data-ttu-id="8ff6c-140">La valeur doit refléter la proportion de lignes de numérisation déjà traitées par rapport au nombre total de lignes de numérisation à traiter.</span><span class="sxs-lookup"><span data-stu-id="8ff6c-140">The value should reflect the proportion of scan lines already processed relative to the total number of scan lines to be processed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ff6c-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8ff6c-141">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8ff6c-142">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="8ff6c-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8ff6c-143">**ProgressNotificationCallback**</span><span class="sxs-lookup"><span data-stu-id="8ff6c-143">**ProgressNotificationCallback**</span></span>](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)
</dt> <dt>

[<span data-ttu-id="8ff6c-144">**IWICBitmapCodecProgressNotification**</span><span class="sxs-lookup"><span data-stu-id="8ff6c-144">**IWICBitmapCodecProgressNotification**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification)
</dt> <dt>

<span data-ttu-id="8ff6c-145">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="8ff6c-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8ff6c-146">Implémentation de IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="8ff6c-146">Implementing IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[<span data-ttu-id="8ff6c-147">Implémentation de IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="8ff6c-147">Implementing IWICBitmapSource</span></span>](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[<span data-ttu-id="8ff6c-148">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="8ff6c-148">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="8ff6c-149">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="8ff6c-149">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



