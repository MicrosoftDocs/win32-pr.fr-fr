---
description: Définit ou récupère les indicateurs de contrôle de validité d’un certificat.
ms.assetid: c80c95a0-8a9b-441d-b243-7ee0552731e4
title: CertificateStatus. CheckFlag, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.CheckFlag
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 00b0c648de17f6aca931ab3f3417d9ecb53ac558
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523524"
---
# <a name="certificatestatuscheckflag-property"></a>CertificateStatus. CheckFlag, propriété

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**structure X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **CheckFlag** définit ou récupère les indicateurs de contrôle de validité d’un certificat.

## <a name="syntax"></a>Syntaxe


```VB
CertificateStatus.CheckFlag As CAPICOM_CHECK_FLAG
```



## <a name="property-value"></a>Valeur de la propriété

Valeur de l’énumération de l' [**\_ \_ indicateur de vérification CAPICOM**](capicom-check-flag.md) qui décrit les vérifications de validité du certificat. La valeur par défaut est **CAPICOM \_ vérifier \_ en ligne \_**.

**CAPICOM 2.0.0.3/2.0.0.2/2.0.0.1 :** La valeur par défaut est la vérification de la [**\_ \_ \_ validité**](capicom-check-flag.md)de la signature, de la [**\_ \_ \_ validité de la vérification CAPICOM**](capicom-check-flag.md), de la vérification de la [**\_ \_ \_ racine approuvée**](capicom-check-flag.md)et de la [**\_ \_ \_ chaîne complète**](capicom-check-flag.md)de la vérification CAPICOM.

**Capicom 2,0 et versions antérieures :** La valeur par défaut est la vérification de la [**\_ \_ \_ validité**](capicom-check-flag.md)de la signature, la validité de la [**\_ vérification \_ \_ CAPICOM**](capicom-check-flag.md)et la vérification de la [**\_ \_ \_ racine de confiance de CAPICOM**](capicom-check-flag.md).

Le tableau suivant répertorie les valeurs possibles.



| Value                                                                                                                                                                                                                                          | Signification                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CHECK_BASIC_CONSTRAINTS"></span><span id="capicom_check_basic_constraints"></span><dl> <dt>**CAPICOM- \_ vérifier les \_ contraintes de base \_**</dt> </dl>                          | Vérifie les contraintes de base. Introduit dans CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_CHECK_COMPLETE_CHAIN"></span><span id="capicom_check_complete_chain"></span><dl> <dt>**vérification de la \_ \_ chaîne complète de CAPICOM \_**</dt> </dl>                                   | Vérifie la chaîne complète. Introduit dans CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_CHECK_NAME_CONSTRAINTS"></span><span id="capicom_check_name_constraints"></span><dl> <dt>**\_vérifier les contraintes de \_ nom dans CAPICOM \_**</dt> </dl>                             | Vérifie les contraintes de nom. Introduit dans CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <span id="CAPICOM_CHECK_NESTED_VALIDITY_PERIOD"></span><span id="capicom_check_nested_validity_period"></span><dl> <dt>**vérification de la \_ \_ période de validité imbriquée pour \_ CAPICOM \_**</dt> </dl>          | Vérifie la validité imbriquée. Introduit dans CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_CHECK_NONE"></span><span id="capicom_check_none"></span><dl> <dt>**vérification de CAPICOM \_ \_ aucun**</dt> </dl>                                                                  | Aucune vérification de validité n’est effectuée.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| <span id="CAPICOM_CHECK_OFFLINE_ALL"></span><span id="capicom_check_offline_all"></span><dl> <dt>**\_vérification CAPICOM \_ tout en mode hors connexion \_**</dt> </dl>                                            | Vérifie tout en mode hors connexion. Les vérifications de révocation sont effectuées sur tous les certificats de la chaîne, à l’exception du certificat racine. Introduit dans CAPICOM 2,0.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_CHECK_ONLINE_ALL"></span><span id="capicom_check_online_all"></span><dl> <dt>**CAPICOM- \_ vérifier \_ en ligne \_ tout**</dt> </dl>                                               | Vérifie tout en ligne. Les vérifications de révocation sont effectuées sur tous les certificats de la chaîne, à l’exception du certificat racine. Introduit dans CAPICOM 2,0.<br/>                                                                                                                                                                                                                                         |
| <span id="CAPICOM_CHECK_OFFLINE_REVOCATION_STATUS"></span><span id="capicom_check_offline_revocation_status"></span><dl> <dt>**\_vérifier l’état de \_ \_ révocation hors \_ connexion dans CAPICOM**</dt> </dl> | Vérifie l’état de révocation de tous les certificats de la chaîne en utilisant uniquement les listes de révocation de certificats hors connexion.<br/>                                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_CHECK_ONLINE_REVOCATION_STATUS"></span><span id="capicom_check_online_revocation_status"></span><dl> <dt>**\_vérifier l’état de \_ \_ révocation en \_ ligne de CAPICOM**</dt> </dl>    | Vérifie l’état de révocation de tous les certificats de la chaîne à l’aide des listes de révocation de certificats disponibles en ligne. Les listes de révocation de certificats sont téléchargées à l’aide de l’extension CDP dans le certificat.<br/> Si la liste de révocation de certificats a été téléchargée et n’a pas expiré, CAPICOM l’utilise et ne passe pas en ligne.<br/> Si une liste de révocation de certificats n’a pas été téléchargée ou est obsolète, CAPICOM se met en ligne pour tenter de télécharger la liste de révocation de certificats.<br/> |
| <span id="CAPICOM_CHECK_SIGNATURE_VALIDITY"></span><span id="capicom_check_signature_validity"></span><dl> <dt>**vérification de la \_ validité de la \_ signature de CAPICOM \_**</dt> </dl>                       | Recherche des signatures valides sur tous les certificats de la chaîne.<br/>                                                                                                                                                                                                                                                                                                                           |
| <span id="CAPICOM_CHECK_TIME_VALIDITY"></span><span id="capicom_check_time_validity"></span><dl> <dt>**vérification de la \_ validité de la durée du contrôle CAPICOM \_ \_**</dt> </dl>                                      | Vérifie la validité de tous les certificats de la chaîne.<br/>                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_CHECK_TRUSTED_ROOT"></span><span id="capicom_check_trusted_root"></span><dl> <dt>**CAPICOM vérifier la \_ \_ racine approuvée \_**</dt> </dl>                                         | Recherche une racine approuvée de la chaîne de certificats.<br/>                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
