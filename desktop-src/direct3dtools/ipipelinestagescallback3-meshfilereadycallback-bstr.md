---
description: Rappel qui avertit l’hôte des informations de maillage écrites par la requête associée.
MS-HAID: vspixengine.IPipeLineStagesCallback3\_MeshFileReadyCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback3 :: MeshFileReadyCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BD4719A5-AC07-446A-A7CA-5978F869F66E
api_name:
- IPipeLineStagesCallback3.MeshFileReadyCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7974a9f04acf8e620d792b377fa482dab6de71dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515127"
---
# <a name="span-idvspixengineipipelinestagescallback3_meshfilereadycallback_bstrspanipipelinestagescallback3meshfilereadycallback-method"></a><span data-ttu-id="7bc64-103"><span id="vspixengine.ipipelinestagescallback3_meshfilereadycallback_bstr"></span>IPipeLineStagesCallback3 :: MeshFileReadyCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="7bc64-103"><span id="vspixengine.ipipelinestagescallback3_meshfilereadycallback_bstr"></span>IPipeLineStagesCallback3::MeshFileReadyCallback method</span></span>

<span data-ttu-id="7bc64-104">Rappel qui avertit l’hôte des informations de maillage écrites par la requête associée.</span><span class="sxs-lookup"><span data-stu-id="7bc64-104">A callback that notifies the host of Mesh information written by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bc64-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7bc64-105">Syntax</span></span>


```C++
HRESULT MeshFileReadyCallback(
   BSTR meshFilename
);
```

## <a name="parameters"></a><span data-ttu-id="7bc64-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7bc64-106">Parameters</span></span>

<span data-ttu-id="7bc64-107">*meshFilename* </span><span class="sxs-lookup"><span data-stu-id="7bc64-107">*meshFilename* </span></span>  
<span data-ttu-id="7bc64-108">Chaîne COM contenant le nom du chemin d’accès du fichier dans lequel les données de maillage sont écrites.</span><span class="sxs-lookup"><span data-stu-id="7bc64-108">A COM string containing the pathname of the file where the mesh data is written.</span></span>

## <a name="return-value"></a><span data-ttu-id="7bc64-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7bc64-109">Return value</span></span>

<span data-ttu-id="7bc64-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7bc64-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7bc64-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7bc64-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bc64-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7bc64-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="7bc64-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="7bc64-113">Header</span></span></p></td><td><span data-ttu-id="7bc64-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="7bc64-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="7bc64-115"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bc64-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="7bc64-116">**IPipeLineStagesCallback3**</span><span class="sxs-lookup"><span data-stu-id="7bc64-116">**IPipeLineStagesCallback3**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback3)

 

 
