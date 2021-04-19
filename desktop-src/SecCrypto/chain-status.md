---
description: Récupère l’état de validité de la chaîne ou d’un certificat spécifique dans la chaîne.
title: 'IChain2 :: Status, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Status
- IChain.Status
- Chain.Status
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 23673289e2ff39d4180a4be8dc0be61f4a5cffc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537752"
---
# <a name="ichain2status-property"></a><span data-ttu-id="a77a7-103">IChain2 :: Status, propriété</span><span class="sxs-lookup"><span data-stu-id="a77a7-103">IChain2::Status property</span></span>

<span data-ttu-id="a77a7-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a77a7-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a77a7-105">Utilisez plutôt la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a77a7-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a77a7-106">La propriété **Status** récupère l’état de validité de la chaîne ou un certificat spécifique dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="a77a7-106">The **Status** property retrieves the validity status of the chain or a specific certificate in the chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="a77a7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a77a7-107">Syntax</span></span>


```VB
Chain.Status( _
  ByVal Index _
) As Long
```



## <a name="property-value"></a><span data-ttu-id="a77a7-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a77a7-108">Property value</span></span>

<span data-ttu-id="a77a7-109">Valeur de **type long** qui représente l’indicateur d’état de validité de la chaîne ou du certificat spécifié.</span><span class="sxs-lookup"><span data-stu-id="a77a7-109">A **LONG** value that represents the validity status indicator of the chain or the specified certificate.</span></span> <span data-ttu-id="a77a7-110">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="a77a7-110">The following table shows the possible values.</span></span> <span data-ttu-id="a77a7-111">Cette propriété contient zéro si la chaîne ou le certificat spécifié est valide.</span><span class="sxs-lookup"><span data-stu-id="a77a7-111">This property will contain zero if the chain or specified certificate is valid.</span></span> <span data-ttu-id="a77a7-112">Sinon, cette propriété contiendra une combinaison d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a77a7-112">Otherwise, this property will contain a combination of one or more of the following values.</span></span>

<dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>

<span data-ttu-id="a77a7-113"><span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM \_ L’approbation \_ n’est \_ pas \_ \_ valide** (&H00000001)</span><span class="sxs-lookup"><span data-stu-id="a77a7-113"><span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM\_TRUST\_IS\_NOT\_TIME\_VALID** (&H00000001)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-114">Ce certificat ou l’un des certificats de la chaîne de certificats n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a77a7-114">This certificate or one of the certificates in the certificate chain is not time valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>

<span data-ttu-id="a77a7-115"><span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM \_ L’approbation \_ n’est \_ pas \_ \_ imbriquée** dans le temps (&H00000002)</span><span class="sxs-lookup"><span data-stu-id="a77a7-115"><span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM\_TRUST\_IS\_NOT\_TIME\_NESTED** (&H00000002)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-116">Les certificats de la chaîne ne sont pas correctement imbriqués dans le temps.</span><span class="sxs-lookup"><span data-stu-id="a77a7-116">Certificates in the chain are not properly time nested.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>

<span data-ttu-id="a77a7-117"><span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM \_ L’approbation \_ est \_ révoquée** (&H00000004)</span><span class="sxs-lookup"><span data-stu-id="a77a7-117"><span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM\_TRUST\_IS\_REVOKED** (&H00000004)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-118">L’approbation de ce certificat ou l’un des certificats de la chaîne de certificats a été révoqué.</span><span class="sxs-lookup"><span data-stu-id="a77a7-118">Trust for this certificate or one of the certificates in the certificate chain has been revoked.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>

<span data-ttu-id="a77a7-119"><span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM \_ La signature de l’approbation \_ n’est \_ pas \_ \_ valide** (&H00000008)</span><span class="sxs-lookup"><span data-stu-id="a77a7-119"><span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM\_TRUST\_IS\_NOT\_SIGNATURE\_VALID** (&H00000008)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-120">Le certificat ou l’un des certificats de la chaîne de certificats n’a pas de signature valide.</span><span class="sxs-lookup"><span data-stu-id="a77a7-120">The certificate or one of the certificates in the certificate chain does not have a valid signature.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>

<span data-ttu-id="a77a7-121"><span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM \_ \_L’approbation n’est \_ pas \_ valide \_ pour \_ l’utilisation** (&H00000010)</span><span class="sxs-lookup"><span data-stu-id="a77a7-121"><span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM\_TRUST\_IS\_NOT\_VALID\_FOR\_USAGE** (&H00000010)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-122">Le certificat ou la chaîne de certificats n’est pas valide pour son utilisation proposée.</span><span class="sxs-lookup"><span data-stu-id="a77a7-122">The certificate or certificate chain is not valid for its proposed usage.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>

<span data-ttu-id="a77a7-123"><span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM \_ L’approbation \_ est une \_ \_ racine non approuvée** (&H00000020)</span><span class="sxs-lookup"><span data-stu-id="a77a7-123"><span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM\_TRUST\_IS\_UNTRUSTED\_ROOT** (&H00000020)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-124">Le certificat ou la chaîne de certificats est basé sur une racine non approuvée.</span><span class="sxs-lookup"><span data-stu-id="a77a7-124">The certificate or certificate chain is based on an untrusted root.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>

<span data-ttu-id="a77a7-125"><span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM \_ \_État de révocation de confiance \_ \_ inconnu** (&H00000040)</span><span class="sxs-lookup"><span data-stu-id="a77a7-125"><span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM\_TRUST\_REVOCATION\_STATUS\_UNKNOWN** (&H00000040)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-126">L’état de révocation du certificat ou de l’un des certificats de la chaîne de certificats est inconnu.</span><span class="sxs-lookup"><span data-stu-id="a77a7-126">The revocation status of the certificate or one of the certificates in the certificate chain is unknown.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>

<span data-ttu-id="a77a7-127"><span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM \_ L’approbation \_ est \_ cyclique** (&H00000080)</span><span class="sxs-lookup"><span data-stu-id="a77a7-127"><span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM\_TRUST\_IS\_CYCLIC** (&H00000080)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-128">L’un des certificats de la chaîne a été émis par une [*autorité de certification*](../secgloss/c-gly.md) que le certificat d’origine avait certifié.</span><span class="sxs-lookup"><span data-stu-id="a77a7-128">One of the certificates in the chain was issued by a [*certification authority*](../secgloss/c-gly.md) that the original certificate had certified.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>

<span data-ttu-id="a77a7-129"><span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM \_ APPROUVER \_ une \_ extension non valide** (&H00000100)</span><span class="sxs-lookup"><span data-stu-id="a77a7-129"><span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM\_TRUST\_INVALID\_EXTENSION** (&H00000100)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-130">L’un des certificats a une extension qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a77a7-130">One of the certificates has an extension that is not valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>

<span data-ttu-id="a77a7-131"><span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM \_ APPROUVER \_ les \_ \_ contraintes de stratégie non valides** (&H00000200)</span><span class="sxs-lookup"><span data-stu-id="a77a7-131"><span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM\_TRUST\_INVALID\_POLICY\_CONSTRAINTS** (&H00000200)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-132">Le certificat ou l’un des certificats de la chaîne de certificats possède une extension de contraintes de stratégie et l’un des certificats émis a une extension de mappage de stratégie non autorisée ou n’a pas d’extension de stratégies d’émission obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a77a7-132">The certificate or one of the certificates in the certificate chain has a policy constraints extension, and one of the issued certificates has a disallowed policy mapping extension or does not have a required issuance policies extension.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>

<span data-ttu-id="a77a7-133"><span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM \_ APPROUVER \_ les \_ \_ contraintes de base non valides** (&H00000400)</span><span class="sxs-lookup"><span data-stu-id="a77a7-133"><span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM\_TRUST\_INVALID\_BASIC\_CONSTRAINTS** (&H00000400)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-134">Le certificat ou l’un des certificats de la chaîne de certificats possède une extension de contraintes de base, et soit le certificat ne peut pas être utilisé pour émettre d’autres certificats, soit la longueur du chemin d’accès de la chaîne a été dépassée.</span><span class="sxs-lookup"><span data-stu-id="a77a7-134">The certificate or one of the certificates in the certificate chain has a basic constraints extension, and either the certificate cannot be used to issue other certificates, or the chain path length has been exceeded.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>

<span data-ttu-id="a77a7-135"><span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM \_ APPROUVER \_ les \_ \_ contraintes de nom non valides** (&H00000800)</span><span class="sxs-lookup"><span data-stu-id="a77a7-135"><span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM\_TRUST\_INVALID\_NAME\_CONSTRAINTS** (&H00000800)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-136">Le certificat ou l’un des certificats de la chaîne de certificats possède une extension de contraintes de nom qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a77a7-136">The certificate or one of the certificates in the certificate chain has a name constraints extension that is not valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>

<span data-ttu-id="a77a7-137"><span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM \_ L’approbation n' \_ a \_ pas \_ pris en charge la \_ \_ contrainte de nom** (&H00001000)</span><span class="sxs-lookup"><span data-stu-id="a77a7-137"><span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_NOT\_SUPPORTED\_NAME\_CONSTRAINT** (&H00001000)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-138">Le certificat ou l’un des certificats de la chaîne de certificats possède une extension de contraintes de nom qui contient des champs non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a77a7-138">The certificate or one of the certificates in the certificate chain has a name constraints extension that contains unsupported fields.</span></span> <span data-ttu-id="a77a7-139">Les champs minimum et maximum ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a77a7-139">The minimum and maximum fields are not supported.</span></span> <span data-ttu-id="a77a7-140">La valeur minimale doit toujours être égale à zéro et la valeur maximum doit toujours être absente.</span><span class="sxs-lookup"><span data-stu-id="a77a7-140">Thus minimum must always be zero and maximum must always be absent.</span></span> <span data-ttu-id="a77a7-141">Seul l’UPN est pris en charge pour un autre nom.</span><span class="sxs-lookup"><span data-stu-id="a77a7-141">Only UPN is supported for an Other Name.</span></span> <span data-ttu-id="a77a7-142">Les autres choix de noms suivants ne sont pas pris en charge :</span><span class="sxs-lookup"><span data-stu-id="a77a7-142">The following alternative name choices are not supported:</span></span>

-   <span data-ttu-id="a77a7-143">Adresse x400</span><span class="sxs-lookup"><span data-stu-id="a77a7-143">X400 Address</span></span>
-   <span data-ttu-id="a77a7-144">Nom du tiers EDI</span><span class="sxs-lookup"><span data-stu-id="a77a7-144">EDI Party Name</span></span>
-   <span data-ttu-id="a77a7-145">ID inscrit</span><span class="sxs-lookup"><span data-stu-id="a77a7-145">Registered Id</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>

<span data-ttu-id="a77a7-146"><span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM \_ L’approbation n' \_ a \_ pas \_ défini de \_ \_ contrainte de nom** (&H00002000)</span><span class="sxs-lookup"><span data-stu-id="a77a7-146"><span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_NOT\_DEFINED\_NAME\_CONSTRAINT** (&H00002000)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-147">Le certificat ou l’un des certificats de la chaîne de certificats possède une extension de contraintes de nom, et une contrainte de nom est manquante pour l’un des choix de noms dans le certificat de fin.</span><span class="sxs-lookup"><span data-stu-id="a77a7-147">The certificate or one of the certificates in the certificate chain has a name constraints extension, and a name constraint is missing for one of the name choices in the end certificate.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>

<span data-ttu-id="a77a7-148"><span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM \_ L’approbation n' \_ a \_ pas \_ autorisé la \_ \_ contrainte de nom** (&H00004000)</span><span class="sxs-lookup"><span data-stu-id="a77a7-148"><span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_NOT\_PERMITTED\_NAME\_CONSTRAINT** (&H00004000)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-149">Le certificat ou l’un des certificats de la chaîne de certificats possède une extension de contraintes de nom, et il n’existe pas de contrainte de nom autorisée pour l’un des choix de noms dans le certificat de fin.</span><span class="sxs-lookup"><span data-stu-id="a77a7-149">The certificate or one of the certificates in the certificate chain has a name constraints extension, and there is not a permitted name constraint for one of the name choices in the end certificate.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>

<span data-ttu-id="a77a7-150"><span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM \_ L’approbation \_ a une \_ \_ \_ contrainte de nom exclue** (&H00008000)</span><span class="sxs-lookup"><span data-stu-id="a77a7-150"><span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_EXCLUDED\_NAME\_CONSTRAINT** (&H00008000)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-151">Le certificat ou l’un des certificats de la chaîne de certificats possède une extension de contraintes de nom, et l’un des choix de noms dans le certificat de fin est explicitement exclu.</span><span class="sxs-lookup"><span data-stu-id="a77a7-151">The certificate or one of the certificates in the certificate chain has a name constraints extension, and one of the name choices in the end certificate is explicitly excluded.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>

<span data-ttu-id="a77a7-152"><span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM \_ L’approbation \_ est une \_ \_ révocation hors connexion** (&H01000000)</span><span class="sxs-lookup"><span data-stu-id="a77a7-152"><span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM\_TRUST\_IS\_OFFLINE\_REVOCATION** (&H01000000)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-153">L’état de révocation du certificat ou l’un des certificats de la chaîne de certificats est hors connexion ou obsolète.</span><span class="sxs-lookup"><span data-stu-id="a77a7-153">The revocation status of the certificate or one of the certificates in the certificate chain is either offline or stale.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>

<span data-ttu-id="a77a7-154"><span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM \_ APPROUVER \_ aucune \_ \_ \_ stratégie de chaîne d’émission** (&H02000000)</span><span class="sxs-lookup"><span data-stu-id="a77a7-154"><span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM\_TRUST\_NO\_ISSUANCE\_CHAIN\_POLICY** (&H02000000)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-155">Le certificat de fin n’a aucune stratégie d’émission résultante et l’un des certificats d’autorité de certification émettrice a une extension de contraintes de stratégie qui le requiert.</span><span class="sxs-lookup"><span data-stu-id="a77a7-155">The end certificate does not have any resultant issuance policies, and one of the issuing CA certificates has a policy constraints extension requiring it.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>

<span data-ttu-id="a77a7-156"><span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM \_ L’approbation \_ est une \_ \_ chaîne partielle** (&H00010000)</span><span class="sxs-lookup"><span data-stu-id="a77a7-156"><span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM\_TRUST\_IS\_PARTIAL\_CHAIN** (&H00010000)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-157">La chaîne de certificats n’est pas en concurrence.</span><span class="sxs-lookup"><span data-stu-id="a77a7-157">The certificate chain is not compete.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>

<span data-ttu-id="a77a7-158"><span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM \_ La \_ liste CTL de confiance \_ n’est \_ pas \_ \_ valide** dans le temps (&H00020000)</span><span class="sxs-lookup"><span data-stu-id="a77a7-158"><span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM\_TRUST\_CTL\_IS\_NOT\_TIME\_VALID** (&H00020000)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-159">Une liste de certificats de confiance utilisée pour créer cette chaîne n’était pas valide.</span><span class="sxs-lookup"><span data-stu-id="a77a7-159">A CTL used to create this chain was not time valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>

<span data-ttu-id="a77a7-160"><span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM \_ La \_ liste CTL de confiance \_ n’est \_ pas une \_ signature \_ valide** (&H00040000)</span><span class="sxs-lookup"><span data-stu-id="a77a7-160"><span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM\_TRUST\_CTL\_IS\_NOT\_SIGNATURE\_VALID** (&H00040000)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-161">Une liste de certificats de confiance utilisée pour créer cette chaîne n’a pas de signature valide.</span><span class="sxs-lookup"><span data-stu-id="a77a7-161">A CTL used to create this chain did not have a valid signature.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>

<span data-ttu-id="a77a7-162"><span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM \_ La \_ liste CTL \_ de confiance n’est \_ pas \_ valide \_ pour \_ l’utilisation** (&H00080000)</span><span class="sxs-lookup"><span data-stu-id="a77a7-162"><span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM\_TRUST\_CTL\_IS\_NOT\_VALID\_FOR\_USAGE** (&H00080000)</span></span>


</dt> <dd>

<span data-ttu-id="a77a7-163">Une liste de certificats de confiance utilisée pour créer cette chaîne n’est pas valide pour cette utilisation.</span><span class="sxs-lookup"><span data-stu-id="a77a7-163">A CTL used to create this chain is not valid for this usage.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a77a7-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a77a7-164">Requirements</span></span>



| <span data-ttu-id="a77a7-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a77a7-165">Requirement</span></span> | <span data-ttu-id="a77a7-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="a77a7-166">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a77a7-167">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a77a7-167">End of client support</span></span><br/> | <span data-ttu-id="a77a7-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a77a7-168">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a77a7-169">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="a77a7-169">End of server support</span></span><br/> | <span data-ttu-id="a77a7-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a77a7-170">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a77a7-171">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a77a7-171">Redistributable</span></span><br/>       | <span data-ttu-id="a77a7-172">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="a77a7-172">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a77a7-173">DLL</span><span class="sxs-lookup"><span data-stu-id="a77a7-173">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a77a7-174"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a77a7-174"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
