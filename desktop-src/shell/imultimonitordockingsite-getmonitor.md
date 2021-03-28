---
description: Obtient l’analyseur par défaut actuel.
title: 'IMultiMonitorDockingSite :: GetMonitor, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.GetMonitor
api_type:
- COM
api_location: ''
ms.assetid: 0bae75eb-ebd5-4de4-9249-0e9bb489f61f
ms.openlocfilehash: 1260da5ee4404a7ec4597a57e7e3836d6f133426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991696"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a><span data-ttu-id="d6485-103">IMultiMonitorDockingSite :: GetMonitor, méthode</span><span class="sxs-lookup"><span data-stu-id="d6485-103">IMultiMonitorDockingSite::GetMonitor method</span></span>

<span data-ttu-id="d6485-104">Obtient l’analyseur par défaut actuel.</span><span class="sxs-lookup"><span data-stu-id="d6485-104">Gets the current default monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6485-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6485-105">Syntax</span></span>


```C++
HRESULT GetMonitor(
  [in]  IUnknown *punkSrc,
  [out] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="d6485-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6485-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6485-107">*punkSrc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d6485-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6485-108">Tapez : \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="d6485-108">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="d6485-109">Pointeur vers l’objet implémentant l’interface [_ *IDockingWindow* \*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) pour laquelle l’analyse est demandée.</span><span class="sxs-lookup"><span data-stu-id="d6485-109">A pointer to the object implementing the [_ *IDockingWindow*\*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="d6485-110">*phMon* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d6485-110">*phMon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6485-111">Tapez : \**HMONITOR \** _</span><span class="sxs-lookup"><span data-stu-id="d6485-111">Type: \**HMONITOR\** _</span></span>

<span data-ttu-id="d6485-112">Quand la fonction retourne une valeur, contient un pointeur vers le handle de l’analyseur par défaut.</span><span class="sxs-lookup"><span data-stu-id="d6485-112">When the function returns, contains a pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6485-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d6485-113">Return value</span></span>

<span data-ttu-id="d6485-114">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d6485-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d6485-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d6485-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d6485-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d6485-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6485-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d6485-117">Requirements</span></span>



| <span data-ttu-id="d6485-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6485-118">Requirement</span></span> | <span data-ttu-id="d6485-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6485-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="d6485-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6485-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d6485-121">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6485-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d6485-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6485-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d6485-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6485-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
