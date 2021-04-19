---
description: La \_ méthode obtenir ErrorLog récupère le journal des erreurs actuel de cet objet.
ms.assetid: 580b8a06-6bf2-49ef-a5fb-5e6df2f09793
title: 'IAMSetErrorLog :: get_ErrorLog, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog.get_ErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 508a73d6475698dca628de7e3bb96001fe13bcd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541066"
---
# <a name="iamseterrorlogget_errorlog-method"></a><span data-ttu-id="4d41b-103">IAMSetErrorLog :: obtient le \_ Journal des erreurs (méthode)</span><span class="sxs-lookup"><span data-stu-id="4d41b-103">IAMSetErrorLog::get\_ErrorLog method</span></span>

> [!Note]  
> <span data-ttu-id="4d41b-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="4d41b-104">\[Deprecated.</span></span> <span data-ttu-id="4d41b-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4d41b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4d41b-106">La `get_ErrorLog` méthode récupère le journal des erreurs actuel de cet objet.</span><span class="sxs-lookup"><span data-stu-id="4d41b-106">The `get_ErrorLog` method retrieves the current error log for this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d41b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d41b-107">Syntax</span></span>


```C++
HRESULT get_ErrorLog(
  [out, retval] IAMErrorLog **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="4d41b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d41b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d41b-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4d41b-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4d41b-110">Reçoit un pointeur vers l’interface [**IAMErrorLog**](iamerrorlog.md) du journal des erreurs.</span><span class="sxs-lookup"><span data-stu-id="4d41b-110">Receives a pointer to the error log's [**IAMErrorLog**](iamerrorlog.md) interface.</span></span> <span data-ttu-id="4d41b-111">Si la chronologie n’a pas de journal des erreurs, la valeur est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="4d41b-111">If the timeline does not have an error log, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d41b-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4d41b-112">Return value</span></span>

<span data-ttu-id="4d41b-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4d41b-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4d41b-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4d41b-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d41b-115">Notes</span><span class="sxs-lookup"><span data-stu-id="4d41b-115">Remarks</span></span>

<span data-ttu-id="4d41b-116">Si la valeur retournée dans *pval* n’est pas **null**, l’interface [**IAMErrorLog**](iamerrorlog.md) a un nombre de références en attente.</span><span class="sxs-lookup"><span data-stu-id="4d41b-116">If the value returned in *pVal* is not **NULL**, the [**IAMErrorLog**](iamerrorlog.md) interface has an outstanding reference count.</span></span> <span data-ttu-id="4d41b-117">Veillez à libérer l’interface lorsque vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="4d41b-117">Be sure to release the interface when you are done using it.</span></span>

> [!Note]  
> <span data-ttu-id="4d41b-118">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="4d41b-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4d41b-119">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4d41b-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4d41b-120">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4d41b-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4d41b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d41b-121">Requirements</span></span>



| <span data-ttu-id="4d41b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d41b-122">Requirement</span></span> | <span data-ttu-id="4d41b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d41b-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d41b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="4d41b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4d41b-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d41b-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4d41b-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4d41b-126">Library</span></span><br/> | <dl> <span data-ttu-id="4d41b-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d41b-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d41b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d41b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d41b-129">**Interface IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="4d41b-129">**IAMSetErrorLog Interface**</span></span>](iamseterrorlog.md)
</dt> <dt>

[<span data-ttu-id="4d41b-130">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="4d41b-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




