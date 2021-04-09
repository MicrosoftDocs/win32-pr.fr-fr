---
description: La \_ méthode d’authentification utilisateur autorise l’accès aux services d’authentification des utilisateurs.
ms.assetid: 110da052-c581-46bc-8e81-5be112ee9b43
title: 'ISCardAuth :: User_Auth, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.User_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae810f93c322449109576b37f01afa4f277fc32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862406"
---
# <a name="iscardauthuser_auth-method"></a><span data-ttu-id="289e4-103">ISCardAuth :: User \_ auth, méthode</span><span class="sxs-lookup"><span data-stu-id="289e4-103">ISCardAuth::User\_Auth method</span></span>

<span data-ttu-id="289e4-104">\[La méthode d' **\_ authentification utilisateur** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="289e4-104">\[The **User\_Auth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="289e4-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="289e4-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="289e4-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="289e4-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="289e4-107">La **méthode \_ d’authentification utilisateur** autorise l’accès aux services d’authentification des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="289e4-107">The **User\_Auth** method allows access to user authentication services.</span></span>

## <a name="syntax"></a><span data-ttu-id="289e4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="289e4-108">Syntax</span></span>


```C++
HRESULT User_Auth(
  [in] LONG         lAlgorID,
  [in] LPBYTEBUFFER pParam,
  [in] LPBYTEBUFFER pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="289e4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="289e4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="289e4-110">*lAlgorID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="289e4-110">*lAlgorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="289e4-111">Algorithme à utiliser dans le processus d’authentification.</span><span class="sxs-lookup"><span data-stu-id="289e4-111">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="289e4-112">*pParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="289e4-112">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="289e4-113">Objet [**IByteBuffer**](ibytebuffer.md) contenant les paramètres spécifiques au fournisseur du processus d’authentification.</span><span class="sxs-lookup"><span data-stu-id="289e4-113">An [**IByteBuffer**](ibytebuffer.md) object containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="289e4-114">*pbuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="289e4-114">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="289e4-115">Données à utiliser dans le processus d’authentification.</span><span class="sxs-lookup"><span data-stu-id="289e4-115">Data to be used in the authentication process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="289e4-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="289e4-116">Return value</span></span>

<span data-ttu-id="289e4-117">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="289e4-117">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="289e4-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="289e4-118">Return code</span></span>                                                                                   | <span data-ttu-id="289e4-119">Description</span><span class="sxs-lookup"><span data-stu-id="289e4-119">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="289e4-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="289e4-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="289e4-121">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="289e4-121">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="289e4-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="289e4-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="289e4-123">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="289e4-123">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="289e4-124"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="289e4-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="289e4-125">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="289e4-125">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="289e4-126"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="289e4-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="289e4-127">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="289e4-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="289e4-128">Notes</span><span class="sxs-lookup"><span data-stu-id="289e4-128">Remarks</span></span>

<span data-ttu-id="289e4-129">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardAuth**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="289e4-129">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="289e4-130">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="289e4-130">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="289e4-131">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="289e4-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="289e4-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="289e4-132">Requirements</span></span>



| <span data-ttu-id="289e4-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="289e4-133">Requirement</span></span> | <span data-ttu-id="289e4-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="289e4-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="289e4-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="289e4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="289e4-136">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="289e4-136">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="289e4-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="289e4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="289e4-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="289e4-138">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="289e4-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="289e4-139">End of client support</span></span><br/>    | <span data-ttu-id="289e4-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="289e4-140">Windows XP</span></span><br/>                                |
| <span data-ttu-id="289e4-141">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="289e4-141">End of server support</span></span><br/>    | <span data-ttu-id="289e4-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="289e4-142">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="289e4-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="289e4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="289e4-144">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="289e4-144">**ISCardAuth**</span></span>](iscardauth.md)
</dt> <dt>

[<span data-ttu-id="289e4-145">**IByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="289e4-145">**IByteBuffer**</span></span>](ibytebuffer.md)
</dt> </dl>

 

 
