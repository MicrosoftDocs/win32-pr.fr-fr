---
title: IDXCoreAdapter
description: L’interface **IDXCoreAdapter**   implémente des méthodes pour récupérer des détails sur un élément de l’adaptateur.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0930ce76353d556f7839f476ec8979823eac3a6c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102193"
---
# <a name="idxcoreadapter-interface"></a><span data-ttu-id="b2dbb-103">Interface IDXCoreAdapter</span><span class="sxs-lookup"><span data-stu-id="b2dbb-103">IDXCoreAdapter interface</span></span>

<span data-ttu-id="b2dbb-104">L’interface **IDXCoreAdapter**   implémente des méthodes pour récupérer des détails sur un élément de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="b2dbb-104">The **IDXCoreAdapter** interface implements methods for retrieving details about an adapter item.</span></span> <span data-ttu-id="b2dbb-105">**IDXCoreAdapter** hérite de l’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b2dbb-105">**IDXCoreAdapter** inherits from the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b2dbb-106">Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="b2dbb-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b2dbb-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b2dbb-107">Remarks</span></span>

<span data-ttu-id="b2dbb-108">Les propriétés d’un adaptateur sont établies au moment du démarrage de l’adaptateur et sont immuables pendant toute la durée de vie de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="b2dbb-108">An adapter's properties are established at the time the adapter starts, and they're immutable for the lifetime of the adapter.</span></span> <span data-ttu-id="b2dbb-109">Cela diffère de l’état d’une carte, qui peut être interrogé ou défini, et dont les valeurs peuvent changer au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="b2dbb-109">This is in contrast to an adapter's state, which can be queried or set, and the values of which can change over time.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2dbb-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2dbb-110">See also</span></span>

<span data-ttu-id="b2dbb-111">[Référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="b2dbb-111">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>