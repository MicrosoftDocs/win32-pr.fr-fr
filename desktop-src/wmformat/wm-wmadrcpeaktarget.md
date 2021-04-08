---
title: WM/WMADRCPeakTarget
description: L’attribut WM/WMADRCPeakTarget contient le niveau de volume maximal demandé par l’utilisateur. Cette valeur est utilisée par le lecteur Windows Media pour le contrôle de plage dynamique.
ms.assetid: 94ef5db1-34f4-4cf8-ac56-c85cca10536b
keywords:
- Format Windows Media WM/WMADRCPeakTarget
topic_type:
- apiref
api_name:
- WM/WMADRCPeakTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55eac4ea68cd61e2cfa0b5c185dc1a4ad17e5ce8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678606"
---
# <a name="wmwmadrcpeaktarget"></a><span data-ttu-id="6a119-105">WM/WMADRCPeakTarget</span><span class="sxs-lookup"><span data-stu-id="6a119-105">WM/WMADRCPeakTarget</span></span>

<span data-ttu-id="6a119-106">L’attribut **WM/WMADRCPeakTarget** contient le niveau de volume maximal demandé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a119-106">The **WM/WMADRCPeakTarget** attribute contains the maximum volume level requested by the user.</span></span> <span data-ttu-id="6a119-107">Cette valeur est utilisée par le lecteur Windows Media pour le contrôle de plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="6a119-107">This value is used by Windows Media Player for dynamic range control.</span></span>

## <a name="global-constant"></a><span data-ttu-id="6a119-108">Constante globale</span><span class="sxs-lookup"><span data-stu-id="6a119-108">Global Constant</span></span>

<span data-ttu-id="6a119-109">\_wszWMWMADRCPeakTarget g</span><span class="sxs-lookup"><span data-stu-id="6a119-109">g\_wszWMWMADRCPeakTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="6a119-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="6a119-110">Data Type</span></span>

<span data-ttu-id="6a119-111">**\_valeur DWORD de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="6a119-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="6a119-112">Notes</span><span class="sxs-lookup"><span data-stu-id="6a119-112">Remarks</span></span>

<span data-ttu-id="6a119-113">Il existe quatre attributs utilisés par le lecteur Windows Media pour le contrôle de plage dynamique : **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** et **WM/WMADRCPeakTarget**.</span><span class="sxs-lookup"><span data-stu-id="6a119-113">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="6a119-114">Toutes ces valeurs sont définies par le writer en fonction des informations du codec lors de l’écriture de flux avec le codec Windows Media Audio 9 ou Windows Media Audio 9 Professional.</span><span class="sxs-lookup"><span data-stu-id="6a119-114">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="6a119-115">Les valeurs moyennes sont définies sur le niveau de volume moyen du flux, et les valeurs maximales sont définies sur le niveau de volume maximal dans le flux.</span><span class="sxs-lookup"><span data-stu-id="6a119-115">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="6a119-116">Les valeurs de référence sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6a119-116">The reference values are read-only.</span></span> <span data-ttu-id="6a119-117">Les valeurs cibles sont définies par le lecteur Windows Media lorsque le fichier est lu pour enregistrer les préférences de contrôle de plage dynamique de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a119-117">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a119-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a119-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a119-119">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="6a119-119">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="6a119-120">**WM/WMADRCAverageReference**</span><span class="sxs-lookup"><span data-stu-id="6a119-120">**WM/WMADRCAverageReference**</span></span>](wm-wmadrcaveragereference.md)
</dt> <dt>

[<span data-ttu-id="6a119-121">**WM/WMADRCAverageTarget**</span><span class="sxs-lookup"><span data-stu-id="6a119-121">**WM/WMADRCAverageTarget**</span></span>](wm-wmadrcaveragetarget.md)
</dt> <dt>

[<span data-ttu-id="6a119-122">**WM/WMADRCPeakReference**</span><span class="sxs-lookup"><span data-stu-id="6a119-122">**WM/WMADRCPeakReference**</span></span>](wm-wmadrcpeakreference.md)
</dt> </dl>

 

 




