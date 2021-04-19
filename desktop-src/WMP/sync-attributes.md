---
title: Attributs de synchronisation
description: Les attributs Sync01 via Sync16 sont des représentations sous forme de chaîne de valeurs 32 bits que le lecteur Windows Media utilise lorsqu’il synchronise des sélections avec un maximum de 16 périphériques portables.
ms.assetid: b9ae3420-aa09-4969-8637-f16d438942f3
keywords:
- Attributs de synchronisation lecteur Windows Media
topic_type:
- apiref
api_name:
- Sync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5af26ae563a38efcc40b0bcd319c5fc62b4776dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528031"
---
# <a name="sync-attributes"></a><span data-ttu-id="a4686-104">Attributs de synchronisation</span><span class="sxs-lookup"><span data-stu-id="a4686-104">Sync Attributes</span></span>

<span data-ttu-id="a4686-105">Les attributs **Sync01** via **Sync16** sont des représentations sous forme de chaîne de valeurs 32 bits que le lecteur Windows Media utilise lorsqu’il synchronise des sélections avec un maximum de 16 périphériques portables.</span><span class="sxs-lookup"><span data-stu-id="a4686-105">The **Sync01** through **Sync16** attributes are string representations of 32-bit values that Windows Media Player uses when it synchronizes playlists with one of up to 16 portable devices.</span></span>

## <a name="applies-to"></a><span data-ttu-id="a4686-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="a4686-106">Applies To</span></span>

-   [<span data-ttu-id="a4686-107">Sélections</span><span class="sxs-lookup"><span data-stu-id="a4686-107">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="remarks"></a><span data-ttu-id="a4686-108">Notes</span><span class="sxs-lookup"><span data-stu-id="a4686-108">Remarks</span></span>

<span data-ttu-id="a4686-109">Il s’agit d’attributs en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a4686-109">These are read/write attributes.</span></span> <span data-ttu-id="a4686-110">La valeur zéro indique que le lecteur Windows Media ne doit pas synchroniser la playlist avec l’appareil associé.</span><span class="sxs-lookup"><span data-stu-id="a4686-110">A value of zero indicates that Windows Media Player should not synchronize the playlist with the associated device.</span></span> <span data-ttu-id="a4686-111">Une valeur supérieure à zéro indique une priorité de synchronisation pour la sélection donnée.</span><span class="sxs-lookup"><span data-stu-id="a4686-111">A value greater than zero indicates a synchronization priority for the given playlist.</span></span>

<span data-ttu-id="a4686-112">En fonction de l’entrée de l’utilisateur, le lecteur Windows Media définit cet attribut pour chacune des sélections dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="a4686-112">Based on user input, Windows Media Player sets this attribute for each of the playlists in the library.</span></span> <span data-ttu-id="a4686-113">Lorsque le lecteur Windows Media tente de synchroniser une sélection avec un appareil mobile, il examine chaque playlist pour comparer les valeurs des attributs **Sync**_XX_ qui représentent le partenariat de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a4686-113">When Windows Media Player attempts to synchronize a playlist with a portable device, it examines each playlist to compare the values for the **Sync**_XX_ attributes that represent the device partnership.</span></span> <span data-ttu-id="a4686-114">Les sélections qui ont des valeurs de **synchronisation**_XX_ inférieures reçoivent une priorité de synchronisation supérieure.</span><span class="sxs-lookup"><span data-stu-id="a4686-114">Playlists that have lower **Sync**_XX_ values receive higher synchronization priority.</span></span>

<span data-ttu-id="a4686-115">Par exemple, la bibliothèque peut contenir les quatre sélections suivantes et les valeurs de **synchronisation**_XX_ respectives :</span><span class="sxs-lookup"><span data-stu-id="a4686-115">For example, the library might contain the following four playlists and respective **Sync**_XX_ values:</span></span>



| <span data-ttu-id="a4686-116">Nom de la sélection</span><span class="sxs-lookup"><span data-stu-id="a4686-116">Playlist Name</span></span> | <span data-ttu-id="a4686-117">Valeur Sync01</span><span class="sxs-lookup"><span data-stu-id="a4686-117">Sync01 Value</span></span> |
|---------------|--------------|
| <span data-ttu-id="a4686-118">GymMusic. WPL</span><span class="sxs-lookup"><span data-stu-id="a4686-118">GymMusic.WPL</span></span>  | <span data-ttu-id="a4686-119">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="a4686-119">0x0000000D</span></span>   |
| <span data-ttu-id="a4686-120">Assouplissez. WPL</span><span class="sxs-lookup"><span data-stu-id="a4686-120">Relax.WPL</span></span>     | <span data-ttu-id="a4686-121">0x00000020</span><span class="sxs-lookup"><span data-stu-id="a4686-121">0x00000020</span></span>   |
| <span data-ttu-id="a4686-122">DriveHome. WPL</span><span class="sxs-lookup"><span data-stu-id="a4686-122">DriveHome.WPL</span></span> | <span data-ttu-id="a4686-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a4686-123">0x00000001</span></span>   |
| <span data-ttu-id="a4686-124">NoGo. WPL</span><span class="sxs-lookup"><span data-stu-id="a4686-124">NoGo.WPL</span></span>      | <span data-ttu-id="a4686-125">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4686-125">0x00000000</span></span>   |



 

<span data-ttu-id="a4686-126">Lorsque le lecteur Windows Media synchronise l’appareil associé à l’attribut, il synchronise les sélections dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="a4686-126">When Windows Media Player synchronizes the device associated with the attribute, it will synchronize the playlists in the following order:</span></span>

1.  <span data-ttu-id="a4686-127">DriveHome. WPL</span><span class="sxs-lookup"><span data-stu-id="a4686-127">DriveHome.WPL</span></span>
2.  <span data-ttu-id="a4686-128">GymMusic. WPL</span><span class="sxs-lookup"><span data-stu-id="a4686-128">GymMusic.WPL</span></span>
3.  <span data-ttu-id="a4686-129">Assouplissez. WPL</span><span class="sxs-lookup"><span data-stu-id="a4686-129">Relax.WPL</span></span>

<span data-ttu-id="a4686-130">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="a4686-130">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4686-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4686-131">Requirements</span></span>



| <span data-ttu-id="a4686-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4686-132">Requirement</span></span> | <span data-ttu-id="a4686-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4686-133">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="a4686-134">Version</span><span class="sxs-lookup"><span data-stu-id="a4686-134">Version</span></span><br/> | <span data-ttu-id="a4686-135">Lecteur Windows Media 10 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a4686-135">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a4686-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4686-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4686-137">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="a4686-137">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="a4686-138">**Énumération des sélections de synchronisation**</span><span class="sxs-lookup"><span data-stu-id="a4686-138">**Enumerating Synchronization Playlists**</span></span>](enumerating-synchronization-playlists.md)
</dt> </dl>

 

 





