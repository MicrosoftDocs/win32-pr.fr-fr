---
description: Les fonctions de prototype du gestionnaire d’événements sont utilisées pour toutes les fonctions qui gèrent les événements de notification Winlogon.
ms.assetid: 99b91e80-5e4e-4119-89aa-c0a80fce69e3
title: Fonction de rappel de prototype de fonction du gestionnaire d’événements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event_Handler_Function_Name
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 935ddac5660c814b898be17218d879678f2135ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521354"
---
# <a name="event-handler-function-prototype-callback-function"></a><span data-ttu-id="b8fa4-103">Fonction de rappel de prototype de fonction du gestionnaire d’événements</span><span class="sxs-lookup"><span data-stu-id="b8fa4-103">Event Handler Function Prototype callback function</span></span>

<span data-ttu-id="b8fa4-104">\[Les fonctions de prototype du gestionnaire d’événements ne sont plus disponibles pour une utilisation à partir de Windows Server 2008 et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b8fa4-104">\[Event Handler Prototype functions are no longer available for use as of Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="b8fa4-105">\]</span><span class="sxs-lookup"><span data-stu-id="b8fa4-105">\]</span></span>

<span data-ttu-id="b8fa4-106">Les fonctions de prototype du gestionnaire d’événements sont utilisées pour toutes les fonctions qui gèrent les événements de notification [*Winlogon*](/windows/desktop/SecGloss/w-gly) .</span><span class="sxs-lookup"><span data-stu-id="b8fa4-106">Event Handler Prototype functions are used for all functions that handle [*Winlogon*](/windows/desktop/SecGloss/w-gly) notification events.</span></span> <span data-ttu-id="b8fa4-107">Le nom de la fonction, représenté ci-dessous par le nom de la fonction du gestionnaire d’événements de l’espace réservé, reflète généralement le nom de l’événement géré par la fonction. *\_ \_ \_*</span><span class="sxs-lookup"><span data-stu-id="b8fa4-107">The name of the function, represented below by the place holder *Event\_Handler\_Function\_Name*, typically reflects the name of the event that the function handles.</span></span> <span data-ttu-id="b8fa4-108">Par exemple, la fonction qui gère les événements d’ouverture de session peut être nommée : **WLEventLogon**.</span><span class="sxs-lookup"><span data-stu-id="b8fa4-108">For example, the function that handles logon events might be named: **WLEventLogon**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8fa4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8fa4-109">Syntax</span></span>


```C++
void Event_Handler_Function_Name(
  _In_ PWLX_NOTIFICATION_INFO pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="b8fa4-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8fa4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8fa4-111">*pinfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8fa4-111">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8fa4-112">Pointeur vers une structure [**d' \_ \_ informations de notification wlx**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) qui contient les détails de l’événement.</span><span class="sxs-lookup"><span data-stu-id="b8fa4-112">A pointer to a [**WLX\_NOTIFICATION\_INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) structure that contains the details of the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8fa4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b8fa4-113">Return value</span></span>

<span data-ttu-id="b8fa4-114">Cette fonction de rappel ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b8fa4-114">This callback function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8fa4-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b8fa4-115">Remarks</span></span>

<span data-ttu-id="b8fa4-116">Si votre gestionnaire d’événements doit créer des processus enfants, il doit appeler la fonction [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) .</span><span class="sxs-lookup"><span data-stu-id="b8fa4-116">If your event handler needs to create child processes, it should call the [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="b8fa4-117">Dans le cas contraire, le nouveau processus sera créé sur le bureau Winlogon, et non sur le Bureau de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b8fa4-117">Otherwise, the new process will be created on the Winlogon desktop, not the user's desktop.</span></span>

## <a name="examples"></a><span data-ttu-id="b8fa4-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="b8fa4-118">Examples</span></span>

<span data-ttu-id="b8fa4-119">L’exemple suivant montre comment implémenter des gestionnaires d’événements pour les événements Winlogon.</span><span class="sxs-lookup"><span data-stu-id="b8fa4-119">The following sample shows how to implement event handlers for Winlogon events.</span></span> <span data-ttu-id="b8fa4-120">Par souci de simplicité, seules les implémentations des gestionnaires d’événements Logon et Logoff sont affichées.</span><span class="sxs-lookup"><span data-stu-id="b8fa4-120">For simplicity, only the implementations of the Logon and Logoff event handlers are shown.</span></span> <span data-ttu-id="b8fa4-121">Vous pouvez implémenter des gestionnaires pour le reste des événements exactement de la même manière.</span><span class="sxs-lookup"><span data-stu-id="b8fa4-121">You can implement handlers for the rest of the events in exactly the same manner.</span></span>


```C++
// Copyright (C) Microsoft. All rights reserved. 
#include <windows.h>

// Here is the entrance function for the DLL.
BOOL WINAPI LibMain(HINSTANCE hInstance, DWORD dwReason, LPVOID lpReserved)
{
    switch (dwReason)
    {
        case DLL_PROCESS_ATTACH:
            {

             // Disable DLL_THREAD_ATTACH & DLL_THREAD_DETACH
             // notification calls. This is a performance optimization
             // for multithreaded applications that do not need 
             // thread-level notifications of attachment or
             // detachment.

            DisableThreadLibraryCalls (hInstance);
            }
            break;
    }

    return TRUE;
}

// Here is the event handler for the Winlogon Logon event.
void WLEventLogon (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogon.\r\n"));
}

// Here is the event handler for the Winlogon Logoff event.
void WLEventLogoff (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogff.\r\n"));
}
```



## <a name="requirements"></a><span data-ttu-id="b8fa4-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8fa4-122">Requirements</span></span>



| <span data-ttu-id="b8fa4-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8fa4-123">Requirement</span></span> | <span data-ttu-id="b8fa4-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8fa4-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b8fa4-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8fa4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b8fa4-126">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8fa4-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b8fa4-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8fa4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b8fa4-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8fa4-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b8fa4-129">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b8fa4-129">End of client support</span></span><br/>    | <span data-ttu-id="b8fa4-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b8fa4-130">Windows XP</span></span><br/>                                |
| <span data-ttu-id="b8fa4-131">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="b8fa4-131">End of server support</span></span><br/>    | <span data-ttu-id="b8fa4-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b8fa4-132">Windows Server 2003</span></span><br/>                       |



 

