---
description: Fonction de rappel utilisée pour informer l’hôte des informations de la table objet.
MS-HAID: vspixengine.IObjectTableCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IObjectTableCallback :: ResultCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AAD02864-AE08-406B-A0E9-2228DC9A73E7
api_name:
- IObjectTableCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 66247dddbf0926b420faa998461393397a4717b7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747396"
---
# <a name="span-idvspixengineiobjecttablecallback_resultcallback_dword_dword_dword_variant_arrspaniobjecttablecallbackresultcallback-method"></a><span data-ttu-id="48b09-103"><span id="vspixengine.iobjecttablecallback_resultcallback_dword_dword_dword_variant_arr"></span>IObjectTableCallback :: ResultCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="48b09-103"><span id="vspixengine.iobjecttablecallback_resultcallback_dword_dword_dword_variant_arr"></span>IObjectTableCallback::ResultCallback method</span></span>

<span data-ttu-id="48b09-104">Fonction de rappel utilisée pour informer l’hôte des informations de la table objet.</span><span class="sxs-lookup"><span data-stu-id="48b09-104">A callback function used to notify the host of object table information.</span></span>

## <a name="syntax"></a><span data-ttu-id="48b09-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="48b09-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD      numElements,
   DWORD      numRows,
   DWORD      numColumns,
   VARIANT [] count0_pRowData
);
```

## <a name="parameters"></a><span data-ttu-id="48b09-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48b09-106">Parameters</span></span>

<span data-ttu-id="48b09-107">*numElements* </span><span class="sxs-lookup"><span data-stu-id="48b09-107">*numElements* </span></span>  
<span data-ttu-id="48b09-108">Nombre total de champs dans toutes les colonnes de tous les objets.</span><span class="sxs-lookup"><span data-stu-id="48b09-108">The total number of fields in all columns of all objects.</span></span>

<span data-ttu-id="48b09-109">*numRows* </span><span class="sxs-lookup"><span data-stu-id="48b09-109">*numRows* </span></span>  
<span data-ttu-id="48b09-110">Nombre d’objets en cours de transfert.</span><span class="sxs-lookup"><span data-stu-id="48b09-110">The number of objects being transferred.</span></span>

<span data-ttu-id="48b09-111">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="48b09-111">*numColumns* </span></span>  
<span data-ttu-id="48b09-112">Nombre de colonnes (champs) d’informations transférées pour chaque objet.</span><span class="sxs-lookup"><span data-stu-id="48b09-112">The number of columns (fields) of information being transferred for each object.</span></span>

<span data-ttu-id="48b09-113">*count0 \_ pRowData* </span><span class="sxs-lookup"><span data-stu-id="48b09-113">*count0\_pRowData* </span></span>  
<span data-ttu-id="48b09-114">Informations sur les objets ; un élément pour chaque champ de chaque objet.</span><span class="sxs-lookup"><span data-stu-id="48b09-114">Information about the objects; one item for each field of each object.</span></span>

## <a name="return-value"></a><span data-ttu-id="48b09-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="48b09-115">Return value</span></span>

<span data-ttu-id="48b09-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="48b09-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="48b09-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="48b09-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="48b09-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48b09-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="48b09-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="48b09-119">Header</span></span></p></td><td><span data-ttu-id="48b09-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="48b09-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="48b09-121"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48b09-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="48b09-122">**IObjectTableCallback**</span><span class="sxs-lookup"><span data-stu-id="48b09-122">**IObjectTableCallback**</span></span>](/windows/desktop/direct3dtools/iobjecttablecallback)

 

 
