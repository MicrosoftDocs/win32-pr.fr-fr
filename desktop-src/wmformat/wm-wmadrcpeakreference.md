---
title: WM/WMADRCPeakReference
description: L’attribut WM/WMADRCPeakReference contient le niveau de volume maximal du fichier encodé. Cette valeur est utilisée par le lecteur Windows Media pour le contrôle de plage dynamique. Cette valeur est définie par le codec et est en lecture seule.
ms.assetid: c732ee88-437b-4970-8f17-61aed2d91022
keywords:
- Format Windows Media WM/WMADRCPeakReference
topic_type:
- apiref
api_name:
- WM/WMADRCPeakReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59660f950c748c45a1affccee10ae86e38998f23
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380848"
---
# <a name="wmwmadrcpeakreference"></a><span data-ttu-id="d4017-106">WM/WMADRCPeakReference</span><span class="sxs-lookup"><span data-stu-id="d4017-106">WM/WMADRCPeakReference</span></span>

<span data-ttu-id="d4017-107">L’attribut **WM/WMADRCPeakReference** contient le niveau de volume maximal du fichier encodé.</span><span class="sxs-lookup"><span data-stu-id="d4017-107">The **WM/WMADRCPeakReference** attribute contains the maximum volume level of the file as encoded.</span></span> <span data-ttu-id="d4017-108">Cette valeur est utilisée par le lecteur Windows Media pour le contrôle de plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="d4017-108">This value is used by Windows Media Player for dynamic range control.</span></span> <span data-ttu-id="d4017-109">Cette valeur est définie par le codec et est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d4017-109">This value is set by the codec and is read-only.</span></span>

## <a name="global-constant"></a><span data-ttu-id="d4017-110">Constante globale</span><span class="sxs-lookup"><span data-stu-id="d4017-110">Global Constant</span></span>

<span data-ttu-id="d4017-111">\_wszWMWMADRCPeakReference g</span><span class="sxs-lookup"><span data-stu-id="d4017-111">g\_wszWMWMADRCPeakReference</span></span>

## <a name="data-type"></a><span data-ttu-id="d4017-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="d4017-112">Data Type</span></span>

<span data-ttu-id="d4017-113">**\_valeur DWORD de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d4017-113">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="d4017-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d4017-114">Remarks</span></span>

<span data-ttu-id="d4017-115">Il existe quatre attributs utilisés par le lecteur Windows Media pour le contrôle de plage dynamique : **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** et **WM/WMADRCPeakTarget**.</span><span class="sxs-lookup"><span data-stu-id="d4017-115">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="d4017-116">Toutes ces valeurs sont définies par le writer en fonction des informations du codec lors de l’écriture de flux avec le codec Windows Media Audio 9 ou Windows Media Audio 9 Professional.</span><span class="sxs-lookup"><span data-stu-id="d4017-116">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="d4017-117">Les valeurs moyennes sont définies sur le niveau de volume moyen du flux, et les valeurs maximales sont définies sur le niveau de volume maximal dans le flux.</span><span class="sxs-lookup"><span data-stu-id="d4017-117">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="d4017-118">Les valeurs de référence sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d4017-118">The reference values are read-only.</span></span> <span data-ttu-id="d4017-119">Les valeurs cibles sont définies par le lecteur Windows Media lorsque le fichier est lu pour enregistrer les préférences de contrôle de plage dynamique de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d4017-119">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4017-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4017-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4017-121">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="d4017-121">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="d4017-122">**WM/WMADRCAverageReference**</span><span class="sxs-lookup"><span data-stu-id="d4017-122">**WM/WMADRCAverageReference**</span></span>](wm-wmadrcaveragereference.md)
</dt> <dt>

[<span data-ttu-id="d4017-123">**WM/WMADRCAverageTarget**</span><span class="sxs-lookup"><span data-stu-id="d4017-123">**WM/WMADRCAverageTarget**</span></span>](wm-wmadrcaveragetarget.md)
</dt> <dt>

[<span data-ttu-id="d4017-124">**WM/WMADRCPeakTarget**</span><span class="sxs-lookup"><span data-stu-id="d4017-124">**WM/WMADRCPeakTarget**</span></span>](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




