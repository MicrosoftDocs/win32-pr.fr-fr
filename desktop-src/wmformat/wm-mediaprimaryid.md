---
title: WM/MediaClassPrimaryID
description: L’attribut WM/MediaClassPrimaryID contient le GUID de la classe de média principale.
ms.assetid: 1d01e273-e6ec-49f1-90af-5c2ae171b199
keywords:
- Format Windows Media WM/MediaClassPrimaryID
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f84d987d57b1d825fac54e6a7de41b0154952e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841462"
---
# <a name="wmmediaclassprimaryid"></a><span data-ttu-id="e9d15-104">WM/MediaClassPrimaryID</span><span class="sxs-lookup"><span data-stu-id="e9d15-104">WM/MediaClassPrimaryID</span></span>

<span data-ttu-id="e9d15-105">L’attribut **WM/MediaClassPrimaryID** contient le GUID de la classe de média principale.</span><span class="sxs-lookup"><span data-stu-id="e9d15-105">The **WM/MediaClassPrimaryID** attribute contains the GUID of the primary media class.</span></span>

## <a name="global-constant"></a><span data-ttu-id="e9d15-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="e9d15-106">Global Constant</span></span>

<span data-ttu-id="e9d15-107">\_wszWMMediaClassPrimaryID g</span><span class="sxs-lookup"><span data-stu-id="e9d15-107">g\_wszWMMediaClassPrimaryID</span></span>

## <a name="data-type"></a><span data-ttu-id="e9d15-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="e9d15-108">Data Type</span></span>

<span data-ttu-id="e9d15-109">**\_GUID du type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="e9d15-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="e9d15-110">Notes</span><span class="sxs-lookup"><span data-stu-id="e9d15-110">Remarks</span></span>

<span data-ttu-id="e9d15-111">Cet attribut doit être défini sur l’une des valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e9d15-111">This attribute should be set to one of the values in the following table.</span></span>



| <span data-ttu-id="e9d15-112">GUID de la classe principale</span><span class="sxs-lookup"><span data-stu-id="e9d15-112">Primary class GUID</span></span>                     | <span data-ttu-id="e9d15-113">Description</span><span class="sxs-lookup"><span data-stu-id="e9d15-113">Description</span></span>                                                  |
|----------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="e9d15-114">"D1607DBC-E323-4BE2-86A1-48A42A28441E"</span><span class="sxs-lookup"><span data-stu-id="e9d15-114">"D1607DBC-E323-4BE2-86A1-48A42A28441E"</span></span> | <span data-ttu-id="e9d15-115">Utilisez pour les fichiers musicaux.</span><span class="sxs-lookup"><span data-stu-id="e9d15-115">Use for music files.</span></span> <span data-ttu-id="e9d15-116">N’utilisez pas pour le son qui n’est pas musical.</span><span class="sxs-lookup"><span data-stu-id="e9d15-116">Do not use for audio that is not music.</span></span> |
| <span data-ttu-id="e9d15-117">"DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B"</span><span class="sxs-lookup"><span data-stu-id="e9d15-117">"DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B"</span></span> | <span data-ttu-id="e9d15-118">Utilisez pour les fichiers vidéo.</span><span class="sxs-lookup"><span data-stu-id="e9d15-118">Use for video files.</span></span>                                         |
| <span data-ttu-id="e9d15-119">"01CD0F29-DA4E-4157-897B-6275D50C4F11"</span><span class="sxs-lookup"><span data-stu-id="e9d15-119">"01CD0F29-DA4E-4157-897B-6275D50C4F11"</span></span> | <span data-ttu-id="e9d15-120">Utilisez pour les fichiers audio qui ne sont pas musicaux.</span><span class="sxs-lookup"><span data-stu-id="e9d15-120">Use for audio files that are not music.</span></span>                      |
| <span data-ttu-id="e9d15-121">"FCF24A76-9A57-4036-990D-E35DD8B244E1"</span><span class="sxs-lookup"><span data-stu-id="e9d15-121">"FCF24A76-9A57-4036-990D-E35DD8B244E1"</span></span> | <span data-ttu-id="e9d15-122">Utilisez pour les fichiers qui ne sont ni du son ni de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="e9d15-122">Use for files that are neither audio or video.</span></span>               |



 

<span data-ttu-id="e9d15-123">Lorsque vous spécifiez un identificateur de classe primaire, vous devez également définir un identificateur de classe secondaire pour clarifier le type de contenu dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="e9d15-123">When you specify a primary class identifier, you should also set a secondary class identifier to clarify the type of content in the file.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9d15-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9d15-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9d15-125">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="e9d15-125">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="e9d15-126">**WM/MediaClassSecondaryID**</span><span class="sxs-lookup"><span data-stu-id="e9d15-126">**WM/MediaClassSecondaryID**</span></span>](wm-mediasecondaryid.md)
</dt> </dl>

 

 




