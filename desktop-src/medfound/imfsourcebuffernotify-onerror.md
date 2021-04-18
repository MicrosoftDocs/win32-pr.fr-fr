---
description: Permet d’indiquer qu’une erreur s’est produite avec la mémoire tampon source.
ms.assetid: a7187b7a-0090-4380-82bb-a7f72d54232e
title: 'IMFSourceBufferNotify :: OnError, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBufferNotify.OnError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 8b5f48c3517eb62b0a70acb9cbb28a5ecf7c90cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516058"
---
# <a name="imfsourcebuffernotifyonerror-method"></a><span data-ttu-id="b678f-103">IMFSourceBufferNotify :: OnError, méthode</span><span class="sxs-lookup"><span data-stu-id="b678f-103">IMFSourceBufferNotify::OnError method</span></span>

<span data-ttu-id="b678f-104">Permet d’indiquer qu’une erreur s’est produite avec la mémoire tampon source.</span><span class="sxs-lookup"><span data-stu-id="b678f-104">Used to indicate that an error has occurred with the source buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b678f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b678f-105">Syntax</span></span>


```C++
void OnError(
  [in] HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="b678f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b678f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b678f-107">*RH* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b678f-107">*hr* \[in\]</span></span>
<span data-ttu-id="b678f-108"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b678f-108"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="b678f-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b678f-109">Return value</span></span>

<span data-ttu-id="b678f-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b678f-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b678f-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b678f-111">Requirements</span></span>



| <span data-ttu-id="b678f-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b678f-112">Requirement</span></span> | <span data-ttu-id="b678f-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="b678f-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b678f-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b678f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b678f-115">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b678f-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b678f-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b678f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b678f-117">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b678f-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b678f-118">MIDL</span><span class="sxs-lookup"><span data-stu-id="b678f-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b678f-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b678f-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b678f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b678f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b678f-121">**IMFSourceBufferNotify**</span><span class="sxs-lookup"><span data-stu-id="b678f-121">**IMFSourceBufferNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffernotify)
</dt> </dl>

 

 




