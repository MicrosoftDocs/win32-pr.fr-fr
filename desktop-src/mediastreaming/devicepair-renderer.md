---
title: Propriété de convertisseur DevicePair
description: Obtient le convertisseur pour la paire d’appareils de base active.
ms.assetid: DB2ED5D3-CCDF-4704-A29A-F1A13F7B953A
keywords:
- API de diffusion multimédia en continu des propriétés de convertisseur
- Propriété de convertisseur diffusion multimédia en continu API, interface DevicePair
- API de diffusion multimédia en continu de l’interface DevicePair, propriété de convertisseur
topic_type:
- apiref
api_name:
- DevicePair.Renderer
- DevicePair.get_Renderer
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f74b212ed4e8ec29b0234a3769c3beff91c0c777
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381830"
---
# <a name="devicepairrenderer-property"></a><span data-ttu-id="1434d-106">DevicePair :: Renderer, propriété</span><span class="sxs-lookup"><span data-stu-id="1434d-106">DevicePair::Renderer property</span></span>

<span data-ttu-id="1434d-107">Obtient le convertisseur pour la paire d’appareils de base active.</span><span class="sxs-lookup"><span data-stu-id="1434d-107">Gets the renderer for the active basic device pair.</span></span>

<span data-ttu-id="1434d-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1434d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1434d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1434d-109">Syntax</span></span>


```C++
HRESULT get_Renderer(
  [out] ActiveBasicDevice **value
);
```



## <a name="property-value"></a><span data-ttu-id="1434d-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1434d-110">Property value</span></span>

<span data-ttu-id="1434d-111">Reçoit un objet [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) qui représente l’appareil du convertisseur.</span><span class="sxs-lookup"><span data-stu-id="1434d-111">Receives a [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) object that represents the renderer device.</span></span>

## <a name="see-also"></a><span data-ttu-id="1434d-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1434d-112">See also</span></span>

<dl> <dt>

<span data-ttu-id="1434d-113">[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1434d-113">[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))</span></span>
</dt> </dl>

 

 