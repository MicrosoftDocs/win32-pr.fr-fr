---
title: Chaînes UrlPrefix
description: Dans l’API du serveur HTTP, un UrlPrefix est une chaîne Unicode à caractères larges (UTF-16) avec une forme canonique qui spécifie une section d’espace de noms d’URL.
ms.assetid: 4f317bf6-ee6a-47a8-a531-78534217109d
keywords:
- API serveur HTTP des chaînes UrlPrefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bddc484f26bc1b3de5d20196dadec9201d3ea272
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "103734740"
---
# <a name="urlprefix-strings"></a><span data-ttu-id="09085-104">Chaînes UrlPrefix</span><span class="sxs-lookup"><span data-stu-id="09085-104">UrlPrefix Strings</span></span>

<span data-ttu-id="09085-105">Dans l’API du serveur HTTP, un *URLPrefix* est une chaîne Unicode à caractères larges (UTF-16) avec une forme canonique qui spécifie une section d’espace de noms d’URL.</span><span class="sxs-lookup"><span data-stu-id="09085-105">In the HTTP Server API, a *UrlPrefix* is a wide-character (UTF-16) Unicode string with a canonical form that specifies a section of URL namespace.</span></span> <span data-ttu-id="09085-106">Elle est utilisée pour réserver une section de l’espace de noms d’URL pour un compte d’utilisateur ou pour enregistrer une section d’espace de noms d’URL pour un processus.</span><span class="sxs-lookup"><span data-stu-id="09085-106">It is used to reserve a section of URL namespace for a user account or register a section of URL namespace for a process.</span></span>

## <a name="urlprefix-format"></a><span data-ttu-id="09085-107">Format UrlPrefix</span><span class="sxs-lookup"><span data-stu-id="09085-107">UrlPrefix Format</span></span>

<span data-ttu-id="09085-108">Un UrlPrefix a la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="09085-108">A UrlPrefix has the following syntax:</span></span>

<span data-ttu-id="09085-109">« schéma://Host : port/relativeURI »</span><span class="sxs-lookup"><span data-stu-id="09085-109">"scheme://host:port/relativeURI"</span></span>

<span data-ttu-id="09085-110">Les éléments de schéma, d’hôte et de port d’un UrlPrefix doivent être présents et non vides, et doivent respecter les règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="09085-110">The scheme, host and port elements of a UrlPrefix must be present and non-empty, and must obey the following rules:</span></span>

<dl> <dt>

<span data-ttu-id="09085-111"><span id="scheme"></span><span id="SCHEME"></span>mode</span><span class="sxs-lookup"><span data-stu-id="09085-111"><span id="scheme"></span><span id="SCHEME"></span>scheme</span></span>
</dt> <dd>

<span data-ttu-id="09085-112">Doit être http ou HTTPS, tout en minuscules.</span><span class="sxs-lookup"><span data-stu-id="09085-112">Must be either http or https, all in lowercase.</span></span>

</dd> <dt>

<span data-ttu-id="09085-113"><span id="host"></span><span id="HOST"></span>HBA</span><span class="sxs-lookup"><span data-stu-id="09085-113"><span id="host"></span><span id="HOST"></span>host</span></span>
</dt> <dd>

<span data-ttu-id="09085-114">Il doit s’agir d’un nom de domaine complet, d’une chaîne littérale IPv4 ou IPv6 ou d’un caractère générique.</span><span class="sxs-lookup"><span data-stu-id="09085-114">Must be a fully qualified domain name, an IPv4 or IPv6 literal string, or a wildcard.</span></span> <span data-ttu-id="09085-115">Contrairement au schéma, qui doit être en minuscules, la partie hôte ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="09085-115">Unlike the scheme, which must be lowercase, the host portion is case-insensitive.</span></span> <span data-ttu-id="09085-116">Selon la façon dont la partie hôte est spécifiée, un UrlPrefix se trouve dans l’une des quatre catégories de routage suivantes, qui sont décrites plus en détail ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="09085-116">Depending on how its host portion is specified, a UrlPrefix falls into one of the following four routing categories, which are described in more detail below:</span></span>

<dl> <dd><span data-ttu-id="09085-117">Caractère générique fort</span><span class="sxs-lookup"><span data-stu-id="09085-117">Strong wildcard</span></span></dd> <dd><span data-ttu-id="09085-118">Explicite</span><span class="sxs-lookup"><span data-stu-id="09085-118">Explicit</span></span></dd> <dd><span data-ttu-id="09085-119">Caractère générique faible lié à IP</span><span class="sxs-lookup"><span data-stu-id="09085-119">IP-bound weak wildcard</span></span></dd> <dd><span data-ttu-id="09085-120">Caractère générique faible</span><span class="sxs-lookup"><span data-stu-id="09085-120">Weak wildcard</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="09085-121"><span id="port"></span><span id="PORT"></span>importer</span><span class="sxs-lookup"><span data-stu-id="09085-121"><span id="port"></span><span id="PORT"></span>port</span></span>
</dt> <dd>

<span data-ttu-id="09085-122">Chaîne numérique décimale qui ne commence pas par zéro et qui représente un numéro de port TCP valide (1 à 65 535).</span><span class="sxs-lookup"><span data-stu-id="09085-122">A decimal numeric string that does not start with zero and that represents a valid TCP port number (1 to 65,535).</span></span> <span data-ttu-id="09085-123">Cette valeur ne peut pas être un caractère générique.</span><span class="sxs-lookup"><span data-stu-id="09085-123">This value cannot be a wildcard.</span></span>

</dd> <dt>

<span data-ttu-id="09085-124"><span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>relativeURI</span><span class="sxs-lookup"><span data-stu-id="09085-124"><span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>relativeURI</span></span>
</dt> <dd>

<span data-ttu-id="09085-125">L’élément relativeURI est facultatif, mais s’il est présent, il doit toujours être suivi d’une barre oblique ("/").</span><span class="sxs-lookup"><span data-stu-id="09085-125">The relativeURI element is optional, but if present must always be followed by a slash character ("/").</span></span> <span data-ttu-id="09085-126">Il s’agit d’une chaîne de préfixe qui indique une sous-arborescence au sein de l’espace de noms de l’ordinateur, spécifiée par rapport aux valeurs de schéma, d’hôte et de port.</span><span class="sxs-lookup"><span data-stu-id="09085-126">This is a prefix string that indicates a subtree within the machine's namespace specified relative to the scheme, host and port values.</span></span> <span data-ttu-id="09085-127">Contrairement au schéma, qui doit être en minuscules, la partie relativeURI ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="09085-127">Unlike the scheme, which must be lowercase, the relativeURI portion is case-insensitive.</span></span>

</dd> </dl>

<span data-ttu-id="09085-128">Voici quelques exemples de UrlPrefixes correctement formés :</span><span class="sxs-lookup"><span data-stu-id="09085-128">Examples of properly formed UrlPrefixes are:</span></span>

-   `https://www.adatum.com:80/vroot/`
-   `https://adatum.com:443/secure/database/`
-   `https://+:80/vroot/`

## <a name="host-specifier-categories"></a><span data-ttu-id="09085-129">Catégories de Host-Specifier</span><span class="sxs-lookup"><span data-stu-id="09085-129">Host-Specifier Categories</span></span>

<span data-ttu-id="09085-130">Pour une flexibilité et une facilité d’utilisation, l’API du serveur HTTP prend en charge quatre façons différentes de spécifier des hôtes.</span><span class="sxs-lookup"><span data-stu-id="09085-130">For flexibility and ease of use, the HTTP Server API supports four different ways to specify hosts.</span></span> <span data-ttu-id="09085-131">Les quatre catégories Host-specifier sont répertoriées ci-dessous par ordre de priorité :</span><span class="sxs-lookup"><span data-stu-id="09085-131">The four host-specifier categories are listed below in order of precedence:</span></span>

<dl> <dt>

<span data-ttu-id="09085-132"><span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Caractère générique fort (signe plus)</span><span class="sxs-lookup"><span data-stu-id="09085-132"><span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Strong wildcard (Plus Sign)</span></span>
</dt> <dd>

<span data-ttu-id="09085-133">Lorsque l’élément hôte d’un UrlPrefix se compose d’un seul signe plus (+), le UrlPrefix correspond à tous les noms d’hôtes possibles dans le contexte de ses éléments Scheme, port et relativeURI et est inclus dans la catégorie caractère générique forte.</span><span class="sxs-lookup"><span data-stu-id="09085-133">When the host element of a UrlPrefix consists of a single plus sign (+), the UrlPrefix matches all possible host names in the context of its scheme, port and relativeURI elements, and falls into the strong wildcard category.</span></span>

<span data-ttu-id="09085-134">Un caractère générique fort est utile lorsqu’une application doit traiter les demandes adressées à un ou plusieurs relativeURIs, quelle que soit la façon dont ces demandes arrivent sur l’ordinateur ou le site qu’elles spécifient dans leurs en-têtes d’hôte.</span><span class="sxs-lookup"><span data-stu-id="09085-134">A strong wildcard is useful when an application needs to serve requests addressed to one or more relativeURIs, regardless of how those requests arrive on the machine or what site they specify in their Host headers.</span></span> <span data-ttu-id="09085-135">Dans ce cas, l’utilisation d’un caractère générique fort vous évite de devoir spécifier une liste exhaustive des adresses hôte et/ou IP.</span><span class="sxs-lookup"><span data-stu-id="09085-135">Use of a strong wildcard in this situation avoids the need to specify an exhaustive list of host and/or IP-addresses.</span></span>

</dd> <dt>

<span data-ttu-id="09085-136"><span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>Explicitement</span><span class="sxs-lookup"><span data-stu-id="09085-136"><span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>Explicit</span></span>
</dt> <dd>

<span data-ttu-id="09085-137">Un nom d’hôte explicite, tel qu’un nom de domaine complet dans l’élément hôte, place un UrlPrefix dans la catégorie explicite.</span><span class="sxs-lookup"><span data-stu-id="09085-137">An explicit host name such as a fully qualified domain name in the host element places a UrlPrefix in the explicit category.</span></span> <span data-ttu-id="09085-138">Ce type d’élément hôte est mis en correspondance directement avec les en-têtes d’hôte des requêtes entrantes.</span><span class="sxs-lookup"><span data-stu-id="09085-138">This kind of host element is matched directly against the Host headers of incoming requests.</span></span>

<span data-ttu-id="09085-139">Les spécifications d’hôte explicites sont utiles pour les applications multisites, telles que les serveurs Web qui fournissent des contenus différents en fonction du site vers lequel la demande a été dirigée.</span><span class="sxs-lookup"><span data-stu-id="09085-139">Explicit host specifications are useful for multi-site applications such as Web servers that deliver different content depending on the site to which the request was directed.</span></span>

</dd> <dt>

<span data-ttu-id="09085-140"><span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>Caractère générique faible lié à IP</span><span class="sxs-lookup"><span data-stu-id="09085-140"><span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>IP-bound weak wildcard</span></span>
</dt> <dd>

<span data-ttu-id="09085-141">Quand une adresse IP apparaît en tant qu’élément hôte, le UrlPrefix se trouve dans la catégorie caractère générique faible liée à IP.</span><span class="sxs-lookup"><span data-stu-id="09085-141">When an IP address appears as the host element, then the UrlPrefix falls into the IP-bound Weak Wildcard category.</span></span> <span data-ttu-id="09085-142">Ce type de UrlPrefix correspond à n’importe quel nom d’hôte pour l’interface IP spécifiée avec le schéma, le port et le relativeURI spécifiés, et qui n’a pas déjà été mis en correspondance par un caractère générique fort ou un UrlPrefix explicite.</span><span class="sxs-lookup"><span data-stu-id="09085-142">This kind of UrlPrefix matches any host name for the specified IP interface with the specified scheme, port and relativeURI, and that has not already been matched by a strong-wildcard or explicit UrlPrefix.</span></span> <span data-ttu-id="09085-143">L’adresse IP prend l’une des deux formes suivantes dans l’élément hôte :</span><span class="sxs-lookup"><span data-stu-id="09085-143">The IP address takes one of two forms in the host element:</span></span>

<dl> <dt>

<span data-ttu-id="09085-144"><span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>Chaîne littérale IPv4</span><span class="sxs-lookup"><span data-stu-id="09085-144"><span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>IPv4 Literal String</span></span>
</dt> <dd>

<span data-ttu-id="09085-145">Un littéral IPv4 se compose de quatre nombres décimaux séparés par des points, chacun dans la plage 0-255, comme 192.168.0.0.</span><span class="sxs-lookup"><span data-stu-id="09085-145">An IPv4 literal consists of four dotted decimal numbers, each in the range 0-255, such as 192.168.0.0.</span></span>

</dd> <dt>

<span data-ttu-id="09085-146"><span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>Chaîne littérale IPv6</span><span class="sxs-lookup"><span data-stu-id="09085-146"><span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>IPv6 Literal String</span></span>
</dt> <dd>

<span data-ttu-id="09085-147">Une chaîne littérale IPv6 est placée entre crochets et contient des nombres hexadécimaux séparés par des signes deux-points ; par exemple :: \[ 1 \] ou \[ 3FFE : FFFF :: 6ECB : 0101 \] .</span><span class="sxs-lookup"><span data-stu-id="09085-147">An IPv6 literal string is enclosed in square brackets and contains hex numbers separated by colons; for example: \[::1\] or \[3ffe:ffff::6ECB:0101\].</span></span>

</dd> </dl>

<span data-ttu-id="09085-148">Les spécificateurs d’hôte avec caractère générique faible liés à IP sont destinés aux applications qui font varier le contenu qu’ils servent en fonction de l’itinéraire utilisé par les demandes entrantes.</span><span class="sxs-lookup"><span data-stu-id="09085-148">IP-bound weak-wildcard host specifiers are intended for applications that vary the content they serve based on the route taken by incoming requests.</span></span> <span data-ttu-id="09085-149">Ne comptez pas sur les spécificateurs d’hôte avec caractère générique faible lié à IP pour appliquer la sécurité.</span><span class="sxs-lookup"><span data-stu-id="09085-149">Do not rely on IP-bound weak-wildcard host specifiers to enforce security.</span></span>

</dd> <dt>

<span data-ttu-id="09085-150"><span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Caractère générique faible (astérisque)</span><span class="sxs-lookup"><span data-stu-id="09085-150"><span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Weak wildcard (asterisk)</span></span>
</dt> <dd>

<span data-ttu-id="09085-151">Lorsqu’un astérisque ( \* ) apparaît en tant qu’élément hôte, le URLPrefix se trouve dans la catégorie caractère générique faible.</span><span class="sxs-lookup"><span data-stu-id="09085-151">When an asterisk (\*) appears as the host element, then the UrlPrefix falls into the weak wildcard category.</span></span> <span data-ttu-id="09085-152">Ce type de UrlPrefix correspond à n’importe quel nom d’hôte associé au schéma, au port et au relativeURI spécifiés qui n’a pas déjà été mis en correspondance par un UrlPrefix avec caractères génériques forts, explicites ou avec des caractères génériques faibles liés à l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="09085-152">This kind of UrlPrefix matches any host name associated with the specified scheme, port and relativeURI that has not already been matched by a strong-wildcard, explicit, or IP-bound weak-wildcard UrlPrefix.</span></span>

<span data-ttu-id="09085-153">Cette spécification de l’hôte peut être utilisée comme valeur par défaut de rattrapage dans certaines circonstances, ou peut être utilisée pour spécifier une grande section de l’espace de noms d’URL sans avoir à utiliser de nombreux UrlPrefixes.</span><span class="sxs-lookup"><span data-stu-id="09085-153">This host specification can be used as a default catch-all in some circumstances, or can be used to specify a large section of URL namespace without having to use many UrlPrefixes.</span></span>

</dd> </dl>

## <a name="urlprefix-conflict-detection-during-reservation-and-registration"></a><span data-ttu-id="09085-154">Détection de conflit UrlPrefix pendant la réservation et l’inscription</span><span class="sxs-lookup"><span data-stu-id="09085-154">UrlPrefix Conflict Detection During Reservation and Registration</span></span>

<span data-ttu-id="09085-155">À des fins de réservation et d’enregistrement, les quatre catégories différentes de UrlPrefix sont traitées séparément, sans référence les unes aux autres.</span><span class="sxs-lookup"><span data-stu-id="09085-155">For reservation and registration purposes, the four different categories of UrlPrefix are treated separately, without reference to one another.</span></span> <span data-ttu-id="09085-156">Il est possible d’enregistrer les UrlPrefixes en conflit tant qu’ils se trouvent dans des catégories différentes.</span><span class="sxs-lookup"><span data-stu-id="09085-156">It is possible to register conflicting UrlPrefixes as long as they are in different categories.</span></span> <span data-ttu-id="09085-157">Une tentative de réservation échoue uniquement dans la même catégorie.</span><span class="sxs-lookup"><span data-stu-id="09085-157">Only within the same category does a conflict cause a reservation attempt to fail.</span></span>

<span data-ttu-id="09085-158">Par exemple, il est possible de réserver à la fois les UrlPrefix explicites `https://www.adatum.com:80/vroot/` et les URLPrefix génériques forts en conflit `https://+:80/vroot/` , car ils appartiennent à des catégories différentes.</span><span class="sxs-lookup"><span data-stu-id="09085-158">For example, it would be possible to reserve both the explicit UrlPrefix `https://www.adatum.com:80/vroot/` and the conflicting strong wildcard UrlPrefix `https://+:80/vroot/`, since they belong to different categories.</span></span> <span data-ttu-id="09085-159">Toutefois, une tentative ultérieure de réservation https://+:80/vroot/ à un autre utilisateur échoue, car elle serait en conflit avec une réservation existante dans sa propre catégorie.</span><span class="sxs-lookup"><span data-stu-id="09085-159">However, a subsequent attempt to reserve https://+:80/vroot/ to a different user would fail because it would conflict with an existing reservation in its own category.</span></span>

## <a name="routing-behavior"></a><span data-ttu-id="09085-160">Comportement de routage</span><span class="sxs-lookup"><span data-stu-id="09085-160">Routing Behavior</span></span>

<span data-ttu-id="09085-161">Lors du routage d’une requête HTTP entrante, l’API du serveur HTTP commence par la catégorie de caractères génériques forts et compare l’URL entrante avec les UrlPrefixes inscrits et réservés dans cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="09085-161">When routing an incoming HTTP request, the HTTP Server API starts with the strong wildcard category and compares the incoming URL with both registered and reserved UrlPrefixes in that category.</span></span>

<span data-ttu-id="09085-162">Si l’URL entrante correspond à une réservation mais pas à une inscription, l’API du serveur HTTP fait échouer la requête.</span><span class="sxs-lookup"><span data-stu-id="09085-162">If the incoming URL matches a reservation but not a registration, the HTTP Server API fails the request.</span></span> <span data-ttu-id="09085-163">Cela empêche les inscriptions de faible priorité d’être en mesure de récupérer les demandes qui ne sont pas prévues pour elle.</span><span class="sxs-lookup"><span data-stu-id="09085-163">This prevents a lower-priority registrations from being able to pick up requests not intended for it.</span></span> <span data-ttu-id="09085-164">L’État en cas d’échec est 400 (« requête incorrecte ») au lieu de 503 (« service non disponible »), car un retour de 503 est parfois interprété par erreur par les passerelles d’équilibrage de charge, comme indiquant que le serveur a été surchargé.</span><span class="sxs-lookup"><span data-stu-id="09085-164">The status on failure is 400 ("Bad Request") rather than 503 ("Service not available"), because a 503 return is sometimes mistakenly interpreted by load-balancing gateways as indicating that the server was overloaded.</span></span>

<span data-ttu-id="09085-165">Si une inscription correspondante est trouvée dans la catégorie, la demande est routée vers la file d’attente de demandes associée à cette inscription.</span><span class="sxs-lookup"><span data-stu-id="09085-165">If a matching registration is found within the category, the request is routed to the request queue associated with that registration.</span></span> <span data-ttu-id="09085-166">La demande est toujours routée vers la file d’attente associée aux UrlPrefix les plus longues correspondantes dans une catégorie.</span><span class="sxs-lookup"><span data-stu-id="09085-166">The request is always routed to the queue associated with the longest matching UrlPrefix within a category.</span></span>

<span data-ttu-id="09085-167">Si aucune correspondance n’est trouvée dans la catégorie, l’API du serveur HTTP passe à la catégorie explicite et répète la même procédure.</span><span class="sxs-lookup"><span data-stu-id="09085-167">If no match is found in the category, then the HTTP Server API proceeds to the explicit category and repeats the same procedure.</span></span> <span data-ttu-id="09085-168">Pour résumer, l’ordre dans lequel les catégories sont examinées est le suivant :</span><span class="sxs-lookup"><span data-stu-id="09085-168">To summarize, the order in which the categories are examined is as follows:</span></span>

1.  <span data-ttu-id="09085-169">Caractère générique fort</span><span class="sxs-lookup"><span data-stu-id="09085-169">Strong wildcard</span></span>
2.  <span data-ttu-id="09085-170">Explicite</span><span class="sxs-lookup"><span data-stu-id="09085-170">Explicit</span></span>
3.  <span data-ttu-id="09085-171">Caractère générique IP-Bound faible</span><span class="sxs-lookup"><span data-stu-id="09085-171">IP-Bound weak wildcard</span></span>
4.  <span data-ttu-id="09085-172">Caractère générique faible</span><span class="sxs-lookup"><span data-stu-id="09085-172">Weak wildcard</span></span>

<span data-ttu-id="09085-173">Si aucune correspondance n’est trouvée dans l’une des catégories, l’API du serveur HTTP envoie une réponse avec un code d’état de 400 pour indiquer que la demande ne peut pas être routée.</span><span class="sxs-lookup"><span data-stu-id="09085-173">If no match is found in any of the categories, the HTTP Server API sends a response with a status code of 400 to indicate that the request cannot be routed.</span></span>

## <a name="longest-match-rule"></a><span data-ttu-id="09085-174">Règle de correspondance la plus longue</span><span class="sxs-lookup"><span data-stu-id="09085-174">Longest Match Rule</span></span>

<span data-ttu-id="09085-175">Dans chaque catégorie UrlPrefix, l’API du serveur HTTP achemine une requête vers la file d’attente associée au UrlPrefix correspondant le plus long.</span><span class="sxs-lookup"><span data-stu-id="09085-175">Within each UrlPrefix category, HTTP Server API routes a request to the queue associated with the longest matching UrlPrefix.</span></span> <span data-ttu-id="09085-176">Par exemple, supposons que les deux UrlPrefixes suivants sont inscrits dans différentes files d’attente :</span><span class="sxs-lookup"><span data-stu-id="09085-176">For example, suppose the following two UrlPrefixes are registered to different queues:</span></span>

- `Queue1 https://www.adatum.com:80/`
- `Queue2 https://www.adatum.com:80/dir/sna/`

<span data-ttu-id="09085-177">L’API du serveur HTTP achemine une requête pour `https://www.adatum.com:80/default.htm` à attente queue1 et une demande `https://www.adatum.com:80/dir/sna/snadefault.htm` à Queue2.</span><span class="sxs-lookup"><span data-stu-id="09085-177">The HTTP Server API routes a request for `https://www.adatum.com:80/default.htm` to Queue1, and a request for `https://www.adatum.com:80/dir/sna/snadefault.htm` to Queue2.</span></span> <span data-ttu-id="09085-178">Il achemine une requête pour `https://www.adatum.com:80/dir/app.htm` à attente queue1, car la correspondance la plus longue est avec `https://www.adatum.com:80/` URLPrefix, et non avec `https://www.adatum.com:80/dir/sna` URLPrefix.</span><span class="sxs-lookup"><span data-stu-id="09085-178">It routes a request for `https://www.adatum.com:80/dir/app.htm` to Queue1 because the longest complete match is with the `https://www.adatum.com:80/` UrlPrefix, not with the `https://www.adatum.com:80/dir/sna` UrlPrefix.</span></span>

 

 




