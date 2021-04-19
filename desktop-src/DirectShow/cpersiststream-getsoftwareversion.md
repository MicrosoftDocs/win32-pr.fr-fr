---
description: Récupère la version du logiciel pour ce flux.
ms.assetid: f54153df-5593-4784-acc5-3e0dcef424b5
title: Méthode CPersistStream. GetSoftwareVersion (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSoftwareVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0954e9a113342217dd389c64ec4fc6c04a6f767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535248"
---
# <a name="cpersiststreamgetsoftwareversion-method"></a><span data-ttu-id="4325b-103">Méthode CPersistStream. GetSoftwareVersion</span><span class="sxs-lookup"><span data-stu-id="4325b-103">CPersistStream.GetSoftwareVersion method</span></span>

<span data-ttu-id="4325b-104">Récupère la version du logiciel pour ce flux.</span><span class="sxs-lookup"><span data-stu-id="4325b-104">Retrieves the software version for this stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="4325b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4325b-105">Syntax</span></span>


```C++
virtual DWORD GetSoftwareVersion();
```



## <a name="parameters"></a><span data-ttu-id="4325b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4325b-106">Parameters</span></span>

<span data-ttu-id="4325b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4325b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4325b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4325b-108">Return value</span></span>

<span data-ttu-id="4325b-109">Retourne une **valeur DWORD** contenant le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="4325b-109">Returns a **DWORD** containing the version number.</span></span> <span data-ttu-id="4325b-110">Chaque fois que le format du flux est modifié, cette fonction doit être modifiée pour retourner un nombre plus élevé qu’avant.</span><span class="sxs-lookup"><span data-stu-id="4325b-110">Each time the format of the stream is changed, this function should be altered to return a larger number than before.</span></span>

## <a name="requirements"></a><span data-ttu-id="4325b-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4325b-111">Requirements</span></span>



| <span data-ttu-id="4325b-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4325b-112">Requirement</span></span> | <span data-ttu-id="4325b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="4325b-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4325b-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="4325b-114">Header</span></span><br/>  | <dl> <span data-ttu-id="4325b-115"><dt>PStream. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4325b-115"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4325b-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4325b-116">Library</span></span><br/> | <dl> <span data-ttu-id="4325b-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4325b-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4325b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4325b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4325b-119">**CPersistStream, classe**</span><span class="sxs-lookup"><span data-stu-id="4325b-119">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




