---
title: Méthode IRemoteDesktopClientEvents OnDisconnected
description: Appelé lorsque le contrôle client a été déconnecté d’une session à distance.
ms.assetid: EA26B530-0AA8-49D6-8E3C-E53179FC5104
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnDisconnected
- Méthode OnDisconnected Services Bureau à distance, interface IRemoteDesktopClientEvents
- Services Bureau à distance de l’interface IRemoteDesktopClientEvents, méthode OnDisconnected
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd59b03fe9cb23309d53773289291c8a791935a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742381"
---
# <a name="iremotedesktopclienteventsondisconnected-method"></a><span data-ttu-id="c3d89-106">IRemoteDesktopClientEvents :: OnDisconnected, méthode</span><span class="sxs-lookup"><span data-stu-id="c3d89-106">IRemoteDesktopClientEvents::OnDisconnected method</span></span>

<span data-ttu-id="c3d89-107">Appelé lorsque le contrôle client a été déconnecté d’une session à distance.</span><span class="sxs-lookup"><span data-stu-id="c3d89-107">Called when the client control has been disconnected from a remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3d89-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3d89-108">Syntax</span></span>


```C++
void OnDisconnected(
  [in] long disconnectReason,
  [in] long ExtendedDisconnectReason,
  [in] BSTR disconnectErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="c3d89-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3d89-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3d89-110">*disconnectReason* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3d89-110">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3d89-111">Raison de l’événement de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="c3d89-111">The reason for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="c3d89-112">*ExtendedDisconnectReason* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3d89-112">*ExtendedDisconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3d89-113">Informations étendues pour l’événement de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="c3d89-113">Extended information for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="c3d89-114">*disconnectErrorMessage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3d89-114">*disconnectErrorMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3d89-115">Message d’erreur pour l’événement de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="c3d89-115">The error message for the disconnect event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3d89-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3d89-116">Return value</span></span>

<span data-ttu-id="c3d89-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c3d89-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3d89-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3d89-118">Requirements</span></span>



| <span data-ttu-id="c3d89-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3d89-119">Requirement</span></span> | <span data-ttu-id="c3d89-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3d89-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3d89-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3d89-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c3d89-122">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c3d89-122">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="c3d89-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3d89-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c3d89-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3d89-124">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="c3d89-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c3d89-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="c3d89-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3d89-126"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="c3d89-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c3d89-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3d89-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3d89-128"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="c3d89-129">IID</span><span class="sxs-lookup"><span data-stu-id="c3d89-129">IID</span></span><br/>                      | <span data-ttu-id="c3d89-130">DIID \_ IRemoteDesktopClientEvents est défini comme 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="c3d89-130">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c3d89-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3d89-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3d89-132">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="c3d89-132">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





