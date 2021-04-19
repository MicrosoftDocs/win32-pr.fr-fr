---
title: WM/WMADRCAverageReference
description: L’attribut WM/WMADRCAverageReference contient le niveau de volume moyen du fichier encodé.
ms.assetid: 994614e3-06e2-48f0-bdac-6de5ab0c0eff
keywords:
- Format Windows Media WM/WMADRCAverageReference
topic_type:
- apiref
api_name:
- WM/WMADRCAverageReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7059b68658d070ca71a738a5e20658474139558
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106538586"
---
# <a name="wmwmadrcaveragereference"></a><span data-ttu-id="9370d-104">WM/WMADRCAverageReference</span><span class="sxs-lookup"><span data-stu-id="9370d-104">WM/WMADRCAverageReference</span></span>

<span data-ttu-id="9370d-105">L’attribut **WM/WMADRCAverageReference** contient le niveau de volume moyen du fichier encodé.</span><span class="sxs-lookup"><span data-stu-id="9370d-105">The **WM/WMADRCAverageReference** attribute contains the average volume level of the file as encoded.</span></span>

## <a name="global-constant"></a><span data-ttu-id="9370d-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="9370d-106">Global Constant</span></span>

<span data-ttu-id="9370d-107">\_wszWMWMADRCAverageReference g</span><span class="sxs-lookup"><span data-stu-id="9370d-107">g\_wszWMWMADRCAverageReference</span></span>

## <a name="data-type"></a><span data-ttu-id="9370d-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="9370d-108">Data Type</span></span>

<span data-ttu-id="9370d-109">**\_valeur DWORD de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="9370d-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="9370d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="9370d-110">Remarks</span></span>

<span data-ttu-id="9370d-111">Il existe quatre attributs utilisés par le lecteur Windows Media pour le contrôle de plage dynamique : **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** et **WM/WMADRCPeakTarget**.</span><span class="sxs-lookup"><span data-stu-id="9370d-111">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="9370d-112">Toutes ces valeurs sont définies par le writer en fonction des informations du codec lors de l’écriture de flux avec le codec Windows Media Audio 9 ou Windows Media Audio 9 Professional.</span><span class="sxs-lookup"><span data-stu-id="9370d-112">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="9370d-113">Les valeurs moyennes sont définies sur le niveau de volume moyen du flux, et les valeurs maximales sont définies sur le niveau de volume maximal dans le flux.</span><span class="sxs-lookup"><span data-stu-id="9370d-113">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="9370d-114">Les valeurs de référence sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9370d-114">The reference values are read-only.</span></span> <span data-ttu-id="9370d-115">Les valeurs cibles sont définies par le lecteur Windows Media lorsque le fichier est lu pour enregistrer les préférences de contrôle de plage dynamique de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9370d-115">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="9370d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9370d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9370d-117">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="9370d-117">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="9370d-118">**WM/WMADRCAverageTarget**</span><span class="sxs-lookup"><span data-stu-id="9370d-118">**WM/WMADRCAverageTarget**</span></span>](wm-wmadrcaveragetarget.md)
</dt> <dt>

[<span data-ttu-id="9370d-119">**WM/WMADRCPeakReference**</span><span class="sxs-lookup"><span data-stu-id="9370d-119">**WM/WMADRCPeakReference**</span></span>](wm-wmadrcpeakreference.md)
</dt> <dt>

[<span data-ttu-id="9370d-120">**WM/WMADRCPeakTarget**</span><span class="sxs-lookup"><span data-stu-id="9370d-120">**WM/WMADRCPeakTarget**</span></span>](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




