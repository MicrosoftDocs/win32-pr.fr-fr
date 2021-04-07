---
description: La méthode d’authentification d’application \_ authentifie l’application. Il permet à une application de s’authentifier elle-même (à l’aide d’un protocole de stimulation/signature) lorsque l’authentification est demandée par une carte à puce.
ms.assetid: 0b86ce09-ca17-4d74-bc14-46b17262e669
title: 'ISCardAuth :: APP_Auth, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.APP_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: 792cd1b43a43f020e62e87048741935a82da28dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863533"
---
# <a name="iscardauthapp_auth-method"></a><span data-ttu-id="506bd-104">ISCardAuth :: APP, \_ méthode d’authentification</span><span class="sxs-lookup"><span data-stu-id="506bd-104">ISCardAuth::APP\_Auth method</span></span>

<span data-ttu-id="506bd-105">\[La méthode d' **\_ authentification d’application** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="506bd-105">\[The **APP\_Auth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="506bd-106">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="506bd-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="506bd-107">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="506bd-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="506bd-108">La méthode d' **\_ authentification d’application** authentifie l’application.</span><span class="sxs-lookup"><span data-stu-id="506bd-108">The **APP\_Auth** method authenticates the application.</span></span> <span data-ttu-id="506bd-109">Il permet à une application de s’authentifier elle-même (à l’aide d’un protocole de stimulation/signature) lorsque l’authentification est demandée par une [*carte à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="506bd-109">It allows an application to authenticate itself (using a challenge/signature protocol) when authentication is requested by a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="506bd-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="506bd-110">Syntax</span></span>


```C++
HRESULT APP_Auth(
  [in] LONG         lAlgoID,
  [in] LPBYTEBUFFER pParam,
  [in] LPBYTEBUFFER pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="506bd-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="506bd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="506bd-112">*lAlgoID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="506bd-112">*lAlgoID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="506bd-113">Algorithme à utiliser dans le processus d’authentification.</span><span class="sxs-lookup"><span data-stu-id="506bd-113">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="506bd-114">*pParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="506bd-114">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="506bd-115">[**IByteBuffer**](ibytebuffer.md) contenant des paramètres spécifiques au fournisseur du processus d’authentification.</span><span class="sxs-lookup"><span data-stu-id="506bd-115">An [**IByteBuffer**](ibytebuffer.md) containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="506bd-116">*pbuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="506bd-116">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="506bd-117">Données requises pour le calcul.</span><span class="sxs-lookup"><span data-stu-id="506bd-117">Data required for the calculation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="506bd-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="506bd-118">Return value</span></span>

<span data-ttu-id="506bd-119">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="506bd-119">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="506bd-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="506bd-120">Return code</span></span>                                                                                   | <span data-ttu-id="506bd-121">Description</span><span class="sxs-lookup"><span data-stu-id="506bd-121">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="506bd-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="506bd-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="506bd-123">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="506bd-123">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="506bd-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="506bd-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="506bd-125">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="506bd-125">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="506bd-126"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="506bd-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="506bd-127">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="506bd-127">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="506bd-128"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="506bd-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="506bd-129">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="506bd-129">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="506bd-130">Notes</span><span class="sxs-lookup"><span data-stu-id="506bd-130">Remarks</span></span>

<span data-ttu-id="506bd-131">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardAuth**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="506bd-131">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="506bd-132">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="506bd-132">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="506bd-133">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="506bd-133">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="506bd-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="506bd-134">Requirements</span></span>



| <span data-ttu-id="506bd-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="506bd-135">Requirement</span></span> | <span data-ttu-id="506bd-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="506bd-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="506bd-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="506bd-137">Minimum supported client</span></span><br/> | <span data-ttu-id="506bd-138">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="506bd-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="506bd-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="506bd-139">Minimum supported server</span></span><br/> | <span data-ttu-id="506bd-140">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="506bd-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="506bd-141">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="506bd-141">End of client support</span></span><br/>    | <span data-ttu-id="506bd-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="506bd-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="506bd-143">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="506bd-143">End of server support</span></span><br/>    | <span data-ttu-id="506bd-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="506bd-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="506bd-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="506bd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="506bd-146">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="506bd-146">**ISCardAuth**</span></span>](iscardauth.md)
</dt> <dt>

[<span data-ttu-id="506bd-147">**IByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="506bd-147">**IByteBuffer**</span></span>](ibytebuffer.md)
</dt> </dl>

 

 
