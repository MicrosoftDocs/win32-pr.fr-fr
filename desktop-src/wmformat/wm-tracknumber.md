---
title: WM/TrackNumber
description: L’attribut WM/TrackNumber contient le numéro de suivi du contenu. Cet attribut est de base 1.
ms.assetid: cd338cd9-a5de-4311-8089-1d5d90570f69
keywords:
- Format Windows Media WM/TrackNumber
topic_type:
- apiref
api_name:
- WM/TrackNumber
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55691335faaf835b270013c6499197c0e3f7bee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106512477"
---
# <a name="wmtracknumber"></a><span data-ttu-id="27a43-105">WM/TrackNumber</span><span class="sxs-lookup"><span data-stu-id="27a43-105">WM/TrackNumber</span></span>

<span data-ttu-id="27a43-106">L’attribut **WM/TrackNumber** contient le numéro de suivi du contenu.</span><span class="sxs-lookup"><span data-stu-id="27a43-106">The **WM/TrackNumber** attribute contains the track number of the content.</span></span> <span data-ttu-id="27a43-107">Cet attribut est de base 1.</span><span class="sxs-lookup"><span data-stu-id="27a43-107">This attribute is 1-based.</span></span>

## <a name="global-constant"></a><span data-ttu-id="27a43-108">Constante globale</span><span class="sxs-lookup"><span data-stu-id="27a43-108">Global Constant</span></span>

<span data-ttu-id="27a43-109">\_wszWMTrackNumber g</span><span class="sxs-lookup"><span data-stu-id="27a43-109">g\_wszWMTrackNumber</span></span>

## <a name="data-type"></a><span data-ttu-id="27a43-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="27a43-110">Data Type</span></span>

<span data-ttu-id="27a43-111">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="27a43-111">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="27a43-112">Notes</span><span class="sxs-lookup"><span data-stu-id="27a43-112">Remarks</span></span>

<span data-ttu-id="27a43-113">De nombreuses applications existantes écrivent la valeur de **WM/TrackNumber** comme **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="27a43-113">Many existing applications write the value for **WM/TrackNumber** as a **DWORD**.</span></span> <span data-ttu-id="27a43-114">Si vous créez une application qui lit des fichiers provenant de sources inconnues, vous devez inclure du code pour gérer les valeurs de type chaîne et **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="27a43-114">If you create an application that plays files from unknown sources, you should include code to handle both string and **DWORD** values.</span></span>

## <a name="see-also"></a><span data-ttu-id="27a43-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27a43-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27a43-116">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="27a43-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




