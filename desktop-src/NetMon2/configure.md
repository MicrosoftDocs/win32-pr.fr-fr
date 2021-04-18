---
description: Configure l’expert au sein de la DLL de l’expert.
ms.assetid: 3906569d-9ad4-4c03-9637-f4a57697b227
title: Configurer la fonction de rappel (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Configure
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 76ba55b7544e35a07b74a41788a3befa766f87bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106542938"
---
# <a name="configure-callback-function"></a><span data-ttu-id="7587f-103">Configurer la fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="7587f-103">Configure callback function</span></span>

<span data-ttu-id="7587f-104">La fonction de **configuration** configure l’expert au sein de la dll de l’expert.</span><span class="sxs-lookup"><span data-stu-id="7587f-104">The **Configure** function configures the expert within the expert DLL.</span></span>

<span data-ttu-id="7587f-105">L’expert doit implémenter la fonction de **configuration** .</span><span class="sxs-lookup"><span data-stu-id="7587f-105">The expert must implement the **Configure** function.</span></span> <span data-ttu-id="7587f-106">Lors de la réception de l’appel de fonction, l’expert affiche une boîte de dialogue qui permet à l’utilisateur de modifier un élément configurable.</span><span class="sxs-lookup"><span data-stu-id="7587f-106">When the function call is received, the expert displays a dialog box that enables the user to change any configurable item.</span></span>

## <a name="syntax"></a><span data-ttu-id="7587f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7587f-107">Syntax</span></span>


```C++
BOOL WINAPI Configure(
  _In_    HEXPERTKEY         hExpertKey,
  _Inout_ PEXPERTCONFIG      *ppConfig,
  _In_    PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_    DWORD              StartupFlags,
  _In_    HWND               hWnd
);
```



## <a name="parameters"></a><span data-ttu-id="7587f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7587f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7587f-109">*hExpertKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7587f-109">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7587f-110">Identificateur d’expert unique.</span><span class="sxs-lookup"><span data-stu-id="7587f-110">Unique expert identifier.</span></span>

<span data-ttu-id="7587f-111">L’identificateur unique est renvoyé sur toutes les fonctions de Moniteur réseau spécifiques à un expert.</span><span class="sxs-lookup"><span data-stu-id="7587f-111">The unique identifier is passed back on all expert-specific Network Monitor functions.</span></span> <span data-ttu-id="7587f-112">N’oubliez pas que l’identificateur peut ne pas être la même clé d’expert que celle transmise à la fonction d' [**exécution**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="7587f-112">Be aware that the identifier may not be the same expert key as the one passed to the [**Run**](run.md) function.</span></span> <span data-ttu-id="7587f-113">Ne stockez pas la clé d’expert à partir de l’appel de **configuration** .</span><span class="sxs-lookup"><span data-stu-id="7587f-113">Do not store the expert key from the **Configure** call.</span></span>

</dd> <dt>

<span data-ttu-id="7587f-114">*ppConfig* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7587f-114">*ppConfig* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7587f-115">Pointeur vers un pointeur vers une structure [**EXPERTCONFIG**](expertconfig.md) à l’entrée.</span><span class="sxs-lookup"><span data-stu-id="7587f-115">A pointer to a pointer to an [**EXPERTCONFIG**](expertconfig.md) structure upon entry.</span></span>

<span data-ttu-id="7587f-116">Après une sortie réussie, la structure [**EXPERTCONFIG**](expertconfig.md) référencée contient les nouvelles données de configuration.</span><span class="sxs-lookup"><span data-stu-id="7587f-116">After a successful exit, the referenced [**EXPERTCONFIG**](expertconfig.md) structure contains the new configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="7587f-117">*pExpertStartupInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7587f-117">*pExpertStartupInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7587f-118">Pointeur vers l’élément de capture ayant le focus au démarrage de l’expert.</span><span class="sxs-lookup"><span data-stu-id="7587f-118">A pointer to the capture element with focus when the expert started.</span></span>

</dd> <dt>

<span data-ttu-id="7587f-119">*StartupFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7587f-119">*StartupFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7587f-120">Indicateurs qui indiquent comment l’expert doit utiliser le paramètre *pExpertStartupInfo* .</span><span class="sxs-lookup"><span data-stu-id="7587f-120">The flags that indicate how the expert should use the *pExpertStartupInfo* parameter.</span></span> <span data-ttu-id="7587f-121">Le seul indicateur défini est **l' \_ indicateur de démarrage expert \_ utiliser les données de \_ \_ démarrage \_ sur les \_ \_ \_ données de configuration**.</span><span class="sxs-lookup"><span data-stu-id="7587f-121">The only flag defined is **EXPERT\_STARTUP\_FLAG\_USE\_STARTUP\_DATA\_OVER\_CONFIG\_DATA**.</span></span> <span data-ttu-id="7587f-122">L’indicateur indique que l’expert doit utiliser le paramètre *pExpertStartupInfo* plutôt que le paramètre *ppConfig* qui a été transmis.</span><span class="sxs-lookup"><span data-stu-id="7587f-122">The flag indicates that the expert will use the *pExpertStartupInfo* parameter rather than the *ppConfig* parameter that passed in.</span></span> <span data-ttu-id="7587f-123">En règle générale, vous définissez l’indicateur lorsque vous démarrez l’expert à partir d’un menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="7587f-123">Typically, you set the flag when you start the expert from a context menu.</span></span>

</dd> <dt>

<span data-ttu-id="7587f-124">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7587f-124">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7587f-125">Handle de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="7587f-125">A handle to the parent window.</span></span> <span data-ttu-id="7587f-126">Utilisez la poignée pour ouvrir une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="7587f-126">Use the handle to open a dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7587f-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7587f-127">Return value</span></span>

<span data-ttu-id="7587f-128">Si la fonction réussit (autrement dit, s’il existe une configuration en cours), la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="7587f-128">If the function is successful (that is, if a current configuration exists), the return value is **TRUE**.</span></span>

<span data-ttu-id="7587f-129">Si la fonction échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="7587f-129">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7587f-130">Notes</span><span class="sxs-lookup"><span data-stu-id="7587f-130">Remarks</span></span>

<span data-ttu-id="7587f-131">Moniteur réseau appelle la **fonction de configuration avec** la configuration actuelle de l’expert, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="7587f-131">Network Monitor calls the **Configure** function with the current configuration of the expert, if one exists.</span></span> <span data-ttu-id="7587f-132">L’expert affiche une boîte de dialogue, dans laquelle vous pouvez modifier n’importe quel élément configurable.</span><span class="sxs-lookup"><span data-stu-id="7587f-132">The expert displays a dialog box, with which you can change any configurable item.</span></span>

<span data-ttu-id="7587f-133">Lorsque *ppConfig* est transmis et que Moniteur réseau n’a pas de configuration stockée pour l’expert spécifié, la valeur du paramètre peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="7587f-133">When *ppConfig* is passed in and Network Monitor does not have a configuration stored for the specified expert, the parameter value can be **NULL**.</span></span> <span data-ttu-id="7587f-134">Dans ce cas, la fonction **configure** prend en compte les valeurs par défaut codées en dur (ou, utilise les informations de démarrage) pour ouvrir la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="7587f-134">In this case, the **Configure** function assumes hard-coded default values (or, uses the startup information) to open the dialog box.</span></span>

<span data-ttu-id="7587f-135">Les données de configuration peuvent également être **null** lorsque la fonction **configure** est retournée, et une **valeur null** a été passée.</span><span class="sxs-lookup"><span data-stu-id="7587f-135">The configuration data can also be **NULL** when the **Configure** function returns, and a **NULL** was passed-in.</span></span> <span data-ttu-id="7587f-136">Cette situation se produit lorsque Moniteur réseau n’a pas de valeur par défaut stockée et que l’utilisateur appuie sur **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="7587f-136">This situation occurs when Network Monitor does not have a stored default, and the user presses **Cancel**.</span></span>

<span data-ttu-id="7587f-137">Le début de la structure de données [**EXPERTCONFIG**](expertconfig.md) comprend une section privée qui stocke les informations de taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="7587f-137">The beginning of the [**EXPERTCONFIG**](expertconfig.md) data structure includes a Private section that stores the structure size information.</span></span> <span data-ttu-id="7587f-138">La taille de la structure **EXPERTCONFIG** doit inclure la longueur **DWORD** réservée qui apparaît au début de la structure.</span><span class="sxs-lookup"><span data-stu-id="7587f-138">The size of the **EXPERTCONFIG** structure should include the reserved **DWORD** length that appears at the beginning of the structure.</span></span> <span data-ttu-id="7587f-139">Par exemple, si vos données de configuration nécessitent 20 octets d’espace de stockage, allouez 24 octets pour stocker les données.</span><span class="sxs-lookup"><span data-stu-id="7587f-139">For example, if your configuration data requires 20 bytes of storage space, allocate 24 bytes to store the data.</span></span> <span data-ttu-id="7587f-140">Si un *ppConfig* a la **valeur null**, la fonction **configure** appelle la fonction [**ExpertAllocMemory**](expertallocmemory.md) pour allouer une nouvelle configuration dont la taille est correcte.</span><span class="sxs-lookup"><span data-stu-id="7587f-140">If a *ppConfig* is **NULL**, the **Configure** function calls the [**ExpertAllocMemory**](expertallocmemory.md) function to allocate a new configuration that is the correct size.</span></span> <span data-ttu-id="7587f-141">Si la mémoire tampon n’est pas suffisante pour contenir les données de l’expert, l’expert doit appeler la fonction [**ExpertReallocMemory**](expertreallocmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="7587f-141">If the buffer is not enough to hold the expert data, the expert should call the [**ExpertReallocMemory**](expertreallocmemory.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7587f-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7587f-142">Requirements</span></span>



| <span data-ttu-id="7587f-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7587f-143">Requirement</span></span> | <span data-ttu-id="7587f-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="7587f-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7587f-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7587f-145">Minimum supported client</span></span><br/> | <span data-ttu-id="7587f-146">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7587f-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7587f-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7587f-147">Minimum supported server</span></span><br/> | <span data-ttu-id="7587f-148">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7587f-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7587f-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="7587f-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="7587f-150"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7587f-150"><dt>Netmon.h</dt></span></span> </dl> |



 

 




