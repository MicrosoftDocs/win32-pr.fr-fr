---
UID: ''
title: GetMsgProc fonction de rappel
description: Le système appelle cette fonction lorsqu’une fonction de message reçoit un message à partir d’une file d’attente de messages d’application.
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: aa055e4184cdc9be5bb60a421ad5937bbfd15393
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/05/2021
ms.locfileid: "106516535"
---
# <a name="getmsgproc-function"></a><span data-ttu-id="be447-103">GetMsgProc fonction)</span><span class="sxs-lookup"><span data-stu-id="be447-103">GetMsgProc function</span></span>

## <a name="-description"></a><span data-ttu-id="be447-104">-Description</span><span class="sxs-lookup"><span data-stu-id="be447-104">-description</span></span>

<span data-ttu-id="be447-105">Fonction de rappel définie par l’application ou définie par la Bibliothèque utilisée avec la fonction [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="be447-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span> <span data-ttu-id="be447-106">Le système appelle cette fonction chaque fois que la fonction [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) a récupéré un message à partir d’une file d’attente de messages d’application.</span><span class="sxs-lookup"><span data-stu-id="be447-106">The system calls this function whenever the [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function has retrieved a message from an application message queue.</span></span>
<span data-ttu-id="be447-107">Avant de retourner le message récupéré à l’appelant, le système transmet le message à la procédure de Hook.</span><span class="sxs-lookup"><span data-stu-id="be447-107">Before returning the retrieved message to the caller, the system passes the message to the hook procedure.</span></span>

<span data-ttu-id="be447-108">Le type **HOOKPROC** définit un pointeur vers cette fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="be447-108">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="be447-109">**GetMsgProc** est un espace réservé pour le nom de la fonction définie par l’application ou par la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="be447-109">**GetMsgProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK GetMsgProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="-parameters"></a><span data-ttu-id="be447-110">-paramètres</span><span class="sxs-lookup"><span data-stu-id="be447-110">-parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="be447-111">Code [in]</span><span class="sxs-lookup"><span data-stu-id="be447-111">code [in]</span></span>

<span data-ttu-id="be447-112">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="be447-112">Type: **int**</span></span>

<span data-ttu-id="be447-113">Spécifie si la procédure de raccordement doit traiter le message.</span><span class="sxs-lookup"><span data-stu-id="be447-113">Specifies whether the hook procedure must process the message.</span></span>
<span data-ttu-id="be447-114">Si le *code* est **HC_ACTION**, la procédure de raccordement doit traiter le message.</span><span class="sxs-lookup"><span data-stu-id="be447-114">If *code* is **HC_ACTION**, the hook procedure must process the message.</span></span>
<span data-ttu-id="be447-115">Si le *code* est inférieur à zéro, la procédure de raccordement doit passer le message à la fonction [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sans traitement supplémentaire et doit retourner la valeur retournée par **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="be447-115">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>

### <a name="wparam-in"></a><span data-ttu-id="be447-116">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="be447-116">wParam [in]</span></span>

<span data-ttu-id="be447-117">Type : **wParam**</span><span class="sxs-lookup"><span data-stu-id="be447-117">Type: **WPARAM**</span></span>

<span data-ttu-id="be447-118">Spécifie si le message a été supprimé de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="be447-118">Specifies whether the message has been removed from the queue.</span></span>
<span data-ttu-id="be447-119">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="be447-119">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="be447-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="be447-120">Value</span></span> | <span data-ttu-id="be447-121">Signification</span><span class="sxs-lookup"><span data-stu-id="be447-121">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="be447-122">**PM_NOREMOVE** 0x0000</span><span class="sxs-lookup"><span data-stu-id="be447-122">**PM_NOREMOVE** 0x0000</span></span> | <span data-ttu-id="be447-123">Le message n’a pas été supprimé de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="be447-123">The message has not been removed from the queue.</span></span> <span data-ttu-id="be447-124">(Une application appelée fonction **PeekMessage** , en spécifiant l’indicateur **PM_NOREMOVE** .)</span><span class="sxs-lookup"><span data-stu-id="be447-124">(An application called the **PeekMessage** function, specifying the **PM_NOREMOVE** flag.)</span></span> |
| <span data-ttu-id="be447-125">**PM_REMOVE** 0x0001</span><span class="sxs-lookup"><span data-stu-id="be447-125">**PM_REMOVE** 0x0001</span></span> | <span data-ttu-id="be447-126">Le message a été supprimé de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="be447-126">The message has been removed from the queue.</span></span> <span data-ttu-id="be447-127">(Une application appelée **GetMessage** ou appelée fonction  **PeekMessage** , en spécifiant l’indicateur **PM_REMOVE** .)</span><span class="sxs-lookup"><span data-stu-id="be447-127">(An application called **GetMessage**, or it called the  **PeekMessage** function, specifying the **PM_REMOVE** flag.)</span></span>|

### <a name="lparam-in"></a><span data-ttu-id="be447-128">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="be447-128">lParam [in]</span></span>

<span data-ttu-id="be447-129">Type : **lParam**</span><span class="sxs-lookup"><span data-stu-id="be447-129">Type: **LPARAM**</span></span>

<span data-ttu-id="be447-130">Pointeur vers une structure [MSG](/windows/desktop/api/winuser/ns-winuser-msg) qui contient des détails sur le message.</span><span class="sxs-lookup"><span data-stu-id="be447-130">A pointer to an [MSG](/windows/desktop/api/winuser/ns-winuser-msg) structure that contains details about the message.</span></span>

## <a name="-returns"></a><span data-ttu-id="be447-131">-retourne</span><span class="sxs-lookup"><span data-stu-id="be447-131">-returns</span></span>

<span data-ttu-id="be447-132">Si le *code* est inférieur à zéro, la procédure de raccordement doit retourner la valeur retournée par [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex).</span><span class="sxs-lookup"><span data-stu-id="be447-132">If *code* is less than zero, the hook procedure must return the value returned by [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex).</span></span>

<span data-ttu-id="be447-133">Si le *code* est supérieur ou égal à zéro, il est fortement recommandé d’appeler **CallNextHookEx** et de retourner la valeur qu’il retourne ; dans le cas contraire, les autres applications qui ont installé [WH_GETMESSAGE](about-hooks.md) hooks ne recevront pas de notifications de raccordement et pourront se comporter de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="be447-133">If *code* is greater than or equal to zero, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_GETMESSAGE](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="be447-134">Si la procédure de hook n’appelle pas **CallNextHookEx**, la valeur de retour doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="be447-134">If the hook procedure does not call **CallNextHookEx**, the return value should be zero.</span></span>

## <a name="-remarks"></a><span data-ttu-id="be447-135">-Remarques</span><span class="sxs-lookup"><span data-stu-id="be447-135">-remarks</span></span>

<span data-ttu-id="be447-136">La procédure de hook **GetMsgProc** peut examiner ou modifier le message.</span><span class="sxs-lookup"><span data-stu-id="be447-136">The **GetMsgProc** hook procedure can examine or modify the message.</span></span>
<span data-ttu-id="be447-137">Une fois que la procédure de Hook a retourné le contrôle au système, la fonction **GetMessage** ou **PeekMessage** retourne le message, ainsi que toutes les modifications, à l’application qui l’a appelée à l’origine.</span><span class="sxs-lookup"><span data-stu-id="be447-137">After the hook procedure returns control to the system, the **GetMessage** or **PeekMessage** function returns the message, along with any modifications, to the application that originally called it.</span></span>

<span data-ttu-id="be447-138">Une application installe cette procédure de hook en spécifiant le type de hook **WH_GETMESSAGE** et un pointeur vers la procédure de Hook dans un appel à la fonction **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="be447-138">An application installs this hook procedure by specifying the **WH_GETMESSAGE** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

## <a name="see-also"></a><span data-ttu-id="be447-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be447-139">See also</span></span>

[<span data-ttu-id="be447-140">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="be447-140">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="be447-141">GetMessage</span><span class="sxs-lookup"><span data-stu-id="be447-141">GetMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-getmessage)

[<span data-ttu-id="be447-142">FRAGMENT</span><span class="sxs-lookup"><span data-stu-id="be447-142">MSG</span></span>](/windows/desktop/api/winuser/ns-winuser-msg)

[<span data-ttu-id="be447-143">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="be447-143">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="be447-144">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="be447-144">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="be447-145">Hooks</span><span class="sxs-lookup"><span data-stu-id="be447-145">Hooks</span></span>](hooks.md)
