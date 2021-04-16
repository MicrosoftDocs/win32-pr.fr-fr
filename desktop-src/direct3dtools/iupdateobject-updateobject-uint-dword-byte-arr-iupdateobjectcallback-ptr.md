---
description: Demande de mise à jour de l’état initial d’un objet ; par exemple, une texture ou un nuanceur.
MS-HAID: vspixengine.IUpdateObject\_UpdateObject\_UINT\_DWORD\_BYTE\_arr\_IUpdateObjectCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IUpdateObject :: UpdateObject, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 824AB599-7377-4F77-8FC8-41E17ED57A79
api_name:
- IUpdateObject.UpdateObject
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9b04918878de15a2b9a5b004d3dff252ab3ddc9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482000"
---
# <a name="span-idvspixengineiupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptrspaniupdateobjectupdateobject-method"></a><span data-ttu-id="205ea-103"><span id="vspixengine.iupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptr"></span>IUpdateObject :: UpdateObject, méthode</span><span class="sxs-lookup"><span data-stu-id="205ea-103"><span id="vspixengine.iupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptr"></span>IUpdateObject::UpdateObject method</span></span>

<span data-ttu-id="205ea-104">Demande de mise à jour de l’état initial d’un objet ; par exemple, une texture ou un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="205ea-104">A request to update the initial state of an object; for example, a texture or shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="205ea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="205ea-105">Syntax</span></span>


```C++
HRESULT UpdateObject(
   UINT                    objectAddress,
   DWORD                   size,
   BYTE []                 count1_buffer,
   IUpdateObjectCallback * pCallback
);
```

## <a name="parameters"></a><span data-ttu-id="205ea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="205ea-106">Parameters</span></span>

<span data-ttu-id="205ea-107">*objectAddress* </span><span class="sxs-lookup"><span data-stu-id="205ea-107">*objectAddress* </span></span>  
<span data-ttu-id="205ea-108">ID de l’objet à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="205ea-108">The ID of the object to be updated.</span></span>

<span data-ttu-id="205ea-109">*corps* </span><span class="sxs-lookup"><span data-stu-id="205ea-109">*size* </span></span>  
<span data-ttu-id="205ea-110">Taille de la charge utile de mise à jour en octets.</span><span class="sxs-lookup"><span data-stu-id="205ea-110">The size of the update payload in bytes.</span></span>

<span data-ttu-id="205ea-111">*\_mémoire tampon count1* </span><span class="sxs-lookup"><span data-stu-id="205ea-111">*count1\_buffer* </span></span>  
<span data-ttu-id="205ea-112">Charge utile de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="205ea-112">The update payload.</span></span>

<span data-ttu-id="205ea-113">*pCallback* </span><span class="sxs-lookup"><span data-stu-id="205ea-113">*pCallback* </span></span>  
<span data-ttu-id="205ea-114">Adresse d’une fonction utilisée pour notifier l’hôte que l’objet a été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="205ea-114">The address of a function used to notify the host that the object was updated.</span></span>

## <a name="return-value"></a><span data-ttu-id="205ea-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="205ea-115">Return value</span></span>

<span data-ttu-id="205ea-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="205ea-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="205ea-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="205ea-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="205ea-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="205ea-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="205ea-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="205ea-119">Header</span></span></p></td><td><span data-ttu-id="205ea-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="205ea-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="205ea-121"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="205ea-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="205ea-122">**IUpdateObject**</span><span class="sxs-lookup"><span data-stu-id="205ea-122">**IUpdateObject**</span></span>](/windows/desktop/direct3dtools/iupdateobject)

 

 
