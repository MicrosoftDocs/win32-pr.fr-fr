---
description: Utilisé pour libérer de la mémoire qui a été allouée par l’une des fonctions du fournisseur SSL (SSL (Secure Sockets Layer) Protocol).
ms.assetid: 75a85013-c745-43cb-85b5-e13a2778ec1d
title: SslFreeBuffer, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeBuffer
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: bced83b52ddf37266f64ae0c2b8919902f30fff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042810"
---
# <a name="sslfreebuffer-function"></a><span data-ttu-id="6988e-103">SslFreeBuffer fonction)</span><span class="sxs-lookup"><span data-stu-id="6988e-103">SslFreeBuffer function</span></span>

<span data-ttu-id="6988e-104">La fonction **SslFreeBuffer** est utilisée pour libérer de la mémoire qui a été allouée par l’une des fonctions du fournisseur SSL ( [*SSL (Secure Sockets Layer) Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="6988e-104">The **SslFreeBuffer** function is used to free memory that was allocated by one of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="6988e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6988e-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslFreeBuffer(
  _In_ PVOID pvInput
);
```



## <a name="parameters"></a><span data-ttu-id="6988e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6988e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6988e-107">*pvInput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6988e-107">*pvInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6988e-108">Pointeur vers la mémoire tampon à libérer.</span><span class="sxs-lookup"><span data-stu-id="6988e-108">A pointer to the memory buffer to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6988e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6988e-109">Return value</span></span>

<span data-ttu-id="6988e-110">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="6988e-110">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="6988e-111">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="6988e-111">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="6988e-112">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="6988e-112">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="6988e-113">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="6988e-113">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="6988e-114">Description</span><span class="sxs-lookup"><span data-stu-id="6988e-114">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6988e-115"><dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6988e-115"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="6988e-116">Le paramètre *pdwProviderCount* ou *PpProviderList* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="6988e-116">The *pdwProviderCount* or *ppProviderList* parameter is **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6988e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6988e-117">Requirements</span></span>



| <span data-ttu-id="6988e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6988e-118">Requirement</span></span> | <span data-ttu-id="6988e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6988e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6988e-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6988e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6988e-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6988e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6988e-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6988e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6988e-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6988e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6988e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="6988e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6988e-125"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="6988e-125"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="6988e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6988e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6988e-127"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6988e-127"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

