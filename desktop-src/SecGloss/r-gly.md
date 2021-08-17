---
description: Contient les définitions des termes de sécurité qui commencent par la lettre R.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ce589e18-02ac-42c2-b76b-776deb686bbd
title: R (Glossaire sécurité)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a566a939746cd65c6336e8f31ff05a7ee3f0a3b7954e9d790d3f15a8163f138b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895288"
---
# <a name="r-security-glossary"></a>R (Glossaire sécurité)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q R [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_rc2_gly"></span><span id="_SECURITY_RC2_GLY"></span>**POSTÉRIEUR**
</dt> <dd>

Nom de l’algorithme [*CryptoAPI*](c-gly.md) pour l’algorithme RC2.

Voir aussi *algorithme de bloc RC2*.

</dd> <dt>

<span id="_security_rc2_block_algorithm_gly"></span><span id="_SECURITY_RC2_BLOCK_ALGORITHM_GLY"></span>**Algorithme de bloc RC2**
</dt> <dd>

Algorithme de [*chiffrement*](e-gly.md) de données basé sur le chiffrement par bloc symétrique 64 bits RC2. RC2 est spécifié par les \_ \_ types de fournisseur complet RSA Prov. [*CryptoAPI*](c-gly.md) fait référence à cet algorithme par son identificateur (CALG \_ RC2), son nom (RC2) et sa classe ( \_ classe ALG \_ \_ Encrypt).

</dd> <dt>

<span id="_security_rc4_gly"></span><span id="_SECURITY_RC4_GLY"></span>**RC4**
</dt> <dd>

Nom de l’algorithme [*CryptoAPI*](c-gly.md) pour l’algorithme RC4.

Voir aussi *algorithme de flux RC4*.

</dd> <dt>

<span id="_security_rc4_stream_algorithm_gly"></span><span id="_SECURITY_RC4_STREAM_ALGORITHM_GLY"></span>**Algorithme de flux RC4**
</dt> <dd>

Algorithme de [*chiffrement*](e-gly.md) de données basé sur le chiffrement de flux symétrique RC4. RC4 est spécifié par les \_ \_ types de fournisseur complet RSA Prov. [*CryptoAPI*](c-gly.md) fait référence à cet algorithme par son identificateur (CALG \_ RC4), son nom (RC4) et sa classe (ALG \_ Class \_ Data \_ Encrypt).

</dd> <dt>

<span id="_security_rdn_gly"></span><span id="_SECURITY_RDN_GLY"></span>**UNIQUE**
</dt> <dd>

Consultez *nom unique relatif*.

</dd> <dt>

<span id="_security_reader_gly"></span><span id="_SECURITY_READER_GLY"></span>**lecteur**
</dt> <dd>

Un appareil standard au sein du sous-système de [*carte à puce*](s-gly.md) . Appareil d’interface (IFD) qui prend en charge l’entrée/sortie bidirectionnelle vers une carte à puce. Il peut être associé à un système entier, à un ou plusieurs groupes de lecteurs, ou à un terminal spécifique. Le sous-système de carte à puce permet à un lecteur d’être dédié au terminal auquel il est attribué. Toutefois, il n’existe actuellement qu’un seul terminal sur un ordinateur.

</dd> <dt>

<span id="_security_reader_driver_gly"></span><span id="_SECURITY_READER_DRIVER_GLY"></span>**pilote du lecteur**
</dt> <dd>

Pilote spécifique qui mappe les services de pilote à un périphérique de lecteur matériel spécifique. Il doit communiquer les événements d’insertion et de suppression de cartes au pilote de classe de [*carte*](s-gly.md) à puce pour le transfert vers le gestionnaire de ressources de carte à puce, et il doit fournir des fonctionnalités d’échange de données à la carte par n’importe quel protocole brut, t = 0, t = 1 ou pts.

</dd> <dt>

<span id="_security_reader_group_gly"></span><span id="_SECURITY_READER_GROUP_GLY"></span>**Groupe de lecteurs**
</dt> <dd>

Groupe logique de lecteurs. Les groupes de lecteurs peuvent être définis par le système ou créés par des utilisateurs ou des administrateurs. Les groupes de lecteurs sont utilisés par les fonctions de carte à puce qui peuvent agir sur des groupes de lecteurs. Pour éviter les conflits de noms avec les groupes définis par l’utilisateur, Microsoft se réserve l’utilisation d’un nom qui contient le signe dollar ($).

</dd> <dt>

<span id="_security_reader_helper_driver_gly"></span><span id="_SECURITY_READER_HELPER_DRIVER_GLY"></span>**pilote d’assistance de lecteur**
</dt> <dd>

Fournit des routines de prise en charge courantes des pilotes de carte à puce et une prise en charge de protocole T = 0 et T = 1 supplémentaire à des pilotes spécifiques en fonction des besoins.

</dd> <dt>

<span id="_security_reference_count_gly"></span><span id="_SECURITY_REFERENCE_COUNT_GLY"></span>**nombre de références**
</dt> <dd>

Valeur entière utilisée pour effectuer le suivi d’un objet COM. Lorsqu’un objet est créé, son décompte de références a la valeur 1. Chaque fois qu’une interface est liée à l’objet, son décompte de références est incrémenté ; Lorsque la connexion à l’interface est détruite, le décompte de références est décrémenté. L’objet est détruit lorsque le nombre de références atteint zéro. Toutes les interfaces à cet objet ne sont pas valides.

</dd> <dt>

<span id="_security_relative_distinguished_name_gly"></span><span id="_SECURITY_RELATIVE_DISTINGUISHED_NAME_GLY"></span>**nom unique relatif**
</dt> <dd>

UNIQUE Entité incluse comme objet dans une demande de certificat. Les éléments d’un RDN sont définis par leurs attributs et n’ont pas besoin d’inclure un nom. En ce qui concerne [*CryptoAPI*](c-gly.md), un RDN est défini par une \_ structure de certificat RDN, qui pointe à son tour vers un tableau de \_ structures d’attributs attr RDN du certificat \_ . Chaque structure d’attribut spécifie un attribut unique.

</dd> <dt>

<span id="_security_relative_identifier_gly"></span><span id="_SECURITY_RELATIVE_IDENTIFIER_GLY"></span>**identificateur relatif**
</dt> <dd>

RID Partie d’un [*identificateur de sécurité*](s-gly.md) (SID) qui identifie un utilisateur ou un groupe par rapport à l’autorité qui a émis le SID.

</dd> <dt>

<span id="_security_relocated_store_gly"></span><span id="_SECURITY_RELOCATED_STORE_GLY"></span>**magasin déplacé**
</dt> <dd>

[*Magasin de certificats*](c-gly.md) qui a été déplacé de son emplacement de Registre par défaut vers un emplacement différent dans le registre.

</dd> <dt>

<span id="_security_remote_store_gly"></span><span id="_SECURITY_REMOTE_STORE_GLY"></span>**magasin distant**
</dt> <dd>

Un [*magasin de certificats*](c-gly.md) situé sur un autre ordinateur, tel qu’un serveur de fichiers ou un autre ordinateur distant partagé.

</dd> <dt>

<span id="_security_reply_apdu_gly"></span><span id="_SECURITY_REPLY_APDU_GLY"></span>**réponse APDU**
</dt> <dd>

[*Unité de données de protocole d’application*](a-gly.md) (APDU) envoyée en réponse à un APDU reçu.

</dd> <dt>

<span id="_security_repudiation_gly"></span><span id="_SECURITY_REPUDIATION_GLY"></span>**répudiation**
</dt> <dd>

Capacité d'un utilisateur à nier l'exécution d'une action alors que les autres parties ne peuvent prouver le contraire. Par exemple, un utilisateur qui a supprimé un fichier et qui peut le refuser avec succès.

</dd> <dt>

<span id="_security_resource_manager_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_GLY"></span>**Gestionnaire de ressources**
</dt> <dd>

Module du sous-système de [*carte à puce*](s-gly.md) qui gère l’accès à plusieurs lecteurs et cartes à puce. Le gestionnaire de ressources identifie et effectue le suivi des ressources, alloue les lecteurs et les ressources à plusieurs applications et prend en charge les primitives de transaction pour accéder aux services disponibles sur une carte donnée.

</dd> <dt>

<span id="_security_resource_manager_api_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_API_GLY"></span>**API Resource Manager**
</dt> <dd>

ensemble de fonctions de Windows qui fournissent un accès direct aux services du gestionnaire de ressources.

</dd> <dt>

<span id="_security_resource_manager_context_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_CONTEXT_GLY"></span>**contexte du gestionnaire de ressources**
</dt> <dd>

Contexte utilisé par le gestionnaire de ressources lors de l’accès à la base de données de la carte à puce. Le contexte du gestionnaire de ressources est principalement utilisé par les fonctions de requête et de gestion lors de l’accès à la base de données. L’étendue du contexte du gestionnaire de ressources peut être l’utilisateur actuel ou le système.

</dd> <dt>

<span id="_security_revocation_list_gly"></span><span id="_SECURITY_REVOCATION_LIST_GLY"></span>**liste de révocation**
</dt> <dd>

Consultez [*liste de révocation de certificats*](c-gly.md).

</dd> <dt>

<span id="_security_rid_gly"></span><span id="_SECURITY_RID_GLY"></span>**RID**
</dt> <dd>

Consultez *identificateur relatif*.

</dd> <dt>

<span id="_security_root_authority_gly"></span><span id="_SECURITY_ROOT_AUTHORITY_GLY"></span>**autorité racine**
</dt> <dd>

[*Autorité de certification*](c-gly.md) en haut d’une hiérarchie d’autorité de certification. L'autorité racine certifie les autorités de certification dans le niveau suivant de la hiérarchie.

</dd> <dt>

<span id="_security_root_certificate_gly"></span><span id="_SECURITY_ROOT_CERTIFICATE_GLY"></span>**certificat racine**
</dt> <dd>

Certificat d’autorité de [*certification*](c-gly.md) auto-signé qui identifie une autorité de certification. Il s’agit d’un certificat racine, car il s’agit du certificat de l’autorité de certification racine. L’autorité de certification racine doit signer son propre certificat d’autorité de certification, car par définition il n’existe aucune autorité de certification plus élevée pour la signature de son certificat d’autorité de certification.

</dd> <dt>

<span id="_security_rsa_gly"></span><span id="_SECURITY_RSA_GLY"></span>**DOTÉ**
</dt> <dd>

RSA Data Security, Inc., un développeur et un éditeur majeurs des [*normes de chiffrement à clé publique*](p-gly.md) (PKCS). « RSA » dans le nom correspond aux noms des trois développeurs et propriétaires de la société : Rivest, Shamir et Adleman.

</dd> <dt>

<span id="_security_rsa_keyx_gly"></span><span id="_SECURITY_RSA_KEYX_GLY"></span>**RSA \_ KEYX**
</dt> <dd>

Nom de l’algorithme [*CryptoAPI*](c-gly.md) pour l’algorithme d’échange de clés RSA. CryptoAPI fait également référence à cet algorithme par son identificateur d’algorithme (CALG \_ RSA \_ KEYX) et la classe (l' \_ échange de clés de classe ALG \_ \_ ).

</dd> <dt>

<span id="_security_rsa_sign_gly"></span><span id="_SECURITY_RSA_SIGN_GLY"></span>**\_authentification RSA**
</dt> <dd>

Nom de l’algorithme CryptoAPI pour l’algorithme de signature RSA. CryptoAPI fait également référence à cet algorithme par son identificateur d’algorithme (CALG \_ RSA \_ Sign) et la classe ( \_ signature de classe ALG \_ ).

</dd> <dt>

<span id="_security_rsa_public_key_algorithm_gly"></span><span id="_SECURITY_RSA_PUBLIC_KEY_ALGORITHM_GLY"></span>**Algorithme de clé publique RSA**
</dt> <dd>

Un algorithme d’échange de clés et de signature basé sur le chiffrement de clé publique RSA populaire. Cet algorithme est utilisé par \_ \_ les types Prov RSA complet, Prov \_ RSA \_ SIG, PROV- \_ \_ Exchange et prove \_ SSL Provider. CryptoAPI fait référence à cet algorithme par ses identificateurs (CALG \_ RSA \_ KEYX et CALG \_ RSA \_ Sign), les noms (RSA \_ KEYX et RSA \_ Sign) et la classe ( \_ échange de clés de classe ALG \_ \_ ).

</dd> </dl>

 

 



