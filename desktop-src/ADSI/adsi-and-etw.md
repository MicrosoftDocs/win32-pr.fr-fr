---
title: Suivi d’événements dans ADSI
description: Windows Server 2008 et Windows Vista introduisent le suivi d’événements dans les interfaces de service Active Directory (ADSI).
ms.assetid: 743aeeba-5b48-47c7-aaf5-0e9b48e206db
ms.tgt_platform: multiple
keywords:
- suivi d’événements (ADSI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b26aee00404f5cf97d228698f64fec804c28e62
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423710"
---
# <a name="event-tracing-in-adsi"></a><span data-ttu-id="21cde-104">Suivi d’événements dans ADSI</span><span class="sxs-lookup"><span data-stu-id="21cde-104">Event Tracing in ADSI</span></span>

<span data-ttu-id="21cde-105">Windows Server 2008 et Windows Vista introduisent [le suivi d’événements](/windows/desktop/ETW/event-tracing-portal) dans les [Interfaces de service Active Directory](active-directory-service-interfaces-adsi.md) (ADSI).</span><span class="sxs-lookup"><span data-stu-id="21cde-105">Windows Server 2008 and Windows Vista introduce [Event Tracing](/windows/desktop/ETW/event-tracing-portal) in [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI).</span></span> <span data-ttu-id="21cde-106">Certaines zones du fournisseur LDAP ADSI ont une implémentation sous-jacente qui est complexe ou qui implique une séquence d’étapes qui complique le diagnostic des problèmes.</span><span class="sxs-lookup"><span data-stu-id="21cde-106">Certain areas of the ADSI LDAP Provider have an underlying implementation that is complex or that involves a sequence of steps that makes it difficult to diagnose problems.</span></span> <span data-ttu-id="21cde-107">Pour aider les développeurs d’applications à résoudre les problèmes, le suivi d’événements a été ajouté aux domaines suivants :</span><span class="sxs-lookup"><span data-stu-id="21cde-107">To help application developers troubleshoot, Event Tracing has been added to the following areas:</span></span>

## <a name="schema-parsing-and-downloading"></a><span data-ttu-id="21cde-108">Analyse et téléchargement de schéma</span><span class="sxs-lookup"><span data-stu-id="21cde-108">Schema Parsing and Downloading</span></span>

<span data-ttu-id="21cde-109">L’interface IADs dans ADSI exige que le schéma LDAP soit mis en cache sur le client afin que les attributs puissent être correctement marshalés (comme décrit dans le [modèle de schéma ADSI](adsi-schema-model.md)).</span><span class="sxs-lookup"><span data-stu-id="21cde-109">The IADs interface in ADSI requires that the LDAP schema be cached on the client so that attributes can be marshaled correctly (as described in the [ADSI Schema Model](adsi-schema-model.md)).</span></span> <span data-ttu-id="21cde-110">Pour ce faire, ADSI charge le schéma pour chaque processus (et pour chaque serveur/domaine LDAP) dans la mémoire soit à partir d’un fichier de schéma (. SCH) qui est enregistré sur le disque local, soit en le téléchargeant à partir du serveur LDAP.</span><span class="sxs-lookup"><span data-stu-id="21cde-110">To achieve this, ADSI loads the schema for each process (and for each LDAP server/domain) into memory either from a schema (.sch) file that is saved on the local disk or by downloading it from the LDAP server.</span></span> <span data-ttu-id="21cde-111">Des processus différents sur le même ordinateur client utilisent le schéma mis en cache sur le disque, s’il est disponible et applicable.</span><span class="sxs-lookup"><span data-stu-id="21cde-111">Different processes on the same client machine use the cached schema on disk if it is available and applicable.</span></span>

<span data-ttu-id="21cde-112">Si le schéma ne peut pas être obtenu à partir du disque ou du serveur, ADSI utilise un schéma par défaut codé en dur.</span><span class="sxs-lookup"><span data-stu-id="21cde-112">If the schema cannot be obtained from the disk or the server, ADSI uses a hardcoded default schema.</span></span> <span data-ttu-id="21cde-113">Lorsque cela se produit, les attributs qui ne font pas partie de ce schéma par défaut ne peuvent pas être marshalés et ADSI retourne une erreur lors de la récupération de ces attributs.</span><span class="sxs-lookup"><span data-stu-id="21cde-113">When this occurs, attributes that are not part of this default schema cannot be marshaled and ADSI returns an error while retrieving these attributes.</span></span> <span data-ttu-id="21cde-114">Un certain nombre de facteurs peuvent être à l’origine de ce problème, y compris des problèmes d’analyse du schéma et des privilèges insuffisants pour télécharger le schéma.</span><span class="sxs-lookup"><span data-stu-id="21cde-114">A number of factors could cause this to happen, including problems in parsing the schema, and insufficient privileges to download the schema.</span></span> <span data-ttu-id="21cde-115">Il est souvent difficile de déterminer la raison pour laquelle un certain schéma par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="21cde-115">It is often difficult to determine why a certain default schema is being used.</span></span> <span data-ttu-id="21cde-116">L’utilisation du suivi d’événements dans cette zone permet de diagnostiquer plus rapidement le problème et de le résoudre.</span><span class="sxs-lookup"><span data-stu-id="21cde-116">Using Event Tracing in this area will help to more quickly diagnose the problem and fix it.</span></span>

## <a name="changing-and-setting-the-password"></a><span data-ttu-id="21cde-117">Modification et définition du mot de passe</span><span class="sxs-lookup"><span data-stu-id="21cde-117">Changing and Setting the Password</span></span>

<span data-ttu-id="21cde-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) et [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) utilisent plusieurs mécanismes pour effectuer l’opération demandée en fonction de la configuration disponible (comme décrit dans [définition et modification des mots de passe utilisateur à l’aide du fournisseur LDAP](setting-user-passwords-for-ldap-providers.md)).</span><span class="sxs-lookup"><span data-stu-id="21cde-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) and [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) employ more than one mechanism to perform the requested operation based on the available configuration (as described in [Setting and Changing User Passwords with the LDAP Provider](setting-user-passwords-for-ldap-providers.md)).</span></span> <span data-ttu-id="21cde-119">Lorsque **ChangePassword** et **SetPassword** échouent, il peut être difficile de déterminer précisément pourquoi et le suivi d’événements vous aidera à résoudre les problèmes liés à ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="21cde-119">When **ChangePassword** and **SetPassword** fail, it can be difficult to determine exactly why, and Event Tracing will help to troubleshoot problems with these methods.</span></span>

## <a name="adsi-bind-cache"></a><span data-ttu-id="21cde-120">Cache de liaison ADSI</span><span class="sxs-lookup"><span data-stu-id="21cde-120">ADSI Bind Cache</span></span>

<span data-ttu-id="21cde-121">ADSI tente de réutiliser les connexions LDAP en interne chaque fois que cela est possible (voir [mise en cache de connexion](connection-caching.md)).</span><span class="sxs-lookup"><span data-stu-id="21cde-121">ADSI internally tries to reuse LDAP connections whenever possible (see [Connection Caching](connection-caching.md)).</span></span> <span data-ttu-id="21cde-122">Lors de la résolution des problèmes, il est utile de déterminer si une nouvelle connexion a été ouverte pour la communication avec le serveur ou si une connexion existante a été utilisée.</span><span class="sxs-lookup"><span data-stu-id="21cde-122">When troubleshooting, it is useful to trace whether a new connection was opened for communication with the server or whether an existing connection was used.</span></span> <span data-ttu-id="21cde-123">Il peut également être utile pour effectuer le suivi du cycle de vie du cache de connexion (parfois appelé cache de liaison) et de sa création ou de sa fermeture, et si une référence de connexion a eu lieu.</span><span class="sxs-lookup"><span data-stu-id="21cde-123">It can also be useful to trace the lifecycle of the connection cache (sometimes referred to as the bind cache) and its creation or closure, and whether a connection referral took place.</span></span> <span data-ttu-id="21cde-124">Dans le cas d’une [liaison sans serveur](/windows/desktop/AD/serverless-binding-and-rootdse), ADSI appelle le localisateur de contrôleur de domaine pour sélectionner un serveur pour le domaine du contexte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="21cde-124">In the case of a [serverless bind](/windows/desktop/AD/serverless-binding-and-rootdse), ADSI calls the DC locator to select a server for the domain of the user's context.</span></span> <span data-ttu-id="21cde-125">ADSI gère ensuite un cache du mappage du serveur de domaine pour les connexions suivantes.</span><span class="sxs-lookup"><span data-stu-id="21cde-125">ADSI then maintains a cache of the domain-server mapping for subsequent connections.</span></span> <span data-ttu-id="21cde-126">Le suivi d’événements permet de suivre la sélection du contrôleur de périphérique et est donc utile pour résoudre les problèmes liés à la connexion.</span><span class="sxs-lookup"><span data-stu-id="21cde-126">Event Tracing helps to trace the selection of the DC, and is therefore helpful in troubleshooting connection-related issues.</span></span>

## <a name="enabling-tracing-and-starting-a-tracing-session"></a><span data-ttu-id="21cde-127">Activation du traçage et du démarrage d’une session de suivi</span><span class="sxs-lookup"><span data-stu-id="21cde-127">Enabling Tracing and Starting a Tracing Session</span></span>

<span data-ttu-id="21cde-128">Pour activer le suivi ADSI, créez la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="21cde-128">To turn on ADSI tracing, create the following registry key:</span></span>

<span data-ttu-id="21cde-129">**HKEY \_ \_Ordinateur local** \\ **système** de \\ **CurrentControlSet** \\ **services** de CurrentControlSet \\  \\ **suivi** \\ \*\*\*\* ADSI</span><span class="sxs-lookup"><span data-stu-id="21cde-129">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**_ProcessName_**</span></span>

<span data-ttu-id="21cde-130">*ProcessName* est le nom complet du processus que vous souhaitez suivre, y compris son extension (par exemple, « Svchost.exe »).</span><span class="sxs-lookup"><span data-stu-id="21cde-130">*ProcessName* is the full name of the process that you want to trace, including its extension (for example, "Svchost.exe").</span></span> <span data-ttu-id="21cde-131">En outre, vous pouvez placer une valeur facultative de type **DWORD** nommée PID dans cette clé.</span><span class="sxs-lookup"><span data-stu-id="21cde-131">In addition, you can place an optional value of type **DWORD** named PID in this key.</span></span> <span data-ttu-id="21cde-132">Il est fortement recommandé de définir cette valeur et de tracer ainsi un seul processus particulier.</span><span class="sxs-lookup"><span data-stu-id="21cde-132">It is highly recommended that you set this value and thereby trace only a particular process.</span></span> <span data-ttu-id="21cde-133">Dans le cas contraire, toutes les instances de l’application spécifiées par *ProcessName* sont tracées.</span><span class="sxs-lookup"><span data-stu-id="21cde-133">Otherwise, all instances of the application specified by *ProcessName* will be traced.</span></span>

<span data-ttu-id="21cde-134">Exécutez ensuite la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="21cde-134">Then execute the following command:</span></span>

<span data-ttu-id="21cde-135">**tracelog.exe-Start** *nom_session* **-GUID \#** _Provider \_ GUID_ **-f** *nom* **-indicateur** *traceFlags* **-Level** *TraceLevel*</span><span class="sxs-lookup"><span data-stu-id="21cde-135">**tracelog.exe -start** *sessionname* **-guid \#**_provider\_guid_ **-f** *filename* **-flag** *traceFlags* **-level** *traceLevel*</span></span>

<span data-ttu-id="21cde-136">*NomSession* est simplement un identificateur arbitraire utilisé pour étiqueter la session de suivi (vous devrez faire référence à ce nom de session ultérieurement lorsque vous arrêtez la session de suivi).</span><span class="sxs-lookup"><span data-stu-id="21cde-136">*sessionname* is simply an arbitrary identifier that is used to label the tracing session (you will need to refer to this session name later when you stop the tracing session).</span></span> <span data-ttu-id="21cde-137">Le GUID du fournisseur de suivi ADSI est « 7288c9f8-D63C-4932-A345-89d6b060174d ».</span><span class="sxs-lookup"><span data-stu-id="21cde-137">The GUID for the ADSI tracking provider is "7288c9f8-d63c-4932-a345-89d6b060174d".</span></span> <span data-ttu-id="21cde-138">*filename* spécifie le fichier journal dans lequel les événements seront écrits.</span><span class="sxs-lookup"><span data-stu-id="21cde-138">*filename* specifies the logfile to which events will be written.</span></span> <span data-ttu-id="21cde-139">*traceFlags* doit avoir l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="21cde-139">*traceFlags* should be one of the following values:</span></span>



|         <span data-ttu-id="21cde-140">Indicateur</span><span class="sxs-lookup"><span data-stu-id="21cde-140">Flag</span></span>                        |         <span data-ttu-id="21cde-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="21cde-141">Value</span></span>              |
|---------------------------------|-----------------------|
| <span data-ttu-id="21cde-142">**schéma de débogage \_**</span><span class="sxs-lookup"><span data-stu-id="21cde-142">**DEBUG\_SCHEMA**</span></span><br/>    | <span data-ttu-id="21cde-143">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21cde-143">0x00000001</span></span><br/> |
| <span data-ttu-id="21cde-144">**CHANGEPWD de débogage \_**</span><span class="sxs-lookup"><span data-stu-id="21cde-144">**DEBUG\_CHANGEPWD**</span></span><br/> | <span data-ttu-id="21cde-145">0x00000002</span><span class="sxs-lookup"><span data-stu-id="21cde-145">0x00000002</span></span><br/> |
| <span data-ttu-id="21cde-146">**déboguer \_ setpwd**</span><span class="sxs-lookup"><span data-stu-id="21cde-146">**DEBUG\_SETPWD**</span></span><br/>    | <span data-ttu-id="21cde-147">0x00000004</span><span class="sxs-lookup"><span data-stu-id="21cde-147">0x00000004</span></span><br/> |
| <span data-ttu-id="21cde-148">**BINDCACHE de débogage \_**</span><span class="sxs-lookup"><span data-stu-id="21cde-148">**DEBUG\_BINDCACHE**</span></span><br/> | <span data-ttu-id="21cde-149">0x00000008</span><span class="sxs-lookup"><span data-stu-id="21cde-149">0x00000008</span></span><br/> |



 

<span data-ttu-id="21cde-150">Ces indicateurs déterminent les méthodes [ADSI](active-directory-service-interfaces-adsi.md) qui seront suivies, en fonction du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="21cde-150">These flags determine which [ADSI](active-directory-service-interfaces-adsi.md) methods will be traced, according to the following table:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="21cde-151"><strong>DEBUG_SCHEMA</strong></span><span class="sxs-lookup"><span data-stu-id="21cde-151"><strong>DEBUG_SCHEMA</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="21cde-152">LdapGetSchema</span><span class="sxs-lookup"><span data-stu-id="21cde-152">LdapGetSchema</span></span></li>
<li><span data-ttu-id="21cde-153">GetSchemaInfoTime</span><span class="sxs-lookup"><span data-stu-id="21cde-153">GetSchemaInfoTime</span></span></li>
<li><span data-ttu-id="21cde-154">LdapReadSchemaInfoFromServer</span><span class="sxs-lookup"><span data-stu-id="21cde-154">LdapReadSchemaInfoFromServer</span></span></li>
<li><span data-ttu-id="21cde-155">ProcessSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="21cde-155">ProcessSchemaInfo</span></span></li>
<li><span data-ttu-id="21cde-156">HelperReadLdapSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="21cde-156">HelperReadLdapSchemaInfo</span></span></li>
<li><span data-ttu-id="21cde-157">ProcessClassInfoArray</span><span class="sxs-lookup"><span data-stu-id="21cde-157">ProcessClassInfoArray</span></span></li>
<li><span data-ttu-id="21cde-158">ReadSchemaInfoFromRegistry</span><span class="sxs-lookup"><span data-stu-id="21cde-158">ReadSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="21cde-159">StoreSchemaInfoFromRegistry</span><span class="sxs-lookup"><span data-stu-id="21cde-159">StoreSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="21cde-160">AttributeTypeDescription</span><span class="sxs-lookup"><span data-stu-id="21cde-160">AttributeTypeDescription</span></span></li>
<li><span data-ttu-id="21cde-161">ObjectClassDescription</span><span class="sxs-lookup"><span data-stu-id="21cde-161">ObjectClassDescription</span></span></li>
<li><span data-ttu-id="21cde-162">DITContentRuleDescription</span><span class="sxs-lookup"><span data-stu-id="21cde-162">DITContentRuleDescription</span></span></li>
<li><span data-ttu-id="21cde-163">DirectoryString</span><span class="sxs-lookup"><span data-stu-id="21cde-163">DirectoryString</span></span></li>
<li><span data-ttu-id="21cde-164">DirectoryStrings</span><span class="sxs-lookup"><span data-stu-id="21cde-164">DirectoryStrings</span></span></li>
<li><span data-ttu-id="21cde-165">DITContentRuleDescription</span><span class="sxs-lookup"><span data-stu-id="21cde-165">DITContentRuleDescription</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cde-166"><strong>DEBUG_CHANGEPWD</strong></span><span class="sxs-lookup"><span data-stu-id="21cde-166"><strong>DEBUG_CHANGEPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="21cde-167">CADsUser :: ChangePassword</span><span class="sxs-lookup"><span data-stu-id="21cde-167">CADsUser::ChangePassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cde-168"><strong>DEBUG_SETPWD</strong></span><span class="sxs-lookup"><span data-stu-id="21cde-168"><strong>DEBUG_SETPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="21cde-169">CADsUser :: SetPassword</span><span class="sxs-lookup"><span data-stu-id="21cde-169">CADsUser::SetPassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cde-170"><strong>DEBUG_BINDCACHE</strong></span><span class="sxs-lookup"><span data-stu-id="21cde-170"><strong>DEBUG_BINDCACHE</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="21cde-171">GetServerBasedObject</span><span class="sxs-lookup"><span data-stu-id="21cde-171">GetServerBasedObject</span></span></li>
<li><span data-ttu-id="21cde-172">GetServerLessBasedObject</span><span class="sxs-lookup"><span data-stu-id="21cde-172">GetServerLessBasedObject</span></span></li>
<li><span data-ttu-id="21cde-173">GetGCDomainName</span><span class="sxs-lookup"><span data-stu-id="21cde-173">GetGCDomainName</span></span></li>
<li><span data-ttu-id="21cde-174">GetDefaultDomainName</span><span class="sxs-lookup"><span data-stu-id="21cde-174">GetDefaultDomainName</span></span></li>
<li><span data-ttu-id="21cde-175">GetUserDomainFlatName</span><span class="sxs-lookup"><span data-stu-id="21cde-175">GetUserDomainFlatName</span></span></li>
<li><span data-ttu-id="21cde-176">BindCacheLookup</span><span class="sxs-lookup"><span data-stu-id="21cde-176">BindCacheLookup</span></span></li>
<li><span data-ttu-id="21cde-177">EquivalentPortNumbers</span><span class="sxs-lookup"><span data-stu-id="21cde-177">EquivalentPortNumbers</span></span></li>
<li><span data-ttu-id="21cde-178">CanCredentialsBeReused</span><span class="sxs-lookup"><span data-stu-id="21cde-178">CanCredentialsBeReused</span></span></li>
<li><span data-ttu-id="21cde-179">BindCacheAdd</span><span class="sxs-lookup"><span data-stu-id="21cde-179">BindCacheAdd</span></span></li>
<li><span data-ttu-id="21cde-180">BindCacheAddRef</span><span class="sxs-lookup"><span data-stu-id="21cde-180">BindCacheAddRef</span></span></li>
<li><span data-ttu-id="21cde-181">AddReferralLink</span><span class="sxs-lookup"><span data-stu-id="21cde-181">AddReferralLink</span></span></li>
<li><span data-ttu-id="21cde-182">CommonRemoveEntry</span><span class="sxs-lookup"><span data-stu-id="21cde-182">CommonRemoveEntry</span></span></li>
<li><span data-ttu-id="21cde-183">BindCacheDerefHelper</span><span class="sxs-lookup"><span data-stu-id="21cde-183">BindCacheDerefHelper</span></span></li>
<li><span data-ttu-id="21cde-184">NotifyNewConnection</span><span class="sxs-lookup"><span data-stu-id="21cde-184">NotifyNewConnection</span></span></li>
<li><span data-ttu-id="21cde-185">QueryForConnection</span><span class="sxs-lookup"><span data-stu-id="21cde-185">QueryForConnection</span></span></li>
<li><span data-ttu-id="21cde-186">LdapOpenBindWithCredentials</span><span class="sxs-lookup"><span data-stu-id="21cde-186">LdapOpenBindWithCredentials</span></span></li>
<li><span data-ttu-id="21cde-187">LdapOpenBindWithDefaultCredentials</span><span class="sxs-lookup"><span data-stu-id="21cde-187">LdapOpenBindWithDefaultCredentials</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="21cde-188">Vous pouvez combiner des indicateurs en combinant les bits appropriés dans l’argument *traceFlags* .</span><span class="sxs-lookup"><span data-stu-id="21cde-188">You can combine flags by combining the appropriate bits in the *traceFlags* argument.</span></span> <span data-ttu-id="21cde-189">Par exemple, pour spécifier le **\_ schéma de débogage** et **déboguer les indicateurs \_ BINDCACHE** , la valeur *traceFlags* appropriée est 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="21cde-189">For example, to specify the **DEBUG\_SCHEMA** and **DEBUG\_BINDCACHE** flags, the appropriate *traceFlags* value would be 0x00000009.</span></span>

<span data-ttu-id="21cde-190">Enfin, l’indicateur *TraceLevel* doit avoir l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="21cde-190">Finally, the *traceLevel* flag should be one of the following values:</span></span>



|      <span data-ttu-id="21cde-191">Indicateur</span><span class="sxs-lookup"><span data-stu-id="21cde-191">Flag</span></span>                                    |       <span data-ttu-id="21cde-192">Valeur</span><span class="sxs-lookup"><span data-stu-id="21cde-192">Value</span></span>                |
|------------------------------------------|-----------------------|
| <span data-ttu-id="21cde-193">**\_erreur au niveau de la trace \_**</span><span class="sxs-lookup"><span data-stu-id="21cde-193">**TRACE\_LEVEL\_ERROR**</span></span><br/>       | <span data-ttu-id="21cde-194">0x00000002</span><span class="sxs-lookup"><span data-stu-id="21cde-194">0x00000002</span></span><br/> |
| <span data-ttu-id="21cde-195">**\_informations sur le niveau de suivi \_**</span><span class="sxs-lookup"><span data-stu-id="21cde-195">**TRACE\_LEVEL\_INFORMATION**</span></span><br/> | <span data-ttu-id="21cde-196">0x00000004</span><span class="sxs-lookup"><span data-stu-id="21cde-196">0x00000004</span></span><br/> |



 

<span data-ttu-id="21cde-197">**Trace \_ Les \_ informations de niveau** entraînent l’enregistrement de tous les événements par le processus de suivi, tandis que le suivi de l' **\_ \_ erreur** entraîne l’enregistrement des événements d’erreur par le processus de suivi.</span><span class="sxs-lookup"><span data-stu-id="21cde-197">**TRACE\_LEVEL\_INFORMATION** causes the tracing process to record all events, whereas **TRACE\_LEVEL\_ERROR** causes the tracing process to record only error events.</span></span>

<span data-ttu-id="21cde-198">Pour terminer le suivi, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="21cde-198">To terminate tracing, run the following command:</span></span>

<span data-ttu-id="21cde-199">**tracelog.exe-Stop** *nom_session*</span><span class="sxs-lookup"><span data-stu-id="21cde-199">**tracelog.exe -stop** *sessionname*</span></span>

<span data-ttu-id="21cde-200">Dans l’exemple précédent, *NomSession* est le même nom que celui fourni avec la commande qui a démarré la section de suivi.</span><span class="sxs-lookup"><span data-stu-id="21cde-200">In the previous example, *sessionname* is the same name as the one that was provided with the command that started the tracing section.</span></span>

## <a name="remarks"></a><span data-ttu-id="21cde-201">Remarques</span><span class="sxs-lookup"><span data-stu-id="21cde-201">Remarks</span></span>

<span data-ttu-id="21cde-202">Il est plus efficace de suivre uniquement des processus spécifiques en spécifiant un PID particulier pour suivre tous les processus sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="21cde-202">It is more effective to trace only specific processes by specifying a particular PID than to trace all processes on a computer.</span></span> <span data-ttu-id="21cde-203">Si vous avez besoin d’effectuer le suivi de plusieurs applications sur le même ordinateur, il peut y avoir un impact sur les performances. Il y a une sortie de débogage substantielle dans les sections orientées performance du code.</span><span class="sxs-lookup"><span data-stu-id="21cde-203">If you do need to trace multiple applications on the same machine, there might be a performance impact; there is substantial debugging output in performance-oriented sections of the code.</span></span> <span data-ttu-id="21cde-204">En outre, les administrateurs doivent veiller à définir correctement les autorisations des fichiers journaux lors du suivi de plusieurs processus. dans le cas contraire, n’importe quel utilisateur peut être en mesure de lire les journaux de suivi, et les autres utilisateurs pourront suivre les processus qui contiennent des informations sécurisées.</span><span class="sxs-lookup"><span data-stu-id="21cde-204">Also, administrators must be careful to properly set the permissions of the log files when tracing multiple processes; otherwise, any user might be able to read the tracing logs, and other users will be able to trace processes that contain secure information.</span></span>

<span data-ttu-id="21cde-205">Par exemple, supposons que l’administrateur configure le suivi pour une application « Test.exe » et ne spécifie pas un PID dans le registre pour suivre plusieurs instances du processus.</span><span class="sxs-lookup"><span data-stu-id="21cde-205">For example, presume the administrator sets up tracing for an application "Test.exe", and does not specify a PID in the registry to trace multiple instances of the process.</span></span> <span data-ttu-id="21cde-206">À présent, un autre utilisateur souhaite suivre l’application « Secure.exe ».</span><span class="sxs-lookup"><span data-stu-id="21cde-206">Now another user wants to trace the application "Secure.exe".</span></span> <span data-ttu-id="21cde-207">Si les fichiers journaux de suivi ne sont pas correctement restreints, il suffit à l’utilisateur de renommer « Secure.exe » en « Test.exe », et il sera suivi.</span><span class="sxs-lookup"><span data-stu-id="21cde-207">If the tracing log files are not properly restricted, all that user needs to do is rename "Secure.exe" to "Test.exe", and it will be traced.</span></span> <span data-ttu-id="21cde-208">En général, il est préférable de suivre uniquement des processus spécifiques pendant la résolution des problèmes et de supprimer la clé de registre de suivi dès que le dépannage est terminé.</span><span class="sxs-lookup"><span data-stu-id="21cde-208">In general, it is best to trace only specific processes while troubleshooting, and to remove the tracing registry key as soon as troubleshooting is done.</span></span>

<span data-ttu-id="21cde-209">Étant donné que l’activation du suivi d’événements génère des fichiers journaux supplémentaires, les administrateurs doivent surveiller attentivement les tailles des fichiers journaux. un manque d’espace disque sur l’ordinateur local peut provoquer un déni de service.</span><span class="sxs-lookup"><span data-stu-id="21cde-209">Since enabling Event Tracing will produce extra log files, administrators should carefully monitor log file sizes; lack of disk space on the local computer can cause a denial-of-service.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="21cde-210">Exemples de scénarios</span><span class="sxs-lookup"><span data-stu-id="21cde-210">Example Scenarios</span></span>

<span data-ttu-id="21cde-211">Scénario 1 : l’administrateur voit une erreur inattendue dans une application qui définit des mots de passe pour les comptes d’utilisateur. par conséquent, ils prennent les mesures suivantes pour résoudre le problème à l’aide du suivi d’événements.</span><span class="sxs-lookup"><span data-stu-id="21cde-211">Scenario 1: The administrator sees an unexpected error in an application that sets passwords for user accounts, so they would take the following steps to fix the problem using Event Tracing.</span></span>

1.  <span data-ttu-id="21cde-212">Écrire un script qui reproduit le problème et créer la clé de Registre</span><span class="sxs-lookup"><span data-stu-id="21cde-212">Write a script that reproduces the problem, and create the registry key</span></span>

    <span data-ttu-id="21cde-213">**HKEY \_ \_** \\  \\  \\  \\  \\ **Suivi** ADSI des services \\ \*\*\*\* de CurrentControlSet de système d’ordinateur localcscript.exe</span><span class="sxs-lookup"><span data-stu-id="21cde-213">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

2.  <span data-ttu-id="21cde-214">Démarrez une session de suivi, en affectant à *traceFlags* la valeur 0X2 (**Déboguer \_ CHANGEPASSWD**) et *TraceLevel* à 0x4 (**informations de \_ niveau \_ de suivi**), à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="21cde-214">Start a tracing session, setting *traceFlags* to 0x2 (**DEBUG\_CHANGEPASSWD**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**), using the following command:</span></span>

    <span data-ttu-id="21cde-215">**tracelog.exe-Start scripttrace-GUID \# 7288c9f8-D63C-4932-A345-89d6b060174d-f. \\ ADSI. etl-indicateur 0X2-niveau 0x4**</span><span class="sxs-lookup"><span data-stu-id="21cde-215">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

3.  <span data-ttu-id="21cde-216">Exécutez cscript.exe avec le script de test pour reproduire le problème, puis terminez la session de suivi :</span><span class="sxs-lookup"><span data-stu-id="21cde-216">Run cscript.exe with their test script to reproduce the problem, and then terminate the tracing session:</span></span>

    <span data-ttu-id="21cde-217">**tracelog.exe-arrêter scripttrace**</span><span class="sxs-lookup"><span data-stu-id="21cde-217">**tracelog.exe -stop scripttrace**</span></span>

4.  <span data-ttu-id="21cde-218">Supprimer la clé de Registre</span><span class="sxs-lookup"><span data-stu-id="21cde-218">Delete the registry key</span></span>

    <span data-ttu-id="21cde-219">**HKEY \_ \_** \\  \\  \\  \\  \\ **Suivi** ADSI des services \\ \*\*\*\* de CurrentControlSet de système d’ordinateur localcscript.exe</span><span class="sxs-lookup"><span data-stu-id="21cde-219">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

5.  <span data-ttu-id="21cde-220">Exécutez l’outil ETW Tracerpt.exe pour analyser les informations de suivi du journal :</span><span class="sxs-lookup"><span data-stu-id="21cde-220">Run the ETW tool Tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="21cde-221">**tracelog.exe-Start scripttrace-GUID \# 7288c9f8-D63C-4932-A345-89d6b060174d-f. \\ ADSI. etl-indicateur 0X2-niveau 0x4**</span><span class="sxs-lookup"><span data-stu-id="21cde-221">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

<span data-ttu-id="21cde-222">Scénario 2 : l’administrateur souhaite suivre les opérations d’analyse et de téléchargement du schéma dans une application [asp](https://msdn.microsoft.com/asp.net/default.aspx) nommée w3wp.exe qui est déjà en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="21cde-222">Scenario 2: The administrator wants to trace the schema parsing and download operations in an [ASP](https://msdn.microsoft.com/asp.net/default.aspx) application named w3wp.exe that is already running.</span></span> <span data-ttu-id="21cde-223">Pour ce faire, l’administrateur doit effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="21cde-223">To do this, the administrator would take the following steps:</span></span>

1.  <span data-ttu-id="21cde-224">Créer la clé de Registre</span><span class="sxs-lookup"><span data-stu-id="21cde-224">Create the registry key</span></span>

    <span data-ttu-id="21cde-225">**HKEY \_ \_** \\  \\  \\  \\  \\ **Suivi** ADSI des services \\ \*\*\*\* de CurrentControlSet de système d’ordinateur localw3wp.exe</span><span class="sxs-lookup"><span data-stu-id="21cde-225">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**</span></span>

    <span data-ttu-id="21cde-226">et à l’intérieur de cette clé, créez une valeur de type DWORD nommée PID et affectez-lui l’ID de processus de l’instance de w3wp.exe en cours d’exécution sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="21cde-226">and inside that key, create a value of type DWORD that is named PID and set it to the process ID of the instance of w3wp.exe that is currently running on the local computer.</span></span>

2.  <span data-ttu-id="21cde-227">Ensuite, ils créent une session de suivi, en affectant à *traceFlags* la valeur 0x1 (**\_ schéma de débogage**) et *TraceLevel* à 0x4 (**\_ \_ informations de niveau de suivi**) :</span><span class="sxs-lookup"><span data-stu-id="21cde-227">Then they create a tracing session, setting *traceFlags* to 0x1 (**DEBUG\_SCHEMA**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**):</span></span>

    <span data-ttu-id="21cde-228">**tracelog.exe-Start w3wptrace-GUID \# 7288c9f8-D63C-4932-A345-89d6b060174d-f. \\ w3wp. etl-indicateur 0x1-niveau 0x4**</span><span class="sxs-lookup"><span data-stu-id="21cde-228">**tracelog.exe -start w3wptrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\w3wp.etl -flag 0x1 -level 0x4**</span></span>

3.  <span data-ttu-id="21cde-229">Reproduisez l’opération qui nécessite un dépannage.</span><span class="sxs-lookup"><span data-stu-id="21cde-229">Reproduce the operation that needs troubleshooting.</span></span>
4.  <span data-ttu-id="21cde-230">Mettre fin à la session de suivi :</span><span class="sxs-lookup"><span data-stu-id="21cde-230">Terminate the tracing session:</span></span>

    <span data-ttu-id="21cde-231">**tracelog.exe-arrêter w3wptrace**</span><span class="sxs-lookup"><span data-stu-id="21cde-231">**tracelog.exe -stop w3wptrace**</span></span>

5.  <span data-ttu-id="21cde-232">Supprimez la clé de Registre **HKEY \_ local \_ machine** \\ **System** \\ **CurrentControlSet** \\ **service** \\ **ADSI** \\ **Tracing** \\ **w3wp.exe**.</span><span class="sxs-lookup"><span data-stu-id="21cde-232">Delete the registry key **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**.</span></span>
6.  <span data-ttu-id="21cde-233">Exécutez l’outil ETW tracerpt.exe pour analyser les informations de suivi du journal :</span><span class="sxs-lookup"><span data-stu-id="21cde-233">Run the ETW tool tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="21cde-234">**tracerpt.exe. \\ w3wp. etl-o-Report**</span><span class="sxs-lookup"><span data-stu-id="21cde-234">**tracerpt.exe .\\w3wp.etl -o -report**</span></span>

 

