---
description: Modifie l’analyse qui est utilisée pour les barres d’outils ancrées sur un système à plusieurs écrans.
title: 'IMultiMonitorDockingSite :: SetMonitor, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.SetMonitor
api_type:
- COM
api_location: ''
ms.assetid: ba4ace13-7096-4f05-bcb0-ab37f1632406
ms.openlocfilehash: be773ee68c214f6a2fab8da89f1f48b867e71239
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841940"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a><span data-ttu-id="030cc-103">IMultiMonitorDockingSite :: SetMonitor, méthode</span><span class="sxs-lookup"><span data-stu-id="030cc-103">IMultiMonitorDockingSite::SetMonitor method</span></span>

<span data-ttu-id="030cc-104">Modifie l’analyse qui est utilisée pour les barres d’outils ancrées sur un système à plusieurs écrans.</span><span class="sxs-lookup"><span data-stu-id="030cc-104">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span>

## <a name="syntax"></a><span data-ttu-id="030cc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="030cc-105">Syntax</span></span>


```C++
HRESULT SetMonitor(
  [in]  IUnknown *punkSrc,
  [in]  HMONITOR hMonNew,
  [out] HMONITOR *phMonOld
);
```



## <a name="parameters"></a><span data-ttu-id="030cc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="030cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="030cc-107">*punkSrc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="030cc-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="030cc-108">Type : **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="030cc-108">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="030cc-109">Pointeur vers l’objet implémentant l’interface [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) pour laquelle l’analyse est en cours de modification.</span><span class="sxs-lookup"><span data-stu-id="030cc-109">A pointer to the object implementing the [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being altered.</span></span>

</dd> <dt>

<span data-ttu-id="030cc-110">*hMonNew* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="030cc-110">*hMonNew* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="030cc-111">Type : **HMONITOR**</span><span class="sxs-lookup"><span data-stu-id="030cc-111">Type: **HMONITOR**</span></span>

<span data-ttu-id="030cc-112">Handle vers l’analyseur qui remplace l’analyse par défaut existante.</span><span class="sxs-lookup"><span data-stu-id="030cc-112">A handle to the monitor that replaces the existing default monitor.</span></span>

</dd> <dt>

<span data-ttu-id="030cc-113">*phMonOld* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="030cc-113">*phMonOld* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="030cc-114">Type : **HMONITOR \***</span><span class="sxs-lookup"><span data-stu-id="030cc-114">Type: **HMONITOR\***</span></span>

<span data-ttu-id="030cc-115">Lorsque cette fonction est retournée, contient un pointeur vers le handle de l’analyseur par défaut précédent.</span><span class="sxs-lookup"><span data-stu-id="030cc-115">When this function returns, contains a pointer to the previous default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="030cc-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="030cc-116">Return value</span></span>

<span data-ttu-id="030cc-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="030cc-117">Type: **HRESULT**</span></span>

<span data-ttu-id="030cc-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="030cc-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="030cc-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="030cc-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="030cc-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="030cc-120">Requirements</span></span>



| <span data-ttu-id="030cc-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="030cc-121">Requirement</span></span> | <span data-ttu-id="030cc-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="030cc-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="030cc-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="030cc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="030cc-124">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="030cc-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="030cc-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="030cc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="030cc-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="030cc-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
