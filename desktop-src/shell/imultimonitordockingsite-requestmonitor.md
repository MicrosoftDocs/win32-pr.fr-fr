---
description: Vérifie que le moniteur est actif et disponible.
title: 'IMultiMonitorDockingSite :: RequestMonitor, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.RequestMonitor
api_type:
- COM
api_location: ''
ms.assetid: 9aa6eb20-de39-41f7-a17e-183f4088f972
ms.openlocfilehash: 7f219e5fd62fb4f85fd206501e6a53ac3927195a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841970"
---
# <a name="imultimonitordockingsiterequestmonitor-method"></a><span data-ttu-id="066f0-103">IMultiMonitorDockingSite :: RequestMonitor, méthode</span><span class="sxs-lookup"><span data-stu-id="066f0-103">IMultiMonitorDockingSite::RequestMonitor method</span></span>

<span data-ttu-id="066f0-104">Vérifie que le moniteur est actif et disponible.</span><span class="sxs-lookup"><span data-stu-id="066f0-104">Verifies that the monitor is active and available.</span></span>

## <a name="syntax"></a><span data-ttu-id="066f0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="066f0-105">Syntax</span></span>


```C++
HRESULT RequestMonitor(
  [in] IUnknown *punkSrc,
  [in] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="066f0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="066f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="066f0-107">*punkSrc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="066f0-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="066f0-108">Type : **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="066f0-108">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="066f0-109">Pointeur vers l’objet implémentant l’interface [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) .</span><span class="sxs-lookup"><span data-stu-id="066f0-109">A pointer to the object implementing the [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface.</span></span>

</dd> <dt>

<span data-ttu-id="066f0-110">*phMon* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="066f0-110">*phMon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="066f0-111">Type : **HMONITOR \***</span><span class="sxs-lookup"><span data-stu-id="066f0-111">Type: **HMONITOR\***</span></span>

<span data-ttu-id="066f0-112">Pointeur vers le handle de l’analyseur par défaut.</span><span class="sxs-lookup"><span data-stu-id="066f0-112">A pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="066f0-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="066f0-113">Return value</span></span>

<span data-ttu-id="066f0-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="066f0-114">Type: **HRESULT**</span></span>

<span data-ttu-id="066f0-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="066f0-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="066f0-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="066f0-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="066f0-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="066f0-117">Requirements</span></span>



| <span data-ttu-id="066f0-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="066f0-118">Requirement</span></span> | <span data-ttu-id="066f0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="066f0-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="066f0-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="066f0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="066f0-121">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="066f0-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="066f0-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="066f0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="066f0-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="066f0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
