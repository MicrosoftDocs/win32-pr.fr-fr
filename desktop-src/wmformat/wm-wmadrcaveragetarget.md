---
title: WM/WMADRCAverageTarget
description: L’attribut WM/WMADRCAverageTarget contient le niveau de volume moyen demandé par l’utilisateur. Cette valeur est utilisée par le lecteur Windows Media pour le contrôle de plage dynamique.
ms.assetid: 8173b5ab-27e4-4af9-aea8-6c1310f065f5
keywords:
- Format Windows Media WM/WMADRCAverageTarget
topic_type:
- apiref
api_name:
- WM/WMADRCAverageTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 387eed9112e8e0d79943b99bf326b07f42f425d1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106511056"
---
# <a name="wmwmadrcaveragetarget"></a><span data-ttu-id="9e7ca-105">WM/WMADRCAverageTarget</span><span class="sxs-lookup"><span data-stu-id="9e7ca-105">WM/WMADRCAverageTarget</span></span>

<span data-ttu-id="9e7ca-106">L’attribut **WM/WMADRCAverageTarget** contient le niveau de volume moyen demandé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-106">The **WM/WMADRCAverageTarget** attribute contains the average volume level requested by the user.</span></span> <span data-ttu-id="9e7ca-107">Cette valeur est utilisée par le lecteur Windows Media pour le contrôle de plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-107">This value is used by Windows Media Player for dynamic range control.</span></span>

## <a name="global-constant"></a><span data-ttu-id="9e7ca-108">Constante globale</span><span class="sxs-lookup"><span data-stu-id="9e7ca-108">Global Constant</span></span>

<span data-ttu-id="9e7ca-109">\_wszWMWMADRCAverageTarget g</span><span class="sxs-lookup"><span data-stu-id="9e7ca-109">g\_wszWMWMADRCAverageTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="9e7ca-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="9e7ca-110">Data Type</span></span>

<span data-ttu-id="9e7ca-111">**\_valeur DWORD de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="9e7ca-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="9e7ca-112">Notes</span><span class="sxs-lookup"><span data-stu-id="9e7ca-112">Remarks</span></span>

<span data-ttu-id="9e7ca-113">Il existe quatre attributs utilisés par le lecteur Windows Media pour le contrôle de plage dynamique : **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** et **WM/WMADRCPeakTarget**.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-113">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="9e7ca-114">Toutes ces valeurs sont définies par le writer en fonction des informations du codec lors de l’écriture de flux avec le codec Windows Media Audio 9 ou Windows Media Audio 9 Professional.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-114">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="9e7ca-115">Les valeurs moyennes sont définies sur le niveau de volume moyen du flux, et les valeurs maximales sont définies sur le niveau de volume maximal dans le flux.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-115">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="9e7ca-116">Les valeurs de référence sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-116">The reference values are read-only.</span></span> <span data-ttu-id="9e7ca-117">Les valeurs cibles sont définies par le lecteur Windows Media lorsque le fichier est lu pour enregistrer les préférences de contrôle de plage dynamique de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-117">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e7ca-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e7ca-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e7ca-119">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="9e7ca-119">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="9e7ca-120">**WM/WMADRCAverageReference**</span><span class="sxs-lookup"><span data-stu-id="9e7ca-120">**WM/WMADRCAverageReference**</span></span>](wm-wmadrcaveragereference.md)
</dt> <dt>

[<span data-ttu-id="9e7ca-121">**WM/WMADRCPeakReference**</span><span class="sxs-lookup"><span data-stu-id="9e7ca-121">**WM/WMADRCPeakReference**</span></span>](wm-wmadrcpeakreference.md)
</dt> <dt>

[<span data-ttu-id="9e7ca-122">**WM/WMADRCPeakTarget**</span><span class="sxs-lookup"><span data-stu-id="9e7ca-122">**WM/WMADRCPeakTarget**</span></span>](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




