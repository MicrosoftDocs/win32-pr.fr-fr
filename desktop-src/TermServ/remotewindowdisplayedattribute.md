---
title: Énumération RemoteWindowDisplayedAttribute
description: Utilisé avec la méthode pour spécifier des informations sur l’événement.
ms.assetid: 22549063-6979-48F2-AEA5-94BFC848C707
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’énumération RemoteWindowDisplayedAttribute
topic_type:
- apiref
api_name:
- RemoteWindowDisplayedAttribute
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a137d0ba0b6b692c949ab6c2a0c7b59b0d1fb341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536914"
---
# <a name="remotewindowdisplayedattribute-enumeration"></a><span data-ttu-id="9d6aa-104">Énumération RemoteWindowDisplayedAttribute</span><span class="sxs-lookup"><span data-stu-id="9d6aa-104">RemoteWindowDisplayedAttribute enumeration</span></span>

<span data-ttu-id="9d6aa-105">Utilisé avec la méthode pour spécifier des informations sur l’événement.</span><span class="sxs-lookup"><span data-stu-id="9d6aa-105">Used with the method to specify information about the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d6aa-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d6aa-106">Syntax</span></span>


```C++
typedef enum  { 
  remoteAppWindowNone          = 0,
  remoteAppWindowDisplayed     = 1,
  remoteAppShellIconDisplayed  = 2
} RemoteWindowDisplayedAttribute;
```



## <a name="constants"></a><span data-ttu-id="9d6aa-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="9d6aa-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9d6aa-108"><span id="remoteAppWindowNone"></span><span id="remoteappwindownone"></span><span id="REMOTEAPPWINDOWNONE"></span>**remoteAppWindowNone**</span><span class="sxs-lookup"><span data-stu-id="9d6aa-108"><span id="remoteAppWindowNone"></span><span id="remoteappwindownone"></span><span id="REMOTEAPPWINDOWNONE"></span>**remoteAppWindowNone**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9d6aa-109"><span id="remoteAppWindowDisplayed"></span><span id="remoteappwindowdisplayed"></span><span id="REMOTEAPPWINDOWDISPLAYED"></span>**remoteAppWindowDisplayed**</span><span class="sxs-lookup"><span data-stu-id="9d6aa-109"><span id="remoteAppWindowDisplayed"></span><span id="remoteappwindowdisplayed"></span><span id="REMOTEAPPWINDOWDISPLAYED"></span>**remoteAppWindowDisplayed**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9d6aa-110"><span id="remoteAppShellIconDisplayed"></span><span id="remoteappshellicondisplayed"></span><span id="REMOTEAPPSHELLICONDISPLAYED"></span>**remoteAppShellIconDisplayed**</span><span class="sxs-lookup"><span data-stu-id="9d6aa-110"><span id="remoteAppShellIconDisplayed"></span><span id="remoteappshellicondisplayed"></span><span id="REMOTEAPPSHELLICONDISPLAYED"></span>**remoteAppShellIconDisplayed**</span></span>
<span data-ttu-id="9d6aa-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9d6aa-111"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="9d6aa-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d6aa-112">Requirements</span></span>



| <span data-ttu-id="9d6aa-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d6aa-113">Requirement</span></span> | <span data-ttu-id="9d6aa-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d6aa-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d6aa-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d6aa-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9d6aa-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9d6aa-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="9d6aa-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d6aa-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9d6aa-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9d6aa-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="9d6aa-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9d6aa-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="9d6aa-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d6aa-120"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d6aa-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d6aa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d6aa-122">**OnRemoteWindowDisplayed**</span><span class="sxs-lookup"><span data-stu-id="9d6aa-122">**OnRemoteWindowDisplayed**</span></span>](imstscaxevents-onremotewindowdisplayed.md)
</dt> </dl>

 

 





