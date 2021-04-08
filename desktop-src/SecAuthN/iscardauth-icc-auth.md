---
description: La \_ méthode d’authentification ICC permet à une application d’authentifier la carte à puce.
ms.assetid: 98aea241-6bdc-4f47-b56c-a90f69fcd9a4
title: 'ISCardAuth :: ICC_Auth, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.ICC_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: 015b5c395f025abea4ab2dc756c03691bbc27e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951124"
---
# <a name="iscardauthicc_auth-method"></a><span data-ttu-id="ac058-103">ISCardAuth :: ICC, \_ méthode d’authentification</span><span class="sxs-lookup"><span data-stu-id="ac058-103">ISCardAuth::ICC\_Auth method</span></span>

<span data-ttu-id="ac058-104">\[La méthode d' **\_ authentification ICC** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="ac058-104">\[The **ICC\_Auth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ac058-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ac058-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ac058-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="ac058-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ac058-107">La méthode d' **\_ authentification ICC** permet à une application d’authentifier la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="ac058-107">The **ICC\_Auth** method allows an application to authenticate the smart card.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac058-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac058-108">Syntax</span></span>


```C++
HRESULT ICC_Auth(
  [in]      LONG         lAlgoID,
  [in]      LPBYTEBUFFER pParam,
  [in, out] LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="ac058-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac058-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac058-110">*lAlgoID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ac058-110">*lAlgoID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac058-111">Algorithme à utiliser dans le processus d’authentification.</span><span class="sxs-lookup"><span data-stu-id="ac058-111">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="ac058-112">*pParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ac058-112">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac058-113">Objet [**IByteBuffer**](ibytebuffer.md) contenant les paramètres spécifiques au fournisseur du processus d’authentification.</span><span class="sxs-lookup"><span data-stu-id="ac058-113">An [**IByteBuffer**](ibytebuffer.md) object containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="ac058-114">*pbuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ac058-114">*pBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac058-115">En entrée, contient les données à utiliser dans le processus d’authentification.</span><span class="sxs-lookup"><span data-stu-id="ac058-115">On input, contains data to be used in the authentication process.</span></span>

<span data-ttu-id="ac058-116">Lors de la sortie, contient le résultat du processus d’authentification.</span><span class="sxs-lookup"><span data-stu-id="ac058-116">On output, contains the result of the authentication process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac058-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ac058-117">Return value</span></span>

<span data-ttu-id="ac058-118">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="ac058-118">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ac058-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ac058-119">Return code</span></span>                                                                                   | <span data-ttu-id="ac058-120">Description</span><span class="sxs-lookup"><span data-stu-id="ac058-120">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ac058-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ac058-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ac058-122">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="ac058-122">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="ac058-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ac058-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ac058-124">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="ac058-124">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="ac058-125"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="ac058-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ac058-126">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="ac058-126">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="ac058-127"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="ac058-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ac058-128">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="ac058-128">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="ac058-129">Notes</span><span class="sxs-lookup"><span data-stu-id="ac058-129">Remarks</span></span>

<span data-ttu-id="ac058-130">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardAuth**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="ac058-130">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="ac058-131">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="ac058-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ac058-132">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ac058-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac058-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac058-133">Requirements</span></span>



| <span data-ttu-id="ac058-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac058-134">Requirement</span></span> | <span data-ttu-id="ac058-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac058-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ac058-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac058-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ac058-137">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac058-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="ac058-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac058-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ac058-139">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac058-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ac058-140">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="ac058-140">End of client support</span></span><br/>    | <span data-ttu-id="ac058-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ac058-141">Windows XP</span></span><br/>                                |
| <span data-ttu-id="ac058-142">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="ac058-142">End of server support</span></span><br/>    | <span data-ttu-id="ac058-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ac058-143">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="ac058-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac058-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac058-145">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="ac058-145">**ISCardAuth**</span></span>](iscardauth.md)
</dt> </dl>

 

 
