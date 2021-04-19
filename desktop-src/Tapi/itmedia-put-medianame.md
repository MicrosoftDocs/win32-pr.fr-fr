---
description: La \_ méthode put MEDIANAME définit le nom du support. Les médias définis sont audio, vidéo, tableau blanc, texte et données.
ms.assetid: 0dd18add-6c7e-40a8-8b39-10c65bdfb2e0
title: ITMedia ::p ut_MediaName, méthode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66dcbd4e29f59694d610fb4e6af9fd49aa53323d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538095"
---
# <a name="itmediaput_medianame-method"></a><span data-ttu-id="3b54b-104">ITMedia ::p ut \_ MEDIANAME, méthode</span><span class="sxs-lookup"><span data-stu-id="3b54b-104">ITMedia::put\_MediaName method</span></span>

<span data-ttu-id="3b54b-105">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3b54b-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3b54b-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="3b54b-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3b54b-107">La méthode **put \_ MEDIANAME** définit le nom du support.</span><span class="sxs-lookup"><span data-stu-id="3b54b-107">The **put\_MediaName** method sets the media name.</span></span> <span data-ttu-id="3b54b-108">Les médias définis sont audio, vidéo, tableau blanc, texte et données.</span><span class="sxs-lookup"><span data-stu-id="3b54b-108">Defined media are audio, video, whiteboard, text, and data.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b54b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b54b-109">Syntax</span></span>


```C++
HRESULT put_MediaName(
  [in] BSTR pMediaName
);
```



## <a name="parameters"></a><span data-ttu-id="3b54b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b54b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b54b-111">*pMediaName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b54b-111">*pMediaName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b54b-112">Pointeur vers un **BSTR** contenant le nom du support à définir.</span><span class="sxs-lookup"><span data-stu-id="3b54b-112">Pointer to a **BSTR** containing the media name to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b54b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b54b-113">Return value</span></span>

<span data-ttu-id="3b54b-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="3b54b-114">This method can return one of these values.</span></span>



| <span data-ttu-id="3b54b-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3b54b-115">Return code</span></span>                                                                                   | <span data-ttu-id="3b54b-116">Description</span><span class="sxs-lookup"><span data-stu-id="3b54b-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="3b54b-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3b54b-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3b54b-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="3b54b-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3b54b-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="3b54b-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3b54b-120">Le paramètre *pMediaName* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="3b54b-120">The *pMediaName* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="3b54b-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="3b54b-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3b54b-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="3b54b-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="3b54b-123"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="3b54b-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="3b54b-124">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3b54b-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="3b54b-125"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="3b54b-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="3b54b-126">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="3b54b-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="3b54b-127">Notes</span><span class="sxs-lookup"><span data-stu-id="3b54b-127">Remarks</span></span>

<span data-ttu-id="3b54b-128">L’application doit utiliser [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire pour le paramètre *PMediaName* et utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque la variable n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3b54b-128">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pMediaName* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="3b54b-129">Cette fonction peut envoyer des données sur le réseau sous une forme non chiffrée ; par conséquent, une personne malveillante sur le réseau peut être en mesure de lire les données.</span><span class="sxs-lookup"><span data-stu-id="3b54b-129">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="3b54b-130">Les risques de sécurité liés à l’envoi des données en texte clair doivent être pris en compte avant d’utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3b54b-130">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b54b-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b54b-131">Requirements</span></span>



| <span data-ttu-id="3b54b-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b54b-132">Requirement</span></span> | <span data-ttu-id="3b54b-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b54b-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b54b-134">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="3b54b-134">TAPI version</span></span><br/> | <span data-ttu-id="3b54b-135">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="3b54b-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3b54b-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b54b-136">Header</span></span><br/>       | <dl> <span data-ttu-id="3b54b-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b54b-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b54b-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3b54b-138">Library</span></span><br/>      | <dl> <span data-ttu-id="3b54b-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b54b-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3b54b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3b54b-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="3b54b-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b54b-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b54b-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b54b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b54b-143">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="3b54b-143">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="3b54b-144">**ITMedia :: obtient \_ MEDIANAME**</span><span class="sxs-lookup"><span data-stu-id="3b54b-144">**ITMedia::get\_MediaName**</span></span>](itmedia-get-medianame.md)
</dt> </dl>

 

