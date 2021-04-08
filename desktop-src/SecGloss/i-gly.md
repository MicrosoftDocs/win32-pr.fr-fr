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
# <a name="i-security-glossary"></a><span data-ttu-id="2b635-103">I (Glossaire de la sécurité)</span><span class="sxs-lookup"><span data-stu-id="2b635-103">I (Security Glossary)</span></span>

<span data-ttu-id="2b635-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) F [G](g-gly.md) [H](h-gly.md) I J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="2b635-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) I J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="2b635-105"><span id="_security_iis_gly"></span><span id="_SECURITY_IIS_GLY"></span>**INFORMATION**</span><span class="sxs-lookup"><span data-stu-id="2b635-105"><span id="_security_iis_gly"></span><span id="_SECURITY_IIS_GLY"></span>**IIS**</span></span>
</dt> <dd>

<span data-ttu-id="2b635-106">Services logiciels qui prennent en charge la création, la configuration et la gestion de sites Web, ainsi que d’autres fonctions Internet.</span><span class="sxs-lookup"><span data-stu-id="2b635-106">Software services that support website creation, configuration, and management, along with other Internet functions.</span></span> <span data-ttu-id="2b635-107">Internet Information Services inclure le protocole NNTP (Network News Transfer Protocol), le protocole FTP (FTP) et le protocole SMTP (Simple Mail Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="2b635-107">Internet Information Services include Network News Transfer Protocol (NNTP), File Transfer Protocol (FTP), and Simple Mail Transfer Protocol (SMTP).</span></span> <span data-ttu-id="2b635-108">IIS intègre différentes fonctions pour la sécurité, permet d’obtenir des applications CGI et fournit des serveurs Gopher et FTP.</span><span class="sxs-lookup"><span data-stu-id="2b635-108">IIS incorporates various functions for security, allows for CGI applications, and provides for Gopher and FTP servers.</span></span>

</dd> <dt>

<span data-ttu-id="2b635-109"><span id="_security_impersonation_gly"></span><span id="_SECURITY_IMPERSONATION_GLY"></span>**emprunt d’identité**</span><span class="sxs-lookup"><span data-stu-id="2b635-109"><span id="_security_impersonation_gly"></span><span id="_SECURITY_IMPERSONATION_GLY"></span>**impersonation**</span></span>
</dt> <dd>

<span data-ttu-id="2b635-110">Mécanisme qui permet à un processus de serveur de s’exécuter à l’aide des informations d’identification de sécurité du client ou d’un autre utilisateur à l’aide des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="2b635-110">A mechanism that allows a server process to run by using the security credentials of the client or some other user using the credentials.</span></span> <span data-ttu-id="2b635-111">Lorsque le serveur emprunte l’identité du client, toutes les opérations effectuées par le serveur sont effectuées à l’aide des informations d’identification de l’utilisateur (empruntant l’identité de l’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="2b635-111">When the server is impersonating the client, any operations performed by the server are performed by using the client's (impersonating user's) credentials.</span></span> <span data-ttu-id="2b635-112">L’emprunt d’identité ne permet pas au serveur d’accéder aux ressources distantes pour le compte du client.</span><span class="sxs-lookup"><span data-stu-id="2b635-112">Impersonation does not allow the server to access remote resources on behalf of the client.</span></span> <span data-ttu-id="2b635-113">Cela nécessite une délégation.</span><span class="sxs-lookup"><span data-stu-id="2b635-113">This requires delegation.</span></span>

</dd> <dt>

<span data-ttu-id="2b635-114"><span id="_security_impersonation_token_gly"></span><span id="_SECURITY_IMPERSONATION_TOKEN_GLY"></span>**jeton d’emprunt d’identité**</span><span class="sxs-lookup"><span data-stu-id="2b635-114"><span id="_security_impersonation_token_gly"></span><span id="_SECURITY_IMPERSONATION_TOKEN_GLY"></span>**impersonation token**</span></span>
</dt> <dd>

<span data-ttu-id="2b635-115">Jeton d’accès qui a été créé pour capturer les informations de sécurité d’un processus client, ce qui permet à un serveur d’emprunter l’identité du processus client dans les opérations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="2b635-115">An access token that has been created to capture the security information of a client process, allowing a server to "impersonate" the client process in security operations.</span></span>

<span data-ttu-id="2b635-116">Voir aussi [*jeton d’accès*](a-gly.md) et [*jeton principal*](p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2b635-116">See also [*access token*](a-gly.md) and [*primary token*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b635-117"><span id="_security_initialization_vector_gly"></span><span id="_SECURITY_INITIALIZATION_VECTOR_GLY"></span>**vecteur d’initialisation**</span><span class="sxs-lookup"><span data-stu-id="2b635-117"><span id="_security_initialization_vector_gly"></span><span id="_SECURITY_INITIALIZATION_VECTOR_GLY"></span>**initialization vector**</span></span>
</dt> <dd>

<span data-ttu-id="2b635-118">(IV) séquence d’octets aléatoires ajoutée au début du texte en clair avant le chiffrement par un chiffrement par bloc.</span><span class="sxs-lookup"><span data-stu-id="2b635-118">(IV) A sequence of random bytes appended to the front of the plaintext before encryption by a block cipher.</span></span> <span data-ttu-id="2b635-119">L’ajout du vecteur d’initialisation au début du texte brut élimine la possibilité de faire en sorte que le bloc de texte chiffré initial soit le même pour deux messages quelconques.</span><span class="sxs-lookup"><span data-stu-id="2b635-119">Adding the initialization vector to the beginning of the plaintext eliminates the possibility of having the initial ciphertext block the same for any two messages.</span></span> <span data-ttu-id="2b635-120">Par exemple, si les messages commencent toujours par un en-tête commun (un en-tête ou une ligne « de »), leur texte chiffré initial est toujours le même, en supposant que les mêmes algorithmes de chiffrement et clé symétrique ont été utilisés.</span><span class="sxs-lookup"><span data-stu-id="2b635-120">For example, if messages always start with a common header (a letterhead or "From" line) their initial ciphertext would always be the same, assuming that the same cryptographic algorithm and symmetric key was used.</span></span> <span data-ttu-id="2b635-121">L’ajout d’un vecteur d’initialisation aléatoire élimine ce problème.</span><span class="sxs-lookup"><span data-stu-id="2b635-121">Adding a random initialization vector eliminates this from happening.</span></span>

</dd> <dt>

<span data-ttu-id="2b635-122"><span id="_security_inner_data_gly"></span><span id="_SECURITY_INNER_DATA_GLY"></span>**données internes**</span><span class="sxs-lookup"><span data-stu-id="2b635-122"><span id="_security_inner_data_gly"></span><span id="_SECURITY_INNER_DATA_GLY"></span>**inner data**</span></span>
</dt> <dd>

<span data-ttu-id="2b635-123">Toutes les données encodées utilisées comme message pour un autre message encodé.</span><span class="sxs-lookup"><span data-stu-id="2b635-123">Any encoded data used as the message for another encoded message.</span></span> <span data-ttu-id="2b635-124">Par exemple, un message enveloppé et sa valeur de hachage peuvent être les données internes d’un deuxième message.</span><span class="sxs-lookup"><span data-stu-id="2b635-124">For example, an enveloped message and its hash value may be the inner data for a second message.</span></span>

</dd> <dt>

<span data-ttu-id="2b635-125"><span id="_security_inner_content_gly"></span><span id="_SECURITY_INNER_CONTENT_GLY"></span>**contenu interne**</span><span class="sxs-lookup"><span data-stu-id="2b635-125"><span id="_security_inner_content_gly"></span><span id="_SECURITY_INNER_CONTENT_GLY"></span>**inner content**</span></span>
</dt> <dd>

<span data-ttu-id="2b635-126">Données améliorées, par exemple avec une signature numérique.</span><span class="sxs-lookup"><span data-stu-id="2b635-126">Data that is enhanced, such as with a digital signature.</span></span> <span data-ttu-id="2b635-127">Ce terme est principalement utilisé lors de la discussion de données améliorées dans un \# message PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="2b635-127">This term is used primarily when discussing enhanced data in a PKCS \#7 message.</span></span>

</dd> <dt>

<span data-ttu-id="2b635-128"><span id="_security_integrity_gly"></span><span id="_SECURITY_INTEGRITY_GLY"></span>**garantis**</span><span class="sxs-lookup"><span data-stu-id="2b635-128"><span id="_security_integrity_gly"></span><span id="_SECURITY_INTEGRITY_GLY"></span>**integrity**</span></span>
</dt> <dd>

<span data-ttu-id="2b635-129">L’exhaustivité et la précision d’un message après son envoi ou son stockage.</span><span class="sxs-lookup"><span data-stu-id="2b635-129">The completeness and accuracy of a message after it has been sent or stored.</span></span>

</dd> <dt>

<span data-ttu-id="2b635-130"><span id="_security_integrity_sid_gly"></span><span id="_SECURITY_INTEGRITY_SID_GLY"></span>**SID d’intégrité**</span><span class="sxs-lookup"><span data-stu-id="2b635-130"><span id="_security_integrity_sid_gly"></span><span id="_SECURITY_INTEGRITY_SID_GLY"></span>**integrity SID**</span></span>
</dt> <dd>

<span data-ttu-id="2b635-131">[*Identificateur de sécurité*](s-gly.md) (SID) qui représente un niveau d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="2b635-131">A [*security identifier*](s-gly.md) (SID) that represents an integrity level.</span></span> <span data-ttu-id="2b635-132">Un SID d’intégrité de la [*liste de contrôle d’accès système*](s-gly.md) (SACL) du descripteur de sécurité d’un objet spécifie le niveau d’intégrité de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2b635-132">An integrity SID in the [*system access control list*](s-gly.md) (SACL) of an object's security descriptor specifies the integrity level of the object.</span></span> <span data-ttu-id="2b635-133">Les SID d’intégrité d’un jeton d’accès spécifient le niveau d’intégrité du jeton.</span><span class="sxs-lookup"><span data-stu-id="2b635-133">Integrity SIDs in an access token specify the integrity level of the token.</span></span>

</dd> <dt>

<span data-ttu-id="2b635-134"><span id="_security_interrupt_request_level_gly"></span><span id="_SECURITY_INTERRUPT_REQUEST_LEVEL_GLY"></span>**NIVEAU**</span><span class="sxs-lookup"><span data-stu-id="2b635-134"><span id="_security_interrupt_request_level_gly"></span><span id="_SECURITY_INTERRUPT_REQUEST_LEVEL_GLY"></span>**IRQL**</span></span>
</dt> <dd>

<span data-ttu-id="2b635-135">Un niveau de requête d’interruption (IRQL) définit la priorité matérielle à laquelle un processeur s’exécute à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="2b635-135">An interrupt request level (IRQL) defines the hardware priority at which a processor operates at any given time.</span></span> <span data-ttu-id="2b635-136">Dans le Windows Driver Model, un thread s’exécutant à un niveau IRQL faible peut être interrompu pour exécuter du code à un niveau IRQL supérieur.</span><span class="sxs-lookup"><span data-stu-id="2b635-136">In the Windows Driver Model, a thread running at a low IRQL can be interrupted to run code at a higher IRQL.</span></span>

</dd> <dt>

<span data-ttu-id="2b635-137"><span id="_security_iv_gly"></span><span id="_SECURITY_IV_GLY"></span>**ÉVALUER**</span><span class="sxs-lookup"><span data-stu-id="2b635-137"><span id="_security_iv_gly"></span><span id="_SECURITY_IV_GLY"></span>**IV**</span></span>
</dt> <dd>

<span data-ttu-id="2b635-138">Consultez *vecteur d’initialisation*.</span><span class="sxs-lookup"><span data-stu-id="2b635-138">See *initialization vector*.</span></span>

</dd> </dl>

 

 



