---
description: Récupère la taille maximale en octets nécessaire pour le flux actuel, y compris le numéro de version.
ms.assetid: 55ea4568-5ca4-4139-8def-bef20071835d
title: Méthode CPersistStream. GetSizeMax (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ef9fcd176463aa8b0bc69fabbd74d78d4ca17cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530546"
---
# <a name="cpersiststreamgetsizemax-method"></a><span data-ttu-id="99233-103">Méthode CPersistStream. GetSizeMax</span><span class="sxs-lookup"><span data-stu-id="99233-103">CPersistStream.GetSizeMax method</span></span>

<span data-ttu-id="99233-104">Récupère la taille maximale en octets nécessaire pour le flux actuel, y compris le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="99233-104">Retrieves the maximum byte size needed for the current stream, including the version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="99233-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99233-105">Syntax</span></span>


```C++
HRESULT GetSizeMax(
   ULARGE_INTEGER *pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="99233-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99233-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99233-107">*PCB*</span><span class="sxs-lookup"><span data-stu-id="99233-107">*pcbSize*</span></span> 
</dt> <dd>

<span data-ttu-id="99233-108">Pointeur vers la taille en octets nécessaire pour enregistrer ce flux, y compris le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="99233-108">Pointer to the size in bytes needed to save this stream, including the version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99233-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="99233-109">Return value</span></span>

<span data-ttu-id="99233-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="99233-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="99233-111">Notes</span><span class="sxs-lookup"><span data-stu-id="99233-111">Remarks</span></span>

<span data-ttu-id="99233-112">Cette fonction membre implémente la méthode **IPersistStream :: GetSizeMax** .</span><span class="sxs-lookup"><span data-stu-id="99233-112">This member function implements the **IPersistStream::GetSizeMax** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="99233-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99233-113">Requirements</span></span>



| <span data-ttu-id="99233-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99233-114">Requirement</span></span> | <span data-ttu-id="99233-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="99233-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99233-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="99233-116">Header</span></span><br/>  | <dl> <span data-ttu-id="99233-117"><dt>PStream. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99233-117"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="99233-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="99233-118">Library</span></span><br/> | <dl> <span data-ttu-id="99233-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="99233-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99233-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99233-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99233-121">**CPersistStream, classe**</span><span class="sxs-lookup"><span data-stu-id="99233-121">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




