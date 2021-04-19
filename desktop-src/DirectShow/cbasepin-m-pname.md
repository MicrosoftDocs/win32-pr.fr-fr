---
description: Nom du code confidentiel.
ms.assetid: 324cb8cc-7e57-43d0-9358-2683efc4fb1e
title: 'Membre CBasePin :: m_pName (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pName
api_type:
- HeaderDef
api_location:
- Amfilter.h
ms.openlocfilehash: f2580b9aba379362c39e3d792504434fa18fe076
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533181"
---
# <a name="cbasepinm_pname-member"></a><span data-ttu-id="443bd-103">Membre CBasePin :: m \_ pname</span><span class="sxs-lookup"><span data-stu-id="443bd-103">CBasePin::m\_pName member</span></span>

<span data-ttu-id="443bd-104">Nom du code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="443bd-104">Pin name.</span></span>

## <a name="syntax"></a><span data-ttu-id="443bd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="443bd-105">Syntax</span></span>


```C++
WCHAR *m_pName;
```



## <a name="remarks"></a><span data-ttu-id="443bd-106">Notes</span><span class="sxs-lookup"><span data-stu-id="443bd-106">Remarks</span></span>

<span data-ttu-id="443bd-107">La méthode [**CBasePin :: QueryPinInfo**](cbasepin-querypininfo.md) retourne cette chaîne comme nom de code confidentiel, et la méthode [**CBasePin :: QueryId**](cbasepin-queryid.md) la retourne comme identificateur de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="443bd-107">The [**CBasePin::QueryPinInfo**](cbasepin-querypininfo.md) method returns this string as the pin name, and the [**CBasePin::QueryId**](cbasepin-queryid.md) method returns it as the pin identifier.</span></span> <span data-ttu-id="443bd-108">En général, toutefois, le nom du code confidentiel et l’identificateur du code confidentiel ne doivent pas nécessairement être identiques.</span><span class="sxs-lookup"><span data-stu-id="443bd-108">In general, however, the pin name and the pin identifier are not required to be the same.</span></span> <span data-ttu-id="443bd-109">L’identificateur de code confidentiel est utilisé pour la persistance des graphiques.</span><span class="sxs-lookup"><span data-stu-id="443bd-109">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="443bd-110">Pour plus d’informations, consultez [**IBaseFilter :: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).</span><span class="sxs-lookup"><span data-stu-id="443bd-110">For more information, see [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).</span></span>

## <a name="requirements"></a><span data-ttu-id="443bd-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="443bd-111">Requirements</span></span>



| <span data-ttu-id="443bd-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="443bd-112">Requirement</span></span> | <span data-ttu-id="443bd-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="443bd-113">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="443bd-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="443bd-114">Header</span></span><br/> | <dl> <span data-ttu-id="443bd-115"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="443bd-115"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="443bd-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="443bd-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="443bd-117">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="443bd-117">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




