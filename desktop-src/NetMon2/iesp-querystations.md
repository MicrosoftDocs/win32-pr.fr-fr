---
description: La méthode QueryStations fournit la liste de tous les ordinateurs qui utilisent actuellement Moniteur réseau pour capturer les données réseau.
ms.assetid: 5ad99810-e463-4477-a542-cf4dfa6967a4
title: 'IESP :: QueryStations, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 5287f472b2a0641eb29e4f1b37b6fe4e089dfa86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544613"
---
# <a name="iespquerystations-method"></a><span data-ttu-id="4f6e7-103">IESP :: QueryStations, méthode</span><span class="sxs-lookup"><span data-stu-id="4f6e7-103">IESP::QueryStations method</span></span>

<span data-ttu-id="4f6e7-104">La méthode **QueryStations** fournit la liste de tous les ordinateurs qui utilisent actuellement Moniteur réseau pour capturer les données réseau.</span><span class="sxs-lookup"><span data-stu-id="4f6e7-104">The **QueryStations** method provides a list of all computers that currently use Network Monitor to capture network data.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f6e7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f6e7-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a><span data-ttu-id="4f6e7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f6e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f6e7-107">*lpQueryTable* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4f6e7-107">*lpQueryTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f6e7-108">Pointeur vers une structure [QUERYTABLE](querytable.md) .</span><span class="sxs-lookup"><span data-stu-id="4f6e7-108">Pointer to a [QUERYTABLE](querytable.md) structure.</span></span> <span data-ttu-id="4f6e7-109">En entrée, cette structure doit contenir le nombre maximal d’ordinateurs que vous souhaitez Moniteur réseau retourner et un tableau de structures [STATIONQUERY](stationquery.md) .</span><span class="sxs-lookup"><span data-stu-id="4f6e7-109">On input, this structure must contain the maximum number of computers you want Network Monitor to return and an array of [STATIONQUERY](stationquery.md) structures.</span></span>

<span data-ttu-id="4f6e7-110">Lors de la sortie, cette structure retourne le nombre d’ordinateurs qui capturent des données et une structure [STATIONQUERY](stationquery.md) pour chaque ordinateur trouvé.</span><span class="sxs-lookup"><span data-stu-id="4f6e7-110">On output, this structure returns the number of computers that are capturing data and a [STATIONQUERY](stationquery.md) structure for each computer found.</span></span> <span data-ttu-id="4f6e7-111">Notez que ce total peut inclure des ordinateurs utilisant des versions de Moniteur réseau qui prédatent la version 2,0.</span><span class="sxs-lookup"><span data-stu-id="4f6e7-111">Note that this total may include computers using versions of Network Monitor that predate version 2.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f6e7-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4f6e7-112">Return value</span></span>

<span data-ttu-id="4f6e7-113">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="4f6e7-113">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="4f6e7-114">Si la méthode échoue, la valeur de retour est le code d’erreur suivant :</span><span class="sxs-lookup"><span data-stu-id="4f6e7-114">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="4f6e7-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4f6e7-115">Return code</span></span>                                                                                           | <span data-ttu-id="4f6e7-116">Description</span><span class="sxs-lookup"><span data-stu-id="4f6e7-116">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="4f6e7-117"><dt>**NMERR \_ \_ de \_ mémoire insuffisante**</dt></span><span class="sxs-lookup"><span data-stu-id="4f6e7-117"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="4f6e7-118">La mémoire nécessaire pour traiter cette requête n’était pas disponible.</span><span class="sxs-lookup"><span data-stu-id="4f6e7-118">The memory needed to process this query was unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4f6e7-119">Notes</span><span class="sxs-lookup"><span data-stu-id="4f6e7-119">Remarks</span></span>

<span data-ttu-id="4f6e7-120">Cette méthode peut être appelée à tout moment après l’appel de la méthode [CreateNPPInterface](createnppinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="4f6e7-120">This method can be called at any time after the [CreateNPPInterface](createnppinterface.md) method is called.</span></span> <span data-ttu-id="4f6e7-121">Un appel à cette méthode est un appel synchrone, qui peut prendre plusieurs secondes pour s’exécuter Moniteur réseau attend que les ordinateurs distants répondent à la requête.</span><span class="sxs-lookup"><span data-stu-id="4f6e7-121">A call to this method is a synchronous call, which may take several seconds to complete as Network Monitor waits for remote computers to respond to the query.</span></span> <span data-ttu-id="4f6e7-122">Seuls les ordinateurs sur le sous-réseau local peuvent être interrogés.</span><span class="sxs-lookup"><span data-stu-id="4f6e7-122">Only computers on the local subnet can be queried.</span></span>

<span data-ttu-id="4f6e7-123">Il vous incombe d’allouer la mémoire pour la structure [QUERYTABLE](querytable.md) et de libérer de la mémoire une fois que la table n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4f6e7-123">It is your responsibility to allocate the memory for the [QUERYTABLE](querytable.md) structure and free that memory after the table is no longer needed.</span></span> <span data-ttu-id="4f6e7-124">Cette exigence comprend la mémoire nécessaire pour le tableau [STATIONQUERY](stationquery.md) utilisé dans QUERYTABLE.</span><span class="sxs-lookup"><span data-stu-id="4f6e7-124">This requirement includes the memory needed for the [STATIONQUERY](stationquery.md) array used in QUERYTABLE.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f6e7-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f6e7-125">Requirements</span></span>



| <span data-ttu-id="4f6e7-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f6e7-126">Requirement</span></span> | <span data-ttu-id="4f6e7-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f6e7-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f6e7-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f6e7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4f6e7-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f6e7-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="4f6e7-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f6e7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4f6e7-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f6e7-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="4f6e7-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f6e7-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f6e7-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f6e7-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="4f6e7-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4f6e7-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f6e7-135"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f6e7-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f6e7-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f6e7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f6e7-137">IESP</span><span class="sxs-lookup"><span data-stu-id="4f6e7-137">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="4f6e7-138">QUERYTABLE</span><span class="sxs-lookup"><span data-stu-id="4f6e7-138">QUERYTABLE</span></span>](querytable.md)
</dt> <dt>

[<span data-ttu-id="4f6e7-139">STATIONQUERY</span><span class="sxs-lookup"><span data-stu-id="4f6e7-139">STATIONQUERY</span></span>](stationquery.md)
</dt> </dl>

 

 




