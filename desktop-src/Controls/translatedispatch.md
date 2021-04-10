---
title: TranslateDispatch fonction de rappel
description: Utilisé par le client de la fonction DoReaderMode pour intercepter et gérer explicitement tous les messages Windows ciblés pour la zone de défilement de la fenêtre du mode lecteur. Il s’agit d’une fonction de rappel définie par l’application.
ms.assetid: a50cff4f-ae10-4c3c-a386-9ec7c7d6256f
keywords:
- Contrôles Windows de fonction de rappel TranslateDispatch
topic_type:
- apiref
api_name:
- TranslateDispatch
- PFNREADERTRANSLATEDISPATCH
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1230ed1e65f8d739f9a0a05e4788eb919c45c4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942017"
---
# <a name="translatedispatch-callback-function"></a><span data-ttu-id="85a13-105">TranslateDispatch fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="85a13-105">TranslateDispatch callback function</span></span>

<span data-ttu-id="85a13-106">\[*TranslateDispatch* peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="85a13-106">\[*TranslateDispatch* is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="85a13-107">Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="85a13-107">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="85a13-108">Utilisé par le client de la fonction [**DoReaderMode**](doreadermode.md) pour intercepter et gérer explicitement tous les messages Windows ciblés pour la zone de défilement de la fenêtre du mode lecteur.</span><span class="sxs-lookup"><span data-stu-id="85a13-108">Used by the client of the [**DoReaderMode**](doreadermode.md) function to intercept and explicitly handle any windows messages targeted for the scrolling area of the reader mode window.</span></span> <span data-ttu-id="85a13-109">Il s’agit d’une fonction de rappel définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="85a13-109">This is an application-defined callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="85a13-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85a13-110">Syntax</span></span>


```C++
BOOL CALLBACK TranslateDispatch(
  _In_ const MSG *lpmsg
);
```



## <a name="parameters"></a><span data-ttu-id="85a13-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85a13-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85a13-112">*lpmsg* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="85a13-112">*lpmsg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85a13-113">Type : \**const [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) \** _</span><span class="sxs-lookup"><span data-stu-id="85a13-113">Type: \**const [**MSG**](/windows/win32/api/winuser/ns-winuser-msg)\** _</span></span>

<span data-ttu-id="85a13-114">Pointeur vers une structure [_ *MSG* \*](/windows/win32/api/winuser/ns-winuser-msg) qui contient le message intercepté.</span><span class="sxs-lookup"><span data-stu-id="85a13-114">A pointer to an [_ *MSG*\*](/windows/win32/api/winuser/ns-winuser-msg) structure that contains the intercepted message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85a13-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="85a13-115">Return value</span></span>

<span data-ttu-id="85a13-116">Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="85a13-116">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="85a13-117">**True** si le message a été géré par cette fonction. Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="85a13-117">**TRUE** if the message was handled by this function; otherwise, **FALSE**.</span></span> <span data-ttu-id="85a13-118">Si la **valeur est false**, le message est géré par l’implémentation du mode lecteur par défaut.</span><span class="sxs-lookup"><span data-stu-id="85a13-118">If **FALSE**, the message is handled by the default reader mode implementation.</span></span> <span data-ttu-id="85a13-119">Cette implémentation gère le déplacement et les boutons de la souris, ainsi que les pressions sur les touches.</span><span class="sxs-lookup"><span data-stu-id="85a13-119">That implementation handles mouse movement and buttons as well as key presses.</span></span>

## <a name="examples"></a><span data-ttu-id="85a13-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="85a13-120">Examples</span></span>

<span data-ttu-id="85a13-121">L’exemple suivant présente une implémentation de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="85a13-121">The following example outlines an implementation of this function.</span></span>


```C++
BOOL CALLBACK
TranslateDispatchCallback(LPMSG lpmsg)
{
    BOOL fResult = FALSE;

    if (lpmsg->message == WM_KEYDOWN)
    {
        
        // Perform custom keyboard actions here.
        fResult = TRUE;
    }

    return fResult;
}
```



## <a name="requirements"></a><span data-ttu-id="85a13-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85a13-122">Requirements</span></span>



| <span data-ttu-id="85a13-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85a13-123">Requirement</span></span> | <span data-ttu-id="85a13-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="85a13-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="85a13-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85a13-125">Minimum supported client</span></span><br/> | <span data-ttu-id="85a13-126">Windows Vista, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85a13-126">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="85a13-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85a13-127">Minimum supported server</span></span><br/> | <span data-ttu-id="85a13-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85a13-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>          |



 

