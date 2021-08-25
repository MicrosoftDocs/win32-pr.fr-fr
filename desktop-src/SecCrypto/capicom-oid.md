---
description: Fournit les noms des identificateurs d’objet CAPICOM.
ms.assetid: 6c1eb2cc-84ac-4920-99ba-56ac8de4a851
title: Énumération CAPICOM_OID (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_OID
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 8c008a77e11bd7803dfb09ed2e6ddf1f57ed8695f2de33655239eb73ac49a248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879029"
---
# <a name="capicom_oid-enumeration"></a>CAPICOM OID ( \_ énumération)

L’énumération **CAPICOM \_ OID** fournit les noms des identificateurs d’objet CAPICOM.

Cette énumération est utilisée par l' [**OID. Propriété Name**](oid-name.md) .

## <a name="members"></a>Membres



| Membre                                                        | Description                                                                                                                                                                                                                                    | Valeur |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ OID \_ autre**                                       | L’objet n’est pas l’un des types d’objet CAPICOM prédéfinis.<br/>                                                                                                                                                                       | 0     |
| **EXTENSION de l' \_ \_ identificateur de \_ clé \_ de l’autorité de l’OID \_ CAPICOM**       | L’objet est une extension de certificat qui contient l’identificateur de clé publique de l’autorité de certification.<br/>                                                                                                                  | 1     |
| **\_extension des attributs de \_ clé CAPICOM OID \_ \_**                  | L’objet est une extension de certificat qui contient des attributs facultatifs d’une clé publique.<br/>                                                                                                                                            | 2     |
| **EXTENSION de stratégies de certificat de l' \_ OID capicom \_ \_ \_ 95 \_**               | l’objet est une extension de certificat qui contient des informations de stratégie de certificat Windows 95.<br/>                                                                                                                                      | 3     |
| **EXTENSION de restriction d’utilisation de la \_ clé CAPICOM OID \_ \_ \_ \_**          | L’objet est une extension de certificat qui contient des restrictions sur l’utilisation de la clé publique d’un certificat.<br/>                                                                                                                          | 4     |
| **\_ \_ \_ extension des \_ mappages de stratégies héritées de CAPICOM OID \_**         | L’objet est une extension de certificat qui contient des informations de mappage de stratégie héritées.<br/>                                                                                                                                              | 5     |
| **EXTENSION de nom de remplacement de l' \_ objet CAPICOM OID \_ \_ \_ \_**               | L’objet est une extension de certificat qui contient un autre nom pour le sujet du certificat.<br/>                                                                                                                         | 6     |
| **EXTENSION de nom de remplacement de l' \_ émetteur d’OID CAPICOM \_ \_ \_ \_**                | L’objet est une extension de certificat qui contient un autre nom pour l’émetteur du certificat.<br/>                                                                                                                          | 7     |
| **EXTENSION des contraintes de base de CAPICOM \_ OID \_ \_ \_**               | L’objet est une extension de certificat qui indique si l’objet certifié peut agir en tant qu’autorité de certification, entité de fin ou les deux. <br/>                                                                                                        | 8     |
| **EXTENSION de l' \_ \_ identificateur de \_ clé du sujet \_ de CAPICOM OID \_**         | L’objet est une extension de certificat qui contient l’identificateur de clé du sujet du certificat.<br/>                                                                                                                           | 9     |
| **EXTENSION d’utilisation de la \_ clé CAPICOM OID \_ \_ \_**                       | L’objet est une extension de certificat qui contient des informations sur l’utilisation prévue de la clé publique d’un certificat.<br/>                                                                                                               | 10    |
| **\_extension de période d' \_ utilisation de PRIVATEKEY OID OID \_ \_ \_**        | L’objet est une extension de certificat qui contient des informations sur la période pendant laquelle la clé privée d’un certificat est utilisable.<br/>                                                                                           | 11    |
| **\_ \_ \_ Extension de Alt \_ nom2 \_ de l’objet OID OID**              | L’objet est une extension de certificat qui contient un autre nom pour le sujet du certificat.<br/>                                                                                                                         | 12    |
| **\_Extension OID de CAPICOM \_ \_ Alt \_ nom2 \_**               | L’objet est une extension de certificat qui contient un autre nom pour l’émetteur du certificat.<br/>                                                                                                                          | 13    |
| **\_ \_ Extension CONSTRAINTS2 de base OID \_ OID \_**              | L’objet est une extension de certificat qui indique si l’objet certifié peut agir en tant qu’autorité de certification, entité de fin ou les deux. <br/>                                                                                                        | 14    |
| **\_extension de contraintes de \_ nom CAPICOM OID \_ \_**                | L’objet est une extension de certificat qui contient des informations sur les certificats qui sont spécifiquement autorisés ou exclus de l’approbation.<br/>                                                                                          | 15    |
| **\_ \_ \_ extension des points de distribution de \_ l’OID de CAPICOM OID \_**                | L’objet est une extension de certificat qui contient des informations utilisées pour mettre à jour la liste de révocation de certificats (CRL).<br/>                                                                                                               | 16    |
| **EXTENSION des stratégies de certificat de CAPICOM \_ OID \_ \_ \_**                   | L’objet est une extension de certificat qui contient une liste des stratégies que le certificat prend en charge.<br/>                                                                                                                           | 17    |
| **\_ \_ \_ extension de mappages de stratégie d’OID CAPICOM \_**                 | L’objet est une extension de certificat qui fournit des mappages entre des stratégies dans des domaines différents.<br/>                                                                                                                                 | 18    |
| **EXTENSION de la clé de l’autorité de l' \_ OID CAPICOM \_ \_ \_ \_**      | L’objet est une extension de certificat qui contient l’identificateur de clé publique de l’autorité de certification.<br/>                                                                                                                                            | 19    |
| **\_extension de contraintes de \_ stratégie d’OID \_ CAPICOM \_**              | L’objet est une extension de certificat qui contient des stratégies établies pour accepter des certificats comme approuvés.<br/>                                                                                                                     | 20    |
| **\_ \_ extension d’utilisation améliorée de \_ la \_ clé \_ CAPICOM OID**             | L’objet est une extension de certificat qui contient des informations améliorées sur l’utilisation prévue de la clé publique d’un certificat.<br/>                                                                                                      | 21    |
| **\_extension de modèle de \_ certificat CAPICOM OID \_ \_**            | L’objet est une extension de certificat qui contient un modèle de certificat.<br/>                                                                                                                                                         | 22    |
| **\_ \_ \_ extension de \_ stratégies CERT \_ de l’application CAPICOM OID**      | L’objet est une extension de certificat qui contient la stratégie d’application du certificat.<br/>                                                                                                                                      | 23    |
| **\_ \_ \_ extension des \_ mappages de stratégie d’application \_ de CAPICOM OID**    | L’objet est une extension de certificat qui contient des mappages entre différentes stratégies d’application.<br/>                                                                                                                                | 24    |
| **\_extension des contraintes de \_ \_ stratégie d' \_ application \_ de l’OID CAPICOM** | L’objet est une extension de certificat qui contient les contraintes de stratégie d’application du certificat.<br/>                                                                                                                          | 25    |
| **\_ \_ \_ extension d’accès aux informations de \_ l' \_ autorité d’OID CAPICOM**          | L’objet est une extension de certificat qui indique comment accéder aux informations et aux services de l’autorité de certification pour l’émetteur du certificat.<br/>                                                                                                   | 26    |
| **\_ \_ \_ authentification EKU du serveur CAPICOM OID \_**                           | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour authentifier un serveur.<br/>                                                                                                                | 100   |
| **\_EKU d’authentification du \_ client CAPICOM OID \_ \_**                           | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour authentifier un client.<br/>                                                                                                                | 101   |
| **utilisation améliorée de la \_ \_ signature de code OID \_ de CAPICOM \_**                          | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour créer une signature numérique.<br/>                                                                                                           | 102   |
| **\_utilisation améliorée de la \_ protection par E-mail de CAPICOM OID \_ \_**                      | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour la protection de la messagerie.<br/>                                                                                                                    | 103   |
| **\_utilisation améliorée de la \_ \_ \_ \_ EKU système IPSec de l’OID CAPICOM**                     | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour un système de terminaison IPSec.<br/>                                                                                                                 | 104   |
| **\_ \_ \_ utilisation améliorée du tunnel IPSec CAPICOM \_ OID**                          | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour le tunneling IPSec.<br/>                                                                                                                     | 105   |
| **\_ \_ \_ EKU d’utilisateur IPSec CAPICOM OID \_**                            | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour un utilisateur IPSec.<br/>                                                                                                                       | 106   |
| **utilisation améliorée de l’horodateur de l’horodatage de l' \_ OID CAPICOM \_ \_ \_**                         | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour l’horodatage.<br/>                                                                                                                       | 107   |
| **\_utilisation améliorée de la \_ liste CTL pour la \_ signature d’utilisation de l’OID \_ CAPICOM \_**                    | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour signer la liste de certificats de confiance (CTL).<br/>                                                                                                | 108   |
| **\_ \_ \_ \_ \_ utilisation améliorée de la signature de l’horodatage de l’OID CAPICOM**                   | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour signer un horodatage.<br/>                                                                                                                    | 109   |
| **\_ \_ \_ \_ utilisation améliorée du chiffrement par le serveur CAPICOM OID \_**                  | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour le [*chiffrement SGC (Server-Gated Cryptography*](../secgloss/s-gly.md) ).<br/> | 110   |
| **\_utilisation améliorée de la \_ EKU du \_ système de fichiers de chiffrement OID \_ \_**               | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour le [*système de fichiers EFS*](../secgloss/e-gly.md) (EFS).<br/>      | 111   |
| **\_utilisation améliorée de la \_ récupération EFS de CAPICOM OID EFS \_ \_**                          | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour la récupération du système de fichiers EFS.<br/>                                                                                                                 | 112   |
| **\_utilisation améliorée de la \_ \_ EKU de chiffrement de CAPICOM OID WHQL \_**                           | l’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour Windows le chiffrement WHQL (Hardware Quality Labs).<br/>                                                                                   | 113   |
| **\_Utilisation améliorée de la \_ \_ EKU crypto \_ OID de CAPICOM**                            | l’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour le chiffrement Windows Server 2003 et Windows XP.<br/>                                                                                     | 114   |
| **utilisation améliorée de la version \_ \_ \_ améliorée du \_ chiffrement \_ de l’OID de CAPICOM OEM WHQL**                      | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour le chiffrement WHQL du fabricant d’ordinateurs OEM (Original Equipment Manufacturers).<br/>                                                                            | 115   |
| **\_utilisation améliorée de la \_ EKU de \_ \_ chiffrement \_ NT par l’OID de CAPICOM**                    | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour Windows le chiffrement NT Embedded.<br/>                                                                                                    | 116   |
| **\_utilisation améliorée de la \_ liste racine du signataire de la liste racine CAPICOM OID \_ \_ \_**                     | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour signer une liste racine.<br/>                                                                                                                     | 117   |
| **\_ \_ EKU de subordination qualifiée d’OID \_ CAPICOM \_**               | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour la subordination qualifiée.<br/>                                                                                                             | 118   |
| **\_utilisation améliorée de la \_ clé de récupération de clé OID OID \_ \_**                          | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour la récupération de clé.<br/>                                                                                                                        | 119   |
| **\_utilisation améliorée de la \_ \_ EKU des droits numériques CAPICOM OID \_**                        | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour les droits numériques.<br/>                                                                                                                      | 120   |
| **\_utilisation améliorée de la licence d’OID de CAPICOM \_ \_**                               | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour les licences.<br/>                                                                                                                            | 121   |
| **utilisation améliorée de la \_ licence du serveur de licences CAPICOM OID \_ \_ \_**                        | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour un serveur de licences.<br/>                                                                                                                    | 122   |
| **\_utilisation améliorée de la \_ \_ connexion par carte à puce \_ de l’OID CAPICOM \_**                     | L’objet est un objet [**EKU**](eku.md) qui spécifie que le certificat peut être utilisé pour l’ouverture de session par carte à puce.<br/>                                                                                                                    | 123   |
| **\_ \_ \_ \_ identificateur \_ CPS de la stratégie de l’OID d’OID CAPICOM**                | L’objet est une déclaration CPS (certification Practice Statement) qui peut être utilisée pour le qualificateur de stratégie de l’infrastructure de clé publique X. 509 (PKIX).<br/>                                                                                            | 124   |
| **\_qualificateur de stratégie PKIX de CAPICOM OID \_ \_ \_ \_ USERNOTICE**         | L’objet est un avis de l’utilisateur qui peut être utilisé pour le qualificateur de stratégie de l’infrastructure de clé publique X. 509 (PKIX).<br/>                                                                                                                       | 125   |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
