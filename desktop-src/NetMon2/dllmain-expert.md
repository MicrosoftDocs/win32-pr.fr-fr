---
description: L’expert implémente la fonction DllMain. Le système d’exploitation appelle DllMain pour obtenir un descripteur d’une instance de l’expert.
ms.assetid: 38593ba0-dc37-4620-bb49-2e50c3d9ea3c
title: Fonction de rappel d’expert DllMain (Process. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 914f50b75e83fdc67448770b32ac8d0f8e8ab656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866270"
---
# <a name="dllmain-expert-callback-function"></a><span data-ttu-id="53d5b-104">Fonction de rappel d’expert DllMain</span><span class="sxs-lookup"><span data-stu-id="53d5b-104">DllMain Expert callback function</span></span>

<span data-ttu-id="53d5b-105">L’expert implémente la fonction [**DllMain**](/windows/desktop/Dlls/dllmain) .</span><span class="sxs-lookup"><span data-stu-id="53d5b-105">The expert implements the [**DllMain**](/windows/desktop/Dlls/dllmain) function.</span></span> <span data-ttu-id="53d5b-106">Le système d’exploitation appelle **DllMain** pour obtenir un descripteur d’une instance de l’expert.</span><span class="sxs-lookup"><span data-stu-id="53d5b-106">The operating system calls **DllMain** to obtain a handle to an instance of the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="53d5b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53d5b-107">Syntax</span></span>


```C++
BOOL WINAPI DllMain(
  _Out_ HINSTANCE hInstance,
  _In_  ULONG     ulReason,
        LPVOID    Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="53d5b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53d5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53d5b-109">*HINSTANCE* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="53d5b-109">*hInstance* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53d5b-110">Handle vers une instance de l’expert.</span><span class="sxs-lookup"><span data-stu-id="53d5b-110">Handle to an instance of the expert.</span></span>

<span data-ttu-id="53d5b-111">Si l’expert utilise l’interface utilisateur Moniteur réseau, la valeur *HINSTANCE* doit être stockée dans une variable globale.</span><span class="sxs-lookup"><span data-stu-id="53d5b-111">If the expert uses the Network Monitor user interface, the *hInstance* value must be stored in a global variable.</span></span> <span data-ttu-id="53d5b-112">Cette approche est nécessaire uniquement lorsque la valeur du paramètre *ulReason* est définie sur dll \_ process \_ Attach.</span><span class="sxs-lookup"><span data-stu-id="53d5b-112">This approach is necessary only when the value of the *ulReason* parameter is set to DLL\_PROCESS\_ATTACH.</span></span>

</dd> <dt>

<span data-ttu-id="53d5b-113">*ulReason* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="53d5b-113">*ulReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53d5b-114">Indicateur de la raison pour laquelle la fonction a été appelée.</span><span class="sxs-lookup"><span data-stu-id="53d5b-114">Indicator of why the function was called.</span></span> <span data-ttu-id="53d5b-115">La valeur d' \_ attachement du processus dll \_ (qui s’applique lorsque la dll est chargée pour la première fois) indique que l’expert doit enregistrer la valeur *HINSTANCE* dans une variable globale.</span><span class="sxs-lookup"><span data-stu-id="53d5b-115">A value of DLL\_PROCESS\_ATTACH, (which applies when the DLL is first loaded) indicates that the expert should save the *hInstance* value in a global variable.</span></span>

<span data-ttu-id="53d5b-116">Avec toute autre valeur, tous les appels à la fonction [**DllMain**](/windows/desktop/Dlls/dllmain) peuvent être ignorés.</span><span class="sxs-lookup"><span data-stu-id="53d5b-116">With any other value, all calls to the [**DllMain**](/windows/desktop/Dlls/dllmain) function can be ignored.</span></span> <span data-ttu-id="53d5b-117">Pour obtenir la liste de tous les indicateurs possibles définis par le système d’exploitation, consultez **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="53d5b-117">For a list of all possible flags set by the operating system, see **DLLMain**.</span></span>

</dd> <dt>

<span data-ttu-id="53d5b-118">*Reserved*</span><span class="sxs-lookup"><span data-stu-id="53d5b-118">*Reserved*</span></span> 
</dt> <dd>

<span data-ttu-id="53d5b-119">Le paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="53d5b-119">Parameter is not in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53d5b-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="53d5b-120">Return value</span></span>

<span data-ttu-id="53d5b-121">Si la fonction réussit, la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="53d5b-121">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="53d5b-122">Si la fonction échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="53d5b-122">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="53d5b-123">Notes</span><span class="sxs-lookup"><span data-stu-id="53d5b-123">Remarks</span></span>

<span data-ttu-id="53d5b-124">Le système d’exploitation appelle la fonction d’expert **DllMain** lorsqu’un processus charge ou décharge la dll d’expert.</span><span class="sxs-lookup"><span data-stu-id="53d5b-124">The operating system calls the **DllMain** expert function when a process loads or unloads the expert DLL.</span></span> <span data-ttu-id="53d5b-125">La fonction d’expert **DllMain** doit être exportée uniquement si l’expert dispose d’une interface utilisateur pour l’affichage de la configuration ou des résultats, puis uniquement pour retourner la valeur *HINSTANCE* appropriée.</span><span class="sxs-lookup"><span data-stu-id="53d5b-125">The **DllMain** expert function must be exported only if the expert has a user interface for viewing either configuration or results, and then only to return the proper *hInstance* value.</span></span>

<span data-ttu-id="53d5b-126">La fonction d’expert **DllMain** est basée sur la fonction [**DllMain**](/windows/desktop/Dlls/dllmain) de la bibliothèque de liens dynamiques.</span><span class="sxs-lookup"><span data-stu-id="53d5b-126">The **DllMain** expert function is based on the dynamic link library [**DllMain**](/windows/desktop/Dlls/dllmain) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="53d5b-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53d5b-127">Requirements</span></span>



| <span data-ttu-id="53d5b-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53d5b-128">Requirement</span></span> | <span data-ttu-id="53d5b-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="53d5b-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="53d5b-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53d5b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="53d5b-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53d5b-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="53d5b-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53d5b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="53d5b-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53d5b-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="53d5b-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="53d5b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="53d5b-135"><dt>Process. h</dt></span><span class="sxs-lookup"><span data-stu-id="53d5b-135"><dt>Process.h</dt></span></span> </dl> |



 

