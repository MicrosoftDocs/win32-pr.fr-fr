---
description: Se produit lors de l’activation d’une application du Windows Store.
ms.assetid: CA0DB2D4-3417-48F5-8455-D87D0F323A1E
title: 'ICoreApplicationView :: Activated, événement (Windows. ApplicationModel. Core. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612f7110aa149396b18815afe664ee404c70fc52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201444"
---
# <a name="icoreapplicationviewactivated-event"></a><span data-ttu-id="2e53d-103">ICoreApplicationView :: Activated, événement</span><span class="sxs-lookup"><span data-stu-id="2e53d-103">ICoreApplicationView::Activated event</span></span>

<span data-ttu-id="2e53d-104">Se produit lors de l’activation d’une application du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="2e53d-104">Occurs when a Windows Store app is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e53d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e53d-105">Syntax</span></span>


```C++
void Activated(
  [in] ITypedEventHandler<ICoreApplicationView*, IActivatedEventArgs*> handler
);
```



## <a name="parameters"></a><span data-ttu-id="2e53d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e53d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e53d-107">*Gestionnaire* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e53d-107">*handler* \[in\]</span></span>
<span data-ttu-id="2e53d-108"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2e53d-108"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="2e53d-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2e53d-109">Return value</span></span>

<span data-ttu-id="2e53d-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2e53d-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e53d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2e53d-111">Remarks</span></span>

<span data-ttu-id="2e53d-112">N’appelez pas la méthode [**Exit**](/previous-versions//hh438368(v=vs.85)) à partir du *Gestionnaire*.</span><span class="sxs-lookup"><span data-stu-id="2e53d-112">Do not call the [**Exit**](/previous-versions//hh438368(v=vs.85)) method from within *handler*.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e53d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e53d-113">Requirements</span></span>



| <span data-ttu-id="2e53d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e53d-114">Requirement</span></span> | <span data-ttu-id="2e53d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e53d-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e53d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e53d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2e53d-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2e53d-117">Windows 8</span></span><br/>                                                                                         |
| <span data-ttu-id="2e53d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e53d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2e53d-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2e53d-119">Windows Server 2012</span></span><br/>                                                                               |
| <span data-ttu-id="2e53d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="2e53d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e53d-121"><dt>Windows. ApplicationModel. Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e53d-121"><dt>Windows.ApplicationModel.Core.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e53d-122">MIDL</span><span class="sxs-lookup"><span data-stu-id="2e53d-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2e53d-123"><dt>Windows. ApplicationModel. Core. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2e53d-123"><dt>Windows.ApplicationModel.Core.idl</dt></span></span> </dl> |



 

 
