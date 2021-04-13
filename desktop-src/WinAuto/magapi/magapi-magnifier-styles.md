---
title: Styles de la loupe
description: Cette rubrique décrit les styles utilisés avec le contrôle magnifier.
ms.assetid: B3C575AC-B8D3-40CF-AF09-BAC73E6C7B45
topic_type:
- apiref
api_name:
- MS_CLIPAROUNDCURSOR
- MS_INVERTCOLORS
- MS_SHOWMAGNIFIEDCURSOR
api_location:
- Magnification.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 212e079a59db9a85b6d232d1c11ac9f46eceb314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384692"
---
# <a name="magnifier-styles"></a><span data-ttu-id="43a8b-103">Styles de la loupe</span><span class="sxs-lookup"><span data-stu-id="43a8b-103">Magnifier Styles</span></span>

<span data-ttu-id="43a8b-104">Cette rubrique décrit les styles utilisés avec le contrôle magnifier.</span><span class="sxs-lookup"><span data-stu-id="43a8b-104">This topic describes the styles used with the magnifier control.</span></span> <span data-ttu-id="43a8b-105">Pour créer un contrôle Magnifier, utilisez la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) et spécifiez la classe de fenêtre WC_MAGNIFIER, ainsi qu’une combinaison des styles de loupe suivants.</span><span class="sxs-lookup"><span data-stu-id="43a8b-105">To create a magnifier control, use the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function and specify the WC_MAGNIFIER window class, along with a combination of the following magnifier styles.</span></span>

| <span data-ttu-id="43a8b-106">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43a8b-106">Requirement</span></span> | <span data-ttu-id="43a8b-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="43a8b-107">Value</span></span> |
|:---|:---|
| <span data-ttu-id="43a8b-108">MS_CLIPAROUNDCURSOR 0x0002L</span><span class="sxs-lookup"><span data-stu-id="43a8b-108">MS_CLIPAROUNDCURSOR 0x0002L</span></span> | <span data-ttu-id="43a8b-109">Découpe la zone de la fenêtre de la loupe qui entoure le curseur système.</span><span class="sxs-lookup"><span data-stu-id="43a8b-109">Clips the area of the magnifier window that surrounds the system cursor.</span></span> <span data-ttu-id="43a8b-110">Ce style permet à l’utilisateur de voir le contenu de l’écran qui se trouve derrière la fenêtre Loupe.</span><span class="sxs-lookup"><span data-stu-id="43a8b-110">This style enables the user to see screen content that is behind the magnifier window.</span></span> |
| <span data-ttu-id="43a8b-111">MS_INVERTCOLORS 0x0004L</span><span class="sxs-lookup"><span data-stu-id="43a8b-111">MS_INVERTCOLORS 0x0004L</span></span> | <span data-ttu-id="43a8b-112">Affiche le contenu agrandi de l’écran à l’aide de couleurs inversées.</span><span class="sxs-lookup"><span data-stu-id="43a8b-112">Displays the magnified screen content using inverted colors.</span></span> |
| <span data-ttu-id="43a8b-113">MS_SHOWMAGNIFIEDCURSOR 0x0001L</span><span class="sxs-lookup"><span data-stu-id="43a8b-113">MS_SHOWMAGNIFIEDCURSOR 0x0001L</span></span> | <span data-ttu-id="43a8b-114">Affiche le curseur système agrandi ainsi que le contenu de l’écran agrandi.</span><span class="sxs-lookup"><span data-stu-id="43a8b-114">Displays the magnified system cursor along with the magnified screen content.</span></span> |

## <a name="requirements"></a><span data-ttu-id="43a8b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43a8b-115">Requirements</span></span>

| <span data-ttu-id="43a8b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43a8b-116">Requirement</span></span> | <span data-ttu-id="43a8b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="43a8b-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="43a8b-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43a8b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="43a8b-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43a8b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="43a8b-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43a8b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="43a8b-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43a8b-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="43a8b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="43a8b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="43a8b-123"><dt>Agrandissement. h</dt></span><span class="sxs-lookup"><span data-stu-id="43a8b-123"><dt>Magnification.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="43a8b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43a8b-124">See also</span></span>

[<span data-ttu-id="43a8b-125">Constantes</span><span class="sxs-lookup"><span data-stu-id="43a8b-125">Constants</span></span>](entry-magapi-constants.md)
