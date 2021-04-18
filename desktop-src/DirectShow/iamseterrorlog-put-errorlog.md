---
description: La \_ méthode put ErrorLog spécifie un journal des erreurs pour l’objet.
ms.assetid: 39da3fb0-57d3-452f-b2ae-6dcd84fa5c8e
title: IAMSetErrorLog ::p ut_ErrorLog, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog.put_ErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 189f0fed57d67d7632d07839ee82dd13494eb418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533018"
---
# <a name="iamseterrorlogput_errorlog-method"></a><span data-ttu-id="751bf-103">IAMSetErrorLog ::p ut \_ ErrorLog (méthode)</span><span class="sxs-lookup"><span data-stu-id="751bf-103">IAMSetErrorLog::put\_ErrorLog method</span></span>

> [!Note]  
> <span data-ttu-id="751bf-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="751bf-104">\[Deprecated.</span></span> <span data-ttu-id="751bf-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="751bf-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="751bf-106">La `put_ErrorLog` méthode spécifie un journal des erreurs pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="751bf-106">The `put_ErrorLog` method specifies an error log for the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="751bf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="751bf-107">Syntax</span></span>


```C++
HRESULT put_ErrorLog(
  [in] IAMErrorLog *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="751bf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="751bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="751bf-109">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="751bf-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="751bf-110">Pointeur vers l’interface [**IAMErrorLog**](iamerrorlog.md) du journal des erreurs.</span><span class="sxs-lookup"><span data-stu-id="751bf-110">Pointer to the error log's [**IAMErrorLog**](iamerrorlog.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="751bf-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="751bf-111">Return value</span></span>

<span data-ttu-id="751bf-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="751bf-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="751bf-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="751bf-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="751bf-114">Notes</span><span class="sxs-lookup"><span data-stu-id="751bf-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="751bf-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="751bf-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="751bf-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="751bf-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="751bf-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="751bf-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="751bf-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="751bf-118">Requirements</span></span>



| <span data-ttu-id="751bf-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="751bf-119">Requirement</span></span> | <span data-ttu-id="751bf-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="751bf-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="751bf-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="751bf-121">Header</span></span><br/>  | <dl> <span data-ttu-id="751bf-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="751bf-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="751bf-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="751bf-123">Library</span></span><br/> | <dl> <span data-ttu-id="751bf-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="751bf-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="751bf-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="751bf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="751bf-126">**Interface IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="751bf-126">**IAMSetErrorLog Interface**</span></span>](iamseterrorlog.md)
</dt> <dt>

[<span data-ttu-id="751bf-127">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="751bf-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




