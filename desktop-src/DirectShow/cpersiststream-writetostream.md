---
description: Écrit les données du filtre dans le flux donné.
ms.assetid: 1b405050-6cfd-4b69-b449-f00a6ecfac6a
title: Méthode CPersistStream. WriteToStream (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.WriteToStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 893d58986db92e50cbafefe74676481162808abf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526726"
---
# <a name="cpersiststreamwritetostream-method"></a><span data-ttu-id="2497b-103">Méthode CPersistStream. WriteToStream</span><span class="sxs-lookup"><span data-stu-id="2497b-103">CPersistStream.WriteToStream method</span></span>

<span data-ttu-id="2497b-104">Écrit les données du filtre dans le flux donné.</span><span class="sxs-lookup"><span data-stu-id="2497b-104">Writes the filter's data to the given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="2497b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2497b-105">Syntax</span></span>


```C++
virtual HRESULT WriteToStream(
   IStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="2497b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2497b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2497b-107">*pStream*</span><span class="sxs-lookup"><span data-stu-id="2497b-107">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="2497b-108">Pointeur vers une interface **IStream** qui spécifie le flux de destination des données de filtre.</span><span class="sxs-lookup"><span data-stu-id="2497b-108">Pointer to an **IStream** interface that specifies the filter data's destination stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2497b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2497b-109">Return value</span></span>

<span data-ttu-id="2497b-110">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2497b-110">Returns S\_OK.</span></span> <span data-ttu-id="2497b-111">La classe dérivée doit retourner une valeur **HRESULT** valide.</span><span class="sxs-lookup"><span data-stu-id="2497b-111">The derived class should return a valid **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2497b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="2497b-112">Remarks</span></span>

<span data-ttu-id="2497b-113">La version par défaut n’écrit rien. Il peut être substitué pour écrire des données spécifiques à votre classe.</span><span class="sxs-lookup"><span data-stu-id="2497b-113">The default version writes nothing; it can be overridden to write data specific to your class.</span></span>

## <a name="requirements"></a><span data-ttu-id="2497b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2497b-114">Requirements</span></span>



| <span data-ttu-id="2497b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2497b-115">Requirement</span></span> | <span data-ttu-id="2497b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2497b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2497b-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="2497b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2497b-118"><dt>PStream. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2497b-118"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2497b-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2497b-119">Library</span></span><br/> | <dl> <span data-ttu-id="2497b-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2497b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2497b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2497b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2497b-122">**CPersistStream, classe**</span><span class="sxs-lookup"><span data-stu-id="2497b-122">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




