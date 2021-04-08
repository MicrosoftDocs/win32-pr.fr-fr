---
description: Retourne le frame demandé à partir d’une capture chargée.
ms.assetid: efd1cff5-a3a1-4910-b003-25b6e10dad6e
title: ExpertGetFrame, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2bd02bde8caf157b6df6b1dd772a8f7574df0e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862021"
---
# <a name="expertgetframe-function"></a><span data-ttu-id="859b0-103">ExpertGetFrame fonction)</span><span class="sxs-lookup"><span data-stu-id="859b0-103">ExpertGetFrame function</span></span>

<span data-ttu-id="859b0-104">La fonction **ExpertGetFrame** retourne le frame demandé à partir d’une capture chargée.</span><span class="sxs-lookup"><span data-stu-id="859b0-104">The **ExpertGetFrame** function returns the requested frame from a loaded capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="859b0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="859b0-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertGetFrame(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  DWORD                   Direction,
  _In_  DWORD                   RequestFlags,
  _In_  DWORD                   RequestedFrameNumber,
  _In_  HFILTER                 hFilter,
  _Out_ LPEXPERTFRAMEDESCRIPTOR pEFrameDescriptor
);
```



## <a name="parameters"></a><span data-ttu-id="859b0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="859b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="859b0-107">*hExpertKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="859b0-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="859b0-108">Identificateur d’expert unique.</span><span class="sxs-lookup"><span data-stu-id="859b0-108">A unique expert identifier.</span></span> <span data-ttu-id="859b0-109">Moniteur réseau transmet l’identificateur *hExpertKey* à l’expert lorsqu’il appelle la fonction [**Run**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="859b0-109">Network Monitor passes the *hExpertKey* identifier to the expert when it calls the [**Run**](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="859b0-110">*Sens* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="859b0-110">*Direction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="859b0-111">Valeur qui identifie la façon dont Moniteur réseau recherche le frame.</span><span class="sxs-lookup"><span data-stu-id="859b0-111">A value that identifies how Network Monitor searches for the frame.</span></span>



| <span data-ttu-id="859b0-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="859b0-112">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="859b0-113">Signification</span><span class="sxs-lookup"><span data-stu-id="859b0-113">Meaning</span></span>                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="GET_SPECIFIED_FRAME"></span><span id="get_specified_frame"></span><dl> <span data-ttu-id="859b0-114"><dt>**Obtient \_ le \_ Frame spécifié**</dt></span><span class="sxs-lookup"><span data-stu-id="859b0-114"><dt>**GET\_SPECIFIED\_FRAME**</dt></span></span> </dl>              | <span data-ttu-id="859b0-115">Retourne le frame demandé.</span><span class="sxs-lookup"><span data-stu-id="859b0-115">Return the requested frame.</span></span><br/> |
| <span id="GET_FRAME_NEXT_FORWARD"></span><span id="get_frame_next_forward"></span><dl> <span data-ttu-id="859b0-116"><dt>**RECEVOIR le \_ cadre \_ suivant \_**</dt></span><span class="sxs-lookup"><span data-stu-id="859b0-116"><dt>**GET\_FRAME\_NEXT\_FORWARD**</dt></span></span> </dl>    | <span data-ttu-id="859b0-117">Retourne le frame suivant.</span><span class="sxs-lookup"><span data-stu-id="859b0-117">Return the next frame.</span></span><br/>      |
| <span id="GET_FRAME_NEXT_BACKWARD"></span><span id="get_frame_next_backward"></span><dl> <span data-ttu-id="859b0-118"><dt>**RECEVOIR le frame vers l' \_ \_ \_ arrière suivant**</dt></span><span class="sxs-lookup"><span data-stu-id="859b0-118"><dt>**GET\_FRAME\_NEXT\_BACKWARD**</dt></span></span> </dl> | <span data-ttu-id="859b0-119">Retourne le frame précédent.</span><span class="sxs-lookup"><span data-stu-id="859b0-119">Return the previous frame.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="859b0-120">*RequestFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="859b0-120">*RequestFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="859b0-121">Indicateurs qui spécifient comment Moniteur réseau doit gérer la requête.</span><span class="sxs-lookup"><span data-stu-id="859b0-121">The flags that specify how Network Monitor should handle the request.</span></span> <span data-ttu-id="859b0-122">Spécifiez un ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="859b0-122">Specify one or more of the following flags.</span></span>



| <span data-ttu-id="859b0-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="859b0-123">Value</span></span>                                                                                                                                                                                             | <span data-ttu-id="859b0-124">Signification</span><span class="sxs-lookup"><span data-stu-id="859b0-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAGS_DEFER_TO_UI_FILTER"></span><span id="flags_defer_to_ui_filter"></span><dl> <span data-ttu-id="859b0-125"><dt>**les indicateurs \_ diffèrent \_ du \_ filtre d’interface utilisateur \_**</dt></span><span class="sxs-lookup"><span data-stu-id="859b0-125"><dt>**FLAGS\_DEFER\_TO\_UI\_FILTER**</dt></span></span> </dl> | <span data-ttu-id="859b0-126">Avant d’appliquer le paramètre de filtre d’affichage de l’expert qui est spécifié dans *hFilter*, appliquez le filtre d’affichage que Moniteur réseau utilise au démarrage de l’expert.</span><span class="sxs-lookup"><span data-stu-id="859b0-126">Before applying the display filter parameter of the expert which is specified in *hFilter*, apply the display filter that Network Monitor is using when the expert starts.</span></span><br/>                                                                                                                              |
| <span id="FLAGS_ATTACH_PROPERTIES"></span><span id="flags_attach_properties"></span><dl> <span data-ttu-id="859b0-127"><dt>**INDICATEURS \_ propriétés d’attachement \_**</dt></span><span class="sxs-lookup"><span data-stu-id="859b0-127"><dt>**FLAGS\_ATTACH\_PROPERTIES**</dt></span></span> </dl>      | <span data-ttu-id="859b0-128">Les propriétés que tous les analyseurs de protocole localisent avec les sections revendiquées de ce frame sont attachées au frame.</span><span class="sxs-lookup"><span data-stu-id="859b0-128">The properties that all protocol parsers find with claimed sections of this frame are attached to the frame.</span></span> <span data-ttu-id="859b0-129">Si l’indicateur n’est pas défini, le champ **lpPropertyTable** de la structure [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) (retournée par **PEFrameDescriptor**) aura la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="859b0-129">If the flag is not set, the **lpPropertyTable** field of the [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) structure (returned by **pEFrameDescriptor**) will be set to **NULL**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="859b0-130">*RequestedFrameNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="859b0-130">*RequestedFrameNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="859b0-131">Numéro de la trame demandée.</span><span class="sxs-lookup"><span data-stu-id="859b0-131">The number of the requested frame.</span></span>

</dd> <dt>

<span data-ttu-id="859b0-132">*hFilter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="859b0-132">*hFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="859b0-133">Handle vers le filtre d’affichage de l’expert.</span><span class="sxs-lookup"><span data-stu-id="859b0-133">A handle to the expert display filter.</span></span> <span data-ttu-id="859b0-134">Si l’expert n’a pas de filtre d’affichage, affectez la valeur **null** au paramètre.</span><span class="sxs-lookup"><span data-stu-id="859b0-134">If the expert does not have a display filter, set the parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="859b0-135">*pEFrameDescriptor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="859b0-135">*pEFrameDescriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="859b0-136">La structure [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) qui, au retour, décrit le frame.</span><span class="sxs-lookup"><span data-stu-id="859b0-136">The [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) structure that, on return, describes the frame.</span></span> <span data-ttu-id="859b0-137">L’expert doit allouer et libérer la mémoire utilisée par cette structure.</span><span class="sxs-lookup"><span data-stu-id="859b0-137">The expert must allocate and free the memory that this structure uses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="859b0-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="859b0-138">Return value</span></span>

<span data-ttu-id="859b0-139">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="859b0-139">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="859b0-140">Si la fonction échoue, la valeur de retour indique la raison de l’échec.</span><span class="sxs-lookup"><span data-stu-id="859b0-140">If the function is unsuccessful, the return value indicates the reason for the failure.</span></span> <span data-ttu-id="859b0-141">Si la valeur de retour est NMERR \_ expert \_ Terminate, l’expert doit immédiatement procéder au nettoyage et au retour ; l’utilisateur a annulé l’exécution de l’expert.</span><span class="sxs-lookup"><span data-stu-id="859b0-141">If the return value is NMERR\_EXPERT\_TERMINATE, the expert must immediately clean up and return; the user has aborted the expert run.</span></span>

## <a name="remarks"></a><span data-ttu-id="859b0-142">Notes</span><span class="sxs-lookup"><span data-stu-id="859b0-142">Remarks</span></span>

<span data-ttu-id="859b0-143">Si vous définissez FLAGs \_ Attach \_ Properties, l’appel nécessite plus de ressources que si vous ne définissez pas l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="859b0-143">If you set FLAGS\_ATTACH\_PROPERTIES, the call requires more resources than if you do not set the flag.</span></span> <span data-ttu-id="859b0-144">Si l’indicateur n’est pas défini, un pointeur pointe vers le frame brut et vers les données relatives au frame.</span><span class="sxs-lookup"><span data-stu-id="859b0-144">If the flag is not set, a pointer points to the raw frame and to data about the frame.</span></span> <span data-ttu-id="859b0-145">Si cet indicateur est défini, Moniteur réseau joint toutes les propriétés au frame en appelant chaque analyseur qui prétend une partie du frame.</span><span class="sxs-lookup"><span data-stu-id="859b0-145">If this flag is set, Network Monitor attaches all properties to the frame by calling every parser that claims a portion of the frame.</span></span> <span data-ttu-id="859b0-146">Il peut s’agir d’un processus lent.</span><span class="sxs-lookup"><span data-stu-id="859b0-146">This can be a slow process.</span></span>

<span data-ttu-id="859b0-147">Les experts ne doivent pas définir \_ l' \_ indicateur de propriétés d’attachement Flags, sauf si les experts requièrent les propriétés que les analyseurs attachent au frame.</span><span class="sxs-lookup"><span data-stu-id="859b0-147">Experts should not set the FLAGS\_ATTACH\_PROPERTIES flag unless the experts require the properties that parsers attach to the frame.</span></span> <span data-ttu-id="859b0-148">Si possible, les experts doivent appeler la fonction **ExpertGetFrame** sans l’indicateur, puis extraire les données requises directement à partir du frame.</span><span class="sxs-lookup"><span data-stu-id="859b0-148">If possible, experts should call the **ExpertGetFrame** function without the flag, and then extract the required data directly from the frame.</span></span>

<span data-ttu-id="859b0-149">Si l’expert appelle **ExpertGetFrame** sans l’indicateur Flags \_ Attach \_ Properties et requiert les propriétés associées à ce frame (un événement, par exemple), l’expert appelle **ExpertGetFrame** avec les mêmes paramètres, à l’exception des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="859b0-149">If the expert calls **ExpertGetFrame** without the FLAGS\_ATTACH\_PROPERTIES flag and requires the properties associated with that frame (an event, for example), the expert calls **ExpertGetFrame** with the same parameters except for the following:</span></span>

``` syntax
Direction = EXPERT_GET_SPECIFIED_FRAME;
RequestFlags &= (~EXPERT_DEFER_TO_UI_FILTER) | EXPERT_ATTACH_PROPERTIES;
RequestedFrameNumber= (The actual frame number you want);
hFilter = NULL;
pEFrameDescriptor = (The same one as last time);
```

<span data-ttu-id="859b0-150">L’utilisation du code précédent garantit que l’expert obtient le frame requis sans devoir rappeler le code de filtre.</span><span class="sxs-lookup"><span data-stu-id="859b0-150">Using the preceding code ensures that the expert gets the required frame without having to call filter code again.</span></span>

<span data-ttu-id="859b0-151">Vous pouvez définir le paramètre *hFilter* en tant que **LPVOID**.</span><span class="sxs-lookup"><span data-stu-id="859b0-151">You can set the *hFilter* parameter as an **LPVOID**.</span></span> <span data-ttu-id="859b0-152">S’il existe, le frame retourné passe ce filtre.</span><span class="sxs-lookup"><span data-stu-id="859b0-152">If it exists, the returned frame passes this filter.</span></span> <span data-ttu-id="859b0-153">Si l’expert n’a pas de filtre d’affichage à passer à la fonction (si *hFilter* a la **valeur null** ), le frame retourné n’est pas filtré.</span><span class="sxs-lookup"><span data-stu-id="859b0-153">If the expert does not have a display filter to pass to the function (if *hFilter* is **NULL** ), then the frame returned is not filtered.</span></span>

<span data-ttu-id="859b0-154">La fonction **ExpertGetFrame** peut uniquement être appelée par des experts qui implémentent la fonction [**exécuter**](run.md) ou [**configurer**](configure.md) l’exportation.</span><span class="sxs-lookup"><span data-stu-id="859b0-154">The **ExpertGetFrame** function can only be called by experts that implement the [**Run**](run.md) or [**Configure**](configure.md) export function.</span></span>

## <a name="requirements"></a><span data-ttu-id="859b0-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="859b0-155">Requirements</span></span>



| <span data-ttu-id="859b0-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="859b0-156">Requirement</span></span> | <span data-ttu-id="859b0-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="859b0-157">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="859b0-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="859b0-158">Minimum supported client</span></span><br/> | <span data-ttu-id="859b0-159">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="859b0-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="859b0-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="859b0-160">Minimum supported server</span></span><br/> | <span data-ttu-id="859b0-161">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="859b0-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="859b0-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="859b0-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="859b0-163"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="859b0-163"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="859b0-164">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="859b0-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="859b0-165"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="859b0-165"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="859b0-166">DLL</span><span class="sxs-lookup"><span data-stu-id="859b0-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="859b0-167"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="859b0-167"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




