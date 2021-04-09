---
description: L’expert doit implémenter la fonction Run. Moniteur réseau appelle la fonction Run pour démarrer l’expert au sein de la DLL de l’expert.
ms.assetid: 9ef3941b-d9e9-4acb-97ed-5f39573f2946
title: Exécuter une fonction de rappel (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Run
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: c2dff2cf70a6d989928f17447fa3491dd9509f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862898"
---
# <a name="run-callback-function"></a><span data-ttu-id="3cd09-104">Exécuter une fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="3cd09-104">Run callback function</span></span>

<span data-ttu-id="3cd09-105">L’expert doit implémenter la fonction **Run** .</span><span class="sxs-lookup"><span data-stu-id="3cd09-105">The expert must implement the **Run** function.</span></span> <span data-ttu-id="3cd09-106">Moniteur réseau appelle la fonction **Run** pour démarrer l’expert au sein de la dll de l’expert.</span><span class="sxs-lookup"><span data-stu-id="3cd09-106">Network Monitor calls the **Run** function to start the expert within the expert DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cd09-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cd09-107">Syntax</span></span>


```C++
BOOL WINAPI Run(
  _In_ HEXPERTKEY         hExpertKey,
  _In_ PEXPERTCONFIG      pConfig,
  _In_ PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_ DWORD              StartupFlags,
  _In_ HWND               hWndParent
);
```



## <a name="parameters"></a><span data-ttu-id="3cd09-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3cd09-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cd09-109">*hExpertKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3cd09-109">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cd09-110">Identificateur unique de l’expert qui est passé à toutes les fonctions Moniteur réseau spécifiques à l’expert.</span><span class="sxs-lookup"><span data-stu-id="3cd09-110">Unique identifier of the expert that is passed back to all expert-specific Network Monitor functions.</span></span>

> [!Note]  
> <span data-ttu-id="3cd09-111">L’identificateur *hExpertKey* peut passer une clé d’expert qui est différente de la clé d’expert que la fonction de [**configuration**](configure.md) passe.</span><span class="sxs-lookup"><span data-stu-id="3cd09-111">The *hExpertKey* identifier may pass an expert key that is different from the expert key that the [**Configure**](configure.md) function passes.</span></span>

 

</dd> <dt>

<span data-ttu-id="3cd09-112">*pConfig* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3cd09-112">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cd09-113">Pointeur vers la configuration existante.</span><span class="sxs-lookup"><span data-stu-id="3cd09-113">Pointer to the existing configuration.</span></span> <span data-ttu-id="3cd09-114">Le paramètre *pConfig* peut avoir la **valeur null** , ce qui signifie que l’expert peut s’exécuter avec des valeurs par défaut codées en dur, ou des informations de démarrage auxquelles le paramètre *pExpertStartupInfo* fait référence.</span><span class="sxs-lookup"><span data-stu-id="3cd09-114">The *pConfig* parameter may be **NULL** which means that the expert can run with hard-coded defaults, or startup information that the *pExpertStartupInfo* parameter references.</span></span>

</dd> <dt>

<span data-ttu-id="3cd09-115">*pExpertStartupInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3cd09-115">*pExpertStartupInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cd09-116">Pointeur vers l’élément de capture qui a le focus au démarrage de l’expert.</span><span class="sxs-lookup"><span data-stu-id="3cd09-116">Pointer to the capture element that has focus when the expert starts.</span></span>

</dd> <dt>

<span data-ttu-id="3cd09-117">*StartupFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3cd09-117">*StartupFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cd09-118">Indicateur de la façon dont l’expert doit utiliser le paramètre *pExpertStartupInfo* .</span><span class="sxs-lookup"><span data-stu-id="3cd09-118">Indicator for how the expert should use the *pExpertStartupInfo* parameter.</span></span>

<span data-ttu-id="3cd09-119">Le seul indicateur défini est :</span><span class="sxs-lookup"><span data-stu-id="3cd09-119">The only flag defined is:</span></span>



| <span data-ttu-id="3cd09-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="3cd09-120">Value</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="3cd09-121">Signification</span><span class="sxs-lookup"><span data-stu-id="3cd09-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EXPERT_STARTUP_FLAG_USE_STARTUP_DATA_OVER_CONFIG_DATA."></span><span id="expert_startup_flag_use_startup_data_over_config_data."></span><dl> <span data-ttu-id="3cd09-122"><dt>**l' \_ indicateur de démarrage expert \_ utilise les données de \_ \_ démarrage sur les données de \_ \_ \_ configuration \_ .**</dt></span><span class="sxs-lookup"><span data-stu-id="3cd09-122"><dt>**EXPERT\_STARTUP\_FLAG\_USE\_STARTUP\_DATA\_OVER\_CONFIG\_DATA.**</dt></span></span> </dl> | <span data-ttu-id="3cd09-123">Cet indicateur indique que l’expert utilise le paramètre *pExpertStartupInfo* et n’utilise pas le paramètre *pConfig* .</span><span class="sxs-lookup"><span data-stu-id="3cd09-123">This flag indicates that the expert uses the *pExpertStartupInfo* parameter, and does not use the *pConfig* parameter.</span></span> <span data-ttu-id="3cd09-124">En règle générale, vous pouvez définir cet indicateur lorsque l’expert peut démarrer à partir d’un clic avec la souris.</span><span class="sxs-lookup"><span data-stu-id="3cd09-124">Typically, you can set this flag when the expert can start from a right-mouse click.</span></span> <span data-ttu-id="3cd09-125">Si l’indicateur n’est pas défini, les deux éléments suivants peuvent se produire : l’expert ne démarre pas à partir d’un clic droit, ou l’expert commence à partir d’un clic avec la souris, puis l’utilisateur le configure.</span><span class="sxs-lookup"><span data-stu-id="3cd09-125">If the flag is not set, the following two things can occur: either the expert does not start from a right-mouse click, or the expert starts from a right-mouse click, and then the user configures it.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3cd09-126">*hwndParent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3cd09-126">*hWndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cd09-127">Le paramètre *HWND* du parent (généralement l’interface utilisateur Moniteur réseau).</span><span class="sxs-lookup"><span data-stu-id="3cd09-127">The *hWnd* parameter of the parent (usually the Network Monitor user interface).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cd09-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3cd09-128">Return value</span></span>

<span data-ttu-id="3cd09-129">Si la fonction réussit (autrement dit, si l’expert démarre), la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="3cd09-129">If the function is successful (that is, if the expert starts), the return value is **TRUE**.</span></span>

<span data-ttu-id="3cd09-130">Si la fonction échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="3cd09-130">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cd09-131">Notes</span><span class="sxs-lookup"><span data-stu-id="3cd09-131">Remarks</span></span>

<span data-ttu-id="3cd09-132">Lors de son exécution, l’expert parcourt les frames du fichier de capture et génère un rapport ou crée des événements qui présentent des problèmes.</span><span class="sxs-lookup"><span data-stu-id="3cd09-132">When running, the expert loops through the frames in the capture file and either generates a report or creates events that show problems.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cd09-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3cd09-133">Requirements</span></span>



| <span data-ttu-id="3cd09-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3cd09-134">Requirement</span></span> | <span data-ttu-id="3cd09-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="3cd09-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3cd09-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3cd09-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3cd09-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3cd09-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3cd09-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3cd09-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3cd09-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3cd09-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3cd09-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="3cd09-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cd09-141"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cd09-141"><dt>Netmon.h</dt></span></span> </dl> |



 

 




