---
description: Avertit un appbar que l’état d’affichage automatique ou de masquage automatique de la barre des tâches a changé&\# 8212 ; autrement dit, l’utilisateur a sélectionné ou désactivé la &\# 0034 ; Always on&\# 0034 ; ou &\# 0034 ; Masquer automatiquement&\# 0034 ; case à cocher dans la feuille de propriétés de la barre des tâches.
title: Message ABN_STATECHANGE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ac2c00a2-ac20-40a5-947e-6b75a2620a0b
api_name:
- ABN_STATECHANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 33879fcb5e9435e2245bc3d00a9fab75bf1cbdc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862134"
---
# <a name="abn_statechange-message"></a><span data-ttu-id="c4266-103">\_Message ABN STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="c4266-103">ABN\_STATECHANGE message</span></span>

<span data-ttu-id="c4266-104">Avertit un appbar que l’état d’affichage automatique ou de masquage automatique de la barre des tâches a changé. autrement dit, l’utilisateur a activé ou désactivé la case à cocher « toujours visible » ou « masquer automatiquement » dans la feuille de propriétés de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="c4266-104">Notifies an appbar that the taskbar's autohide or always-on-top state has changed that is, the user has selected or cleared the "Always on top" or "Auto hide" check box on the taskbar's property sheet.</span></span>


```C++
ABN_STATECHANGE 
```



## <a name="parameters"></a><span data-ttu-id="c4266-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4266-105">Parameters</span></span>

<span data-ttu-id="c4266-106">Ce message n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="c4266-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c4266-107">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4266-107">Return value</span></span>

<span data-ttu-id="c4266-108">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="c4266-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4266-109">Notes</span><span class="sxs-lookup"><span data-stu-id="c4266-109">Remarks</span></span>

<span data-ttu-id="c4266-110">Un appbar peut utiliser ce message de notification pour définir son état sur conforme à celui de la barre des tâches, si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="c4266-110">An appbar can use this notification message to set its state to conform to that of the taskbar, if desired.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4266-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c4266-111">Requirements</span></span>



| <span data-ttu-id="c4266-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4266-112">Requirement</span></span> | <span data-ttu-id="c4266-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4266-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4266-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4266-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c4266-115">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4266-115">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c4266-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4266-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c4266-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4266-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c4266-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4266-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4266-119"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4266-119"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




