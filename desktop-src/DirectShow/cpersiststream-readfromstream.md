---
description: Lit les données du filtre à partir du flux donné.
ms.assetid: 009f4812-8cc6-436a-9553-3a3161d5e992
title: Méthode CPersistStream. ReadFromStream (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.ReadFromStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce6c037fbce9fbaeabf7491b1b840000f67e25d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540503"
---
# <a name="cpersiststreamreadfromstream-method"></a><span data-ttu-id="10389-103">Méthode CPersistStream. ReadFromStream</span><span class="sxs-lookup"><span data-stu-id="10389-103">CPersistStream.ReadFromStream method</span></span>

<span data-ttu-id="10389-104">Lit les données du filtre à partir du flux donné.</span><span class="sxs-lookup"><span data-stu-id="10389-104">Reads the filter's data from the given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="10389-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10389-105">Syntax</span></span>


```C++
virtual HRESULT ReadFromStream(
   IStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="10389-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="10389-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10389-107">*pStream*</span><span class="sxs-lookup"><span data-stu-id="10389-107">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="10389-108">Pointeur vers une interface **IStream** à partir de laquelle les données doivent être lues.</span><span class="sxs-lookup"><span data-stu-id="10389-108">Pointer to an **IStream** interface from which data is to be read.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10389-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="10389-109">Return value</span></span>

<span data-ttu-id="10389-110">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="10389-110">Returns S\_OK.</span></span> <span data-ttu-id="10389-111">La classe dérivée doit retourner une valeur **HRESULT** valide.</span><span class="sxs-lookup"><span data-stu-id="10389-111">The derived class should return a valid **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="10389-112">Notes</span><span class="sxs-lookup"><span data-stu-id="10389-112">Remarks</span></span>

<span data-ttu-id="10389-113">La version par défaut ne lit rien ; Il peut être substitué pour lire des données spécifiques à votre classe.</span><span class="sxs-lookup"><span data-stu-id="10389-113">The default version reads nothing; it can be overridden to read data specific to your class.</span></span>

## <a name="requirements"></a><span data-ttu-id="10389-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10389-114">Requirements</span></span>



| <span data-ttu-id="10389-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10389-115">Requirement</span></span> | <span data-ttu-id="10389-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="10389-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10389-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="10389-117">Header</span></span><br/>  | <dl> <span data-ttu-id="10389-118"><dt>PStream. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10389-118"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="10389-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="10389-119">Library</span></span><br/> | <dl> <span data-ttu-id="10389-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="10389-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10389-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10389-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10389-122">**CPersistStream, classe**</span><span class="sxs-lookup"><span data-stu-id="10389-122">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




