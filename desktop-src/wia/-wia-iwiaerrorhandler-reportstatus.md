---
description: Gère les messages d’État et d’erreur pendant les transferts de données d’image et les affiche à l’utilisateur.
ms.assetid: 23e85c63-80b9-4510-854d-289c8d23be2d
title: 'IWiaErrorHandler :: ReportStatus, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 30a082502d4c7bc5b789fd1ec19fdb76f63d8fab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544870"
---
# <a name="iwiaerrorhandlerreportstatus-method"></a><span data-ttu-id="f6553-103">IWiaErrorHandler :: ReportStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="f6553-103">IWiaErrorHandler::ReportStatus method</span></span>

<span data-ttu-id="f6553-104">Gère les messages d’État et d’erreur pendant les transferts de données d’image et les affiche à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f6553-104">Handles status and error messages during image data transfers and displays them to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6553-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6553-105">Syntax</span></span>


```C++
HRESULT ReportStatus(
  [in] HWND     hwndParent,
  [in] IUnknown *punkItem,
  [in] HRESULT  hrStatus,
  [in] LONG     cbResLength,
  [in] BYTE     *pbData
);
```



## <a name="parameters"></a><span data-ttu-id="f6553-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f6553-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6553-107">*hwndParent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f6553-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6553-108">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="f6553-108">Type: **HWND**</span></span>

<span data-ttu-id="f6553-109">**HWND** qui est la fenêtre parente pour la fenêtre de message.</span><span class="sxs-lookup"><span data-stu-id="f6553-109">**HWND** that is the parent window for the message window.</span></span>

</dd> <dt>

<span data-ttu-id="f6553-110">*punkItem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f6553-110">*punkItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6553-111">Tapez : \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="f6553-111">Type: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="f6553-112">Pointeur vers l’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) de l’élément en cours de transfert.</span><span class="sxs-lookup"><span data-stu-id="f6553-112">Pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the item being transferred.</span></span> <span data-ttu-id="f6553-113">Cet objet implémente au minimum [_ *IWiaItem2* \*](-wia-iwiaitem2.md) et [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span><span class="sxs-lookup"><span data-stu-id="f6553-113">This object minimally implements [_ *IWiaItem2*\*](-wia-iwiaitem2.md) and [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span></span>

</dd> <dt>

<span data-ttu-id="f6553-114">*hrStatus* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f6553-114">*hrStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6553-115">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f6553-115">Type: **HRESULT**</span></span>

<span data-ttu-id="f6553-116">**HRESULT** qui correspond au code d’état reçu par [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="f6553-116">**HRESULT** that is the status code received by [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> <dt>

<span data-ttu-id="f6553-117">*cbResLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f6553-117">*cbResLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6553-118">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="f6553-118">Type: **LONG**</span></span>

<span data-ttu-id="f6553-119">**Valeur de type long** qui correspond à la taille des données référencées par *pbData*.</span><span class="sxs-lookup"><span data-stu-id="f6553-119">**LONG** that is the size of the data referred to by *pbData*.</span></span>

</dd> <dt>

<span data-ttu-id="f6553-120">*pbData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f6553-120">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6553-121">Type : \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="f6553-121">Type: \**BYTE\** _</span></span>

<span data-ttu-id="f6553-122">Pointeur vers la mémoire tampon de données telle qu’elle a été reçue par [_ *BandedDataCallback* \*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="f6553-122">Pointer to the data buffer as received by [_ *BandedDataCallback*\*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6553-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f6553-123">Return value</span></span>

<span data-ttu-id="f6553-124">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f6553-124">Type: **HRESULT**</span></span>

<span data-ttu-id="f6553-125">Retourne *hrStatus* si l’erreur ne peut pas être récupérée à partir de.</span><span class="sxs-lookup"><span data-stu-id="f6553-125">Returns *hrStatus* if the error cannot be recovered from.</span></span> <span data-ttu-id="f6553-126">Dans le cas contraire, elle retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f6553-126">Otherwise, it returns one of the following values.</span></span>



| <span data-ttu-id="f6553-127">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f6553-127">Return code</span></span>                                                                             | <span data-ttu-id="f6553-128">Description</span><span class="sxs-lookup"><span data-stu-id="f6553-128">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f6553-129"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f6553-129"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="f6553-130">L’action appropriée a été prise pour corriger l’erreur et le transfert peut se poursuivre.</span><span class="sxs-lookup"><span data-stu-id="f6553-130">The appropriate action was taken to correct the error and the transfer can continue.</span></span> <br/> |
| <dl> <span data-ttu-id="f6553-131"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="f6553-131"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="f6553-132">Aucune action n’a été prise pour gérer l’état d’erreur ou de rapport à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f6553-132">No action was taken to handle the error or report status to the user.</span></span> <br/>                |
| <dl> <span data-ttu-id="f6553-133"><dt>**E \_ Abort**</dt></span><span class="sxs-lookup"><span data-stu-id="f6553-133"><dt>**E\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="f6553-134">L’utilisateur a choisi d’abandonner le transfert en réponse à la boîte de dialogue affichée.</span><span class="sxs-lookup"><span data-stu-id="f6553-134">The user chose to abort the transfer in response to the displayed dialog box.</span></span> <br/>        |



 

## <a name="remarks"></a><span data-ttu-id="f6553-135">Notes</span><span class="sxs-lookup"><span data-stu-id="f6553-135">Remarks</span></span>

<span data-ttu-id="f6553-136">L’acquisition d’images Windows (WIA) 2,0 appelle **IWiaErrorHandler :: ReportStatus** lorsque le pilote envoie un message d’état de l' **\_ \_ appareil \_ MSG MSG** à [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="f6553-136">Windows Image Acquisition (WIA) 2.0 calls **IWiaErrorHandler::ReportStatus** when the driver sends an **IT\_MSG\_DEVICE\_STATUS** message to [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span> <span data-ttu-id="f6553-137">Cette méthode gère le message et affiche des informations à l’utilisateur sur l’État ou l’erreur.</span><span class="sxs-lookup"><span data-stu-id="f6553-137">This method handles the message and displays information to the user about the status or error.</span></span> <span data-ttu-id="f6553-138">Si le message concerne une erreur, la méthode permet à l’utilisateur de choisir, si possible, s’il faut essayer de récupérer à partir de l’erreur et continuer le transfert ou l’abandonner.</span><span class="sxs-lookup"><span data-stu-id="f6553-138">If the message is about an error, the method lets the user choose, if possible, whether to try to recover from the error and continue the transfer or to abort.</span></span>

<span data-ttu-id="f6553-139">*hrStatus* est défini sur WIA \_ Status \_ Transfer \_ Begin pour informer le gestionnaire qu’un transfert a démarré.</span><span class="sxs-lookup"><span data-stu-id="f6553-139">*hrStatus* is set to WIA\_STATUS\_TRANSFER\_BEGIN to inform the handler a transfer has started.</span></span> <span data-ttu-id="f6553-140">Elle est définie sur \_ \_ la fin du transfert d’État WIA une \_ fois le transfert terminé.</span><span class="sxs-lookup"><span data-stu-id="f6553-140">It is set to WIA\_STATUS\_TRANSFER\_END when the transfer is complete.</span></span>

<span data-ttu-id="f6553-141">Si le niveau de gravité de la valeur de *hrStatus* est \_ réussite, l’utilisateur doit être autorisé à annuler le transfert.</span><span class="sxs-lookup"><span data-stu-id="f6553-141">If *hrStatus* is SEVERITY\_SUCCESS, the user should be allowed to cancel the transfer.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6553-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6553-142">Requirements</span></span>



| <span data-ttu-id="f6553-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6553-143">Requirement</span></span> | <span data-ttu-id="f6553-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6553-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6553-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6553-145">Minimum supported client</span></span><br/> | <span data-ttu-id="f6553-146">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6553-146">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f6553-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6553-147">Minimum supported server</span></span><br/> | <span data-ttu-id="f6553-148">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6553-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f6553-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="f6553-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6553-150"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6553-150"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="f6553-151">MIDL</span><span class="sxs-lookup"><span data-stu-id="f6553-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f6553-152"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f6553-152"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="f6553-153">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f6553-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="f6553-154"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6553-154"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
