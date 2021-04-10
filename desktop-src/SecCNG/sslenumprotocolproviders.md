---
description: Retourne un tableau de fournisseurs de protocoles SSL (SSL (Secure Sockets Layer) Protocole) installés.
ms.assetid: a61ddcf5-b7e3-40b2-82fc-1cf87eb963ec
title: SslEnumProtocolProviders, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumProtocolProviders
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 94c8648950af20a97bcc34b614aee0d0f716b043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210753"
---
# <a name="sslenumprotocolproviders-function"></a><span data-ttu-id="c87b7-103">SslEnumProtocolProviders fonction)</span><span class="sxs-lookup"><span data-stu-id="c87b7-103">SslEnumProtocolProviders function</span></span>

<span data-ttu-id="c87b7-104">La fonction **SslEnumProtocolProviders** retourne un tableau de fournisseurs de protocole SSL ( [*SSL (Secure Sockets Layer) protocole*](/windows/desktop/SecGloss/s-gly) ) installés.</span><span class="sxs-lookup"><span data-stu-id="c87b7-104">The **SslEnumProtocolProviders** function returns an array of installed [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol providers.</span></span>

## <a name="syntax"></a><span data-ttu-id="c87b7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c87b7-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslEnumProtocolProviders(
  _Out_ DWORD              *pdwProviderCount,
  _Out_ NCryptProviderName **ppProviderList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="c87b7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c87b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c87b7-107">*pdwProviderCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c87b7-107">*pdwProviderCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c87b7-108">Pointeur vers une valeur **DWORD** pour recevoir le nombre de fournisseurs de protocole retourné.</span><span class="sxs-lookup"><span data-stu-id="c87b7-108">A pointer to a **DWORD** value to receive the number of protocol providers returned.</span></span>

</dd> <dt>

<span data-ttu-id="c87b7-109">*ppProviderList* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c87b7-109">*ppProviderList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c87b7-110">Pointeur vers une mémoire tampon qui reçoit le tableau de structures [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) .</span><span class="sxs-lookup"><span data-stu-id="c87b7-110">A pointer to a buffer that receives the array of [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) structures.</span></span>

</dd> <dt>

<span data-ttu-id="c87b7-111">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c87b7-111">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c87b7-112">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="c87b7-112">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c87b7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c87b7-113">Return value</span></span>

<span data-ttu-id="c87b7-114">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="c87b7-114">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="c87b7-115">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="c87b7-115">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="c87b7-116">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="c87b7-116">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="c87b7-117">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c87b7-117">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="c87b7-118">Description</span><span class="sxs-lookup"><span data-stu-id="c87b7-118">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c87b7-119"><dt>**NPD \_ \_Indicateurs INcorrects**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="c87b7-119"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="c87b7-120">Le paramètre *dwFlags* n’est pas égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="c87b7-120">The *dwFlags* parameter is not zero.</span></span><br/>                              |
| <dl> <span data-ttu-id="c87b7-121"><dt>**NPD \_ AUCUNE \_ mémoire**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="c87b7-121"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="c87b7-122">La mémoire disponible est insuffisante pour allouer les tampons nécessaires.</span><span class="sxs-lookup"><span data-stu-id="c87b7-122">Not enough memory is available to allocate necessary buffers.</span></span><br/>     |
| <dl> <span data-ttu-id="c87b7-123"><dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c87b7-123"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="c87b7-124">Le paramètre *pdwProviderCount* ou *PpProviderList* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c87b7-124">The *pdwProviderCount* or *ppProviderList* parameter is **NULL**.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c87b7-125">Notes</span><span class="sxs-lookup"><span data-stu-id="c87b7-125">Remarks</span></span>

<span data-ttu-id="c87b7-126">Lorsque vous avez fini d’utiliser le tableau de structures [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) , appelez la fonction [**SslFreeBuffer**](sslfreebuffer.md) pour libérer le tableau.</span><span class="sxs-lookup"><span data-stu-id="c87b7-126">When you have finished using the array of [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) structures, call the [**SslFreeBuffer**](sslfreebuffer.md) function to free the array.</span></span>

## <a name="requirements"></a><span data-ttu-id="c87b7-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c87b7-127">Requirements</span></span>



| <span data-ttu-id="c87b7-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c87b7-128">Requirement</span></span> | <span data-ttu-id="c87b7-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="c87b7-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c87b7-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c87b7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c87b7-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c87b7-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c87b7-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c87b7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c87b7-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c87b7-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c87b7-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="c87b7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c87b7-135"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="c87b7-135"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="c87b7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c87b7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c87b7-137"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c87b7-137"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

