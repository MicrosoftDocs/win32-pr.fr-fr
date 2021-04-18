---
description: La \_ classe d’erreur CIM contient des informations sur l’échec d’une opération CIM.
ms.assetid: 35acecbd-b972-45b4-9616-2047bba8fd41
title: Classe CIM_Error
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Error
- CIM_Error.ErrorType
- CIM_Error.OtherErrorType
- CIM_Error.OwningEntity
- CIM_Error.MessageID
- CIM_Error.Message
- CIM_Error.MessageArguments
- CIM_Error.PerceivedSeverity
- CIM_Error.ProbableCause
- CIM_Error.ProbableCauseDescription
- CIM_Error.RecommendedActions
- CIM_Error.ErrorSource
- CIM_Error.ErrorSourceFormat
- CIM_Error.OtherErrorSourceFormat
- CIM_Error.CIMStatusCode
- CIM_Error.CIMStatusCodeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 59ae2527478235c14a8f856319178afe00c02a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318034"
---
# <a name="cim_error-class"></a><span data-ttu-id="14f24-103">\_Classe d’erreur CIM</span><span class="sxs-lookup"><span data-stu-id="14f24-103">CIM\_Error class</span></span>

<span data-ttu-id="14f24-104">La classe d' **\_ erreur CIM** contient des informations sur l’échec d’une opération CIM.</span><span class="sxs-lookup"><span data-stu-id="14f24-104">The **CIM\_Error** class contains information about the failure of a CIM operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="14f24-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14f24-105">Syntax</span></span>

``` syntax
[Indication, Abstract, Version("2.22.1"), Exception, UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_Error
{
  uint16 ErrorType;
  string OtherErrorType;
  string OwningEntity;
  string MessageID;
  string Message;
  string MessageArguments[];
  uint16 PerceivedSeverity;
  uint16 ProbableCause;
  string ProbableCauseDescription;
  string RecommendedActions[];
  string ErrorSource;
  uint16 ErrorSourceFormat = 0;
  string OtherErrorSourceFormat;
  uint32 CIMStatusCode;
  string CIMStatusCodeDescription;
};
```

## <a name="members"></a><span data-ttu-id="14f24-106">Membres</span><span class="sxs-lookup"><span data-stu-id="14f24-106">Members</span></span>

<span data-ttu-id="14f24-107">La classe d' **\_ erreur CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="14f24-107">The **CIM\_Error** class has these types of members:</span></span>

-   [<span data-ttu-id="14f24-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="14f24-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="14f24-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="14f24-109">Properties</span></span>

<span data-ttu-id="14f24-110">La classe d' **\_ erreur CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="14f24-110">The **CIM\_Error** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="14f24-111">**CIMStatusCode**</span><span class="sxs-lookup"><span data-stu-id="14f24-111">**CIMStatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14f24-112">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14f24-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14f24-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14f24-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14f24-114">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201. \|erreur DMTF. CODE \| 2,3 "," DSP0200. DMTF \| CIMError \| 1,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erreur CIM**.**CIMStatusCodeDescription**")</span><span class="sxs-lookup"><span data-stu-id="14f24-114">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201.DMTF\|ERROR.CODE\|2.3", "DSP0200.DMTF\|CIMError\|1.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**CIMStatusCodeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="14f24-115">Code d’État CIM qui caractérise cette instance.</span><span class="sxs-lookup"><span data-stu-id="14f24-115">The CIM status code that characterizes this instance.</span></span> <span data-ttu-id="14f24-116">Cette propriété définit les codes d’État qui peuvent être retournés par un serveur ou un écouteur CIM.</span><span class="sxs-lookup"><span data-stu-id="14f24-116">This property defines the status codes that can be return by a CIM server or listener.</span></span>

<dt>

<span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>

<span data-ttu-id="14f24-117"><span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>**CIM \_ \_Échec** de l’erreur (1)</span><span class="sxs-lookup"><span data-stu-id="14f24-117"><span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>**CIM\_ERR\_FAILED** (1)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-118">Une erreur générale s’est produite et n’est pas couverte par un code d’erreur plus spécifique.</span><span class="sxs-lookup"><span data-stu-id="14f24-118">A general error occurred that is not covered by a more specific error code.</span></span>

</dd> <dt>

<span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>

<span data-ttu-id="14f24-119"><span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>**CIM \_ ERREUR d' \_ accès \_ refusé** (2)</span><span class="sxs-lookup"><span data-stu-id="14f24-119"><span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>**CIM\_ERR\_ACCESS\_DENIED** (2)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-120">L’accès à une ressource CIM n’était pas disponible pour le client.</span><span class="sxs-lookup"><span data-stu-id="14f24-120">Access to a CIM resource was not available to the client.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>

<span data-ttu-id="14f24-121"><span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>**CIM \_ ERREUR \_ d' \_ espace de noms non valide** (3)</span><span class="sxs-lookup"><span data-stu-id="14f24-121"><span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>**CIM\_ERR\_INVALID\_NAMESPACE** (3)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-122">L’espace de noms cible n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="14f24-122">The target namespace does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>

<span data-ttu-id="14f24-123"><span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>**CIM \_ \_ \_ Paramètre Err non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="14f24-123"><span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>**CIM\_ERR\_INVALID\_PARAMETER** (4)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-124">Une ou plusieurs valeurs de paramètre passées à la méthode ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="14f24-124">One or more parameter values passed to the method were invalid.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>

<span data-ttu-id="14f24-125"><span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>**CIM \_ ERR \_ , \_ classe non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="14f24-125"><span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>**CIM\_ERR\_INVALID\_CLASS** (5)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-126">La classe spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="14f24-126">The specified Class does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>

<span data-ttu-id="14f24-127"><span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>**CIM \_ ERR \_ \_ introuvable** (6)</span><span class="sxs-lookup"><span data-stu-id="14f24-127"><span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>**CIM\_ERR\_NOT\_FOUND** (6)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-128">L’objet demandé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="14f24-128">The requested object could not be found.</span></span>

</dd> <dt>

<span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>

<span data-ttu-id="14f24-129"><span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>**CIM \_ ERR \_ non \_ prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="14f24-129"><span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>**CIM\_ERR\_NOT\_SUPPORTED** (7)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-130">L'opération demandée n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="14f24-130">The requested operation is not supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>

<span data-ttu-id="14f24-131"><span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>**CIM \_ La \_ classe Err \_ a des \_ enfants** (8)</span><span class="sxs-lookup"><span data-stu-id="14f24-131"><span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>**CIM\_ERR\_CLASS\_HAS\_CHILDREN** (8)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-132">Impossible d’effectuer l’opération sur cette classe, car elle contient des instances.</span><span class="sxs-lookup"><span data-stu-id="14f24-132">Operation cannot be carried out on this class since it has instances.</span></span>

</dd> <dt>

<span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>

<span data-ttu-id="14f24-133"><span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>**CIM \_ La \_ classe Err \_ contient des \_ instances** (9)</span><span class="sxs-lookup"><span data-stu-id="14f24-133"><span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>**CIM\_ERR\_CLASS\_HAS\_INSTANCES** (9)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-134">Impossible d’effectuer l’opération sur cette classe, car elle contient des instances.</span><span class="sxs-lookup"><span data-stu-id="14f24-134">Operation cannot be carried out on this class since it has instances.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>

<span data-ttu-id="14f24-135"><span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>**CIM \_ ERREUR \_ de \_ superclasse non valide** (10)</span><span class="sxs-lookup"><span data-stu-id="14f24-135"><span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>**CIM\_ERR\_INVALID\_SUPERCLASS** (10)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-136">Impossible d’effectuer l’opération, car la superclasse spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="14f24-136">Operation cannot be carried out since the specified superclass does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>

<span data-ttu-id="14f24-137"><span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>**CIM \_ ERR \_ \_ existe déjà** (11)</span><span class="sxs-lookup"><span data-stu-id="14f24-137"><span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>**CIM\_ERR\_ALREADY\_EXISTS** (11)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-138">Impossible d’effectuer l’opération, car un objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="14f24-138">Operation cannot be carried out because an object already exists.</span></span>

</dd> <dt>

<span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>

<span data-ttu-id="14f24-139"><span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>**CIM \_ ERR \_ aucune \_ \_ propriété de ce type** (12)</span><span class="sxs-lookup"><span data-stu-id="14f24-139"><span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>**CIM\_ERR\_NO\_SUCH\_PROPERTY** (12)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-140">La propriété spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="14f24-140">The specified Property does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>

<span data-ttu-id="14f24-141"><span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>**CIM \_ \_Incompatibilité \_ de type Err** (13)</span><span class="sxs-lookup"><span data-stu-id="14f24-141"><span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>**CIM\_ERR\_TYPE\_MISMATCH** (13)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-142">La valeur fournie est incompatible avec le type.</span><span class="sxs-lookup"><span data-stu-id="14f24-142">The value supplied is incompatible with the type.</span></span>

</dd> <dt>

<span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>

<span data-ttu-id="14f24-143"><span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>**CIM \_ \_Langage de requête Err \_ \_ non \_ pris en charge** (14)</span><span class="sxs-lookup"><span data-stu-id="14f24-143"><span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>**CIM\_ERR\_QUERY\_LANGUAGE\_NOT\_SUPPORTED** (14)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-144">Le langage de requête n’est pas reconnu ou n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="14f24-144">The query language is not recognized or supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>

<span data-ttu-id="14f24-145"><span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>**CIM \_ \_ \_ Requête Err non valide** (15)</span><span class="sxs-lookup"><span data-stu-id="14f24-145"><span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>**CIM\_ERR\_INVALID\_QUERY** (15)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-146">La requête n’est pas valide pour le langage de requête spécifié.</span><span class="sxs-lookup"><span data-stu-id="14f24-146">The query is not valid for the specified query language.</span></span>

</dd> <dt>

<span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>

<span data-ttu-id="14f24-147"><span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>**CIM \_ \_Méthode Err \_ non \_ disponible** (16)</span><span class="sxs-lookup"><span data-stu-id="14f24-147"><span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>**CIM\_ERR\_METHOD\_NOT\_AVAILABLE** (16)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-148">La méthode extrinsèque n’a pas pu être exécutée.</span><span class="sxs-lookup"><span data-stu-id="14f24-148">The extrinsic Method could not be executed.</span></span>

</dd> <dt>

<span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>

<span data-ttu-id="14f24-149"><span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>**CIM \_ \_Méthode Err \_ \_ introuvable** (17)</span><span class="sxs-lookup"><span data-stu-id="14f24-149"><span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>**CIM\_ERR\_METHOD\_NOT\_FOUND** (17)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-150">La méthode extrinsèque spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="14f24-150">The specified extrinsic Method does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>

<span data-ttu-id="14f24-151"><span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>**CIM \_ \_ \_ Réponse inattendue Err** (18)</span><span class="sxs-lookup"><span data-stu-id="14f24-151"><span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>**CIM\_ERR\_UNEXPECTED\_RESPONSE** (18)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-152">La réponse retournée à l’opération asynchrone n’était pas attendue.</span><span class="sxs-lookup"><span data-stu-id="14f24-152">The returned response to the asynchronous operation was not expected.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>

<span data-ttu-id="14f24-153"><span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>**CIM \_ Erreur \_ de \_ \_ destination de réponse Err non valide** (19)</span><span class="sxs-lookup"><span data-stu-id="14f24-153"><span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>**CIM\_ERR\_INVALID\_RESPONSE\_DESTINATION** (19)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-154">La destination spécifiée pour la réponse asynchrone n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="14f24-154">The specified destination for the asynchronous response is not valid.</span></span>

</dd> <dt>

<span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>

<span data-ttu-id="14f24-155"><span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>**CIM \_ L' \_ espace de noms Err \_ n’est pas \_ vide** (20)</span><span class="sxs-lookup"><span data-stu-id="14f24-155"><span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>**CIM\_ERR\_NAMESPACE\_NOT\_EMPTY** (20)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-156">L’espace de noms spécifié n’est pas vide.</span><span class="sxs-lookup"><span data-stu-id="14f24-156">The specified Namespace is not empty.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>

<span data-ttu-id="14f24-157"><span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>**CIM \_ ERR \_ \_ \_ contexte d’énumération non valide** (21)</span><span class="sxs-lookup"><span data-stu-id="14f24-157"><span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>**CIM\_ERR\_INVALID\_ENUMERATION\_CONTEXT** (21)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-158">Le contexte d’énumération fourni n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="14f24-158">The enumeration context supplied is not valid.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>

<span data-ttu-id="14f24-159"><span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>**CIM \_ ERR \_ erreur \_ \_ d’opération non valide** (22)</span><span class="sxs-lookup"><span data-stu-id="14f24-159"><span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>**CIM\_ERR\_INVALID\_OPERATION\_TIMEOUT** (22)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-160">L’espace de noms spécifié n’est pas vide.</span><span class="sxs-lookup"><span data-stu-id="14f24-160">The specified Namespace is not empty.</span></span>

</dd> <dt>

<span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>

<span data-ttu-id="14f24-161"><span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>**CIM \_ L’extraction de l’erreur \_ \_ a \_ été \_ abandonnée** (23)</span><span class="sxs-lookup"><span data-stu-id="14f24-161"><span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>**CIM\_ERR\_PULL\_HAS\_BEEN\_ABANDONED** (23)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-162">L’espace de noms spécifié n’est pas vide.</span><span class="sxs-lookup"><span data-stu-id="14f24-162">The specified Namespace is not empty.</span></span>

</dd> <dt>

<span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>

<span data-ttu-id="14f24-163"><span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>**CIM \_ \_Impossible d' \_ \_ \_ abandonner l’extraction** de l’erreur (24)</span><span class="sxs-lookup"><span data-stu-id="14f24-163"><span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>**CIM\_ERR\_PULL\_CANNOT\_BE\_ABANDONED** (24)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-164">La tentative d’abandon d’une opération d’extraction a échoué.</span><span class="sxs-lookup"><span data-stu-id="14f24-164">The attempt to abandon a pull operation has failed.</span></span>

</dd> <dt>

<span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>

<span data-ttu-id="14f24-165"><span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>**CIM \_ \_Énumération d’Err filtrée \_ \_ non \_ prise en charge** (25)</span><span class="sxs-lookup"><span data-stu-id="14f24-165"><span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>**CIM\_ERR\_FILTERED\_ENUMERATION\_NOT\_SUPPORTED** (25)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-166">Les Enumeratrions filtrés ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="14f24-166">Filtered Enumeratrions are not supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>

<span data-ttu-id="14f24-167"><span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>**CIM \_ \_ \_ Erreur de continuation en cas d' \_ erreur \_ non \_ prise en charge** (26)</span><span class="sxs-lookup"><span data-stu-id="14f24-167"><span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>**CIM\_ERR\_CONTINUATION\_ON\_ERROR\_NOT\_SUPPORTED** (26)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-168">Continuer en cas d’erreur n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="14f24-168">Continue on error is not supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>

<span data-ttu-id="14f24-169"><span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>**CIM \_ \_Limites du serveur Err \_ \_ dépassées** (27)</span><span class="sxs-lookup"><span data-stu-id="14f24-169"><span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>**CIM\_ERR\_SERVER\_LIMITS\_EXCEEDED** (27)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-170">Les limites du serveur WBEM ont été dépassées (par exemple, mémoire, connexions, etc.).</span><span class="sxs-lookup"><span data-stu-id="14f24-170">The WBEM Server limits have been exceeded (e.g. memory, connections, ...).</span></span>

</dd> <dt>

<span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>

<span data-ttu-id="14f24-171"><span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>**CIM \_ \_Arrêt du \_ serveur \_ \_ Err** (28)</span><span class="sxs-lookup"><span data-stu-id="14f24-171"><span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>**CIM\_ERR\_SERVER\_IS\_SHUTTING\_DOWN** (28)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-172">Le serveur WBEM est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="14f24-172">The WBEM Server is shutting down.</span></span>

</dd> <dt>

<span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>

<span data-ttu-id="14f24-173"><span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>**CIM \_ \_Fonctionnalité de requête Err \_ \_ non \_ prise en charge** (29)</span><span class="sxs-lookup"><span data-stu-id="14f24-173"><span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>**CIM\_ERR\_QUERY\_FEATURE\_NOT\_SUPPORTED** (29)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-174">La fonctionnalité de requête spécifiée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="14f24-174">The specified Query Feature is not supported.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="14f24-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="14f24-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="14f24-176">**CIMStatusCodeDescription**</span><span class="sxs-lookup"><span data-stu-id="14f24-176">**CIMStatusCodeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14f24-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="14f24-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14f24-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14f24-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14f24-179">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201. \|erreur DMTF. DESCRIPTION \| 2,3 « , » DSP0200. DMTF \| CIMError \| 1,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erreur CIM**.**CIMStatusCode**")</span><span class="sxs-lookup"><span data-stu-id="14f24-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201.DMTF\|ERROR.DESCRIPTION\|2.3", "DSP0200.DMTF\|CIMError\|1.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**CIMStatusCode**")</span></span>
</dt> </dl>

<span data-ttu-id="14f24-180">Chaîne de forme libre qui contient une description explicite de la valeur de la propriété **CIMStatusCode** .</span><span class="sxs-lookup"><span data-stu-id="14f24-180">A free-form string that contains a human-readable description of the **CIMStatusCode** property value.</span></span>

> [!Note]  
> <span data-ttu-id="14f24-181">Cette description peut s’étendre, mais doit être cohérente avec la définition de **CIMStatusCode**.</span><span class="sxs-lookup"><span data-stu-id="14f24-181">This description may extend, but must be consistent with the definition of **CIMStatusCode**.</span></span>

 

</dd> <dt>

<span data-ttu-id="14f24-182">**ErrorSource**</span><span class="sxs-lookup"><span data-stu-id="14f24-182">**ErrorSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14f24-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="14f24-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14f24-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14f24-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14f24-185">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erreur CIM**.**ErrorSourceFormat**")</span><span class="sxs-lookup"><span data-stu-id="14f24-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorSourceFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="14f24-186">Informations identifiant l’entité qui a généré l’erreur.</span><span class="sxs-lookup"><span data-stu-id="14f24-186">Information that identifies the entity that generated the error.</span></span> <span data-ttu-id="14f24-187">Si l’entité est modélisée par le schéma CIM, cette propriété contient le chemin d’accès à l’instance encodée sous la forme d’un paramètre de chaîne.</span><span class="sxs-lookup"><span data-stu-id="14f24-187">If the entity is modeled by the CIM Schema, this property contains the path to the instance encoded as a string parameter.</span></span> <span data-ttu-id="14f24-188">Sinon, la propriété contient une chaîne qui nomme l’entité qui a généré l’erreur.</span><span class="sxs-lookup"><span data-stu-id="14f24-188">Otherwise, the property contains a string that names the entity that generated the error.</span></span> <span data-ttu-id="14f24-189">Le format de cette propriété est spécifié par la propriété **ErrorSourceFormat** .</span><span class="sxs-lookup"><span data-stu-id="14f24-189">The format of this property is specified by the **ErrorSourceFormat** property.</span></span>

</dd> <dt>

<span data-ttu-id="14f24-190">**ErrorSourceFormat**</span><span class="sxs-lookup"><span data-stu-id="14f24-190">**ErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14f24-191">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="14f24-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="14f24-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14f24-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14f24-193">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erreur CIM**.**ErrorSource**","**\_ erreur CIM**.**OtherErrorSourceFormat**")</span><span class="sxs-lookup"><span data-stu-id="14f24-193">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorSource**", "**CIM\_Error**.**OtherErrorSourceFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="14f24-194">Format de la propriété **ErrorSource** .</span><span class="sxs-lookup"><span data-stu-id="14f24-194">The format of the **ErrorSource** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="14f24-195"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="14f24-195"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-196">Le format est inconnu ou ne peut pas être interprété de manière significative par une application cliente CIM.</span><span class="sxs-lookup"><span data-stu-id="14f24-196">The format is unknown or not meaningfully interpretable by a CIM client application.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="14f24-197"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="14f24-197"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-198">Le format est défini par la valeur de la propriété **OtherErrorSourceFormat** .</span><span class="sxs-lookup"><span data-stu-id="14f24-198">The format is defined by the value of the **OtherErrorSourceFormat** property.</span></span>

</dd> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>

<span data-ttu-id="14f24-199"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span><span class="sxs-lookup"><span data-stu-id="14f24-199"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-200">Un chemin d’accès d’objet CIM tel que défini dans la spécification de l’infrastructure CIM.</span><span class="sxs-lookup"><span data-stu-id="14f24-200">A CIM Object Path as defined in the CIM Infrastructure specification.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="14f24-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="14f24-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="14f24-202">**ErrorType**</span><span class="sxs-lookup"><span data-stu-id="14f24-202">**ErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14f24-203">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="14f24-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="14f24-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14f24-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14f24-205">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erreur CIM**.**OtherErrorType**")</span><span class="sxs-lookup"><span data-stu-id="14f24-205">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**OtherErrorType**")</span></span>
</dt> </dl>

<span data-ttu-id="14f24-206">Type d’erreur primaire.</span><span class="sxs-lookup"><span data-stu-id="14f24-206">The primary error type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="14f24-207"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="14f24-207"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="14f24-208"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="14f24-208"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>

<span data-ttu-id="14f24-209"><span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>**Erreur de communication** (2)</span><span class="sxs-lookup"><span data-stu-id="14f24-209"><span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>**Communications Error** (2)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-210">Les erreurs de ce type sont principalement associées aux procédures et/ou aux processus requis pour transmettre des informations d’un point à un autre.</span><span class="sxs-lookup"><span data-stu-id="14f24-210">Errors of this type are principally associated with the procedures and/or processes required to convey information from one point to another.</span></span>

</dd> <dt>

<span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>

<span data-ttu-id="14f24-211"><span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>**Erreur de qualité de service** (3)</span><span class="sxs-lookup"><span data-stu-id="14f24-211"><span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>**Quality of Service Error** (3)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-212">Les erreurs de ce type sont principalement associées à des échecs qui entraînent une réduction des fonctionnalités ou des performances.</span><span class="sxs-lookup"><span data-stu-id="14f24-212">Errors of this type are principally associated with failures that result in reduced functionality or performance.</span></span>

</dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span data-ttu-id="14f24-213"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Erreur logicielle** (4)</span><span class="sxs-lookup"><span data-stu-id="14f24-213"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Software Error** (4)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-214">Une erreur de ce type est principalement associée à un logiciel ou à une erreur de traitement.</span><span class="sxs-lookup"><span data-stu-id="14f24-214">Error of this type are principally associated with a software or processing fault.</span></span>

</dd> <dt>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>

<span data-ttu-id="14f24-215"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Erreur matérielle** (5)</span><span class="sxs-lookup"><span data-stu-id="14f24-215"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Hardware Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-216">Les erreurs de ce type sont principalement associées à une défaillance matérielle ou matérielle.</span><span class="sxs-lookup"><span data-stu-id="14f24-216">Errors of this type are principally associated with an equipment or hardware failure.</span></span>

</dd> <dt>

<span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>

<span data-ttu-id="14f24-217"><span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>**Erreur environnementale** (6)</span><span class="sxs-lookup"><span data-stu-id="14f24-217"><span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>**Environmental Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-218">autres considérations environnementales.</span><span class="sxs-lookup"><span data-stu-id="14f24-218">other environmental considerations.</span></span>

</dd> <dt>

<span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>

<span data-ttu-id="14f24-219"><span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>**Erreur de sécurité** (7)</span><span class="sxs-lookup"><span data-stu-id="14f24-219"><span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>**Security Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-220">Les erreurs de ce type sont associées à des violations de sécurité, à la détection de virus et à des problèmes similaires.</span><span class="sxs-lookup"><span data-stu-id="14f24-220">Errors of this type are associated with security violations, detection of viruses, and similar issues.</span></span>

</dd> <dt>

<span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>

<span data-ttu-id="14f24-221"><span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>**Erreur de surabonnement** (8)</span><span class="sxs-lookup"><span data-stu-id="14f24-221"><span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>**Oversubscription Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-222">Les erreurs de ce type sont principalement associées à l’échec d’allocation des ressources suffisantes pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="14f24-222">Errors of this type are principally associated with the failure to allocate sufficient resources to complete the operation.</span></span>

</dd> <dt>

<span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>

<span data-ttu-id="14f24-223"><span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>**Erreur de ressource non disponible** (9)</span><span class="sxs-lookup"><span data-stu-id="14f24-223"><span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>**Unavailable Resource Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-224">Les erreurs de ce type sont principalement associées à l’échec d’accès à une ressource requise.</span><span class="sxs-lookup"><span data-stu-id="14f24-224">Errors of this type are principally associated with the failure to access a required resource.</span></span>

</dd> <dt>

<span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>

<span data-ttu-id="14f24-225"><span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>**Erreur d’opération non prise en charge** (10)</span><span class="sxs-lookup"><span data-stu-id="14f24-225"><span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>**Unsupported Operation Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-226">Les erreurs de ce type sont associées principalement aux demandes qui ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="14f24-226">Errors of this type are principally associated with requests that are not supported.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="14f24-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="14f24-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="14f24-228">**Message**</span><span class="sxs-lookup"><span data-stu-id="14f24-228">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14f24-229">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="14f24-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14f24-230">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14f24-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14f24-231">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erreur CIM**.**MessageID**","**\_ erreur CIM**.**MessageArguments**")</span><span class="sxs-lookup"><span data-stu-id="14f24-231">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**MessageID**", "**CIM\_Error**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="14f24-232">Message mis en forme.</span><span class="sxs-lookup"><span data-stu-id="14f24-232">The formatted message.</span></span>

> [!Note]  
> <span data-ttu-id="14f24-233">Ce message est créé en combinant des éléments dynamiques de la propriété **MessageArguments** avec les éléments statiques de la propriété **MessageID** , puis en les ajoutant à un registre de messages ou à un catalogue associé à **OwningEntity**.</span><span class="sxs-lookup"><span data-stu-id="14f24-233">This message is created by combining dynamic elements of the **MessageArguments** property with the static elements of the **MessageID** property, and then adding them to a message registry or catalog associated with the **OwningEntity**.</span></span>

 

</dd> <dt>

<span data-ttu-id="14f24-234">**MessageArguments**</span><span class="sxs-lookup"><span data-stu-id="14f24-234">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14f24-235">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="14f24-235">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="14f24-236">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14f24-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14f24-237">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erreur CIM**.**MessageID**","**\_ erreur CIM**.**Message**»)</span><span class="sxs-lookup"><span data-stu-id="14f24-237">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**MessageID**", "**CIM\_Error**.**Message**")</span></span>
</dt> </dl>

<span data-ttu-id="14f24-238">Tableau qui contient le contenu dynamique du message.</span><span class="sxs-lookup"><span data-stu-id="14f24-238">An array that contains the dynamic content of the message.</span></span>

</dd> <dt>

<span data-ttu-id="14f24-239">**ID**</span><span class="sxs-lookup"><span data-stu-id="14f24-239">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14f24-240">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="14f24-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14f24-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14f24-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14f24-242">Qualificateurs : [**requis**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erreur CIM**.**Message**","**\_ erreur CIM**.**MessageArguments**")</span><span class="sxs-lookup"><span data-stu-id="14f24-242">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**Message**", "**CIM\_Error**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="14f24-243">Chaîne opaque qui identifie de façon unique, au sein de la portée de la OwningEntity, le format du message.</span><span class="sxs-lookup"><span data-stu-id="14f24-243">An opaque string that uniquely identifies, within the scope of the OwningEntity, the format of the Message.</span></span>

</dd> <dt>

<span data-ttu-id="14f24-244">**OtherErrorSourceFormat**</span><span class="sxs-lookup"><span data-stu-id="14f24-244">**OtherErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14f24-245">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="14f24-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14f24-246">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14f24-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14f24-247">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erreur CIM**.**ErrorSourceFormat**")</span><span class="sxs-lookup"><span data-stu-id="14f24-247">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorSourceFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="14f24-248">Chaîne qui définit la valeur **ErrorSourceFormat** lorsque **ErrorSourceFormat** est défini sur « 1 » (autre).</span><span class="sxs-lookup"><span data-stu-id="14f24-248">A string that defines the **ErrorSourceFormat** value when **ErrorSourceFormat** is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="14f24-249">**OtherErrorType**</span><span class="sxs-lookup"><span data-stu-id="14f24-249">**OtherErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14f24-250">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="14f24-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14f24-251">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14f24-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14f24-252">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erreur CIM**.**ErrorType**")</span><span class="sxs-lookup"><span data-stu-id="14f24-252">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorType**")</span></span>
</dt> </dl>

<span data-ttu-id="14f24-253">Chaîne de forme libre qui décrit la valeur **ErrorType** quand elle est définie sur « 1 » (autre).</span><span class="sxs-lookup"><span data-stu-id="14f24-253">A free-form string that describes the **ErrorType** value when it is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="14f24-254">**OwningEntity**</span><span class="sxs-lookup"><span data-stu-id="14f24-254">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14f24-255">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="14f24-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14f24-256">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14f24-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="14f24-257">ID unique de l’entité qui possède le format du message décrit par cette instance.</span><span class="sxs-lookup"><span data-stu-id="14f24-257">The unique ID of the entity that owns the format of the message described by this instance.</span></span>

> [!Note]  
> <span data-ttu-id="14f24-258">Cette propriété doit inclure un nom de droits d’auteur, de marque déposée ou unique qui est détenu par l’entité métier ou le corps de normes qui a défini le format du message.</span><span class="sxs-lookup"><span data-stu-id="14f24-258">This property must include a copyrighted, trademarked, or unique name that is owned by the business entity or standards body that defined the message format.</span></span>

 

</dd> <dt>

<span data-ttu-id="14f24-259">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="14f24-259">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14f24-260">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="14f24-260">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="14f24-261">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14f24-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14f24-262">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Gravité perçue»)</span><span class="sxs-lookup"><span data-stu-id="14f24-262">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Perceived severity")</span></span>
</dt> </dl>

<span data-ttu-id="14f24-263">Description de la gravité de l’erreur par rapport au point de vue de l’élément qui a envoyé le message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="14f24-263">A description of the error severity from the point of view of the element that sent the error message.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="14f24-264"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="14f24-264"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-265">la gravité perçue de l’indication est inconnue ou indéterminée.</span><span class="sxs-lookup"><span data-stu-id="14f24-265">the Perceived Severity of the indication is unknown or indeterminate.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="14f24-266"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="14f24-266"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-267">Indique que la valeur de la gravité se trouve dans la propriété **OtherSeverity** .</span><span class="sxs-lookup"><span data-stu-id="14f24-267">Indicates that the Severity's value can be found in the **OtherSeverity** property.</span></span>

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span data-ttu-id="14f24-268"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informations** (2)</span><span class="sxs-lookup"><span data-stu-id="14f24-268"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-269">Les informations doivent être utilisées lors de la fourniture d’une réponse informatif.</span><span class="sxs-lookup"><span data-stu-id="14f24-269">Information should be used when providing an informative response.</span></span>

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="14f24-270"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Détérioré/AVERTISSEMENT** (3)</span><span class="sxs-lookup"><span data-stu-id="14f24-270"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-271">Doit être utilisé pour permettre à l’utilisateur de décider si une action est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="14f24-271">Should be used when its appropriate to let the user decide if action is needed.</span></span>

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span data-ttu-id="14f24-272"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Mineure** (4)</span><span class="sxs-lookup"><span data-stu-id="14f24-272"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Minor** (4)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-273">Une action est nécessaire, mais la situation n’est pas grave pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="14f24-273">Action is needed, but the situation is not serious at this time.</span></span>

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span data-ttu-id="14f24-274"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Principal** (5)</span><span class="sxs-lookup"><span data-stu-id="14f24-274"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Major** (5)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-275">Une action est nécessaire maintenant.</span><span class="sxs-lookup"><span data-stu-id="14f24-275">Action is needed NOW.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="14f24-276"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (6)</span><span class="sxs-lookup"><span data-stu-id="14f24-276"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (6)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-277">L’action est nécessaire maintenant et l’étendue est large (peut-être une interruption imminente d’une ressource critique se produira-t-elle).</span><span class="sxs-lookup"><span data-stu-id="14f24-277">Action is needed NOW and the scope is broad (perhaps an imminent outage to a critical resource will result).</span></span>

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span data-ttu-id="14f24-278"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Irrécupérable/irrécupérable** (7)</span><span class="sxs-lookup"><span data-stu-id="14f24-278"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/NonRecoverable** (7)</span></span>


</dt> <dd>

<span data-ttu-id="14f24-279">une erreur s’est produite, mais il est trop tard pour prendre une mesure corrective.</span><span class="sxs-lookup"><span data-stu-id="14f24-279">an error occurred, but it's too late to take remedial action.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="14f24-280"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="14f24-280"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="14f24-281">**ProbableCause**</span><span class="sxs-lookup"><span data-stu-id="14f24-281">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14f24-282">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="14f24-282">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="14f24-283">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14f24-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14f24-284">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Cause probable "," recommandation. ITU \| M3100. probableCause "," ITU-IANA-Alarm-TC "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erreur CIM**.**ProbableCauseDescription**")</span><span class="sxs-lookup"><span data-stu-id="14f24-284">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Probable cause", "Recommendation.ITU\|M3100.probableCause", "ITU-IANA-ALARM-TC"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ProbableCauseDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="14f24-285">Description de la cause probable de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="14f24-285">A description of te probable cause of the error.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="14f24-286">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="14f24-286">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="14f24-287">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="14f24-287">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>

<span data-ttu-id="14f24-288">**Erreur de carte/carte** (2)</span><span class="sxs-lookup"><span data-stu-id="14f24-288">**Adapter/Card Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="14f24-289">**Défaillance du sous-système d’application** (3)</span><span class="sxs-lookup"><span data-stu-id="14f24-289">**Application Subsystem Failure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>

<span data-ttu-id="14f24-290">**Bande passante réduite** (4)</span><span class="sxs-lookup"><span data-stu-id="14f24-290">**Bandwidth Reduced** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>

<span data-ttu-id="14f24-291">**Erreur d’établissement** de la connexion (5)</span><span class="sxs-lookup"><span data-stu-id="14f24-291">**Connection Establishment Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>

<span data-ttu-id="14f24-292">**Erreur de protocole de communication** (6)</span><span class="sxs-lookup"><span data-stu-id="14f24-292">**Communications Protocol Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="14f24-293">**Défaillance du sous-système de communication** (7)</span><span class="sxs-lookup"><span data-stu-id="14f24-293">**Communications Subsystem Failure** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>

<span data-ttu-id="14f24-294">**Erreur de configuration/personnalisation** (8)</span><span class="sxs-lookup"><span data-stu-id="14f24-294">**Configuration/Customization Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>

<span data-ttu-id="14f24-295">**Congestion** (9)</span><span class="sxs-lookup"><span data-stu-id="14f24-295">**Congestion** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>

<span data-ttu-id="14f24-296">**Données endommagées** (10)</span><span class="sxs-lookup"><span data-stu-id="14f24-296">**Corrupt Data** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>

<span data-ttu-id="14f24-297">**Limite du nombre de cycles de l’UC dépassée** (11)</span><span class="sxs-lookup"><span data-stu-id="14f24-297">**CPU Cycles Limit Exceeded** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>

<span data-ttu-id="14f24-298">**Erreur de jeu de données/modem** (12)</span><span class="sxs-lookup"><span data-stu-id="14f24-298">**Dataset/Modem Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>

<span data-ttu-id="14f24-299">**Signal détérioré** (13)</span><span class="sxs-lookup"><span data-stu-id="14f24-299">**Degraded Signal** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>

<span data-ttu-id="14f24-300">**Erreur d’interface DTE-DCE** (14)</span><span class="sxs-lookup"><span data-stu-id="14f24-300">**DTE-DCE Interface Error** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>

<span data-ttu-id="14f24-301">**Porte de boîtier ouverte** (15)</span><span class="sxs-lookup"><span data-stu-id="14f24-301">**Enclosure Door Open** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>

<span data-ttu-id="14f24-302">**Dysfonctionnements** de l’équipement (16)</span><span class="sxs-lookup"><span data-stu-id="14f24-302">**Equipment Malfunction** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>

<span data-ttu-id="14f24-303">**Vibration excessive** (17)</span><span class="sxs-lookup"><span data-stu-id="14f24-303">**Excessive Vibration** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>

<span data-ttu-id="14f24-304">**Erreur de format de fichier** (18)</span><span class="sxs-lookup"><span data-stu-id="14f24-304">**File Format Error** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>

<span data-ttu-id="14f24-305">**Incendie détecté** (19)</span><span class="sxs-lookup"><span data-stu-id="14f24-305">**Fire Detected** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>

<span data-ttu-id="14f24-306">**Inondation détectée** (20)</span><span class="sxs-lookup"><span data-stu-id="14f24-306">**Flood Detected** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>

<span data-ttu-id="14f24-307">**Erreur de tramage** (21)</span><span class="sxs-lookup"><span data-stu-id="14f24-307">**Framing Error** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>

<span data-ttu-id="14f24-308">**Problème HVAC** (22)</span><span class="sxs-lookup"><span data-stu-id="14f24-308">**HVAC Problem** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>

<span data-ttu-id="14f24-309">**Humidité inacceptable** (23)</span><span class="sxs-lookup"><span data-stu-id="14f24-309">**Humidity Unacceptable** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>

<span data-ttu-id="14f24-310">**Erreur de périphérique d’e/s** (24)</span><span class="sxs-lookup"><span data-stu-id="14f24-310">**I/O Device Error** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>

<span data-ttu-id="14f24-311">**Erreur de l’appareil d’entrée** (25)</span><span class="sxs-lookup"><span data-stu-id="14f24-311">**Input Device Error** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>

<span data-ttu-id="14f24-312">**Erreur LAN** (26)</span><span class="sxs-lookup"><span data-stu-id="14f24-312">**LAN Error** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="14f24-313">**Fuite non toxique détectée** (27)</span><span class="sxs-lookup"><span data-stu-id="14f24-313">**Non-Toxic Leak Detected** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="14f24-314">**Erreur de transmission du nœud local** (28)</span><span class="sxs-lookup"><span data-stu-id="14f24-314">**Local Node Transmission Error** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>

<span data-ttu-id="14f24-315">**Perte de trame** (29)</span><span class="sxs-lookup"><span data-stu-id="14f24-315">**Loss of Frame** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>

<span data-ttu-id="14f24-316">**Perte de signal** (30)</span><span class="sxs-lookup"><span data-stu-id="14f24-316">**Loss of Signal** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Material_Supply_Exhausted"></span><span id="material_supply_exhausted"></span><span id="MATERIAL_SUPPLY_EXHAUSTED"></span>

<span data-ttu-id="14f24-317">**Fourniture de matériel épuisée** (31)</span><span class="sxs-lookup"><span data-stu-id="14f24-317">**Material Supply Exhausted** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>

<span data-ttu-id="14f24-318">**Problème de multiplexeur** (32)</span><span class="sxs-lookup"><span data-stu-id="14f24-318">**Multiplexer Problem** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>

<span data-ttu-id="14f24-319">**Mémoire insuffisante** (33)</span><span class="sxs-lookup"><span data-stu-id="14f24-319">**Out of Memory** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>

<span data-ttu-id="14f24-320">**Erreur de périphérique de sortie** (34)</span><span class="sxs-lookup"><span data-stu-id="14f24-320">**Output Device Error** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>

<span data-ttu-id="14f24-321">**Performances détériorées** (35)</span><span class="sxs-lookup"><span data-stu-id="14f24-321">**Performance Degraded** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>

<span data-ttu-id="14f24-322">**Problème d’alimentation** (36)</span><span class="sxs-lookup"><span data-stu-id="14f24-322">**Power Problem** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>

<span data-ttu-id="14f24-323">**Pression inacceptable** (37)</span><span class="sxs-lookup"><span data-stu-id="14f24-323">**Pressure Unacceptable** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>

<span data-ttu-id="14f24-324">**Problème de processeur (erreur d’ordinateur interne)** (38)</span><span class="sxs-lookup"><span data-stu-id="14f24-324">**Processor Problem (Internal Machine Error)** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>

<span data-ttu-id="14f24-325">**Échec** de la pompe (39)</span><span class="sxs-lookup"><span data-stu-id="14f24-325">**Pump Failure** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>

<span data-ttu-id="14f24-326">**Taille de file d’attente dépassée** (40)</span><span class="sxs-lookup"><span data-stu-id="14f24-326">**Queue Size Exceeded** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>

<span data-ttu-id="14f24-327">**Échec de réception** (41)</span><span class="sxs-lookup"><span data-stu-id="14f24-327">**Receive Failure** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>

<span data-ttu-id="14f24-328">**Échec du récepteur** (42)</span><span class="sxs-lookup"><span data-stu-id="14f24-328">**Receiver Failure** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="14f24-329">**Erreur de transmission du nœud distant** (43)</span><span class="sxs-lookup"><span data-stu-id="14f24-329">**Remote Node Transmission Error** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>

<span data-ttu-id="14f24-330">**Capacité de la ressource à une capacité proche** (44)</span><span class="sxs-lookup"><span data-stu-id="14f24-330">**Resource at or Nearing Capacity** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>

<span data-ttu-id="14f24-331">**Temps de réponse excessif** (45)</span><span class="sxs-lookup"><span data-stu-id="14f24-331">**Response Time Excessive** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>

<span data-ttu-id="14f24-332">**Taux de retransmission excessif** (46)</span><span class="sxs-lookup"><span data-stu-id="14f24-332">**Retransmission Rate Excessive** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span data-ttu-id="14f24-333">**Erreur logicielle** (47)</span><span class="sxs-lookup"><span data-stu-id="14f24-333">**Software Error** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>

<span data-ttu-id="14f24-334">**Programme logiciel terminé anormalement** (48)</span><span class="sxs-lookup"><span data-stu-id="14f24-334">**Software Program Abnormally Terminated** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>

<span data-ttu-id="14f24-335">**Erreur du programme logiciel (résultats incorrects)** (49)</span><span class="sxs-lookup"><span data-stu-id="14f24-335">**Software Program Error (Incorrect Results)** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>

<span data-ttu-id="14f24-336">**Problème de capacité de stockage** (50)</span><span class="sxs-lookup"><span data-stu-id="14f24-336">**Storage Capacity Problem** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>

<span data-ttu-id="14f24-337">**Température inacceptable** (51)</span><span class="sxs-lookup"><span data-stu-id="14f24-337">**Temperature Unacceptable** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>

<span data-ttu-id="14f24-338">**Seuil dépassé** (52)</span><span class="sxs-lookup"><span data-stu-id="14f24-338">**Threshold Crossed** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>

<span data-ttu-id="14f24-339">**Problème de synchronisation** (53)</span><span class="sxs-lookup"><span data-stu-id="14f24-339">**Timing Problem** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="14f24-340">**Fuite toxique détectée** (54)</span><span class="sxs-lookup"><span data-stu-id="14f24-340">**Toxic Leak Detected** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>

<span data-ttu-id="14f24-341">**Échec** de la transmission (55)</span><span class="sxs-lookup"><span data-stu-id="14f24-341">**Transmit Failure** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>

<span data-ttu-id="14f24-342">**Échec** de l’émetteur (56)</span><span class="sxs-lookup"><span data-stu-id="14f24-342">**Transmitter Failure** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>

<span data-ttu-id="14f24-343">**Ressource sous-jacente non disponible** (57)</span><span class="sxs-lookup"><span data-stu-id="14f24-343">**Underlying Resource Unavailable** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>

<span data-ttu-id="14f24-344">**Incompatibilité de version** (58)</span><span class="sxs-lookup"><span data-stu-id="14f24-344">**Version Mismatch** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>

<span data-ttu-id="14f24-345">**Alerte précédente effacée** (59)</span><span class="sxs-lookup"><span data-stu-id="14f24-345">**Previous Alert Cleared** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Login_Attempts_Failed"></span><span id="login_attempts_failed"></span><span id="LOGIN_ATTEMPTS_FAILED"></span>

<span data-ttu-id="14f24-346">**Échec des tentatives de connexion** (60)</span><span class="sxs-lookup"><span data-stu-id="14f24-346">**Login Attempts Failed** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>

<span data-ttu-id="14f24-347">**Virus logiciel détecté** (61)</span><span class="sxs-lookup"><span data-stu-id="14f24-347">**Software Virus Detected** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>

<span data-ttu-id="14f24-348">**Violation de la sécurité matérielle** (62)</span><span class="sxs-lookup"><span data-stu-id="14f24-348">**Hardware Security Breached** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>

<span data-ttu-id="14f24-349">**Déni de service détecté** (63)</span><span class="sxs-lookup"><span data-stu-id="14f24-349">**Denial of Service Detected** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>

<span data-ttu-id="14f24-350">Non- **concordance des informations d’identification de sécurité** (64)</span><span class="sxs-lookup"><span data-stu-id="14f24-350">**Security Credential Mismatch** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>

<span data-ttu-id="14f24-351">**Accès non autorisé** (65)</span><span class="sxs-lookup"><span data-stu-id="14f24-351">**Unauthorized Access** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>

<span data-ttu-id="14f24-352">**Alarme reçue** (66)</span><span class="sxs-lookup"><span data-stu-id="14f24-352">**Alarm Received** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>

<span data-ttu-id="14f24-353">**Perte de pointeur** (67)</span><span class="sxs-lookup"><span data-stu-id="14f24-353">**Loss of Pointer** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>

<span data-ttu-id="14f24-354">**Incompatibilité de charge utile** (68)</span><span class="sxs-lookup"><span data-stu-id="14f24-354">**Payload Mismatch** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>

<span data-ttu-id="14f24-355">**Erreur de transmission** (69)</span><span class="sxs-lookup"><span data-stu-id="14f24-355">**Transmission Error** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>

<span data-ttu-id="14f24-356">**Taux d’erreur excessif** (70)</span><span class="sxs-lookup"><span data-stu-id="14f24-356">**Excessive Error Rate** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>

<span data-ttu-id="14f24-357">**Problème de suivi** (71)</span><span class="sxs-lookup"><span data-stu-id="14f24-357">**Trace Problem** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>

<span data-ttu-id="14f24-358">**Élément non disponible** (72)</span><span class="sxs-lookup"><span data-stu-id="14f24-358">**Element Unavailable** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>

<span data-ttu-id="14f24-359">**Élément manquant** (73)</span><span class="sxs-lookup"><span data-stu-id="14f24-359">**Element Missing** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>

<span data-ttu-id="14f24-360">**Perte de plusieurs trames** (74)</span><span class="sxs-lookup"><span data-stu-id="14f24-360">**Loss of Multi Frame** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>

<span data-ttu-id="14f24-361">**Échec du canal de diffusion** (75)</span><span class="sxs-lookup"><span data-stu-id="14f24-361">**Broadcast Channel Failure** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>

<span data-ttu-id="14f24-362">**Message reçu non valide** (76)</span><span class="sxs-lookup"><span data-stu-id="14f24-362">**Invalid Message Received** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>

<span data-ttu-id="14f24-363">**Échec de routage** (77)</span><span class="sxs-lookup"><span data-stu-id="14f24-363">**Routing Failure** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>

<span data-ttu-id="14f24-364">**Échec du fond de panier** (78)</span><span class="sxs-lookup"><span data-stu-id="14f24-364">**Backplane Failure** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>

<span data-ttu-id="14f24-365">**Duplication des identificateurs** (79)</span><span class="sxs-lookup"><span data-stu-id="14f24-365">**Identifier Duplication** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>

<span data-ttu-id="14f24-366">**Échec du chemin d’accès de protection** (80)</span><span class="sxs-lookup"><span data-stu-id="14f24-366">**Protection Path Failure** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>

<span data-ttu-id="14f24-367">**Perte ou incompatibilité** de la synchronisation (81)</span><span class="sxs-lookup"><span data-stu-id="14f24-367">**Sync Loss or Mismatch** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>

<span data-ttu-id="14f24-368">**Problème de terminal** (82)</span><span class="sxs-lookup"><span data-stu-id="14f24-368">**Terminal Problem** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>

<span data-ttu-id="14f24-369">**Échec de l’horloge en temps réel** (83)</span><span class="sxs-lookup"><span data-stu-id="14f24-369">**Real Time Clock Failure** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>

<span data-ttu-id="14f24-370">**Défaillance** de l’antenne (84)</span><span class="sxs-lookup"><span data-stu-id="14f24-370">**Antenna Failure** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>

<span data-ttu-id="14f24-371">**Échec de chargement** de la batterie (85)</span><span class="sxs-lookup"><span data-stu-id="14f24-371">**Battery Charging Failure** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>

<span data-ttu-id="14f24-372">**Défaillance du disque** (86)</span><span class="sxs-lookup"><span data-stu-id="14f24-372">**Disk Failure** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>

<span data-ttu-id="14f24-373">**Échec du saut de fréquence** (87)</span><span class="sxs-lookup"><span data-stu-id="14f24-373">**Frequency Hopping Failure** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>

<span data-ttu-id="14f24-374">**Perte de redondance** (88)</span><span class="sxs-lookup"><span data-stu-id="14f24-374">**Loss of Redundancy** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>

<span data-ttu-id="14f24-375">**Échec** de l’alimentation (89)</span><span class="sxs-lookup"><span data-stu-id="14f24-375">**Power Supply Failure** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>

<span data-ttu-id="14f24-376">**Problème de qualité du signal** (90)</span><span class="sxs-lookup"><span data-stu-id="14f24-376">**Signal Quality Problem** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Discharging"></span><span id="battery_discharging"></span><span id="BATTERY_DISCHARGING"></span>

<span data-ttu-id="14f24-377">**Déchargement** de la batterie (91)</span><span class="sxs-lookup"><span data-stu-id="14f24-377">**Battery Discharging** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>

<span data-ttu-id="14f24-378">**Défaillance** de la batterie (92)</span><span class="sxs-lookup"><span data-stu-id="14f24-378">**Battery Failure** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>

<span data-ttu-id="14f24-379">**Problème commercial** de l’électricité (93)</span><span class="sxs-lookup"><span data-stu-id="14f24-379">**Commercial Power Problem** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>

<span data-ttu-id="14f24-380">**Défaillance du ventilateur** (94)</span><span class="sxs-lookup"><span data-stu-id="14f24-380">**Fan Failure** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>

<span data-ttu-id="14f24-381">**Défaillance du moteur** (95)</span><span class="sxs-lookup"><span data-stu-id="14f24-381">**Engine Failure** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>

<span data-ttu-id="14f24-382">**Défaillance du capteur** (96)</span><span class="sxs-lookup"><span data-stu-id="14f24-382">**Sensor Failure** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>

<span data-ttu-id="14f24-383">**Échec de fusible** (97)</span><span class="sxs-lookup"><span data-stu-id="14f24-383">**Fuse Failure** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>

<span data-ttu-id="14f24-384">**Échec du générateur** (98)</span><span class="sxs-lookup"><span data-stu-id="14f24-384">**Generator Failure** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>

<span data-ttu-id="14f24-385">**Batterie faible** (99)</span><span class="sxs-lookup"><span data-stu-id="14f24-385">**Low Battery** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>

<span data-ttu-id="14f24-386">**Carburant faible** (100)</span><span class="sxs-lookup"><span data-stu-id="14f24-386">**Low Fuel** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>

<span data-ttu-id="14f24-387">**Faible eau** (101)</span><span class="sxs-lookup"><span data-stu-id="14f24-387">**Low Water** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>

<span data-ttu-id="14f24-388">**Gaz explosif** (102)</span><span class="sxs-lookup"><span data-stu-id="14f24-388">**Explosive Gas** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>

<span data-ttu-id="14f24-389">**Vents élevés** (103)</span><span class="sxs-lookup"><span data-stu-id="14f24-389">**High Winds** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>

<span data-ttu-id="14f24-390">**Accumulations de glace** (104)</span><span class="sxs-lookup"><span data-stu-id="14f24-390">**Ice Buildup** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>

<span data-ttu-id="14f24-391">**Fumée** (105)</span><span class="sxs-lookup"><span data-stu-id="14f24-391">**Smoke** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>

<span data-ttu-id="14f24-392">**Incompatibilité de mémoire** (106)</span><span class="sxs-lookup"><span data-stu-id="14f24-392">**Memory Mismatch** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>

<span data-ttu-id="14f24-393">**Cycles de processeur insuffisants** (107)</span><span class="sxs-lookup"><span data-stu-id="14f24-393">**Out of CPU Cycles** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>

<span data-ttu-id="14f24-394">**Problème de l’environnement logiciel** (108)</span><span class="sxs-lookup"><span data-stu-id="14f24-394">**Software Environment Problem** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>

<span data-ttu-id="14f24-395">**Échec du téléchargement de logiciels** (109)</span><span class="sxs-lookup"><span data-stu-id="14f24-395">**Software Download Failure** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>

<span data-ttu-id="14f24-396">**Élément réinitialisé** (110)</span><span class="sxs-lookup"><span data-stu-id="14f24-396">**Element Reinitialized** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>

<span data-ttu-id="14f24-397">**Délai d’expiration** (111)</span><span class="sxs-lookup"><span data-stu-id="14f24-397">**Timeout** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>

<span data-ttu-id="14f24-398">**Problèmes de journalisation** (112)</span><span class="sxs-lookup"><span data-stu-id="14f24-398">**Logging Problems** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>

<span data-ttu-id="14f24-399">**Fuite détectée** (113)</span><span class="sxs-lookup"><span data-stu-id="14f24-399">**Leak Detected** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>

<span data-ttu-id="14f24-400">**Échec du mécanisme de protection** (114)</span><span class="sxs-lookup"><span data-stu-id="14f24-400">**Protection Mechanism Failure** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="Protecting_Resource_Failure"></span><span id="protecting_resource_failure"></span><span id="PROTECTING_RESOURCE_FAILURE"></span>

<span data-ttu-id="14f24-401">**Protection des échecs de ressource** (115)</span><span class="sxs-lookup"><span data-stu-id="14f24-401">**Protecting Resource Failure** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>

<span data-ttu-id="14f24-402">**Incohérence de base de données** (116)</span><span class="sxs-lookup"><span data-stu-id="14f24-402">**Database Inconsistency** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>

<span data-ttu-id="14f24-403">**Échec de l’authentification** (117)</span><span class="sxs-lookup"><span data-stu-id="14f24-403">**Authentication Failure** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>

<span data-ttu-id="14f24-404">**Violation de la confidentialité** (118)</span><span class="sxs-lookup"><span data-stu-id="14f24-404">**Breach of Confidentiality** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>

<span data-ttu-id="14f24-405">**Falsification de câble** (119)</span><span class="sxs-lookup"><span data-stu-id="14f24-405">**Cable Tamper** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>

<span data-ttu-id="14f24-406">**Informations retardées** (120)</span><span class="sxs-lookup"><span data-stu-id="14f24-406">**Delayed Information** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>

<span data-ttu-id="14f24-407">**Informations dupliquées** (121)</span><span class="sxs-lookup"><span data-stu-id="14f24-407">**Duplicate Information** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>

<span data-ttu-id="14f24-408">**Informations manquantes** (122)</span><span class="sxs-lookup"><span data-stu-id="14f24-408">**Information Missing** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>

<span data-ttu-id="14f24-409">**Modification des informations** (123)</span><span class="sxs-lookup"><span data-stu-id="14f24-409">**Information Modification** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>

<span data-ttu-id="14f24-410">**Informations hors séquence** (124)</span><span class="sxs-lookup"><span data-stu-id="14f24-410">**Information Out of Sequence** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>

<span data-ttu-id="14f24-411">**Clé expirée** (125)</span><span class="sxs-lookup"><span data-stu-id="14f24-411">**Key Expired** (125)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>

<span data-ttu-id="14f24-412">**Échec de la non-répudiation** (126)</span><span class="sxs-lookup"><span data-stu-id="14f24-412">**Non-Repudiation Failure** (126)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>

<span data-ttu-id="14f24-413">**Activité en dehors des heures** (127)</span><span class="sxs-lookup"><span data-stu-id="14f24-413">**Out of Hours Activity** (127)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>

<span data-ttu-id="14f24-414">**Hors service** (128)</span><span class="sxs-lookup"><span data-stu-id="14f24-414">**Out of Service** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>

<span data-ttu-id="14f24-415">**Erreur de procédure** (129)</span><span class="sxs-lookup"><span data-stu-id="14f24-415">**Procedural Error** (129)</span></span>


</dt> <dd></dd> <dt>

<span id="Unexpected_Information"></span><span id="unexpected_information"></span><span id="UNEXPECTED_INFORMATION"></span>

<span data-ttu-id="14f24-416">**Informations inattendues** (130)</span><span class="sxs-lookup"><span data-stu-id="14f24-416">**Unexpected Information** (130)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="14f24-417">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="14f24-417">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="14f24-418">**ProbableCauseDescription**</span><span class="sxs-lookup"><span data-stu-id="14f24-418">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14f24-419">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="14f24-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14f24-420">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14f24-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14f24-421">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erreur CIM**.**ProbableCause**")</span><span class="sxs-lookup"><span data-stu-id="14f24-421">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="14f24-422">Chaîne de forme libre qui décrit la cause probable de l’erreur, lorsque la propriété **ProbableCause** est définie sur « 1 » (autre).</span><span class="sxs-lookup"><span data-stu-id="14f24-422">A free-form string that describes the probable cause of the error, when the **ProbableCause** property is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="14f24-423">**RecommendedActions**</span><span class="sxs-lookup"><span data-stu-id="14f24-423">**RecommendedActions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14f24-424">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="14f24-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="14f24-425">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14f24-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="14f24-426">Tableau de chaînes de forme libre qui décrivent les actions recommandées pour résoudre l’erreur.</span><span class="sxs-lookup"><span data-stu-id="14f24-426">An array of free-form strings that describe the recommended actions to take to resolve the error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14f24-427">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14f24-427">Requirements</span></span>



| <span data-ttu-id="14f24-428">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14f24-428">Requirement</span></span> | <span data-ttu-id="14f24-429">Valeur</span><span class="sxs-lookup"><span data-stu-id="14f24-429">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14f24-430">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14f24-430">Minimum supported client</span></span><br/> | <span data-ttu-id="14f24-431">Windows 8</span><span class="sxs-lookup"><span data-stu-id="14f24-431">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="14f24-432">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14f24-432">Minimum supported server</span></span><br/> | <span data-ttu-id="14f24-433">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14f24-433">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="14f24-434">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="14f24-434">Namespace</span></span><br/>                | <span data-ttu-id="14f24-435">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="14f24-435">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="14f24-436">MOF</span><span class="sxs-lookup"><span data-stu-id="14f24-436">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14f24-437"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14f24-437"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="14f24-438">DLL</span><span class="sxs-lookup"><span data-stu-id="14f24-438">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14f24-439"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="14f24-439"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

