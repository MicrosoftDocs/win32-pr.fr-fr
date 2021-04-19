---
description: La méthode GetMaximumCursors récupère le nombre maximal de curseurs pris en charge par un périphérique tablette.
ms.assetid: 5a43d792-e64c-4506-9792-31efe0885959
title: 'ITablet3 :: GetMaximumCursors, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.GetMaximumCursors
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 7c40184d35ac1d42cb5f5e845396b40efc2d928e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533949"
---
# <a name="itablet3getmaximumcursors-method"></a><span data-ttu-id="3b7dc-103">ITablet3 :: GetMaximumCursors, méthode</span><span class="sxs-lookup"><span data-stu-id="3b7dc-103">ITablet3::GetMaximumCursors method</span></span>

<span data-ttu-id="3b7dc-104">La méthode **GetMaximumCursors** récupère le nombre maximal de curseurs pris en charge par un périphérique tablette.</span><span class="sxs-lookup"><span data-stu-id="3b7dc-104">The **GetMaximumCursors** method retrieves the maximum number of cursors that a tablet device supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b7dc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b7dc-105">Syntax</span></span>


```C++
HRESULT GetMaximumCursors(
   ULONG *pMaximumCursors
);
```



## <a name="parameters"></a><span data-ttu-id="3b7dc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b7dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b7dc-107">*pMaximumCursors*</span><span class="sxs-lookup"><span data-stu-id="3b7dc-107">*pMaximumCursors*</span></span> 
</dt> <dd>

<span data-ttu-id="3b7dc-108">Nombre maximal d’entrées que l’appareil prend en charge.</span><span class="sxs-lookup"><span data-stu-id="3b7dc-108">The maximum number of inputs that the device supports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b7dc-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b7dc-109">Return value</span></span>

<span data-ttu-id="3b7dc-110">Retourne S \_ OK en cas de réussite ; sinon, retourne un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3b7dc-110">Returns S\_OK on success; otherwise, returns an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b7dc-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b7dc-111">Requirements</span></span>



| <span data-ttu-id="3b7dc-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b7dc-112">Requirement</span></span> | <span data-ttu-id="3b7dc-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b7dc-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b7dc-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b7dc-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3b7dc-115">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b7dc-115">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3b7dc-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b7dc-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3b7dc-117">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b7dc-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3b7dc-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3b7dc-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="3b7dc-119"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3b7dc-119"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b7dc-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b7dc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b7dc-121">**ITablet3**</span><span class="sxs-lookup"><span data-stu-id="3b7dc-121">**ITablet3**</span></span>](itablet3.md)
</dt> </dl>

 

 




