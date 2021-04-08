---
description: Rappel qui avertit l’hôte des informations de mémoire tampon génériques retournées par la requête dans.
MS-HAID: vspixengine.IGenericBufferDataCallback\_ResultCallback\_DWORD\_BYTE\_arr\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IGenericBufferDataCallback :: ResultCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5627A93E-8BE8-4413-BFB4-724AF2DDFEB6
api_name:
- IGenericBufferDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: be2d6aa7cd5e844cd5d1297c16de2ebb21c939a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747149"
---
# <a name="span-idvspixengineigenericbufferdatacallback_resultcallback_dword_byte_arr_bstrspanigenericbufferdatacallbackresultcallback-method"></a><span data-ttu-id="ecca0-103"><span id="vspixengine.igenericbufferdatacallback_resultcallback_dword_byte_arr_bstr"></span>IGenericBufferDataCallback :: ResultCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="ecca0-103"><span id="vspixengine.igenericbufferdatacallback_resultcallback_dword_byte_arr_bstr"></span>IGenericBufferDataCallback::ResultCallback method</span></span>

<span data-ttu-id="ecca0-104">Rappel qui avertit l’hôte des informations de mémoire tampon génériques retournées par la requête dans.</span><span class="sxs-lookup"><span data-stu-id="ecca0-104">A callback that notifies the host of generic buffer information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecca0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ecca0-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD   size,
   BYTE [] count0_buffer,
   BSTR    type
);
```

## <a name="parameters"></a><span data-ttu-id="ecca0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ecca0-106">Parameters</span></span>

<span data-ttu-id="ecca0-107">*corps* </span><span class="sxs-lookup"><span data-stu-id="ecca0-107">*size* </span></span>  
<span data-ttu-id="ecca0-108">Taille du contenu de la mémoire tampon en octets.</span><span class="sxs-lookup"><span data-stu-id="ecca0-108">The size of the buffer contents in bytes.</span></span>

<span data-ttu-id="ecca0-109">*\_mémoire tampon count0* </span><span class="sxs-lookup"><span data-stu-id="ecca0-109">*count0\_buffer* </span></span>  
<span data-ttu-id="ecca0-110">Contenu de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ecca0-110">The buffer contents.</span></span> <span data-ttu-id="ecca0-111">Dans la plupart des cas, il s’agit de données XML.</span><span class="sxs-lookup"><span data-stu-id="ecca0-111">In most cases this is XML data.</span></span>

<span data-ttu-id="ecca0-112">*entrer* </span><span class="sxs-lookup"><span data-stu-id="ecca0-112">*type* </span></span>  
<span data-ttu-id="ecca0-113">Chaîne COM qui indique le type de contenu retourné dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ecca0-113">A COM string that indicates the type of content returned in the buffer.</span></span>

## <a name="return-value"></a><span data-ttu-id="ecca0-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ecca0-114">Return value</span></span>

<span data-ttu-id="ecca0-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ecca0-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ecca0-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ecca0-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecca0-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecca0-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ecca0-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="ecca0-118">Header</span></span></p></td><td><span data-ttu-id="ecca0-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ecca0-119">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ecca0-120"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecca0-120"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ecca0-121">**IGenericBufferDataCallback**</span><span class="sxs-lookup"><span data-stu-id="ecca0-121">**IGenericBufferDataCallback**</span></span>](/windows/desktop/direct3dtools/igenericbufferdatacallback)

 

 
