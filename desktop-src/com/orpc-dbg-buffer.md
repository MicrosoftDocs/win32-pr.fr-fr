---
title: Structure ORPC_DBG_BUFFER
description: La \_ structure de \_ mémoire tampon dbg ORPC est le format de mémoire tampon utilisé pour marshaler les données RPC vers les méthodes de l’interface IOrpcDebugNotify.
ms.assetid: 444cd3b8-bc7b-425d-9ccc-04fd6c7393b2
keywords:
- Structure COM ORPC_DBG_BUFFER
- Pointeur de structure PORPC_DBG_BUFFER COM
topic_type:
- apiref
api_name:
- ORPC_DBG_BUFFER
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dc42251b928207a2b009a18c1d88e94dcf1492a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510948"
---
# <a name="orpc_dbg_buffer-structure"></a><span data-ttu-id="d39be-105">ORPC \_ , \_ structure de mémoire tampon dbg</span><span class="sxs-lookup"><span data-stu-id="d39be-105">ORPC\_DBG\_BUFFER structure</span></span>

<span data-ttu-id="d39be-106">La structure de **\_ \_ mémoire tampon dbg ORPC** est le format de mémoire tampon utilisé pour marshaler les données RPC vers les méthodes de l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="d39be-106">The **ORPC\_DBG\_BUFFER** structure is the buffer format used to marshalled RPC data to the methods of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d39be-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d39be-107">Syntax</span></span>


```C++
typedef struct _ORPC_DBG_BUFFER {
  DWORD alwaysOrSometimes;
  BYTE  verMajor;
  BYTE  verMinor;
  DWORD cbRemaining;
  GUID  guidSemantic;
  union {
    BOOL   fStopOnOtherSide;
    USHORT wDebuggingOpCode;
    USHORT cExtent;
    BYTE   padding[2];
    struct {
      ULONG cb;
      GUID  guidExtent;
      BYTE  *rgbData;
    };
  };
} ORPC_DBG_BUFFER, *PORPC_DBG_BUFFER;
```



## <a name="members"></a><span data-ttu-id="d39be-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d39be-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d39be-109">**alwaysOrSometimes**</span><span class="sxs-lookup"><span data-stu-id="d39be-109">**alwaysOrSometimes**</span></span>
</dt> <dd>

<span data-ttu-id="d39be-110">Valeur qui contrôle la génération du débogueur.</span><span class="sxs-lookup"><span data-stu-id="d39be-110">A value that controls debugger spawning.</span></span> <span data-ttu-id="d39be-111">**alwaysOrSometimes** peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="d39be-111">**alwaysOrSometimes** can be one of the following values:</span></span>



| <span data-ttu-id="d39be-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="d39be-112">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="d39be-113">Signification</span><span class="sxs-lookup"><span data-stu-id="d39be-113">Meaning</span></span>                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ORPC_DEBUG_ALWAYS"></span><span id="orpc_debug_always"></span><dl> <span data-ttu-id="d39be-114"><dt>**ORPC \_ Débogage \_ toujours**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="d39be-114"><dt>**ORPC\_DEBUG\_ALWAYS**</dt> <dt>0x00000000</dt></span></span> </dl>                              | <span data-ttu-id="d39be-115">Si cette valeur est définie, COM déclenche toujours la notification du client ou du serveur sur le récepteur.</span><span class="sxs-lookup"><span data-stu-id="d39be-115">If set, COM will always raise the client or server notification on the receiver.</span></span><br/>                                                                                                                                                    |
| <span id="ORPC_DEBUG_IF_HOOK_ENABLED"></span><span id="orpc_debug_if_hook_enabled"></span><dl> <span data-ttu-id="d39be-116"><dt>**ORPC \_ Déboguer \_ si le \_ raccordement est \_ activé**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="d39be-116"><dt>**ORPC\_DEBUG\_IF\_HOOK\_ENABLED**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="d39be-117">Si cette option est définie, COM déclenche uniquement la notification du client ou du serveur sur le récepteur si le débogage COM a été activé en appelant [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) dans ce processus avec la valeur **true** affectée à **fTrace** .</span><span class="sxs-lookup"><span data-stu-id="d39be-117">If set, COM will only raise the client or server notification on the receiver if COM debugging has been enabled by calling [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) in that process with **fTrace** set to **TRUE**.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="d39be-118">**verMajor**</span><span class="sxs-lookup"><span data-stu-id="d39be-118">**verMajor**</span></span>
</dt> <dd>

<span data-ttu-id="d39be-119">Numéro de version principale de la spécification de format de données.</span><span class="sxs-lookup"><span data-stu-id="d39be-119">The major version number of the data format specification.</span></span>

</dd> <dt>

<span data-ttu-id="d39be-120">**verMinor**</span><span class="sxs-lookup"><span data-stu-id="d39be-120">**verMinor**</span></span>
</dt> <dd>

<span data-ttu-id="d39be-121">Numéro de version mineure de la spécification de format de données.</span><span class="sxs-lookup"><span data-stu-id="d39be-121">The minor version number of the data format specification.</span></span>

</dd> <dt>

<span data-ttu-id="d39be-122">**cbRemaining**</span><span class="sxs-lookup"><span data-stu-id="d39be-122">**cbRemaining**</span></span>
</dt> <dd>

<span data-ttu-id="d39be-123">Nombre d’octets, inclus de **cbRemaining**, qui suivent dans cette structure.</span><span class="sxs-lookup"><span data-stu-id="d39be-123">The number of bytes, inclusive of **cbRemaining**, that follow in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="d39be-124">**guidSemantic**</span><span class="sxs-lookup"><span data-stu-id="d39be-124">**guidSemantic**</span></span>
</dt> <dd>

<span data-ttu-id="d39be-125">GUID qui détermine quels membres de l’Union sont présents ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d39be-125">A GUID that determines which members of the union are present below.</span></span> <span data-ttu-id="d39be-126">**guidSemantic** peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="d39be-126">**guidSemantic** can take one of the following values:</span></span>



| <span data-ttu-id="d39be-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="d39be-127">Value</span></span>                                                                                                           | <span data-ttu-id="d39be-128">Signification</span><span class="sxs-lookup"><span data-stu-id="d39be-128">Meaning</span></span>                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d39be-129"><dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt></span><span class="sxs-lookup"><span data-stu-id="d39be-129"><dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt></span></span> </dl> | <span data-ttu-id="d39be-130">Détermine si l’exécution pas à pas unique doit être effectuée par le débogueur.</span><span class="sxs-lookup"><span data-stu-id="d39be-130">Determines if single stepping is to be performed by the debugger.</span></span> <span data-ttu-id="d39be-131">Seul le membre **fStopOnOtherSide** de l’Union est présent ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d39be-131">Only the **fStopOnOtherSide** member of the union is present below.</span></span><br/>                                             |
| <dl> <span data-ttu-id="d39be-132"><dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt></span><span class="sxs-lookup"><span data-stu-id="d39be-132"><dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt></span></span> </dl> | <span data-ttu-id="d39be-133">Détermine si les données RPC triées et les OpCodes de débogage sont passés au récepteur.</span><span class="sxs-lookup"><span data-stu-id="d39be-133">Determines if RPC marshalled data and debugging opcodes are passed to the receiver.</span></span> <span data-ttu-id="d39be-134">Tous les membres de l’Union sont présents ci-dessous, à l’exception de **fStopOnOtherSide**.</span><span class="sxs-lookup"><span data-stu-id="d39be-134">All of the members of the union are present below with the exception of **fStopOnOtherSide**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d39be-135">**fStopOnOtherSide**</span><span class="sxs-lookup"><span data-stu-id="d39be-135">**fStopOnOtherSide**</span></span>
</dt> <dd>

<span data-ttu-id="d39be-136">Si la **valeur est true**, le pas à pas est exécuté par le débogueur et il doit sortir du serveur et continuer l’exécution une fois que l’autre côté est atteint.</span><span class="sxs-lookup"><span data-stu-id="d39be-136">If **TRUE**, single stepping is performed by the debugger and it should step out of the server and continue execution once the other side is reached.</span></span> <span data-ttu-id="d39be-137">Dans le cas contraire, l’exécution pas à pas n’est pas effectuée et l’exécution du débogueur s’arrête de l’autre côté.</span><span class="sxs-lookup"><span data-stu-id="d39be-137">Otherwise, single stepping is not performed and debugger execution stops on the other side.</span></span>

</dd> <dt>

<span data-ttu-id="d39be-138">**wDebuggingOpCode**</span><span class="sxs-lookup"><span data-stu-id="d39be-138">**wDebuggingOpCode**</span></span>
</dt> <dd>

<span data-ttu-id="d39be-139">Valeur qui autorise la spécification d’une série d’opérations.</span><span class="sxs-lookup"><span data-stu-id="d39be-139">A value that allows for one of a series of operations to be specified.</span></span> <span data-ttu-id="d39be-140">**wDebuggingOpCode** peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="d39be-140">**wDebuggingOpCode** can take one of the following values:</span></span>



| <span data-ttu-id="d39be-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="d39be-141">Value</span></span>                                                                             | <span data-ttu-id="d39be-142">Signification</span><span class="sxs-lookup"><span data-stu-id="d39be-142">Meaning</span></span>                                                                                              |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d39be-143"><dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="d39be-143"><dt>0x0000</dt></span></span> </dl> | <span data-ttu-id="d39be-144">Pas d'opération.</span><span class="sxs-lookup"><span data-stu-id="d39be-144">No operation.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="d39be-145"><dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="d39be-145"><dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="d39be-146">Si cette valeur est définie, la sémantique d’une seule étape est identique à celle de **fStopOnOtherSide** lorsqu’elle est définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="d39be-146">If set, single step semantics are identical to **fStopOnOtherSide** when set to **TRUE**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d39be-147">**cExtent**</span><span class="sxs-lookup"><span data-stu-id="d39be-147">**cExtent**</span></span>
</dt> <dd>

<span data-ttu-id="d39be-148">Remplissage.</span><span class="sxs-lookup"><span data-stu-id="d39be-148">Padding.</span></span> <span data-ttu-id="d39be-149">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="d39be-149">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="d39be-150">**padding**</span><span class="sxs-lookup"><span data-stu-id="d39be-150">**padding**</span></span>
</dt> <dd>

<span data-ttu-id="d39be-151">Remplissage.</span><span class="sxs-lookup"><span data-stu-id="d39be-151">Padding.</span></span> <span data-ttu-id="d39be-152">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="d39be-152">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="d39be-153">**libéré**</span><span class="sxs-lookup"><span data-stu-id="d39be-153">**cb**</span></span>
</dt> <dd>

<span data-ttu-id="d39be-154">Taille, en octets, des données dans **rgbData**.</span><span class="sxs-lookup"><span data-stu-id="d39be-154">The size, in bytes of the data in **rgbData**.</span></span>

</dd> <dt>

<span data-ttu-id="d39be-155">**guidExtent**</span><span class="sxs-lookup"><span data-stu-id="d39be-155">**guidExtent**</span></span>
</dt> <dd>

<span data-ttu-id="d39be-156">**GUID** qui détermine le type de données dans **rgbData**.</span><span class="sxs-lookup"><span data-stu-id="d39be-156">A **GUID** that determines the type of data in **rgbData**.</span></span> <span data-ttu-id="d39be-157">**guidExtent** peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="d39be-157">**guidExtent** can take one of the following values:</span></span>



| <span data-ttu-id="d39be-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="d39be-158">Value</span></span>                                                                                                           | <span data-ttu-id="d39be-159">Signification</span><span class="sxs-lookup"><span data-stu-id="d39be-159">Meaning</span></span>                                                   |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="d39be-160"><dt>53199051-57EB-11ce-A964-00AA006C3706</dt></span><span class="sxs-lookup"><span data-stu-id="d39be-160"><dt>53199051-57EB-11ce-A964-00AA006C3706</dt></span></span> </dl> | <span data-ttu-id="d39be-161">**rgbData** est un pointeur d’interface marshalé.</span><span class="sxs-lookup"><span data-stu-id="d39be-161">**rgbData** is a marshalled interface pointer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d39be-162">**rgbData**</span><span class="sxs-lookup"><span data-stu-id="d39be-162">**rgbData**</span></span>
</dt> <dd>

<span data-ttu-id="d39be-163">Mémoire tampon d' **octets** utilisée pour passer des données com triées par RPC entre les débogueurs client et serveur.</span><span class="sxs-lookup"><span data-stu-id="d39be-163">A **BYTE** buffer used to pass RPC marshalled COM data between the client and server debuggers.</span></span> <span data-ttu-id="d39be-164">Le contenu de **rgbData** est déterminé par le **GUID** dans **guidExtent**.</span><span class="sxs-lookup"><span data-stu-id="d39be-164">The contents of **rgbData** are determined by the **GUID** in **guidExtent**.</span></span>



| <span data-ttu-id="d39be-165">Valeur guidExtent</span><span class="sxs-lookup"><span data-stu-id="d39be-165">guidExtent Value</span></span>                     | <span data-ttu-id="d39be-166">contenu rgbData</span><span class="sxs-lookup"><span data-stu-id="d39be-166">rgbData contents</span></span>                                                                                                                                                                                                                                    |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d39be-167">53199051-57EB-11ce-A964-00AA006C3706</span><span class="sxs-lookup"><span data-stu-id="d39be-167">53199051-57EB-11ce-A964-00AA006C3706</span></span> | <span data-ttu-id="d39be-168">Pointeur d’interface marshalé qui résulte de l’appel de [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface).</span><span class="sxs-lookup"><span data-stu-id="d39be-168">A marshalled interface pointer that results from calling [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface).</span></span> <span data-ttu-id="d39be-169">Le pointeur marshalé est converti en son pointeur d’interface correspondant à l’aide de [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span><span class="sxs-lookup"><span data-stu-id="d39be-169">The marshalled pointer is converted into its corresponding interface pointer using [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d39be-170">Notes</span><span class="sxs-lookup"><span data-stu-id="d39be-170">Remarks</span></span>

<span data-ttu-id="d39be-171">Les membres de cette structure ont un alignement sur 1 octet et sont toujours transmis dans l’ordre d’octet avec primauté des octets de poids faible (Little-endian).</span><span class="sxs-lookup"><span data-stu-id="d39be-171">This members of this structure have 1-byte alignment and are always transmitted in little-endian byte order.</span></span>

## <a name="requirements"></a><span data-ttu-id="d39be-172">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d39be-172">Requirements</span></span>



| <span data-ttu-id="d39be-173">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d39be-173">Requirement</span></span> | <span data-ttu-id="d39be-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="d39be-174">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="d39be-175">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d39be-175">Minimum supported client</span></span><br/> | <span data-ttu-id="d39be-176">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d39be-176">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="d39be-177">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d39be-177">Minimum supported server</span></span><br/> | <span data-ttu-id="d39be-178">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d39be-178">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d39be-179">En-tête</span><span class="sxs-lookup"><span data-stu-id="d39be-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="d39be-180"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="d39be-180"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d39be-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d39be-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d39be-182">**ORPC \_ dbg \_ tout**</span><span class="sxs-lookup"><span data-stu-id="d39be-182">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="d39be-183">**ORPC \_ init \_ args**</span><span class="sxs-lookup"><span data-stu-id="d39be-183">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="d39be-184">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="d39be-184">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="d39be-185">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="d39be-185">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

 





