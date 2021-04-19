---
description: Obtient un handle vers la boîte de dialogue qui affiche les messages d’erreur et fournit un ou plusieurs boutons pour continuer, annuler ou abandonner l’application.
ms.assetid: 54deac2e-a395-45dc-b9f9-ecf8140fd9d7
title: 'IWiaAppErrorHandler :: GetWindow, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.GetWindow
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 89a3b2bf87d99c767ab3bea46a27c8a53fab7825
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517093"
---
# <a name="iwiaapperrorhandlergetwindow-method"></a><span data-ttu-id="24f3d-103">IWiaAppErrorHandler :: GetWindow, méthode</span><span class="sxs-lookup"><span data-stu-id="24f3d-103">IWiaAppErrorHandler::GetWindow method</span></span>

<span data-ttu-id="24f3d-104">Obtient un handle vers la boîte de dialogue qui affiche les messages d’erreur et fournit un ou plusieurs boutons pour continuer, annuler ou abandonner l’application.</span><span class="sxs-lookup"><span data-stu-id="24f3d-104">Gets a handle to the dialog box that displays error messages and provides one or more buttons to continue, cancel, or abort the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="24f3d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24f3d-105">Syntax</span></span>


```C++
HRESULT GetWindow(
  [out] HWND *phwnd
);
```



## <a name="parameters"></a><span data-ttu-id="24f3d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24f3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24f3d-107">*phwnd* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="24f3d-107">*phwnd* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24f3d-108">Type : \**HWND \** _</span><span class="sxs-lookup"><span data-stu-id="24f3d-108">Type: \**HWND\** _</span></span>

<span data-ttu-id="24f3d-109">HWND utilisé par le gestionnaire d’erreurs d’application, le gestionnaire d’erreurs de pilote et le gestionnaire d’erreurs par défaut pour les boîtes de dialogue de message de l’appareil (à la fois erreur et information).</span><span class="sxs-lookup"><span data-stu-id="24f3d-109">HWND used by the application error handler, the driver error handler, and the default error handler for device message dialog boxes (both error and informational).</span></span> <span data-ttu-id="24f3d-110">La valeur de sortie peut être _ \* NULL \* \*.</span><span class="sxs-lookup"><span data-stu-id="24f3d-110">The output value may be _\*NULL\*\*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24f3d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="24f3d-111">Return value</span></span>

<span data-ttu-id="24f3d-112">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="24f3d-112">Type: **HRESULT**</span></span>

<span data-ttu-id="24f3d-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="24f3d-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="24f3d-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="24f3d-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="24f3d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="24f3d-115">Remarks</span></span>

<span data-ttu-id="24f3d-116">*phwnd* pointe vers la fenêtre transmise dans [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md) par le proxy 2,0 d’acquisition d’images Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="24f3d-116">*phwnd* points to the window passed into [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md) by the Windows Image Acquisition (WIA) 2.0 Proxy.</span></span> <span data-ttu-id="24f3d-117">Cette fenêtre doit rester valide pendant toute la durée du transfert de données.</span><span class="sxs-lookup"><span data-stu-id="24f3d-117">This window must remain valid for the duration of the data transfer.</span></span>

## <a name="requirements"></a><span data-ttu-id="24f3d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24f3d-118">Requirements</span></span>



| <span data-ttu-id="24f3d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24f3d-119">Requirement</span></span> | <span data-ttu-id="24f3d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="24f3d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24f3d-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24f3d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="24f3d-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24f3d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="24f3d-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24f3d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="24f3d-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24f3d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="24f3d-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="24f3d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="24f3d-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="24f3d-126"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="24f3d-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="24f3d-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="24f3d-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="24f3d-128"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="24f3d-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="24f3d-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="24f3d-130"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24f3d-130"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




