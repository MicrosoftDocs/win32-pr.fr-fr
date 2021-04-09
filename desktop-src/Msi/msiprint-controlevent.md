---
description: Cet événement est publié par le contrôle ScrollableText pour permettre à l’utilisateur d’imprimer le contenu de ce contrôle.
ms.assetid: 8cb91b21-f6db-4f49-827d-1ec739ff4f45
title: MsiPrint ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0dd876f1a98e68c6ad61c7c122e1b51fa9c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868645"
---
# <a name="msiprint-controlevent"></a><span data-ttu-id="43450-103">MsiPrint ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="43450-103">MsiPrint ControlEvent</span></span>

<span data-ttu-id="43450-104">Cet événement est publié par le [contrôle ScrollableText](scrollabletext-control.md) pour permettre à l’utilisateur d’imprimer le contenu de ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="43450-104">This event is published by the [ScrollableText Control](scrollabletext-control.md) to enable the user to print the contents of that control.</span></span>

<span data-ttu-id="43450-105">**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="43450-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="43450-106">Ce ControlEvent, est disponible à partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="43450-106">This ControlEvent is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="43450-107">Cet événement doit être souscrit par un [contrôle PUSHBUTTON](pushbutton-control.md) situé dans la même boîte de dialogue que le [contrôle ScrollableText](scrollabletext-control.md).</span><span class="sxs-lookup"><span data-stu-id="43450-107">This event should be subscribed to by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the [ScrollableText Control](scrollabletext-control.md).</span></span> <span data-ttu-id="43450-108">TheMsiPrint ControlEvent, doit être créé dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="43450-108">TheMsiPrint ControlEvent should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="43450-109">Publié par</span><span class="sxs-lookup"><span data-stu-id="43450-109">Published By</span></span>

[<span data-ttu-id="43450-110">ScrollableText</span><span class="sxs-lookup"><span data-stu-id="43450-110">ScrollableText</span></span>](scrollabletext-control.md)

## <a name="argument"></a><span data-ttu-id="43450-111">Argument</span><span class="sxs-lookup"><span data-stu-id="43450-111">Argument</span></span>

<span data-ttu-id="43450-112">Ce ControlEvent, n’utilise pas d’argument.</span><span class="sxs-lookup"><span data-stu-id="43450-112">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="43450-113">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="43450-113">Action on Subscribers</span></span>

<span data-ttu-id="43450-114">Ce ControlEvent, n’effectue pas d’action sur les abonnés.</span><span class="sxs-lookup"><span data-stu-id="43450-114">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="43450-115">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="43450-115">Typical Use</span></span>

<span data-ttu-id="43450-116">Un contrôle [PUSHBUTTON](pushbutton-control.md) dans la même boîte de dialogue que le [contrôle ScrollableText](scrollabletext-control.md) peut être utilisé pour afficher une boîte de dialogue modale permettant à l’utilisateur d’imprimer le contenu du contrôle ScrollableText.</span><span class="sxs-lookup"><span data-stu-id="43450-116">A [PushButton](pushbutton-control.md) control on the same dialog box as the [ScrollableText Control](scrollabletext-control.md) can be used to display a modal dialog box enabling the user to print the contents of the ScrollableText Control.</span></span>

 

 



