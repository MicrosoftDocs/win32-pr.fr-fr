---
description: Contient les définitions des termes de sécurité qui commencent par la lettre D.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d007cbb9-b547-4dc7-bc22-b526f650f7c2
title: D (Glossaire sécurité)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f81a17b2ba2c34b6d5367c1f920ad4b2a4048b2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311290"
---
# <a name="d-security-glossary"></a>D (Glossaire sécurité)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [e](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_dac_gly"></span><span id="_SECURITY_DAC_GLY"></span>**DAC**
</dt> <dd>

Consultez *contrôle d’accès dynamique*.

</dd> <dt>

<span id="_security_dacl_gly"></span><span id="_SECURITY_DACL_GLY"></span>**DACL**
</dt> <dd>

Consultez *liste de contrôle d’accès discrétionnaire*.

</dd> <dt>

<span id="_security_data_content_type_gly"></span><span id="_SECURITY_DATA_CONTENT_TYPE_GLY"></span>**type de contenu des données**
</dt> <dd>

Type de contenu de base défini par PKCS \# 7. Le contenu de données est simplement une chaîne d’octets (Byte).

</dd> <dt>

<span id="_security_data_encryption_gly"></span><span id="_SECURITY_DATA_ENCRYPTION_GLY"></span>**chiffrement des données**
</dt> <dd>

Consultez [*chiffrement*](e-gly.md).

</dd> <dt>

<span id="_security_data_encryption_function_gly"></span><span id="_SECURITY_DATA_ENCRYPTION_FUNCTION_GLY"></span>**fonction de chiffrement des données**
</dt> <dd>

Consultez [*fonctions de chiffrement et de déchiffrement*](e-gly.md).

</dd> <dt>

<span id="_security_data_encryption_standard_gly"></span><span id="_SECURITY_DATA_ENCRYPTION_STANDARD_GLY"></span>**Data Encryption Standard**
</dt> <dd>

DES Chiffrement par bloc qui chiffre les données dans les blocs 64 bits. DES est un algorithme symétrique qui utilise le même algorithme et la même clé pour le chiffrement et le déchiffrement.

Développé au début des années 1970, est également appelé DEA (Data Encryption Algorithm) par ANSI et DEA-1 par ISO.

</dd> <dt>

<span id="_security_datagram_gly"></span><span id="_SECURITY_DATAGRAM_GLY"></span>**reçus**
</dt> <dd>

Canal de communication qui utilise des informations routées via un réseau de commutation de paquets. Ces informations incluent des paquets d’informations distincts et les informations de remise associées à ces paquets, telles que l’adresse de destination. Dans un réseau de commutation de paquets, les paquets de données sont acheminés indépendamment les uns des autres et peuvent suivre différents itinéraires. Ils peuvent également arriver dans un ordre différent de celui dans lequel ils ont été envoyés.

</dd> <dt>

<span id="_security_decoding_gly"></span><span id="_SECURITY_DECODING_GLY"></span>**décodage**
</dt> <dd>

Processus de conversion d’un objet encodé (tel qu’un certificat) ou de données vers son format d’origine.

En général, les données sont décodées par la couche d’encodage/décodage du protocole de communication. Les certificats sont décodés par un appel à la fonction **CryptDecodeObject** .

</dd> <dt>

<span id="_security_decryption_gly"></span><span id="_SECURITY_DECRYPTION_GLY"></span>**déchiffrement**
</dt> <dd>

Processus de conversion de texte chiffré en texte brut. Le déchiffrement est l’opposé du chiffrement.

</dd> <dt>

<span id="_security_default_mode_gly"></span><span id="_SECURITY_DEFAULT_MODE_GLY"></span>**mode par défaut**
</dt> <dd>

Paramètres par défaut, tels que le mode de chiffrement par bloc ou la méthode de remplissage de chiffrement par bloc.

</dd> <dt>

<span id="_security_der_gly"></span><span id="_SECURITY_DER_GLY"></span>**DER**
</dt> <dd>

consultez *Distinguished Encoding Rules*.

</dd> <dt>

<span id="_security_derived_key_gly"></span><span id="_SECURITY_DERIVED_KEY_GLY"></span>**clé dérivée**
</dt> <dd>

Clé de chiffrement créée par un appel à la fonction **CryptDeriveKey** . Une clé dérivée peut être créée à partir d’un mot de passe ou de toute autre donnée utilisateur. Les clés dérivées permettent aux applications de créer des clés de session en fonction des besoins, ce qui évite d’avoir à stocker une clé particulière.

</dd> <dt>

<span id="_security_des_gly"></span><span id="_SECURITY_DES_GLY"></span>**DES**
</dt> <dd>

Voir *Data Encryption Standard*.

</dd> <dt>

<span id="_security_dh_gly"></span><span id="_SECURITY_DH_GLY"></span>**VA**
</dt> <dd>

Consultez *algorithme Diffie-Hellman*.

</dd> <dt>

<span id="_security_dh_keyx_gly"></span><span id="_SECURITY_DH_KEYX_GLY"></span>**\_KEYX DH**
</dt> <dd>

Nom de l’algorithme CryptoAPI pour l’algorithme d’échange de clés Diffie-Hellman.

Voir aussi *algorithme Diffie-Hellman*.

</dd> <dt>

<span id="_security_diffie_hellman_algorithm_gly"></span><span id="_SECURITY_DIFFIE_HELLMAN_ALGORITHM_GLY"></span>**Algorithme Diffie-Hellman**
</dt> <dd>

VA Algorithme de clé publique utilisé pour l’échange de clés sécurisées. Diffie-Hellman ne peut pas être utilisé pour le chiffrement des données. Cet algorithme est spécifié en tant qu’algorithme d’échange de clés pour les \_ \_ types de fournisseurs DH DSS.

Voir aussi *Diffie-Hellman (stockage et transfert) clé-algorithme d’échange* et *algorithme d’échange de clés Diffie-Hellman (éphémère)*.

</dd> <dt>

<span id="_security_diffie_hellman_store_and_forward_key_exchange_algorithm_gly"></span><span id="_SECURITY_DIFFIE_HELLMAN_STORE_AND_FORWARD_KEY_EXCHANGE_ALGORITHM_GLY"></span>**Diffie-Hellman (stockage et transfert) clé-algorithme d’échange**
</dt> <dd>

Algorithme de Diffie-Hellman dans lequel les valeurs de clé Exchange sont conservées (dans le CSP) après la destruction du handle de clé.

Voir aussi *algorithme d’échange de clés Diffie-Hellman (éphémère)*.

</dd> <dt>

<span id="_security_diffie_hellman_ephemeral_key_exchange_algorithm_gly"></span><span id="_SECURITY_DIFFIE_HELLMAN_EPHEMERAL_KEY_EXCHANGE_ALGORITHM_GLY"></span>**Algorithme d’échange de clés Diffie-Hellman (éphémère)**
</dt> <dd>

Algorithme de Diffie-Hellman dans lequel la valeur de clé d’échange est supprimée du CSP lorsque le handle de clé est détruit.

Voir aussi *algorithme d’échange de clés Diffie-Hellman (stockage et transfert)*.

</dd> <dt>

<span id="_security_digested_data_gly"></span><span id="_SECURITY_DIGESTED_DATA_GLY"></span>**données résumées**
</dt> <dd>

Type de contenu de données défini par PKCS \# 7 qui se compose de tout type de données plus un hachage de message (Digest) du contenu.

</dd> <dt>

<span id="_security_digital_certificate_gly"></span><span id="_SECURITY_DIGITAL_CERTIFICATE_GLY"></span>**certificat numérique**
</dt> <dd>

Consultez [*certificat*](c-gly.md).

</dd> <dt>

<span id="_security_digital_envelope_gly"></span><span id="_SECURITY_DIGITAL_ENVELOPE_GLY"></span>**enveloppe numérique**
</dt> <dd>

Messages privés chiffrés à l’aide de la clé publique du destinataire. Les messages enveloppés ne peuvent être déchiffrés qu’à l’aide de la clé privée du destinataire, ce qui permet uniquement au destinataire de comprendre le message.

</dd> <dt>

<span id="_security_digital_signature_gly"></span><span id="_SECURITY_DIGITAL_SIGNATURE_GLY"></span>**signature numérique**
</dt> <dd>

Données qui lient l'identité d'un expéditeur aux informations qui sont envoyées. Une signature numérique peut être fournie avec tout message, fichier, ou autre information encodée numériquement, ou transmise séparément. Les signatures numériques sont utilisées dans les environnements de clé publique et fournissent des services d'authentification et d'intégrité.

</dd> <dt>

<span id="_security_digital_signature_algorithm_gly"></span><span id="_SECURITY_DIGITAL_SIGNATURE_ALGORITHM_GLY"></span>**Algorithme de signature numérique**
</dt> <dd>

DSA Algorithme de clé publique spécifié par le standard de signature numérique (DSS). DSA est utilisé uniquement pour générer des signatures numériques. Il ne peut pas être utilisé pour le chiffrement des données.

</dd> <dt>

<span id="_security_digital_signature_key_pair_gly"></span><span id="_SECURITY_DIGITAL_SIGNATURE_KEY_PAIR_GLY"></span>**paire de clés de signature numérique**
</dt> <dd>

Consultez [*paire de clés de signature*](s-gly.md).

</dd> <dt>

<span id="_security_digital_signature_standard_gly"></span><span id="_SECURITY_DIGITAL_SIGNATURE_STANDARD_GLY"></span>**Norme de signature numérique**
</dt> <dd>

NORME Norme qui spécifie l’algorithme de signature numérique (DSA) pour son algorithme de signature et SHA-1 comme algorithme de hachage de message. DSA est un chiffrement de clé publique qui est utilisé uniquement pour générer des signatures numériques et qui ne peut pas être utilisé pour le chiffrement des données. DSS est spécifié par les types de fournisseurs PROV-DSS \_ , Prov \_ DSS- \_ DH et Proven \_ Fortezza.

</dd> <dt>

<span id="_security_discretionary_access_control_list_gly"></span><span id="_SECURITY_DISCRETIONARY_ACCESS_CONTROL_LIST_GLY"></span>**liste de contrôle d’accès discrétionnaire**
</dt> <dd>

DACL Liste de contrôle d’accès qui est contrôlée par le propriétaire d’un objet et qui spécifie l’accès à l’objet par des utilisateurs ou des groupes particuliers.

Voir aussi [*liste de contrôle d’accès*](a-gly.md) et [*liste de contrôle d’accès système*](s-gly.md).

</dd> <dt>

<span id="_security_distinguished_encoding_rules_gly"></span><span id="_SECURITY_DISTINGUISHED_ENCODING_RULES_GLY"></span>**Distinguished Encoding Rules**
</dt> <dd>

DER Ensemble de règles pour l’encodage des données définies ASN. 1 comme un flux de bits pour le stockage ou la transmission externes. Chaque objet ASN. 1 a exactement un encodage DER correspondant. DER est défini dans la recommandation CCITT X. 509, section 8,7. Il s’agit de l’une des deux méthodes d’encodage actuellement utilisées par CryptoAPI.

</dd> <dt>

<span id="_security_dll_gly"></span><span id="_SECURITY_DLL_GLY"></span>**DLL**
</dt> <dd>

Consultez *bibliothèque de liens dynamiques*.

</dd> <dt>

<span id="_security_dsa_gly"></span><span id="_SECURITY_DSA_GLY"></span>**DSA**
</dt> <dd>

Voir *algorithme de signature numérique*.

</dd> <dt>

<span id="_security_dss_gly"></span><span id="_SECURITY_DSS_GLY"></span>**NORME**
</dt> <dd>

Voir *signature numérique standard*.

</dd> <dt>

<span id="_security_dynamic_access_control_gly"></span><span id="_SECURITY_DYNAMIC_ACCESS_CONTROL_GLY"></span>**Access Control dynamique**
</dt> <dd>

DAC La possibilité de spécifier des stratégies de contrôle d’accès en fonction des revendications d’utilisateur, de périphérique et de ressource. Cela permet une authentification plus flexible pour les applications tout en conservant les exigences de sécurité et de conformité.

</dd> <dt>

<span id="_security_dynamic_link_library_gly"></span><span id="_SECURITY_DYNAMIC_LINK_LIBRARY_GLY"></span>**bibliothèque de liens dynamiques**
</dt> <dd>

(DLL) fichier qui contient des routines exécutables qui peuvent être appelées à partir d’autres applications.

</dd> </dl>

 

 



