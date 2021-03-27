---
description: Inscrit un nouveau appbar et spécifie l’identificateur de message que le système doit utiliser pour envoyer des messages de notification. Un appbar doit envoyer ce message avant d’envoyer d’autres messages appbar.
ms.assetid: 1da9db13-6fdc-44b3-9985-de32d572675a
title: Message ABM_NEW (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fad11e6712d0afd0c1a5e9de07fd3d690800db13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750309"
---
# <a name="abm_new-message"></a><span data-ttu-id="dd0f3-104">ABM \_ un nouveau message</span><span class="sxs-lookup"><span data-stu-id="dd0f3-104">ABM\_NEW message</span></span>

<span data-ttu-id="dd0f3-105">Inscrit un nouveau appbar et spécifie l’identificateur de message que le système doit utiliser pour envoyer des messages de notification.</span><span class="sxs-lookup"><span data-stu-id="dd0f3-105">Registers a new appbar and specifies the message identifier that the system should use to send it notification messages.</span></span> <span data-ttu-id="dd0f3-106">Un appbar doit envoyer ce message avant d’envoyer d’autres messages appbar.</span><span class="sxs-lookup"><span data-stu-id="dd0f3-106">An appbar should send this message before sending any other appbar messages.</span></span>


```C++
fRegistered = (BOOL) SHAppBarMessage(ABM_NEW, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="dd0f3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd0f3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd0f3-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="dd0f3-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="dd0f3-109">Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) qui contient le handle de fenêtre et l’identificateur de message du nouvel appbar.</span><span class="sxs-lookup"><span data-stu-id="dd0f3-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that contains the new appbar's window handle and message identifier.</span></span> <span data-ttu-id="dd0f3-110">Vous devez spécifier les membres **cbSize**, **HWND** et **uCallbackMessage** lors de l’envoi de ce message. tous les autres membres sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="dd0f3-110">You must specify the **cbSize**, **hWnd**, and **uCallbackMessage** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd0f3-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd0f3-111">Return value</span></span>

<span data-ttu-id="dd0f3-112">Retourne la **valeur true** en cas de réussite, ou **false** si une erreur se produit ou si le appbar est déjà inscrit.</span><span class="sxs-lookup"><span data-stu-id="dd0f3-112">Returns **TRUE** if successful, or **FALSE** if an error occurs or if the appbar is already registered.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd0f3-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dd0f3-113">Requirements</span></span>



| <span data-ttu-id="dd0f3-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd0f3-114">Requirement</span></span> | <span data-ttu-id="dd0f3-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd0f3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd0f3-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd0f3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dd0f3-117">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd0f3-117">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dd0f3-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd0f3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dd0f3-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd0f3-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd0f3-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd0f3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd0f3-121"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd0f3-121"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




