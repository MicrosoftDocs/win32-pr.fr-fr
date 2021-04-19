---
description: La méthode SetBandwidthInfo définit les informations de bande passante.
ms.assetid: bf5db456-ea67-4a65-a681-df0741f73fc9
title: 'ITConnection :: SetBandwidthInfo, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c17054743f6d47775e994dbfe3b80c7afe1ab68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539609"
---
# <a name="itconnectionsetbandwidthinfo-method"></a><span data-ttu-id="2fdf1-103">ITConnection :: SetBandwidthInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="2fdf1-103">ITConnection::SetBandwidthInfo method</span></span>

<span data-ttu-id="2fdf1-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="2fdf1-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2fdf1-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="2fdf1-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2fdf1-106">La méthode **SetBandwidthInfo** définit les informations de bande passante.</span><span class="sxs-lookup"><span data-stu-id="2fdf1-106">The **SetBandwidthInfo** method sets the bandwidth information.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fdf1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fdf1-107">Syntax</span></span>


```C++
HRESULT SetBandwidthInfo(
  [in] BSTR   pModifier,
  [in] DOUBLE Bandwidth
);
```



## <a name="parameters"></a><span data-ttu-id="2fdf1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2fdf1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fdf1-109">*pModifier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2fdf1-109">*pModifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fdf1-110">Pointeur vers un **BSTR** indiquant la portée de la bande passante définie.</span><span class="sxs-lookup"><span data-stu-id="2fdf1-110">Pointer to a **BSTR** indicating the scope of the bandwidth being set.</span></span> <span data-ttu-id="2fdf1-111">Pour plus d'informations, consultez la section Notes qui suit.</span><span class="sxs-lookup"><span data-stu-id="2fdf1-111">For more information, see the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="2fdf1-112">*Bande passante* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2fdf1-112">*Bandwidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fdf1-113">La.</span><span class="sxs-lookup"><span data-stu-id="2fdf1-113">Bandwidth.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fdf1-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2fdf1-114">Return value</span></span>

<span data-ttu-id="2fdf1-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="2fdf1-115">This method can return one of these values.</span></span>



| <span data-ttu-id="2fdf1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fdf1-116">Value</span></span>                                                                                         | <span data-ttu-id="2fdf1-117">Signification</span><span class="sxs-lookup"><span data-stu-id="2fdf1-117">Meaning</span></span>                                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="2fdf1-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2fdf1-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2fdf1-119">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="2fdf1-119">Method succeeded.</span></span><br/>                                      |
| <dl> <span data-ttu-id="2fdf1-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2fdf1-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2fdf1-121">Le paramètre *pModifier* ou *Bandwidth* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2fdf1-121">The *pModifier* or *Bandwidth* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="2fdf1-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="2fdf1-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2fdf1-123">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="2fdf1-123">Insufficient memory exists to perform the operation.</span></span><br/>   |
| <dl> <span data-ttu-id="2fdf1-124"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="2fdf1-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="2fdf1-125">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2fdf1-125">Unspecified error.</span></span><br/>                                     |
| <dl> <span data-ttu-id="2fdf1-126"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="2fdf1-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="2fdf1-127">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="2fdf1-127">This method is not yet implemented.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="2fdf1-128">Notes</span><span class="sxs-lookup"><span data-stu-id="2fdf1-128">Remarks</span></span>

<span data-ttu-id="2fdf1-129">L’application doit utiliser [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire pour le paramètre *PModifier* et utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque la variable n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="2fdf1-129">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pModifier* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="2fdf1-130">Référence : RFC 2327.</span><span class="sxs-lookup"><span data-stu-id="2fdf1-130">Reference: RFC 2327.</span></span>

<span data-ttu-id="2fdf1-131">Le modificateur de bande passante sera normalement soit CT, soit :</span><span class="sxs-lookup"><span data-stu-id="2fdf1-131">The bandwidth modifier will normally be either CT or AS:</span></span>

<span data-ttu-id="2fdf1-132">**Total de la Conférence CT :** Une bande passante maximale implicite est associée à chaque durée de vie (TTL, [*Time to Live*](t-tapgloss.md) ) sur le MBone ou dans une région d’étendue administrative de multidiffusion particulière (les limites de bande passante MBone par rapport à la durée de vie sont indiquées dans le Forum aux questions sur MBone).</span><span class="sxs-lookup"><span data-stu-id="2fdf1-132">**CT Conference Total:** An implicit maximum bandwidth is associated with each [*time to live*](t-tapgloss.md) (TTL) on the Mbone or within a particular multicast administrative scope region (the Mbone bandwidth versus TTL limits are given in the MBone FAQ).</span></span> <span data-ttu-id="2fdf1-133">Si la bande passante d’une session ou d’un support dans une session est différente de la bande passante implicite de l’étendue, un \` b = CT :... la ligne doit être fournie pour la session en donnant la limite supérieure proposée à la bande passante utilisée.</span><span class="sxs-lookup"><span data-stu-id="2fdf1-133">If the bandwidth of a session or media in a session is different from the bandwidth implicit from the scope, a \`b=CT:...' line should be supplied for the session giving the proposed upper limit to the bandwidth used.</span></span> <span data-ttu-id="2fdf1-134">L’objectif principal est de fournir une idée approximative du fait que deux conférences ou plus peuvent coexister simultanément.</span><span class="sxs-lookup"><span data-stu-id="2fdf1-134">The primary purpose of this is to give an approximate idea as to whether two or more conferences can coexist simultaneously.</span></span>

<span data-ttu-id="2fdf1-135">**Comme Application-Specific maximale :** La bande passante est interprétée comme étant spécifique à l’application, c.-à-d., est le concept de bande passante maximale de l’application.</span><span class="sxs-lookup"><span data-stu-id="2fdf1-135">**AS Application-Specific Maximum:** The bandwidth is interpreted to be application-specific, i.e., will be the application's concept of maximum bandwidth.</span></span> <span data-ttu-id="2fdf1-136">Normalement, cela correspond à ce qui est défini sur le contrôle de « bande passante maximale » de l’application, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="2fdf1-136">Normally this will coincide with what is set on the application's "maximum bandwidth" control, if applicable.</span></span>

<span data-ttu-id="2fdf1-137">Notez que CT donne une quantité totale de bande passante pour tous les supports sur tous les sites.</span><span class="sxs-lookup"><span data-stu-id="2fdf1-137">Note that CT gives a total bandwidth figure for all the media at all sites.</span></span> <span data-ttu-id="2fdf1-138">Tout comme donne une quantité de bande passante pour un seul média sur un seul site, bien qu’il puisse y avoir plusieurs sites envoyant simultanément.</span><span class="sxs-lookup"><span data-stu-id="2fdf1-138">AS gives a bandwidth figure for a single media at a single site, although there may be many sites sending simultaneously.</span></span>

<span data-ttu-id="2fdf1-139">**Mécanisme d’extension :** Les rédacteurs d’outils peuvent définir des modificateurs de bande passante expérimentaux en préfixant leurs modificateurs avec « X- ».</span><span class="sxs-lookup"><span data-stu-id="2fdf1-139">**Extension Mechanism:** Tool writers can define experimental bandwidth modifiers by prefixing their modifiers with "X-".</span></span>

## <a name="requirements"></a><span data-ttu-id="2fdf1-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2fdf1-140">Requirements</span></span>



| <span data-ttu-id="2fdf1-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2fdf1-141">Requirement</span></span> | <span data-ttu-id="2fdf1-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fdf1-142">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2fdf1-143">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="2fdf1-143">TAPI version</span></span><br/> | <span data-ttu-id="2fdf1-144">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2fdf1-144">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2fdf1-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="2fdf1-145">Header</span></span><br/>       | <dl> <span data-ttu-id="2fdf1-146"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fdf1-146"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="2fdf1-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2fdf1-147">Library</span></span><br/>      | <dl> <span data-ttu-id="2fdf1-148"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2fdf1-148"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2fdf1-149">DLL</span><span class="sxs-lookup"><span data-stu-id="2fdf1-149">DLL</span></span><br/>          | <dl> <span data-ttu-id="2fdf1-150"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fdf1-150"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fdf1-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fdf1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fdf1-152">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="2fdf1-152">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

