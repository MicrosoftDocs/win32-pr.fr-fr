---
description: Contient les définitions des termes de sécurité qui commencent par la lettre I.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: af511aed-88f5-4b12-ad44-317925297f70
title: I (Glossaire de la sécurité)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d3e727128c2494f313bdffc879b5c5e47a28ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034852"
---
# <a name="i-security-glossary"></a>I (Glossaire de la sécurité)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) F [G](g-gly.md) [H](h-gly.md) I J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_iis_gly"></span><span id="_SECURITY_IIS_GLY"></span>**INFORMATION**
</dt> <dd>

Services logiciels qui prennent en charge la création, la configuration et la gestion de sites Web, ainsi que d’autres fonctions Internet. Internet Information Services inclure le protocole NNTP (Network News Transfer Protocol), le protocole FTP (FTP) et le protocole SMTP (Simple Mail Transfer Protocol). IIS intègre différentes fonctions pour la sécurité, permet d’obtenir des applications CGI et fournit des serveurs Gopher et FTP.

</dd> <dt>

<span id="_security_impersonation_gly"></span><span id="_SECURITY_IMPERSONATION_GLY"></span>**emprunt d’identité**
</dt> <dd>

Mécanisme qui permet à un processus de serveur de s’exécuter à l’aide des informations d’identification de sécurité du client ou d’un autre utilisateur à l’aide des informations d’identification. Lorsque le serveur emprunte l’identité du client, toutes les opérations effectuées par le serveur sont effectuées à l’aide des informations d’identification de l’utilisateur (empruntant l’identité de l’utilisateur). L’emprunt d’identité ne permet pas au serveur d’accéder aux ressources distantes pour le compte du client. Cela nécessite une délégation.

</dd> <dt>

<span id="_security_impersonation_token_gly"></span><span id="_SECURITY_IMPERSONATION_TOKEN_GLY"></span>**jeton d’emprunt d’identité**
</dt> <dd>

Jeton d’accès qui a été créé pour capturer les informations de sécurité d’un processus client, ce qui permet à un serveur d’emprunter l’identité du processus client dans les opérations de sécurité.

Voir aussi [*jeton d’accès*](a-gly.md) et [*jeton principal*](p-gly.md).

</dd> <dt>

<span id="_security_initialization_vector_gly"></span><span id="_SECURITY_INITIALIZATION_VECTOR_GLY"></span>**vecteur d’initialisation**
</dt> <dd>

(IV) séquence d’octets aléatoires ajoutée au début du texte en clair avant le chiffrement par un chiffrement par bloc. L’ajout du vecteur d’initialisation au début du texte brut élimine la possibilité de faire en sorte que le bloc de texte chiffré initial soit le même pour deux messages quelconques. Par exemple, si les messages commencent toujours par un en-tête commun (un en-tête ou une ligne « de »), leur texte chiffré initial est toujours le même, en supposant que les mêmes algorithmes de chiffrement et clé symétrique ont été utilisés. L’ajout d’un vecteur d’initialisation aléatoire élimine ce problème.

</dd> <dt>

<span id="_security_inner_data_gly"></span><span id="_SECURITY_INNER_DATA_GLY"></span>**données internes**
</dt> <dd>

Toutes les données encodées utilisées comme message pour un autre message encodé. Par exemple, un message enveloppé et sa valeur de hachage peuvent être les données internes d’un deuxième message.

</dd> <dt>

<span id="_security_inner_content_gly"></span><span id="_SECURITY_INNER_CONTENT_GLY"></span>**contenu interne**
</dt> <dd>

Données améliorées, par exemple avec une signature numérique. Ce terme est principalement utilisé lors de la discussion de données améliorées dans un \# message PKCS 7.

</dd> <dt>

<span id="_security_integrity_gly"></span><span id="_SECURITY_INTEGRITY_GLY"></span>**garantis**
</dt> <dd>

L’exhaustivité et la précision d’un message après son envoi ou son stockage.

</dd> <dt>

<span id="_security_integrity_sid_gly"></span><span id="_SECURITY_INTEGRITY_SID_GLY"></span>**SID d’intégrité**
</dt> <dd>

[*Identificateur de sécurité*](s-gly.md) (SID) qui représente un niveau d’intégrité. Un SID d’intégrité de la [*liste de contrôle d’accès système*](s-gly.md) (SACL) du descripteur de sécurité d’un objet spécifie le niveau d’intégrité de l’objet. Les SID d’intégrité d’un jeton d’accès spécifient le niveau d’intégrité du jeton.

</dd> <dt>

<span id="_security_interrupt_request_level_gly"></span><span id="_SECURITY_INTERRUPT_REQUEST_LEVEL_GLY"></span>**NIVEAU**
</dt> <dd>

Un niveau de requête d’interruption (IRQL) définit la priorité matérielle à laquelle un processeur s’exécute à un moment donné. Dans le Windows Driver Model, un thread s’exécutant à un niveau IRQL faible peut être interrompu pour exécuter du code à un niveau IRQL supérieur.

</dd> <dt>

<span id="_security_iv_gly"></span><span id="_SECURITY_IV_GLY"></span>**ÉVALUER**
</dt> <dd>

Consultez *vecteur d’initialisation*.

</dd> </dl>

 

 



