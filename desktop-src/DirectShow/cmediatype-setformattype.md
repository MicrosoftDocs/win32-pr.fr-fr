---
description: La méthode SetFormatType spécifie le type de format.
ms.assetid: e8ed9190-7169-4d51-ace7-597f43ff083e
title: Méthode CMediaType. SetFormatType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormatType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7843c5a9788545909ef4297accfa342c08b71e88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537572"
---
# <a name="cmediatypesetformattype-method"></a><span data-ttu-id="d14f1-103">Méthode CMediaType. SetFormatType</span><span class="sxs-lookup"><span data-stu-id="d14f1-103">CMediaType.SetFormatType method</span></span>

<span data-ttu-id="d14f1-104">La méthode SetFormatType «» spécifie le type de format.</span><span class="sxs-lookup"><span data-stu-id="d14f1-104">The \`\`SetFormatType method specifies the format type.</span></span>

## <a name="syntax"></a><span data-ttu-id="d14f1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d14f1-105">Syntax</span></span>


```C++
void SetFormatType(
   const GUID *pformattype
);
```



## <a name="parameters"></a><span data-ttu-id="d14f1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d14f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d14f1-107">*pformattype*</span><span class="sxs-lookup"><span data-stu-id="d14f1-107">*pformattype*</span></span> 
</dt> <dd>

<span data-ttu-id="d14f1-108">Pointeur vers un **GUID** qui spécifie le type de format.</span><span class="sxs-lookup"><span data-stu-id="d14f1-108">Pointer to a **GUID** that specifies the format type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d14f1-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d14f1-109">Return value</span></span>

<span data-ttu-id="d14f1-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d14f1-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d14f1-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d14f1-111">Remarks</span></span>

<span data-ttu-id="d14f1-112">Cette méthode définit le membre **formatType** .</span><span class="sxs-lookup"><span data-stu-id="d14f1-112">This method sets the **formattype** member.</span></span> <span data-ttu-id="d14f1-113">Le type de format définit la disposition du bloc de format.</span><span class="sxs-lookup"><span data-stu-id="d14f1-113">The format type defines the layout of the format block.</span></span> <span data-ttu-id="d14f1-114">Par exemple, si le type de format est \_ VIDEOINFO format, le bloc de format doit contenir une structure **VIDEOINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="d14f1-114">For example, if the format type is FORMAT\_VideoInfo, the format block should contain a **VIDEOINFOHEADER** structure.</span></span> <span data-ttu-id="d14f1-115">Pour définir le bloc de format, appelez la méthode [**CMediaType :: SetFormat**](cmediatype-setformat.md) .</span><span class="sxs-lookup"><span data-stu-id="d14f1-115">To set the format block, call the [**CMediaType::SetFormat**](cmediatype-setformat.md) method.</span></span> <span data-ttu-id="d14f1-116">L’appelant est chargé de s’assurer que le bloc de format correspond au type de format.</span><span class="sxs-lookup"><span data-stu-id="d14f1-116">The caller is responsible for making sure that the format block matches the format type.</span></span>

## <a name="requirements"></a><span data-ttu-id="d14f1-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d14f1-117">Requirements</span></span>



| <span data-ttu-id="d14f1-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d14f1-118">Requirement</span></span> | <span data-ttu-id="d14f1-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d14f1-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d14f1-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d14f1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d14f1-121"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d14f1-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="d14f1-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d14f1-122">Library</span></span><br/> | <dl> <span data-ttu-id="d14f1-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d14f1-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d14f1-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d14f1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d14f1-125">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="d14f1-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 


``
