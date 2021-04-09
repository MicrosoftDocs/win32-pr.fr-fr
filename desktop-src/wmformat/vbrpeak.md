---
title: VBRPeak
description: L’attribut VBRPeak contient le taux binaire le plus élevé dans un flux encodé VBR (variable bit rate).
ms.assetid: 7b735145-8235-4efb-986f-952989b739bc
keywords:
- Format Windows Media VBRPeak
topic_type:
- apiref
api_name:
- VBRPeak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8aacb076c3e92cfa676e73e945506cc4942bf4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030328"
---
# <a name="vbrpeak"></a><span data-ttu-id="e7dad-104">VBRPeak</span><span class="sxs-lookup"><span data-stu-id="e7dad-104">VBRPeak</span></span>

<span data-ttu-id="e7dad-105">L’attribut **VBRPeak** contient le taux binaire le plus élevé dans un flux encodé VBR (variable bit rate).</span><span class="sxs-lookup"><span data-stu-id="e7dad-105">The **VBRPeak** attribute contains the highest momentary bit rate in a variable bit rate (VBR) encoded stream.</span></span>

## <a name="global-constant"></a><span data-ttu-id="e7dad-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="e7dad-106">Global Constant</span></span>

<span data-ttu-id="e7dad-107">\_wszVBRPeak g</span><span class="sxs-lookup"><span data-stu-id="e7dad-107">g\_wszVBRPeak</span></span>

## <a name="data-type"></a><span data-ttu-id="e7dad-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="e7dad-108">Data Type</span></span>

<span data-ttu-id="e7dad-109">**\_valeur DWORD de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="e7dad-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="e7dad-110">Notes</span><span class="sxs-lookup"><span data-stu-id="e7dad-110">Remarks</span></span>

<span data-ttu-id="e7dad-111">Lors de l’accès à l’interface **IWMHeaderInfo3** de l’objet Writer, vous pouvez ajouter ou modifier cette valeur.</span><span class="sxs-lookup"><span data-stu-id="e7dad-111">When accessing the **IWMHeaderInfo3** interface of the writer object, you can add or change this value.</span></span> <span data-ttu-id="e7dad-112">Dans d’autres objets (éditeur de métadonnées, lecteur et lecteur synchrone), cette valeur est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e7dad-112">In other objects (metadata editor, reader, and synchronous reader), this value is read-only.</span></span>

<span data-ttu-id="e7dad-113">Le writer écrit automatiquement une valeur **VBRPeak** pour chaque flux VBR.</span><span class="sxs-lookup"><span data-stu-id="e7dad-113">The writer automatically writes a **VBRPeak** value for each VBR stream.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7dad-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7dad-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7dad-115">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="e7dad-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




