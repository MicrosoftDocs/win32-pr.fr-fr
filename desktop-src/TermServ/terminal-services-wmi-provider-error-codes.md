---
title: Codes d’erreur du fournisseur WMI Services Bureau à distance (Wbemcli. h)
description: Erreurs retournées par le fournisseur WMI Services Bureau à distance. Pour obtenir la liste des autres erreurs WMI, consultez constantes d’erreur WMI.
ms.assetid: 1e68c41d-f321-4bc5-ba30-b69f5ba741eb
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WBEM_E_FAILED
- WBEM_E_NOT_FOUND
- WBEM_E_PROVIDER_FAILURE
- WBEM_E_TYPE_MISMATCH
- WBEM_E_OUT_OF_MEMORY
- WBEM_E_INVALID_PARAMETER
- WBEM_E_NOT_AVAILABLE
- WBEM_E_NOT_SUPPORTED
- WBEM_E_INVALID_NAMESPACE
- WBEM_E_INVALID_OBJECT
- WBEM_E_INITIALIZATION_FAILURE
- WBEM_E_INVALID_OPERATION
- WBEM_E_INVALID_QUERY
- WBEM_E_INVALID_QUERY_TYPE
- WBEM_E_ALREADY_EXISTS
- WBEM_E_INVALID_SYNTAX
- WBEM_E_READ_ONLY
- WBEM_E_PROVIDER_NOT_CAPABLE
- WBEM_E_ILLEGAL_NULL
- WBEM_E_VALUE_OUT_OF_RANGE
- WBEM_E_INVALID_METHOD
- WBEM_E_INVALID_METHOD_PARAMETERS
- WBEM_E_INVALID_OBJECT_PATH
api_location:
- Wbemcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252015a5d80a1487033ad285ce3080f4d666f0c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509382"
---
# <a name="remote-desktop-services-wmi-provider-error-codes"></a><span data-ttu-id="0c0f0-104">Codes d’erreur du fournisseur WMI Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="0c0f0-104">Remote Desktop Services WMI provider error codes</span></span>

<span data-ttu-id="0c0f0-105">La liste suivante répertorie les erreurs WMI retournées par le fournisseur WMI Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-105">The following list lists the WMI errors returned by the Remote Desktop Services WMI provider.</span></span> <span data-ttu-id="0c0f0-106">Pour obtenir la liste des autres erreurs WMI, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="0c0f0-106">For a list of other WMI errors, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="0c0f0-107"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**échec de WBEM \_ E \_**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-107"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM\_E\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-108">2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-108">2147749889 (0x80041001)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-109">Échec de l'appel de la méthode.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-109">The method call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-110"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-110"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM\_E\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-111">2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-111">2147749890 (0x80041002)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-112">L'objet est introuvable.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-112">The object could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-113"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**\_échec du \_ fournisseur WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-113"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**WBEM\_E\_PROVIDER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-114">2147749892 (0x80041004)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-114">2147749892 (0x80041004)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-115">Le fournisseur a échoué à un moment autre que pendant l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-115">The provider has failed at some time other than during initialization.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-116"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**incompatibilité de \_ type WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-116"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**WBEM\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-117">2147749893 (0x80041005)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-117">2147749893 (0x80041005)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-118">Une incompatibilité de type s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-118">A type mismatch has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-119"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**\_mémoire WBEM \_ insuffisante \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-119"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM\_E\_OUT\_OF\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-120">2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-120">2147749894 (0x80041006)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-121">Il n'y a pas assez de mémoire pour l'opération.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-121">There was not enough memory for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-122"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**\_paramètre WBEM E \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-122"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**WBEM\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-123">2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-123">2147749896 (0x80041008)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-124">Un des paramètres de l'appel n'est pas correct.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-124">One of the parameters to the call is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-125"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ non \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-125"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM\_E\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-126">2147749897 (0x80041009)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-126">2147749897 (0x80041009)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-127">La ressource, généralement un serveur distant, n'est pas disponible actuellement.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-127">The resource, typically a remote server, is not currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-128"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E \_ non \_ pris en charge**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-128"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM\_E\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-129">2147749900 (0x8004100C)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-129">2147749900 (0x8004100C)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-130">La fonctionnalité ou l'opération n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-130">The feature or operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-131"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM \_ E \_ espace de noms non valide \_**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-131"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM\_E\_INVALID\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-132">2147749902 (0x8004100E)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-132">2147749902 (0x8004100E)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-133">L'espace de noms spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-133">The specified namespace could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-134"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM \_ E \_ objet non valide \_**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-134"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM\_E\_INVALID\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-135">2147749903 (0x8004100F)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-135">2147749903 (0x8004100F)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-136">L'instance spécifiée n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-136">The specified instance is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-137"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**\_ \_ échec d’initialisation d’E WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-137"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**WBEM\_E\_INITIALIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-138">2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-138">2147749908 (0x80041014)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-139">Un module, tel qu’un fournisseur, n’a pas pu s’initialiser pour des raisons internes.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-139">A module, such as a provider, failed to initialize for internal reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-140"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**\_ \_ opération non valide WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-140"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**WBEM\_E\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-141">2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-141">2147749910 (0x80041016)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-142">L'opération demandée n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-142">The requested operation is not valid.</span></span> <span data-ttu-id="0c0f0-143">Cette erreur s'applique généralement aux tentatives non valides de suppression de classes ou de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-143">This error usually applies to invalid attempts to delete classes or properties.</span></span> <span data-ttu-id="0c0f0-144">Cette erreur est retournée lors d’une tentative de modification d’une propriété de substitution de serveur par le biais du contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-144">This error is returned on an attempt to modify a server-override property through group policy control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-145"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**\_requête E \_ non valide \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-145"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**WBEM\_E\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-146">2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-146">2147749911 (0x80041017)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-147">La syntaxe de la requête n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-147">The query was not syntactically valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-148"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**\_type de \_ requête non valide WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-148"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**WBEM\_E\_INVALID\_QUERY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-149">2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-149">2147749912 (0x80041018)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-150">Le langage de la requête demandé n'est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-150">The requested query language is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-151"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E \_ \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-151"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM\_E\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-152">2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-152">2147749913 (0x80041019)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-153">Dans une opération Put, l’indicateur **wbemChangeFlagCreateOnly** a été spécifié, mais l’instance existe déjà.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-153">In a put operation, the **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-154"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**\_syntaxe WBEM E \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-154"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**WBEM\_E\_INVALID\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-155">2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-155">2147749921 (0x80041021)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-156">La syntaxe de la requête n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-156">Query is not syntactically valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-157"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**\_ \_ lecture seule WBEM \_ E**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-157"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM\_E\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-158">2147749923 (0x80041023)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-158">2147749923 (0x80041023)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-159">La propriété que vous avez tenté de modifier est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-159">The property that you are attempting to modify is read-only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-160"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**\_fournisseur E \_ WBEM \_ non \_ conforme**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-160"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM\_E\_PROVIDER\_NOT\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-161">2147749924 (0x80041024)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-161">2147749924 (0x80041024)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-162">Le fournisseur ne peut pas effectuer l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-162">The provider cannot perform the requested operation.</span></span> <span data-ttu-id="0c0f0-163">L’opération peut inclure une requête qui est trop complexe, la récupération d’une instance, la création d’une classe, la mise à jour d’une classe, la suppression d’une classe ou l’énumération d’une classe.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-163">The operation could include a query that is too complex, retrieving an instance, creating a class, updating a class, deleting a class, or enumerating a class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-164"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E \_ null non conforme \_**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-164"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM\_E\_ILLEGAL\_NULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-165">2147749928 (0x80041028)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-165">2147749928 (0x80041028)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-166">La valeur **Nothing** / **null** a été spécifiée pour une propriété qui ne peut pas être / **null**, telle que celle qui est marquée par un qualificateur [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**indexé**](/windows/desktop/WmiSdk/optional-qualifiers)ou [**not \_ null**](/windows/desktop/WmiSdk/optional-qualifiers) .</span><span class="sxs-lookup"><span data-stu-id="0c0f0-166">A value of **Nothing**/**NULL** was specified for a property that cannot be **Nothing**/**NULL**, such as one that is marked by a [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Indexed**](/windows/desktop/WmiSdk/optional-qualifiers), or [**Not\_Null**](/windows/desktop/WmiSdk/optional-qualifiers) qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-167"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**\_valeur WBEM \_ E \_ hors \_ \_ limites**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-167"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**WBEM\_E\_VALUE\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-168">2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-168">2147749931 (0x8004102B)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-169">La demande a été effectuée avec une valeur hors limites ou est incompatible avec le type.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-169">The request was made with an out-of-range value, or is incompatible with the type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-170"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM \_ E \_ , \_ méthode non valide**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-170"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM\_E\_INVALID\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-171">2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-171">2147749934 (0x8004102E)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-172">La méthode demandée n'est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-172">The requested method is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-173"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**\_paramètres de méthode WBEM E \_ non valides \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-173"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**WBEM\_E\_INVALID\_METHOD\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-174">2147749935 (0x8004102F)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-174">2147749935 (0x8004102F)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-175">Les paramètres fournis pour la méthode ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-175">The parameters provided for the method are not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c0f0-176"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM \_ E \_ \_ chemin d’objet non valide \_**</span><span class="sxs-lookup"><span data-stu-id="0c0f0-176"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM\_E\_INVALID\_OBJECT\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f0-177">2147749946 (0x8004103A)</span><span class="sxs-lookup"><span data-stu-id="0c0f0-177">2147749946 (0x8004103A)</span></span>
</dt> <dt>



<span data-ttu-id="0c0f0-178">Le chemin d’accès à l’objet spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0c0f0-178">The specified object path was not valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c0f0-179">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c0f0-179">Requirements</span></span>



| <span data-ttu-id="0c0f0-180">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c0f0-180">Requirement</span></span> | <span data-ttu-id="0c0f0-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c0f0-181">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0c0f0-182">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c0f0-182">Minimum supported client</span></span><br/> | <span data-ttu-id="0c0f0-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c0f0-183">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="0c0f0-184">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c0f0-184">Minimum supported server</span></span><br/> | <span data-ttu-id="0c0f0-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c0f0-185">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="0c0f0-186">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c0f0-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c0f0-187"><dt>Wbemcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c0f0-187"><dt>Wbemcli.h</dt></span></span> </dl> |



 

