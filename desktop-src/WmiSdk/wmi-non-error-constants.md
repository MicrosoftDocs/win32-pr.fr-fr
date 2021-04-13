---
description: Les codes de retour WMI qui indiquent l’État et n’indiquent pas d’erreur.
ms.assetid: 36faa3fb-9496-47ca-bdba-f8eb52a06ff7
ms.tgt_platform: multiple
title: Constantes WMI non-erreur (WbemCli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0880c9fda00f03c1fa8b174242bfc84ed9d75ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202283"
---
# <a name="wmi-non-error-constants"></a><span data-ttu-id="148fc-103">Constantes non-erreur WMI</span><span class="sxs-lookup"><span data-stu-id="148fc-103">WMI Non-Error Constants</span></span>

<span data-ttu-id="148fc-104">Les codes de retour WMI qui indiquent l’État et n’indiquent pas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="148fc-104">WMI return codes that indicate status and do not indicate an error.</span></span>

<span data-ttu-id="148fc-105">Si une opération ne génère pas d’erreur, WMI retourne l’un des codes suivants sous la forme d’un **HRESULT** qui indique l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="148fc-105">If an operation does not result in an error, WMI returns one of the following codes as an **HRESULT** that indicates the status of the operation.</span></span>

> [!Note]  
> <span data-ttu-id="148fc-106">Certaines méthodes des classes WMI peuvent retourner des codes d’erreur système et réseau (64, par exemple).</span><span class="sxs-lookup"><span data-stu-id="148fc-106">Some methods in WMI classes can return system and network error codes (64 for example).</span></span> <span data-ttu-id="148fc-107">Vous pouvez vérifier la définition de ces types de codes d’erreur à l’aide de la commande **net helpmsg** dans la fenêtre d’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="148fc-107">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="148fc-108">Par exemple, la commande **net helpmsg 64** retourne le message : le nom réseau spécifié n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="148fc-108">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span>

 

<span data-ttu-id="148fc-109">En C++, vous pouvez appeler [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) et spécifier le module de message **C : \\ Windows \\ system32 \\ WBEM \\wmiutils.dll** .</span><span class="sxs-lookup"><span data-stu-id="148fc-109">In C++, you can call [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) and specify **C:\\Windows\\System32\\wbem\\wmiutils.dll** as the message module.</span></span>

<dl> <dt>

<span data-ttu-id="148fc-110"><span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**WBEM \_ S \_ aucune \_ erreur**</span><span class="sxs-lookup"><span data-stu-id="148fc-110"><span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**WBEM\_S\_NO\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148fc-111">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="148fc-111">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="148fc-112">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="148fc-112">The operation was successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="148fc-113"><span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**\_faux S \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="148fc-113"><span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**WBEM\_S\_FALSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148fc-114">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="148fc-114">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="148fc-115">Plus aucun objet n’est disponible, le nombre d’objets retournés est inférieur au nombre demandé, ou il s’agit de la fin d’une énumération.</span><span class="sxs-lookup"><span data-stu-id="148fc-115">No more objects are available, the number of objects returned is less than the number requested, or this is the end of an enumeration.</span></span> <span data-ttu-id="148fc-116">Cette valeur est également retournée lorsque cette méthode est appelée avec la valeur 0 pour le paramètre *uCount* .</span><span class="sxs-lookup"><span data-stu-id="148fc-116">This value is also returned when this method is called with a value of 0 for the *uCount* parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="148fc-117"><span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**WBEM \_ S \_ \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="148fc-117"><span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**WBEM\_S\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148fc-118">262145 (0x40001)</span><span class="sxs-lookup"><span data-stu-id="148fc-118">262145 (0x40001)</span></span>
</dt> <dt>



<span data-ttu-id="148fc-119">Une tentative a été effectuée pour créer un objet ou une classe qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="148fc-119">An attempt was made to create an object or class that already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="148fc-120"><span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**\_paramètres WBEM \_ \_ \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="148fc-120"><span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**WBEM\_S\_RESET\_TO\_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148fc-121">262146 (0x40002)</span><span class="sxs-lookup"><span data-stu-id="148fc-121">262146 (0x40002)</span></span>
</dt> <dt>



<span data-ttu-id="148fc-122">Une propriété substituée a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="148fc-122">An overridden property was deleted.</span></span> <span data-ttu-id="148fc-123">Cette valeur est retournée pour signaler que la valeur non substituée d’origine a été restaurée à la suite de la suppression.</span><span class="sxs-lookup"><span data-stu-id="148fc-123">This value is returned to signal that the original non-overridden value has been restored as a result of the deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="148fc-124"><span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**WBEM \_ S \_ différent**</span><span class="sxs-lookup"><span data-stu-id="148fc-124"><span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**WBEM\_S\_DIFFERENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148fc-125">262147 (0x40003)</span><span class="sxs-lookup"><span data-stu-id="148fc-125">262147 (0x40003)</span></span>
</dt> <dt>



<span data-ttu-id="148fc-126">Les éléments (objets, classes, etc.) qui sont comparés ne sont pas identiques.</span><span class="sxs-lookup"><span data-stu-id="148fc-126">The items (objects, classes, and so on) that are being compared are not identical.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="148fc-127"><span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**délai de la WBEM \_ S \_**</span><span class="sxs-lookup"><span data-stu-id="148fc-127"><span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**WBEM\_S\_TIMEDOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148fc-128">262148 (0x40004)</span><span class="sxs-lookup"><span data-stu-id="148fc-128">262148 (0x40004)</span></span>
</dt> <dt>



<span data-ttu-id="148fc-129">Un appel a expiré. Il ne s’agit pas d’une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="148fc-129">A call timed out. This is not an error condition.</span></span> <span data-ttu-id="148fc-130">Par conséquent, certains résultats peuvent avoir également été retournés.</span><span class="sxs-lookup"><span data-stu-id="148fc-130">Therefore, some results may have also been returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="148fc-131"><span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**WBEM \_ \_ n’a \_ plus de \_ données**</span><span class="sxs-lookup"><span data-stu-id="148fc-131"><span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**WBEM\_S\_NO\_MORE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148fc-132">262149 (0x40005)</span><span class="sxs-lookup"><span data-stu-id="148fc-132">262149 (0x40005)</span></span>
</dt> <dt>



<span data-ttu-id="148fc-133">Aucune donnée supplémentaire n’est disponible à partir de l’énumération, et l’utilisateur doit mettre fin à l’énumération.</span><span class="sxs-lookup"><span data-stu-id="148fc-133">No more data is available from the enumeration, and the user must terminate the enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="148fc-134"><span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**l’opération des S WBEM a été \_ \_ \_ annulée**</span><span class="sxs-lookup"><span data-stu-id="148fc-134"><span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**WBEM\_S\_OPERATION\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148fc-135">262150 (0x40006)</span><span class="sxs-lookup"><span data-stu-id="148fc-135">262150 (0x40006)</span></span>
</dt> <dt>



<span data-ttu-id="148fc-136">L’opération a été intentionnellement ou non intentionnellement annulée.</span><span class="sxs-lookup"><span data-stu-id="148fc-136">The operation was intentionally or unintentionally canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="148fc-137"><span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**WBEM \_ \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="148fc-137"><span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**WBEM\_S\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148fc-138">262151 (0x40007)</span><span class="sxs-lookup"><span data-stu-id="148fc-138">262151 (0x40007)</span></span>
</dt> <dt>



<span data-ttu-id="148fc-139">Une demande est toujours en cours et les résultats ne sont pas encore disponibles.</span><span class="sxs-lookup"><span data-stu-id="148fc-139">A request is still in progress, and the results are not yet available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="148fc-140"><span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**\_objets WBEM \_ en double \_**</span><span class="sxs-lookup"><span data-stu-id="148fc-140"><span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**WBEM\_S\_DUPLICATE\_OBJECTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148fc-141">262152 (0x40008)</span><span class="sxs-lookup"><span data-stu-id="148fc-141">262152 (0x40008)</span></span>
</dt> <dt>



<span data-ttu-id="148fc-142">Plus d'une copie du même objet a été détectée dans le jeu de résultats d'une énumération.</span><span class="sxs-lookup"><span data-stu-id="148fc-142">More than one copy of the same object was detected in the result set of an enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="148fc-143"><span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**\_accès WBEM \_ S \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="148fc-143"><span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**WBEM\_S\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148fc-144">262153 (0x40009)</span><span class="sxs-lookup"><span data-stu-id="148fc-144">262153 (0x40009)</span></span>
</dt> <dt>



<span data-ttu-id="148fc-145">L’utilisateur s’est vu refuser l’accès à certaines ressources, mais pas toutes.</span><span class="sxs-lookup"><span data-stu-id="148fc-145">The user was denied access to some but not all resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="148fc-146"><span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**\_ \_ résultats PARTIELs \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="148fc-146"><span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**WBEM\_S\_PARTIAL\_RESULTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148fc-147">262160 (0x40010)</span><span class="sxs-lookup"><span data-stu-id="148fc-147">262160 (0x40010)</span></span>
</dt> <dt>



<span data-ttu-id="148fc-148">L’utilisateur n’a pas reçu tous les objets demandés en raison de ressources inaccessibles (autres que des violations de sécurité).</span><span class="sxs-lookup"><span data-stu-id="148fc-148">The user did not receive all of the objects requested due to inaccessible resources (other than security violations).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="148fc-149"><span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**\_service WBEM S \_ Limited \_**</span><span class="sxs-lookup"><span data-stu-id="148fc-149"><span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**WBEM\_S\_LIMITED\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148fc-150">274433 (0x43001)</span><span class="sxs-lookup"><span data-stu-id="148fc-150">274433 (0x43001)</span></span>
</dt> <dt>



<span data-ttu-id="148fc-151">Le fournisseur est en capacité de disposer d’un service limité.</span><span class="sxs-lookup"><span data-stu-id="148fc-151">The provider is capable of limited service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="148fc-152"><span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**WBEM \_ S \_ \_ mises à jour indirectement**</span><span class="sxs-lookup"><span data-stu-id="148fc-152"><span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**WBEM\_S\_INDIRECTLY\_UPDATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148fc-153">274434 (0x43002)</span><span class="sxs-lookup"><span data-stu-id="148fc-153">274434 (0x43002)</span></span>
</dt> <dt>



<span data-ttu-id="148fc-154">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="148fc-154">Reserved for future use.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="148fc-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="148fc-155">Requirements</span></span>



| <span data-ttu-id="148fc-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="148fc-156">Requirement</span></span> | <span data-ttu-id="148fc-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="148fc-157">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="148fc-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="148fc-158">Minimum supported client</span></span><br/> | <span data-ttu-id="148fc-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="148fc-159">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="148fc-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="148fc-160">Minimum supported server</span></span><br/> | <span data-ttu-id="148fc-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="148fc-161">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="148fc-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="148fc-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="148fc-163"><dt>WbemCli. h</dt></span><span class="sxs-lookup"><span data-stu-id="148fc-163"><dt>WbemCli.h</dt></span></span> </dl>   |
| <span data-ttu-id="148fc-164">MIDL</span><span class="sxs-lookup"><span data-stu-id="148fc-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="148fc-165"><dt>WbemCli. idl</dt></span><span class="sxs-lookup"><span data-stu-id="148fc-165"><dt>WbemCli.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="148fc-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="148fc-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="148fc-167">Codes de retour WMI</span><span class="sxs-lookup"><span data-stu-id="148fc-167">WMI Return Codes</span></span>](wmi-return-codes.md)
</dt> </dl>

 

