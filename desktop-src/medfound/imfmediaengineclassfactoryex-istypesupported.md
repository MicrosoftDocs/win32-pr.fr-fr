---
description: Obtient une valeur qui indique si le système de clés spécifié prend en charge le type de média spécifié.
ms.assetid: 6f4f50db-e491-46c2-a8b2-1b8e51033b5b
title: 'IMFMediaEngineClassFactoryEx :: IsTypeSupported, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineClassFactoryEx.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 92bf3d64d36c043e9e33b897294ff74a3fda0445
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106537160"
---
# <a name="imfmediaengineclassfactoryexistypesupported-method"></a><span data-ttu-id="eb123-103">IMFMediaEngineClassFactoryEx :: IsTypeSupported, méthode</span><span class="sxs-lookup"><span data-stu-id="eb123-103">IMFMediaEngineClassFactoryEx::IsTypeSupported method</span></span>

<span data-ttu-id="eb123-104">Obtient une valeur qui indique si le système de clés spécifié prend en charge le type de média spécifié.</span><span class="sxs-lookup"><span data-stu-id="eb123-104">Gets a value that indicates if the specified key system supports the specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb123-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb123-105">Syntax</span></span>


```C++
HRESULT IsTypeSupported(
   BSTR type,
   BSTR keySystem,
   BOOL *isSupported
);
```



## <a name="parameters"></a><span data-ttu-id="eb123-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb123-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb123-107">*type*</span><span class="sxs-lookup"><span data-stu-id="eb123-107">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="eb123-108">Type MIME pour lequel vérifier la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="eb123-108">The MIME type to check support for.</span></span>

</dd> <dt>

<span data-ttu-id="eb123-109">*Système*</span><span class="sxs-lookup"><span data-stu-id="eb123-109">*keySystem*</span></span> 
</dt> <dd>

<span data-ttu-id="eb123-110">Système de clé pour lequel vérifier la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="eb123-110">The key system to check support for.</span></span>

</dd> <dt>

<span data-ttu-id="eb123-111">*isSupported*</span><span class="sxs-lookup"><span data-stu-id="eb123-111">*isSupported*</span></span> 
</dt> <dd>

<span data-ttu-id="eb123-112">**true** si le type est pris en charge par *keysystem*; Sinon, **false.**</span><span class="sxs-lookup"><span data-stu-id="eb123-112">**true** if type is supported by *keySystem*; otherwise, **false.**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb123-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb123-113">Return value</span></span>

<span data-ttu-id="eb123-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="eb123-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eb123-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eb123-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb123-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb123-116">Requirements</span></span>



| <span data-ttu-id="eb123-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb123-117">Requirement</span></span> | <span data-ttu-id="eb123-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb123-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb123-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb123-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eb123-120">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb123-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="eb123-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb123-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eb123-122">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb123-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="eb123-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="eb123-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eb123-124"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eb123-124"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb123-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb123-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb123-126">**IMFMediaEngineClassFactoryEx**</span><span class="sxs-lookup"><span data-stu-id="eb123-126">**IMFMediaEngineClassFactoryEx**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex)
</dt> </dl>

 

 




