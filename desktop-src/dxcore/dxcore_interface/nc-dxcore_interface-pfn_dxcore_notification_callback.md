---
title: PFN_DXCORE_NOTIFICATION_CALLBACK
description: Fonction de rappel (implémentée par votre application), qui est appelée par un objet DXCore pour les événements de notification.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 01d65f6907c60d6c68b612308b9105d18bbe037f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941243"
---
# <a name="pfn_dxcore_notification_callback-callback"></a><span data-ttu-id="533c5-103">Rappel de PFN_DXCORE_NOTIFICATION_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="533c5-103">PFN_DXCORE_NOTIFICATION_CALLBACK callback</span></span>

<span data-ttu-id="533c5-104">Fonction de rappel (implémentée par votre application), qui est appelée par un objet DXCore pour les événements de notification.</span><span class="sxs-lookup"><span data-stu-id="533c5-104">A callback function (implemented by your application), which is called by a DXCore object for notification events.</span></span>

## <a name="syntax"></a><span data-ttu-id="533c5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="533c5-105">Syntax</span></span>

```cpp
typedef void (STDMETHODCALLTYPE *PFN_DXCORE_NOTIFICATION_CALLBACK)(
  DXCoreNotificationType notificationType,
  _In_ IUnknown *object,
  _In_opt_ void *context);
```

## <a name="parameters"></a><span data-ttu-id="533c5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="533c5-106">Parameters</span></span>

### <a name="notificationtype"></a><span data-ttu-id="533c5-107">notificationType</span><span class="sxs-lookup"><span data-stu-id="533c5-107">notificationType</span></span>

<span data-ttu-id="533c5-108">Type : **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="533c5-108">Type: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span></span>

<span data-ttu-id="533c5-109">Type de notification représentant cet appel.</span><span class="sxs-lookup"><span data-stu-id="533c5-109">The type of notification representing this invocation.</span></span> <span data-ttu-id="533c5-110">Consultez le tableau dans [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) pour plus d’informations sur les types qui sont valides avec les genres d’objets.</span><span class="sxs-lookup"><span data-stu-id="533c5-110">See the table in [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) for info about what types are valid with which kinds of objects.</span></span>

### <a name="object"></a><span data-ttu-id="533c5-111">object</span><span class="sxs-lookup"><span data-stu-id="533c5-111">object</span></span>

<span data-ttu-id="533c5-112">Type : **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="533c5-112">Type: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="533c5-113">Objet [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) ou [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) déclenchant la notification.</span><span class="sxs-lookup"><span data-stu-id="533c5-113">The [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) or [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) object raising the notification.</span></span>

### <a name="context-in"></a><span data-ttu-id="533c5-114">contexte [in]</span><span class="sxs-lookup"><span data-stu-id="533c5-114">context [in]</span></span>

<span data-ttu-id="533c5-115">Type : **void \***</span><span class="sxs-lookup"><span data-stu-id="533c5-115">Type: **void\***</span></span>

<span data-ttu-id="533c5-116">Pointeur, qui peut être `nullptr` , vers un objet contenant des informations de contexte.</span><span class="sxs-lookup"><span data-stu-id="533c5-116">A pointer, which may be `nullptr`, to an object containing context info.</span></span>

## <a name="see-also"></a><span data-ttu-id="533c5-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="533c5-117">See also</span></span>

<span data-ttu-id="533c5-118">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="533c5-118">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>