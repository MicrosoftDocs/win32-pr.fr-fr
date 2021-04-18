---
description: Obtient une valeur qui indique si le type MIME spécifié est pris en charge par la source du média.
ms.assetid: 894ef7d2-d008-42e1-8a61-26f35a8877be
title: 'IMFMediaSourceExtension :: IsTypeSupported, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 4c2784dc4e97f96ae28ba56544a7f425de8ce742
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106523108"
---
# <a name="imfmediasourceextensionistypesupported-method"></a><span data-ttu-id="2cc53-103">IMFMediaSourceExtension :: IsTypeSupported, méthode</span><span class="sxs-lookup"><span data-stu-id="2cc53-103">IMFMediaSourceExtension::IsTypeSupported method</span></span>

<span data-ttu-id="2cc53-104">Obtient une valeur qui indique si le type MIME spécifié est pris en charge par la source du média.</span><span class="sxs-lookup"><span data-stu-id="2cc53-104">Gets a value that indicates if the specified MIME type is supported by the media source.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cc53-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2cc53-105">Syntax</span></span>


```C++
BOOL IsTypeSupported(
  [in] BSTR type
);
```



## <a name="parameters"></a><span data-ttu-id="2cc53-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2cc53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cc53-107">*type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2cc53-107">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cc53-108">Type de média pour lequel vérifier la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2cc53-108">The media type to check support for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cc53-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2cc53-109">Return value</span></span>

<span data-ttu-id="2cc53-110">**true** si le type de média est pris en charge ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="2cc53-110">**true** if the media type is supported; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cc53-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2cc53-111">Requirements</span></span>



| <span data-ttu-id="2cc53-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2cc53-112">Requirement</span></span> | <span data-ttu-id="2cc53-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="2cc53-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cc53-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2cc53-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2cc53-115">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2cc53-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2cc53-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2cc53-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2cc53-117">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2cc53-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2cc53-118">MIDL</span><span class="sxs-lookup"><span data-stu-id="2cc53-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2cc53-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2cc53-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cc53-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2cc53-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cc53-121">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="2cc53-121">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




