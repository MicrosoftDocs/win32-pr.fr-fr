---
title: IDXCoreAdapterFactory::IsNotificationTypeSupported
description: Détermine si un type de notification spécifié est pris en charge par le système d’exploitation.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 78730167e7ec139733ee1e4011d2e5e59c32782b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315966"
---
# <a name="idxcoreadapterfactoryisnotificationtypesupported-method"></a><span data-ttu-id="55991-103">IDXCoreAdapterFactory :: IsNotificationTypeSupported, méthode</span><span class="sxs-lookup"><span data-stu-id="55991-103">IDXCoreAdapterFactory::IsNotificationTypeSupported method</span></span>

<span data-ttu-id="55991-104">Détermine si un type de notification spécifié est pris en charge par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="55991-104">Determines whether a specified notification type is supported by the operating system (OS).</span></span> <span data-ttu-id="55991-105">Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="55991-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="55991-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55991-106">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsNotificationTypeSupported(
  DXCoreNotificationType notificationType) = 0;
```

## <a name="parameters"></a><span data-ttu-id="55991-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55991-107">Parameters</span></span>

### <a name="notificationtype"></a><span data-ttu-id="55991-108">notificationType</span><span class="sxs-lookup"><span data-stu-id="55991-108">notificationType</span></span>

<span data-ttu-id="55991-109">Type : **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="55991-109">Type: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span></span>

<span data-ttu-id="55991-110">Le type de notification que vous interrogez sur la prise en charge de.</span><span class="sxs-lookup"><span data-stu-id="55991-110">The type of notification that you're querying about support for.</span></span> <span data-ttu-id="55991-111">Pour plus d’informations sur les types de notification, consultez le tableau dans [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) .</span><span class="sxs-lookup"><span data-stu-id="55991-111">See the table in [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) for info about the notification types.</span></span>

## <a name="returns"></a><span data-ttu-id="55991-112">Retours</span><span class="sxs-lookup"><span data-stu-id="55991-112">Returns</span></span>

<span data-ttu-id="55991-113">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="55991-113">Type: **bool**</span></span>

<span data-ttu-id="55991-114">Retourne  `true`   si le type de notification est pris en charge par le système.</span><span class="sxs-lookup"><span data-stu-id="55991-114">Returns `true` if the notification type is supported by the system.</span></span> <span data-ttu-id="55991-115">Sinon, retourne  `false` .</span><span class="sxs-lookup"><span data-stu-id="55991-115">Otherwise, returns `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="55991-116">Notes</span><span class="sxs-lookup"><span data-stu-id="55991-116">Remarks</span></span>

<span data-ttu-id="55991-117">Vous pouvez appeler **IsNotificationTypeSupported** pour déterminer si un type de notification donné est connu pour cette version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="55991-117">You can call **IsNotificationTypeSupported** to determine whether a given notification type is known to this version of the OS.</span></span> <span data-ttu-id="55991-118">Par exemple, un type de notification introduit dans une version particulière de Windows est inconnu des versions précédentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="55991-118">For example, a notification type that's introduced in a particular version of Windows is unknown to previous versions of Windows.</span></span>

## <a name="see-also"></a><span data-ttu-id="55991-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55991-119">See also</span></span>

<span data-ttu-id="55991-120">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [référence dxcore](../dxcore-reference.md), [GUID d’attribut d’adaptateur dxcore](../dxcore-adapter-attribute-guids.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="55991-120">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>