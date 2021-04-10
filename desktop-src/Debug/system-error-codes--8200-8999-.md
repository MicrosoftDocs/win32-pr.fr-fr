---
description: Décrit les codes d’erreur 8200-8999 définis dans le fichier d’en-tête WinError. h et est destiné aux développeurs.
ms.assetid: f16fdfa3-b080-47ee-a7dd-241fe2d24278
title: Codes d’erreur système (8200-8999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 7500ae4c178999de8052b0858089604652dc5237
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200996"
---
# <a name="system-error-codes-8200-8999"></a><span data-ttu-id="07c8f-103">Codes d’erreur système (8200-8999)</span><span class="sxs-lookup"><span data-stu-id="07c8f-103">System Error Codes (8200-8999)</span></span>

> [!NOTE]
> <span data-ttu-id="07c8f-104">Ces informations sont destinées aux développeurs qui déboguent les erreurs système.</span><span class="sxs-lookup"><span data-stu-id="07c8f-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="07c8f-105">Pour les autres erreurs, telles que les problèmes de Windows Update, il existe une liste de ressources dans la page [codes d’erreur](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="07c8f-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="07c8f-106">La liste suivante décrit les [codes d’erreur système](system-error-codes.md) pour les erreurs 8200 à 8999.</span><span class="sxs-lookup"><span data-stu-id="07c8f-106">The following list describes [system error codes](system-error-codes.md) for errors 8200 to 8999.</span></span> <span data-ttu-id="07c8f-107">Elles sont retournées par la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque de nombreuses fonctions échouent.</span><span class="sxs-lookup"><span data-stu-id="07c8f-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="07c8f-108">Pour récupérer le texte de description de l’erreur dans votre application, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le **format \_ message \_ de \_** l’indicateur système.</span><span class="sxs-lookup"><span data-stu-id="07c8f-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="07c8f-109"><span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**ERREUR \_ DS \_ non \_ installée**</span><span class="sxs-lookup"><span data-stu-id="07c8f-109"><span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**ERROR\_DS\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-110">8200 (0x2008)</span><span class="sxs-lookup"><span data-stu-id="07c8f-110">8200 (0x2008)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-111">Une erreur s’est produite lors de l’installation du service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="07c8f-111">An error occurred while installing the directory service.</span></span> <span data-ttu-id="07c8f-112">Pour plus d’informations, consultez le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="07c8f-112">For more information, see the event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-113"><span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**ERREUR d' \_ appartenance aux services DS \_ \_ évaluée \_ localement**</span><span class="sxs-lookup"><span data-stu-id="07c8f-113"><span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**ERROR\_DS\_MEMBERSHIP\_EVALUATED\_LOCALLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-114">8201 (0x2009)</span><span class="sxs-lookup"><span data-stu-id="07c8f-114">8201 (0x2009)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-115">Le service d’annuaire a évalué les appartenances aux groupes localement.</span><span class="sxs-lookup"><span data-stu-id="07c8f-115">The directory service evaluated group memberships locally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-116"><span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**ERREUR \_ DS \_ aucun \_ attribut \_ ou \_ valeur**</span><span class="sxs-lookup"><span data-stu-id="07c8f-116"><span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**ERROR\_DS\_NO\_ATTRIBUTE\_OR\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-117">8202 (0x200A)</span><span class="sxs-lookup"><span data-stu-id="07c8f-117">8202 (0x200A)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-118">L’attribut ou la valeur de service d’annuaire spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="07c8f-118">The specified directory service attribute or value does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-119"><span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**ERREUR \_ de \_ \_ syntaxe d’attribut non valide du service d’annuaire \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-119"><span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**ERROR\_DS\_INVALID\_ATTRIBUTE\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-120">8203 (0x200B)</span><span class="sxs-lookup"><span data-stu-id="07c8f-120">8203 (0x200B)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-121">La syntaxe d’attribut spécifiée pour le service d’annuaire n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="07c8f-121">The attribute syntax specified to the directory service is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-122"><span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**ERREUR \_ de \_ type d’attribut DS \_ \_ non défini**</span><span class="sxs-lookup"><span data-stu-id="07c8f-122"><span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**ERROR\_DS\_ATTRIBUTE\_TYPE\_UNDEFINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-123">8204 (0x200C)</span><span class="sxs-lookup"><span data-stu-id="07c8f-123">8204 (0x200C)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-124">Le type d’attribut spécifié au service d’annuaire n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="07c8f-124">The attribute type specified to the directory service is not defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-125"><span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**l' \_ attribut ou la valeur du service d’annuaire d’erreurs \_ \_ \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="07c8f-125"><span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**ERROR\_DS\_ATTRIBUTE\_OR\_VALUE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-126">8205 (0x200D)</span><span class="sxs-lookup"><span data-stu-id="07c8f-126">8205 (0x200D)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-127">La valeur ou l’attribut de service d’annuaire spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="07c8f-127">The specified directory service attribute or value already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-128"><span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**ERREUR \_ DS \_ occupé**</span><span class="sxs-lookup"><span data-stu-id="07c8f-128"><span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**ERROR\_DS\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-129">8206 (0x200E)</span><span class="sxs-lookup"><span data-stu-id="07c8f-129">8206 (0x200E)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-130">Le service d’annuaire est occupé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-130">The directory service is busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-131"><span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**ERREUR \_ DS \_ non disponible**</span><span class="sxs-lookup"><span data-stu-id="07c8f-131"><span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**ERROR\_DS\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-132">8207 (0x200F)</span><span class="sxs-lookup"><span data-stu-id="07c8f-132">8207 (0x200F)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-133">Le service d’annuaire n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="07c8f-133">The directory service is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-134"><span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**ERREUR \_ DS \_ aucun \_ RID \_ alloué**</span><span class="sxs-lookup"><span data-stu-id="07c8f-134"><span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**ERROR\_DS\_NO\_RIDS\_ALLOCATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-135">8208 (0x2010)</span><span class="sxs-lookup"><span data-stu-id="07c8f-135">8208 (0x2010)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-136">Le service d'annuaire n'a pas pu allouer un identificateur relatif.</span><span class="sxs-lookup"><span data-stu-id="07c8f-136">The directory service was unable to allocate a relative identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-137"><span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**ERREUR \_ DS \_ aucun \_ autre \_ RID**</span><span class="sxs-lookup"><span data-stu-id="07c8f-137"><span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**ERROR\_DS\_NO\_MORE\_RIDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-138">8209 (0x2011)</span><span class="sxs-lookup"><span data-stu-id="07c8f-138">8209 (0x2011)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-139">Le service d’annuaire a épuisé le pool d’identificateurs relatifs.</span><span class="sxs-lookup"><span data-stu-id="07c8f-139">The directory service has exhausted the pool of relative identifiers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-140"><span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**ERREUR \_ \_ propriétaire du \_ rôle incorrect DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-140"><span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**ERROR\_DS\_INCORRECT\_ROLE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-141">8210 (0x2012)</span><span class="sxs-lookup"><span data-stu-id="07c8f-141">8210 (0x2012)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-142">L’opération demandée n’a pas pu être effectuée car le service d’annuaire n’est pas le maître pour ce type d’opération.</span><span class="sxs-lookup"><span data-stu-id="07c8f-142">The requested operation could not be performed because the directory service is not the master for that type of operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-143"><span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**erreur d’initialisation de l' \_ \_ RIDMGR DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-143"><span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**ERROR\_DS\_RIDMGR\_INIT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-144">8211 (0x2013)</span><span class="sxs-lookup"><span data-stu-id="07c8f-144">8211 (0x2013)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-145">Le service d’annuaire n’a pas pu initialiser le sous-système qui alloue des identificateurs relatifs.</span><span class="sxs-lookup"><span data-stu-id="07c8f-145">The directory service was unable to initialize the subsystem that allocates relative identifiers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-146"><span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**ERREUR \_ de \_ \_ violation de classe obj du DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-146"><span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**ERROR\_DS\_OBJ\_CLASS\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-147">8212 (0x2014)</span><span class="sxs-lookup"><span data-stu-id="07c8f-147">8212 (0x2014)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-148">L’opération demandée n’a pas satisfait à une ou plusieurs contraintes associées à la classe de l’objet.</span><span class="sxs-lookup"><span data-stu-id="07c8f-148">The requested operation did not satisfy one or more constraints associated with the class of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-149"><span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**ERREUR \_ DS \_ Impossible \_ sur un \_ non- \_ Terminal**</span><span class="sxs-lookup"><span data-stu-id="07c8f-149"><span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**ERROR\_DS\_CANT\_ON\_NON\_LEAF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-150">8213 (0x2015)</span><span class="sxs-lookup"><span data-stu-id="07c8f-150">8213 (0x2015)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-151">Le service d’annuaire peut effectuer l’opération demandée uniquement sur un objet feuille.</span><span class="sxs-lookup"><span data-stu-id="07c8f-151">The directory service can perform the requested operation only on a leaf object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-152"><span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**ERREUR \_ DS \_ Impossible \_ sur \_ RDN**</span><span class="sxs-lookup"><span data-stu-id="07c8f-152"><span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**ERROR\_DS\_CANT\_ON\_RDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-153">8214 (0x2016)</span><span class="sxs-lookup"><span data-stu-id="07c8f-153">8214 (0x2016)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-154">Le service d’annuaire ne peut pas effectuer l’opération demandée sur l’attribut RDN d’un objet.</span><span class="sxs-lookup"><span data-stu-id="07c8f-154">The directory service cannot perform the requested operation on the RDN attribute of an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-155"><span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**ERREUR DS inverser la \_ \_ \_ \_ \_ classe obj**</span><span class="sxs-lookup"><span data-stu-id="07c8f-155"><span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**ERROR\_DS\_CANT\_MOD\_OBJ\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-156">8215 (0x2017)</span><span class="sxs-lookup"><span data-stu-id="07c8f-156">8215 (0x2017)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-157">Le service d’annuaire a détecté une tentative de modification de la classe d’objet d’un objet.</span><span class="sxs-lookup"><span data-stu-id="07c8f-157">The directory service detected an attempt to modify the object class of an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-158"><span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**erreur \_ de \_ \_ déplacement entre \_ DOM \_ des services d’annuaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-158"><span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**ERROR\_DS\_CROSS\_DOM\_MOVE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-159">8216 (0x2018)</span><span class="sxs-lookup"><span data-stu-id="07c8f-159">8216 (0x2018)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-160">L’opération de déplacement entre domaines demandée n’a pas pu être effectuée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-160">The requested cross-domain move operation could not be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-161"><span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**ERREUR \_ DS \_ GC \_ non \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="07c8f-161"><span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**ERROR\_DS\_GC\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-162">8217 (0x2019)</span><span class="sxs-lookup"><span data-stu-id="07c8f-162">8217 (0x2019)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-163">Impossible de contacter le serveur de catalogue global.</span><span class="sxs-lookup"><span data-stu-id="07c8f-163">Unable to contact the global catalog server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-164"><span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**\_stratégie partagée d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-164"><span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**ERROR\_SHARED\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-165">8218 (0x201A)</span><span class="sxs-lookup"><span data-stu-id="07c8f-165">8218 (0x201A)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-166">L’objet de stratégie est partagé et ne peut être modifié qu’à la racine.</span><span class="sxs-lookup"><span data-stu-id="07c8f-166">The policy object is shared and can only be modified at the root.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-167"><span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**objet de stratégie d’erreur \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="07c8f-167"><span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**ERROR\_POLICY\_OBJECT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-168">8219 (0x201B)</span><span class="sxs-lookup"><span data-stu-id="07c8f-168">8219 (0x201B)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-169">L’objet de stratégie n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="07c8f-169">The policy object does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-170"><span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**\_stratégie \_ d’erreur uniquement \_ dans \_ DS**</span><span class="sxs-lookup"><span data-stu-id="07c8f-170"><span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**ERROR\_POLICY\_ONLY\_IN\_DS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-171">8220 (0x201C)</span><span class="sxs-lookup"><span data-stu-id="07c8f-171">8220 (0x201C)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-172">Les informations de stratégie demandées se trouvent uniquement dans le service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="07c8f-172">The requested policy information is only in the directory service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-173"><span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**PROMOTION d’erreur \_ \_ active**</span><span class="sxs-lookup"><span data-stu-id="07c8f-173"><span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**ERROR\_PROMOTION\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-174">8221 (0x201D)</span><span class="sxs-lookup"><span data-stu-id="07c8f-174">8221 (0x201D)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-175">Une promotion de contrôleur de domaine est actuellement active.</span><span class="sxs-lookup"><span data-stu-id="07c8f-175">A domain controller promotion is currently active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-176"><span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**ERREUR \_ aucune \_ promotion \_ active**</span><span class="sxs-lookup"><span data-stu-id="07c8f-176"><span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**ERROR\_NO\_PROMOTION\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-177">8222 (0x201E)</span><span class="sxs-lookup"><span data-stu-id="07c8f-177">8222 (0x201E)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-178">Une promotion de contrôleur de domaine n’est pas active actuellement.</span><span class="sxs-lookup"><span data-stu-id="07c8f-178">A domain controller promotion is not currently active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-179"><span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**erreur des opérations de l’annuaire d’erreurs \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-179"><span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**ERROR\_DS\_OPERATIONS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-180">8224 (0x2020)</span><span class="sxs-lookup"><span data-stu-id="07c8f-180">8224 (0x2020)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-181">Une erreur d’opération s’est produite.</span><span class="sxs-lookup"><span data-stu-id="07c8f-181">An operations error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-182"><span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**erreur de \_ protocole du service d’annuaire \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-182"><span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**ERROR\_DS\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-183">8225 (0x2021)</span><span class="sxs-lookup"><span data-stu-id="07c8f-183">8225 (0x2021)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-184">Une erreur de protocole s'est produite.</span><span class="sxs-lookup"><span data-stu-id="07c8f-184">A protocol error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-185"><span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**ERREUR \_ TIMELIMIT de l’annuaire de services \_ \_ dépassée**</span><span class="sxs-lookup"><span data-stu-id="07c8f-185"><span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**ERROR\_DS\_TIMELIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-186">8226 (0x2022)</span><span class="sxs-lookup"><span data-stu-id="07c8f-186">8226 (0x2022)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-187">La limite de temps pour cette requête a été dépassée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-187">The time limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-188"><span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**ERREUR \_ SIZELIMIT de l’annuaire de services \_ \_ dépassée**</span><span class="sxs-lookup"><span data-stu-id="07c8f-188"><span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**ERROR\_DS\_SIZELIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-189">8227 (0x2023)</span><span class="sxs-lookup"><span data-stu-id="07c8f-189">8227 (0x2023)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-190">La limite de taille de cette demande a été dépassée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-190">The size limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-191"><span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**ERREUR \_ de \_ limite d’administration DS \_ \_ dépassée**</span><span class="sxs-lookup"><span data-stu-id="07c8f-191"><span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**ERROR\_DS\_ADMIN\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-192">8228 (0x2024)</span><span class="sxs-lookup"><span data-stu-id="07c8f-192">8228 (0x2024)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-193">La limite administrative de cette demande a été dépassée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-193">The administrative limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-194"><span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**ERREUR de \_ comparaison des services d’annuaire \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-194"><span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**ERROR\_DS\_COMPARE\_FALSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-195">8229 (0x2025)</span><span class="sxs-lookup"><span data-stu-id="07c8f-195">8229 (0x2025)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-196">La réponse de comparaison était false.</span><span class="sxs-lookup"><span data-stu-id="07c8f-196">The compare response was false.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-197"><span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**ERREUR de \_ comparaison des services d’annuaire \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-197"><span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**ERROR\_DS\_COMPARE\_TRUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-198">8230 (0x2026)</span><span class="sxs-lookup"><span data-stu-id="07c8f-198">8230 (0x2026)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-199">La réponse de comparaison a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="07c8f-199">The compare response was true.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-200"><span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**ERREUR \_ de \_ méthode d’authentification DS \_ \_ non \_ prise en charge**</span><span class="sxs-lookup"><span data-stu-id="07c8f-200"><span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**ERROR\_DS\_AUTH\_METHOD\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-201">8231 (0x2027)</span><span class="sxs-lookup"><span data-stu-id="07c8f-201">8231 (0x2027)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-202">La méthode d’authentification demandée n’est pas prise en charge par le serveur.</span><span class="sxs-lookup"><span data-stu-id="07c8f-202">The requested authentication method is not supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-203"><span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**ERREUR d’authentification forte de l' \_ Annuaire de services \_ \_ \_ requise**</span><span class="sxs-lookup"><span data-stu-id="07c8f-203"><span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**ERROR\_DS\_STRONG\_AUTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-204">8232 (0x2028)</span><span class="sxs-lookup"><span data-stu-id="07c8f-204">8232 (0x2028)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-205">Une méthode d’authentification plus sécurisée est requise pour ce serveur.</span><span class="sxs-lookup"><span data-stu-id="07c8f-205">A more secure authentication method is required for this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-206"><span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**ERREUR \_ d' \_ authentification incorrecte DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-206"><span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**ERROR\_DS\_INAPPROPRIATE\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-207">8233 (0x2029)</span><span class="sxs-lookup"><span data-stu-id="07c8f-207">8233 (0x2029)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-208">Authentification inappropriée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-208">Inappropriate authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-209"><span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**ERREUR \_ d' \_ authentification DS \_ inconnue**</span><span class="sxs-lookup"><span data-stu-id="07c8f-209"><span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**ERROR\_DS\_AUTH\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-210">8234 (0x202A)</span><span class="sxs-lookup"><span data-stu-id="07c8f-210">8234 (0x202A)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-211">Le mécanisme d’authentification est inconnu.</span><span class="sxs-lookup"><span data-stu-id="07c8f-211">The authentication mechanism is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-212"><span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**Référence de l’annuaire d’erreurs \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-212"><span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**ERROR\_DS\_REFERRAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-213">8235 (0x202B)</span><span class="sxs-lookup"><span data-stu-id="07c8f-213">8235 (0x202B)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-214">Une référence a été retournée à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="07c8f-214">A referral was returned from the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-215"><span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**erreur d’extension d’erreur de \_ service d’annuaire \_ non disponible \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-215"><span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**ERROR\_DS\_UNAVAILABLE\_CRIT\_EXTENSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-216">8236 (0x202C)</span><span class="sxs-lookup"><span data-stu-id="07c8f-216">8236 (0x202C)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-217">Le serveur ne prend pas en charge l’extension critique demandée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-217">The server does not support the requested critical extension.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-218"><span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**confidentialité des erreurs du \_ service d’annuaire \_ \_ requise**</span><span class="sxs-lookup"><span data-stu-id="07c8f-218"><span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**ERROR\_DS\_CONFIDENTIALITY\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-219">8237 (0x202D)</span><span class="sxs-lookup"><span data-stu-id="07c8f-219">8237 (0x202D)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-220">Cette demande requiert une connexion sécurisée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-220">This request requires a secure connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-221"><span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**ERREUR \_ de \_ correspondance inappropriée DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-221"><span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**ERROR\_DS\_INAPPROPRIATE\_MATCHING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-222">8238 (0x202E)</span><span class="sxs-lookup"><span data-stu-id="07c8f-222">8238 (0x202E)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-223">Correspondance inappropriée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-223">Inappropriate matching.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-224"><span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**ERREUR \_ de \_ violation de contrainte DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-224"><span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**ERROR\_DS\_CONSTRAINT\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-225">8239 (0x202F)</span><span class="sxs-lookup"><span data-stu-id="07c8f-225">8239 (0x202F)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-226">Une violation de contrainte s’est produite.</span><span class="sxs-lookup"><span data-stu-id="07c8f-226">A constraint violation occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-227"><span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**ERREUR \_ DS \_ non- \_ objet de ce type \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-227"><span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**ERROR\_DS\_NO\_SUCH\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-228">8240 (0x2030)</span><span class="sxs-lookup"><span data-stu-id="07c8f-228">8240 (0x2030)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-229">Cet objet ne se trouve pas sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="07c8f-229">There is no such object on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-230"><span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**ERREUR d' \_ alias du service d’annuaire \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-230"><span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**ERROR\_DS\_ALIAS\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-231">8241 (0x2031)</span><span class="sxs-lookup"><span data-stu-id="07c8f-231">8241 (0x2031)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-232">Il y a un problème d’alias.</span><span class="sxs-lookup"><span data-stu-id="07c8f-232">There is an alias problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-233"><span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**ERREUR \_ DS \_ \_ syntaxe DN non valide \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-233"><span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**ERROR\_DS\_INVALID\_DN\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-234">8242 (0x2032)</span><span class="sxs-lookup"><span data-stu-id="07c8f-234">8242 (0x2032)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-235">Une syntaxe DN non valide a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-235">An invalid dn syntax has been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-236"><span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**l’erreur \_ DS \_ est \_ feuille**</span><span class="sxs-lookup"><span data-stu-id="07c8f-236"><span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**ERROR\_DS\_IS\_LEAF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-237">8243 (0x2033)</span><span class="sxs-lookup"><span data-stu-id="07c8f-237">8243 (0x2033)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-238">L’objet est un objet feuille.</span><span class="sxs-lookup"><span data-stu-id="07c8f-238">The object is a leaf object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-239"><span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**ERREUR de l' \_ alias du service d’annuaire \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-239"><span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**ERROR\_DS\_ALIAS\_DEREF\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-240">8244 (0x2034)</span><span class="sxs-lookup"><span data-stu-id="07c8f-240">8244 (0x2034)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-241">Il y a un problème de déréférencement d’alias.</span><span class="sxs-lookup"><span data-stu-id="07c8f-241">There is an alias dereferencing problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-242"><span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**ERREUR \_ \_ \_ d’exécution du service d' \_ Annuaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-242"><span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**ERROR\_DS\_UNWILLING\_TO\_PERFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-243">8245 (0x2035)</span><span class="sxs-lookup"><span data-stu-id="07c8f-243">8245 (0x2035)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-244">Le serveur ne souhaite pas traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="07c8f-244">The server is unwilling to process the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-245"><span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**ERREUR \_ de \_ détection de boucle DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-245"><span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**ERROR\_DS\_LOOP\_DETECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-246">8246 (0x2036)</span><span class="sxs-lookup"><span data-stu-id="07c8f-246">8246 (0x2036)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-247">Une boucle a été détectée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-247">A loop has been detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-248"><span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**ERREUR \_ de \_ violation d’appellation des services d’annuaire \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-248"><span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**ERROR\_DS\_NAMING\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-249">8247 (0x2037)</span><span class="sxs-lookup"><span data-stu-id="07c8f-249">8247 (0x2037)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-250">Violation de nom.</span><span class="sxs-lookup"><span data-stu-id="07c8f-250">There is a naming violation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-251"><span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**ERREUR de résultats de l' \_ \_ objet DS \_ \_ trop \_ grand**</span><span class="sxs-lookup"><span data-stu-id="07c8f-251"><span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**ERROR\_DS\_OBJECT\_RESULTS\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-252">8248 (0x2038)</span><span class="sxs-lookup"><span data-stu-id="07c8f-252">8248 (0x2038)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-253">Le jeu de résultats est trop grand.</span><span class="sxs-lookup"><span data-stu-id="07c8f-253">The result set is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-254"><span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**l’erreur \_ DS \_ affecte \_ plusieurs \_ DSA**</span><span class="sxs-lookup"><span data-stu-id="07c8f-254"><span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**ERROR\_DS\_AFFECTS\_MULTIPLE\_DSAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-255">8249 (0x2039)</span><span class="sxs-lookup"><span data-stu-id="07c8f-255">8249 (0x2039)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-256">L’opération affecte plusieurs DSA.</span><span class="sxs-lookup"><span data-stu-id="07c8f-256">The operation affects multiple DSAs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-257"><span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**ERREUR \_ de \_ défaillance du serveur DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-257"><span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**ERROR\_DS\_SERVER\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-258">8250 (0x203A)</span><span class="sxs-lookup"><span data-stu-id="07c8f-258">8250 (0x203A)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-259">Le serveur n’est pas opérationnel.</span><span class="sxs-lookup"><span data-stu-id="07c8f-259">The server is not operational.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-260"><span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**erreur de l’erreur \_ \_ locale DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-260"><span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**ERROR\_DS\_LOCAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-261">8251 (0x203B)</span><span class="sxs-lookup"><span data-stu-id="07c8f-261">8251 (0x203B)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-262">Une erreur locale s’est produite.</span><span class="sxs-lookup"><span data-stu-id="07c8f-262">A local error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-263"><span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**erreur \_ d' \_ encodage du service d’annuaire \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-263"><span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**ERROR\_DS\_ENCODING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-264">8252 (0x203C)</span><span class="sxs-lookup"><span data-stu-id="07c8f-264">8252 (0x203C)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-265">Une erreur d’encodage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="07c8f-265">An encoding error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-266"><span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**erreur \_ de \_ décodage du service d’annuaire \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-266"><span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**ERROR\_DS\_DECODING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-267">8253 (0x203D)</span><span class="sxs-lookup"><span data-stu-id="07c8f-267">8253 (0x203D)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-268">Une erreur de décodage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="07c8f-268">A decoding error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-269"><span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**ERREUR de \_ filtre de service d’annuaire \_ \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="07c8f-269"><span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**ERROR\_DS\_FILTER\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-270">8254 (0x203E)</span><span class="sxs-lookup"><span data-stu-id="07c8f-270">8254 (0x203E)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-271">Le filtre de recherche ne peut pas être reconnu.</span><span class="sxs-lookup"><span data-stu-id="07c8f-271">The search filter cannot be recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-272"><span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**erreur \_ de \_ paramètre DS Error \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-272"><span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**ERROR\_DS\_PARAM\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-273">8255 (0x203F)</span><span class="sxs-lookup"><span data-stu-id="07c8f-273">8255 (0x203F)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-274">Un ou plusieurs paramètres ne sont pas conformes.</span><span class="sxs-lookup"><span data-stu-id="07c8f-274">One or more parameters are illegal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-275"><span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**ERREUR \_ DS \_ non \_ prise en charge**</span><span class="sxs-lookup"><span data-stu-id="07c8f-275"><span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**ERROR\_DS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-276">8256 (0x2040)</span><span class="sxs-lookup"><span data-stu-id="07c8f-276">8256 (0x2040)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-277">La méthode spécifiée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="07c8f-277">The specified method is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-278"><span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**ERREUR \_ DS \_ aucun \_ résultat \_ retourné**</span><span class="sxs-lookup"><span data-stu-id="07c8f-278"><span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**ERROR\_DS\_NO\_RESULTS\_RETURNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-279">8257 (0x2041)</span><span class="sxs-lookup"><span data-stu-id="07c8f-279">8257 (0x2041)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-280">Aucun résultat n’a été retourné.</span><span class="sxs-lookup"><span data-stu-id="07c8f-280">No results were returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-281"><span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**le contrôle de l’annuaire d’erreurs est \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="07c8f-281"><span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**ERROR\_DS\_CONTROL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-282">8258 (0x2042)</span><span class="sxs-lookup"><span data-stu-id="07c8f-282">8258 (0x2042)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-283">Le contrôle spécifié n’est pas pris en charge par le serveur.</span><span class="sxs-lookup"><span data-stu-id="07c8f-283">The specified control is not supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-284"><span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**ERREUR \_ de \_ boucle du client DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-284"><span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**ERROR\_DS\_CLIENT\_LOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-285">8259 (0x2043)</span><span class="sxs-lookup"><span data-stu-id="07c8f-285">8259 (0x2043)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-286">Une boucle de référence a été détectée par le client.</span><span class="sxs-lookup"><span data-stu-id="07c8f-286">A referral loop was detected by the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-287"><span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**ERREUR \_ de \_ \_ dépassement de la limite de référence DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-287"><span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**ERROR\_DS\_REFERRAL\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-288">8260 (0x2044)</span><span class="sxs-lookup"><span data-stu-id="07c8f-288">8260 (0x2044)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-289">La limite de référence prédéfinie a été dépassée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-289">The preset referral limit was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-290"><span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**ERREUR de \_ contrôle de tri des services d’annuaire \_ \_ \_ manquante**</span><span class="sxs-lookup"><span data-stu-id="07c8f-290"><span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**ERROR\_DS\_SORT\_CONTROL\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-291">8261 (0x2045)</span><span class="sxs-lookup"><span data-stu-id="07c8f-291">8261 (0x2045)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-292">La recherche requiert un contrôle SORT.</span><span class="sxs-lookup"><span data-stu-id="07c8f-292">The search requires a SORT control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-293"><span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**erreur d’erreur de \_ \_ plage de décalage DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-293"><span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**ERROR\_DS\_OFFSET\_RANGE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-294">8262 (0x2046)</span><span class="sxs-lookup"><span data-stu-id="07c8f-294">8262 (0x2046)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-295">Les résultats de la recherche dépassent la plage de décalage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-295">The search results exceed the offset range specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-296"><span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**ERREUR \_ DS \_ RIDMGR \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="07c8f-296"><span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**ERROR\_DS\_RIDMGR\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-297">8263 (0x2047)</span><span class="sxs-lookup"><span data-stu-id="07c8f-297">8263 (0x2047)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-298">Le service d’annuaire a détecté que le sous-système qui alloue des identificateurs relatifs est désactivé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-298">The directory service detected the subsystem that allocates relative identifiers is disabled.</span></span> <span data-ttu-id="07c8f-299">Cela peut se produire comme un mécanisme de protection lorsque le système détermine qu’une partie importante des identificateurs relatifs (RID) est épuisée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-299">This can occur as a protective mechanism when the system determines a significant portion of relative identifiers (RIDs) have been exhausted.</span></span> <span data-ttu-id="07c8f-300">Pour connaître <https://go.microsoft.com/fwlink/p/?linkid=228610> les étapes de diagnostic recommandées et la procédure à suivre pour réactiver la création de comptes, consultez.</span><span class="sxs-lookup"><span data-stu-id="07c8f-300">Please see <https://go.microsoft.com/fwlink/p/?linkid=228610> for recommended diagnostic steps and the procedure to re-enable account creation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-301"><span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**l’erreur la \_ \_ racine DS \_ doit \_ être \_ NC**</span><span class="sxs-lookup"><span data-stu-id="07c8f-301"><span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**ERROR\_DS\_ROOT\_MUST\_BE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-302">8301 (0x206D)</span><span class="sxs-lookup"><span data-stu-id="07c8f-302">8301 (0x206D)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-303">L’objet racine doit être le début d’un contexte d’appellation.</span><span class="sxs-lookup"><span data-stu-id="07c8f-303">The root object must be the head of a naming context.</span></span> <span data-ttu-id="07c8f-304">L’objet racine ne peut pas avoir de parent instancié.</span><span class="sxs-lookup"><span data-stu-id="07c8f-304">The root object cannot have an instantiated parent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-305"><span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**ERREUR d’ajout d’un \_ réplica au DS d’erreurs \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-305"><span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**ERROR\_DS\_ADD\_REPLICA\_INHIBITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-306">8302 (0x206E)</span><span class="sxs-lookup"><span data-stu-id="07c8f-306">8302 (0x206E)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-307">Impossible d’effectuer l’opération d’ajout de réplica.</span><span class="sxs-lookup"><span data-stu-id="07c8f-307">The add replica operation cannot be performed.</span></span> <span data-ttu-id="07c8f-308">Le contexte d’appellation doit être accessible en écriture pour pouvoir créer le réplica.</span><span class="sxs-lookup"><span data-stu-id="07c8f-308">The naming context must be writeable in order to create the replica.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-309"><span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**ERREUR \_ DS \_ att \_ non \_ Def \_ dans le \_ schéma**</span><span class="sxs-lookup"><span data-stu-id="07c8f-309"><span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**ERROR\_DS\_ATT\_NOT\_DEF\_IN\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-310">8303 (0x206F)</span><span class="sxs-lookup"><span data-stu-id="07c8f-310">8303 (0x206F)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-311">Une référence à un attribut qui n’est pas défini dans le schéma s’est produite.</span><span class="sxs-lookup"><span data-stu-id="07c8f-311">A reference to an attribute that is not defined in the schema occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-312"><span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**ERREUR de dépassement de la \_ \_ taille maximale du \_ obj DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-312"><span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**ERROR\_DS\_MAX\_OBJ\_SIZE\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-313">8304 (0x2070)</span><span class="sxs-lookup"><span data-stu-id="07c8f-313">8304 (0x2070)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-314">La taille maximale d’un objet a été dépassée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-314">The maximum size of an object has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-315"><span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**le nom de la chaîne de l’erreur \_ DS \_ obj \_ \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="07c8f-315"><span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**ERROR\_DS\_OBJ\_STRING\_NAME\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-316">8305 (0x2071)</span><span class="sxs-lookup"><span data-stu-id="07c8f-316">8305 (0x2071)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-317">Une tentative a été effectuée pour ajouter un objet au répertoire avec un nom qui est déjà en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="07c8f-317">An attempt was made to add an object to the directory with a name that is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-318"><span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**ERREUR \_ DS \_ non \_ RDN \_ définie \_ dans le \_ schéma**</span><span class="sxs-lookup"><span data-stu-id="07c8f-318"><span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**ERROR\_DS\_NO\_RDN\_DEFINED\_IN\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-319">8306 (0x2072)</span><span class="sxs-lookup"><span data-stu-id="07c8f-319">8306 (0x2072)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-320">Une tentative a été effectuée pour ajouter un objet d’une classe qui n’a pas de RDN défini dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="07c8f-320">An attempt was made to add an object of a class that does not have an RDN defined in the schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-321"><span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**ERREUR \_ DS \_ RDN ne pas \_ \_ correspondre au \_ schéma**</span><span class="sxs-lookup"><span data-stu-id="07c8f-321"><span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**ERROR\_DS\_RDN\_DOESNT\_MATCH\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-322">8307 (0x2073)</span><span class="sxs-lookup"><span data-stu-id="07c8f-322">8307 (0x2073)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-323">Une tentative d’ajout d’un objet à l’aide d’un RDN qui n’est pas le RDN défini dans le schéma a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-323">An attempt was made to add an object using an RDN that is not the RDN defined in the schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-324"><span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**ERREUR \_ DS \_ aucun \_ \_ ATTS demandé \_ trouvé**</span><span class="sxs-lookup"><span data-stu-id="07c8f-324"><span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**ERROR\_DS\_NO\_REQUESTED\_ATTS\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-325">8308 (0x2074)</span><span class="sxs-lookup"><span data-stu-id="07c8f-325">8308 (0x2074)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-326">Aucun des attributs requis n’a été trouvé sur les objets.</span><span class="sxs-lookup"><span data-stu-id="07c8f-326">None of the requested attributes were found on the objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-327"><span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**ERREUR \_ \_ \_ de mémoire tampon de l’utilisateur DS \_ \_ insuffisant**</span><span class="sxs-lookup"><span data-stu-id="07c8f-327"><span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**ERROR\_DS\_USER\_BUFFER\_TO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-328">8309 (0x2075)</span><span class="sxs-lookup"><span data-stu-id="07c8f-328">8309 (0x2075)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-329">La mémoire tampon de l’utilisateur est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="07c8f-329">The user buffer is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-330"><span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**l’erreur \_ DS \_ att \_ n’est \_ pas \_ sur \_ obj**</span><span class="sxs-lookup"><span data-stu-id="07c8f-330"><span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**ERROR\_DS\_ATT\_IS\_NOT\_ON\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-331">8310 (0x2076)</span><span class="sxs-lookup"><span data-stu-id="07c8f-331">8310 (0x2076)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-332">L’attribut spécifié dans l’opération n’est pas présent sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="07c8f-332">The attribute specified in the operation is not present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-333"><span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**ERREUR de l' \_ \_ \_ opération mod illégale DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-333"><span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**ERROR\_DS\_ILLEGAL\_MOD\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-334">8311 (0x2077)</span><span class="sxs-lookup"><span data-stu-id="07c8f-334">8311 (0x2077)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-335">Opération de modification non autorisée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-335">Illegal modify operation.</span></span> <span data-ttu-id="07c8f-336">Certains aspects de la modification ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="07c8f-336">Some aspect of the modification is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-337"><span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**ERREUR \_ DS \_ obj \_ trop \_ grande**</span><span class="sxs-lookup"><span data-stu-id="07c8f-337"><span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**ERROR\_DS\_OBJ\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-338">8312 (0x2078)</span><span class="sxs-lookup"><span data-stu-id="07c8f-338">8312 (0x2078)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-339">L’objet spécifié est trop grand.</span><span class="sxs-lookup"><span data-stu-id="07c8f-339">The specified object is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-340"><span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**ERREUR \_ de \_ \_ type d’instance incorrecte DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-340"><span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**ERROR\_DS\_BAD\_INSTANCE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-341">8313 (0x2079)</span><span class="sxs-lookup"><span data-stu-id="07c8f-341">8313 (0x2079)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-342">Le type d’instance spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="07c8f-342">The specified instance type is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-343"><span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**ERREUR \_ MASTERDSA de l’annuaire de services \_ \_ requise**</span><span class="sxs-lookup"><span data-stu-id="07c8f-343"><span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**ERROR\_DS\_MASTERDSA\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-344">8314 (0x207A)</span><span class="sxs-lookup"><span data-stu-id="07c8f-344">8314 (0x207A)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-345">L’opération doit être effectuée sur un DSA maître.</span><span class="sxs-lookup"><span data-stu-id="07c8f-345">The operation must be performed at a master DSA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-346"><span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**\_classe d' \_ objet Error DS \_ \_ obligatoire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-346"><span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**ERROR\_DS\_OBJECT\_CLASS\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-347">8315 (0x207B)</span><span class="sxs-lookup"><span data-stu-id="07c8f-347">8315 (0x207B)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-348">L’attribut de classe d’objet doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="07c8f-348">The object class attribute must be specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-349"><span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**erreur indiquant que le \_ service d’annuaire est \_ manquant \_ \_ ATT**</span><span class="sxs-lookup"><span data-stu-id="07c8f-349"><span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**ERROR\_DS\_MISSING\_REQUIRED\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-350">8316 (0x207C)</span><span class="sxs-lookup"><span data-stu-id="07c8f-350">8316 (0x207C)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-351">Un attribut requis est manquant.</span><span class="sxs-lookup"><span data-stu-id="07c8f-351">A required attribute is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-352"><span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**ERREUR \_ DS \_ att \_ non \_ Def \_ pour la \_ classe**</span><span class="sxs-lookup"><span data-stu-id="07c8f-352"><span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**ERROR\_DS\_ATT\_NOT\_DEF\_FOR\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-353">8317 (0x207D)</span><span class="sxs-lookup"><span data-stu-id="07c8f-353">8317 (0x207D)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-354">Une tentative de modification d’un objet pour inclure un attribut qui n’est pas légal pour sa classe a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-354">An attempt was made to modify an object to include an attribute that is not legal for its class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-355"><span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**l' \_ erreur \_ DS \_ att \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="07c8f-355"><span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**ERROR\_DS\_ATT\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-356">8318 (0x207E)</span><span class="sxs-lookup"><span data-stu-id="07c8f-356">8318 (0x207E)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-357">L’attribut spécifié est déjà présent sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="07c8f-357">The specified attribute is already present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-358"><span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**ERREUR \_ DS \_ Impossible d' \_ Ajouter des \_ \_ valeurs ATT**</span><span class="sxs-lookup"><span data-stu-id="07c8f-358"><span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**ERROR\_DS\_CANT\_ADD\_ATT\_VALUES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-359">8320 (0x2080)</span><span class="sxs-lookup"><span data-stu-id="07c8f-359">8320 (0x2080)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-360">L’attribut spécifié n’est pas présent ou n’a pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="07c8f-360">The specified attribute is not present, or has no values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-361"><span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**ERREUR \_ de \_ \_ contrainte de valeur unique \_ de l’annuaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-361"><span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**ERROR\_DS\_SINGLE\_VALUE\_CONSTRAINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-362">8321 (0x2081)</span><span class="sxs-lookup"><span data-stu-id="07c8f-362">8321 (0x2081)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-363">Plusieurs valeurs ont été spécifiées pour un attribut qui ne peut avoir qu’une seule valeur.</span><span class="sxs-lookup"><span data-stu-id="07c8f-363">Multiple values were specified for an attribute that can have only one value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-364"><span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**ERREUR \_ de \_ contrainte de plage DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-364"><span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**ERROR\_DS\_RANGE\_CONSTRAINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-365">8322 (0x2082)</span><span class="sxs-lookup"><span data-stu-id="07c8f-365">8322 (0x2082)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-366">Une valeur pour l’attribut n’était pas dans la plage de valeurs acceptable.</span><span class="sxs-lookup"><span data-stu-id="07c8f-366">A value for the attribute was not in the acceptable range of values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-367"><span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**l' \_ erreur \_ DS \_ att \_ Val \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="07c8f-367"><span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**ERROR\_DS\_ATT\_VAL\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-368">8323 (0x2083)</span><span class="sxs-lookup"><span data-stu-id="07c8f-368">8323 (0x2083)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-369">La valeur spécifiée existe déjà.</span><span class="sxs-lookup"><span data-stu-id="07c8f-369">The specified value already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-370"><span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**ERREUR DS inversion \_ \_ \_ REM \_ manquant \_ ATT**</span><span class="sxs-lookup"><span data-stu-id="07c8f-370"><span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**ERROR\_DS\_CANT\_REM\_MISSING\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-371">8324 (0x2084)</span><span class="sxs-lookup"><span data-stu-id="07c8f-371">8324 (0x2084)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-372">Impossible de supprimer l’attribut, car il n’est pas présent sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="07c8f-372">The attribute cannot be removed because it is not present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-373"><span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**erreur Impossible de trouver une erreur dans \_ DS \_ \_ \_ \_ \_ Val**</span><span class="sxs-lookup"><span data-stu-id="07c8f-373"><span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**ERROR\_DS\_CANT\_REM\_MISSING\_ATT\_VAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-374">8325 (0x2085)</span><span class="sxs-lookup"><span data-stu-id="07c8f-374">8325 (0x2085)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-375">La valeur de l’attribut ne peut pas être supprimée, car elle n’est pas présente sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="07c8f-375">The attribute value cannot be removed because it is not present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-376"><span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**ERREUR \_ la \_ racine \_ DS \_ ne peut pas être \_ SUBREF**</span><span class="sxs-lookup"><span data-stu-id="07c8f-376"><span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**ERROR\_DS\_ROOT\_CANT\_BE\_SUBREF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-377">8326 (0x2086)</span><span class="sxs-lookup"><span data-stu-id="07c8f-377">8326 (0x2086)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-378">L’objet racine spécifié ne peut pas être un subref.</span><span class="sxs-lookup"><span data-stu-id="07c8f-378">The specified root object cannot be a subref.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-379"><span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**ERREUR de chaînage du service d' \_ annuaire \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-379"><span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**ERROR\_DS\_NO\_CHAINING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-380">8327 (0x2087)</span><span class="sxs-lookup"><span data-stu-id="07c8f-380">8327 (0x2087)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-381">Le chaînage n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-381">Chaining is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-382"><span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**ERREUR \_ DS \_ sans \_ chaîne \_ eval**</span><span class="sxs-lookup"><span data-stu-id="07c8f-382"><span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**ERROR\_DS\_NO\_CHAINED\_EVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-383">8328 (0x2088)</span><span class="sxs-lookup"><span data-stu-id="07c8f-383">8328 (0x2088)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-384">L’évaluation chaînée n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-384">Chained evaluation is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-385"><span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**ERREUR \_ DS \_ aucun \_ \_ objet parent**</span><span class="sxs-lookup"><span data-stu-id="07c8f-385"><span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**ERROR\_DS\_NO\_PARENT\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-386">8329 (0x2089)</span><span class="sxs-lookup"><span data-stu-id="07c8f-386">8329 (0x2089)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-387">L'opération n'a pas pu être effectuée car le parent de l'objet n'est pas instancié ou a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-387">The operation could not be performed because the object's parent is either uninstantiated or deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-388"><span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**ERREUR \_ le \_ parent DS \_ est \_ un \_ alias**</span><span class="sxs-lookup"><span data-stu-id="07c8f-388"><span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**ERROR\_DS\_PARENT\_IS\_AN\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-389">8330 (0x208A)</span><span class="sxs-lookup"><span data-stu-id="07c8f-389">8330 (0x208A)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-390">Le fait de disposer d’un parent qui est un alias n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-390">Having a parent that is an alias is not permitted.</span></span> <span data-ttu-id="07c8f-391">Les alias sont des objets feuilles.</span><span class="sxs-lookup"><span data-stu-id="07c8f-391">Aliases are leaf objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-392"><span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**ERREUR \_ de combinaison du maître d’erreurs DS \_ \_ \_ \_ et des \_ représentants**</span><span class="sxs-lookup"><span data-stu-id="07c8f-392"><span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**ERROR\_DS\_CANT\_MIX\_MASTER\_AND\_REPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-393">8331 (0x208B)</span><span class="sxs-lookup"><span data-stu-id="07c8f-393">8331 (0x208B)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-394">L’objet et le parent doivent être du même type, qu’il s’agisse de maîtres ou de deux réplicas.</span><span class="sxs-lookup"><span data-stu-id="07c8f-394">The object and parent must be of the same type, either both masters or both replicas.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-395"><span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**ERREUR \_ les \_ enfants DS \_ existent**</span><span class="sxs-lookup"><span data-stu-id="07c8f-395"><span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**ERROR\_DS\_CHILDREN\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-396">8332 (0x208C)</span><span class="sxs-lookup"><span data-stu-id="07c8f-396">8332 (0x208C)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-397">Impossible d’effectuer l’opération, car des objets enfants existent.</span><span class="sxs-lookup"><span data-stu-id="07c8f-397">The operation cannot be performed because child objects exist.</span></span> <span data-ttu-id="07c8f-398">Cette opération ne peut être effectuée que sur un objet feuille.</span><span class="sxs-lookup"><span data-stu-id="07c8f-398">This operation can only be performed on a leaf object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-399"><span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**ERREUR \_ DS \_ obj \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="07c8f-399"><span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**ERROR\_DS\_OBJ\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-400">8333 (0x208D)</span><span class="sxs-lookup"><span data-stu-id="07c8f-400">8333 (0x208D)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-401">Objet répertoire introuvable.</span><span class="sxs-lookup"><span data-stu-id="07c8f-401">Directory object not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-402"><span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**\_obj avec alias DS d’erreur \_ \_ \_ manquant**</span><span class="sxs-lookup"><span data-stu-id="07c8f-402"><span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**ERROR\_DS\_ALIASED\_OBJ\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-403">8334 (0x208E)</span><span class="sxs-lookup"><span data-stu-id="07c8f-403">8334 (0x208E)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-404">L’objet avec alias est manquant.</span><span class="sxs-lookup"><span data-stu-id="07c8f-404">The aliased object is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-405"><span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**ERREUR \_ de \_ \_ syntaxe de nom incorrect DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-405"><span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**ERROR\_DS\_BAD\_NAME\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-406">8335 (0x208F)</span><span class="sxs-lookup"><span data-stu-id="07c8f-406">8335 (0x208F)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-407">La syntaxe du nom de l’objet est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="07c8f-407">The object name has bad syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-408"><span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**l' \_ \_ alias \_ d’erreur \_ du service d’annuaire pointe vers l' \_ alias**</span><span class="sxs-lookup"><span data-stu-id="07c8f-408"><span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**ERROR\_DS\_ALIAS\_POINTS\_TO\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-409">8336 (0x2090)</span><span class="sxs-lookup"><span data-stu-id="07c8f-409">8336 (0x2090)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-410">Un alias ne peut pas faire référence à un autre alias.</span><span class="sxs-lookup"><span data-stu-id="07c8f-410">It is not permitted for an alias to refer to another alias.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-411"><span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**ERREUR DS inverse \_ \_ \_ Deref \_ alias**</span><span class="sxs-lookup"><span data-stu-id="07c8f-411"><span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**ERROR\_DS\_CANT\_DEREF\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-412">8337 (0x2091)</span><span class="sxs-lookup"><span data-stu-id="07c8f-412">8337 (0x2091)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-413">L’alias ne peut pas être déréférencé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-413">The alias cannot be dereferenced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-414"><span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**ERREUR \_ \_ du service \_ d’annuaire hors de l' \_ étendue**</span><span class="sxs-lookup"><span data-stu-id="07c8f-414"><span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**ERROR\_DS\_OUT\_OF\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-415">8338 (0x2092)</span><span class="sxs-lookup"><span data-stu-id="07c8f-415">8338 (0x2092)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-416">L’opération est hors de portée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-416">The operation is out of scope.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-417"><span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**ERREUR de suppression de l' \_ \_ objet DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-417"><span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**ERROR\_DS\_OBJECT\_BEING\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-418">8339 (0x2093)</span><span class="sxs-lookup"><span data-stu-id="07c8f-418">8339 (0x2093)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-419">L’opération ne peut pas continuer, car l’objet est en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="07c8f-419">The operation cannot continue because the object is in the process of being removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-420"><span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**ERREUR \_ DS \_ Impossible de \_ supprimer le \_ DSA \_ obj**</span><span class="sxs-lookup"><span data-stu-id="07c8f-420"><span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**ERROR\_DS\_CANT\_DELETE\_DSA\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-421">8340 (0x2094)</span><span class="sxs-lookup"><span data-stu-id="07c8f-421">8340 (0x2094)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-422">Impossible de supprimer l’objet DSA.</span><span class="sxs-lookup"><span data-stu-id="07c8f-422">The DSA object cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-423"><span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**erreur \_ générique de l’annuaire de services \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-423"><span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**ERROR\_DS\_GENERIC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-424">8341 (0x2095)</span><span class="sxs-lookup"><span data-stu-id="07c8f-424">8341 (0x2095)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-425">Une erreur de service d’annuaire s’est produite.</span><span class="sxs-lookup"><span data-stu-id="07c8f-425">A directory service error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-426"><span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**l’erreur le \_ \_ DSA DS \_ doit \_ être de \_ type int \_ maître**</span><span class="sxs-lookup"><span data-stu-id="07c8f-426"><span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**ERROR\_DS\_DSA\_MUST\_BE\_INT\_MASTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-427">8342 (0x2096)</span><span class="sxs-lookup"><span data-stu-id="07c8f-427">8342 (0x2096)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-428">L’opération ne peut être effectuée que sur un objet DSA maître interne.</span><span class="sxs-lookup"><span data-stu-id="07c8f-428">The operation can only be performed on an internal master DSA object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-429"><span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**ERREUR de \_ classe de service d’annuaire \_ \_ non \_ DSA**</span><span class="sxs-lookup"><span data-stu-id="07c8f-429"><span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**ERROR\_DS\_CLASS\_NOT\_DSA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-430">8343 (0x2097)</span><span class="sxs-lookup"><span data-stu-id="07c8f-430">8343 (0x2097)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-431">L’objet doit être de type DSA.</span><span class="sxs-lookup"><span data-stu-id="07c8f-431">The object must be of class DSA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-432"><span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**\_droits d' \_ \_ accès insuff \_ des erreurs DS**</span><span class="sxs-lookup"><span data-stu-id="07c8f-432"><span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**ERROR\_DS\_INSUFF\_ACCESS\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-433">8344 (0x2098)</span><span class="sxs-lookup"><span data-stu-id="07c8f-433">8344 (0x2098)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-434">Droits d’accès insuffisants pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="07c8f-434">Insufficient access rights to perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-435"><span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**ERREUR \_ DS \_ non conforme \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-435"><span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**ERROR\_DS\_ILLEGAL\_SUPERIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-436">8345 (0x2099)</span><span class="sxs-lookup"><span data-stu-id="07c8f-436">8345 (0x2099)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-437">Impossible d’ajouter l’objet, car le parent ne figure pas dans la liste des supérieurs possibles.</span><span class="sxs-lookup"><span data-stu-id="07c8f-437">The object cannot be added because the parent is not on the list of possible superiors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-438"><span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**ERREUR \_ \_ d’attribut DS \_ appartenant \_ à \_ Sam**</span><span class="sxs-lookup"><span data-stu-id="07c8f-438"><span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**ERROR\_DS\_ATTRIBUTE\_OWNED\_BY\_SAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-439">8346 (0x209A)</span><span class="sxs-lookup"><span data-stu-id="07c8f-439">8346 (0x209A)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-440">L’accès à l’attribut n’est pas autorisé, car l’attribut appartient au gestionnaire de comptes de sécurité (SAM).</span><span class="sxs-lookup"><span data-stu-id="07c8f-440">Access to the attribute is not permitted because the attribute is owned by the Security Accounts Manager (SAM).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-441"><span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**ERREUR \_ nom du service d’annuaire \_ \_ trop \_ grand nombre de \_ parties**</span><span class="sxs-lookup"><span data-stu-id="07c8f-441"><span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**ERROR\_DS\_NAME\_TOO\_MANY\_PARTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-442">8347 (0x209B)</span><span class="sxs-lookup"><span data-stu-id="07c8f-442">8347 (0x209B)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-443">Le nom comporte un trop grand nombre de parties.</span><span class="sxs-lookup"><span data-stu-id="07c8f-443">The name has too many parts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-444"><span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**ERREUR \_ nom du service d’annuaire \_ \_ trop \_ long**</span><span class="sxs-lookup"><span data-stu-id="07c8f-444"><span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**ERROR\_DS\_NAME\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-445">8348 (0x209C)</span><span class="sxs-lookup"><span data-stu-id="07c8f-445">8348 (0x209C)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-446">Le nom est trop long.</span><span class="sxs-lookup"><span data-stu-id="07c8f-446">The name is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-447"><span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**ERREUR de \_ nom de service d’annuaire \_ \_ \_ trop \_ longue**</span><span class="sxs-lookup"><span data-stu-id="07c8f-447"><span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**ERROR\_DS\_NAME\_VALUE\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-448">8349 (0x209D)</span><span class="sxs-lookup"><span data-stu-id="07c8f-448">8349 (0x209D)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-449">La valeur de nom est trop longue.</span><span class="sxs-lookup"><span data-stu-id="07c8f-449">The name value is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-450"><span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**ERREUR de \_ nom de service d’annuaire non \_ \_ analysable**</span><span class="sxs-lookup"><span data-stu-id="07c8f-450"><span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**ERROR\_DS\_NAME\_UNPARSEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-451">8350 (0x209E)</span><span class="sxs-lookup"><span data-stu-id="07c8f-451">8350 (0x209E)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-452">Le service d’annuaire a rencontré une erreur lors de l’analyse d’un nom.</span><span class="sxs-lookup"><span data-stu-id="07c8f-452">The directory service encountered an error parsing a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-453"><span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**ERREUR de \_ type de nom de service d’annuaire \_ \_ \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="07c8f-453"><span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**ERROR\_DS\_NAME\_TYPE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-454">8351 (0x209F)</span><span class="sxs-lookup"><span data-stu-id="07c8f-454">8351 (0x209F)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-455">Le service d’annuaire ne peut pas obtenir le type d’attribut d’un nom.</span><span class="sxs-lookup"><span data-stu-id="07c8f-455">The directory service cannot get the attribute type for a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-456"><span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**ERREUR \_ DS \_ n’est pas \_ un \_ objet**</span><span class="sxs-lookup"><span data-stu-id="07c8f-456"><span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**ERROR\_DS\_NOT\_AN\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-457">8352 (0x20A0)</span><span class="sxs-lookup"><span data-stu-id="07c8f-457">8352 (0x20A0)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-458">Le nom n’identifie pas un objet ; le nom identifie un fantôme.</span><span class="sxs-lookup"><span data-stu-id="07c8f-458">The name does not identify an object; the name identifies a phantom.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-459"><span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**Erreur Description de l’erreur \_ DS \_ sec \_ \_ trop \_ brève**</span><span class="sxs-lookup"><span data-stu-id="07c8f-459"><span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**ERROR\_DS\_SEC\_DESC\_TOO\_SHORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-460">8353 (0x20A1)</span><span class="sxs-lookup"><span data-stu-id="07c8f-460">8353 (0x20A1)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-461">Le descripteur de sécurité est trop petit.</span><span class="sxs-lookup"><span data-stu-id="07c8f-461">The security descriptor is too short.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-462"><span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**ERREUR de \_ Description du service d’annuaire \_ sec \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="07c8f-462"><span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**ERROR\_DS\_SEC\_DESC\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-463">8354 (0x20A2)</span><span class="sxs-lookup"><span data-stu-id="07c8f-463">8354 (0x20A2)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-464">Le descripteur de sécurité n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="07c8f-464">The security descriptor is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-465"><span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**ERREUR \_ DS \_ no \_ Deleted \_ Name**</span><span class="sxs-lookup"><span data-stu-id="07c8f-465"><span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**ERROR\_DS\_NO\_DELETED\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-466">8355 (0x20A3)</span><span class="sxs-lookup"><span data-stu-id="07c8f-466">8355 (0x20A3)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-467">Impossible de créer le nom de l’objet supprimé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-467">Failed to create name for deleted object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-468"><span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**l' \_ erreur \_ SUBREF DS \_ doit \_ avoir le \_ parent**</span><span class="sxs-lookup"><span data-stu-id="07c8f-468"><span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**ERROR\_DS\_SUBREF\_MUST\_HAVE\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-469">8356 (0x20A4)</span><span class="sxs-lookup"><span data-stu-id="07c8f-469">8356 (0x20A4)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-470">Le parent d’un nouveau subref doit exister.</span><span class="sxs-lookup"><span data-stu-id="07c8f-470">The parent of a new subref must exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-471"><span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**l’erreur le \_ NCName du DS \_ \_ doit \_ être \_ NC**</span><span class="sxs-lookup"><span data-stu-id="07c8f-471"><span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**ERROR\_DS\_NCNAME\_MUST\_BE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-472">8357 (0x20A5)</span><span class="sxs-lookup"><span data-stu-id="07c8f-472">8357 (0x20A5)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-473">L’objet doit être un contexte d’appellation.</span><span class="sxs-lookup"><span data-stu-id="07c8f-473">The object must be a naming context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-474"><span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**ERREUR \_ DS \_ Impossible d' \_ Ajouter le \_ système \_ uniquement**</span><span class="sxs-lookup"><span data-stu-id="07c8f-474"><span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**ERROR\_DS\_CANT\_ADD\_SYSTEM\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-475">8358 (0x20A6)</span><span class="sxs-lookup"><span data-stu-id="07c8f-475">8358 (0x20A6)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-476">L’ajout d’un attribut détenu par le système n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-476">It is not permitted to add an attribute which is owned by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-477"><span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**la classe de l’erreur \_ DS \_ \_ doit \_ être \_ concrète**</span><span class="sxs-lookup"><span data-stu-id="07c8f-477"><span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**ERROR\_DS\_CLASS\_MUST\_BE\_CONCRETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-478">8359 (0x20A7)</span><span class="sxs-lookup"><span data-stu-id="07c8f-478">8359 (0x20A7)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-479">La classe de l’objet doit être structurelle ; vous ne pouvez pas instancier une classe abstraite.</span><span class="sxs-lookup"><span data-stu-id="07c8f-479">The class of the object must be structural; you cannot instantiate an abstract class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-480"><span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**ERREUR de la \_ \_ DMD non valide du DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-480"><span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**ERROR\_DS\_INVALID\_DMD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-481">8360 (0x20A8)</span><span class="sxs-lookup"><span data-stu-id="07c8f-481">8360 (0x20A8)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-482">L’objet de schéma est introuvable.</span><span class="sxs-lookup"><span data-stu-id="07c8f-482">The schema object could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-483"><span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**le \_ GUID obj du DS d’erreur \_ \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="07c8f-483"><span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**ERROR\_DS\_OBJ\_GUID\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-484">8361 (0x20A9)</span><span class="sxs-lookup"><span data-stu-id="07c8f-484">8361 (0x20A9)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-485">Un objet local avec ce GUID (Dead ou Alive) existe déjà.</span><span class="sxs-lookup"><span data-stu-id="07c8f-485">A local object with this GUID (dead or alive) already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-486"><span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**ERREUR \_ DS \_ non \_ sur \_ lien secondaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-486"><span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**ERROR\_DS\_NOT\_ON\_BACKLINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-487">8362 (0x20AA)</span><span class="sxs-lookup"><span data-stu-id="07c8f-487">8362 (0x20AA)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-488">L’opération ne peut pas être effectuée sur un lien précédent.</span><span class="sxs-lookup"><span data-stu-id="07c8f-488">The operation cannot be performed on a back link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-489"><span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**ERREUR \_ DS \_ no \_ CROSSREF \_ pour \_ NC**</span><span class="sxs-lookup"><span data-stu-id="07c8f-489"><span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**ERROR\_DS\_NO\_CROSSREF\_FOR\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-490">8363 (0x20AB)</span><span class="sxs-lookup"><span data-stu-id="07c8f-490">8363 (0x20AB)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-491">La référence croisée pour le contexte d’appellation spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="07c8f-491">The cross reference for the specified naming context could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-492"><span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**ERREUR d' \_ arrêt du service d’annuaire \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-492"><span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**ERROR\_DS\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-493">8364 (0x20AC)</span><span class="sxs-lookup"><span data-stu-id="07c8f-493">8364 (0x20AC)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-494">L’opération n’a pas pu être effectuée car le service d’annuaire est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="07c8f-494">The operation could not be performed because the directory service is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-495"><span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**ERREUR de l' \_ \_ \_ opération inconnue de l’annuaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-495"><span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**ERROR\_DS\_UNKNOWN\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-496">8365 (0x20AD)</span><span class="sxs-lookup"><span data-stu-id="07c8f-496">8365 (0x20AD)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-497">La demande du service d’annuaire n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="07c8f-497">The directory service request is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-498"><span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**ERREUR \_ DS \_ \_ propriétaire du rôle non valide \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-498"><span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**ERROR\_DS\_INVALID\_ROLE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-499">8366 (0x20AE)</span><span class="sxs-lookup"><span data-stu-id="07c8f-499">8366 (0x20AE)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-500">Impossible de lire l’attribut propriétaire du rôle.</span><span class="sxs-lookup"><span data-stu-id="07c8f-500">The role owner attribute could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-501"><span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**ERREUR \_ \_ impossible du \_ contact du service d’annuaire \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-501"><span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**ERROR\_DS\_COULDNT\_CONTACT\_FSMO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-502">8367 (0x20AF)</span><span class="sxs-lookup"><span data-stu-id="07c8f-502">8367 (0x20AF)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-503">L'opération FSMO demandée a échoué.</span><span class="sxs-lookup"><span data-stu-id="07c8f-503">The requested FSMO operation failed.</span></span> <span data-ttu-id="07c8f-504">Le propriétaire FSMO actuel n'a pas pu être contacté.</span><span class="sxs-lookup"><span data-stu-id="07c8f-504">The current FSMO holder could not be contacted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-505"><span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**ERREUR \_ de \_ changement \_ de \_ nom du DN Cross NC \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-505"><span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**ERROR\_DS\_CROSS\_NC\_DN\_RENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-506">8368 (0x20B0)</span><span class="sxs-lookup"><span data-stu-id="07c8f-506">8368 (0x20B0)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-507">La modification d’un DN dans un contexte d’appellation n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-507">Modification of a DN across a naming context is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-508"><span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**ERREUR DS inverser \_ \_ \_ \_ système \_ uniquement**</span><span class="sxs-lookup"><span data-stu-id="07c8f-508"><span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**ERROR\_DS\_CANT\_MOD\_SYSTEM\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-509">8369 (0x20B1)</span><span class="sxs-lookup"><span data-stu-id="07c8f-509">8369 (0x20B1)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-510">L’attribut ne peut pas être modifié, car il appartient au système.</span><span class="sxs-lookup"><span data-stu-id="07c8f-510">The attribute cannot be modified because it is owned by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-511"><span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**ERREUR \_ du \_ réplicateur DS \_ uniquement**</span><span class="sxs-lookup"><span data-stu-id="07c8f-511"><span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**ERROR\_DS\_REPLICATOR\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-512">8370 (0x20B2)</span><span class="sxs-lookup"><span data-stu-id="07c8f-512">8370 (0x20B2)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-513">Seul le réplicateur peut exécuter cette fonction.</span><span class="sxs-lookup"><span data-stu-id="07c8f-513">Only the replicator can perform this function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-514"><span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**ERREUR \_ de \_ classe obj du DS \_ \_ non \_ définie**</span><span class="sxs-lookup"><span data-stu-id="07c8f-514"><span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**ERROR\_DS\_OBJ\_CLASS\_NOT\_DEFINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-515">8371 (0x20B3)</span><span class="sxs-lookup"><span data-stu-id="07c8f-515">8371 (0x20B3)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-516">La classe spécifiée n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="07c8f-516">The specified class is not defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-517"><span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**ERREUR \_ de \_ \_ classe \_ non sous- \_ classe obj de l’annuaire d’annuaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-517"><span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**ERROR\_DS\_OBJ\_CLASS\_NOT\_SUBCLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-518">8372 (0x20B4)</span><span class="sxs-lookup"><span data-stu-id="07c8f-518">8372 (0x20B4)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-519">La classe spécifiée n’est pas une sous-classe.</span><span class="sxs-lookup"><span data-stu-id="07c8f-519">The specified class is not a subclass.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-520"><span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**ERREUR de \_ référence de nom de service d’annuaire \_ \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="07c8f-520"><span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**ERROR\_DS\_NAME\_REFERENCE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-521">8373 (0x20B5)</span><span class="sxs-lookup"><span data-stu-id="07c8f-521">8373 (0x20B5)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-522">La référence de nom n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="07c8f-522">The name reference is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-523"><span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**ERREUR \_ de \_ référence croisée DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-523"><span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**ERROR\_DS\_CROSS\_REF\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-524">8374 (0x20B6)</span><span class="sxs-lookup"><span data-stu-id="07c8f-524">8374 (0x20B6)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-525">Une référence croisée existe déjà.</span><span class="sxs-lookup"><span data-stu-id="07c8f-525">A cross reference already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-526"><span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**ERREUR DS ne dispose pas de l' \_ \_ \_ \_ \_ CROSSREF maître**</span><span class="sxs-lookup"><span data-stu-id="07c8f-526"><span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**ERROR\_DS\_CANT\_DEL\_MASTER\_CROSSREF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-527">8375 (0x20B7)</span><span class="sxs-lookup"><span data-stu-id="07c8f-527">8375 (0x20B7)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-528">La suppression d’une référence croisée principale n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-528">It is not permitted to delete a master cross reference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-529"><span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**ERREUR de notification de la \_ \_ \_ sous-arborescence DS \_ non \_ \_ -en-tête**</span><span class="sxs-lookup"><span data-stu-id="07c8f-529"><span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**ERROR\_DS\_SUBTREE\_NOTIFY\_NOT\_NC\_HEAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-530">8376 (0x20B8)</span><span class="sxs-lookup"><span data-stu-id="07c8f-530">8376 (0x20B8)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-531">Les notifications de sous-arborescence sont uniquement prises en charge sur les têtes NC.</span><span class="sxs-lookup"><span data-stu-id="07c8f-531">Subtree notifications are only supported on NC heads.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-532"><span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**ERREUR de \_ filtre de notification du service d’annuaire \_ \_ \_ trop \_ complexe**</span><span class="sxs-lookup"><span data-stu-id="07c8f-532"><span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**ERROR\_DS\_NOTIFY\_FILTER\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-533">8377 (0x20B9)</span><span class="sxs-lookup"><span data-stu-id="07c8f-533">8377 (0x20B9)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-534">Le filtre de notification est trop complexe.</span><span class="sxs-lookup"><span data-stu-id="07c8f-534">Notification filter is too complex.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-535"><span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**ERREUR du RDN du service d' \_ annuaire \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-535"><span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**ERROR\_DS\_DUP\_RDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-536">8378 (0x20BA)</span><span class="sxs-lookup"><span data-stu-id="07c8f-536">8378 (0x20BA)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-537">Échec de la mise à jour du schéma : RDN dupliqué.</span><span class="sxs-lookup"><span data-stu-id="07c8f-537">Schema update failed: duplicate RDN.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-538"><span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**ERREUR \_ d' \_ OID DUP du DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-538"><span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**ERROR\_DS\_DUP\_OID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-539">8379 (0x20BB)</span><span class="sxs-lookup"><span data-stu-id="07c8f-539">8379 (0x20BB)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-540">Échec de la mise à jour du schéma : OID dupliqué.</span><span class="sxs-lookup"><span data-stu-id="07c8f-540">Schema update failed: duplicate OID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-541"><span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**\_ \_ \_ ID MAPI DUP \_ de l’erreur DS**</span><span class="sxs-lookup"><span data-stu-id="07c8f-541"><span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**ERROR\_DS\_DUP\_MAPI\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-542">8380 (0x20BC)</span><span class="sxs-lookup"><span data-stu-id="07c8f-542">8380 (0x20BC)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-543">Échec de la mise à jour du schéma : identificateur MAPI dupliqué.</span><span class="sxs-lookup"><span data-stu-id="07c8f-543">Schema update failed: duplicate MAPI identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-544"><span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**ERREUR \_ GUID de l’ID de \_ schéma DUP du DS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-544"><span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**ERROR\_DS\_DUP\_SCHEMA\_ID\_GUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-545">8381 (0x20BD)</span><span class="sxs-lookup"><span data-stu-id="07c8f-545">8381 (0x20BD)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-546">Échec de la mise à jour du schéma : GUID de l’ID de schéma dupliqué.</span><span class="sxs-lookup"><span data-stu-id="07c8f-546">Schema update failed: duplicate schema-id GUID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-547"><span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**ERREUR \_ \_ \_ \_ nom complet LDAP DUP du DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-547"><span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**ERROR\_DS\_DUP\_LDAP\_DISPLAY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-548">8382 (0x20BE)</span><span class="sxs-lookup"><span data-stu-id="07c8f-548">8382 (0x20BE)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-549">Échec de la mise à jour du schéma : nom complet LDAP dupliqué.</span><span class="sxs-lookup"><span data-stu-id="07c8f-549">Schema update failed: duplicate LDAP display name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-550"><span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**ERREUR du test de la \_ \_ sémantique \_ att DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-550"><span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**ERROR\_DS\_SEMANTIC\_ATT\_TEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-551">8383 (0x20BF)</span><span class="sxs-lookup"><span data-stu-id="07c8f-551">8383 (0x20BF)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-552">Échec de la mise à jour du schéma : plage inférieure à la plage supérieure à la plage supérieure.</span><span class="sxs-lookup"><span data-stu-id="07c8f-552">Schema update failed: range-lower less than range upper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-553"><span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**ERREUR \_ d' \_ incompatibilité de syntaxe DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-553"><span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**ERROR\_DS\_SYNTAX\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-554">8384 (0x20C0)</span><span class="sxs-lookup"><span data-stu-id="07c8f-554">8384 (0x20C0)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-555">Échec de la mise à jour du schéma : incompatibilité de syntaxe.</span><span class="sxs-lookup"><span data-stu-id="07c8f-555">Schema update failed: syntax mismatch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-556"><span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**\_l’erreur DS \_ existe \_ dans \_ doit \_ avoir**</span><span class="sxs-lookup"><span data-stu-id="07c8f-556"><span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**ERROR\_DS\_EXISTS\_IN\_MUST\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-557">8385 (0x20C1)</span><span class="sxs-lookup"><span data-stu-id="07c8f-557">8385 (0x20C1)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-558">Échec de la suppression du schéma : l’attribut est utilisé dans la doit contenir.</span><span class="sxs-lookup"><span data-stu-id="07c8f-558">Schema deletion failed: attribute is used in must-contain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-559"><span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**\_l’erreur \_ DS \_ existe \_ peut- \_ être**</span><span class="sxs-lookup"><span data-stu-id="07c8f-559"><span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**ERROR\_DS\_EXISTS\_IN\_MAY\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-560">8386 (0x20C2)</span><span class="sxs-lookup"><span data-stu-id="07c8f-560">8386 (0x20C2)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-561">Échec de la suppression du schéma : l’attribut est utilisé dans la relation contenant-contenu.</span><span class="sxs-lookup"><span data-stu-id="07c8f-561">Schema deletion failed: attribute is used in may-contain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-562"><span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**l’erreur \_ DS \_ inexistant \_ peut \_ avoir**</span><span class="sxs-lookup"><span data-stu-id="07c8f-562"><span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**ERROR\_DS\_NONEXISTENT\_MAY\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-563">8387 (0x20C3)</span><span class="sxs-lookup"><span data-stu-id="07c8f-563">8387 (0x20C3)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-564">Échec de la mise à jour du schéma : l’attribut dans peut contenir n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="07c8f-564">Schema update failed: attribute in may-contain does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-565"><span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**l’erreur \_ DS \_ inexistant \_ doit \_ avoir**</span><span class="sxs-lookup"><span data-stu-id="07c8f-565"><span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**ERROR\_DS\_NONEXISTENT\_MUST\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-566">8388 (0x20C4)</span><span class="sxs-lookup"><span data-stu-id="07c8f-566">8388 (0x20C4)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-567">Échec de la mise à jour du schéma : l’attribut dans doit contenir n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="07c8f-567">Schema update failed: attribute in must-contain does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-568"><span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**ERREUR \_ échec du test DS aux \_ \_ CLS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-568"><span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**ERROR\_DS\_AUX\_CLS\_TEST\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-569">8389 (0x20C5)</span><span class="sxs-lookup"><span data-stu-id="07c8f-569">8389 (0x20C5)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-570">Échec de la mise à jour du schéma : la classe dans la liste des classes auxiliaires n’existe pas ou n’est pas une classe auxiliaire.</span><span class="sxs-lookup"><span data-stu-id="07c8f-570">Schema update failed: class in aux-class list does not exist or is not an auxiliary class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-571"><span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**ERREUR d' \_ annuaire \_ \_ poss inexistant \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-571"><span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**ERROR\_DS\_NONEXISTENT\_POSS\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-572">8390 (0x20C6)</span><span class="sxs-lookup"><span data-stu-id="07c8f-572">8390 (0x20C6)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-573">Échec de la mise à jour du schéma : la classe dans Poss-Superior n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="07c8f-573">Schema update failed: class in poss-superiors does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-574"><span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**ERREUR \_ \_ échec du test DS Sub \_ CLS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-574"><span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**ERROR\_DS\_SUB\_CLS\_TEST\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-575">8391 (0x20C7)</span><span class="sxs-lookup"><span data-stu-id="07c8f-575">8391 (0x20C7)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-576">Échec de la mise à jour du schéma : la classe dans la liste subclassof n’existe pas ou ne répond pas aux règles de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="07c8f-576">Schema update failed: class in subclassof list does not exist or does not satisfy hierarchy rules.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-577"><span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**ERREUR \_ DS \_ incorrecte, syntaxe de l' \_ \_ ID att att \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-577"><span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**ERROR\_DS\_BAD\_RDN\_ATT\_ID\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-578">8392 (0x20C8)</span><span class="sxs-lookup"><span data-stu-id="07c8f-578">8392 (0x20C8)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-579">Échec de la mise à jour du schéma : RDN-att-ID a une syntaxe incorrecte.</span><span class="sxs-lookup"><span data-stu-id="07c8f-579">Schema update failed: Rdn-Att-Id has wrong syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-580"><span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**\_l’erreur DS \_ existe \_ dans \_ \_ CLS**</span><span class="sxs-lookup"><span data-stu-id="07c8f-580"><span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**ERROR\_DS\_EXISTS\_IN\_AUX\_CLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-581">8393 (0x20C9)</span><span class="sxs-lookup"><span data-stu-id="07c8f-581">8393 (0x20C9)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-582">Échec de la suppression du schéma : la classe est utilisée comme classe auxiliaire.</span><span class="sxs-lookup"><span data-stu-id="07c8f-582">Schema deletion failed: class is used as auxiliary class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-583"><span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**\_l’erreur DS \_ existe dans la sous- \_ \_ \_ spécification CLS**</span><span class="sxs-lookup"><span data-stu-id="07c8f-583"><span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**ERROR\_DS\_EXISTS\_IN\_SUB\_CLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-584">8394 (0x20CA)</span><span class="sxs-lookup"><span data-stu-id="07c8f-584">8394 (0x20CA)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-585">Échec de la suppression du schéma : la classe est utilisée en tant que sous-classe.</span><span class="sxs-lookup"><span data-stu-id="07c8f-585">Schema deletion failed: class is used as sub class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-586"><span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**\_l’erreur DS \_ existe \_ dans \_ poss \_ sup**</span><span class="sxs-lookup"><span data-stu-id="07c8f-586"><span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**ERROR\_DS\_EXISTS\_IN\_POSS\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-587">8395 (0x20CB)</span><span class="sxs-lookup"><span data-stu-id="07c8f-587">8395 (0x20CB)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-588">Échec de la suppression du schéma : la classe est utilisée en tant que Poss Superior.</span><span class="sxs-lookup"><span data-stu-id="07c8f-588">Schema deletion failed: class is used as poss superior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-589"><span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**échec de l’RECALCSCHEMA de l’erreur \_ DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-589"><span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**ERROR\_DS\_RECALCSCHEMA\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-590">8396 (0x20CC)</span><span class="sxs-lookup"><span data-stu-id="07c8f-590">8396 (0x20CC)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-591">Échec de la mise à jour du schéma lors du recalcul du cache de validation.</span><span class="sxs-lookup"><span data-stu-id="07c8f-591">Schema update failed in recalculating validation cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-592"><span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**ERREUR de suppression de l' \_ arborescence du service d’annuaire \_ \_ \_ non \_ terminée**</span><span class="sxs-lookup"><span data-stu-id="07c8f-592"><span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**ERROR\_DS\_TREE\_DELETE\_NOT\_FINISHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-593">8397 (0x20CD)</span><span class="sxs-lookup"><span data-stu-id="07c8f-593">8397 (0x20CD)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-594">La suppression de l’arborescence n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-594">The tree deletion is not finished.</span></span> <span data-ttu-id="07c8f-595">La demande doit être réexécutée pour poursuivre la suppression de l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="07c8f-595">The request must be made again to continue deleting the tree.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-596"><span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**ERREUR \_ DS \_ Impossible de \_ Supprimer**</span><span class="sxs-lookup"><span data-stu-id="07c8f-596"><span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**ERROR\_DS\_CANT\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-597">8398 (0x20CE)</span><span class="sxs-lookup"><span data-stu-id="07c8f-597">8398 (0x20CE)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-598">Impossible d’effectuer l’opération de suppression demandée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-598">The requested delete operation could not be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-599"><span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**ERREUR de l’ID de la \_ \_ demande de schéma DS att \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-599"><span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**ERROR\_DS\_ATT\_SCHEMA\_REQ\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-600">8399 (0x20CF)</span><span class="sxs-lookup"><span data-stu-id="07c8f-600">8399 (0x20CF)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-601">Impossible de lire l’identificateur de classe gouvernes pour l’enregistrement de schéma.</span><span class="sxs-lookup"><span data-stu-id="07c8f-601">Cannot read the governs class identifier for the schema record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-602"><span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**ERREUR \_ de \_ \_ syntaxe de \_ schéma \_ att de l’annuaire de services**</span><span class="sxs-lookup"><span data-stu-id="07c8f-602"><span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**ERROR\_DS\_BAD\_ATT\_SCHEMA\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-603">8400 (0x20D0)</span><span class="sxs-lookup"><span data-stu-id="07c8f-603">8400 (0x20D0)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-604">La syntaxe du schéma d’attribut est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="07c8f-604">The attribute schema has bad syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-605"><span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**ERREUR \_ DS \_ Impossible de mettre \_ en cache \_ ATT**</span><span class="sxs-lookup"><span data-stu-id="07c8f-605"><span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**ERROR\_DS\_CANT\_CACHE\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-606">8401 (0x20D1)</span><span class="sxs-lookup"><span data-stu-id="07c8f-606">8401 (0x20D1)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-607">L’attribut n’a pas pu être mis en cache.</span><span class="sxs-lookup"><span data-stu-id="07c8f-607">The attribute could not be cached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-608"><span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**ERREUR \_ de \_ \_ classe de cache du service DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-608"><span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**ERROR\_DS\_CANT\_CACHE\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-609">8402 (0x20D2)</span><span class="sxs-lookup"><span data-stu-id="07c8f-609">8402 (0x20D2)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-610">La classe n’a pas pu être mise en cache.</span><span class="sxs-lookup"><span data-stu-id="07c8f-610">The class could not be cached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-611"><span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**ERREUR \_ DS \_ Impossible de \_ supprimer le \_ \_ cache ATT**</span><span class="sxs-lookup"><span data-stu-id="07c8f-611"><span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**ERROR\_DS\_CANT\_REMOVE\_ATT\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-612">8403 (0x20D3)</span><span class="sxs-lookup"><span data-stu-id="07c8f-612">8403 (0x20D3)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-613">L’attribut n’a pas pu être supprimé du cache.</span><span class="sxs-lookup"><span data-stu-id="07c8f-613">The attribute could not be removed from the cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-614"><span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**ERREUR \_ DS \_ Impossible de \_ supprimer le \_ cache de classe \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-614"><span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**ERROR\_DS\_CANT\_REMOVE\_CLASS\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-615">8404 (0x20D4)</span><span class="sxs-lookup"><span data-stu-id="07c8f-615">8404 (0x20D4)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-616">La classe n’a pas pu être supprimée du cache.</span><span class="sxs-lookup"><span data-stu-id="07c8f-616">The class could not be removed from the cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-617"><span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**ERREUR \_ DS \_ Impossible de \_ récupérer le \_ DN**</span><span class="sxs-lookup"><span data-stu-id="07c8f-617"><span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**ERROR\_DS\_CANT\_RETRIEVE\_DN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-618">8405 (0x20D5)</span><span class="sxs-lookup"><span data-stu-id="07c8f-618">8405 (0x20D5)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-619">L’attribut de nom unique n’a pas pu être lu.</span><span class="sxs-lookup"><span data-stu-id="07c8f-619">The distinguished name attribute could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-620"><span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**ERREUR \_ \_ SUPREF manquante du service d’annuaire \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-620"><span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**ERROR\_DS\_MISSING\_SUPREF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-621">8406 (0x20D6)</span><span class="sxs-lookup"><span data-stu-id="07c8f-621">8406 (0x20D6)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-622">Aucun renvoi supérieur n'a été configuré pour le service d'annuaire.</span><span class="sxs-lookup"><span data-stu-id="07c8f-622">No superior reference has been configured for the directory service.</span></span> <span data-ttu-id="07c8f-623">Le service d'annuaire n'est donc pas en mesure d'émettre des renvois vers des objets situés en dehors de cette forêt.</span><span class="sxs-lookup"><span data-stu-id="07c8f-623">The directory service is therefore unable to issue referrals to objects outside this forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-624"><span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**ERREUR \_ DS \_ Impossible de \_ récupérer l' \_ instance**</span><span class="sxs-lookup"><span data-stu-id="07c8f-624"><span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**ERROR\_DS\_CANT\_RETRIEVE\_INSTANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-625">8407 (0x20D7)</span><span class="sxs-lookup"><span data-stu-id="07c8f-625">8407 (0x20D7)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-626">L’attribut de type d’instance n’a pas pu être récupéré.</span><span class="sxs-lookup"><span data-stu-id="07c8f-626">The instance type attribute could not be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-627"><span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**ERREUR \_ d' \_ incohérence de code DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-627"><span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**ERROR\_DS\_CODE\_INCONSISTENCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-628">8408 (0x20D8)</span><span class="sxs-lookup"><span data-stu-id="07c8f-628">8408 (0x20D8)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-629">Une erreur interne s'est produite.</span><span class="sxs-lookup"><span data-stu-id="07c8f-629">An internal error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-630"><span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**erreur \_ \_ de base de données DS Error \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-630"><span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**ERROR\_DS\_DATABASE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-631">8409 (0x20D9)</span><span class="sxs-lookup"><span data-stu-id="07c8f-631">8409 (0x20D9)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-632">Une erreur de base de données s’est produite.</span><span class="sxs-lookup"><span data-stu-id="07c8f-632">A database error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-633"><span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**ERREUR \_ de \_ governsID DS \_ manquante**</span><span class="sxs-lookup"><span data-stu-id="07c8f-633"><span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**ERROR\_DS\_GOVERNSID\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-634">8410 (0x20DA)</span><span class="sxs-lookup"><span data-stu-id="07c8f-634">8410 (0x20DA)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-635">L’attribut GOVERNSID est manquant.</span><span class="sxs-lookup"><span data-stu-id="07c8f-635">The attribute GOVERNSID is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-636"><span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**erreur indiquant que le \_ DS est \_ manquant \_ \_ ATT**</span><span class="sxs-lookup"><span data-stu-id="07c8f-636"><span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**ERROR\_DS\_MISSING\_EXPECTED\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-637">8411 (0x20DB)</span><span class="sxs-lookup"><span data-stu-id="07c8f-637">8411 (0x20DB)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-638">Un attribut attendu est manquant.</span><span class="sxs-lookup"><span data-stu-id="07c8f-638">An expected attribute is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-639"><span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**ERREUR du NCName de la \_ DM du service DS \_ \_ manquant \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-639"><span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**ERROR\_DS\_NCNAME\_MISSING\_CR\_REF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-640">8412 (0x20DC)</span><span class="sxs-lookup"><span data-stu-id="07c8f-640">8412 (0x20DC)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-641">Il manque une référence croisée dans le contexte d’appellation spécifié.</span><span class="sxs-lookup"><span data-stu-id="07c8f-641">The specified naming context is missing a cross reference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-642"><span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**erreur de vérification de la \_ sécurité du service d’annuaire \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-642"><span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**ERROR\_DS\_SECURITY\_CHECKING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-643">8413 (0x20DD)</span><span class="sxs-lookup"><span data-stu-id="07c8f-643">8413 (0x20DD)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-644">Une erreur de vérification de la sécurité s’est produite.</span><span class="sxs-lookup"><span data-stu-id="07c8f-644">A security checking error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-645"><span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**ERREUR de chargement du schéma du service d' \_ annuaire \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-645"><span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**ERROR\_DS\_SCHEMA\_NOT\_LOADED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-646">8414 (0x20DE)</span><span class="sxs-lookup"><span data-stu-id="07c8f-646">8414 (0x20DE)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-647">Le schéma n’est pas chargé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-647">The schema is not loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-648"><span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**ERREUR \_ échec de l’allocation du \_ schéma DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-648"><span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**ERROR\_DS\_SCHEMA\_ALLOC\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-649">8415 (0x20DF)</span><span class="sxs-lookup"><span data-stu-id="07c8f-649">8415 (0x20DF)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-650">Échec de l’allocation du schéma.</span><span class="sxs-lookup"><span data-stu-id="07c8f-650">Schema allocation failed.</span></span> <span data-ttu-id="07c8f-651">Vérifiez que la mémoire est insuffisante sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="07c8f-651">Please check if the machine is running low on memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-652"><span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**ERREUR de syntaxe de la \_ \_ demande de schéma DS att \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-652"><span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**ERROR\_DS\_ATT\_SCHEMA\_REQ\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-653">8416 (0x20E0)</span><span class="sxs-lookup"><span data-stu-id="07c8f-653">8416 (0x20E0)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-654">Échec de l’obtention de la syntaxe requise pour le schéma d’attribut.</span><span class="sxs-lookup"><span data-stu-id="07c8f-654">Failed to obtain the required syntax for the attribute schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-655"><span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**erreur de \_ GCVERIFY du service d’annuaire \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-655"><span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**ERROR\_DS\_GCVERIFY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-656">8417 (0x20E1)</span><span class="sxs-lookup"><span data-stu-id="07c8f-656">8417 (0x20E1)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-657">Échec de la vérification du catalogue global.</span><span class="sxs-lookup"><span data-stu-id="07c8f-657">The global catalog verification failed.</span></span> <span data-ttu-id="07c8f-658">Le catalogue global n’est pas disponible ou ne prend pas en charge l’opération.</span><span class="sxs-lookup"><span data-stu-id="07c8f-658">The global catalog is not available or does not support the operation.</span></span> <span data-ttu-id="07c8f-659">Une partie du répertoire n’est pas disponible actuellement.</span><span class="sxs-lookup"><span data-stu-id="07c8f-659">Some part of the directory is currently not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-660"><span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**ERREUR \_ d' \_ \_ incompatibilité de schéma DRA de l’annuaire \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-660"><span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**ERROR\_DS\_DRA\_SCHEMA\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-661">8418 (0x20E2)</span><span class="sxs-lookup"><span data-stu-id="07c8f-661">8418 (0x20E2)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-662">L’opération de réplication a échoué en raison d’une incompatibilité de schéma entre les serveurs impliqués.</span><span class="sxs-lookup"><span data-stu-id="07c8f-662">The replication operation failed because of a schema mismatch between the servers involved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-663"><span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**ERREUR \_ DS \_ Impossible de \_ trouver \_ DSA \_ obj**</span><span class="sxs-lookup"><span data-stu-id="07c8f-663"><span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**ERROR\_DS\_CANT\_FIND\_DSA\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-664">8419 (0x20E3)</span><span class="sxs-lookup"><span data-stu-id="07c8f-664">8419 (0x20E3)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-665">L’objet DSA est introuvable.</span><span class="sxs-lookup"><span data-stu-id="07c8f-665">The DSA object could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-666"><span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**ERREUR \_ \_ Impossible de \_ trouver le \_ contexte de nommage DS attendu \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-666"><span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**ERROR\_DS\_CANT\_FIND\_EXPECTED\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-667">8420 (0x20E4)</span><span class="sxs-lookup"><span data-stu-id="07c8f-667">8420 (0x20E4)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-668">Le contexte d’appellation est introuvable.</span><span class="sxs-lookup"><span data-stu-id="07c8f-668">The naming context could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-669"><span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**ERREUR \_ DS \_ Impossible \_ de trouver le \_ contexte \_ de nommage dans le \_ cache**</span><span class="sxs-lookup"><span data-stu-id="07c8f-669"><span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**ERROR\_DS\_CANT\_FIND\_NC\_IN\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-670">8421 (0x20E5)</span><span class="sxs-lookup"><span data-stu-id="07c8f-670">8421 (0x20E5)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-671">Le contexte d’appellation est introuvable dans le cache.</span><span class="sxs-lookup"><span data-stu-id="07c8f-671">The naming context could not be found in the cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-672"><span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**ERREUR \_ DS \_ Impossible de \_ récupérer l' \_ enfant**</span><span class="sxs-lookup"><span data-stu-id="07c8f-672"><span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**ERROR\_DS\_CANT\_RETRIEVE\_CHILD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-673">8422 (0x20E6)</span><span class="sxs-lookup"><span data-stu-id="07c8f-673">8422 (0x20E6)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-674">Impossible de récupérer l’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="07c8f-674">The child object could not be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-675"><span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**ERREUR \_ de \_ \_ modification non conforme de la sécurité DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-675"><span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**ERROR\_DS\_SECURITY\_ILLEGAL\_MODIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-676">8423 (0x20E7)</span><span class="sxs-lookup"><span data-stu-id="07c8f-676">8423 (0x20E7)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-677">La modification n’a pas été autorisée pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="07c8f-677">The modification was not permitted for security reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-678"><span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**ERREUR \_ DS \_ Impossible de \_ remplacer le \_ \_ Rapp masqué**</span><span class="sxs-lookup"><span data-stu-id="07c8f-678"><span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**ERROR\_DS\_CANT\_REPLACE\_HIDDEN\_REC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-679">8424 (0x20E8)</span><span class="sxs-lookup"><span data-stu-id="07c8f-679">8424 (0x20E8)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-680">L’opération ne peut pas remplacer l’enregistrement masqué.</span><span class="sxs-lookup"><span data-stu-id="07c8f-680">The operation cannot replace the hidden record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-681"><span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**ERREUR \_ du \_ \_ fichier de hiérarchie incorrecte DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-681"><span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**ERROR\_DS\_BAD\_HIERARCHY\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-682">8425 (0x20E9)</span><span class="sxs-lookup"><span data-stu-id="07c8f-682">8425 (0x20E9)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-683">Le fichier de hiérarchie n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="07c8f-683">The hierarchy file is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-684"><span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**ERREUR lors de la table de la \_ \_ hiérarchie de génération DS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-684"><span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**ERROR\_DS\_BUILD\_HIERARCHY\_TABLE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-685">8426 (0x20EA)</span><span class="sxs-lookup"><span data-stu-id="07c8f-685">8426 (0x20EA)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-686">Échec de la tentative de création de la table de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="07c8f-686">The attempt to build the hierarchy table failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-687"><span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**paramètre de configuration de l’annuaire d’erreurs \_ \_ \_ \_ manquant**</span><span class="sxs-lookup"><span data-stu-id="07c8f-687"><span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**ERROR\_DS\_CONFIG\_PARAM\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-688">8427 (0x20EB)</span><span class="sxs-lookup"><span data-stu-id="07c8f-688">8427 (0x20EB)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-689">Le paramètre de configuration de répertoire est manquant dans le registre.</span><span class="sxs-lookup"><span data-stu-id="07c8f-689">The directory configuration parameter is missing from the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-690"><span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**ERREUR \_ de \_ comptage \_ des \_ indices AB du service d’annuaire \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-690"><span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**ERROR\_DS\_COUNTING\_AB\_INDICES\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-691">8428 (0x20EC)</span><span class="sxs-lookup"><span data-stu-id="07c8f-691">8428 (0x20EC)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-692">La tentative de compter les index du carnet d’adresses a échoué.</span><span class="sxs-lookup"><span data-stu-id="07c8f-692">The attempt to count the address book indices failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-693"><span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**ERREUR d’échec de malloc de la table de \_ hiérarchie des services d’annuaire \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-693"><span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**ERROR\_DS\_HIERARCHY\_TABLE\_MALLOC\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-694">8429 (0x20ED)</span><span class="sxs-lookup"><span data-stu-id="07c8f-694">8429 (0x20ED)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-695">Échec de l’allocation de la table de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="07c8f-695">The allocation of the hierarchy table failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-696"><span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**ERREUR \_ interne de l’annuaire de services \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-696"><span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**ERROR\_DS\_INTERNAL\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-697">8430 (0x20EE)</span><span class="sxs-lookup"><span data-stu-id="07c8f-697">8430 (0x20EE)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-698">Le service d’annuaire a rencontré une erreur interne.</span><span class="sxs-lookup"><span data-stu-id="07c8f-698">The directory service encountered an internal failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-699"><span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**erreur \_ DS erreur \_ inconnue \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-699"><span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**ERROR\_DS\_UNKNOWN\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-700">8431 (0x20EF)</span><span class="sxs-lookup"><span data-stu-id="07c8f-700">8431 (0x20EF)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-701">Le service d’annuaire a rencontré une erreur inconnue.</span><span class="sxs-lookup"><span data-stu-id="07c8f-701">The directory service encountered an unknown failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-702"><span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**la racine de l’erreur \_ DS \_ requiert la \_ \_ classe \_ Top**</span><span class="sxs-lookup"><span data-stu-id="07c8f-702"><span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**ERROR\_DS\_ROOT\_REQUIRES\_CLASS\_TOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-703">8432 (0x20F0)</span><span class="sxs-lookup"><span data-stu-id="07c8f-703">8432 (0x20F0)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-704">Un objet racine requiert une classe de’Top'.</span><span class="sxs-lookup"><span data-stu-id="07c8f-704">A root object requires a class of 'top'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-705"><span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**ERREUR \_ de \_ refus des \_ \_ rôles FSMO pour le service d’annuaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-705"><span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**ERROR\_DS\_REFUSING\_FSMO\_ROLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-706">8433 (0x20F1)</span><span class="sxs-lookup"><span data-stu-id="07c8f-706">8433 (0x20F1)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-707">Ce serveur d’annuaire est en cours d’arrêt et ne peut pas prendre possession de nouveaux rôles d’opérations à maître unique flottant.</span><span class="sxs-lookup"><span data-stu-id="07c8f-707">This directory server is shutting down, and cannot take ownership of new floating single-master operation roles.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-708"><span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**\_ \_ paramètres FSMO manquants de \_ l’erreur DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-708"><span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**ERROR\_DS\_MISSING\_FSMO\_SETTINGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-709">8434 (0x20F2)</span><span class="sxs-lookup"><span data-stu-id="07c8f-709">8434 (0x20F2)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-710">Les informations de configuration obligatoires sont manquantes dans le service d’annuaire et il est impossible de déterminer la propriété des rôles d’opérations à maître unique flottant.</span><span class="sxs-lookup"><span data-stu-id="07c8f-710">The directory service is missing mandatory configuration information, and is unable to determine the ownership of floating single-master operation roles.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-711"><span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**ERREUR \_ DS \_ Impossible \_ de \_ renoncer aux \_ rôles**</span><span class="sxs-lookup"><span data-stu-id="07c8f-711"><span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**ERROR\_DS\_UNABLE\_TO\_SURRENDER\_ROLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-712">8435 (0x20F3)</span><span class="sxs-lookup"><span data-stu-id="07c8f-712">8435 (0x20F3)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-713">Le service d’annuaire n’a pas pu transférer la propriété d’un ou plusieurs rôles d’opérations à maître unique flottants à d’autres serveurs.</span><span class="sxs-lookup"><span data-stu-id="07c8f-713">The directory service was unable to transfer ownership of one or more floating single-master operation roles to other servers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-714"><span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**ERREUR \_ \_ générique DRA de l’annuaire \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-714"><span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**ERROR\_DS\_DRA\_GENERIC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-715">8436 (0x20F4)</span><span class="sxs-lookup"><span data-stu-id="07c8f-715">8436 (0x20F4)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-716">L’opération de réplication a échoué.</span><span class="sxs-lookup"><span data-stu-id="07c8f-716">The replication operation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-717"><span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**ERREUR \_ du \_ \_ paramètre DRA non valide du service d’annuaire \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-717"><span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**ERROR\_DS\_DRA\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-718">8437 (0x20F5)</span><span class="sxs-lookup"><span data-stu-id="07c8f-718">8437 (0x20F5)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-719">Un paramètre non valide a été spécifié pour cette opération de réplication.</span><span class="sxs-lookup"><span data-stu-id="07c8f-719">An invalid parameter was specified for this replication operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-720"><span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**ERREUR \_ \_ DRA \_ occupée**</span><span class="sxs-lookup"><span data-stu-id="07c8f-720"><span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**ERROR\_DS\_DRA\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-721">8438 (0x20F6)</span><span class="sxs-lookup"><span data-stu-id="07c8f-721">8438 (0x20F6)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-722">Le service d’annuaire est trop occupé pour terminer l’opération de réplication pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="07c8f-722">The directory service is too busy to complete the replication operation at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-723"><span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**ERREUR \_ de \_ \_ DN DRA incorrecte du DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-723"><span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**ERROR\_DS\_DRA\_BAD\_DN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-724">8439 (0x20F7)</span><span class="sxs-lookup"><span data-stu-id="07c8f-724">8439 (0x20F7)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-725">Le nom unique spécifié pour cette opération de réplication n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="07c8f-725">The distinguished name specified for this replication operation is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-726"><span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**ERREUR \_ \_ NC DRA \_ Bad \_ NC**</span><span class="sxs-lookup"><span data-stu-id="07c8f-726"><span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**ERROR\_DS\_DRA\_BAD\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-727">8440 (0x20F8)</span><span class="sxs-lookup"><span data-stu-id="07c8f-727">8440 (0x20F8)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-728">Le contexte d’appellation spécifié pour cette opération de réplication n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="07c8f-728">The naming context specified for this replication operation is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-729"><span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**ERREUR \_ de \_ \_ nom de domaine DRA \_ de l’annuaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-729"><span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**ERROR\_DS\_DRA\_DN\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-730">8441 (0x20F9)</span><span class="sxs-lookup"><span data-stu-id="07c8f-730">8441 (0x20F9)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-731">Le nom unique spécifié pour cette opération de réplication existe déjà.</span><span class="sxs-lookup"><span data-stu-id="07c8f-731">The distinguished name specified for this replication operation already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-732"><span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**erreur \_ \_ interne de DRA DRA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-732"><span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**ERROR\_DS\_DRA\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-733">8442 (0x20FA)</span><span class="sxs-lookup"><span data-stu-id="07c8f-733">8442 (0x20FA)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-734">Le système de réplication a rencontré une erreur interne.</span><span class="sxs-lookup"><span data-stu-id="07c8f-734">The replication system encountered an internal error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-735"><span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**ERREUR \_ \_ DRA non \_ cohérente du DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-735"><span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**ERROR\_DS\_DRA\_INCONSISTENT\_DIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-736">8443 (0x20FB)</span><span class="sxs-lookup"><span data-stu-id="07c8f-736">8443 (0x20FB)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-737">L’opération de réplication a rencontré une incohérence de base de données.</span><span class="sxs-lookup"><span data-stu-id="07c8f-737">The replication operation encountered a database inconsistency.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-738"><span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**ERREUR \_ échec de la \_ \_ connexion DRA \_ de l’annuaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-738"><span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**ERROR\_DS\_DRA\_CONNECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-739">8444 (0x20FC)</span><span class="sxs-lookup"><span data-stu-id="07c8f-739">8444 (0x20FC)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-740">Le serveur spécifié pour cette opération de réplication n’a pas pu être contacté.</span><span class="sxs-lookup"><span data-stu-id="07c8f-740">The server specified for this replication operation could not be contacted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-741"><span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**ERREUR \_ de \_ \_ type d' \_ instance incorrecte du DS DRA \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-741"><span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**ERROR\_DS\_DRA\_BAD\_INSTANCE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-742">8445 (0x20FD)</span><span class="sxs-lookup"><span data-stu-id="07c8f-742">8445 (0x20FD)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-743">L’opération de réplication a rencontré un objet avec un type d’instance non valide.</span><span class="sxs-lookup"><span data-stu-id="07c8f-743">The replication operation encountered an object with an invalid instance type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-744"><span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**ERREUR \_ \_ de l' \_ agent \_ de récupération de la \_ mémoire DS**</span><span class="sxs-lookup"><span data-stu-id="07c8f-744"><span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**ERROR\_DS\_DRA\_OUT\_OF\_MEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-745">8446 (0x20FE)</span><span class="sxs-lookup"><span data-stu-id="07c8f-745">8446 (0x20FE)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-746">L’opération de réplication n’a pas pu allouer de mémoire.</span><span class="sxs-lookup"><span data-stu-id="07c8f-746">The replication operation failed to allocate memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-747"><span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**ERREUR du \_ service de \_ \_ messages DRA \_ de l’erreur**</span><span class="sxs-lookup"><span data-stu-id="07c8f-747"><span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**ERROR\_DS\_DRA\_MAIL\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-748">8447 (0x20FF)</span><span class="sxs-lookup"><span data-stu-id="07c8f-748">8447 (0x20FF)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-749">L’opération de réplication a rencontré une erreur avec le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="07c8f-749">The replication operation encountered an error with the mail system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-750"><span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**l’erreur la \_ référence DRA de l’annuaire \_ \_ \_ \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="07c8f-750"><span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**ERROR\_DS\_DRA\_REF\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-751">8448 (0x2100)</span><span class="sxs-lookup"><span data-stu-id="07c8f-751">8448 (0x2100)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-752">Les informations de référence sur la réplication du serveur cible existent déjà.</span><span class="sxs-lookup"><span data-stu-id="07c8f-752">The replication reference information for the target server already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-753"><span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**ERREUR \_ de \_ \_ référence DRA \_ non \_ trouvée**</span><span class="sxs-lookup"><span data-stu-id="07c8f-753"><span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**ERROR\_DS\_DRA\_REF\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-754">8449 (0x2101)</span><span class="sxs-lookup"><span data-stu-id="07c8f-754">8449 (0x2101)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-755">Les informations de référence sur la réplication du serveur cible n’existent pas.</span><span class="sxs-lookup"><span data-stu-id="07c8f-755">The replication reference information for the target server does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-756"><span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**erreur la source DRA de l’annuaire d’erreurs \_ \_ \_ \_ est \_ REP \_ .**</span><span class="sxs-lookup"><span data-stu-id="07c8f-756"><span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**ERROR\_DS\_DRA\_OBJ\_IS\_REP\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-757">8450 (0x2102)</span><span class="sxs-lookup"><span data-stu-id="07c8f-757">8450 (0x2102)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-758">Impossible de supprimer le contexte d’appellation, car il est répliqué sur un autre serveur.</span><span class="sxs-lookup"><span data-stu-id="07c8f-758">The naming context cannot be removed because it is replicated to another server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-759"><span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**erreur \_ de \_ \_ base \_ de**</span><span class="sxs-lookup"><span data-stu-id="07c8f-759"><span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**ERROR\_DS\_DRA\_DB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-760">8451 (0x2103)</span><span class="sxs-lookup"><span data-stu-id="07c8f-760">8451 (0x2103)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-761">L’opération de réplication a rencontré une erreur de base de données.</span><span class="sxs-lookup"><span data-stu-id="07c8f-761">The replication operation encountered a database error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-762"><span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**ERREUR \_ \_ DRA \_ non \_ répliquée du service d’annuaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-762"><span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**ERROR\_DS\_DRA\_NO\_REPLICA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-763">8452 (0x2104)</span><span class="sxs-lookup"><span data-stu-id="07c8f-763">8452 (0x2104)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-764">Le contexte d’appellation est en cours de suppression ou n’est pas répliqué à partir du serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="07c8f-764">The naming context is in the process of being removed or is not replicated from the specified server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-765"><span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**ERREUR \_ de \_ refus d’accès DRA de \_ l’annuaire \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-765"><span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**ERROR\_DS\_DRA\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-766">8453 (0x2105)</span><span class="sxs-lookup"><span data-stu-id="07c8f-766">8453 (0x2105)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-767">L’accès à la réplication a été refusé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-767">Replication access was denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-768"><span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**ERREUR \_ \_ DRA \_ non \_ prise en charge**</span><span class="sxs-lookup"><span data-stu-id="07c8f-768"><span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**ERROR\_DS\_DRA\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-769">8454 (0x2106)</span><span class="sxs-lookup"><span data-stu-id="07c8f-769">8454 (0x2106)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-770">L’opération demandée n’est pas prise en charge par cette version du service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="07c8f-770">The requested operation is not supported by this version of the directory service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-771"><span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**ERREUR \_ \_ RPC DRA \_ \_ annulée**</span><span class="sxs-lookup"><span data-stu-id="07c8f-771"><span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**ERROR\_DS\_DRA\_RPC\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-772">8455 (0x2107)</span><span class="sxs-lookup"><span data-stu-id="07c8f-772">8455 (0x2107)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-773">L’appel de procédure distante de réplication a été annulé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-773">The replication remote procedure call was cancelled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-774"><span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**ERREUR \_ de \_ source DRA de l’annuaire \_ \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="07c8f-774"><span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**ERROR\_DS\_DRA\_SOURCE\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-775">8456 (0x2108)</span><span class="sxs-lookup"><span data-stu-id="07c8f-775">8456 (0x2108)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-776">Le serveur source rejette actuellement les demandes de réplication.</span><span class="sxs-lookup"><span data-stu-id="07c8f-776">The source server is currently rejecting replication requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-777"><span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**ERREUR du \_ récepteur DRA du service d’annuaire \_ \_ \_ désactivé**</span><span class="sxs-lookup"><span data-stu-id="07c8f-777"><span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**ERROR\_DS\_DRA\_SINK\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-778">8457 (0x2109)</span><span class="sxs-lookup"><span data-stu-id="07c8f-778">8457 (0x2109)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-779">Le serveur de destination rejette actuellement les demandes de réplication.</span><span class="sxs-lookup"><span data-stu-id="07c8f-779">The destination server is currently rejecting replication requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-780"><span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**ERREUR \_ de \_ \_ collision de nom DRA \_ de l’annuaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-780"><span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**ERROR\_DS\_DRA\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-781">8458 (0x210A)</span><span class="sxs-lookup"><span data-stu-id="07c8f-781">8458 (0x210A)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-782">L’opération de réplication a échoué en raison d’une collision de noms d’objets.</span><span class="sxs-lookup"><span data-stu-id="07c8f-782">The replication operation failed due to a collision of object names.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-783"><span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**ERREUR lors de la \_ RÉinstallation de la \_ source DRA DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-783"><span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**ERROR\_DS\_DRA\_SOURCE\_REINSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-784">8459 (0x210B)</span><span class="sxs-lookup"><span data-stu-id="07c8f-784">8459 (0x210B)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-785">La source de réplication a été réinstallée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-785">The replication source has been reinstalled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-786"><span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**ERREUR de l' \_ \_ absence du \_ parent du DRA \_ de l’annuaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-786"><span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**ERROR\_DS\_DRA\_MISSING\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-787">8460 (0x210C)</span><span class="sxs-lookup"><span data-stu-id="07c8f-787">8460 (0x210C)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-788">L’opération de réplication a échoué car un objet parent requis est manquant.</span><span class="sxs-lookup"><span data-stu-id="07c8f-788">The replication operation failed because a required parent object is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-789"><span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**ERREUR \_ \_ DRA en \_ préemption**</span><span class="sxs-lookup"><span data-stu-id="07c8f-789"><span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**ERROR\_DS\_DRA\_PREEMPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-790">8461 (0x210D)</span><span class="sxs-lookup"><span data-stu-id="07c8f-790">8461 (0x210D)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-791">L’opération de réplication a été préemptée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-791">The replication operation was preempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-792"><span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**ERREUR \_ de \_ \_ synchronisation des abandons DRA \_ de l’annuaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-792"><span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**ERROR\_DS\_DRA\_ABANDON\_SYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-793">8462 (0x210E)</span><span class="sxs-lookup"><span data-stu-id="07c8f-793">8462 (0x210E)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-794">La tentative de synchronisation de réplication a été abandonnée en raison d’un manque de mises à jour.</span><span class="sxs-lookup"><span data-stu-id="07c8f-794">The replication synchronization attempt was abandoned because of a lack of updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-795"><span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**ERREUR de l' \_ \_ arrêt DRA du DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-795"><span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**ERROR\_DS\_DRA\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-796">8463 (0x210F)</span><span class="sxs-lookup"><span data-stu-id="07c8f-796">8463 (0x210F)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-797">L’opération de réplication a été arrêtée car le système est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="07c8f-797">The replication operation was terminated because the system is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-798"><span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**ERREUR de l' \_ \_ \_ \_ ensemble partiel incompatible \_ de la DRA du DS**</span><span class="sxs-lookup"><span data-stu-id="07c8f-798"><span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**ERROR\_DS\_DRA\_INCOMPATIBLE\_PARTIAL\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-799">8464 (0x2110)</span><span class="sxs-lookup"><span data-stu-id="07c8f-799">8464 (0x2110)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-800">La tentative de synchronisation a échoué car le DC de destination attend actuellement de synchroniser de nouveaux attributs partiels à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="07c8f-800">Synchronization attempt failed because the destination DC is currently waiting to synchronize new partial attributes from source.</span></span> <span data-ttu-id="07c8f-801">Cette condition est normale si une modification récente du schéma a modifié l’ensemble des attributs partiels.</span><span class="sxs-lookup"><span data-stu-id="07c8f-801">This condition is normal if a recent schema change modified the partial attribute set.</span></span> <span data-ttu-id="07c8f-802">L’ensemble d’attributs partiels de destination n’est pas un sous-ensemble de l’ensemble d’attributs partiels source.</span><span class="sxs-lookup"><span data-stu-id="07c8f-802">The destination partial attribute set is not a subset of source partial attribute set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-803"><span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**ERREUR \_ la \_ source DRA du DS \_ est un \_ \_ \_ réplica partiel**</span><span class="sxs-lookup"><span data-stu-id="07c8f-803"><span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**ERROR\_DS\_DRA\_SOURCE\_IS\_PARTIAL\_REPLICA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-804">8465 (0x2111)</span><span class="sxs-lookup"><span data-stu-id="07c8f-804">8465 (0x2111)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-805">La tentative de synchronisation de la réplication a échoué car un réplica principal a tenté de se synchroniser à partir d’un réplica partiel.</span><span class="sxs-lookup"><span data-stu-id="07c8f-805">The replication synchronization attempt failed because a master replica attempted to sync from a partial replica.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-806"><span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**ERREUR \_ échec de la \_ \_ connexion DRA Extn \_ \_ de l’annuaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-806"><span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**ERROR\_DS\_DRA\_EXTN\_CONNECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-807">8466 (0x2112)</span><span class="sxs-lookup"><span data-stu-id="07c8f-807">8466 (0x2112)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-808">Le serveur spécifié pour cette opération de réplication a été contacté, mais ce serveur n’a pas pu contacter un serveur supplémentaire nécessaire pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="07c8f-808">The server specified for this replication operation was contacted, but that server was unable to contact an additional server needed to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-809"><span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**ERREUR \_ d' \_ \_ incompatibilité de schéma d’installation du service d’annuaire \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-809"><span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**ERROR\_DS\_INSTALL\_SCHEMA\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-810">8467 (0x2113)</span><span class="sxs-lookup"><span data-stu-id="07c8f-810">8467 (0x2113)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-811">La version du schéma du service d’annuaire de la forêt source n’est pas compatible avec la version du service d’annuaire sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="07c8f-811">The version of the directory service schema of the source forest is not compatible with the version of directory service on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-812"><span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**\_ID de \_ lien du doublon DS d' \_ erreur \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-812"><span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**ERROR\_DS\_DUP\_LINK\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-813">8468 (0x2114)</span><span class="sxs-lookup"><span data-stu-id="07c8f-813">8468 (0x2114)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-814">Échec de la mise à jour du schéma : un attribut avec le même identificateur de lien existe déjà.</span><span class="sxs-lookup"><span data-stu-id="07c8f-814">Schema update failed: An attribute with the same link identifier already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-815"><span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**ERREUR \_ de \_ \_ résolution des erreurs de nom du service d’annuaire \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-815"><span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**ERROR\_DS\_NAME\_ERROR\_RESOLVING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-816">8469 (0x2115)</span><span class="sxs-lookup"><span data-stu-id="07c8f-816">8469 (0x2115)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-817">Traduction de nom : erreur de traitement générique.</span><span class="sxs-lookup"><span data-stu-id="07c8f-817">Name translation: Generic processing error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-818"><span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**ERREUR de \_ nom du service d’annuaire \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="07c8f-818"><span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**ERROR\_DS\_NAME\_ERROR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-819">8470 (0x2116)</span><span class="sxs-lookup"><span data-stu-id="07c8f-819">8470 (0x2116)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-820">Traduction de nom : impossible de trouver le nom ou le droit insuffisant pour afficher le nom.</span><span class="sxs-lookup"><span data-stu-id="07c8f-820">Name translation: Could not find the name or insufficient right to see name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-821"><span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**erreur de \_ nom du service d’annuaire \_ \_ \_ non \_ unique**</span><span class="sxs-lookup"><span data-stu-id="07c8f-821"><span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**ERROR\_DS\_NAME\_ERROR\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-822">8471 (0x2117)</span><span class="sxs-lookup"><span data-stu-id="07c8f-822">8471 (0x2117)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-823">Traduction de nom : nom d’entrée mappé à plusieurs noms de sortie.</span><span class="sxs-lookup"><span data-stu-id="07c8f-823">Name translation: Input name mapped to more than one output name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-824"><span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**ERREUR de nom d’erreur de \_ nom de service d’annuaire \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-824"><span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**ERROR\_DS\_NAME\_ERROR\_NO\_MAPPING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-825">8472 (0x2118)</span><span class="sxs-lookup"><span data-stu-id="07c8f-825">8472 (0x2118)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-826">Traduction de nom : nom d’entrée trouvé, mais pas le format de sortie associé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-826">Name translation: Input name found, but not the associated output format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-827"><span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**ERREUR \_ \_ nom du \_ domaine d’erreur du nom \_ \_ de l’annuaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-827"><span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**ERROR\_DS\_NAME\_ERROR\_DOMAIN\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-828">8473 (0x2119)</span><span class="sxs-lookup"><span data-stu-id="07c8f-828">8473 (0x2119)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-829">Traduction de nom : impossible de résoudre complètement, seul le domaine a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-829">Name translation: Unable to resolve completely, only the domain was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-830"><span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**ERREUR de nom de l’annuaire d’erreurs \_ \_ \_ \_ sans \_ \_ mappage syntaxique**</span><span class="sxs-lookup"><span data-stu-id="07c8f-830"><span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**ERROR\_DS\_NAME\_ERROR\_NO\_SYNTACTICAL\_MAPPING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-831">8474 (0x211A)</span><span class="sxs-lookup"><span data-stu-id="07c8f-831">8474 (0x211A)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-832">Traduction de noms : impossible d’effectuer un mappage syntaxique purement incorrect au client sans passer par le câble.</span><span class="sxs-lookup"><span data-stu-id="07c8f-832">Name translation: Unable to perform purely syntactical mapping at the client without going out to the wire.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-833"><span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**ERREUR \_ de \_ \_ modification att \_ construite par DS**</span><span class="sxs-lookup"><span data-stu-id="07c8f-833"><span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**ERROR\_DS\_CONSTRUCTED\_ATT\_MOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-834">8475 (0x211B)</span><span class="sxs-lookup"><span data-stu-id="07c8f-834">8475 (0x211B)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-835">La modification d’un attribut construit n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-835">Modification of a constructed attribute is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-836"><span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**erreur \_ du \_ \_ modèle de \_ \_ classe obj de l’erreur DS incorrect**</span><span class="sxs-lookup"><span data-stu-id="07c8f-836"><span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**ERROR\_DS\_WRONG\_OM\_OBJ\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-837">8476 (0x211C)</span><span class="sxs-lookup"><span data-stu-id="07c8f-837">8476 (0x211C)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-838">La classe OM-Object-Class spécifiée est incorrecte pour un attribut avec la syntaxe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-838">The OM-Object-Class specified is incorrect for an attribute with the specified syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-839"><span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**ERREUR \_ de \_ \_ REPL DRA \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="07c8f-839"><span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**ERROR\_DS\_DRA\_REPL\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-840">8477 (0x211D)</span><span class="sxs-lookup"><span data-stu-id="07c8f-840">8477 (0x211D)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-841">La demande de réplication a été publiée ; en attente de réponse.</span><span class="sxs-lookup"><span data-stu-id="07c8f-841">The replication request has been posted; waiting for reply.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-842"><span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**ERREUR \_ DS \_ \_ obligatoire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-842"><span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**ERROR\_DS\_DS\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-843">8478 (0x211E)</span><span class="sxs-lookup"><span data-stu-id="07c8f-843">8478 (0x211E)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-844">L’opération demandée requiert un service d’annuaire et aucune n’était disponible.</span><span class="sxs-lookup"><span data-stu-id="07c8f-844">The requested operation requires a directory service, and none was available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-845"><span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**ERREUR \_ DS \_ \_ \_ nom complet LDAP non valide \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-845"><span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**ERROR\_DS\_INVALID\_LDAP\_DISPLAY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-846">8479 (0x211F)</span><span class="sxs-lookup"><span data-stu-id="07c8f-846">8479 (0x211F)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-847">Le nom complet LDAP de la classe ou de l’attribut contient des caractères non-ASCII.</span><span class="sxs-lookup"><span data-stu-id="07c8f-847">The LDAP display name of the class or attribute contains non-ASCII characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-848"><span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**ERREUR \_ DS \_ non \_ - \_ recherche de base**</span><span class="sxs-lookup"><span data-stu-id="07c8f-848"><span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**ERROR\_DS\_NON\_BASE\_SEARCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-849">8480 (0x2120)</span><span class="sxs-lookup"><span data-stu-id="07c8f-849">8480 (0x2120)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-850">L’opération de recherche demandée est uniquement prise en charge pour les recherches de base.</span><span class="sxs-lookup"><span data-stu-id="07c8f-850">The requested search operation is only supported for base searches.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-851"><span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**ERREUR \_ DS \_ Impossible de \_ récupérer \_ ATTS**</span><span class="sxs-lookup"><span data-stu-id="07c8f-851"><span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**ERROR\_DS\_CANT\_RETRIEVE\_ATTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-852">8481 (0x2121)</span><span class="sxs-lookup"><span data-stu-id="07c8f-852">8481 (0x2121)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-853">La recherche n’a pas pu récupérer les attributs de la base de données.</span><span class="sxs-lookup"><span data-stu-id="07c8f-853">The search failed to retrieve attributes from the database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-854"><span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**ERREUR \_ DS \_ lien secondaire \_ sans \_ lien**</span><span class="sxs-lookup"><span data-stu-id="07c8f-854"><span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**ERROR\_DS\_BACKLINK\_WITHOUT\_LINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-855">8482 (0x2122)</span><span class="sxs-lookup"><span data-stu-id="07c8f-855">8482 (0x2122)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-856">L’opération de mise à jour du schéma a tenté d’ajouter un attribut de lien ascendant qui n’a pas de lien de transfert correspondant.</span><span class="sxs-lookup"><span data-stu-id="07c8f-856">The schema update operation tried to add a backward link attribute that has no corresponding forward link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-857"><span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**ERREUR \_ d' \_ incompatibilité de l’époque du DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-857"><span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**ERROR\_DS\_EPOCH\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-858">8483 (0x2123)</span><span class="sxs-lookup"><span data-stu-id="07c8f-858">8483 (0x2123)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-859">La source et la destination d’un déplacement entre domaines ne sont pas d’accord sur le numéro de la époque de l’objet.</span><span class="sxs-lookup"><span data-stu-id="07c8f-859">Source and destination of a cross-domain move do not agree on the object's epoch number.</span></span> <span data-ttu-id="07c8f-860">La source ou la destination ne dispose pas de la dernière version de l’objet.</span><span class="sxs-lookup"><span data-stu-id="07c8f-860">Either source or destination does not have the latest version of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-861"><span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**ERREUR \_ d' \_ \_ incompatibilité de nom de source DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-861"><span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**ERROR\_DS\_SRC\_NAME\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-862">8484 (0x2124)</span><span class="sxs-lookup"><span data-stu-id="07c8f-862">8484 (0x2124)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-863">La source et la destination d’un déplacement entre domaines ne sont pas d’accord sur le nom actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="07c8f-863">Source and destination of a cross-domain move do not agree on the object's current name.</span></span> <span data-ttu-id="07c8f-864">La source ou la destination ne dispose pas de la dernière version de l’objet.</span><span class="sxs-lookup"><span data-stu-id="07c8f-864">Either source or destination does not have the latest version of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-865"><span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**ERREUR du contrôleur \_ \_ de domaine source \_ et \_ DST \_ \_ identique**</span><span class="sxs-lookup"><span data-stu-id="07c8f-865"><span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**ERROR\_DS\_SRC\_AND\_DST\_NC\_IDENTICAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-866">8485 (0x2125)</span><span class="sxs-lookup"><span data-stu-id="07c8f-866">8485 (0x2125)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-867">La source et la destination de l’opération de déplacement entre domaines sont identiques.</span><span class="sxs-lookup"><span data-stu-id="07c8f-867">Source and destination for the cross-domain move operation are identical.</span></span> <span data-ttu-id="07c8f-868">L’appelant doit utiliser l’opération de déplacement local au lieu de l’opération de déplacement entre domaines.</span><span class="sxs-lookup"><span data-stu-id="07c8f-868">Caller should use local move operation instead of cross-domain move operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-869"><span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**ERREUR \_ d' \_ \_ \_ incompatibilité NC du service d’heure DS**</span><span class="sxs-lookup"><span data-stu-id="07c8f-869"><span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**ERROR\_DS\_DST\_NC\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-870">8486 (0x2126)</span><span class="sxs-lookup"><span data-stu-id="07c8f-870">8486 (0x2126)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-871">La source et la destination d’un déplacement entre domaines ne sont pas accordées sur les contextes d’attribution de noms de la forêt.</span><span class="sxs-lookup"><span data-stu-id="07c8f-871">Source and destination for a cross-domain move are not in agreement on the naming contexts in the forest.</span></span> <span data-ttu-id="07c8f-872">La source ou la destination ne dispose pas de la dernière version du conteneur partitions.</span><span class="sxs-lookup"><span data-stu-id="07c8f-872">Either source or destination does not have the latest version of the Partitions container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-873"><span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**ERREUR \_ DS \_ non \_ AUTHORITIVE \_ pour le \_ contexte d’heure d’été \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-873"><span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**ERROR\_DS\_NOT\_AUTHORITIVE\_FOR\_DST\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-874">8487 (0x2127)</span><span class="sxs-lookup"><span data-stu-id="07c8f-874">8487 (0x2127)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-875">La destination d’un déplacement entre domaines ne fait pas autorité pour le contexte d’appellation de destination.</span><span class="sxs-lookup"><span data-stu-id="07c8f-875">Destination of a cross-domain move is not authoritative for the destination naming context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-876"><span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**ERREUR \_ d' \_ \_ incompatibilité de GUID SRC DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-876"><span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**ERROR\_DS\_SRC\_GUID\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-877">8488 (0x2128)</span><span class="sxs-lookup"><span data-stu-id="07c8f-877">8488 (0x2128)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-878">La source et la destination d’un déplacement inter-domaines ne sont pas d’accord sur l’identité de l’objet source.</span><span class="sxs-lookup"><span data-stu-id="07c8f-878">Source and destination of a cross-domain move do not agree on the identity of the source object.</span></span> <span data-ttu-id="07c8f-879">La source ou la destination ne dispose pas de la dernière version de l’objet source.</span><span class="sxs-lookup"><span data-stu-id="07c8f-879">Either source or destination does not have the latest version of the source object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-880"><span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**ERREUR \_ DS \_ Impossible de \_ déplacer l' \_ \_ objet supprimé**</span><span class="sxs-lookup"><span data-stu-id="07c8f-880"><span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**ERROR\_DS\_CANT\_MOVE\_DELETED\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-881">8489 (0x2129)</span><span class="sxs-lookup"><span data-stu-id="07c8f-881">8489 (0x2129)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-882">L’objet en cours de déplacement entre domaines est déjà connu pour être supprimé par le serveur de destination.</span><span class="sxs-lookup"><span data-stu-id="07c8f-882">Object being moved across-domains is already known to be deleted by the destination server.</span></span> <span data-ttu-id="07c8f-883">Le serveur source ne dispose pas de la dernière version de l’objet source.</span><span class="sxs-lookup"><span data-stu-id="07c8f-883">The source server does not have the latest version of the source object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-884"><span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**ERREUR \_ \_ \_ de l’opération de contrôleur de domaine principal DS \_ en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="07c8f-884"><span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**ERROR\_DS\_PDC\_OPERATION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-885">8490 (0x212A)</span><span class="sxs-lookup"><span data-stu-id="07c8f-885">8490 (0x212A)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-886">Une autre opération qui requiert un accès exclusif au FSMO du contrôleur de domaine principal est déjà en cours.</span><span class="sxs-lookup"><span data-stu-id="07c8f-886">Another operation which requires exclusive access to the PDC FSMO is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-887"><span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**ERREUR \_ de \_ nettoyage inter- \_ domaines DS \_ \_ REQD**</span><span class="sxs-lookup"><span data-stu-id="07c8f-887"><span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**ERROR\_DS\_CROSS\_DOMAIN\_CLEANUP\_REQD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-888">8491 (0x212B)</span><span class="sxs-lookup"><span data-stu-id="07c8f-888">8491 (0x212B)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-889">Une opération de déplacement entre domaines a échoué, de sorte que deux versions de l’objet déplacé existent-une dans les domaines source et de destination.</span><span class="sxs-lookup"><span data-stu-id="07c8f-889">A cross-domain move operation failed such that two versions of the moved object exist - one each in the source and destination domains.</span></span> <span data-ttu-id="07c8f-890">L’objet de destination doit être supprimé pour restaurer le système à un état cohérent.</span><span class="sxs-lookup"><span data-stu-id="07c8f-890">The destination object needs to be removed to restore the system to a consistent state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-891"><span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**ERREUR \_ d' \_ \_ opération de \_ déplacement \_ XDOM illégale du service d’annuaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-891"><span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**ERROR\_DS\_ILLEGAL\_XDOM\_MOVE\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-892">8492 (0x212C)</span><span class="sxs-lookup"><span data-stu-id="07c8f-892">8492 (0x212C)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-893">Cet objet ne peut pas être déplacé au-delà des limites du domaine, soit parce que les déplacements inter-domaines pour cette classe ne sont pas autorisés, soit parce que l’objet a des caractéristiques spéciales, par exemple : compte de confiance ou RID restreint, ce qui empêche son déplacement.</span><span class="sxs-lookup"><span data-stu-id="07c8f-893">This object may not be moved across domain boundaries either because cross-domain moves for this class are disallowed, or the object has some special characteristics, e.g.: trust account or restricted RID, which prevent its move.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-894"><span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**ERREUR DS inversion \_ \_ avec le \_ \_ \_ groupe ACCT \_ MEMBERSHPS**</span><span class="sxs-lookup"><span data-stu-id="07c8f-894"><span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**ERROR\_DS\_CANT\_WITH\_ACCT\_GROUP\_MEMBERSHPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-895">8493 (0x212D)</span><span class="sxs-lookup"><span data-stu-id="07c8f-895">8493 (0x212D)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-896">Impossible de déplacer des objets ayant des appartenances au-delà des limites du domaine, car une fois qu’ils sont déplacés, cela ne respecte pas les conditions d’appartenance du groupe de comptes.</span><span class="sxs-lookup"><span data-stu-id="07c8f-896">Can't move objects with memberships across domain boundaries as once moved, this would violate the membership conditions of the account group.</span></span> <span data-ttu-id="07c8f-897">Supprimez l’objet des appartenances aux groupes de comptes et réessayez.</span><span class="sxs-lookup"><span data-stu-id="07c8f-897">Remove the object from any account group memberships and retry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-898"><span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**l’erreur \_ DS \_ NC \_ doit avoir un \_ \_ \_ parent NC**</span><span class="sxs-lookup"><span data-stu-id="07c8f-898"><span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**ERROR\_DS\_NC\_MUST\_HAVE\_NC\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-899">8494 (0x212E)</span><span class="sxs-lookup"><span data-stu-id="07c8f-899">8494 (0x212E)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-900">Un en-tête de contexte d’appellation doit être l’enfant immédiat d’un autre en-tête de contexte d’attribution de noms, et non d’un nœud intérieur.</span><span class="sxs-lookup"><span data-stu-id="07c8f-900">A naming context head must be the immediate child of another naming context head, not of an interior node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-901"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**ERREUR \_ DS \_ CR \_ Impossible \_ à \_ valider**</span><span class="sxs-lookup"><span data-stu-id="07c8f-901"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**ERROR\_DS\_CR\_IMPOSSIBLE\_TO\_VALIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-902">8495 (0x212F)</span><span class="sxs-lookup"><span data-stu-id="07c8f-902">8495 (0x212F)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-903">Le répertoire ne peut pas valider le nom de contexte de nommage proposé, car il ne contient pas de réplica du contexte d’appellation au-dessus du contexte d’appellation proposé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-903">The directory cannot validate the proposed naming context name because it does not hold a replica of the naming context above the proposed naming context.</span></span> <span data-ttu-id="07c8f-904">Vérifiez que le rôle de maître d’attribution de noms de domaine est détenu par un serveur configuré en tant que serveur de catalogue global et que le serveur est à jour avec ses partenaires de réplication.</span><span class="sxs-lookup"><span data-stu-id="07c8f-904">Please ensure that the domain naming master role is held by a server that is configured as a global catalog server, and that the server is up to date with its replication partners.</span></span> <span data-ttu-id="07c8f-905">(S’applique uniquement aux maîtres d’attribution de noms de domaine Windows 2000.)</span><span class="sxs-lookup"><span data-stu-id="07c8f-905">(Applies only to Windows 2000 Domain Naming masters.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-906"><span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**ERREUR \_ de \_ domaine d’heure d’été DS \_ \_ non \_ Native**</span><span class="sxs-lookup"><span data-stu-id="07c8f-906"><span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**ERROR\_DS\_DST\_DOMAIN\_NOT\_NATIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-907">8496 (0x2130)</span><span class="sxs-lookup"><span data-stu-id="07c8f-907">8496 (0x2130)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-908">Le domaine de destination doit être en mode natif.</span><span class="sxs-lookup"><span data-stu-id="07c8f-908">Destination domain must be in native mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-909"><span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**ERREUR \_ de \_ \_ conteneur d’infrastructure manquante du service d’annuaire \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-909"><span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**ERROR\_DS\_MISSING\_INFRASTRUCTURE\_CONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-910">8497 (0x2131)</span><span class="sxs-lookup"><span data-stu-id="07c8f-910">8497 (0x2131)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-911">Impossible d’effectuer l’opération, car le serveur n’a pas de conteneur d’infrastructure dans le domaine d’intérêt.</span><span class="sxs-lookup"><span data-stu-id="07c8f-911">The operation cannot be performed because the server does not have an infrastructure container in the domain of interest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-912"><span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**ERREUR \_ DS \_ Impossible de \_ déplacer le \_ groupe de comptes \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-912"><span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**ERROR\_DS\_CANT\_MOVE\_ACCOUNT\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-913">8498 (0x2132)</span><span class="sxs-lookup"><span data-stu-id="07c8f-913">8498 (0x2132)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-914">Le déplacement entre domaines de groupes de comptes non vides n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-914">Cross-domain move of non-empty account groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-915"><span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**ERREUR \_ DS \_ Impossible de \_ déplacer le \_ groupe de ressources \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-915"><span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**ERROR\_DS\_CANT\_MOVE\_RESOURCE\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-916">8499 (0x2133)</span><span class="sxs-lookup"><span data-stu-id="07c8f-916">8499 (0x2133)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-917">Le déplacement entre domaines de groupes de ressources non vides n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-917">Cross-domain move of non-empty resource groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-918"><span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**indicateur de recherche de l’erreur \_ DS \_ non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-918"><span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**ERROR\_DS\_INVALID\_SEARCH\_FLAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-919">8500 (0x2134)</span><span class="sxs-lookup"><span data-stu-id="07c8f-919">8500 (0x2134)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-920">Les indicateurs de recherche de l’attribut ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="07c8f-920">The search flags for the attribute are invalid.</span></span> <span data-ttu-id="07c8f-921">Le bit ANR n’est valide que sur les attributs des chaînes Unicode ou TELETEX.</span><span class="sxs-lookup"><span data-stu-id="07c8f-921">The ANR bit is valid only on attributes of Unicode or Teletex strings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-922"><span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**ERREUR \_ DS \_ non \_ arborescence \_ supprimée \_ au-dessus du \_ contexte de nommage**</span><span class="sxs-lookup"><span data-stu-id="07c8f-922"><span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**ERROR\_DS\_NO\_TREE\_DELETE\_ABOVE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-923">8501 (0x2135)</span><span class="sxs-lookup"><span data-stu-id="07c8f-923">8501 (0x2135)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-924">Les suppressions d’arborescence à partir d’un objet qui a une tête NC en tant que descendant ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="07c8f-924">Tree deletions starting at an object which has an NC head as a descendant are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-925"><span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**ERREUR \_ \_ de l' \_ arborescence de verrous impossible DS \_ \_ pour \_ suppression**</span><span class="sxs-lookup"><span data-stu-id="07c8f-925"><span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**ERROR\_DS\_COULDNT\_LOCK\_TREE\_FOR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-926">8502 (0x2136)</span><span class="sxs-lookup"><span data-stu-id="07c8f-926">8502 (0x2136)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-927">Le service d’annuaire n’a pas pu verrouiller une arborescence en vue d’une suppression de l’arborescence, car l’arborescence était en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="07c8f-927">The directory service failed to lock a tree in preparation for a tree deletion because the tree was in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-928"><span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**ERREUR \_ \_ Impossible \_ de l' \_ identification \_ des objets pour la \_ Suppression d’arborescence \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-928"><span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**ERROR\_DS\_COULDNT\_IDENTIFY\_OBJECTS\_FOR\_TREE\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-929">8503 (0x2137)</span><span class="sxs-lookup"><span data-stu-id="07c8f-929">8503 (0x2137)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-930">Le service d’annuaire n’a pas pu identifier la liste des objets à supprimer lors de la tentative de suppression de l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="07c8f-930">The directory service failed to identify the list of objects to delete while attempting a tree deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-931"><span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**ERREUR \_ échec de l’initialisation du service DS \_ sam \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-931"><span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**ERROR\_DS\_SAM\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-932">8504 (0x2138)</span><span class="sxs-lookup"><span data-stu-id="07c8f-932">8504 (0x2138)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-933">L’initialisation du gestionnaire des comptes de sécurité a échoué en raison de l’erreur suivante : %1.</span><span class="sxs-lookup"><span data-stu-id="07c8f-933">Security Accounts Manager initialization failed because of the following error: %1.</span></span> <span data-ttu-id="07c8f-934">État d’erreur : 0x %2.</span><span class="sxs-lookup"><span data-stu-id="07c8f-934">Error Status: 0x%2.</span></span> <span data-ttu-id="07c8f-935">Arrêtez ce système et redémarrez en mode restauration des services d’annuaire, consultez le journal des événements pour obtenir des informations plus détaillées.</span><span class="sxs-lookup"><span data-stu-id="07c8f-935">Please shutdown this system and reboot into Directory Services Restore Mode, check the event log for more detailed information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-936"><span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**ERREUR \_ de \_ \_ violation de groupe sensible aux services d’annuaire \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-936"><span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**ERROR\_DS\_SENSITIVE\_GROUP\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-937">8505 (0x2139)</span><span class="sxs-lookup"><span data-stu-id="07c8f-937">8505 (0x2139)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-938">Seul un administrateur peut modifier la liste des membres d’un groupe d’administration.</span><span class="sxs-lookup"><span data-stu-id="07c8f-938">Only an administrator can modify the membership list of an administrative group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-939"><span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**ERREUR DS inverser \_ \_ \_ \_ PRIMARYGROUPID**</span><span class="sxs-lookup"><span data-stu-id="07c8f-939"><span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**ERROR\_DS\_CANT\_MOD\_PRIMARYGROUPID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-940">8506 (0x213A)</span><span class="sxs-lookup"><span data-stu-id="07c8f-940">8506 (0x213A)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-941">Impossible de modifier l’ID de groupe principal d’un compte de contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="07c8f-941">Cannot change the primary group ID of a domain controller account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-942"><span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**ERREUR \_ de \_ \_ schéma de base illégal du \_ service d’annuaire \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-942"><span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**ERROR\_DS\_ILLEGAL\_BASE\_SCHEMA\_MOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-943">8507 (0x213B)</span><span class="sxs-lookup"><span data-stu-id="07c8f-943">8507 (0x213B)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-944">Une tentative de modification du schéma de base a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-944">An attempt is made to modify the base schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-945"><span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**ERREUR \_ de \_ changement de schéma non sécurisé DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-945"><span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**ERROR\_DS\_NONSAFE\_SCHEMA\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-946">8508 (0x213C)</span><span class="sxs-lookup"><span data-stu-id="07c8f-946">8508 (0x213C)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-947">L’ajout d’un nouvel attribut obligatoire à une classe existante, la suppression d’un attribut obligatoire d’une classe existante, ou l’ajout d’un attribut facultatif à la classe spéciale Top qui n’est pas un attribut lien secondaire (directement ou par héritage, par exemple, en ajoutant ou supprimant une classe auxiliaire) n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-947">Adding a new mandatory attribute to an existing class, deleting a mandatory attribute from an existing class, or adding an optional attribute to the special class Top that is not a backlink attribute (directly or through inheritance, for example, by adding or deleting an auxiliary class) is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-948"><span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**ERREUR \_ de \_ \_ mise à jour du schéma DS non \_ autorisée**</span><span class="sxs-lookup"><span data-stu-id="07c8f-948"><span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**ERROR\_DS\_SCHEMA\_UPDATE\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-949">8509 (0x213D)</span><span class="sxs-lookup"><span data-stu-id="07c8f-949">8509 (0x213D)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-950">La mise à jour du schéma n’est pas autorisée sur ce contrôleur de périphérique car le contrôleur de périphérique n’est pas le propriétaire du rôle FSMO du schéma.</span><span class="sxs-lookup"><span data-stu-id="07c8f-950">Schema update is not allowed on this DC because the DC is not the schema FSMO Role Owner.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-951"><span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**ERREUR \_ DS \_ Impossible de \_ créer \_ sous le \_ schéma**</span><span class="sxs-lookup"><span data-stu-id="07c8f-951"><span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**ERROR\_DS\_CANT\_CREATE\_UNDER\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-952">8510 (0x213E)</span><span class="sxs-lookup"><span data-stu-id="07c8f-952">8510 (0x213E)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-953">Impossible de créer un objet de cette classe sous le conteneur de schéma.</span><span class="sxs-lookup"><span data-stu-id="07c8f-953">An object of this class cannot be created under the schema container.</span></span> <span data-ttu-id="07c8f-954">Vous pouvez uniquement créer des objets attribute-Schema et Class-Schema sous le conteneur Schema.</span><span class="sxs-lookup"><span data-stu-id="07c8f-954">You can only create attribute-schema and class-schema objects under the schema container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-955"><span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**ERREUR d' \_ installation du service d’annuaire \_ \_ non \_ src \_ \_ version SCH**</span><span class="sxs-lookup"><span data-stu-id="07c8f-955"><span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**ERROR\_DS\_INSTALL\_NO\_SRC\_SCH\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-956">8511 (0x213F)</span><span class="sxs-lookup"><span data-stu-id="07c8f-956">8511 (0x213F)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-957">Le réplica/l’installation enfant n’a pas pu récupérer l’attribut objectVersion sur le conteneur de schéma sur le contrôleur de périphérique source.</span><span class="sxs-lookup"><span data-stu-id="07c8f-957">The replica/child install failed to get the objectVersion attribute on the schema container on the source DC.</span></span> <span data-ttu-id="07c8f-958">Soit l’attribut est manquant dans le conteneur de schéma, soit les informations d’identification fournies n’ont pas l’autorisation de le lire.</span><span class="sxs-lookup"><span data-stu-id="07c8f-958">Either the attribute is missing on the schema container or the credentials supplied do not have permission to read it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-959"><span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**ERREUR \_ \_ d’installation \_ de la DS non \_ \_ version SCH \_ dans \_ INIFILE**</span><span class="sxs-lookup"><span data-stu-id="07c8f-959"><span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**ERROR\_DS\_INSTALL\_NO\_SCH\_VERSION\_IN\_INIFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-960">8512 (0x2140)</span><span class="sxs-lookup"><span data-stu-id="07c8f-960">8512 (0x2140)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-961">L’installation du réplica/enfant n’a pas pu lire l’attribut objectVersion dans la section SCHEMA du fichier schema.ini dans le répertoire system32.</span><span class="sxs-lookup"><span data-stu-id="07c8f-961">The replica/child install failed to read the objectVersion attribute in the SCHEMA section of the file schema.ini in the system32 directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-962"><span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**ERREUR \_ de \_ \_ type de groupe non valide DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-962"><span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**ERROR\_DS\_INVALID\_GROUP\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-963">8513 (0x2141)</span><span class="sxs-lookup"><span data-stu-id="07c8f-963">8513 (0x2141)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-964">Le type de groupe spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="07c8f-964">The specified group type is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-965"><span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**ERREUR \_ DS \_ non \_ imbriquer \_ GLOBALGROUP \_ dans \_ MIXEDDOMAIN**</span><span class="sxs-lookup"><span data-stu-id="07c8f-965"><span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**ERROR\_DS\_NO\_NEST\_GLOBALGROUP\_IN\_MIXEDDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-966">8514 (0x2142)</span><span class="sxs-lookup"><span data-stu-id="07c8f-966">8514 (0x2142)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-967">Vous ne pouvez pas imbriquer des groupes globaux dans un domaine mixte si la sécurité est activée pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="07c8f-967">You cannot nest global groups in a mixed domain if the group is security-enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-968"><span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**ERREUR \_ DS \_ non \_ imbriquer un \_ localgroup \_ dans \_ MIXEDDOMAIN**</span><span class="sxs-lookup"><span data-stu-id="07c8f-968"><span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**ERROR\_DS\_NO\_NEST\_LOCALGROUP\_IN\_MIXEDDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-969">8515 (0x2143)</span><span class="sxs-lookup"><span data-stu-id="07c8f-969">8515 (0x2143)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-970">Vous ne pouvez pas imbriquer des groupes locaux dans un domaine mixte si la sécurité est activée pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="07c8f-970">You cannot nest local groups in a mixed domain if the group is security-enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-971"><span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**ERREUR le \_ service \_ Global DS \_ \_ ne dispose pas du \_ \_ membre local**</span><span class="sxs-lookup"><span data-stu-id="07c8f-971"><span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**ERROR\_DS\_GLOBAL\_CANT\_HAVE\_LOCAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-972">8516 (0x2144)</span><span class="sxs-lookup"><span data-stu-id="07c8f-972">8516 (0x2144)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-973">Un groupe global ne peut pas avoir un groupe local en tant que membre.</span><span class="sxs-lookup"><span data-stu-id="07c8f-973">A global group cannot have a local group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-974"><span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**ERREUR \_ \_ global des services DS impossible d’avoir un \_ \_ \_ \_ membre universel**</span><span class="sxs-lookup"><span data-stu-id="07c8f-974"><span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**ERROR\_DS\_GLOBAL\_CANT\_HAVE\_UNIVERSAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-975">8517 (0x2145)</span><span class="sxs-lookup"><span data-stu-id="07c8f-975">8517 (0x2145)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-976">Un groupe global ne peut pas avoir un groupe universel en tant que membre.</span><span class="sxs-lookup"><span data-stu-id="07c8f-976">A global group cannot have a universal group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-977"><span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**ERREUR le \_ service \_ universel DS \_ \_ n’a pas de \_ \_ membre local**</span><span class="sxs-lookup"><span data-stu-id="07c8f-977"><span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**ERROR\_DS\_UNIVERSAL\_CANT\_HAVE\_LOCAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-978">8518 (0x2146)</span><span class="sxs-lookup"><span data-stu-id="07c8f-978">8518 (0x2146)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-979">Un groupe universel ne peut pas avoir un groupe local en tant que membre.</span><span class="sxs-lookup"><span data-stu-id="07c8f-979">A universal group cannot have a local group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-980"><span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**ERREUR le \_ service \_ Global DS \_ \_ ne dispose pas d’un \_ \_ membre CROSSDOMAIN**</span><span class="sxs-lookup"><span data-stu-id="07c8f-980"><span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**ERROR\_DS\_GLOBAL\_CANT\_HAVE\_CROSSDOMAIN\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-981">8519 (0x2147)</span><span class="sxs-lookup"><span data-stu-id="07c8f-981">8519 (0x2147)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-982">Un groupe global ne peut pas avoir de membre inter-domaines.</span><span class="sxs-lookup"><span data-stu-id="07c8f-982">A global group cannot have a cross-domain member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-983"><span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**ERREUR \_ DS \_ local \_ Impossible d' \_ utiliser le \_ \_ membre local CROSSDOMAIN \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-983"><span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**ERROR\_DS\_LOCAL\_CANT\_HAVE\_CROSSDOMAIN\_LOCAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-984">8520 (0x2148)</span><span class="sxs-lookup"><span data-stu-id="07c8f-984">8520 (0x2148)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-985">Un groupe local ne peut pas avoir un autre groupe local inter-domaines en tant que membre.</span><span class="sxs-lookup"><span data-stu-id="07c8f-985">A local group cannot have another cross domain local group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-986"><span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**l’erreur \_ DS \_ a des \_ \_ membres principaux**</span><span class="sxs-lookup"><span data-stu-id="07c8f-986"><span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**ERROR\_DS\_HAVE\_PRIMARY\_MEMBERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-987">8521 (0x2149)</span><span class="sxs-lookup"><span data-stu-id="07c8f-987">8521 (0x2149)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-988">Un groupe avec des membres principaux ne peut pas passer à un groupe dont la sécurité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-988">A group with primary members cannot change to a security-disabled group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-989"><span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**ERREUR lors de la \_ \_ \_ conversion SD de la chaîne DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-989"><span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**ERROR\_DS\_STRING\_SD\_CONVERSION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-990">8522 (0x214A)</span><span class="sxs-lookup"><span data-stu-id="07c8f-990">8522 (0x214A)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-991">Le chargement du cache de schéma n’a pas pu convertir le SD par défaut de la chaîne sur un objet de schéma de classe.</span><span class="sxs-lookup"><span data-stu-id="07c8f-991">The schema cache load failed to convert the string default SD on a class-schema object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-992"><span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**ERREUR \_ du \_ maître d’attribution de noms DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-992"><span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**ERROR\_DS\_NAMING\_MASTER\_GC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-993">8523 (0x214B)</span><span class="sxs-lookup"><span data-stu-id="07c8f-993">8523 (0x214B)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-994">Seuls les serveurs DSA configurés comme serveurs de catalogue global doivent être autorisés à conserver le rôle FSMO du maître d’attribution de noms de domaine.</span><span class="sxs-lookup"><span data-stu-id="07c8f-994">Only DSAs configured to be Global Catalog servers should be allowed to hold the Domain Naming Master FSMO role.</span></span> <span data-ttu-id="07c8f-995">(S’applique uniquement aux serveurs Windows 2000.)</span><span class="sxs-lookup"><span data-stu-id="07c8f-995">(Applies only to Windows 2000 servers.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-996"><span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**ERREUR d’échec de la \_ \_ recherche DNS DNS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-996"><span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**ERROR\_DS\_DNS\_LOOKUP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-997">8524 (0x214C)</span><span class="sxs-lookup"><span data-stu-id="07c8f-997">8524 (0x214C)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-998">L’opération DSA ne peut pas continuer en raison d’un échec de la recherche DNS.</span><span class="sxs-lookup"><span data-stu-id="07c8f-998">The DSA operation is unable to proceed because of a DNS lookup failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-999"><span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**ERREUR \_ de \_ \_ mise à jour des SPN impossible DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-999"><span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**ERROR\_DS\_COULDNT\_UPDATE\_SPNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1000">8525 (0x214D)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1000">8525 (0x214D)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1001">Lors du traitement d’une modification apportée au nom d’hôte DNS pour un objet, les valeurs de nom de principal du service n’ont pas pu être synchronisées.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1001">While processing a change to the DNS Host Name for an object, the Service Principal Name values could not be kept in sync.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1002"><span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**ERREUR \_ DS \_ Impossible de \_ récupérer la \_ SD**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1002"><span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**ERROR\_DS\_CANT\_RETRIEVE\_SD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1003">8526 (0x214E)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1003">8526 (0x214E)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1004">Impossible de lire l’attribut descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1004">The Security Descriptor attribute could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1005"><span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**ERREUR \_ de \_ clé DS \_ non \_ unique**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1005"><span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**ERROR\_DS\_KEY\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1006">8527 (0x214F)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1006">8527 (0x214F)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1007">L’objet demandé est introuvable, mais un objet avec cette clé a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1007">The object requested was not found, but an object with that key was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1008"><span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**ERREUR \_ de \_ \_ \_ syntaxe att liée \_ à l’erreur DS**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1008"><span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**ERROR\_DS\_WRONG\_LINKED\_ATT\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1009">8528 (0x2150)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1009">8528 (0x2150)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1010">La syntaxe de l’attribut lié en cours d’ajout est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1010">The syntax of the linked attribute being added is incorrect.</span></span> <span data-ttu-id="07c8f-1011">Les liens de transfert peuvent uniquement avoir la syntaxe 2.5.5.1, 2.5.5.7 et 2.5.5.14, et les liens de liaison ne peuvent comporter que des 2.5.5.1 de syntaxe.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1011">Forward links can only have syntax 2.5.5.1, 2.5.5.7, and 2.5.5.14, and backlinks can only have syntax 2.5.5.1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1012"><span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**ERREUR \_ DS \_ sam \_ nécessite \_ un \_ mot de passe BOOTKEY**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1012"><span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**ERROR\_DS\_SAM\_NEED\_BOOTKEY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1013">8529 (0x2151)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1013">8529 (0x2151)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1014">Le gestionnaire de compte de sécurité doit recevoir le mot de passe de démarrage.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1014">Security Account Manager needs to get the boot password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1015"><span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**ERREUR \_ DS \_ sam \_ nécessite \_ une \_ disquette BOOTKEY**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1015"><span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**ERROR\_DS\_SAM\_NEED\_BOOTKEY\_FLOPPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1016">8530 (0x2152)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1016">8530 (0x2152)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1017">Le gestionnaire de compte de sécurité doit récupérer la clé de démarrage à partir d’une disquette.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1017">Security Account Manager needs to get the boot key from floppy disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1018"><span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**ERREUR \_ \_ Impossible de \_ Démarrer DS**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1018"><span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**ERROR\_DS\_CANT\_START**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1019">8531 (0x2153)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1019">8531 (0x2153)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1020">Impossible de démarrer le service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1020">Directory Service cannot start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1021"><span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**ERREUR d' \_ initialisation du service d’annuaire \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1021"><span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**ERROR\_DS\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1022">8532 (0x2154)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1022">8532 (0x2154)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1023">Les services d’annuaire n’ont pas pu démarrer.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1023">Directory Services could not start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1024"><span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**ERREUR \_ DS \_ no \_ PKT \_ Privacy \_ on \_ Connection**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1024"><span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**ERROR\_DS\_NO\_PKT\_PRIVACY\_ON\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1025">8533 (0x2155)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1025">8533 (0x2155)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1026">La connexion entre le client et le serveur nécessite une confidentialité du paquet ou une meilleure.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1026">The connection between client and server requires packet privacy or better.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1027"><span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**ERREUR \_ \_ \_ de domaine source DS dans la \_ \_ forêt**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1027"><span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**ERROR\_DS\_SOURCE\_DOMAIN\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1028">8534 (0x2156)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1028">8534 (0x2156)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1029">Le domaine source n’est peut-être pas dans la même forêt que la destination.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1029">The source domain may not be in the same forest as destination.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1030"><span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**ERREUR \_ \_ \_ domaine de destination DS \_ non dans la \_ \_ forêt**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1030"><span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**ERROR\_DS\_DESTINATION\_DOMAIN\_NOT\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1031">8535 (0x2157)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1031">8535 (0x2157)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1032">Le domaine de destination doit se trouver dans la forêt.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1032">The destination domain must be in the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1033"><span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**\_ \_ l’audit de destination de \_ l’annuaire d’erreurs \_ n’est pas \_ activé**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1033"><span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**ERROR\_DS\_DESTINATION\_AUDITING\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1034">8536 (0x2158)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1034">8536 (0x2158)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1035">L’opération requiert l’activation de l’audit du domaine de destination.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1035">The operation requires that destination domain auditing be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1036"><span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**ERREUR \_ DS \_ Impossible \_ de trouver le \_ contrôleur \_ de domaine pour le \_ \_ domaine SRC**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1036"><span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**ERROR\_DS\_CANT\_FIND\_DC\_FOR\_SRC\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1037">8537 (0x2159)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1037">8537 (0x2159)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1038">L’opération n’a pas pu localiser de contrôleur de domaine pour le domaine source.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1038">The operation couldn't locate a DC for the source domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1039"><span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**ERREUR \_ du \_ \_ \_ \_ groupe \_ ou de l' \_ utilisateur de la source DS SRC**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1039"><span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**ERROR\_DS\_SRC\_OBJ\_NOT\_GROUP\_OR\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1040">8538 (0x215A)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1040">8538 (0x215A)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1041">L’objet source doit être un groupe ou un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1041">The source object must be a group or user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1042"><span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**ERREUR \_ \_ \_ de sid SRC SRC dans la \_ \_ \_ forêt**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1042"><span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**ERROR\_DS\_SRC\_SID\_EXISTS\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1043">8539 (0x215B)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1043">8539 (0x215B)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1044">Le SID de l’objet source existe déjà dans la forêt de destination.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1044">The source object's SID already exists in destination forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1045"><span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**ERREUR \_ d' \_ \_ \_ \_ incompatibilité de la classe d’objet source et DST du \_ \_ DS**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1045"><span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**ERROR\_DS\_SRC\_AND\_DST\_OBJECT\_CLASS\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1046">8540 (0x215C)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1046">8540 (0x215C)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1047">L’objet source et l’objet de destination doivent être du même type.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1047">The source and destination object must be of the same type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1048"><span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**ERREUR \_ sam \_ init \_ Failure**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1048"><span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**ERROR\_SAM\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1049">8541 (0x215D)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1049">8541 (0x215D)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1050">L’initialisation du gestionnaire des comptes de sécurité a échoué en raison de l’erreur suivante : %1.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1050">Security Accounts Manager initialization failed because of the following error: %1.</span></span> <span data-ttu-id="07c8f-1051">État d’erreur : 0x %2.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1051">Error Status: 0x%2.</span></span> <span data-ttu-id="07c8f-1052">Cliquez sur OK pour arrêter le système et redémarrez en mode sans échec.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1052">Click OK to shut down the system and reboot into Safe Mode.</span></span> <span data-ttu-id="07c8f-1053">Pour plus d’informations, consultez le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1053">Check the event log for detailed information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1054"><span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**ERREUR \_ d' \_ \_ informations sur le schéma DRA \_ \_ de l’annuaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1054"><span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**ERROR\_DS\_DRA\_SCHEMA\_INFO\_SHIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1055">8542 (0x215E)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1055">8542 (0x215E)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1056">Les informations de schéma n’ont pas pu être incluses dans la demande de réplication.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1056">Schema information could not be included in the replication request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1057"><span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**ERREUR \_ de \_ \_ conflit de schéma DRA \_ de l’annuaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1057"><span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**ERROR\_DS\_DRA\_SCHEMA\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1058">8543 (0x215F)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1058">8543 (0x215F)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1059">L’opération de réplication n’a pas pu aboutir en raison d’une incompatibilité de schéma.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1059">The replication operation could not be completed due to a schema incompatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1060"><span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**ERREUR \_ de \_ \_ schéma DRA \_ antérieur \_ du service d’annuaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1060"><span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**ERROR\_DS\_DRA\_EARLIER\_SCHEMA\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1061">8544 (0x2160)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1061">8544 (0x2160)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1062">L’opération de réplication n’a pas pu aboutir en raison d’une incompatibilité de schéma précédente.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1062">The replication operation could not be completed due to a previous schema incompatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1063"><span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**ERREUR de non- \_ \_ concordance du contexte de \_ \_ nommage DRA DRA \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1063"><span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**ERROR\_DS\_DRA\_OBJ\_NC\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1064">8545 (0x2161)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1064">8545 (0x2161)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1065">Impossible d’appliquer la mise à jour de réplication, car la source ou la destination n’a pas encore reçu d’informations concernant une opération de déplacement entre domaines récente.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1065">The replication update could not be applied because either the source or the destination has not yet received information regarding a recent cross-domain move operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1066"><span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**l' \_ erreur \_ DS \_ NC \_ contient toujours des \_ DSA**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1066"><span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**ERROR\_DS\_NC\_STILL\_HAS\_DSAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1067">8546 (0x2162)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1067">8546 (0x2162)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1068">Le domaine demandé n’a pas pu être supprimé, car il existe des contrôleurs de domaine qui hébergent toujours ce domaine.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1068">The requested domain could not be deleted because there exist domain controllers that still host this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1069"><span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**ERREUR \_ de \_ GC DS \_ obligatoire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1069"><span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**ERROR\_DS\_GC\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1070">8547 (0x2163)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1070">8547 (0x2163)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1071">L’opération demandée ne peut être effectuée que sur un serveur de catalogue global.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1071">The requested operation can be performed only on a global catalog server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1072"><span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**ERREUR \_ \_ \_ de membre local DS \_ de \_ local \_ uniquement**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1072"><span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**ERROR\_DS\_LOCAL\_MEMBER\_OF\_LOCAL\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1073">8548 (0x2164)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1073">8548 (0x2164)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1074">Un groupe local peut uniquement être membre d’autres groupes locaux dans le même domaine.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1074">A local group can only be a member of other local groups in the same domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1075"><span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**ERREUR \_ DS \_ non \_ FPO \_ dans \_ les \_ groupes universels**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1075"><span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**ERROR\_DS\_NO\_FPO\_IN\_UNIVERSAL\_GROUPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1076">8549 (0x2165)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1076">8549 (0x2165)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1077">Les principaux de sécurité étrangers ne peuvent pas être membres de groupes universels.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1077">Foreign security principals cannot be members of universal groups.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1078"><span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**ERREUR \_ DS \_ Impossible \_ \_ d’ajouter à \_ gc**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1078"><span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**ERROR\_DS\_CANT\_ADD\_TO\_GC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1079">8550 (0x2166)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1079">8550 (0x2166)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1080">L’attribut ne peut pas être répliqué dans le catalogue global pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1080">The attribute is not allowed to be replicated to the GC because of security reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1081"><span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**ERREUR \_ DS \_ aucun \_ point de contrôle \_ avec \_ PDC**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1081"><span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**ERROR\_DS\_NO\_CHECKPOINT\_WITH\_PDC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1082">8551 (0x2167)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1082">8551 (0x2167)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1083">Le point de contrôle avec le contrôleur de domaine principal n’a pas pu être pris en raison d’un trop grand nombre de modifications actuellement traitées.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1083">The checkpoint with the PDC could not be taken because there too many modifications being processed currently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1084"><span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**ERREUR \_ \_ d’audit de la source DS \_ \_ non \_ activée**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1084"><span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**ERROR\_DS\_SOURCE\_AUDITING\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1085">8552 (0x2168)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1085">8552 (0x2168)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1086">L’opération requiert l’activation de l’audit du domaine source.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1086">The operation requires that source domain auditing be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1087"><span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**ERREUR \_ DS \_ Impossible \_ \_ de créer dans le \_ contexte de nommage de domaine \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1087"><span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**ERROR\_DS\_CANT\_CREATE\_IN\_NONDOMAIN\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1088">8553 (0x2169)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1088">8553 (0x2169)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1089">Les objets principal de sécurité peuvent uniquement être créés dans des contextes d’attribution de noms de domaine.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1089">Security principal objects can only be created inside domain naming contexts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1090"><span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**ERREUR \_ \_ \_ de nom de service d’annuaire non valide \_ pour le \_ SPN**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1090"><span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**ERROR\_DS\_INVALID\_NAME\_FOR\_SPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1091">8554 (0x216A)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1091">8554 (0x216A)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1092">Impossible de construire un nom de principal du service (SPN) car le nom d’hôte fourni n’est pas au format nécessaire.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1092">A Service Principal Name (SPN) could not be constructed because the provided hostname is not in the necessary format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1093"><span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**ERREUR \_ le \_ filtre DS \_ utilise \_ construit \_ ATTRS**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1093"><span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**ERROR\_DS\_FILTER\_USES\_CONTRUCTED\_ATTRS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1094">8555 (0x216B)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1094">8555 (0x216B)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1095">Un filtre qui utilise des attributs construits a été passé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1095">A Filter was passed that uses constructed attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1096"><span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**ERREUR \_ \_ de l’erreur DS UNICODEPWD \_ non \_ entre \_ guillemets**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1096"><span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**ERROR\_DS\_UNICODEPWD\_NOT\_IN\_QUOTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1097">8556 (0x216C)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1097">8556 (0x216C)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1098">La valeur de l’attribut unicodePwd doit être placée entre guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1098">The unicodePwd attribute value must be enclosed in double quotes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1099"><span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**ERREUR \_ de \_ \_ dépassement du quota du compte d’ordinateur DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1099"><span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**ERROR\_DS\_MACHINE\_ACCOUNT\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1100">8557 (0x216D)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1100">8557 (0x216D)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1101">Votre ordinateur n’a pas pu être joint au domaine.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1101">Your computer could not be joined to the domain.</span></span> <span data-ttu-id="07c8f-1102">Vous avez dépassé le nombre maximal de comptes d’ordinateur que vous êtes autorisé à créer dans ce domaine.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1102">You have exceeded the maximum number of computer accounts you are allowed to create in this domain.</span></span> <span data-ttu-id="07c8f-1103">Contactez votre administrateur système pour que cette limite soit réinitialisée ou augmentée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1103">Contact your system administrator to have this limit reset or increased.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1104"><span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**l’erreur \_ DS \_ doit \_ être \_ exécutée \_ sur le \_ \_ contrôleur de domaine DST**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1104"><span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**ERROR\_DS\_MUST\_BE\_RUN\_ON\_DST\_DC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1105">8558 (0x216E)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1105">8558 (0x216E)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1106">Pour des raisons de sécurité, l’opération doit être exécutée sur le contrôleur de service de destination.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1106">For security reasons, the operation must be run on the destination DC.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1107"><span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**ERREUR \_ le \_ contrôleur de domaine SRC DS \_ \_ doit \_ être \_ \_ supérieur ou égal à SP4 \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1107"><span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**ERROR\_DS\_SRC\_DC\_MUST\_BE\_SP4\_OR\_GREATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1108">8559 (0x216F)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1108">8559 (0x216F)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1109">Pour des raisons de sécurité, le contrôleur de source doit être NT4SP4 ou supérieur.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1109">For security reasons, the source DC must be NT4SP4 or greater.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1110"><span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**ERREUR de suppression de l' \_ \_ \_ arborescence \_ \_ critique \_ du service d’annuaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1110"><span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**ERROR\_DS\_CANT\_TREE\_DELETE\_CRITICAL\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1111">8560 (0x2170)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1111">8560 (0x2170)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1112">Impossible de supprimer les objets de système de service d’annuaire critiques lors des opérations de suppression d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1112">Critical Directory Service System objects cannot be deleted during tree delete operations.</span></span> <span data-ttu-id="07c8f-1113">La suppression de l’arborescence a peut-être été effectuée partiellement.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1113">The tree delete may have been partially performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1114"><span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**ERREUR de la \_ \_ console d’échec d’initialisation DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1114"><span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**ERROR\_DS\_INIT\_FAILURE\_CONSOLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1115">8561 (0x2171)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1115">8561 (0x2171)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1116">Les services d’annuaire n’ont pas pu démarrer en raison de l’erreur suivante : %1.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1116">Directory Services could not start because of the following error: %1.</span></span> <span data-ttu-id="07c8f-1117">État d’erreur : 0x %2.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1117">Error Status: 0x%2.</span></span> <span data-ttu-id="07c8f-1118">Cliquez sur OK pour arrêter le système.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1118">Please click OK to shutdown the system.</span></span> <span data-ttu-id="07c8f-1119">Vous pouvez utiliser la console de récupération pour diagnostiquer le système de manière minutieuse.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1119">You can use the recovery console to diagnose the system further.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1120"><span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**ERREUR de la console d’échec de l' \_ \_ initialisation DS sam \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1120"><span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**ERROR\_DS\_SAM\_INIT\_FAILURE\_CONSOLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1121">8562 (0x2172)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1121">8562 (0x2172)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1122">L’initialisation du gestionnaire des comptes de sécurité a échoué en raison de l’erreur suivante : %1.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1122">Security Accounts Manager initialization failed because of the following error: %1.</span></span> <span data-ttu-id="07c8f-1123">État d’erreur : 0x %2.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1123">Error Status: 0x%2.</span></span> <span data-ttu-id="07c8f-1124">Cliquez sur OK pour arrêter le système.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1124">Please click OK to shutdown the system.</span></span> <span data-ttu-id="07c8f-1125">Vous pouvez utiliser la console de récupération pour diagnostiquer le système de manière minutieuse.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1125">You can use the recovery console to diagnose the system further.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1126"><span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**ERREUR \_ de \_ version de forêt DS \_ \_ trop \_ élevée**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1126"><span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**ERROR\_DS\_FOREST\_VERSION\_TOO\_HIGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1127">8563 (0x2173)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1127">8563 (0x2173)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1128">La version du système d’exploitation est incompatible avec le niveau fonctionnel actuel de la forêt AD DS ou AD LDS niveau fonctionnel du jeu de configuration.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1128">The version of the operating system is incompatible with the current AD DS forest functional level or AD LDS Configuration Set functional level.</span></span> <span data-ttu-id="07c8f-1129">Vous devez effectuer une mise à niveau vers une nouvelle version du système d’exploitation pour que ce serveur puisse devenir un contrôleur de domaine AD DS ou ajouter une instance de AD LDS dans ce AD DS forêt ou le jeu de configuration AD LDS.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1129">You must upgrade to a new version of the operating system before this server can become an AD DS Domain Controller or add an AD LDS Instance in this AD DS Forest or AD LDS Configuration Set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1130"><span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**ERREUR \_ de \_ version de domaine DS \_ \_ trop \_ élevée**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1130"><span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**ERROR\_DS\_DOMAIN\_VERSION\_TOO\_HIGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1131">8564 (0x2174)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1131">8564 (0x2174)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1132">La version du système d’exploitation installée n’est pas compatible avec le niveau fonctionnel du domaine actuel.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1132">The version of the operating system installed is incompatible with the current domain functional level.</span></span> <span data-ttu-id="07c8f-1133">Vous devez effectuer une mise à niveau vers une nouvelle version du système d’exploitation pour que ce serveur puisse devenir un contrôleur de domaine dans ce domaine.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1133">You must upgrade to a new version of the operating system before this server can become a domain controller in this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1134"><span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**ERREUR \_ de \_ version de forêt DS \_ \_ trop \_ faible**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1134"><span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**ERROR\_DS\_FOREST\_VERSION\_TOO\_LOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1135">8565 (0x2175)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1135">8565 (0x2175)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1136">La version du système d’exploitation installé sur ce serveur ne prend plus en charge le niveau fonctionnel actuel de la forêt AD DS ou AD LDS niveau fonctionnel du jeu de configuration.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1136">The version of the operating system installed on this server no longer supports the current AD DS Forest functional level or AD LDS Configuration Set functional level.</span></span> <span data-ttu-id="07c8f-1137">Vous devez élever le niveau fonctionnel de la forêt AD DS ou AD LDS niveau fonctionnel du jeu de configuration pour que ce serveur puisse devenir un contrôleur de domaine AD DS ou une instance de AD LDS dans cette forêt ou ce jeu de configuration.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1137">You must raise the AD DS Forest functional level or AD LDS Configuration Set functional level before this server can become an AD DS Domain Controller or an AD LDS Instance in this Forest or Configuration Set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1138"><span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**ERREUR \_ de \_ version du domaine DS \_ \_ trop \_ faible**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1138"><span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**ERROR\_DS\_DOMAIN\_VERSION\_TOO\_LOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1139">8566 (0x2176)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1139">8566 (0x2176)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1140">La version du système d’exploitation installé sur ce serveur ne prend plus en charge le niveau fonctionnel du domaine actuel.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1140">The version of the operating system installed on this server no longer supports the current domain functional level.</span></span> <span data-ttu-id="07c8f-1141">Vous devez augmenter le niveau fonctionnel du domaine pour que ce serveur puisse devenir un contrôleur de domaine dans ce domaine.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1141">You must raise the domain functional level before this server can become a domain controller in this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1142"><span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**ERREUR \_ de \_ version incompatible de DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1142"><span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**ERROR\_DS\_INCOMPATIBLE\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1143">8567 (0x2177)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1143">8567 (0x2177)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1144">La version du système d’exploitation installé sur ce serveur est incompatible avec le niveau fonctionnel du domaine ou de la forêt.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1144">The version of the operating system installed on this server is incompatible with the functional level of the domain or forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1145"><span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**ERREUR \_ DS \_ \_ version faible DSA \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1145"><span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**ERROR\_DS\_LOW\_DSA\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1146">8568 (0x2178)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1146">8568 (0x2178)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1147">Le niveau fonctionnel du domaine (ou de la forêt) ne peut pas être élevé à la valeur demandée, car il existe un ou plusieurs contrôleurs de domaine dans le domaine (ou la forêt) qui sont à un niveau fonctionnel inférieur incompatible.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1147">The functional level of the domain (or forest) cannot be raised to the requested value, because there exist one or more domain controllers in the domain (or forest) that are at a lower incompatible functional level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1148"><span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**ERREUR \_ DS \_ aucune \_ \_ version \_ de comportement dans \_ MIXEDDOMAIN**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1148"><span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**ERROR\_DS\_NO\_BEHAVIOR\_VERSION\_IN\_MIXEDDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1149">8569 (0x2179)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1149">8569 (0x2179)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1150">Le niveau fonctionnel de la forêt ne peut pas être élevé à la valeur demandée, car un ou plusieurs domaines sont toujours en mode de domaine mixte.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1150">The forest functional level cannot be raised to the requested value since one or more domains are still in mixed domain mode.</span></span> <span data-ttu-id="07c8f-1151">Tous les domaines de la forêt doivent être en mode natif, pour vous permettre d’augmenter le niveau fonctionnel de la forêt.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1151">All domains in the forest must be in native mode, for you to raise the forest functional level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1152"><span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**ordre de tri des erreurs d' \_ annuaire \_ non \_ pris en charge \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1152"><span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**ERROR\_DS\_NOT\_SUPPORTED\_SORT\_ORDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1153">8570 (0x217A)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1153">8570 (0x217A)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1154">L’ordre de tri demandé n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1154">The sort order requested is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1155"><span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**le \_ nom du service d’annuaire \_ \_ n’est pas \_ unique**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1155"><span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**ERROR\_DS\_NAME\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1156">8571 (0x217B)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1156">8571 (0x217B)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1157">Le nom demandé existe déjà en tant qu’identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1157">The requested name already exists as a unique identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1158"><span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**ERREUR \_ de \_ création du compte d’ordinateur DS \_ \_ \_ PRENT4**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1158"><span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**ERROR\_DS\_MACHINE\_ACCOUNT\_CREATED\_PRENT4**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1159">8572 (0x217C)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1159">8572 (0x217C)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1160">Le compte d’ordinateur a été créé avant NT4.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1160">The machine account was created pre-NT4.</span></span> <span data-ttu-id="07c8f-1161">Le compte doit être recréé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1161">The account needs to be recreated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1162"><span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**ERREUR \_ \_ de la \_ \_ Banque des versions du service d’annuaire \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1162"><span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**ERROR\_DS\_OUT\_OF\_VERSION\_STORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1163">8573 (0x217D)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1163">8573 (0x217D)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1164">La base de données est hors de la Banque des versions.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1164">The database is out of version store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1165"><span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**ERREUR de contrôle de l' \_ \_ incompatibilité des services DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1165"><span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**ERROR\_DS\_INCOMPATIBLE\_CONTROLS\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1166">8574 (0x217E)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1166">8574 (0x217E)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1167">Impossible de poursuivre l’opération, car plusieurs contrôles conflictuels ont été utilisés.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1167">Unable to continue operation because multiple conflicting controls were used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1168"><span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**ERREUR \_ DS \_ aucun \_ domaine de référence \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1168"><span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**ERROR\_DS\_NO\_REF\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1169">8575 (0x217F)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1169">8575 (0x217F)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1170">Impossible de trouver un domaine de référence de descripteur de sécurité valide pour cette partition.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1170">Unable to find a valid security descriptor reference domain for this partition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1171"><span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**\_ID de \_ \_ lien réservé \_ d’erreur DS**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1171"><span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**ERROR\_DS\_RESERVED\_LINK\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1172">8576 (0x2180)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1172">8576 (0x2180)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1173">Échec de la mise à jour du schéma : l’identificateur de lien est réservé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1173">Schema update failed: The link identifier is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1174"><span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**ERREUR \_ d' \_ ID de lien DS \_ \_ non \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1174"><span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**ERROR\_DS\_LINK\_ID\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1175">8577 (0x2181)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1175">8577 (0x2181)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1176">Échec de la mise à jour du schéma : aucun identificateur de lien n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1176">Schema update failed: There are no link identifiers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1177"><span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**ERREUR \_ DS \_ AG \_ \_ ne pas avoir de \_ \_ membre universel**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1177"><span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**ERROR\_DS\_AG\_CANT\_HAVE\_UNIVERSAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1178">8578 (0x2182)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1178">8578 (0x2182)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1179">Un groupe de comptes ne peut pas avoir un groupe universel en tant que membre.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1179">An account group cannot have a universal group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1180"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**ERREUR \_ DS \_ modifyDN non \_ autorisée \_ par \_ type d’instance \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1180"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**ERROR\_DS\_MODIFYDN\_DISALLOWED\_BY\_INSTANCE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1181">8579 (0x2183)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1181">8579 (0x2183)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1182">Les opérations de renommage ou de déplacement sur des têtes de contexte d’appellation ou des objets en lecture seule ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1182">Rename or move operations on naming context heads or read-only objects are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1183"><span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**ERREUR \_ DS \_ aucun \_ \_ déplacement \_ d’objet dans le \_ contexte de nommage de schéma \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1183"><span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**ERROR\_DS\_NO\_OBJECT\_MOVE\_IN\_SCHEMA\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1184">8580 (0x2184)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1184">8580 (0x2184)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1185">Les opérations de déplacement sur les objets dans le contexte de nommage de schéma ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1185">Move operations on objects in the schema naming context are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1186"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**ERREUR \_ DS \_ modifyDN non \_ autorisée \_ par l' \_ indicateur**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1186"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**ERROR\_DS\_MODIFYDN\_DISALLOWED\_BY\_FLAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1187">8581 (0x2185)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1187">8581 (0x2185)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1188">Un indicateur système a été défini sur l’objet et ne permet pas de déplacer ou de renommer l’objet.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1188">A system flag has been set on the object and does not allow the object to be moved or renamed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1189"><span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**ERREUR \_ DS modifyDN le grand- \_ \_ parent incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1189"><span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**ERROR\_DS\_MODIFYDN\_WRONG\_GRANDPARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1190">8582 (0x2186)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1190">8582 (0x2186)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1191">Cet objet n’est pas autorisé à modifier son conteneur grand-parent.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1191">This object is not allowed to change its grandparent container.</span></span> <span data-ttu-id="07c8f-1192">Les déplacements ne sont pas interdits sur cet objet, mais sont limités aux conteneurs frères.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1192">Moves are not forbidden on this object, but are restricted to sibling containers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1193"><span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**ERREUR de référence de l' \_ approbation d’erreur de nom de service d’annuaire \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1193"><span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**ERROR\_DS\_NAME\_ERROR\_TRUST\_REFERRAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1194">8583 (0x2187)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1194">8583 (0x2187)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1195">Impossible de résoudre complètement, une référence à une autre forêt est générée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1195">Unable to resolve completely, a referral to another forest is generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1196"><span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**ERREUR \_ non \_ prise en charge \_ sur le \_ \_ serveur standard**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1196"><span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**ERROR\_NOT\_SUPPORTED\_ON\_STANDARD\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1197">8584 (0x2188)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1197">8584 (0x2188)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1198">L’action demandée n’est pas prise en charge sur le serveur standard.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1198">The requested action is not supported on standard server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1199"><span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**ERREUR \_ DS \_ Impossible \_ \_ d’accéder à la partie distante \_ \_ d' \_ ad**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1199"><span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**ERROR\_DS\_CANT\_ACCESS\_REMOTE\_PART\_OF\_AD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1200">8585 (0x2189)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1200">8585 (0x2189)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1201">Impossible d’accéder à une partition du service d’annuaire situé sur un serveur distant.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1201">Could not access a partition of the directory service located on a remote server.</span></span> <span data-ttu-id="07c8f-1202">Assurez-vous qu’au moins un serveur est en cours d’exécution pour la partition en question.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1202">Make sure at least one server is running for the partition in question.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1203"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**ERREUR \_ DS \_ CR \_ Impossible \_ de \_ valider \_ v2**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1203"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**ERROR\_DS\_CR\_IMPOSSIBLE\_TO\_VALIDATE\_V2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1204">8586 (0x218A)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1204">8586 (0x218A)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1205">Le répertoire ne peut pas valider le nom de contexte de nommage (ou de partition) proposé, car il ne contient pas de réplica et ne peut pas contacter un réplica du contexte d’appellation au-dessus du contexte de nommage proposé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1205">The directory cannot validate the proposed naming context (or partition) name because it does not hold a replica nor can it contact a replica of the naming context above the proposed naming context.</span></span> <span data-ttu-id="07c8f-1206">Assurez-vous que le contexte de nommage parent est correctement inscrit dans DNS, et qu’au moins un réplica de ce contexte de nommage est accessible par le maître d’attribution de noms de domaine.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1206">Please ensure that the parent naming context is properly registered in DNS, and at least one replica of this naming context is reachable by the Domain Naming master.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1207"><span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**limite de threads de l’annuaire des erreurs \_ \_ \_ \_ dépassée**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1207"><span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**ERROR\_DS\_THREAD\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1208">8587 (0x218B)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1208">8587 (0x218B)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1209">La limite de threads pour cette requête a été dépassée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1209">The thread limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1210"><span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**ERREUR \_ DS \_ non \_ plus proche**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1210"><span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**ERROR\_DS\_NOT\_CLOSEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1211">8588 (0x218C)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1211">8588 (0x218C)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1212">Le serveur de catalogue global n’est pas sur le site le plus proche.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1212">The Global catalog server is not in the closest site.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1213"><span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**ERREUR \_ DS \_ Impossible de \_ dériver le \_ SPN \_ sans \_ serveur de \_ référence**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1213"><span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**ERROR\_DS\_CANT\_DERIVE\_SPN\_WITHOUT\_SERVER\_REF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1214">8589 (0x218D)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1214">8589 (0x218D)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1215">Le DS ne peut pas dériver un nom de principal du service (SPN) avec lequel authentifier mutuellement le serveur cible, car l’objet serveur correspondant dans la base de données DS locale n’a pas d’attribut serverReference.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1215">The DS cannot derive a service principal name (SPN) with which to mutually authenticate the target server because the corresponding server object in the local DS database has no serverReference attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1216"><span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**ERREUR \_ \_ échec du mode mono-utilisateur du service d’annuaire \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1216"><span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**ERROR\_DS\_SINGLE\_USER\_MODE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1217">8590 (0x218E)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1217">8590 (0x218E)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1218">Le service d’annuaire n’a pas pu passer en mode mono-utilisateur.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1218">The Directory Service failed to enter single user mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1219"><span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**erreur \_ de \_ syntaxe de NTDSCRIPT du service d’annuaire \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1219"><span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**ERROR\_DS\_NTDSCRIPT\_SYNTAX\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1220">8591 (0x218F)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1220">8591 (0x218F)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1221">Le service d’annuaire ne peut pas analyser le script en raison d’une erreur de syntaxe.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1221">The Directory Service cannot parse the script because of a syntax error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1222"><span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**erreur \_ de \_ \_ traitement NTDSCRIPT \_ de l’annuaire d’erreurs**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1222"><span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**ERROR\_DS\_NTDSCRIPT\_PROCESS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1223">8592 (0x2190)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1223">8592 (0x2190)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1224">Le service d’annuaire ne peut pas traiter le script en raison d’une erreur.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1224">The Directory Service cannot process the script because of an error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1225"><span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**ERREUR \_ des \_ \_ époques de réplication différente DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1225"><span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**ERROR\_DS\_DIFFERENT\_REPL\_EPOCHS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1226">8593 (0x2191)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1226">8593 (0x2191)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1227">Le service d’annuaire ne peut pas effectuer l’opération demandée, car les serveurs impliqués ont des époques de réplication différentes (généralement liées à un changement de nom de domaine en cours).</span><span class="sxs-lookup"><span data-stu-id="07c8f-1227">The directory service cannot perform the requested operation because the servers involved are of different replication epochs (which is usually related to a domain rename that is in progress).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1228"><span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**ERREUR \_ de \_ \_ modification des extensions \_ des services d’annuaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1228"><span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**ERROR\_DS\_DRS\_EXTENSIONS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1229">8594 (0x2192)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1229">8594 (0x2192)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1230">La liaison de service d’annuaire doit être renégociée en raison d’une modification des informations des extensions serveur.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1230">The directory service binding must be renegotiated due to a change in the server extensions information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1231"><span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**ERREUR \_ \_ \_ de modification du jeu de réplicas DS \_ \_ non \_ autorisée \_ sur un \_ \_ CR désactivé**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1231"><span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**ERROR\_DS\_REPLICA\_SET\_CHANGE\_NOT\_ALLOWED\_ON\_DISABLED\_CR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1232">8595 (0x2193)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1232">8595 (0x2193)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1233">Opération non autorisée sur une référence croisée désactivée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1233">Operation not allowed on a disabled cross ref.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1234"><span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**ERREUR \_ DS \_ no \_ MSDS \_ IntID**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1234"><span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**ERROR\_DS\_NO\_MSDS\_INTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1235">8596 (0x2194)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1235">8596 (0x2194)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1236">Échec de la mise à jour du schéma : aucune valeur pour msDS-IntId n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1236">Schema update failed: No values for msDS-IntId are available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1237"><span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**ERREUR \_ MSDS de l' \_ attribut de reduplication du DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1237"><span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**ERROR\_DS\_DUP\_MSDS\_INTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1238">8597 (0x2195)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1238">8597 (0x2195)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1239">Échec de la mise à jour du schéma : msDS-INtId dupliqué.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1239">Schema update failed: Duplicate msDS-INtId.</span></span> <span data-ttu-id="07c8f-1240">Retentez l’opération.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1240">Retry the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1241"><span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**\_l’erreur DS \_ existe \_ dans \_ RDNATTID**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1241"><span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**ERROR\_DS\_EXISTS\_IN\_RDNATTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1242">8598 (0x2196)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1242">8598 (0x2196)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1243">Échec de la suppression du schéma : l’attribut est utilisé dans rDNAttID.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1243">Schema deletion failed: attribute is used in rDNAttID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1244"><span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**ERREUR \_ échec de l’autorisation du service \_ d’annuaire \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1244"><span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**ERROR\_DS\_AUTHORIZATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1245">8599 (0x2197)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1245">8599 (0x2197)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1246">Le service d’annuaire n’a pas pu autoriser la demande.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1246">The directory service failed to authorize the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1247"><span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**ERREUR \_ de \_ script DS non valide \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1247"><span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**ERROR\_DS\_INVALID\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1248">8600 (0x2198)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1248">8600 (0x2198)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1249">Le service d’annuaire ne peut pas traiter le script, car il n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1249">The Directory Service cannot process the script because it is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1250"><span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**erreur Échec de l’opération de l’erreur de la \_ \_ CROSSREF à distance DS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1250"><span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**ERROR\_DS\_REMOTE\_CROSSREF\_OP\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1251">8601 (0x2199)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1251">8601 (0x2199)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1252">Échec de l’opération de création d’une référence croisée distante sur le FSMO du maître d’attribution de noms de domaine.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1252">The remote create cross reference operation failed on the Domain Naming Master FSMO.</span></span> <span data-ttu-id="07c8f-1253">L’erreur de l’opération se trouve dans les données étendues.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1253">The operation's error is in the extended data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1254"><span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**ERREUR \_ \_ croisée de \_ référence des \_ services de domaine Active Directory**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1254"><span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**ERROR\_DS\_CROSS\_REF\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1255">8602 (0x219A)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1255">8602 (0x219A)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1256">Une référence croisée est en cours d’utilisation localement avec le même nom.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1256">A cross reference is in use locally with the same name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1257"><span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**ERREUR \_ DS \_ Impossible \_ de dériver le \_ SPN \_ pour le \_ \_ domaine supprimé**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1257"><span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**ERROR\_DS\_CANT\_DERIVE\_SPN\_FOR\_DELETED\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1258">8603 (0x219B)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1258">8603 (0x219B)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1259">Le DS ne peut pas dériver un nom de principal du service (SPN) avec lequel authentifier mutuellement le serveur cible, car le domaine du serveur a été supprimé de la forêt.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1259">The DS cannot derive a service principal name (SPN) with which to mutually authenticate the target server because the server's domain has been deleted from the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1260"><span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**ERREUR \_ DS \_ Impossible \_ de rétrograder \_ avec le \_ contexte de \_ nommage inscriptible**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1260"><span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**ERROR\_DS\_CANT\_DEMOTE\_WITH\_WRITEABLE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1261">8604 (0x219C)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1261">8604 (0x219C)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1262">Les NC inscriptibles empêchent ce contrôleur de l’être de rétrograder.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1262">Writeable NCs prevent this DC from demoting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1263"><span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**ERREUR \_ ID dupliqué de l’annuaire de services \_ \_ \_ trouvée**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1263"><span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**ERROR\_DS\_DUPLICATE\_ID\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1264">8605 (0x219D)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1264">8605 (0x219D)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1265">L’objet demandé a un identificateur non unique et ne peut pas être récupéré.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1265">The requested object has a non-unique identifier and cannot be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1266"><span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**ERREUR \_ Impossible \_ pour l’attr insuffisant \_ \_ pour \_ créer un \_ objet**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1266"><span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**ERROR\_DS\_INSUFFICIENT\_ATTR\_TO\_CREATE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1267">8606 (0x219E)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1267">8606 (0x219E)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1268">Des attributs insuffisants ont été donnés pour créer un objet.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1268">Insufficient attributes were given to create an object.</span></span> <span data-ttu-id="07c8f-1269">Cet objet n’existe peut-être pas, car il a peut-être été supprimé et a déjà été récupéré par le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1269">This object may not exist because it may have been deleted and already garbage collected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1270"><span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**erreur \_ de \_ conversion du groupe des services d’annuaire \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1270"><span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**ERROR\_DS\_GROUP\_CONVERSION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1271">8607 (0x219F)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1271">8607 (0x219F)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1272">Le groupe ne peut pas être converti en raison de restrictions d’attribut sur le type de groupe demandé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1272">The group cannot be converted due to attribute restrictions on the requested group type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1273"><span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**ERREUR \_ DS \_ Impossible de \_ déplacer le \_ \_ groupe de base \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1273"><span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**ERROR\_DS\_CANT\_MOVE\_APP\_BASIC\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1274">8608 (0x21A0)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1274">8608 (0x21A0)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1275">Le déplacement entre domaines de groupes d’applications de base non vides n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1275">Cross-domain move of non-empty basic application groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1276"><span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**ERREUR \_ DS \_ Impossible de \_ déplacer le groupe de \_ requêtes d’application \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1276"><span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**ERROR\_DS\_CANT\_MOVE\_APP\_QUERY\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1277">8609 (0x21A1)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1277">8609 (0x21A1)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1278">Le déplacement entre domaines d’un groupe d’applications non vide basé sur une requête n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1278">Cross-domain move of non-empty query based application groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1279"><span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**le rôle de l’annuaire d’erreurs \_ \_ n’a \_ pas été \_ vérifié**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1279"><span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**ERROR\_DS\_ROLE\_NOT\_VERIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1280">8610 (0x21A2)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1280">8610 (0x21A2)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1281">La propriété du rôle FSMO n’a pas pu être vérifiée, car sa partition d’annuaire n’a pas été répliquée avec au moins un partenaire de réplication.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1281">The FSMO role ownership could not be verified because its directory partition has not replicated successfully with at least one replication partner.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1282"><span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**ERREUR \_ le \_ conteneur WKO DS \_ \_ ne peut pas \_ être \_ spécial**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1282"><span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**ERROR\_DS\_WKO\_CONTAINER\_CANNOT\_BE\_SPECIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1283">8611 (0x21A3)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1283">8611 (0x21A3)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1284">Le conteneur cible pour une redirection d’un conteneur d’objets bien connu ne peut pas déjà être un conteneur spécial.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1284">The target container for a redirection of a well known object container cannot already be a special container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1285"><span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**ERREUR \_ \_ \_ de changement de nom \_ de domaine DS en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1285"><span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**ERROR\_DS\_DOMAIN\_RENAME\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1286">8612 (0x21A4)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1286">8612 (0x21A4)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1287">Le service d’annuaire ne peut pas effectuer l’opération demandée, car une opération de changement de nom de domaine est en cours.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1287">The Directory Service cannot perform the requested operation because a domain rename operation is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1288"><span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**ERREUR \_ du \_ \_ contexte de \_ nommage enfant ad \_ de l’annuaire Active Directory existant**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1288"><span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**ERROR\_DS\_EXISTING\_AD\_CHILD\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1289">8613 (0x21A5)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1289">8613 (0x21A5)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1290">Le service d’annuaire a détecté une partition enfant sous le nom de partition demandé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1290">The directory service detected a child partition below the requested partition name.</span></span> <span data-ttu-id="07c8f-1291">La hiérarchie de la partition doit être créée dans une méthode de haut en haut.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1291">The partition hierarchy must be created in a top down method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1292"><span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**ERREUR \_ de \_ durée de vie de réplication DS \_ \_ dépassée**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1292"><span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**ERROR\_DS\_REPL\_LIFETIME\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1293">8614 (0x21A6)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1293">8614 (0x21A6)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1294">Le service d’annuaire ne peut pas répliquer avec ce serveur, car la durée de vie de la dernière réplication avec ce serveur a dépassé la durée de vie de désactivation.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1294">The directory service cannot replicate with this server because the time since the last replication with this server has exceeded the tombstone lifetime.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1295"><span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**ERREUR \_ DS non \_ autorisée \_ dans le \_ \_ conteneur système**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1295"><span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**ERROR\_DS\_DISALLOWED\_IN\_SYSTEM\_CONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1296">8615 (0x21A7)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1296">8615 (0x21A7)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1297">L’opération demandée n’est pas autorisée sur un objet sous le conteneur système.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1297">The requested operation is not allowed on an object under the system container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1298"><span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**ERREUR de saturation de la \_ \_ \_ \_ file d’attente d’envoi LDAP DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1298"><span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**ERROR\_DS\_LDAP\_SEND\_QUEUE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1299">8616 (0x21A8)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1299">8616 (0x21A8)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1300">La file d’attente d’envoi réseau des serveurs LDAP a été remplie car le client ne traite pas les résultats de ses demandes suffisamment rapidement.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1300">The LDAP servers network send queue has filled up because the client is not processing the results of its requests fast enough.</span></span> <span data-ttu-id="07c8f-1301">Aucune demande supplémentaire n’est traitée tant que le client n’a pas effectué la capture.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1301">No more requests will be processed until the client catches up.</span></span> <span data-ttu-id="07c8f-1302">Si le client ne rattrape pas le problème, il sera déconnecté.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1302">If the client does not catch up then it will be disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1303"><span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**fenêtre d’erreur de planification de la récupération du \_ service d’annuaire \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1303"><span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**ERROR\_DS\_DRA\_OUT\_SCHEDULE\_WINDOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1304">8617 (0x21A9)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1304">8617 (0x21A9)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1305">La réplication planifiée n’a pas eu lieu car le système était trop occupé pour exécuter la demande dans la fenêtre de planification.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1305">The scheduled replication did not take place because the system was too busy to execute the request within the schedule window.</span></span> <span data-ttu-id="07c8f-1306">La file d’attente de réplication est surchargée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1306">The replication queue is overloaded.</span></span> <span data-ttu-id="07c8f-1307">Envisagez de réduire le nombre de partenaires ou de réduire la fréquence de réplication planifiée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1307">Consider reducing the number of partners or decreasing the scheduled replication frequency.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1308"><span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**ERREUR \_ de \_ stratégie DS \_ non \_ connue**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1308"><span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**ERROR\_DS\_POLICY\_NOT\_KNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1309">8618 (0x21AA)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1309">8618 (0x21AA)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1310">À ce stade, il n’est pas possible de déterminer si la stratégie de réplication de branche est disponible sur le contrôleur de domaine Hub.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1310">At this time, it cannot be determined if the branch replication policy is available on the hub domain controller.</span></span> <span data-ttu-id="07c8f-1311">Réessayez ultérieurement pour prendre en compte les latences de réplication.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1311">Please retry at a later time to account for replication latencies.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1312"><span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**ERREUR \_ aucun \_ \_ objet paramètres de site \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1312"><span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**ERROR\_NO\_SITE\_SETTINGS\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1313">8619 (0x21AB)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1313">8619 (0x21AB)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1314">L’objet de paramètres de site pour le site spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1314">The site settings object for the specified site does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1315"><span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**ERREUR \_ aucun \_ secret**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1315"><span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**ERROR\_NO\_SECRETS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1316">8620 (0x21AC)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1316">8620 (0x21AC)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1317">Le magasin de comptes local ne contient pas de matériel secret pour le compte spécifié.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1317">The local account store does not contain secret material for the specified account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1318"><span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**ERREUR \_ aucun \_ contrôleur de périphérique accessible en écriture \_ \_ trouvé**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1318"><span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**ERROR\_NO\_WRITABLE\_DC\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1319">8621 (0x21AD)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1319">8621 (0x21AD)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1320">Impossible de trouver un contrôleur de domaine accessible en écriture dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1320">Could not find a writable domain controller in the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1321"><span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**ERREUR \_ DS \_ aucun \_ \_ objet serveur**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1321"><span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**ERROR\_DS\_NO\_SERVER\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1322">8622 (0x21AE)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1322">8622 (0x21AE)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1323">L’objet serveur pour le contrôleur de domaine n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1323">The server object for the domain controller does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1324"><span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**ERREUR \_ DS \_ no \_ ntdsa \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1324"><span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**ERROR\_DS\_NO\_NTDSA\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1325">8623 (0x21AF)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1325">8623 (0x21AF)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1326">L’objet Paramètres NTDS pour le contrôleur de domaine n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1326">The NTDS Settings object for the domain controller does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1327"><span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**ERREUR \_ DS \_ \_ recherche non ASQ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1327"><span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**ERROR\_DS\_NON\_ASQ\_SEARCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1328">8624 (0x21B0)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1328">8624 (0x21B0)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1329">L’opération de recherche demandée n’est pas prise en charge pour les recherches ASQ.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1329">The requested search operation is not supported for ASQ searches.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1330"><span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**ERREUR \_ \_ d’audit du service d’annuaire \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1330"><span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**ERROR\_DS\_AUDIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1331">8625 (0x21B1)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1331">8625 (0x21B1)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1332">Un événement d’audit requis n’a pas pu être généré pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1332">A required audit event could not be generated for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1333"><span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**ERREUR de sous-arborescence de l' \_ \_ indicateur de recherche non valide DS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1333"><span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**ERROR\_DS\_INVALID\_SEARCH\_FLAG\_SUBTREE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1334">8626 (0x21B2)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1334">8626 (0x21B2)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1335">Les indicateurs de recherche de l’attribut ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1335">The search flags for the attribute are invalid.</span></span> <span data-ttu-id="07c8f-1336">Le bit d’index de sous-arborescence n’est valide que sur des attributs à valeur unique.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1336">The subtree index bit is valid only on single valued attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1337"><span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**ERREUR du TUPLE de l' \_ \_ indicateur de recherche non valide DS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1337"><span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**ERROR\_DS\_INVALID\_SEARCH\_FLAG\_TUPLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1338">8627 (0x21B3)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1338">8627 (0x21B3)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1339">Les indicateurs de recherche de l’attribut ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1339">The search flags for the attribute are invalid.</span></span> <span data-ttu-id="07c8f-1340">Le bit d’index de tuple est valide uniquement sur les attributs de chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1340">The tuple index bit is valid only on attributes of Unicode strings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1341"><span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**ERREUR de \_ table de hiérarchie des services d’annuaire \_ \_ \_ trop \_ profonde**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1341"><span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**ERROR\_DS\_HIERARCHY\_TABLE\_TOO\_DEEP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1342">8628 (0x21B4)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1342">8628 (0x21B4)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1343">Les carnets d’adresses sont imbriqués trop profondément.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1343">The address books are nested too deeply.</span></span> <span data-ttu-id="07c8f-1344">Échec de la création de la table de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1344">Failed to build the hierarchy table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1345"><span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**ERREUR \_ du \_ \_ \_ vecteur UTD) de l’agent DRA endommagé \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1345"><span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**ERROR\_DS\_DRA\_CORRUPT\_UTD\_VECTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1346">8629 (0x21B5)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1346">8629 (0x21B5)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1347">Le vecteur d’inscription à jour spécifié est endommagé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1347">The specified up-to-date-ness vector is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1348"><span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**ERREUR \_ de \_ \_ secrets DRA \_ refusés**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1348"><span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**ERROR\_DS\_DRA\_SECRETS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1349">8630 (0x21B6)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1349">8630 (0x21B6)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1350">La demande de réplication des secrets est refusée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1350">The request to replicate secrets is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1351"><span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**\_ \_ \_ ID MAPI réservé de l’annuaire d’erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1351"><span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**ERROR\_DS\_RESERVED\_MAPI\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1352">8631 (0x21B7)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1352">8631 (0x21B7)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1353">Échec de la mise à jour du schéma : l’identificateur MAPI est réservé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1353">Schema update failed: The MAPI identifier is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1354"><span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**ERREUR de l' \_ \_ ID MAPI MAPI \_ \_ non \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1354"><span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**ERROR\_DS\_MAPI\_ID\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1355">8632 (0x21B8)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1355">8632 (0x21B8)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1356">Échec de la mise à jour du schéma : aucun identificateur MAPI n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1356">Schema update failed: There are no MAPI identifiers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1357"><span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**ERREUR \_ le \_ \_ \_ secret krbtgt est manquant dans le DRA du DS \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1357"><span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**ERROR\_DS\_DRA\_MISSING\_KRBTGT\_SECRET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1358">8633 (0x21B9)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1358">8633 (0x21B9)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1359">L’opération de réplication a échoué car les attributs requis de l’objet krbtgt local sont manquants.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1359">The replication operation failed because the required attributes of the local krbtgt object are missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1360"><span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**ERREUR \_ le \_ \_ nom de domaine DS \_ existe dans la \_ \_ forêt**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1360"><span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**ERROR\_DS\_DOMAIN\_NAME\_EXISTS\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1361">8634 (0x21BA)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1361">8634 (0x21BA)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1362">Le nom de domaine du domaine approuvé existe déjà dans la forêt.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1362">The domain name of the trusted domain already exists in the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1363"><span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**ERREUR \_ \_ \_ de nom plat DS dans la \_ \_ \_ forêt**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1363"><span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**ERROR\_DS\_FLAT\_NAME\_EXISTS\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1364">8635 (0x21BB)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1364">8635 (0x21BB)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1365">Le nom plat du domaine approuvé existe déjà dans la forêt.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1365">The flat name of the trusted domain already exists in the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1366"><span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**ERREUR \_ \_ nom d’utilisateur \_ principal \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1366"><span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**ERROR\_INVALID\_USER\_PRINCIPAL\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1367">8636 (0x21BC)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1367">8636 (0x21BC)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1368">Le nom d’utilisateur principal (UPN) n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1368">The User Principal Name (UPN) is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1369"><span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**ERREUR \_ le \_ groupe mappé de l’OID des services de domaine \_ \_ \_ \_ a des \_ membres**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1369"><span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**ERROR\_DS\_OID\_MAPPED\_GROUP\_CANT\_HAVE\_MEMBERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1370">8637 (0x21BD)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1370">8637 (0x21BD)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1371">Les groupes mappés OID ne peuvent pas avoir de membres.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1371">OID mapped groups cannot have members.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1372"><span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**ERREUR de l' \_ OID du DS \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1372"><span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**ERROR\_DS\_OID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1373">8638 (0x21BE)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1373">8638 (0x21BE)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1374">L’OID spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1374">The specified OID cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1375"><span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**ERREUR de la \_ \_ \_ cible recyclée DRA \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1375"><span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**ERROR\_DS\_DRA\_RECYCLED\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1376">8639 (0x21BF)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1376">8639 (0x21BF)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1377">L’opération de réplication a échoué, car l’objet cible référencé par une valeur de lien est recyclé.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1377">The replication operation failed because the target object referred by a link value is recycled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1378"><span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**ERREUR \_ de \_ \_ redirection NC non autorisée dans le service d’annuaire \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1378"><span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**ERROR\_DS\_DISALLOWED\_NC\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1379">8640 (0x21C0)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1379">8640 (0x21C0)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1380">L’opération de redirection a échoué, car l’objet cible est dans un contexte de nommage différent du contexte de nommage de domaine du contrôleur de domaine actuel.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1380">The redirect operation failed because the target object is in a NC different from the domain NC of the current domain controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1381"><span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**ERREUR \_ DS \_ High \_ ADLDS \_ FFL**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1381"><span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**ERROR\_DS\_HIGH\_ADLDS\_FFL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1382">8641 (0x21C1)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1382">8641 (0x21C1)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1383">Le niveau fonctionnel du jeu de configuration AD LDS ne peut pas être abaissé à la valeur demandée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1383">The functional level of the AD LDS configuration set cannot be lowered to the requested value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1384"><span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**ERREUR \_ de \_ \_ version DSA \_ élevée du DS**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1384"><span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**ERROR\_DS\_HIGH\_DSA\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1385">8642 (0x21C2)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1385">8642 (0x21C2)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1386">Le niveau fonctionnel du domaine (ou de la forêt) ne peut pas être abaissé à la valeur demandée.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1386">The functional level of the domain (or forest) cannot be lowered to the requested value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1387"><span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**ERREUR \_ DS \_ Low \_ ADLDS \_ FFL**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1387"><span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**ERROR\_DS\_LOW\_ADLDS\_FFL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1388">8643 (0x21C3)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1388">8643 (0x21C3)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1389">Le niveau fonctionnel du jeu de configuration AD LDS ne peut pas être élevé à la valeur demandée, car il existe une ou plusieurs instances ADLDS qui ont un niveau fonctionnel inférieur incompatible.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1389">The functional level of the AD LDS configuration set cannot be raised to the requested value, because there exist one or more ADLDS instances that are at a lower incompatible functional level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1390"><span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**SID du domaine d’erreur \_ \_ \_ identique \_ à la \_ station de \_ travail locale**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1390"><span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**ERROR\_DOMAIN\_SID\_SAME\_AS\_LOCAL\_WORKSTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1391">8644 (0x21C4)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1391">8644 (0x21C4)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1392">La jonction de domaine ne peut pas être effectuée, car le SID du domaine que vous avez tenté de joindre était identique au SID de cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1392">The domain join cannot be completed because the SID of the domain you attempted to join was identical to the SID of this machine.</span></span> <span data-ttu-id="07c8f-1393">Il s’agit d’un symptôme de l’installation d’un système d’exploitation cloné de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1393">This is a symptom of an improperly cloned operating system install.</span></span> <span data-ttu-id="07c8f-1394">Vous devez exécuter Sysprep sur cet ordinateur afin de générer un nouveau SID d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1394">You should run sysprep on this machine in order to generate a new machine SID.</span></span> <span data-ttu-id="07c8f-1395">Pour plus d’informations, consultez <https://go.microsoft.com/fwlink/p/?linkid=168895>.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1395">Please see <https://go.microsoft.com/fwlink/p/?linkid=168895> for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1396"><span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**ERREUR \_ \_ échec de la \_ \_ validation sam \_ de l’annulation de la suppression du service d’annuaire**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1396"><span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**ERROR\_DS\_UNDELETE\_SAM\_VALIDATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1397">8645 (0x21C5)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1397">8645 (0x21C5)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1398">L’opération d’annulation de suppression a échoué, car le nom de compte Sam ou le nom de compte Sam supplémentaire de l’objet en cours de restauration est en conflit avec un objet dynamique existant.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1398">The undelete operation failed because the Sam Account Name or Additional Sam Account Name of the object being undeleted conflicts with an existing live object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07c8f-1399"><span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**ERREUR \_ de \_ type de compte incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="07c8f-1399"><span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**ERROR\_INCORRECT\_ACCOUNT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c8f-1400">8646 (0x21C6)</span><span class="sxs-lookup"><span data-stu-id="07c8f-1400">8646 (0x21C6)</span></span>
</dt> <dt>



<span data-ttu-id="07c8f-1401">Le système ne fait pas autorité pour le compte spécifié et ne peut donc pas terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1401">The system is not authoritative for the specified account and therefore cannot complete the operation.</span></span> <span data-ttu-id="07c8f-1402">Recommencez l’opération en utilisant le fournisseur associé à ce compte.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1402">Please retry the operation using the provider associated with this account.</span></span> <span data-ttu-id="07c8f-1403">S’il s’agit d’un fournisseur en ligne, utilisez le site en ligne du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="07c8f-1403">If this is an online provider please use the provider's online site.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="07c8f-1404">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07c8f-1404">Requirements</span></span>



| <span data-ttu-id="07c8f-1405">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07c8f-1405">Requirement</span></span> | <span data-ttu-id="07c8f-1406">Valeur</span><span class="sxs-lookup"><span data-stu-id="07c8f-1406">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07c8f-1407">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07c8f-1407">Minimum supported client</span></span><br/> | <span data-ttu-id="07c8f-1408">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07c8f-1408">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="07c8f-1409">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07c8f-1409">Minimum supported server</span></span><br/> | <span data-ttu-id="07c8f-1410">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07c8f-1410">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="07c8f-1411">En-tête</span><span class="sxs-lookup"><span data-stu-id="07c8f-1411">Header</span></span><br/>                   | <dl> <span data-ttu-id="07c8f-1412"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="07c8f-1412"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07c8f-1413">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07c8f-1413">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07c8f-1414">Codes d’erreur système</span><span class="sxs-lookup"><span data-stu-id="07c8f-1414">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




