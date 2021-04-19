---
title: Suivi d’événements dans ADSI
description: Windows Server 2008 et Windows Vista introduisent le suivi d’événements dans les interfaces de service Active Directory (ADSI).
ms.assetid: 743aeeba-5b48-47c7-aaf5-0e9b48e206db
ms.tgt_platform: multiple
keywords:
- suivi d’événements (ADSI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f43c0d840cd1f3f70d293a0a4f5c299fd129efe
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106510705"
---
# <a name="event-tracing-in-adsi"></a><span data-ttu-id="15881-104">Suivi d’événements dans ADSI</span><span class="sxs-lookup"><span data-stu-id="15881-104">Event Tracing in ADSI</span></span>

<span data-ttu-id="15881-105">Windows Server 2008 et Windows Vista introduisent [le suivi d’événements](/windows/desktop/ETW/event-tracing-portal) dans les [Interfaces de service Active Directory](active-directory-service-interfaces-adsi.md) (ADSI).</span><span class="sxs-lookup"><span data-stu-id="15881-105">Windows Server 2008 and Windows Vista introduce [Event Tracing](/windows/desktop/ETW/event-tracing-portal) in [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI).</span></span> <span data-ttu-id="15881-106">Certaines zones du fournisseur LDAP ADSI ont une implémentation sous-jacente qui est complexe ou qui implique une séquence d’étapes qui complique le diagnostic des problèmes.</span><span class="sxs-lookup"><span data-stu-id="15881-106">Certain areas of the ADSI LDAP Provider have an underlying implementation that is complex or that involves a sequence of steps that makes it difficult to diagnose problems.</span></span> <span data-ttu-id="15881-107">Pour aider les développeurs d’applications à résoudre les problèmes, le suivi d’événements a été ajouté aux domaines suivants :</span><span class="sxs-lookup"><span data-stu-id="15881-107">To help application developers troubleshoot, Event Tracing has been added to the following areas:</span></span>

## <a name="schema-parsing-and-downloading"></a><span data-ttu-id="15881-108">Analyse et téléchargement de schéma</span><span class="sxs-lookup"><span data-stu-id="15881-108">Schema Parsing and Downloading</span></span>

<span data-ttu-id="15881-109">L’interface IADs dans ADSI exige que le schéma LDAP soit mis en cache sur le client afin que les attributs puissent être correctement marshalés (comme décrit dans le [modèle de schéma ADSI](adsi-schema-model.md)).</span><span class="sxs-lookup"><span data-stu-id="15881-109">The IADs interface in ADSI requires that the LDAP schema be cached on the client so that attributes can be marshaled correctly (as described in the [ADSI Schema Model](adsi-schema-model.md)).</span></span> <span data-ttu-id="15881-110">Pour ce faire, ADSI charge le schéma pour chaque processus (et pour chaque serveur/domaine LDAP) dans la mémoire soit à partir d’un fichier de schéma (. SCH) qui est enregistré sur le disque local, soit en le téléchargeant à partir du serveur LDAP.</span><span class="sxs-lookup"><span data-stu-id="15881-110">To achieve this, ADSI loads the schema for each process (and for each LDAP server/domain) into memory either from a schema (.sch) file that is saved on the local disk or by downloading it from the LDAP server.</span></span> <span data-ttu-id="15881-111">Des processus différents sur le même ordinateur client utilisent le schéma mis en cache sur le disque, s’il est disponible et applicable.</span><span class="sxs-lookup"><span data-stu-id="15881-111">Different processes on the same client machine use the cached schema on disk if it is available and applicable.</span></span>

<span data-ttu-id="15881-112">Si le schéma ne peut pas être obtenu à partir du disque ou du serveur, ADSI utilise un schéma par défaut codé en dur.</span><span class="sxs-lookup"><span data-stu-id="15881-112">If the schema cannot be obtained from the disk or the server, ADSI uses a hardcoded default schema.</span></span> <span data-ttu-id="15881-113">Lorsque cela se produit, les attributs qui ne font pas partie de ce schéma par défaut ne peuvent pas être marshalés et ADSI retourne une erreur lors de la récupération de ces attributs.</span><span class="sxs-lookup"><span data-stu-id="15881-113">When this occurs, attributes that are not part of this default schema cannot be marshaled and ADSI returns an error while retrieving these attributes.</span></span> <span data-ttu-id="15881-114">Un certain nombre de facteurs peuvent être à l’origine de ce problème, y compris des problèmes d’analyse du schéma et des privilèges insuffisants pour télécharger le schéma.</span><span class="sxs-lookup"><span data-stu-id="15881-114">A number of factors could cause this to happen, including problems in parsing the schema, and insufficient privileges to download the schema.</span></span> <span data-ttu-id="15881-115">Il est souvent difficile de déterminer la raison pour laquelle un certain schéma par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="15881-115">It is often difficult to determine why a certain default schema is being used.</span></span> <span data-ttu-id="15881-116">L’utilisation du suivi d’événements dans cette zone permet de diagnostiquer plus rapidement le problème et de le résoudre.</span><span class="sxs-lookup"><span data-stu-id="15881-116">Using Event Tracing in this area will help to more quickly diagnose the problem and fix it.</span></span>

## <a name="changing-and-setting-the-password"></a><span data-ttu-id="15881-117">Modification et définition du mot de passe</span><span class="sxs-lookup"><span data-stu-id="15881-117">Changing and Setting the Password</span></span>

<span data-ttu-id="15881-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) et [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) utilisent plusieurs mécanismes pour effectuer l’opération demandée en fonction de la configuration disponible (comme décrit dans [définition et modification des mots de passe utilisateur à l’aide du fournisseur LDAP](setting-user-passwords-for-ldap-providers.md)).</span><span class="sxs-lookup"><span data-stu-id="15881-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) and [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) employ more than one mechanism to perform the requested operation based on the available configuration (as described in [Setting and Changing User Passwords with the LDAP Provider](setting-user-passwords-for-ldap-providers.md)).</span></span> <span data-ttu-id="15881-119">Lorsque **ChangePassword** et **SetPassword** échouent, il peut être difficile de déterminer précisément pourquoi et le suivi d’événements vous aidera à résoudre les problèmes liés à ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="15881-119">When **ChangePassword** and **SetPassword** fail, it can be difficult to determine exactly why, and Event Tracing will help to troubleshoot problems with these methods.</span></span>

## <a name="adsi-bind-cache"></a><span data-ttu-id="15881-120">Cache de liaison ADSI</span><span class="sxs-lookup"><span data-stu-id="15881-120">ADSI Bind Cache</span></span>

<span data-ttu-id="15881-121">ADSI tente de réutiliser les connexions LDAP en interne chaque fois que cela est possible (voir [mise en cache de connexion](connection-caching.md)).</span><span class="sxs-lookup"><span data-stu-id="15881-121">ADSI internally tries to reuse LDAP connections whenever possible (see [Connection Caching](connection-caching.md)).</span></span> <span data-ttu-id="15881-122">Lors de la résolution des problèmes, il est utile de déterminer si une nouvelle connexion a été ouverte pour la communication avec le serveur ou si une connexion existante a été utilisée.</span><span class="sxs-lookup"><span data-stu-id="15881-122">When troubleshooting, it is useful to trace whether a new connection was opened for communication with the server or whether an existing connection was used.</span></span> <span data-ttu-id="15881-123">Il peut également être utile pour effectuer le suivi du cycle de vie du cache de connexion (parfois appelé cache de liaison) et de sa création ou de sa fermeture, et si une référence de connexion a eu lieu.</span><span class="sxs-lookup"><span data-stu-id="15881-123">It can also be useful to trace the lifecycle of the connection cache (sometimes referred to as the bind cache) and its creation or closure, and whether a connection referral took place.</span></span> <span data-ttu-id="15881-124">Dans le cas d’une [liaison sans serveur](/windows/desktop/AD/serverless-binding-and-rootdse), ADSI appelle le localisateur de contrôleur de domaine pour sélectionner un serveur pour le domaine du contexte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="15881-124">In the case of a [serverless bind](/windows/desktop/AD/serverless-binding-and-rootdse), ADSI calls the DC locator to select a server for the domain of the user's context.</span></span> <span data-ttu-id="15881-125">ADSI gère ensuite un cache du mappage du serveur de domaine pour les connexions suivantes.</span><span class="sxs-lookup"><span data-stu-id="15881-125">ADSI then maintains a cache of the domain-server mapping for subsequent connections.</span></span> <span data-ttu-id="15881-126">Le suivi d’événements permet de suivre la sélection du contrôleur de périphérique et est donc utile pour résoudre les problèmes liés à la connexion.</span><span class="sxs-lookup"><span data-stu-id="15881-126">Event Tracing helps to trace the selection of the DC, and is therefore helpful in troubleshooting connection-related issues.</span></span>

## <a name="enabling-tracing-and-starting-a-tracing-session"></a><span data-ttu-id="15881-127">Activation du traçage et du démarrage d’une session de suivi</span><span class="sxs-lookup"><span data-stu-id="15881-127">Enabling Tracing and Starting a Tracing Session</span></span>

<span data-ttu-id="15881-128">Pour activer le suivi ADSI, créez la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="15881-128">To turn on ADSI tracing, create the following registry key:</span></span>

<span data-ttu-id="15881-129">**HKEY \_ \_Ordinateur local** \\ **système** de \\ **CurrentControlSet** \\ **services** de CurrentControlSet \\  \\ **suivi** \\  ADSI</span><span class="sxs-lookup"><span data-stu-id="15881-129">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\***ProcessName***</span></span>

<span data-ttu-id="15881-130">*ProcessName* est le nom complet du processus que vous souhaitez suivre, y compris son extension (par exemple, « Svchost.exe »).</span><span class="sxs-lookup"><span data-stu-id="15881-130">*ProcessName* is the full name of the process that you want to trace, including its extension (for example, "Svchost.exe").</span></span> <span data-ttu-id="15881-131">En outre, vous pouvez placer une valeur facultative de type **DWORD** nommée PID dans cette clé.</span><span class="sxs-lookup"><span data-stu-id="15881-131">In addition, you can place an optional value of type **DWORD** named PID in this key.</span></span> <span data-ttu-id="15881-132">Il est fortement recommandé de définir cette valeur et de tracer ainsi un seul processus particulier.</span><span class="sxs-lookup"><span data-stu-id="15881-132">It is highly recommended that you set this value and thereby trace only a particular process.</span></span> <span data-ttu-id="15881-133">Dans le cas contraire, toutes les instances de l’application spécifiées par *ProcessName* sont tracées.</span><span class="sxs-lookup"><span data-stu-id="15881-133">Otherwise, all instances of the application specified by *ProcessName* will be traced.</span></span>

<span data-ttu-id="15881-134">Exécutez ensuite la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="15881-134">Then execute the following command:</span></span>

<span data-ttu-id="15881-135">**tracelog.exe-Start** *nom_session*  \* *-GUID \# \* \* \* \_ GUID du fournisseur* **-f** *NomFichier* **-indicateur** *traceFlags* **-Level** *TraceLevel*</span><span class="sxs-lookup"><span data-stu-id="15881-135">**tracelog.exe -start** *sessionname* \**-guid \#\*\*\*provider\_guid* **-f** *filename* **-flag** *traceFlags* **-level** *traceLevel*</span></span>

<span data-ttu-id="15881-136">*NomSession* est simplement un identificateur arbitraire utilisé pour étiqueter la session de suivi (vous devrez faire référence à ce nom de session ultérieurement lorsque vous arrêtez la session de suivi).</span><span class="sxs-lookup"><span data-stu-id="15881-136">*sessionname* is simply an arbitrary identifier that is used to label the tracing session (you will need to refer to this session name later when you stop the tracing session).</span></span> <span data-ttu-id="15881-137">Le GUID du fournisseur de suivi ADSI est « 7288c9f8-D63C-4932-A345-89d6b060174d ».</span><span class="sxs-lookup"><span data-stu-id="15881-137">The GUID for the ADSI tracking provider is "7288c9f8-d63c-4932-a345-89d6b060174d".</span></span> <span data-ttu-id="15881-138">*filename* spécifie le fichier journal dans lequel les événements seront écrits.</span><span class="sxs-lookup"><span data-stu-id="15881-138">*filename* specifies the logfile to which events will be written.</span></span> <span data-ttu-id="15881-139">*traceFlags* doit avoir l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="15881-139">*traceFlags* should be one of the following values:</span></span>



|                                 |                       |
|---------------------------------|-----------------------|
| <span data-ttu-id="15881-140">**schéma de débogage \_**</span><span class="sxs-lookup"><span data-stu-id="15881-140">**DEBUG\_SCHEMA**</span></span><br/>    | <span data-ttu-id="15881-141">0x00000001</span><span class="sxs-lookup"><span data-stu-id="15881-141">0x00000001</span></span><br/> |
| <span data-ttu-id="15881-142">**CHANGEPWD de débogage \_**</span><span class="sxs-lookup"><span data-stu-id="15881-142">**DEBUG\_CHANGEPWD**</span></span><br/> | <span data-ttu-id="15881-143">0x00000002</span><span class="sxs-lookup"><span data-stu-id="15881-143">0x00000002</span></span><br/> |
| <span data-ttu-id="15881-144">**déboguer \_ setpwd**</span><span class="sxs-lookup"><span data-stu-id="15881-144">**DEBUG\_SETPWD**</span></span><br/>    | <span data-ttu-id="15881-145">0x00000004</span><span class="sxs-lookup"><span data-stu-id="15881-145">0x00000004</span></span><br/> |
| <span data-ttu-id="15881-146">**BINDCACHE de débogage \_**</span><span class="sxs-lookup"><span data-stu-id="15881-146">**DEBUG\_BINDCACHE**</span></span><br/> | <span data-ttu-id="15881-147">0x00000008</span><span class="sxs-lookup"><span data-stu-id="15881-147">0x00000008</span></span><br/> |



 

<span data-ttu-id="15881-148">Ces indicateurs déterminent les méthodes [ADSI](active-directory-service-interfaces-adsi.md) qui seront suivies, en fonction du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="15881-148">These flags determine which [ADSI](active-directory-service-interfaces-adsi.md) methods will be traced, according to the following table:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="15881-149"><strong>DEBUG_SCHEMA</strong></span><span class="sxs-lookup"><span data-stu-id="15881-149"><strong>DEBUG_SCHEMA</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="15881-150">LdapGetSchema</span><span class="sxs-lookup"><span data-stu-id="15881-150">LdapGetSchema</span></span></li>
<li><span data-ttu-id="15881-151">GetSchemaInfoTime</span><span class="sxs-lookup"><span data-stu-id="15881-151">GetSchemaInfoTime</span></span></li>
<li><span data-ttu-id="15881-152">LdapReadSchemaInfoFromServer</span><span class="sxs-lookup"><span data-stu-id="15881-152">LdapReadSchemaInfoFromServer</span></span></li>
<li><span data-ttu-id="15881-153">ProcessSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="15881-153">ProcessSchemaInfo</span></span></li>
<li><span data-ttu-id="15881-154">HelperReadLdapSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="15881-154">HelperReadLdapSchemaInfo</span></span></li>
<li><span data-ttu-id="15881-155">ProcessClassInfoArray</span><span class="sxs-lookup"><span data-stu-id="15881-155">ProcessClassInfoArray</span></span></li>
<li><span data-ttu-id="15881-156">ReadSchemaInfoFromRegistry</span><span class="sxs-lookup"><span data-stu-id="15881-156">ReadSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="15881-157">StoreSchemaInfoFromRegistry</span><span class="sxs-lookup"><span data-stu-id="15881-157">StoreSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="15881-158">AttributeTypeDescription</span><span class="sxs-lookup"><span data-stu-id="15881-158">AttributeTypeDescription</span></span></li>
<li><span data-ttu-id="15881-159">ObjectClassDescription</span><span class="sxs-lookup"><span data-stu-id="15881-159">ObjectClassDescription</span></span></li>
<li><span data-ttu-id="15881-160">DITContentRuleDescription</span><span class="sxs-lookup"><span data-stu-id="15881-160">DITContentRuleDescription</span></span></li>
<li><span data-ttu-id="15881-161">DirectoryString</span><span class="sxs-lookup"><span data-stu-id="15881-161">DirectoryString</span></span></li>
<li><span data-ttu-id="15881-162">DirectoryStrings</span><span class="sxs-lookup"><span data-stu-id="15881-162">DirectoryStrings</span></span></li>
<li><span data-ttu-id="15881-163">DITContentRuleDescription</span><span class="sxs-lookup"><span data-stu-id="15881-163">DITContentRuleDescription</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15881-164"><strong>DEBUG_CHANGEPWD</strong></span><span class="sxs-lookup"><span data-stu-id="15881-164"><strong>DEBUG_CHANGEPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="15881-165">CADsUser :: ChangePassword</span><span class="sxs-lookup"><span data-stu-id="15881-165">CADsUser::ChangePassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15881-166"><strong>DEBUG_SETPWD</strong></span><span class="sxs-lookup"><span data-stu-id="15881-166"><strong>DEBUG_SETPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="15881-167">CADsUser :: SetPassword</span><span class="sxs-lookup"><span data-stu-id="15881-167">CADsUser::SetPassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15881-168"><strong>DEBUG_BINDCACHE</strong></span><span class="sxs-lookup"><span data-stu-id="15881-168"><strong>DEBUG_BINDCACHE</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="15881-169">GetServerBasedObject</span><span class="sxs-lookup"><span data-stu-id="15881-169">GetServerBasedObject</span></span></li>
<li><span data-ttu-id="15881-170">GetServerLessBasedObject</span><span class="sxs-lookup"><span data-stu-id="15881-170">GetServerLessBasedObject</span></span></li>
<li><span data-ttu-id="15881-171">GetGCDomainName</span><span class="sxs-lookup"><span data-stu-id="15881-171">GetGCDomainName</span></span></li>
<li><span data-ttu-id="15881-172">GetDefaultDomainName</span><span class="sxs-lookup"><span data-stu-id="15881-172">GetDefaultDomainName</span></span></li>
<li><span data-ttu-id="15881-173">GetUserDomainFlatName</span><span class="sxs-lookup"><span data-stu-id="15881-173">GetUserDomainFlatName</span></span></li>
<li><span data-ttu-id="15881-174">BindCacheLookup</span><span class="sxs-lookup"><span data-stu-id="15881-174">BindCacheLookup</span></span></li>
<li><span data-ttu-id="15881-175">EquivalentPortNumbers</span><span class="sxs-lookup"><span data-stu-id="15881-175">EquivalentPortNumbers</span></span></li>
<li><span data-ttu-id="15881-176">CanCredentialsBeReused</span><span class="sxs-lookup"><span data-stu-id="15881-176">CanCredentialsBeReused</span></span></li>
<li><span data-ttu-id="15881-177">BindCacheAdd</span><span class="sxs-lookup"><span data-stu-id="15881-177">BindCacheAdd</span></span></li>
<li><span data-ttu-id="15881-178">BindCacheAddRef</span><span class="sxs-lookup"><span data-stu-id="15881-178">BindCacheAddRef</span></span></li>
<li><span data-ttu-id="15881-179">AddReferralLink</span><span class="sxs-lookup"><span data-stu-id="15881-179">AddReferralLink</span></span></li>
<li><span data-ttu-id="15881-180">CommonRemoveEntry</span><span class="sxs-lookup"><span data-stu-id="15881-180">CommonRemoveEntry</span></span></li>
<li><span data-ttu-id="15881-181">BindCacheDerefHelper</span><span class="sxs-lookup"><span data-stu-id="15881-181">BindCacheDerefHelper</span></span></li>
<li><span data-ttu-id="15881-182">NotifyNewConnection</span><span class="sxs-lookup"><span data-stu-id="15881-182">NotifyNewConnection</span></span></li>
<li><span data-ttu-id="15881-183">QueryForConnection</span><span class="sxs-lookup"><span data-stu-id="15881-183">QueryForConnection</span></span></li>
<li><span data-ttu-id="15881-184">LdapOpenBindWithCredentials</span><span class="sxs-lookup"><span data-stu-id="15881-184">LdapOpenBindWithCredentials</span></span></li>
<li><span data-ttu-id="15881-185">LdapOpenBindWithDefaultCredentials</span><span class="sxs-lookup"><span data-stu-id="15881-185">LdapOpenBindWithDefaultCredentials</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="15881-186">Vous pouvez combiner des indicateurs en combinant les bits appropriés dans l’argument *traceFlags* .</span><span class="sxs-lookup"><span data-stu-id="15881-186">You can combine flags by combining the appropriate bits in the *traceFlags* argument.</span></span> <span data-ttu-id="15881-187">Par exemple, pour spécifier le **\_ schéma de débogage** et **déboguer les indicateurs \_ BINDCACHE** , la valeur *traceFlags* appropriée est 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="15881-187">For example, to specify the **DEBUG\_SCHEMA** and **DEBUG\_BINDCACHE** flags, the appropriate *traceFlags* value would be 0x00000009.</span></span>

<span data-ttu-id="15881-188">Enfin, l’indicateur *TraceLevel* doit avoir l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="15881-188">Finally, the *traceLevel* flag should be one of the following values:</span></span>



|                                          |                       |
|------------------------------------------|-----------------------|
| <span data-ttu-id="15881-189">**\_erreur au niveau de la trace \_**</span><span class="sxs-lookup"><span data-stu-id="15881-189">**TRACE\_LEVEL\_ERROR**</span></span><br/>       | <span data-ttu-id="15881-190">0x00000002</span><span class="sxs-lookup"><span data-stu-id="15881-190">0x00000002</span></span><br/> |
| <span data-ttu-id="15881-191">**\_informations sur le niveau de suivi \_**</span><span class="sxs-lookup"><span data-stu-id="15881-191">**TRACE\_LEVEL\_INFORMATION**</span></span><br/> | <span data-ttu-id="15881-192">0x00000004</span><span class="sxs-lookup"><span data-stu-id="15881-192">0x00000004</span></span><br/> |



 

<span data-ttu-id="15881-193">**Trace \_ Les \_ informations de niveau** entraînent l’enregistrement de tous les événements par le processus de suivi, tandis que le suivi de l' **\_ \_ erreur** entraîne l’enregistrement des événements d’erreur par le processus de suivi.</span><span class="sxs-lookup"><span data-stu-id="15881-193">**TRACE\_LEVEL\_INFORMATION** causes the tracing process to record all events, whereas **TRACE\_LEVEL\_ERROR** causes the tracing process to record only error events.</span></span>

<span data-ttu-id="15881-194">Pour terminer le suivi, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="15881-194">To terminate tracing, run the following command:</span></span>

<span data-ttu-id="15881-195">**tracelog.exe-Stop** *nom_session*</span><span class="sxs-lookup"><span data-stu-id="15881-195">**tracelog.exe -stop** *sessionname*</span></span>

<span data-ttu-id="15881-196">Dans l’exemple précédent, *NomSession* est le même nom que celui fourni avec la commande qui a démarré la section de suivi.</span><span class="sxs-lookup"><span data-stu-id="15881-196">In the previous example, *sessionname* is the same name as the one that was provided with the command that started the tracing section.</span></span>

## <a name="remarks"></a><span data-ttu-id="15881-197">Notes</span><span class="sxs-lookup"><span data-stu-id="15881-197">Remarks</span></span>

<span data-ttu-id="15881-198">Il est plus efficace de suivre uniquement des processus spécifiques en spécifiant un PID particulier pour suivre tous les processus sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="15881-198">It is more effective to trace only specific processes by specifying a particular PID than to trace all processes on a computer.</span></span> <span data-ttu-id="15881-199">Si vous avez besoin d’effectuer le suivi de plusieurs applications sur le même ordinateur, il peut y avoir un impact sur les performances. Il y a une sortie de débogage substantielle dans les sections orientées performance du code.</span><span class="sxs-lookup"><span data-stu-id="15881-199">If you do need to trace multiple applications on the same machine, there might be a performance impact; there is substantial debugging output in performance-oriented sections of the code.</span></span> <span data-ttu-id="15881-200">En outre, les administrateurs doivent veiller à définir correctement les autorisations des fichiers journaux lors du suivi de plusieurs processus. dans le cas contraire, n’importe quel utilisateur peut être en mesure de lire les journaux de suivi, et les autres utilisateurs pourront suivre les processus qui contiennent des informations sécurisées.</span><span class="sxs-lookup"><span data-stu-id="15881-200">Also, administrators must be careful to properly set the permissions of the log files when tracing multiple processes; otherwise, any user might be able to read the tracing logs, and other users will be able to trace processes that contain secure information.</span></span>

<span data-ttu-id="15881-201">Par exemple, supposons que l’administrateur configure le suivi pour une application « Test.exe » et ne spécifie pas un PID dans le registre pour suivre plusieurs instances du processus.</span><span class="sxs-lookup"><span data-stu-id="15881-201">For example, presume the administrator sets up tracing for an application "Test.exe", and does not specify a PID in the registry to trace multiple instances of the process.</span></span> <span data-ttu-id="15881-202">À présent, un autre utilisateur souhaite suivre l’application « Secure.exe ».</span><span class="sxs-lookup"><span data-stu-id="15881-202">Now another user wants to trace the application "Secure.exe".</span></span> <span data-ttu-id="15881-203">Si les fichiers journaux de suivi ne sont pas correctement restreints, il suffit à l’utilisateur de renommer « Secure.exe » en « Test.exe », et il sera suivi.</span><span class="sxs-lookup"><span data-stu-id="15881-203">If the tracing log files are not properly restricted, all that user needs to do is rename "Secure.exe" to "Test.exe", and it will be traced.</span></span> <span data-ttu-id="15881-204">En général, il est préférable de suivre uniquement des processus spécifiques pendant la résolution des problèmes et de supprimer la clé de registre de suivi dès que le dépannage est terminé.</span><span class="sxs-lookup"><span data-stu-id="15881-204">In general, it is best to trace only specific processes while troubleshooting, and to remove the tracing registry key as soon as troubleshooting is done.</span></span>

<span data-ttu-id="15881-205">Étant donné que l’activation du suivi d’événements génère des fichiers journaux supplémentaires, les administrateurs doivent surveiller attentivement les tailles des fichiers journaux. un manque d’espace disque sur l’ordinateur local peut provoquer un déni de service.</span><span class="sxs-lookup"><span data-stu-id="15881-205">Since enabling Event Tracing will produce extra log files, administrators should carefully monitor log file sizes; lack of disk space on the local computer can cause a denial-of-service.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="15881-206">Exemples de scénarios</span><span class="sxs-lookup"><span data-stu-id="15881-206">Example Scenarios</span></span>

<span data-ttu-id="15881-207">Scénario 1 : l’administrateur voit une erreur inattendue dans une application qui définit des mots de passe pour les comptes d’utilisateur. par conséquent, ils prennent les mesures suivantes pour résoudre le problème à l’aide du suivi d’événements.</span><span class="sxs-lookup"><span data-stu-id="15881-207">Scenario 1: The administrator sees an unexpected error in an application that sets passwords for user accounts, so they would take the following steps to fix the problem using Event Tracing.</span></span>

1.  <span data-ttu-id="15881-208">Écrire un script qui reproduit le problème et créer la clé de Registre</span><span class="sxs-lookup"><span data-stu-id="15881-208">Write a script that reproduces the problem, and create the registry key</span></span>

    <span data-ttu-id="15881-209">**HKEY \_ \_** \\  \\  \\  \\  \\ **Suivi** ADSI des services \\ \*\*\*\* de CurrentControlSet de système d’ordinateur localcscript.exe</span><span class="sxs-lookup"><span data-stu-id="15881-209">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

2.  <span data-ttu-id="15881-210">Démarrez une session de suivi, en affectant à *traceFlags* la valeur 0X2 (**Déboguer \_ CHANGEPASSWD**) et *TraceLevel* à 0x4 (**informations de \_ niveau \_ de suivi**), à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="15881-210">Start a tracing session, setting *traceFlags* to 0x2 (**DEBUG\_CHANGEPASSWD**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**), using the following command:</span></span>

    <span data-ttu-id="15881-211">**tracelog.exe-Start scripttrace-GUID \# 7288c9f8-D63C-4932-A345-89d6b060174d-f. \\ ADSI. etl-indicateur 0X2-niveau 0x4**</span><span class="sxs-lookup"><span data-stu-id="15881-211">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

3.  <span data-ttu-id="15881-212">Exécutez cscript.exe avec le script de test pour reproduire le problème, puis terminez la session de suivi :</span><span class="sxs-lookup"><span data-stu-id="15881-212">Run cscript.exe with their test script to reproduce the problem, and then terminate the tracing session:</span></span>

    <span data-ttu-id="15881-213">**tracelog.exe-arrêter scripttrace**</span><span class="sxs-lookup"><span data-stu-id="15881-213">**tracelog.exe -stop scripttrace**</span></span>

4.  <span data-ttu-id="15881-214">Supprimer la clé de Registre</span><span class="sxs-lookup"><span data-stu-id="15881-214">Delete the registry key</span></span>

    <span data-ttu-id="15881-215">**HKEY \_ \_** \\  \\  \\  \\  \\ **Suivi** ADSI des services \\ \*\*\*\* de CurrentControlSet de système d’ordinateur localcscript.exe</span><span class="sxs-lookup"><span data-stu-id="15881-215">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

5.  <span data-ttu-id="15881-216">Exécutez l’outil ETW Tracerpt.exe pour analyser les informations de suivi du journal :</span><span class="sxs-lookup"><span data-stu-id="15881-216">Run the ETW tool Tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="15881-217">**tracelog.exe-Start scripttrace-GUID \# 7288c9f8-D63C-4932-A345-89d6b060174d-f. \\ ADSI. etl-indicateur 0X2-niveau 0x4**</span><span class="sxs-lookup"><span data-stu-id="15881-217">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

<span data-ttu-id="15881-218">Scénario 2 : l’administrateur souhaite suivre les opérations d’analyse et de téléchargement du schéma dans une application [asp](https://msdn.microsoft.com/asp.net/default.aspx) nommée w3wp.exe qui est déjà en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="15881-218">Scenario 2: The administrator wants to trace the schema parsing and download operations in an [ASP](https://msdn.microsoft.com/asp.net/default.aspx) application named w3wp.exe that is already running.</span></span> <span data-ttu-id="15881-219">Pour ce faire, l’administrateur doit effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="15881-219">To do this, the administrator would take the following steps:</span></span>

1.  <span data-ttu-id="15881-220">Créer la clé de Registre</span><span class="sxs-lookup"><span data-stu-id="15881-220">Create the registry key</span></span>

    <span data-ttu-id="15881-221">**HKEY \_ \_** \\  \\  \\  \\  \\ **Suivi** ADSI des services \\ \*\*\*\* de CurrentControlSet de système d’ordinateur localw3wp.exe</span><span class="sxs-lookup"><span data-stu-id="15881-221">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**</span></span>

    <span data-ttu-id="15881-222">et à l’intérieur de cette clé, créez une valeur de type DWORD nommée PID et affectez-lui l’ID de processus de l’instance de w3wp.exe en cours d’exécution sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="15881-222">and inside that key, create a value of type DWORD that is named PID and set it to the process ID of the instance of w3wp.exe that is currently running on the local computer.</span></span>

2.  <span data-ttu-id="15881-223">Ensuite, ils créent une session de suivi, en affectant à *traceFlags* la valeur 0x1 (**\_ schéma de débogage**) et *TraceLevel* à 0x4 (**\_ \_ informations de niveau de suivi**) :</span><span class="sxs-lookup"><span data-stu-id="15881-223">Then they create a tracing session, setting *traceFlags* to 0x1 (**DEBUG\_SCHEMA**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**):</span></span>

    <span data-ttu-id="15881-224">**tracelog.exe-Start w3wptrace-GUID \# 7288c9f8-D63C-4932-A345-89d6b060174d-f. \\ w3wp. etl-indicateur 0x1-niveau 0x4**</span><span class="sxs-lookup"><span data-stu-id="15881-224">**tracelog.exe -start w3wptrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\w3wp.etl -flag 0x1 -level 0x4**</span></span>

3.  <span data-ttu-id="15881-225">Reproduisez l’opération qui nécessite un dépannage.</span><span class="sxs-lookup"><span data-stu-id="15881-225">Reproduce the operation that needs troubleshooting.</span></span>
4.  <span data-ttu-id="15881-226">Mettre fin à la session de suivi :</span><span class="sxs-lookup"><span data-stu-id="15881-226">Terminate the tracing session:</span></span>

    <span data-ttu-id="15881-227">**tracelog.exe-arrêter w3wptrace**</span><span class="sxs-lookup"><span data-stu-id="15881-227">**tracelog.exe -stop w3wptrace**</span></span>

5.  <span data-ttu-id="15881-228">Supprimez la clé de Registre **HKEY \_ local \_ machine** \\ **System** \\ **CurrentControlSet** \\ **service** \\ **ADSI** \\ **Tracing** \\ **w3wp.exe**.</span><span class="sxs-lookup"><span data-stu-id="15881-228">Delete the registry key **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**.</span></span>
6.  <span data-ttu-id="15881-229">Exécutez l’outil ETW tracerpt.exe pour analyser les informations de suivi du journal :</span><span class="sxs-lookup"><span data-stu-id="15881-229">Run the ETW tool tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="15881-230">**tracerpt.exe. \\ w3wp. etl-o-Report**</span><span class="sxs-lookup"><span data-stu-id="15881-230">**tracerpt.exe .\\w3wp.etl -o -report**</span></span>

 

