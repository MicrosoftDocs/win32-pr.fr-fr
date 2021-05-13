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
ms.openlocfilehash: 2cd437fd6c0e842eb314db6c57420af6b54b05ff
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840640"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a><span data-ttu-id="4a97d-103">IMultiMonitorDockingSite :: GetMonitor, méthode</span><span class="sxs-lookup"><span data-stu-id="4a97d-103">IMultiMonitorDockingSite::GetMonitor method</span></span>

<span data-ttu-id="4a97d-104">Obtient l’analyseur par défaut actuel.</span><span class="sxs-lookup"><span data-stu-id="4a97d-104">Gets the current default monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a97d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a97d-105">Syntax</span></span>


```C++
HRESULT GetMonitor(
  [in]  IUnknown *punkSrc,
  [out] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="4a97d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a97d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a97d-107">*punkSrc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4a97d-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a97d-108">Type : **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="4a97d-108">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="4a97d-109">Pointeur vers l’objet implémentant l’interface [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) pour laquelle l’analyse est demandée.</span><span class="sxs-lookup"><span data-stu-id="4a97d-109">A pointer to the object implementing the [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="4a97d-110">*phMon* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4a97d-110">*phMon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a97d-111">Type : **HMONITOR \***</span><span class="sxs-lookup"><span data-stu-id="4a97d-111">Type: **HMONITOR\***</span></span>

<span data-ttu-id="4a97d-112">Quand la fonction retourne une valeur, contient un pointeur vers le handle de l’analyseur par défaut.</span><span class="sxs-lookup"><span data-stu-id="4a97d-112">When the function returns, contains a pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a97d-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4a97d-113">Return value</span></span>

<span data-ttu-id="4a97d-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4a97d-114">Type: **HRESULT**</span></span>

<span data-ttu-id="4a97d-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4a97d-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4a97d-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4a97d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a97d-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4a97d-117">Requirements</span></span>



| <span data-ttu-id="4a97d-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a97d-118">Requirement</span></span> | <span data-ttu-id="4a97d-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a97d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="4a97d-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a97d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4a97d-121">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a97d-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4a97d-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a97d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4a97d-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a97d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
