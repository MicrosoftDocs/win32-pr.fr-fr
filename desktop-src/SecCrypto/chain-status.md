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
# <a name="ichain2status-property"></a>IChain2 :: Status, propriété

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **Status** récupère l’état de validité de la chaîne ou un certificat spécifique dans la chaîne.

## <a name="syntax"></a>Syntaxe


```VB
Chain.Status( _
  ByVal Index _
) As Long
```



## <a name="property-value"></a>Valeur de la propriété

Valeur de **type long** qui représente l’indicateur d’état de validité de la chaîne ou du certificat spécifié. Le tableau suivant répertorie les valeurs possibles. Cette propriété contient zéro si la chaîne ou le certificat spécifié est valide. Sinon, cette propriété contiendra une combinaison d’une ou plusieurs des valeurs suivantes.

<dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM \_ L’approbation \_ n’est \_ pas \_ \_ valide** (&H00000001)


</dt> <dd>

Ce certificat ou l’un des certificats de la chaîne de certificats n’est pas valide.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM \_ L’approbation \_ n’est \_ pas \_ \_ imbriquée** dans le temps (&H00000002)


</dt> <dd>

Les certificats de la chaîne ne sont pas correctement imbriqués dans le temps.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM \_ L’approbation \_ est \_ révoquée** (&H00000004)


</dt> <dd>

L’approbation de ce certificat ou l’un des certificats de la chaîne de certificats a été révoqué.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM \_ La signature de l’approbation \_ n’est \_ pas \_ \_ valide** (&H00000008)


</dt> <dd>

Le certificat ou l’un des certificats de la chaîne de certificats n’a pas de signature valide.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM \_ \_L’approbation n’est \_ pas \_ valide \_ pour \_ l’utilisation** (&H00000010)


</dt> <dd>

Le certificat ou la chaîne de certificats n’est pas valide pour son utilisation proposée.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM \_ L’approbation \_ est une \_ \_ racine non approuvée** (&H00000020)


</dt> <dd>

Le certificat ou la chaîne de certificats est basé sur une racine non approuvée.

</dd> <dt>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM \_ \_État de révocation de confiance \_ \_ inconnu** (&H00000040)


</dt> <dd>

L’état de révocation du certificat ou de l’un des certificats de la chaîne de certificats est inconnu.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM \_ L’approbation \_ est \_ cyclique** (&H00000080)


</dt> <dd>

L’un des certificats de la chaîne a été émis par une [*autorité de certification*](../secgloss/c-gly.md) que le certificat d’origine avait certifié.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM \_ APPROUVER \_ une \_ extension non valide** (&H00000100)


</dt> <dd>

L’un des certificats a une extension qui n’est pas valide.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM \_ APPROUVER \_ les \_ \_ contraintes de stratégie non valides** (&H00000200)


</dt> <dd>

Le certificat ou l’un des certificats de la chaîne de certificats possède une extension de contraintes de stratégie et l’un des certificats émis a une extension de mappage de stratégie non autorisée ou n’a pas d’extension de stratégies d’émission obligatoire.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM \_ APPROUVER \_ les \_ \_ contraintes de base non valides** (&H00000400)


</dt> <dd>

Le certificat ou l’un des certificats de la chaîne de certificats possède une extension de contraintes de base, et soit le certificat ne peut pas être utilisé pour émettre d’autres certificats, soit la longueur du chemin d’accès de la chaîne a été dépassée.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM \_ APPROUVER \_ les \_ \_ contraintes de nom non valides** (&H00000800)


</dt> <dd>

Le certificat ou l’un des certificats de la chaîne de certificats possède une extension de contraintes de nom qui n’est pas valide.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM \_ L’approbation n' \_ a \_ pas \_ pris en charge la \_ \_ contrainte de nom** (&H00001000)


</dt> <dd>

Le certificat ou l’un des certificats de la chaîne de certificats possède une extension de contraintes de nom qui contient des champs non pris en charge. Les champs minimum et maximum ne sont pas pris en charge. La valeur minimale doit toujours être égale à zéro et la valeur maximum doit toujours être absente. Seul l’UPN est pris en charge pour un autre nom. Les autres choix de noms suivants ne sont pas pris en charge :

-   Adresse x400
-   Nom du tiers EDI
-   ID inscrit

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM \_ L’approbation n' \_ a \_ pas \_ défini de \_ \_ contrainte de nom** (&H00002000)


</dt> <dd>

Le certificat ou l’un des certificats de la chaîne de certificats possède une extension de contraintes de nom, et une contrainte de nom est manquante pour l’un des choix de noms dans le certificat de fin.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM \_ L’approbation n' \_ a \_ pas \_ autorisé la \_ \_ contrainte de nom** (&H00004000)


</dt> <dd>

Le certificat ou l’un des certificats de la chaîne de certificats possède une extension de contraintes de nom, et il n’existe pas de contrainte de nom autorisée pour l’un des choix de noms dans le certificat de fin.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM \_ L’approbation \_ a une \_ \_ \_ contrainte de nom exclue** (&H00008000)


</dt> <dd>

Le certificat ou l’un des certificats de la chaîne de certificats possède une extension de contraintes de nom, et l’un des choix de noms dans le certificat de fin est explicitement exclu.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM \_ L’approbation \_ est une \_ \_ révocation hors connexion** (&H01000000)


</dt> <dd>

L’état de révocation du certificat ou l’un des certificats de la chaîne de certificats est hors connexion ou obsolète.

</dd> <dt>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM \_ APPROUVER \_ aucune \_ \_ \_ stratégie de chaîne d’émission** (&H02000000)


</dt> <dd>

Le certificat de fin n’a aucune stratégie d’émission résultante et l’un des certificats d’autorité de certification émettrice a une extension de contraintes de stratégie qui le requiert.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM \_ L’approbation \_ est une \_ \_ chaîne partielle** (&H00010000)


</dt> <dd>

La chaîne de certificats n’est pas en concurrence.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM \_ La \_ liste CTL de confiance \_ n’est \_ pas \_ \_ valide** dans le temps (&H00020000)


</dt> <dd>

Une liste de certificats de confiance utilisée pour créer cette chaîne n’était pas valide.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM \_ La \_ liste CTL de confiance \_ n’est \_ pas une \_ signature \_ valide** (&H00040000)


</dt> <dd>

Une liste de certificats de confiance utilisée pour créer cette chaîne n’a pas de signature valide.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM \_ La \_ liste CTL \_ de confiance n’est \_ pas \_ valide \_ pour \_ l’utilisation** (&H00080000)


</dt> <dd>

Une liste de certificats de confiance utilisée pour créer cette chaîne n’est pas valide pour cette utilisation.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
