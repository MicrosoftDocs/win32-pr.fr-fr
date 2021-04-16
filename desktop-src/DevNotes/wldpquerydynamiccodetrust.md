---
description: Récupère une valeur qui détermine si le code dynamique de la liste de révocation de certificats .NET en mémoire ou sur disque spécifié est approuvé par la stratégie Device Guard.
ms.assetid: 9C12894D-98AF-4408-A11A-865E4DA1DA68
title: WldpQueryDynamicCodeTrust, fonction (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 1b9b3cc30f5a02ae86fd8a30043a9ab417ec1ac7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523468"
---
# <a name="wldpquerydynamiccodetrust-function"></a><span data-ttu-id="ff98b-103">WldpQueryDynamicCodeTrust fonction)</span><span class="sxs-lookup"><span data-stu-id="ff98b-103">WldpQueryDynamicCodeTrust function</span></span>

<span data-ttu-id="ff98b-104">Récupère une valeur qui détermine si le code dynamique de la liste de révocation de certificats .NET en mémoire ou sur disque spécifié est approuvé par la stratégie Device Guard.</span><span class="sxs-lookup"><span data-stu-id="ff98b-104">Retrieves a value that determines if the specified in-memory or on-disk .NET CRL dynamic code is trusted by Device Guard policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff98b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff98b-105">Syntax</span></span>


```C++
HRESULT WINAPI WldpQueryDynamicCodeTrust(
   _When_(baseImage != NULL, _In_opt_)
    _When_(baseImage == NULL, _In_)
    HANDLE                                                 fileHandle,
   _When_(fileHandle == NULL, _In_reads_bytes_opt_(imageSize))
    _When_(fileHandle != NULL, _In_reads_bytes_(imageSize))
    PVOID  baseImage,
   _In_ ULONG                                                                                                                         ImageSize
);
```



## <a name="parameters"></a><span data-ttu-id="ff98b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff98b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff98b-107">*fileHandle*</span><span class="sxs-lookup"><span data-stu-id="ff98b-107">*fileHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="ff98b-108">Handle vers le fichier de code dynamique sur disque à vérifier.</span><span class="sxs-lookup"><span data-stu-id="ff98b-108">Handle to the on-disk dynamic code file to check.</span></span> <span data-ttu-id="ff98b-109">Si *fileHandle* n’a pas la **valeur null**, *BaseImage* doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ff98b-109">If *fileHandle* is non-**NULL**, *baseImage* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ff98b-110">*baseImage*</span><span class="sxs-lookup"><span data-stu-id="ff98b-110">*baseImage*</span></span> 
</dt> <dd>

<span data-ttu-id="ff98b-111">Pointeur vers le fichier PE en mémoire à vérifier.</span><span class="sxs-lookup"><span data-stu-id="ff98b-111">Pointer to the in-memory PE file to check.</span></span> <span data-ttu-id="ff98b-112">Si *baseImage* n’a pas la **valeur null**, *FileHandle* doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ff98b-112">If *baseImage* is non-**NULL**, *FileHandle* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ff98b-113">*ImageSize*</span><span class="sxs-lookup"><span data-stu-id="ff98b-113">*ImageSize*</span></span> 
</dt> <dd>

<span data-ttu-id="ff98b-114">Lorsque *baseImage* est non **null**, indique la taille de la mémoire tampon vers laquelle pointe *baseImage* .</span><span class="sxs-lookup"><span data-stu-id="ff98b-114">When *baseImage* is non-**NULL**, indicates the buffer size that *baseImage* points to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff98b-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ff98b-115">Return value</span></span>

<span data-ttu-id="ff98b-116">Cette méthode retourne **S \_ OK** en cas de réussite ou un code d’échec dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ff98b-116">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff98b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff98b-117">Requirements</span></span>



| <span data-ttu-id="ff98b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff98b-118">Requirement</span></span> | <span data-ttu-id="ff98b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff98b-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ff98b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff98b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ff98b-121">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff98b-121">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ff98b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff98b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ff98b-123">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff98b-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ff98b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff98b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff98b-125"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff98b-125"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ff98b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ff98b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff98b-127"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff98b-127"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




