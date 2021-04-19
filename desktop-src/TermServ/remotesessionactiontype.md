---
title: Énumération RemoteSessionActionType
description: Utilisé pour spécifier le type d’action à distance.
ms.assetid: C0DA0FA2-6FE0-4B40-B169-4592A1BE2AD6
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’énumération RemoteSessionActionType
topic_type:
- apiref
api_name:
- RemoteSessionActionType
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 291bb9fdd2cadfef3881bc27a47f9fc1bb1bce68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509908"
---
# <a name="remotesessionactiontype-enumeration"></a><span data-ttu-id="e4c68-104">Énumération RemoteSessionActionType</span><span class="sxs-lookup"><span data-stu-id="e4c68-104">RemoteSessionActionType enumeration</span></span>

<span data-ttu-id="e4c68-105">Utilisé pour spécifier le type d’action à distance.</span><span class="sxs-lookup"><span data-stu-id="e4c68-105">Used to specify the type of remote action.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4c68-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4c68-106">Syntax</span></span>


```C++
typedef enum _RemoteSessionActionType { 
  RemoteSessionActionCharms        = 0,
  RemoteSessionActionAppbar        = 1,
  RemoteSessionActionSnap          = 2,
  RemoteSessionActionStartScreen   = 3,
  RemoteSessionActionAppSwitch     = 4,
  RemoteSessionActionActionCenter  = 4
} RemoteSessionActionType;
```



## <a name="constants"></a><span data-ttu-id="e4c68-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="e4c68-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e4c68-108"><span id="RemoteSessionActionCharms"></span><span id="remotesessionactioncharms"></span><span id="REMOTESESSIONACTIONCHARMS"></span>**RemoteSessionActionCharms**</span><span class="sxs-lookup"><span data-stu-id="e4c68-108"><span id="RemoteSessionActionCharms"></span><span id="remotesessionactioncharms"></span><span id="REMOTESESSIONACTIONCHARMS"></span>**RemoteSessionActionCharms**</span></span>
</dt> <dd>

<span data-ttu-id="e4c68-109">Affiche les icônes dans la session à distance.</span><span class="sxs-lookup"><span data-stu-id="e4c68-109">Displays the charms in the remote session.</span></span>

</dd> <dt>

<span data-ttu-id="e4c68-110"><span id="RemoteSessionActionAppbar"></span><span id="remotesessionactionappbar"></span><span id="REMOTESESSIONACTIONAPPBAR"></span>**RemoteSessionActionAppbar**</span><span class="sxs-lookup"><span data-stu-id="e4c68-110"><span id="RemoteSessionActionAppbar"></span><span id="remotesessionactionappbar"></span><span id="REMOTESESSIONACTIONAPPBAR"></span>**RemoteSessionActionAppbar**</span></span>
</dt> <dd>

<span data-ttu-id="e4c68-111">Affiche la barre de l’application dans la session à distance.</span><span class="sxs-lookup"><span data-stu-id="e4c68-111">Displays the app bar in the remote session.</span></span>

</dd> <dt>

<span data-ttu-id="e4c68-112"><span id="RemoteSessionActionSnap"></span><span id="remotesessionactionsnap"></span><span id="REMOTESESSIONACTIONSNAP"></span>**RemoteSessionActionSnap**</span><span class="sxs-lookup"><span data-stu-id="e4c68-112"><span id="RemoteSessionActionSnap"></span><span id="remotesessionactionsnap"></span><span id="REMOTESESSIONACTIONSNAP"></span>**RemoteSessionActionSnap**</span></span>
</dt> <dd>

<span data-ttu-id="e4c68-113">Ancre l’application dans la session à distance.</span><span class="sxs-lookup"><span data-stu-id="e4c68-113">Docks the application in the remote session.</span></span> <span data-ttu-id="e4c68-114">Cette option est dépréciée et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="e4c68-114">This option has been deprecated and should not be used.</span></span>

</dd> <dt>

<span data-ttu-id="e4c68-115"><span id="RemoteSessionActionStartScreen"></span><span id="remotesessionactionstartscreen"></span><span id="REMOTESESSIONACTIONSTARTSCREEN"></span>**RemoteSessionActionStartScreen**</span><span class="sxs-lookup"><span data-stu-id="e4c68-115"><span id="RemoteSessionActionStartScreen"></span><span id="remotesessionactionstartscreen"></span><span id="REMOTESESSIONACTIONSTARTSCREEN"></span>**RemoteSessionActionStartScreen**</span></span>
</dt> <dd>

<span data-ttu-id="e4c68-116">Provoque l’affichage de l’écran de démarrage dans la session à distance.</span><span class="sxs-lookup"><span data-stu-id="e4c68-116">Causes the start screen to be displayed in the remote session.</span></span>

</dd> <dt>

<span data-ttu-id="e4c68-117"><span id="RemoteSessionActionAppSwitch"></span><span id="remotesessionactionappswitch"></span><span id="REMOTESESSIONACTIONAPPSWITCH"></span>**RemoteSessionActionAppSwitch**</span><span class="sxs-lookup"><span data-stu-id="e4c68-117"><span id="RemoteSessionActionAppSwitch"></span><span id="remotesessionactionappswitch"></span><span id="REMOTESESSIONACTIONAPPSWITCH"></span>**RemoteSessionActionAppSwitch**</span></span>
</dt> <dd>

<span data-ttu-id="e4c68-118">Provoque l’affichage de la fenêtre de changement d’application dans la session à distance.</span><span class="sxs-lookup"><span data-stu-id="e4c68-118">Causes the application switch window to be displayed in the remote session.</span></span> <span data-ttu-id="e4c68-119">C’est le même que l’utilisateur qui appuie sur Alt + Tab.</span><span class="sxs-lookup"><span data-stu-id="e4c68-119">This is the same as the user pressing Alt+Tab.</span></span>

</dd> <dt>

<span data-ttu-id="e4c68-120"><span id="RemoteSessionActionActionCenter"></span><span id="remotesessionactionactioncenter"></span><span id="REMOTESESSIONACTIONACTIONCENTER"></span>**RemoteSessionActionActionCenter**</span><span class="sxs-lookup"><span data-stu-id="e4c68-120"><span id="RemoteSessionActionActionCenter"></span><span id="remotesessionactionactioncenter"></span><span id="REMOTESESSIONACTIONACTIONCENTER"></span>**RemoteSessionActionActionCenter**</span></span>
</dt> <dd>

<span data-ttu-id="e4c68-121">Entraîne l’affichage du centre de maintenance dans la session à distance.</span><span class="sxs-lookup"><span data-stu-id="e4c68-121">Causes the Action Center to be displayed in the remote session.</span></span> <span data-ttu-id="e4c68-122">C’est le même que l’utilisateur qui appuie sur Win + A.</span><span class="sxs-lookup"><span data-stu-id="e4c68-122">This is the same as the user pressing Win+A.</span></span>

<span data-ttu-id="e4c68-123">**Windows server 2012 R2, Windows 8.1, Windows server 2012 et Windows 8 :** Cette valeur n’est pas prise en charge avant Windows Server 2016 et Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e4c68-123">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012 and Windows 8:** This value is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4c68-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4c68-124">Requirements</span></span>



| <span data-ttu-id="e4c68-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4c68-125">Requirement</span></span> | <span data-ttu-id="e4c68-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4c68-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4c68-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4c68-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e4c68-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e4c68-128">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="e4c68-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4c68-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e4c68-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e4c68-130">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="e4c68-131">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e4c68-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="e4c68-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4c68-132"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4c68-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4c68-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4c68-134">**IMsRdpClient8::SendRemoteAction**</span><span class="sxs-lookup"><span data-stu-id="e4c68-134">**IMsRdpClient8::SendRemoteAction**</span></span>](imsrdpclient8-sendremoteaction.md)
</dt> </dl>

 

 





