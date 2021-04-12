---
description: Enregistre une texture.
MS-HAID: vspixengine.IPixEngine5\_SaveTextureAsync\_UINT\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5 :: SaveTextureAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6F08F49E-6FFD-4A9B-86F5-8CB499947F57
api_name:
- IPixEngine5.SaveTextureAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2590f793d0ba05af1ccf9e10ba04fa8b6aa2421b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482633"
---
# <a name="span-idvspixengineipixengine5_savetextureasync_uint_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5savetextureasync-method"></a><span data-ttu-id="3a03a-103"><span id="vspixengine.ipixengine5_savetextureasync_uint_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5 :: SaveTextureAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="3a03a-103"><span id="vspixengine.ipixengine5_savetextureasync_uint_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::SaveTextureAsync method</span></span>

<span data-ttu-id="3a03a-104">Enregistre une texture.</span><span class="sxs-lookup"><span data-stu-id="3a03a-104">Saves a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a03a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a03a-105">Syntax</span></span>


```C++
HRESULT SaveTextureAsync(
   UINT                  textureId,
   BSTR                  fileName,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="3a03a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a03a-106">Parameters</span></span>

<span data-ttu-id="3a03a-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="3a03a-107">*textureId* </span></span>  
<span data-ttu-id="3a03a-108">ID de la texture à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="3a03a-108">The ID of the texture to save.</span></span>

<span data-ttu-id="3a03a-109">*Extension* </span><span class="sxs-lookup"><span data-stu-id="3a03a-109">*fileName* </span></span>  
<span data-ttu-id="3a03a-110">Chaîne COM contenant le nom du chemin d’accès de la texture enregistrée.</span><span class="sxs-lookup"><span data-stu-id="3a03a-110">A COM string containing the pathname of the saved texture.</span></span>

<span data-ttu-id="3a03a-111">*rappels* </span><span class="sxs-lookup"><span data-stu-id="3a03a-111">*callbacks* </span></span>  
<span data-ttu-id="3a03a-112">Adresse d’un objet qui fournit l’interface de rappels IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="3a03a-112">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="3a03a-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="3a03a-113">*requestCookie* </span></span>  
<span data-ttu-id="3a03a-114">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="3a03a-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="3a03a-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="3a03a-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="3a03a-116">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="3a03a-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="3a03a-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a03a-117">Return value</span></span>

<span data-ttu-id="3a03a-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3a03a-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3a03a-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3a03a-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a03a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a03a-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3a03a-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a03a-121">Header</span></span></p></td><td><span data-ttu-id="3a03a-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="3a03a-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3a03a-123"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a03a-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3a03a-124">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="3a03a-124">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
