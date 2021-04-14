---
title: Méthode IConfigAsfWriter GetIndexMode
description: La méthode GetIndexMode récupère le mode d’index temporel actuel.
ms.assetid: beb874ea-d0d5-4323-a817-47984911da4c
keywords:
- Méthode GetIndexMode format Windows Media
- Méthode GetIndexMode format Windows Media, interface IConfigAsfWriter
- Interface IConfigAsfWriter Windows Media format, méthode GetIndexMode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb701f591579d3113e79b0b9b74167ac8de3d75f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382211"
---
# <a name="iconfigasfwritergetindexmode-method"></a><span data-ttu-id="cc174-106">IConfigAsfWriter :: GetIndexMode, méthode</span><span class="sxs-lookup"><span data-stu-id="cc174-106">IConfigAsfWriter::GetIndexMode method</span></span>

<span data-ttu-id="cc174-107">La méthode **GetIndexMode** récupère le mode d’index temporel actuel.</span><span class="sxs-lookup"><span data-stu-id="cc174-107">The **GetIndexMode** method retrieves the current temporal index mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc174-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc174-108">Syntax</span></span>


```C++
HRESULT GetIndexMode(
  [out] BOOL *pbIndexFile
);
```



## <a name="parameters"></a><span data-ttu-id="cc174-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc174-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc174-110">*pbIndexFile* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cc174-110">*pbIndexFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc174-111">Pointeur vers une variable de type **bool** qui reçoit le paramètre de mode d’index temporel.</span><span class="sxs-lookup"><span data-stu-id="cc174-111">Pointer to a variable of type **BOOL** that receives the temporal index mode setting.</span></span> <span data-ttu-id="cc174-112">La valeur **true** indique que l’enregistreur ASF WM est configuré pour écrire des fichiers indexés temporellement.</span><span class="sxs-lookup"><span data-stu-id="cc174-112">A value of **TRUE** indicates that the WM ASF Writer is configured to write temporally indexed files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc174-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cc174-113">Return value</span></span>

<span data-ttu-id="cc174-114">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cc174-114">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="cc174-115">En cas d’échec, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cc174-115">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc174-116">Notes</span><span class="sxs-lookup"><span data-stu-id="cc174-116">Remarks</span></span>

<span data-ttu-id="cc174-117">Utilisez cette méthode pour déterminer si l' [enregistreur ASF WM](wm-asf-writer-filter.md) est actuellement configuré pour écrire des fichiers ASF indexés temporellement.</span><span class="sxs-lookup"><span data-stu-id="cc174-117">Use this method to determine whether the [WM ASF Writer](wm-asf-writer-filter.md) is currently configured to write temporally indexed ASF files.</span></span> <span data-ttu-id="cc174-118">Pour plus d’informations sur les fichiers indexés et indexés dans le cadre d’une indexation temporelle, consultez les notes pour [**IConfigAsfWriter :: SetIndexMode**](iconfigasfwriter-setindexmode.md).</span><span class="sxs-lookup"><span data-stu-id="cc174-118">For more information on temporally indexed and frame-indexed files, see the Remarks for [**IConfigAsfWriter::SetIndexMode**](iconfigasfwriter-setindexmode.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="cc174-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc174-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="cc174-120">[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cc174-120">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 