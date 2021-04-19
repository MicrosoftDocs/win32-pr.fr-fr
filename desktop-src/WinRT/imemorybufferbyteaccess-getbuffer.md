---
description: Obtient un IMemoryBuffer sous la forme d’un tableau d’octets.
ms.assetid: E9C2AF2D-ADBE-4D76-A549-2DBCB9818B09
title: 'IMemoryBufferByteAccess :: GetBuffer, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMemoryBufferByteAccess.GetBuffer
api_type:
- COM
api_location: ''
ms.openlocfilehash: f31d1506822f21977e2d60492248c2d70a51829c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516664"
---
# <a name="imemorybufferbyteaccessgetbuffer-method"></a><span data-ttu-id="fa165-103">IMemoryBufferByteAccess :: GetBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="fa165-103">IMemoryBufferByteAccess::GetBuffer method</span></span>

<span data-ttu-id="fa165-104">Obtient un [**IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) sous la forme d’un tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="fa165-104">Gets an [**IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) as an array of bytes.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa165-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa165-105">Syntax</span></span>


```C++
HRESULT GetBuffer(
  [out] BYTE   **value,
  [out] UINT32 *capacity
);
```



## <a name="parameters"></a><span data-ttu-id="fa165-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa165-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa165-107">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fa165-107">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa165-108">Pointeur vers un tableau d’octets contenant les données de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="fa165-108">A pointer to a byte array containing the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="fa165-109">*capacité* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fa165-109">*capacity* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa165-110">Nombre d’octets dans le tableau retourné</span><span class="sxs-lookup"><span data-stu-id="fa165-110">The number of bytes in the returned array</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa165-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa165-111">Return value</span></span>

<span data-ttu-id="fa165-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fa165-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fa165-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fa165-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa165-114">Notes</span><span class="sxs-lookup"><span data-stu-id="fa165-114">Remarks</span></span>

<span data-ttu-id="fa165-115">Quand [**MemoryBuffer :: Close**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) est appelé, le code qui utilise cette mémoire tampon doit définir le pointeur de *valeur* sur null.</span><span class="sxs-lookup"><span data-stu-id="fa165-115">When [**MemoryBuffer::Close**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) is called, the code using this buffer should set the *value* pointer to null.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa165-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa165-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="fa165-117">[**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fa165-117">[**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85))</span></span>
</dt> </dl>

 

 
