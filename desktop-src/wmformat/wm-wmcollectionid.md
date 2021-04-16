---
title: WM/WMCollectionID
description: L’attribut WM/WMCollectionID contient un GUID identifiant la collection.
ms.assetid: 088fe2d7-e2d9-42a3-8deb-1d7948ff7df9
keywords:
- Format Windows Media WM/WMCollectionID
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d2ffe9ca827b19b4ce403b2e2929dea64ae684
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380847"
---
# <a name="wmwmcollectionid"></a><span data-ttu-id="8e4eb-104">WM/WMCollectionID</span><span class="sxs-lookup"><span data-stu-id="8e4eb-104">WM/WMCollectionID</span></span>

<span data-ttu-id="8e4eb-105">L’attribut **WM/WMCollectionID** contient un GUID identifiant la collection.</span><span class="sxs-lookup"><span data-stu-id="8e4eb-105">The **WM/WMCollectionID** attribute contains a GUID identifying the collection.</span></span>

## <a name="global-constant"></a><span data-ttu-id="8e4eb-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="8e4eb-106">Global Constant</span></span>

<span data-ttu-id="8e4eb-107">\_wszWMWMCollectionID g</span><span class="sxs-lookup"><span data-stu-id="8e4eb-107">g\_wszWMWMCollectionID</span></span>

## <a name="data-type"></a><span data-ttu-id="8e4eb-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="8e4eb-108">Data Type</span></span>

<span data-ttu-id="8e4eb-109">**\_GUID du type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="8e4eb-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="8e4eb-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8e4eb-110">Remarks</span></span>

<span data-ttu-id="8e4eb-111">Le contenu est identifié par les technologies Windows Media à l’aide de trois valeurs : **WM/WMCollectionGroupID**, **WM/WMCollectionID** et **WM/WMContentID**.</span><span class="sxs-lookup"><span data-stu-id="8e4eb-111">Content is identified by Windows Media technologies by using three values: **WM/WMCollectionGroupID**, **WM/WMCollectionID**, and **WM/WMContentID**.</span></span> <span data-ttu-id="8e4eb-112">Ces valeurs identifient le contenu, la collection à laquelle il appartient et le groupe auquel appartient la collection.</span><span class="sxs-lookup"><span data-stu-id="8e4eb-112">These values identify the content, the collection to which it belongs, and the group to which the collection belongs.</span></span> <span data-ttu-id="8e4eb-113">Ces trois valeurs sont remplies par le lecteur Windows Media lorsque les métadonnées du contenu sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="8e4eb-113">All three of these values are populated by Windows Media Player when metadata for the content is retrieved.</span></span> <span data-ttu-id="8e4eb-114">Vous pouvez demander à votre application d’enregistrer ces valeurs et de les utiliser pour identifier le contenu, mais vous ne devez pas les modifier si elles sont présentes.</span><span class="sxs-lookup"><span data-stu-id="8e4eb-114">You can have your application record these values and use them to identify content, but you should not change them if they are present.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e4eb-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e4eb-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e4eb-116">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="8e4eb-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




