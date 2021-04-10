---
title: BufferAverage
description: L’attribut BufferAverage contient la taille moyenne de la mémoire tampon nécessaire pour un flux de vitesse de transmission variable (VBR).
ms.assetid: 5fd69534-6655-4c98-bf07-a694585fc9ae
keywords:
- Format Windows Media BufferAverage
topic_type:
- apiref
api_name:
- BufferAverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce5767ed329fde43cc1022af54d937fc99e0e323
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100988"
---
# <a name="bufferaverage"></a><span data-ttu-id="f78c6-104">BufferAverage</span><span class="sxs-lookup"><span data-stu-id="f78c6-104">BufferAverage</span></span>

<span data-ttu-id="f78c6-105">L’attribut **BufferAverage** contient la taille moyenne de la mémoire tampon nécessaire pour un flux de vitesse de transmission variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="f78c6-105">The **BufferAverage** attribute contains the average buffer size needed for a variable bit rate (VBR) stream.</span></span>

## <a name="global-constant"></a><span data-ttu-id="f78c6-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="f78c6-106">Global Constant</span></span>

<span data-ttu-id="f78c6-107">\_wszBufferAverage g</span><span class="sxs-lookup"><span data-stu-id="f78c6-107">g\_wszBufferAverage</span></span>

## <a name="data-type"></a><span data-ttu-id="f78c6-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="f78c6-108">Data Type</span></span>

<span data-ttu-id="f78c6-109">**\_valeur DWORD de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="f78c6-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="f78c6-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f78c6-110">Remarks</span></span>

<span data-ttu-id="f78c6-111">Lors de l’accès à l’interface **IWMHeaderInfo3** de l’objet Writer, vous pouvez ajouter ou modifier cette valeur.</span><span class="sxs-lookup"><span data-stu-id="f78c6-111">When accessing the **IWMHeaderInfo3** interface of the writer object, you can add or change this value.</span></span> <span data-ttu-id="f78c6-112">Dans d’autres objets (éditeur de métadonnées, lecteur et lecteur synchrone), cette valeur est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f78c6-112">In other objects (metadata editor, reader, and synchronous reader), this value is read-only.</span></span>

<span data-ttu-id="f78c6-113">Le writer écrit automatiquement une valeur **BufferAverage** pour chaque flux VBR.</span><span class="sxs-lookup"><span data-stu-id="f78c6-113">The writer automatically writes a **BufferAverage** value for each VBR stream.</span></span>

## <a name="see-also"></a><span data-ttu-id="f78c6-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f78c6-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f78c6-115">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="f78c6-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




