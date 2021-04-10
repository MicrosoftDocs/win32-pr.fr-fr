---
description: Contient des informations sur la gravité, la cause, les actions recommandées et d’autres données relatives à l’échec d’une opération CIM.
ms.assetid: 128B9ECE-D26C-4A7D-BFB7-69CD986B0DBA
title: Classe Msvm_Error
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Error
- Msvm_Error.ErrorType
- Msvm_Error.OtherErrorType
- Msvm_Error.OwningEntity
- Msvm_Error.MessageID
- Msvm_Error.Message
- Msvm_Error.MessageArguments
- Msvm_Error.PerceivedSeverity
- Msvm_Error.ProbableCause
- Msvm_Error.ProbableCauseDescription
- Msvm_Error.RecommendedActions
- Msvm_Error.ErrorSource
- Msvm_Error.ErrorSourceFormat
- Msvm_Error.OtherErrorSourceFormat
- Msvm_Error.CIMStatusCode
- Msvm_Error.CIMStatusCodeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 56b3b30f1d64146db2554d097b11104df09ba018
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034581"
---
# <a name="msvm_error-class"></a><span data-ttu-id="a5bec-103">MSVM, \_ classe d’erreur</span><span class="sxs-lookup"><span data-stu-id="a5bec-103">Msvm\_Error class</span></span>

<span data-ttu-id="a5bec-104">Classe spécialisée qui contient des informations sur la gravité, la cause, les actions recommandées et d’autres données relatives à l’échec d’une opération CIM.</span><span class="sxs-lookup"><span data-stu-id="a5bec-104">A specialized class that contains information about the severity, cause, recommended actions, and other data related to the failure of a CIM Operation.</span></span>

<span data-ttu-id="a5bec-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a5bec-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5bec-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5bec-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Error : CIM_Error
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

## <a name="members"></a><span data-ttu-id="a5bec-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a5bec-107">Members</span></span>

<span data-ttu-id="a5bec-108">La classe d' **\_ erreur MSVM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a5bec-108">The **Msvm\_Error** class has these types of members:</span></span>

-   [<span data-ttu-id="a5bec-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a5bec-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5bec-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a5bec-110">Properties</span></span>

<span data-ttu-id="a5bec-111">La classe d' **\_ erreur MSVM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a5bec-111">The **Msvm\_Error** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a5bec-112">**CIMStatusCode**</span><span class="sxs-lookup"><span data-stu-id="a5bec-112">**CIMStatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bec-113">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a5bec-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5bec-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bec-115">Code d’État CIM qui caractérise cette instance.</span><span class="sxs-lookup"><span data-stu-id="a5bec-115">The CIM status code that characterizes this instance.</span></span> <span data-ttu-id="a5bec-116">Cette propriété définit les codes d’État qui peuvent être retournés par un serveur ou un écouteur CIM conforme.</span><span class="sxs-lookup"><span data-stu-id="a5bec-116">This property defines the status codes that may be return by a conforming CIM Server or Listener.</span></span> <span data-ttu-id="a5bec-117">Tous les codes d’État ne sont pas valides pour chaque opération.</span><span class="sxs-lookup"><span data-stu-id="a5bec-117">Not all status codes are valid for each operation.</span></span> <span data-ttu-id="a5bec-118">La spécification de chaque opération doit définir les codes d’État qui peuvent être renvoyés par cette opération.</span><span class="sxs-lookup"><span data-stu-id="a5bec-118">The specification for each operation should define the status codes that may be returned by that operation.</span></span> <span data-ttu-id="a5bec-119">Les valeurs suivantes pour le code d’État CIM sont définies.</span><span class="sxs-lookup"><span data-stu-id="a5bec-119">The following values for CIM status code are defined.</span></span> <span data-ttu-id="a5bec-120">Cette propriété est héritée de l' [**\_ erreur CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5bec-120">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>



| <span data-ttu-id="a5bec-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5bec-121">Value</span></span>                                                                                                                                                                                                                                                                                          | <span data-ttu-id="a5bec-122">Signification</span><span class="sxs-lookup"><span data-stu-id="a5bec-122">Meaning</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span><dl> <span data-ttu-id="a5bec-123"><dt>**CIM \_ \_Échec**</dt> de l’erreur <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-123"><dt>**CIM\_ERR\_FAILED**</dt> <dt>1</dt></span></span> </dl>                                                                       | <span data-ttu-id="a5bec-124">Une erreur générale s’est produite et n’est pas couverte par un code d’erreur plus spécifique.</span><span class="sxs-lookup"><span data-stu-id="a5bec-124">A general error occurred that is not covered by a more specific error code.</span></span><br/>    |
| <span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span><dl> <span data-ttu-id="a5bec-125"><dt>**CIM \_ \_Accès à Err \_ refusé**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-125"><dt>**CIM\_ERR\_ACCESS\_DENIED**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="a5bec-126">L’accès à une ressource CIM n’était pas disponible pour le client.</span><span class="sxs-lookup"><span data-stu-id="a5bec-126">Access to a CIM resource was not available to the client.</span></span><br/>                      |
| <span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span><dl> <span data-ttu-id="a5bec-127"><dt>**CIM \_ ERREUR de l' \_ \_ espace de noms 3 non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-127"><dt>**CIM\_ERR\_INVALID\_NAMESPACE**</dt> <dt>3</dt></span></span> </dl>                                     | <span data-ttu-id="a5bec-128">L’espace de noms cible n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="a5bec-128">The target namespace does not exist.</span></span><br/>                                           |
| <span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span><dl> <span data-ttu-id="a5bec-129"><dt>**CIM \_ ERR \_ \_ paramètre non valide**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-129"><dt>**CIM\_ERR\_INVALID\_PARAMETER**</dt> <dt>4</dt></span></span> </dl>                                     | <span data-ttu-id="a5bec-130">Une ou plusieurs valeurs de paramètre passées à la méthode ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="a5bec-130">One or more parameter values passed to the method were invalid.</span></span><br/>                |
| <span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span><dl> <span data-ttu-id="a5bec-131"><dt>**CIM \_ ERR \_ \_ classe 5 non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-131"><dt>**CIM\_ERR\_INVALID\_CLASS**</dt> <dt>5</dt></span></span> </dl>                                                 | <span data-ttu-id="a5bec-132">La classe spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="a5bec-132">The specified class does not exist.</span></span><br/>                                            |
| <span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span><dl> <span data-ttu-id="a5bec-133"><dt>**CIM \_ ERR \_ \_ introuvable**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-133"><dt>**CIM\_ERR\_NOT\_FOUND**</dt> <dt>6</dt></span></span> </dl>                                                             | <span data-ttu-id="a5bec-134">L’objet demandé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="a5bec-134">The requested object could not be found.</span></span><br/>                                       |
| <span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span><dl> <span data-ttu-id="a5bec-135"><dt>**CIM \_ ERR \_ non \_ prise en charge**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-135"><dt>**CIM\_ERR\_NOT\_SUPPORTED**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="a5bec-136">L'opération demandée n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a5bec-136">The requested operation is not supported.</span></span><br/>                                      |
| <span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span><dl> <span data-ttu-id="a5bec-137"><dt>**CIM \_ La \_ classe Err \_ a des \_ enfants**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-137"><dt>**CIM\_ERR\_CLASS\_HAS\_CHILDREN**</dt> <dt>8</dt></span></span> </dl>                                 | <span data-ttu-id="a5bec-138">Impossible d’effectuer l’opération sur cette classe, car elle contient des instances.</span><span class="sxs-lookup"><span data-stu-id="a5bec-138">Operation cannot be carried out on this class because it has instances.</span></span><br/>        |
| <span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span><dl> <span data-ttu-id="a5bec-139"><dt>**CIM \_ La \_ classe Err \_ a des \_ instances**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-139"><dt>**CIM\_ERR\_CLASS\_HAS\_INSTANCES**</dt> <dt>9</dt></span></span> </dl>                              | <span data-ttu-id="a5bec-140">Impossible d’effectuer l’opération sur cette classe, car elle contient des instances.</span><span class="sxs-lookup"><span data-stu-id="a5bec-140">Operation cannot be carried out on this class since it has instances.</span></span><br/>          |
| <span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span><dl> <span data-ttu-id="a5bec-141"><dt>**CIM \_ ERREUR \_ de \_ superclasse 10 non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-141"><dt>**CIM\_ERR\_INVALID\_SUPERCLASS**</dt> <dt>10</dt></span></span> </dl>                                 | <span data-ttu-id="a5bec-142">Impossible d’effectuer l’opération, car la superclasse spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="a5bec-142">Operation cannot be carried out since the specified superclass does not exist.</span></span><br/> |
| <span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span><dl> <span data-ttu-id="a5bec-143"><dt>**CIM \_ ERR \_ \_ existe déjà**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-143"><dt>**CIM\_ERR\_ALREADY\_EXISTS**</dt> <dt>11</dt></span></span> </dl>                                             | <span data-ttu-id="a5bec-144">Impossible d’effectuer l’opération, car un objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="a5bec-144">Operation cannot be carried out because an object already exists.</span></span><br/>              |
| <span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span><dl> <span data-ttu-id="a5bec-145"><dt>**CIM \_ ERR \_ aucune \_ \_ propriété**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-145"><dt>**CIM\_ERR\_NO\_SUCH\_PROPERTY**</dt> <dt>12</dt></span></span> </dl>                                      | <span data-ttu-id="a5bec-146">La propriété spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="a5bec-146">The specified Property does not exist.</span></span><br/>                                         |
| <span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span><dl> <span data-ttu-id="a5bec-147"><dt>**CIM \_ \_Incompatibilité \_ de type Err**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-147"><dt>**CIM\_ERR\_TYPE\_MISMATCH**</dt> <dt>13</dt></span></span> </dl>                                                | <span data-ttu-id="a5bec-148">La valeur fournie est incompatible avec le type.</span><span class="sxs-lookup"><span data-stu-id="a5bec-148">The value supplied is incompatible with the type.</span></span><br/>                              |
| <span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span><dl> <span data-ttu-id="a5bec-149"><dt>**CIM \_ \_Langue de requête Err \_ \_ non \_ prise en charge**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-149"><dt>**CIM\_ERR\_QUERY\_LANGUAGE\_NOT\_SUPPORTED**</dt> <dt>14</dt></span></span> </dl> | <span data-ttu-id="a5bec-150">Le langage de requête n’est pas reconnu ou n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a5bec-150">The query language is not recognized or supported.</span></span><br/>                             |
| <span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span><dl> <span data-ttu-id="a5bec-151"><dt>**CIM \_ \_ \_ Requête Err non valide**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-151"><dt>**CIM\_ERR\_INVALID\_QUERY**</dt> <dt>15</dt></span></span> </dl>                                                | <span data-ttu-id="a5bec-152">La requête n’est pas valide pour le langage de requête spécifié.</span><span class="sxs-lookup"><span data-stu-id="a5bec-152">The query is not valid for the specified query language.</span></span><br/>                       |
| <span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span><dl> <span data-ttu-id="a5bec-153"><dt>**CIM \_ \_Méthode Err \_ non \_ disponible**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-153"><dt>**CIM\_ERR\_METHOD\_NOT\_AVAILABLE**</dt> <dt>16</dt></span></span> </dl>                          | <span data-ttu-id="a5bec-154">La méthode extrinsèque n’a pas pu être exécutée.</span><span class="sxs-lookup"><span data-stu-id="a5bec-154">The extrinsic method could not be executed.</span></span><br/>                                    |
| <span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span><dl> <span data-ttu-id="a5bec-155"><dt>**CIM \_ \_Méthode Err \_ \_ introuvable**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-155"><dt>**CIM\_ERR\_METHOD\_NOT\_FOUND**</dt> <dt>17</dt></span></span> </dl>                                      | <span data-ttu-id="a5bec-156">La méthode extrinsèque spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="a5bec-156">The specified extrinsic method does not exist.</span></span><br/>                                 |
| <span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span><dl> <span data-ttu-id="a5bec-157"><dt>**CIM \_ \_ \_ Réponse inattendue de Err**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-157"><dt>**CIM\_ERR\_UNEXPECTED\_RESPONSE**</dt> <dt>18</dt></span></span> </dl>                              | <span data-ttu-id="a5bec-158">La réponse retournée à l’opération asynchrone n’était pas attendue.</span><span class="sxs-lookup"><span data-stu-id="a5bec-158">The returned response to the asynchronous operation was not expected.</span></span><br/>          |
| <span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span><dl> <span data-ttu-id="a5bec-159"><dt>**CIM \_ Erreur \_ de \_ \_ destination de réponse Err non valide**</dt> <dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-159"><dt>**CIM\_ERR\_INVALID\_RESPONSE\_DESTINATION**</dt> <dt>19</dt></span></span> </dl>  | <span data-ttu-id="a5bec-160">La destination spécifiée pour la réponse asynchrone n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a5bec-160">The specified destination for the asynchronous response is not valid.</span></span><br/>          |
| <span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span><dl> <span data-ttu-id="a5bec-161"><dt>**CIM \_ L' \_ espace de noms Err \_ n’est pas \_ vide**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-161"><dt>**CIM\_ERR\_NAMESPACE\_NOT\_EMPTY**</dt> <dt>20</dt></span></span> </dl>                             | <span data-ttu-id="a5bec-162">L’espace de noms spécifié n’est pas vide.</span><span class="sxs-lookup"><span data-stu-id="a5bec-162">The specified namespace is not empty.</span></span><br/>                                          |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="a5bec-163"><dt>**DMTF, réservé**</dt> <dt>21 = *valeur*</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-163"><dt>**DMTF Reserved**</dt> <dt>21 = *value* </dt></span></span> </dl>                            | <span data-ttu-id="a5bec-164">Valeurs réservées.</span><span class="sxs-lookup"><span data-stu-id="a5bec-164">Reserved values.</span></span><br/>                                                               |



 

</dd> <dt>

<span data-ttu-id="a5bec-165">**CIMStatusCodeDescription**</span><span class="sxs-lookup"><span data-stu-id="a5bec-165">**CIMStatusCodeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bec-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a5bec-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5bec-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bec-168">Chaîne contenant une description lisible par l’utilisateur de la propriété **CIMStatusCode** .</span><span class="sxs-lookup"><span data-stu-id="a5bec-168">A string containing a user-readable description of the **CIMStatusCode** property.</span></span> <span data-ttu-id="a5bec-169">Cette description peut s’étendre, mais doit être cohérente avec, la définition de **CIMStatusCode**.</span><span class="sxs-lookup"><span data-stu-id="a5bec-169">This description may extend, but must be consistent with, the definition of **CIMStatusCode**.</span></span> <span data-ttu-id="a5bec-170">Cette propriété est héritée de l' [**\_ erreur CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5bec-170">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a5bec-171">**ErrorSource**</span><span class="sxs-lookup"><span data-stu-id="a5bec-171">**ErrorSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bec-172">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a5bec-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5bec-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bec-174">Informations d’identification de l’entité (instance) générant l’erreur.</span><span class="sxs-lookup"><span data-stu-id="a5bec-174">The identifying information of the entity (the instance) generating the error.</span></span> <span data-ttu-id="a5bec-175">Si cette entité est modélisée dans le schéma CIM, cette propriété contient le chemin d’accès de l’instance encodée sous la forme d’un paramètre de chaîne.</span><span class="sxs-lookup"><span data-stu-id="a5bec-175">If this entity is modeled in the CIM Schema, this property contains the path of the instance encoded as a string parameter.</span></span> <span data-ttu-id="a5bec-176">Si elle n’est pas modélisée, la propriété contient une chaîne d’identification qui nomme l’entité qui a généré l’erreur.</span><span class="sxs-lookup"><span data-stu-id="a5bec-176">If not modeled, the property contains some identifying string that names the entity that generated the error.</span></span> <span data-ttu-id="a5bec-177">Le chemin d’accès ou la chaîne d’identification est mis en forme selon la propriété **ErrorSourceFormat** .</span><span class="sxs-lookup"><span data-stu-id="a5bec-177">The path or identifying string is formatted per the **ErrorSourceFormat** property.</span></span> <span data-ttu-id="a5bec-178">Cette propriété est héritée de l' [**\_ erreur CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5bec-178">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a5bec-179">**ErrorSourceFormat**</span><span class="sxs-lookup"><span data-stu-id="a5bec-179">**ErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bec-180">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a5bec-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5bec-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bec-182">Le format de la propriété **ErrorSource** peut être interprété en fonction de la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="a5bec-182">The format of the **ErrorSource** property is interpretable based on the value of this property.</span></span> <span data-ttu-id="a5bec-183">Cette propriété est héritée de l' [**\_ erreur CIM**](/previous-versions//cc150671(v=vs.85))et est toujours définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="a5bec-183">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)), and it is always set to 0.</span></span>



| <span data-ttu-id="a5bec-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5bec-184">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="a5bec-185">Signification</span><span class="sxs-lookup"><span data-stu-id="a5bec-185">Meaning</span></span>                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="a5bec-186"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-186"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="a5bec-187">Le format est inconnu ou ne peut pas être interprété de manière significative par une application cliente CIM.</span><span class="sxs-lookup"><span data-stu-id="a5bec-187">The format is unknown or not meaningfully interpretable by a CIM client application.</span></span><br/>                                         |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="a5bec-188"><dt>**Autre**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-188"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                          | <span data-ttu-id="a5bec-189">Le format est défini par la valeur de la propriété **OtherErrorSourceFormat** .</span><span class="sxs-lookup"><span data-stu-id="a5bec-189">The format is defined by the value of the **OtherErrorSourceFormat** property.</span></span><br/>                                               |
| <span id="CIMObjectHandle"></span><span id="cimobjecthandle"></span><span id="CIMOBJECTHANDLE"></span><dl> <span data-ttu-id="a5bec-190"><dt>**CIMObjectHandle**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-190"><dt>**CIMObjectHandle**</dt> <dt>2 </dt></span></span> </dl> | <span data-ttu-id="a5bec-191">Un handle d’objet CIM, encodé à l’aide de la syntaxe MOF définie pour le objectHandle non-terminal, est utilisé pour identifier l’entité.</span><span class="sxs-lookup"><span data-stu-id="a5bec-191">A CIM Object Handle, encoded using the MOF syntax defined for the objectHandle non-terminal, is used to identify the entity.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a5bec-192">**ErrorType**</span><span class="sxs-lookup"><span data-stu-id="a5bec-192">**ErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bec-193">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a5bec-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5bec-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bec-195">Classification principale de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="a5bec-195">Primary classification of the error.</span></span> <span data-ttu-id="a5bec-196">Les valeurs suivantes sont définies.</span><span class="sxs-lookup"><span data-stu-id="a5bec-196">The following values are defined.</span></span> <span data-ttu-id="a5bec-197">Cette propriété est héritée de l' [**\_ erreur CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5bec-197">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>



| <span data-ttu-id="a5bec-198">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5bec-198">Value</span></span>                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="a5bec-199">Signification</span><span class="sxs-lookup"><span data-stu-id="a5bec-199">Meaning</span></span>                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="a5bec-200"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-200"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                                                   |                                                                                                                                                          |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="a5bec-201"><dt>**Autre**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-201"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                                                           |                                                                                                                                                          |
| <span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span><dl> <span data-ttu-id="a5bec-202"><dt>**Erreur de communication**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-202"><dt>**Communications Error**</dt> <dt>2</dt></span></span> </dl>                               | <span data-ttu-id="a5bec-203">Les erreurs de ce type sont principalement associées aux procédures et/ou aux processus requis pour transmettre des informations d’un point à un autre.</span><span class="sxs-lookup"><span data-stu-id="a5bec-203">Errors of this type are principally associated with the procedures and/or processes required to convey information from one point to another.</span></span><br/> |
| <span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span><dl> <span data-ttu-id="a5bec-204"><dt>**Erreur de qualité de service**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-204"><dt>**Quality of Service Error**</dt> <dt>3</dt></span></span> </dl>               | <span data-ttu-id="a5bec-205">Les erreurs de ce type sont principalement associées à des échecs qui entraînent une réduction des fonctionnalités ou des performances.</span><span class="sxs-lookup"><span data-stu-id="a5bec-205">Errors of this type are principally associated with failures that result in reduced functionality or performance.</span></span><br/>                             |
| <span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span><dl> <span data-ttu-id="a5bec-206"><dt>**Erreur logicielle**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-206"><dt>**Software Error**</dt> <dt>4</dt></span></span> </dl>                                                       | <span data-ttu-id="a5bec-207">Une erreur de ce type est principalement associée à un logiciel ou à une erreur de traitement.</span><span class="sxs-lookup"><span data-stu-id="a5bec-207">Error of this type are principally associated with a software or processing fault.</span></span><br/>                                                            |
| <span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span><dl> <span data-ttu-id="a5bec-208"><dt>**Erreur matérielle**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-208"><dt>**Hardware Error**</dt> <dt>5</dt></span></span> </dl>                                                       | <span data-ttu-id="a5bec-209">Les erreurs de ce type sont principalement associées à une défaillance matérielle ou matérielle.</span><span class="sxs-lookup"><span data-stu-id="a5bec-209">Errors of this type are principally associated with an equipment or hardware failure.</span></span><br/>                                                         |
| <span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span><dl> <span data-ttu-id="a5bec-210"><dt>**Erreur environnementale**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-210"><dt>**Environmental Error**</dt> <dt>6</dt></span></span> </dl>                                   | <span data-ttu-id="a5bec-211">Les erreurs de ce type sont principalement associées à une condition d’échec relative à l’installation ou à d’autres considérations environnementales.</span><span class="sxs-lookup"><span data-stu-id="a5bec-211">Errors of this type are principally associated with a failure condition relating to the facility, or other environmental considerations.</span></span><br/>      |
| <span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span><dl> <span data-ttu-id="a5bec-212"><dt>**Erreur de sécurité**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-212"><dt>**Security Error**</dt> <dt>7</dt></span></span> </dl>                                                       | <span data-ttu-id="a5bec-213">Les erreurs de ce type sont associées à des violations de sécurité, à la détection de virus et à des problèmes similaires.</span><span class="sxs-lookup"><span data-stu-id="a5bec-213">Errors of this type are associated with security violations, detection of viruses, and similar issues.</span></span><br/>                                        |
| <span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span><dl> <span data-ttu-id="a5bec-214"><dt>**Erreur de surabonnement**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-214"><dt>**Oversubscription Error**</dt> <dt>8</dt></span></span> </dl>                       | <span data-ttu-id="a5bec-215">Les erreurs de ce type sont principalement associées à l’échec d’allocation des ressources suffisantes pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="a5bec-215">Errors of this type are principally associated with the failure to allocate sufficient resources to complete the operation.</span></span><br/>                   |
| <span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span><dl> <span data-ttu-id="a5bec-216"><dt>**Erreur de ressource non disponible**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-216"><dt>**Unavailable Resource Error**</dt> <dt>9</dt></span></span> </dl>       | <span data-ttu-id="a5bec-217">Les erreurs de ce type sont principalement associées à l’échec d’accès à une ressource requise.</span><span class="sxs-lookup"><span data-stu-id="a5bec-217">Errors of this type are principally associated with the failure to access a required resource.</span></span><br/>                                                |
| <span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span><dl> <span data-ttu-id="a5bec-218"><dt>**Erreur d’opération 10 non prise en charge**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-218"><dt>**Unsupported Operation Error**</dt> <dt>10 </dt></span></span> </dl> | <span data-ttu-id="a5bec-219">Les erreurs de ce type sont associées principalement aux demandes qui ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a5bec-219">Errors of this type are principally associated with requests that are not supported.</span></span><br/>                                                          |



 

</dd> <dt>

<span data-ttu-id="a5bec-220">**Message**</span><span class="sxs-lookup"><span data-stu-id="a5bec-220">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bec-221">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a5bec-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5bec-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bec-223">Message mis en forme.</span><span class="sxs-lookup"><span data-stu-id="a5bec-223">The formatted message.</span></span> <span data-ttu-id="a5bec-224">Ce message est construit en appliquant le contenu dynamique du message, décrit dans **MessageArguments**, à la chaîne de format identifiée de façon unique, dans l’étendue du **OwningEntity**, par **MessageID**.</span><span class="sxs-lookup"><span data-stu-id="a5bec-224">This message is constructed by applying the dynamic content of the message, described in **MessageArguments**, to the format string uniquely identified, within the scope of the **OwningEntity**, by **MessageID**.</span></span> <span data-ttu-id="a5bec-225">Cette propriété est héritée de l' [**\_ erreur CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5bec-225">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a5bec-226">**MessageArguments**</span><span class="sxs-lookup"><span data-stu-id="a5bec-226">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bec-227">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="a5bec-227">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5bec-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bec-229">Tableau contenant le contenu dynamique du message.</span><span class="sxs-lookup"><span data-stu-id="a5bec-229">An array containing the dynamic content of the message.</span></span> <span data-ttu-id="a5bec-230">Cette propriété est héritée de l' [**\_ erreur CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5bec-230">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a5bec-231">**ID**</span><span class="sxs-lookup"><span data-stu-id="a5bec-231">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bec-232">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a5bec-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5bec-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bec-234">Chaîne opaque qui identifie de façon unique, au sein de la portée de la **OwningEntity**, le format du message.</span><span class="sxs-lookup"><span data-stu-id="a5bec-234">An opaque string that uniquely identifies, within the scope of the **OwningEntity**, the format of the message.</span></span> <span data-ttu-id="a5bec-235">Cette propriété est héritée de l' [**\_ erreur CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5bec-235">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a5bec-236">**OtherErrorSourceFormat**</span><span class="sxs-lookup"><span data-stu-id="a5bec-236">**OtherErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bec-237">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a5bec-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5bec-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bec-239">Chaîne définissant les valeurs « Other » pour **ErrorSourceFormat**.</span><span class="sxs-lookup"><span data-stu-id="a5bec-239">A string defining "Other" values for **ErrorSourceFormat**.</span></span> <span data-ttu-id="a5bec-240">Cette valeur doit être définie sur une valeur non NULL lorsque **ErrorSourceFormat** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="a5bec-240">This value must be set to a non-NULL value when **ErrorSourceFormat** is set to a value of 1 (Other).</span></span> <span data-ttu-id="a5bec-241">Pour toutes les autres valeurs de **ErrorSourceFormat**, la valeur de cette chaîne doit être définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="a5bec-241">For all other values of **ErrorSourceFormat**, the value of this string must be set to **Null**.</span></span> <span data-ttu-id="a5bec-242">Cette propriété est héritée de l' [**\_ erreur CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5bec-242">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a5bec-243">**OtherErrorType**</span><span class="sxs-lookup"><span data-stu-id="a5bec-243">**OtherErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bec-244">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a5bec-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-245">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5bec-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bec-246">Chaîne qui décrit le **ErrorType** lorsque 1, (other), est spécifié en tant que **ErrorType**.</span><span class="sxs-lookup"><span data-stu-id="a5bec-246">A string that describes the **ErrorType** when 1, (Other), is specified as the **ErrorType**.</span></span> <span data-ttu-id="a5bec-247">Cette propriété est héritée de l' [**\_ erreur CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5bec-247">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a5bec-248">**OwningEntity**</span><span class="sxs-lookup"><span data-stu-id="a5bec-248">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bec-249">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a5bec-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-250">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5bec-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bec-251">Chaîne qui identifie de façon unique l’entité qui possède la définition du format du message décrit dans cette instance.</span><span class="sxs-lookup"><span data-stu-id="a5bec-251">A string that uniquely identifies the entity that owns the definition of the format of the message described in this instance.</span></span> <span data-ttu-id="a5bec-252">**OwningEntity** doit inclure un nom de droits d’auteur, de marque déposée ou un nom unique qui est détenu par l’entité métier ou le corps de normes définissant le format.</span><span class="sxs-lookup"><span data-stu-id="a5bec-252">**OwningEntity** must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity or standards body defining the format.</span></span> <span data-ttu-id="a5bec-253">Cette propriété est héritée de l' [**\_ erreur CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5bec-253">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a5bec-254">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="a5bec-254">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bec-255">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a5bec-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-256">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5bec-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bec-257">Valeur énumérée qui décrit la gravité de l’erreur du point de vue du notificateur : 2-Low doit être utilisé pour les problèmes non critiques, tels que les paramètres non valides, l’utilisation incorrecte et les fonctionnalités non prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a5bec-257">An enumerated value that describes the severity of the error from the notifier's point of view: 2 - Low should be used for noncritical issues such as invalid parameters, incorrect usage, unsupported functionality.</span></span> <span data-ttu-id="a5bec-258">3-moyen doit être utilisé pour indiquer qu’une action est nécessaire, mais que la situation n’est pas grave pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="a5bec-258">3 - Medium should be used to indicate action is needed, but the situation is not serious at this time.</span></span> <span data-ttu-id="a5bec-259">4-élevé doit être utilisé pour indiquer que l’action est nécessaire maintenant.</span><span class="sxs-lookup"><span data-stu-id="a5bec-259">4 - High should be used to indicate action is needed now.</span></span> <span data-ttu-id="a5bec-260">5-fatal doit être utilisé pour indiquer une perte de données ou une défaillance du système ou du service irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="a5bec-260">5 - Fatal should be used to indicate a loss of data or unrecoverable system or service failure.</span></span> <span data-ttu-id="a5bec-261">Cette propriété est héritée de l' [**\_ erreur CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5bec-261">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="a5bec-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="a5bec-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-263"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Faible** (2)</span><span class="sxs-lookup"><span data-stu-id="a5bec-263"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-264"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Moyenne** (3)</span><span class="sxs-lookup"><span data-stu-id="a5bec-264"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Medium** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-265"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Élevé** (4)</span><span class="sxs-lookup"><span data-stu-id="a5bec-265"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-266"><span id="Fatal_"></span><span id="fatal_"></span><span id="FATAL_"></span>**Irrécupérable** (5)</span><span class="sxs-lookup"><span data-stu-id="a5bec-266"><span id="Fatal_"></span><span id="fatal_"></span><span id="FATAL_"></span>**Fatal** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a5bec-267">**ProbableCause**</span><span class="sxs-lookup"><span data-stu-id="a5bec-267">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bec-268">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a5bec-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-269">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5bec-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bec-270">Valeur énumérée qui décrit la cause probable de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="a5bec-270">An enumerated value that describes the probable cause of the error.</span></span> <span data-ttu-id="a5bec-271">Cette propriété est héritée de l' [**\_ erreur CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5bec-271">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="a5bec-272"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="a5bec-272"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-273"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="a5bec-273"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-274"><span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>**Erreur de carte/carte** (2)</span><span class="sxs-lookup"><span data-stu-id="a5bec-274"><span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>**Adapter/Card Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-275"><span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>**Défaillance du sous-système d’application** (3)</span><span class="sxs-lookup"><span data-stu-id="a5bec-275"><span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>**Application Subsystem Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-276"><span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>**Bande passante réduite** (4)</span><span class="sxs-lookup"><span data-stu-id="a5bec-276"><span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>**Bandwidth Reduced** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-277"><span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>**Erreur d’établissement** de la connexion (5)</span><span class="sxs-lookup"><span data-stu-id="a5bec-277"><span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>**Connection Establishment Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-278"><span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>**Erreur de protocole de communication** (6)</span><span class="sxs-lookup"><span data-stu-id="a5bec-278"><span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>**Communications Protocol Error** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-279"><span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>**Défaillance du sous-système de communication** (7)</span><span class="sxs-lookup"><span data-stu-id="a5bec-279"><span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>**Communications Subsystem Failure** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-280"><span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>**Erreur de configuration/personnalisation** (8)</span><span class="sxs-lookup"><span data-stu-id="a5bec-280"><span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>**Configuration/Customization Error** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-281"><span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>**Congestion** (9)</span><span class="sxs-lookup"><span data-stu-id="a5bec-281"><span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>**Congestion** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-282"><span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>**Données endommagées** (10)</span><span class="sxs-lookup"><span data-stu-id="a5bec-282"><span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>**Corrupt Data** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-283"><span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>**Limite du nombre de cycles de l’UC dépassée** (11)</span><span class="sxs-lookup"><span data-stu-id="a5bec-283"><span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>**CPU Cycles Limit Exceeded** (11)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-284"><span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>**Erreur de jeu de données/modem** (12)</span><span class="sxs-lookup"><span data-stu-id="a5bec-284"><span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>**Dataset/Modem Error** (12)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-285"><span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>**Signal détérioré** (13)</span><span class="sxs-lookup"><span data-stu-id="a5bec-285"><span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>**Degraded Signal** (13)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-286"><span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>**Erreur d’interface DTE-DCE** (14)</span><span class="sxs-lookup"><span data-stu-id="a5bec-286"><span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>**DTE-DCE Interface Error** (14)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-287"><span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>**Porte de boîtier ouverte** (15)</span><span class="sxs-lookup"><span data-stu-id="a5bec-287"><span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>**Enclosure Door Open** (15)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-288"><span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>**Dysfonctionnements** de l’équipement (16)</span><span class="sxs-lookup"><span data-stu-id="a5bec-288"><span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>**Equipment Malfunction** (16)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-289"><span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>**Vibration excessive** (17)</span><span class="sxs-lookup"><span data-stu-id="a5bec-289"><span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>**Excessive Vibration** (17)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-290"><span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>**Erreur de format de fichier** (18)</span><span class="sxs-lookup"><span data-stu-id="a5bec-290"><span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>**File Format Error** (18)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-291"><span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>**Incendie détecté** (19)</span><span class="sxs-lookup"><span data-stu-id="a5bec-291"><span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>**Fire Detected** (19)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-292"><span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>**Inondation détectée** (20)</span><span class="sxs-lookup"><span data-stu-id="a5bec-292"><span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>**Flood Detected** (20)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-293"><span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>**Erreur de tramage** (21)</span><span class="sxs-lookup"><span data-stu-id="a5bec-293"><span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>**Framing Error** (21)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-294"><span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>**Problème HVAC** (22)</span><span class="sxs-lookup"><span data-stu-id="a5bec-294"><span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>**HVAC Problem** (22)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-295"><span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>**Humidité inacceptable** (23)</span><span class="sxs-lookup"><span data-stu-id="a5bec-295"><span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>**Humidity Unacceptable** (23)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-296"><span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>**Erreur de périphérique d’e/s** (24)</span><span class="sxs-lookup"><span data-stu-id="a5bec-296"><span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>**I/O Device Error** (24)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-297"><span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>**Erreur de l’appareil d’entrée** (25)</span><span class="sxs-lookup"><span data-stu-id="a5bec-297"><span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>**Input Device Error** (25)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-298"><span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>**Erreur LAN** (26)</span><span class="sxs-lookup"><span data-stu-id="a5bec-298"><span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>**LAN Error** (26)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-299"><span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>**Fuite non toxique détectée** (27)</span><span class="sxs-lookup"><span data-stu-id="a5bec-299"><span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>**Non-Toxic Leak Detected** (27)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-300"><span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>**Erreur de transmission du nœud local** (28)</span><span class="sxs-lookup"><span data-stu-id="a5bec-300"><span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>**Local Node Transmission Error** (28)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-301"><span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>**Perte de trame** (29)</span><span class="sxs-lookup"><span data-stu-id="a5bec-301"><span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>**Loss of Frame** (29)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-302"><span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>**Perte de signal** (30)</span><span class="sxs-lookup"><span data-stu-id="a5bec-302"><span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>**Loss of Signal** (30)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-303"><span id="__31____________Material_Supply_Exhausted"></span><span id="__31____________material_supply_exhausted"></span><span id="__31____________MATERIAL_SUPPLY_EXHAUSTED"></span>**//31 alimentations matérielles épuisées** (31)</span><span class="sxs-lookup"><span data-stu-id="a5bec-303"><span id="__31____________Material_Supply_Exhausted"></span><span id="__31____________material_supply_exhausted"></span><span id="__31____________MATERIAL_SUPPLY_EXHAUSTED"></span>**//31 Material Supply Exhausted** (31)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-304"><span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>**Problème de multiplexeur** (32)</span><span class="sxs-lookup"><span data-stu-id="a5bec-304"><span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>**Multiplexer Problem** (32)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-305"><span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>**Mémoire insuffisante** (33)</span><span class="sxs-lookup"><span data-stu-id="a5bec-305"><span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>**Out of Memory** (33)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-306"><span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>**Erreur de périphérique de sortie** (34)</span><span class="sxs-lookup"><span data-stu-id="a5bec-306"><span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>**Output Device Error** (34)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-307"><span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>**Performances détériorées** (35)</span><span class="sxs-lookup"><span data-stu-id="a5bec-307"><span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>**Performance Degraded** (35)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-308"><span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>**Problème d’alimentation** (36)</span><span class="sxs-lookup"><span data-stu-id="a5bec-308"><span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>**Power Problem** (36)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-309"><span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>**Pression inacceptable** (37)</span><span class="sxs-lookup"><span data-stu-id="a5bec-309"><span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>**Pressure Unacceptable** (37)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-310"><span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>**Problème de processeur (erreur d’ordinateur interne)** (38)</span><span class="sxs-lookup"><span data-stu-id="a5bec-310"><span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>**Processor Problem (Internal Machine Error)** (38)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-311"><span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>**Échec** de la pompe (39)</span><span class="sxs-lookup"><span data-stu-id="a5bec-311"><span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>**Pump Failure** (39)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-312"><span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>**Taille de file d’attente dépassée** (40)</span><span class="sxs-lookup"><span data-stu-id="a5bec-312"><span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>**Queue Size Exceeded** (40)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-313"><span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>**Échec de réception** (41)</span><span class="sxs-lookup"><span data-stu-id="a5bec-313"><span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>**Receive Failure** (41)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-314"><span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>**Échec du récepteur** (42)</span><span class="sxs-lookup"><span data-stu-id="a5bec-314"><span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>**Receiver Failure** (42)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-315"><span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>**Erreur de transmission du nœud distant** (43)</span><span class="sxs-lookup"><span data-stu-id="a5bec-315"><span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>**Remote Node Transmission Error** (43)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-316"><span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>**Capacité de la ressource à une capacité proche** (44)</span><span class="sxs-lookup"><span data-stu-id="a5bec-316"><span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>**Resource at or Nearing Capacity** (44)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-317"><span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>**Temps de réponse excessif** (45)</span><span class="sxs-lookup"><span data-stu-id="a5bec-317"><span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>**Response Time Excessive** (45)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-318"><span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>**Taux de retransmission excessif** (46)</span><span class="sxs-lookup"><span data-stu-id="a5bec-318"><span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>**Retransmission Rate Excessive** (46)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-319"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Erreur logicielle** (47)</span><span class="sxs-lookup"><span data-stu-id="a5bec-319"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Software Error** (47)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-320"><span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>**Programme logiciel terminé anormalement** (48)</span><span class="sxs-lookup"><span data-stu-id="a5bec-320"><span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>**Software Program Abnormally Terminated** (48)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-321"><span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>**Erreur du programme logiciel (résultats incorrects)** (49)</span><span class="sxs-lookup"><span data-stu-id="a5bec-321"><span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>**Software Program Error (Incorrect Results)** (49)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-322"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Problème de capacité de stockage** (50)</span><span class="sxs-lookup"><span data-stu-id="a5bec-322"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Storage Capacity Problem** (50)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-323"><span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>**Température inacceptable** (51)</span><span class="sxs-lookup"><span data-stu-id="a5bec-323"><span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>**Temperature Unacceptable** (51)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-324"><span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>**Seuil dépassé** (52)</span><span class="sxs-lookup"><span data-stu-id="a5bec-324"><span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>**Threshold Crossed** (52)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-325"><span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>**Problème de synchronisation** (53)</span><span class="sxs-lookup"><span data-stu-id="a5bec-325"><span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>**Timing Problem** (53)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-326"><span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>**Fuite toxique détectée** (54)</span><span class="sxs-lookup"><span data-stu-id="a5bec-326"><span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>**Toxic Leak Detected** (54)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-327"><span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>**Échec** de la transmission (55)</span><span class="sxs-lookup"><span data-stu-id="a5bec-327"><span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>**Transmit Failure** (55)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-328"><span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>**Échec** de l’émetteur (56)</span><span class="sxs-lookup"><span data-stu-id="a5bec-328"><span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>**Transmitter Failure** (56)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-329"><span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>**Ressource sous-jacente non disponible** (57)</span><span class="sxs-lookup"><span data-stu-id="a5bec-329"><span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>**Underlying Resource Unavailable** (57)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-330"><span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>**Incompatibilité de version** (58)</span><span class="sxs-lookup"><span data-stu-id="a5bec-330"><span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>**Version Mismatch** (58)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-331"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Alerte précédente effacée** (59)</span><span class="sxs-lookup"><span data-stu-id="a5bec-331"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Previous Alert Cleared** (59)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-332"><span id="__60____________Login_Attempts_Failed"></span><span id="__60____________login_attempts_failed"></span><span id="__60____________LOGIN_ATTEMPTS_FAILED"></span>**//60 tentatives de connexion échouées** (60)</span><span class="sxs-lookup"><span data-stu-id="a5bec-332"><span id="__60____________Login_Attempts_Failed"></span><span id="__60____________login_attempts_failed"></span><span id="__60____________LOGIN_ATTEMPTS_FAILED"></span>**//60 Login Attempts Failed** (60)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-333"><span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>**Virus logiciel détecté** (61)</span><span class="sxs-lookup"><span data-stu-id="a5bec-333"><span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>**Software Virus Detected** (61)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-334"><span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>**Violation de la sécurité matérielle** (62)</span><span class="sxs-lookup"><span data-stu-id="a5bec-334"><span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>**Hardware Security Breached** (62)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-335"><span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>**Déni de service détecté** (63)</span><span class="sxs-lookup"><span data-stu-id="a5bec-335"><span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>**Denial of Service Detected** (63)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-336"><span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>Non- **concordance des informations d’identification de sécurité** (64)</span><span class="sxs-lookup"><span data-stu-id="a5bec-336"><span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>**Security Credential Mismatch** (64)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-337"><span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>**Accès non autorisé** (65)</span><span class="sxs-lookup"><span data-stu-id="a5bec-337"><span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>**Unauthorized Access** (65)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-338"><span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>**Alarme reçue** (66)</span><span class="sxs-lookup"><span data-stu-id="a5bec-338"><span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>**Alarm Received** (66)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-339"><span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>**Perte de pointeur** (67)</span><span class="sxs-lookup"><span data-stu-id="a5bec-339"><span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>**Loss of Pointer** (67)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-340"><span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>**Incompatibilité de charge utile** (68)</span><span class="sxs-lookup"><span data-stu-id="a5bec-340"><span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>**Payload Mismatch** (68)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-341"><span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>**Erreur de transmission** (69)</span><span class="sxs-lookup"><span data-stu-id="a5bec-341"><span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>**Transmission Error** (69)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-342"><span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>**Taux d’erreur excessif** (70)</span><span class="sxs-lookup"><span data-stu-id="a5bec-342"><span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>**Excessive Error Rate** (70)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-343"><span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>**Problème de suivi** (71)</span><span class="sxs-lookup"><span data-stu-id="a5bec-343"><span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>**Trace Problem** (71)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-344"><span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>**Élément non disponible** (72)</span><span class="sxs-lookup"><span data-stu-id="a5bec-344"><span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>**Element Unavailable** (72)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-345"><span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>**Élément manquant** (73)</span><span class="sxs-lookup"><span data-stu-id="a5bec-345"><span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>**Element Missing** (73)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-346"><span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>**Perte de plusieurs trames** (74)</span><span class="sxs-lookup"><span data-stu-id="a5bec-346"><span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>**Loss of Multi Frame** (74)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-347"><span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>**Échec du canal de diffusion** (75)</span><span class="sxs-lookup"><span data-stu-id="a5bec-347"><span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>**Broadcast Channel Failure** (75)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-348"><span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>**Message reçu non valide** (76)</span><span class="sxs-lookup"><span data-stu-id="a5bec-348"><span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>**Invalid Message Received** (76)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-349"><span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>**Échec de routage** (77)</span><span class="sxs-lookup"><span data-stu-id="a5bec-349"><span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>**Routing Failure** (77)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-350"><span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>**Échec du fond de panier** (78)</span><span class="sxs-lookup"><span data-stu-id="a5bec-350"><span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>**Backplane Failure** (78)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-351"><span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>**Duplication des identificateurs** (79)</span><span class="sxs-lookup"><span data-stu-id="a5bec-351"><span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>**Identifier Duplication** (79)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-352"><span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>**Échec du chemin d’accès de protection** (80)</span><span class="sxs-lookup"><span data-stu-id="a5bec-352"><span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>**Protection Path Failure** (80)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-353"><span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>**Perte ou incompatibilité** de la synchronisation (81)</span><span class="sxs-lookup"><span data-stu-id="a5bec-353"><span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>**Sync Loss or Mismatch** (81)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-354"><span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>**Problème de terminal** (82)</span><span class="sxs-lookup"><span data-stu-id="a5bec-354"><span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>**Terminal Problem** (82)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-355"><span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>**Échec de l’horloge en temps réel** (83)</span><span class="sxs-lookup"><span data-stu-id="a5bec-355"><span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>**Real Time Clock Failure** (83)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-356"><span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>**Défaillance** de l’antenne (84)</span><span class="sxs-lookup"><span data-stu-id="a5bec-356"><span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>**Antenna Failure** (84)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-357"><span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>**Échec de chargement** de la batterie (85)</span><span class="sxs-lookup"><span data-stu-id="a5bec-357"><span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>**Battery Charging Failure** (85)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-358"><span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>**Défaillance du disque** (86)</span><span class="sxs-lookup"><span data-stu-id="a5bec-358"><span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>**Disk Failure** (86)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-359"><span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>**Échec du saut de fréquence** (87)</span><span class="sxs-lookup"><span data-stu-id="a5bec-359"><span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>**Frequency Hopping Failure** (87)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-360"><span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>**Perte de redondance** (88)</span><span class="sxs-lookup"><span data-stu-id="a5bec-360"><span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>**Loss of Redundancy** (88)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-361"><span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>**Échec** de l’alimentation (89)</span><span class="sxs-lookup"><span data-stu-id="a5bec-361"><span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>**Power Supply Failure** (89)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-362"><span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>**Problème de qualité du signal** (90)</span><span class="sxs-lookup"><span data-stu-id="a5bec-362"><span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>**Signal Quality Problem** (90)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-363"><span id="__91____________Battery_Discharging"></span><span id="__91____________battery_discharging"></span><span id="__91____________BATTERY_DISCHARGING"></span>**//91 déchargement** de la batterie (91)</span><span class="sxs-lookup"><span data-stu-id="a5bec-363"><span id="__91____________Battery_Discharging"></span><span id="__91____________battery_discharging"></span><span id="__91____________BATTERY_DISCHARGING"></span>**//91 Battery Discharging** (91)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-364"><span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>**Défaillance** de la batterie (92)</span><span class="sxs-lookup"><span data-stu-id="a5bec-364"><span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>**Battery Failure** (92)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-365"><span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>**Problème commercial** de l’électricité (93)</span><span class="sxs-lookup"><span data-stu-id="a5bec-365"><span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>**Commercial Power Problem** (93)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-366"><span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>**Défaillance du ventilateur** (94)</span><span class="sxs-lookup"><span data-stu-id="a5bec-366"><span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>**Fan Failure** (94)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-367"><span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>**Défaillance du moteur** (95)</span><span class="sxs-lookup"><span data-stu-id="a5bec-367"><span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>**Engine Failure** (95)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-368"><span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>**Défaillance du capteur** (96)</span><span class="sxs-lookup"><span data-stu-id="a5bec-368"><span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>**Sensor Failure** (96)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-369"><span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>**Échec de fusible** (97)</span><span class="sxs-lookup"><span data-stu-id="a5bec-369"><span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>**Fuse Failure** (97)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-370"><span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>**Échec du générateur** (98)</span><span class="sxs-lookup"><span data-stu-id="a5bec-370"><span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>**Generator Failure** (98)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-371"><span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>**Batterie faible** (99)</span><span class="sxs-lookup"><span data-stu-id="a5bec-371"><span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>**Low Battery** (99)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-372"><span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>**Carburant faible** (100)</span><span class="sxs-lookup"><span data-stu-id="a5bec-372"><span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>**Low Fuel** (100)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-373"><span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>**Faible eau** (101)</span><span class="sxs-lookup"><span data-stu-id="a5bec-373"><span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>**Low Water** (101)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-374"><span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>**Gaz explosif** (102)</span><span class="sxs-lookup"><span data-stu-id="a5bec-374"><span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>**Explosive Gas** (102)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-375"><span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>**Vents élevés** (103)</span><span class="sxs-lookup"><span data-stu-id="a5bec-375"><span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>**High Winds** (103)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-376"><span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>**Accumulations de glace** (104)</span><span class="sxs-lookup"><span data-stu-id="a5bec-376"><span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>**Ice Buildup** (104)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-377"><span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>**Fumée** (105)</span><span class="sxs-lookup"><span data-stu-id="a5bec-377"><span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>**Smoke** (105)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-378"><span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>**Incompatibilité de mémoire** (106)</span><span class="sxs-lookup"><span data-stu-id="a5bec-378"><span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>**Memory Mismatch** (106)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-379"><span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>**Cycles de processeur insuffisants** (107)</span><span class="sxs-lookup"><span data-stu-id="a5bec-379"><span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>**Out of CPU Cycles** (107)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-380"><span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>**Problème de l’environnement logiciel** (108)</span><span class="sxs-lookup"><span data-stu-id="a5bec-380"><span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>**Software Environment Problem** (108)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-381"><span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>**Échec du téléchargement de logiciels** (109)</span><span class="sxs-lookup"><span data-stu-id="a5bec-381"><span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>**Software Download Failure** (109)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-382"><span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>**Élément réinitialisé** (110)</span><span class="sxs-lookup"><span data-stu-id="a5bec-382"><span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>**Element Reinitialized** (110)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-383"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>**Délai d’expiration** (111)</span><span class="sxs-lookup"><span data-stu-id="a5bec-383"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>**Timeout** (111)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-384"><span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>**Problèmes de journalisation** (112)</span><span class="sxs-lookup"><span data-stu-id="a5bec-384"><span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>**Logging Problems** (112)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-385"><span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>**Fuite détectée** (113)</span><span class="sxs-lookup"><span data-stu-id="a5bec-385"><span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>**Leak Detected** (113)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-386"><span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>**Échec du mécanisme de protection** (114)</span><span class="sxs-lookup"><span data-stu-id="a5bec-386"><span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>**Protection Mechanism Failure** (114)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-387"><span id="__115____________Protecting_Resource_Failure"></span><span id="__115____________protecting_resource_failure"></span><span id="__115____________PROTECTING_RESOURCE_FAILURE"></span>**//115 protection** de la défaillance de ressource (115)</span><span class="sxs-lookup"><span data-stu-id="a5bec-387"><span id="__115____________Protecting_Resource_Failure"></span><span id="__115____________protecting_resource_failure"></span><span id="__115____________PROTECTING_RESOURCE_FAILURE"></span>**//115 Protecting Resource Failure** (115)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-388"><span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>**Incohérence de base de données** (116)</span><span class="sxs-lookup"><span data-stu-id="a5bec-388"><span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>**Database Inconsistency** (116)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-389"><span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>**Échec de l’authentification** (117)</span><span class="sxs-lookup"><span data-stu-id="a5bec-389"><span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>**Authentication Failure** (117)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-390"><span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>**Violation de la confidentialité** (118)</span><span class="sxs-lookup"><span data-stu-id="a5bec-390"><span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>**Breach of Confidentiality** (118)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-391"><span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>**Falsification de câble** (119)</span><span class="sxs-lookup"><span data-stu-id="a5bec-391"><span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>**Cable Tamper** (119)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-392"><span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>**Informations retardées** (120)</span><span class="sxs-lookup"><span data-stu-id="a5bec-392"><span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>**Delayed Information** (120)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-393"><span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>**Informations dupliquées** (121)</span><span class="sxs-lookup"><span data-stu-id="a5bec-393"><span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>**Duplicate Information** (121)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-394"><span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>**Informations manquantes** (122)</span><span class="sxs-lookup"><span data-stu-id="a5bec-394"><span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>**Information Missing** (122)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-395"><span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>**Modification des informations** (123)</span><span class="sxs-lookup"><span data-stu-id="a5bec-395"><span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>**Information Modification** (123)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-396"><span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>**Informations hors séquence** (124)</span><span class="sxs-lookup"><span data-stu-id="a5bec-396"><span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>**Information Out of Sequence** (124)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-397"><span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>**Clé expirée** (125)</span><span class="sxs-lookup"><span data-stu-id="a5bec-397"><span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>**Key Expired** (125)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-398"><span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>**Échec de la non-répudiation** (126)</span><span class="sxs-lookup"><span data-stu-id="a5bec-398"><span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>**Non-Repudiation Failure** (126)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-399"><span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>**Activité en dehors des heures** (127)</span><span class="sxs-lookup"><span data-stu-id="a5bec-399"><span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>**Out of Hours Activity** (127)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-400"><span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>**Hors service** (128)</span><span class="sxs-lookup"><span data-stu-id="a5bec-400"><span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>**Out of Service** (128)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-401"><span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>**Erreur de procédure** (129)</span><span class="sxs-lookup"><span data-stu-id="a5bec-401"><span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>**Procedural Error** (129)</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-402"><span id="Unexpected_Information_"></span><span id="unexpected_information_"></span><span id="UNEXPECTED_INFORMATION_"></span>**Informations inattendues** (130)</span><span class="sxs-lookup"><span data-stu-id="a5bec-402"><span id="Unexpected_Information_"></span><span id="unexpected_information_"></span><span id="UNEXPECTED_INFORMATION_"></span>**Unexpected Information** (130 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a5bec-403">**ProbableCauseDescription**</span><span class="sxs-lookup"><span data-stu-id="a5bec-403">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bec-404">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a5bec-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-405">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5bec-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bec-406">Chaîne qui décrit la cause probable de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="a5bec-406">A string that describes the probable cause of the error.</span></span> <span data-ttu-id="a5bec-407">Cette propriété est héritée de l' [**\_ erreur CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5bec-407">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a5bec-408">**RecommendedActions**</span><span class="sxs-lookup"><span data-stu-id="a5bec-408">**RecommendedActions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bec-409">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="a5bec-409">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a5bec-410">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5bec-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bec-411">Chaîne qui décrit les actions recommandées à entreprendre pour résoudre l’erreur.</span><span class="sxs-lookup"><span data-stu-id="a5bec-411">A string that describes recommended actions to take to resolve the error.</span></span> <span data-ttu-id="a5bec-412">Cette propriété est héritée de l' [**\_ erreur CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5bec-412">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5bec-413">Notes</span><span class="sxs-lookup"><span data-stu-id="a5bec-413">Remarks</span></span>

<span data-ttu-id="a5bec-414">L’accès à la classe d' **\_ erreur MSVM** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="a5bec-414">Access to the **Msvm\_Error** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a5bec-415">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a5bec-415">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5bec-416">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5bec-416">Requirements</span></span>



| <span data-ttu-id="a5bec-417">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5bec-417">Requirement</span></span> | <span data-ttu-id="a5bec-418">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5bec-418">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5bec-419">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5bec-419">Minimum supported client</span></span><br/> | <span data-ttu-id="a5bec-420">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5bec-420">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a5bec-421">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5bec-421">Minimum supported server</span></span><br/> | <span data-ttu-id="a5bec-422">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5bec-422">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a5bec-423">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a5bec-423">Namespace</span></span><br/>                | <span data-ttu-id="a5bec-424">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a5bec-424">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a5bec-425">MOF</span><span class="sxs-lookup"><span data-stu-id="a5bec-425">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5bec-426"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-426"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5bec-427">DLL</span><span class="sxs-lookup"><span data-stu-id="a5bec-427">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5bec-428"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a5bec-428"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a5bec-429">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5bec-429">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5bec-430">**\_Erreur CIM**</span><span class="sxs-lookup"><span data-stu-id="a5bec-430">**CIM\_Error**</span></span>](cim-error.md)
</dt> <dt>

<span data-ttu-id="a5bec-431">[**\_Erreur CIM**](/previous-versions//cc150671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a5bec-431">[**CIM\_Error**](/previous-versions//cc150671(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a5bec-432">Classes de gestion du système virtuel</span><span class="sxs-lookup"><span data-stu-id="a5bec-432">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

