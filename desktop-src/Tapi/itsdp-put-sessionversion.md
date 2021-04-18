---
description: La \_ méthode put SessionVersion définit la version de la session.
ms.assetid: 8984d608-0fad-4979-9c58-ac2fb7926796
title: ITSdp ::p ut_SessionVersion, méthode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a096117f894a2ff33f127c683b84ba50e88308e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533227"
---
# <a name="itsdpput_sessionversion-method"></a><span data-ttu-id="3b452-103">ITSdp ::p ut \_ SessionVersion, méthode</span><span class="sxs-lookup"><span data-stu-id="3b452-103">ITSdp::put\_SessionVersion method</span></span>

<span data-ttu-id="3b452-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3b452-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3b452-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="3b452-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3b452-106">La méthode **put \_ SessionVersion** définit la version de la session.</span><span class="sxs-lookup"><span data-stu-id="3b452-106">The **put\_SessionVersion** method sets the session version.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b452-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b452-107">Syntax</span></span>


```C++
HRESULT put_SessionVersion(
  [in] DOUBLE SessionVersion
);
```



## <a name="parameters"></a><span data-ttu-id="3b452-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b452-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b452-109">*SessionVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b452-109">*SessionVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b452-110">Valeur de la version de la session.</span><span class="sxs-lookup"><span data-stu-id="3b452-110">Session version value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b452-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b452-111">Return value</span></span>

<span data-ttu-id="3b452-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="3b452-112">This method can return one of these values.</span></span>



| <span data-ttu-id="3b452-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3b452-113">Return code</span></span>                                                                                   | <span data-ttu-id="3b452-114">Description</span><span class="sxs-lookup"><span data-stu-id="3b452-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="3b452-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3b452-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3b452-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="3b452-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3b452-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3b452-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3b452-118">Le paramètre *SessionVersion* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="3b452-118">The *SessionVersion* parameter is not valid.</span></span><br/>         |
| <dl> <span data-ttu-id="3b452-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="3b452-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3b452-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="3b452-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="3b452-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="3b452-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="3b452-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3b452-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="3b452-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="3b452-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="3b452-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="3b452-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="3b452-125">Notes</span><span class="sxs-lookup"><span data-stu-id="3b452-125">Remarks</span></span>

<span data-ttu-id="3b452-126">La valeur de retour de cette méthode peut être **ULong**, mais Visual Basic ne prend pas en charge le type **ULong** .</span><span class="sxs-lookup"><span data-stu-id="3b452-126">The return value of this method could be **ULONG**, but Visual Basic doesn't support the **ULONG** type.</span></span> <span data-ttu-id="3b452-127">Un **double** est le plus petit type suivant qui englobe la plage entière de valeurs requises.</span><span class="sxs-lookup"><span data-stu-id="3b452-127">A **DOUBLE** is the next smallest type that encompasses the entire range of values required.</span></span>

<span data-ttu-id="3b452-128">Cette fonction peut envoyer des données sur le réseau sous une forme non chiffrée ; par conséquent, une personne malveillante sur le réseau peut être en mesure de lire les données.</span><span class="sxs-lookup"><span data-stu-id="3b452-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="3b452-129">Les risques de sécurité liés à l’envoi des données en texte clair doivent être pris en compte avant d’utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3b452-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b452-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b452-130">Requirements</span></span>



| <span data-ttu-id="3b452-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b452-131">Requirement</span></span> | <span data-ttu-id="3b452-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b452-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b452-133">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="3b452-133">TAPI version</span></span><br/> | <span data-ttu-id="3b452-134">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="3b452-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3b452-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b452-135">Header</span></span><br/>       | <dl> <span data-ttu-id="3b452-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b452-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b452-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3b452-137">Library</span></span><br/>      | <dl> <span data-ttu-id="3b452-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b452-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3b452-139">DLL</span><span class="sxs-lookup"><span data-stu-id="3b452-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="3b452-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b452-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b452-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b452-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b452-142">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="3b452-142">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="3b452-143">**ITSdp :: obtient \_ SessionVersion**</span><span class="sxs-lookup"><span data-stu-id="3b452-143">**ITSdp::get\_SessionVersion**</span></span>](itsdp-get-sessionversion.md)
</dt> </dl>

 

 




