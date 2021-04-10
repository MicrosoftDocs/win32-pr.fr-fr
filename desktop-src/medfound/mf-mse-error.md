---
description: Définit les différents États d’erreur de l’extension de source de média.
ms.assetid: 8FD54833-F60B-49E8-A673-6130F3B06160
title: Énumération MF_MSE_ERROR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_ERROR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 6b6aaea772376b0e57c006a56a5a1bb30bc497c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114602"
---
# <a name="mf_mse_error-enumeration"></a><span data-ttu-id="716d7-103">\_Énumération des erreurs de MSE MF \_</span><span class="sxs-lookup"><span data-stu-id="716d7-103">MF\_MSE\_ERROR enumeration</span></span>

<span data-ttu-id="716d7-104">Définit les différents États d’erreur de l’extension de source de média.</span><span class="sxs-lookup"><span data-stu-id="716d7-104">Defines the different error states of the Media Source Extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="716d7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="716d7-105">Syntax</span></span>


```C++
typedef enum _MF_MSE_ERROR { 
  MF_MSE_ERROR_NOERROR        =  0,
  MF_MSE_ERROR_NETWORK        = 1,
  MF_MSE_ERROR_DECODE         = 2,
  MF_MSE_ERROR_UNKNOWN_ERROR  =  3
} MF_MSE_ERROR;
```



## <a name="constants"></a><span data-ttu-id="716d7-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="716d7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="716d7-107"><span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**\_erreur MF MSE \_ erreur \_**</span><span class="sxs-lookup"><span data-stu-id="716d7-107"><span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**MF\_MSE\_ERROR\_NOERROR**</span></span>
</dt> <dd>

<span data-ttu-id="716d7-108">Ne spécifie aucune erreur.</span><span class="sxs-lookup"><span data-stu-id="716d7-108">Specifies no error.</span></span>

</dd> <dt>

<span data-ttu-id="716d7-109"><span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**\_réseau d' \_ Erreurs MF MSE \_**</span><span class="sxs-lookup"><span data-stu-id="716d7-109"><span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**MF\_MSE\_ERROR\_NETWORK**</span></span>
</dt> <dd>

<span data-ttu-id="716d7-110">Spécifie une erreur avec le réseau.</span><span class="sxs-lookup"><span data-stu-id="716d7-110">Specifies an error with the network.</span></span>

</dd> <dt>

<span data-ttu-id="716d7-111"><span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**\_code d' \_ erreur MF MSE \_**</span><span class="sxs-lookup"><span data-stu-id="716d7-111"><span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**MF\_MSE\_ERROR\_DECODE**</span></span>
</dt> <dd>

<span data-ttu-id="716d7-112">Spécifie une erreur de décodage.</span><span class="sxs-lookup"><span data-stu-id="716d7-112">Specifies an error with decoding.</span></span>

</dd> <dt>

<span data-ttu-id="716d7-113"><span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**erreur MF \_ MSE \_ erreur \_ inconnue \_**</span><span class="sxs-lookup"><span data-stu-id="716d7-113"><span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**MF\_MSE\_ERROR\_UNKNOWN\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="716d7-114">Spécifie une erreur inconnue.</span><span class="sxs-lookup"><span data-stu-id="716d7-114">Specifies an unknown error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="716d7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="716d7-115">Requirements</span></span>



| <span data-ttu-id="716d7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="716d7-116">Requirement</span></span> | <span data-ttu-id="716d7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="716d7-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="716d7-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="716d7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="716d7-119">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="716d7-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="716d7-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="716d7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="716d7-121">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="716d7-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="716d7-122">MIDL</span><span class="sxs-lookup"><span data-stu-id="716d7-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="716d7-123"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="716d7-123"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="716d7-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="716d7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="716d7-125">Énumérations de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="716d7-125">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




