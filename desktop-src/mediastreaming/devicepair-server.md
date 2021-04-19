---
title: Propriété de serveur DevicePair (Asptlb. h)
description: Obtient le serveur pour la paire d’appareils active de base.
ms.assetid: 25FD523F-36C7-4165-BBB2-6A3410D896EF
keywords:
- API de diffusion multimédia en continu des propriétés de serveur
- API de diffusion multimédia en continu des propriétés de serveur, interface DevicePair
- API de diffusion multimédia en continu de l’interface DevicePair, propriété de serveur
topic_type:
- apiref
api_name:
- DevicePair.Server
- DevicePair.get_Server
api_location:
- asptlb.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec2c28e8118f6cf11e89c7ab4a5ba04abd8b8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535851"
---
# <a name="devicepairserver-property"></a><span data-ttu-id="4626b-106">DevicePair :: Server, propriété</span><span class="sxs-lookup"><span data-stu-id="4626b-106">DevicePair::Server property</span></span>

<span data-ttu-id="4626b-107">Obtient le serveur pour la paire d’appareils active de base.</span><span class="sxs-lookup"><span data-stu-id="4626b-107">Gets the server for the active basic device pair.</span></span>

<span data-ttu-id="4626b-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4626b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4626b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4626b-109">Syntax</span></span>


```C++
HRESULT get_Server(
  [out] ActiveBasicDevice **value
);
```



## <a name="property-value"></a><span data-ttu-id="4626b-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4626b-110">Property value</span></span>

<span data-ttu-id="4626b-111">Reçoit un objet [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) qui représente le périphérique serveur.</span><span class="sxs-lookup"><span data-stu-id="4626b-111">Receives a [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) object that represents the server device.</span></span>

## <a name="requirements"></a><span data-ttu-id="4626b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4626b-112">Requirements</span></span>



| <span data-ttu-id="4626b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4626b-113">Requirement</span></span> | <span data-ttu-id="4626b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="4626b-114">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4626b-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="4626b-115">Header</span></span><br/> | <dl> <span data-ttu-id="4626b-116"><dt>Asptlb. h</dt></span><span class="sxs-lookup"><span data-stu-id="4626b-116"><dt>Asptlb.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4626b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4626b-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="4626b-118">[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4626b-118">[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))</span></span>
</dt> </dl>

 

