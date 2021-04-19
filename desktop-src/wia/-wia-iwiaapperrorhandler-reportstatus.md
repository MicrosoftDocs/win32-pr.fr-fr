---
description: Gère l’état des appareils et les messages d’erreur pendant les transferts de données d’image et affiche les messages à l’utilisateur.
ms.assetid: 8d3ba598-8649-4108-aebc-94f2bcb64ad8
title: 'IWiaAppErrorHandler :: ReportStatus, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 1285b5391014919d7108f207917b0c44c03fa360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533762"
---
# <a name="iwiaapperrorhandlerreportstatus-method"></a><span data-ttu-id="2319d-103">IWiaAppErrorHandler :: ReportStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="2319d-103">IWiaAppErrorHandler::ReportStatus method</span></span>

<span data-ttu-id="2319d-104">Gère l’état des appareils et les messages d’erreur pendant les transferts de données d’image et affiche les messages à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2319d-104">Handles device status and error messages during image data transfers and displays the messages to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="2319d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2319d-105">Syntax</span></span>


```C++
HRESULT ReportStatus(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaItem2,
  [in] HRESULT   hrStatus,
  [in] LONG      lPercentComplete
);
```



## <a name="parameters"></a><span data-ttu-id="2319d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2319d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2319d-107">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2319d-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2319d-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="2319d-108">Type: **LONG**</span></span>

<span data-ttu-id="2319d-109">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="2319d-109">Not used.</span></span> <span data-ttu-id="2319d-110">Définit la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="2319d-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="2319d-111">*pWiaItem2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2319d-111">*pWiaItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2319d-112">Tapez : \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="2319d-112">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="2319d-113">Pointeur vers l’élément en cours de transfert.</span><span class="sxs-lookup"><span data-stu-id="2319d-113">Pointer to the item being transferred.</span></span>

</dd> <dt>

<span data-ttu-id="2319d-114">_hrStatus \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2319d-114">_hrStatus\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2319d-115">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2319d-115">Type: **HRESULT**</span></span>

<span data-ttu-id="2319d-116">Code d’état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2319d-116">Device status code.</span></span>

</dd> <dt>

<span data-ttu-id="2319d-117">*lPercentComplete* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2319d-117">*lPercentComplete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2319d-118">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="2319d-118">Type: **LONG**</span></span>

<span data-ttu-id="2319d-119">Pourcentage effectué de l’opération en cours.</span><span class="sxs-lookup"><span data-stu-id="2319d-119">Percentage completed of current operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2319d-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2319d-120">Return value</span></span>

<span data-ttu-id="2319d-121">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2319d-121">Type: **HRESULT**</span></span>

<span data-ttu-id="2319d-122">Retourne *hrStatus* si la récupération à partir de l’erreur n’est pas possible.</span><span class="sxs-lookup"><span data-stu-id="2319d-122">Returns *hrStatus* if recovery from the error is not possible.</span></span> <span data-ttu-id="2319d-123">Dans le cas contraire, elle retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2319d-123">Otherwise, it returns one of the following values.</span></span>



| <span data-ttu-id="2319d-124">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2319d-124">Return code</span></span>                                                                                              | <span data-ttu-id="2319d-125">Description</span><span class="sxs-lookup"><span data-stu-id="2319d-125">Description</span></span>                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2319d-126"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2319d-126"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="2319d-127">Si *hrStatus* est une erreur, l’action appropriée a été effectuée pour corriger l’erreur et le transfert peut continuer.</span><span class="sxs-lookup"><span data-stu-id="2319d-127">If *hrStatus* is an error, the appropriate action was taken to correct the error, and the transfer can continue.</span></span> <span data-ttu-id="2319d-128">Si *hrStatus* est informatif, l’utilisateur a été informé avec une boîte de dialogue non modale et a choisi de ne pas annuler le transfert.</span><span class="sxs-lookup"><span data-stu-id="2319d-128">If *hrStatus* is informational, the user was informed with a modeless dialog box and chose not to cancel the transfer.</span></span><br/> |
| <dl> <span data-ttu-id="2319d-129"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="2319d-129"><dt>**S\_FALSE**</dt></span></span> </dl>                  | <span data-ttu-id="2319d-130">L’utilisateur a annulé le transfert à partir de la boîte de dialogue non modale du gestionnaire d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="2319d-130">The user cancelled the transfer from the error handler modeless dialog box.</span></span> <span data-ttu-id="2319d-131">Cette valeur peut être retournée à n’importe quel point, quelle que soit la valeur de l’élément *hrStatus* .</span><span class="sxs-lookup"><span data-stu-id="2319d-131">This value can be returned at any point no matter what *hrStatus* is.</span></span> <br/>                                                                                      |
| <dl> <span data-ttu-id="2319d-132"><dt>**\_État WIA \_ non \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="2319d-132"><dt>**WIA\_STATUS\_NOT\_HANDLED**</dt></span></span> </dl> | <span data-ttu-id="2319d-133">Aucune action n’a été effectuée ; autrement dit, aucune boîte de dialogue n’a été présentée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2319d-133">No action was taken; that is, no dialog box was presented to the user.</span></span> <span data-ttu-id="2319d-134">Le gestionnaire d’erreurs suivant sera appelé.</span><span class="sxs-lookup"><span data-stu-id="2319d-134">The next error handler will be invoked.</span></span> <span data-ttu-id="2319d-135">L’ordre des gestionnaires d’erreurs est le suivant : application, pilote et système par défaut.</span><span class="sxs-lookup"><span data-stu-id="2319d-135">The order of error handlers is: application, driver, and system default.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="2319d-136">Notes</span><span class="sxs-lookup"><span data-stu-id="2319d-136">Remarks</span></span>

<span data-ttu-id="2319d-137">Le paramètre *lPercentComplete* permet à une fenêtre de gestionnaire d’erreurs d’afficher la progression.</span><span class="sxs-lookup"><span data-stu-id="2319d-137">The *lPercentComplete* parameter enables an error handler window to show progress.</span></span> <span data-ttu-id="2319d-138">Par exemple, un pilote peut fournir une estimation du temps nécessaire à la mise en route.</span><span class="sxs-lookup"><span data-stu-id="2319d-138">For example, a driver might provide an estimate of how long "warming up" takes.</span></span> <span data-ttu-id="2319d-139">Le paramètre *lPercentComplete* passé dans **IWiaAppErrorHandler :: ReportStatus** est la même valeur que le **lPercentComplete** que le pilote définit dans la structure [**WiaTransferParams**](-wia-wiatransferparams.md) .</span><span class="sxs-lookup"><span data-stu-id="2319d-139">The *lPercentComplete* parameter passed into **IWiaAppErrorHandler::ReportStatus** is the same value as the **lPercentComplete** that the driver sets into the [**WiaTransferParams**](-wia-wiatransferparams.md) structure.</span></span>

<span data-ttu-id="2319d-140">Un gestionnaire d’erreurs peut utiliser les macros ayant réussi et échoué pour déterminer si *hrStatus* a une erreur de gravité \_ ou une gravité de gravité \_ .</span><span class="sxs-lookup"><span data-stu-id="2319d-140">An error handler can use the SUCCEEDED and FAILED macros to find out if *hrStatus* has SEVERITY\_ERROR or SEVERITY\_SUCCESS.</span></span>

<span data-ttu-id="2319d-141">Si le niveau de gravité de la valeur de *hrStatus* est \_ réussite, l’utilisateur doit être autorisé à annuler le transfert.</span><span class="sxs-lookup"><span data-stu-id="2319d-141">If *hrStatus* is SEVERITY\_SUCCESS, the user should be allowed to cancel the transfer.</span></span>

<span data-ttu-id="2319d-142">Si *hrStatus* est \_ une erreur de gravité, le gestionnaire d’erreurs doit afficher une boîte de dialogue modale détenue par la fenêtre parente de l’application.</span><span class="sxs-lookup"><span data-stu-id="2319d-142">If *hrStatus* is SEVERITY\_ERROR, the error handler should display a modal dialog box owned by the application parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="2319d-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2319d-143">Requirements</span></span>



| <span data-ttu-id="2319d-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2319d-144">Requirement</span></span> | <span data-ttu-id="2319d-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="2319d-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2319d-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2319d-146">Minimum supported client</span></span><br/> | <span data-ttu-id="2319d-147">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2319d-147">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2319d-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2319d-148">Minimum supported server</span></span><br/> | <span data-ttu-id="2319d-149">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2319d-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2319d-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="2319d-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="2319d-151"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="2319d-151"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="2319d-152">MIDL</span><span class="sxs-lookup"><span data-stu-id="2319d-152">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2319d-153"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2319d-153"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="2319d-154">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2319d-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="2319d-155"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2319d-155"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




