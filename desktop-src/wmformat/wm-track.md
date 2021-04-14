---
title: WM/Track
description: L’attribut WM/Track contient le numéro de piste du contenu. Cet attribut est de base zéro et est pris en charge pour la compatibilité descendante. Le nouveau contenu doit utiliser l’attribut WM/TrackNumber à la place.
ms.assetid: c763d7b0-9d12-4a4e-8c9f-9cf67bd2a02b
keywords:
- WM/Track Windows Media format
topic_type:
- apiref
api_name:
- WM/Track
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 244426175ea74bc0281f8822964c2fc0bfa37aa7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380533"
---
# <a name="wmtrack"></a><span data-ttu-id="0925c-106">WM/Track</span><span class="sxs-lookup"><span data-stu-id="0925c-106">WM/Track</span></span>

<span data-ttu-id="0925c-107">L’attribut **WM/Track** contient le numéro de piste du contenu.</span><span class="sxs-lookup"><span data-stu-id="0925c-107">The **WM/Track** attribute contains the track number of the content.</span></span> <span data-ttu-id="0925c-108">Cet attribut est de base zéro et est pris en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="0925c-108">This attribute is zero-based and is supported for backward compatibility.</span></span> <span data-ttu-id="0925c-109">Le nouveau contenu doit utiliser l’attribut [**WM/TrackNumber**](wm-tracknumber.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="0925c-109">New content should use the [**WM/TrackNumber**](wm-tracknumber.md) attribute instead.</span></span>

## <a name="global-constant"></a><span data-ttu-id="0925c-110">Constante globale</span><span class="sxs-lookup"><span data-stu-id="0925c-110">Global Constant</span></span>

<span data-ttu-id="0925c-111">\_wszWMTrack g</span><span class="sxs-lookup"><span data-stu-id="0925c-111">g\_wszWMTrack</span></span>

## <a name="data-type"></a><span data-ttu-id="0925c-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="0925c-112">Data Type</span></span>

<span data-ttu-id="0925c-113">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="0925c-113">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="0925c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0925c-114">Remarks</span></span>

<span data-ttu-id="0925c-115">De nombreuses applications existantes écrivent la valeur de **WM/Track** en tant que **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="0925c-115">Many existing applications write the value for **WM/Track** as a **DWORD**.</span></span> <span data-ttu-id="0925c-116">Si vous créez une application qui lit des fichiers provenant de sources inconnues, vous devez inclure du code pour gérer les valeurs de type chaîne et **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="0925c-116">If you create an application that plays files from unknown sources, you should include code to handle both string and **DWORD** values.</span></span>

## <a name="see-also"></a><span data-ttu-id="0925c-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0925c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0925c-118">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="0925c-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




