---
description: Met à jour l’état initial d’un objet ; par exemple, une texture ou un nuanceur.
MS-HAID: vspixengine.IPixEngine4\_UpdateObject\_UINT\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine4 :: UpdateObject, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 90B1DE4F-7DF5-44C9-9A57-1BFB6825EB58
api_name:
- IPixEngine4.UpdateObject
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6f21bac93bea44cb7226897a89460788c3900b8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481249"
---
# <a name="span-idvspixengineipixengine4_updateobject_uint_dword_byte_arrspanipixengine4updateobject-method"></a><span data-ttu-id="79680-103"><span id="vspixengine.ipixengine4_updateobject_uint_dword_byte_arr"></span>IPixEngine4 :: UpdateObject, méthode</span><span class="sxs-lookup"><span data-stu-id="79680-103"><span id="vspixengine.ipixengine4_updateobject_uint_dword_byte_arr"></span>IPixEngine4::UpdateObject method</span></span>

<span data-ttu-id="79680-104">Met à jour l’état initial d’un objet ; par exemple, une texture ou un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="79680-104">Updates the initial state of an object; for example, a texture or shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="79680-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79680-105">Syntax</span></span>


```C++
HRESULT UpdateObject(
   UINT    objectAddress,
   DWORD   size,
   BYTE [] count1_buffer
);
```

## <a name="parameters"></a><span data-ttu-id="79680-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79680-106">Parameters</span></span>

<span data-ttu-id="79680-107">*objectAddress* </span><span class="sxs-lookup"><span data-stu-id="79680-107">*objectAddress* </span></span>  
<span data-ttu-id="79680-108">ID de l’objet à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="79680-108">The ID of the object to be updated.</span></span>

<span data-ttu-id="79680-109">*corps* </span><span class="sxs-lookup"><span data-stu-id="79680-109">*size* </span></span>  
<span data-ttu-id="79680-110">Taille de la charge utile de mise à jour en octets.</span><span class="sxs-lookup"><span data-stu-id="79680-110">The size of the update payload in bytes.</span></span>

<span data-ttu-id="79680-111">*\_mémoire tampon count1* </span><span class="sxs-lookup"><span data-stu-id="79680-111">*count1\_buffer* </span></span>  
<span data-ttu-id="79680-112">Charge utile de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="79680-112">The update payload.</span></span>

## <a name="return-value"></a><span data-ttu-id="79680-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="79680-113">Return value</span></span>

<span data-ttu-id="79680-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="79680-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="79680-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="79680-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="79680-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79680-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="79680-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="79680-117">Header</span></span></p></td><td><span data-ttu-id="79680-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="79680-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="79680-119"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79680-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="79680-120">**IPixEngine4**</span><span class="sxs-lookup"><span data-stu-id="79680-120">**IPixEngine4**</span></span>](/windows/desktop/direct3dtools/ipixengine4)

 

 
