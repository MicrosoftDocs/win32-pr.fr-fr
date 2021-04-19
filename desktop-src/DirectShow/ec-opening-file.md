---
description: Le graphique ouvre un fichier ou a fini d’ouvrir un fichier.
ms.assetid: 352867e1-025f-4adb-be32-f7941c0ec8cf
title: EC_OPENING_FILE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf275a2f9b64f9a30c8049b5207622270edc5098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530352"
---
# <a name="ec_opening_file"></a><span data-ttu-id="52f09-103">\_fichier d’ouverture EC \_</span><span class="sxs-lookup"><span data-stu-id="52f09-103">EC\_OPENING\_FILE</span></span>

<span data-ttu-id="52f09-104">Le graphique ouvre un fichier ou a fini d’ouvrir un fichier.</span><span class="sxs-lookup"><span data-stu-id="52f09-104">The graph is opening a file, or has finished opening a file.</span></span>

## <a name="parameters"></a><span data-ttu-id="52f09-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52f09-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52f09-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="52f09-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="52f09-107">**True** si le graphique commence à ouvrir un fichier, ou **false** si le graphique n’ouvre plus le fichier.</span><span class="sxs-lookup"><span data-stu-id="52f09-107">**TRUE** if the graph is starting to open a file, or **FALSE** if the graph is no longer opening the file.</span></span>

</dd> <dt>

<span data-ttu-id="52f09-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="52f09-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="52f09-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="52f09-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="52f09-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="52f09-110">Default Action</span></span>

<span data-ttu-id="52f09-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="52f09-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="52f09-112">Notes</span><span class="sxs-lookup"><span data-stu-id="52f09-112">Remarks</span></span>

<span data-ttu-id="52f09-113">Un filtre peut envoyer cet événement s’il consacre beaucoup de temps à ouvrir un fichier.</span><span class="sxs-lookup"><span data-stu-id="52f09-113">A filter can send this event if it spends significant time opening a file.</span></span> <span data-ttu-id="52f09-114">(Par exemple, le fichier peut se trouver sur un réseau.) L’application peut utiliser cet événement pour ajuster son interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="52f09-114">(For example, the file might be located on a network.) The application can use this event to adjust its user interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="52f09-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52f09-115">Requirements</span></span>



| <span data-ttu-id="52f09-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52f09-116">Requirement</span></span> | <span data-ttu-id="52f09-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="52f09-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="52f09-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="52f09-118">Header</span></span><br/> | <dl> <span data-ttu-id="52f09-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="52f09-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52f09-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52f09-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52f09-121">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="52f09-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="52f09-122">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="52f09-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




