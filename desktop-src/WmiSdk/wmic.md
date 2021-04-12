---
description: L’utilitaire de ligne de commande WMI (WMIC) fournit une interface de ligne de commande pour WMI.
ms.assetid: a0f5c1e2-9a4d-4c2b-b324-58ec01e67b6e
ms.tgt_platform: multiple
title: wmic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed46e8aeab24acb44f51099a6e813e921dd77eaa
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104211653"
---
# <a name="wmic"></a><span data-ttu-id="7c61c-103">wmic</span><span class="sxs-lookup"><span data-stu-id="7c61c-103">wmic</span></span>

<span data-ttu-id="7c61c-104">L’utilitaire de ligne de commande WMI (WMIC) fournit une interface de ligne de commande pour Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="7c61c-104">The WMI command-line (WMIC) utility provides a command-line interface for Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="7c61c-105">WMIC est compatible avec les interpréteurs de commandes et les commandes utilitaires existantes.</span><span class="sxs-lookup"><span data-stu-id="7c61c-105">WMIC is compatible with existing shells and utility commands.</span></span> <span data-ttu-id="7c61c-106">Voici une rubrique de référence générale pour WMIC.</span><span class="sxs-lookup"><span data-stu-id="7c61c-106">The following is a general reference topic for WMIC.</span></span> <span data-ttu-id="7c61c-107">Pour plus d’informations et des instructions sur l’utilisation de WMIC, y compris des informations supplémentaires sur les alias, les verbes, les commutateurs et les commandes, consultez [utilisation de Windows Management Instrumentation ligne de commande](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) et [WMIC-prendre le contrôle de ligne de commande sur WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="7c61c-107">For more information and guidelines on how to use WMIC, including additional information on aliases, verbs, switches, and commands, see [Using Windows Management Instrumentation Command-line](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) and [WMIC - Take Command-line Control over WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10)).</span></span>

## <a name="alias"></a><span data-ttu-id="7c61c-108">Alias</span><span class="sxs-lookup"><span data-stu-id="7c61c-108">Alias</span></span>

<span data-ttu-id="7c61c-109">Un alias est un changement de nom convivial d’une classe, d’une propriété ou d’une méthode qui facilite l’utilisation et la lecture de WMI.</span><span class="sxs-lookup"><span data-stu-id="7c61c-109">An alias is a friendly renaming of a class, property, or method that makes WMI easier to use and read.</span></span> <span data-ttu-id="7c61c-110">Vous pouvez déterminer les alias disponibles pour WMIC via le **/ ?**</span><span class="sxs-lookup"><span data-stu-id="7c61c-110">You can determine what aliases are available for WMIC through the **/?**</span></span> <span data-ttu-id="7c61c-111">.</span><span class="sxs-lookup"><span data-stu-id="7c61c-111">command.</span></span> <span data-ttu-id="7c61c-112">Vous pouvez également déterminer les alias pour une classe spécifique à l’aide du **<className> / ?**</span><span class="sxs-lookup"><span data-stu-id="7c61c-112">You can also determine the aliases for a specific class using the **<className> /?**</span></span> <span data-ttu-id="7c61c-113">.</span><span class="sxs-lookup"><span data-stu-id="7c61c-113">command.</span></span> <span data-ttu-id="7c61c-114">Pour plus d’informations, consultez [alias WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="7c61c-114">For more information, see [WMIC Aliases](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).</span></span>

## <a name="switch"></a><span data-ttu-id="7c61c-115">Commutateur</span><span class="sxs-lookup"><span data-stu-id="7c61c-115">Switch</span></span>

<span data-ttu-id="7c61c-116">Un commutateur est une option WMIC que vous pouvez définir globalement ou éventuellement.</span><span class="sxs-lookup"><span data-stu-id="7c61c-116">A switch is a WMIC option you can set globally or optionally.</span></span> <span data-ttu-id="7c61c-117">Pour obtenir la liste des commutateurs disponibles, consultez [commutateurs WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="7c61c-117">For a list of available switches, see [WMIC Switches](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).</span></span>

## <a name="verbs"></a><span data-ttu-id="7c61c-118">Verbes et adverbes</span><span class="sxs-lookup"><span data-stu-id="7c61c-118">Verbs</span></span>

<span data-ttu-id="7c61c-119">Pour utiliser des verbes dans WMIC, entrez le nom d’alias suivi du verbe.</span><span class="sxs-lookup"><span data-stu-id="7c61c-119">To use verbs in WMIC, enter the alias name followed by the verb.</span></span> <span data-ttu-id="7c61c-120">Si un alias ne prend pas en charge un verbe, vous recevez le message « le fournisseur ne peut pas prendre en charge l’opération tentée ».</span><span class="sxs-lookup"><span data-stu-id="7c61c-120">If an alias does not support a verb, you receive the message "provider is not capable of the attempted operation."</span></span> <span data-ttu-id="7c61c-121">Pour plus d’informations, consultez [verbes WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="7c61c-121">For more information, see [WMIC Verbs](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).</span></span>

<span data-ttu-id="7c61c-122">La plupart des alias prennent en charge les verbes suivants.</span><span class="sxs-lookup"><span data-stu-id="7c61c-122">Most aliases support the following verbs.</span></span>

<dl> <dt>

<span data-ttu-id="7c61c-123"><span id="ASSOC"></span><span id="assoc"></span>Craddock</span><span class="sxs-lookup"><span data-stu-id="7c61c-123"><span id="ASSOC"></span><span id="assoc"></span>ASSOC</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-124">Retourne le résultat de la `Associators of (<wmi_object>)` requête où *<\_ objet WMI>* correspond au chemin d’accès des objets retournés par les commandes **path** ou **Class** .</span><span class="sxs-lookup"><span data-stu-id="7c61c-124">Returns the result of the `Associators of (<wmi_object>)` query where *<wmi\_object>* is the path of objects returned by the **PATH** or **CLASS** commands.</span></span> <span data-ttu-id="7c61c-125">Les résultats sont des instances associées à l’objet.</span><span class="sxs-lookup"><span data-stu-id="7c61c-125">The results are instances associated with the object.</span></span> <span data-ttu-id="7c61c-126">Lorsque ASSOC est utilisé avec un alias, les classes avec la classe sous-jacente de l’alias sont retournées.</span><span class="sxs-lookup"><span data-stu-id="7c61c-126">When ASSOC is used with an alias, the classes with the class underlying the alias are returned.</span></span> <span data-ttu-id="7c61c-127">Par défaut, la sortie est retournée au format HTML.</span><span class="sxs-lookup"><span data-stu-id="7c61c-127">By default the output is returned in HTML format.</span></span>

<span data-ttu-id="7c61c-128">Le verbe ASSOC contient les commutateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="7c61c-128">The ASSOC verb has the following switches.</span></span>



| <span data-ttu-id="7c61c-129">Commutateur</span><span class="sxs-lookup"><span data-stu-id="7c61c-129">Switch</span></span>                         | <span data-ttu-id="7c61c-130">Description</span><span class="sxs-lookup"><span data-stu-id="7c61c-130">Description</span></span>                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c61c-131">/RESULTCLASS:<classname></span><span class="sxs-lookup"><span data-stu-id="7c61c-131">/RESULTCLASS:<classname></span></span> | <span data-ttu-id="7c61c-132">Les points de terminaison retournés associés à l’objet source doivent appartenir à la classe spécifiée ou en être dérivés.</span><span class="sxs-lookup"><span data-stu-id="7c61c-132">Returned endpoints associated with the source object must belong to, or be derived from the specified class.</span></span>      |
| <span data-ttu-id="7c61c-133">/RESULTROLE:<rolename></span><span class="sxs-lookup"><span data-stu-id="7c61c-133">/RESULTROLE:<rolename></span></span>   | <span data-ttu-id="7c61c-134">Les points de terminaison retournés doivent jouer un rôle spécifique dans les associations avec l’objet source.</span><span class="sxs-lookup"><span data-stu-id="7c61c-134">Returned endpoints must play a specific role in associations with the source object.</span></span>                              |
| <span data-ttu-id="7c61c-135">/ASSOCCLASS:<assocclass></span><span class="sxs-lookup"><span data-stu-id="7c61c-135">/ASSOCCLASS:<assocclass></span></span> | <span data-ttu-id="7c61c-136">Les points de terminaison retournés doivent être associés à la source par le biais de la classe spécifiée ou de l’une de ses classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="7c61c-136">Returned endpoints must be associated with the source through the specified class, or one of its derived classes.</span></span> |



 

<span data-ttu-id="7c61c-137">Exemple : **Assoc du système d’exploitation**</span><span class="sxs-lookup"><span data-stu-id="7c61c-137">Example: **OS ASSOC**</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-138"><span id="CALL"></span><span id="call"></span>INVOQU</span><span class="sxs-lookup"><span data-stu-id="7c61c-138"><span id="CALL"></span><span id="call"></span>CALL</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-139">Exécute une méthode.</span><span class="sxs-lookup"><span data-stu-id="7c61c-139">Executes a method.</span></span>

<span data-ttu-id="7c61c-140">Exemple : **service où Caption = 'telnet’appelle STARTSERVICE**</span><span class="sxs-lookup"><span data-stu-id="7c61c-140">Example: **SERVICE WHERE CAPTION='TELNET' CALL STARTSERVICE**</span></span>

> [!Note]  
> <span data-ttu-id="7c61c-141">Pour déterminer les méthodes disponibles pour une classe donnée, utilisez **/ ?**.</span><span class="sxs-lookup"><span data-stu-id="7c61c-141">To determine the methods available for a given class, use **/?**.</span></span> <span data-ttu-id="7c61c-142">Par exemple, **service où Caption = 'telnet’appelle/ ?**</span><span class="sxs-lookup"><span data-stu-id="7c61c-142">For example, **SERVICE WHERE CAPTION='TELNET' CALL /?**</span></span> <span data-ttu-id="7c61c-143">répertorie les fonctions disponibles pour la classe de service.</span><span class="sxs-lookup"><span data-stu-id="7c61c-143">lists the available functions for the service class.</span></span>

 

</dd> <dt>

<span data-ttu-id="7c61c-144"><span id="CREATE"></span><span id="create"></span>CRÉÉS</span><span class="sxs-lookup"><span data-stu-id="7c61c-144"><span id="CREATE"></span><span id="create"></span>CREATE</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-145">Crée une nouvelle instance et définit les valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="7c61c-145">Creates a new instance and sets the property values.</span></span> <span data-ttu-id="7c61c-146">Impossible d’utiliser CREATe pour créer une nouvelle classe.</span><span class="sxs-lookup"><span data-stu-id="7c61c-146">CREATE cannot be used to create a new class.</span></span>

<span data-ttu-id="7c61c-147">Exemple : **Environment Create Name = "Temp"; VARIABLEVALUE = "nouveau"**</span><span class="sxs-lookup"><span data-stu-id="7c61c-147">Example: **ENVIRONMENT CREATE NAME="TEMP"; VARIABLEVALUE="NEW"**</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-148"><span id="DELETE"></span><span id="delete"></span>SUPPRIMER</span><span class="sxs-lookup"><span data-stu-id="7c61c-148"><span id="DELETE"></span><span id="delete"></span>DELETE</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-149">Supprime l’instance actuelle ou l’ensemble d’instances.</span><span class="sxs-lookup"><span data-stu-id="7c61c-149">Deletes the current instance or set of instances.</span></span> <span data-ttu-id="7c61c-150">La suppression peut être utilisée pour supprimer une classe.</span><span class="sxs-lookup"><span data-stu-id="7c61c-150">DELETE can be used to delete a class.</span></span>

<span data-ttu-id="7c61c-151">Exemple : **processus où name = "CALC.EXE" Delete**</span><span class="sxs-lookup"><span data-stu-id="7c61c-151">Example: **PROCESS WHERE NAME="CALC.EXE" DELETE**</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-152"><span id="GET"></span><span id="get"></span>Télécharger</span><span class="sxs-lookup"><span data-stu-id="7c61c-152"><span id="GET"></span><span id="get"></span>GET</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-153">Récupérer des valeurs de propriété spécifiques.</span><span class="sxs-lookup"><span data-stu-id="7c61c-153">Retrieve specific property values.</span></span>

<span data-ttu-id="7c61c-154">La commande dispose des commutateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="7c61c-154">GET has the following switches.</span></span>



| <span data-ttu-id="7c61c-155">Commutateur</span><span class="sxs-lookup"><span data-stu-id="7c61c-155">Switch</span></span>                               | <span data-ttu-id="7c61c-156">Description</span><span class="sxs-lookup"><span data-stu-id="7c61c-156">Description</span></span>                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c61c-157">/VALUE</span><span class="sxs-lookup"><span data-stu-id="7c61c-157">/VALUE</span></span>                               | <span data-ttu-id="7c61c-158">La sortie est mise en forme avec chaque valeur figurant sur une ligne distincte et avec le nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="7c61c-158">Output is formatted with each value listed on a separate line and with the name of the property.</span></span>                                           |
| <span data-ttu-id="7c61c-159">/ALL</span><span class="sxs-lookup"><span data-stu-id="7c61c-159">/ALL</span></span>                                 | <span data-ttu-id="7c61c-160">La sortie est mise en forme en tant que table.</span><span class="sxs-lookup"><span data-stu-id="7c61c-160">Output is formatted as a table.</span></span>                                                                                                            |
| <span data-ttu-id="7c61c-161">Traduire<translation table></span><span class="sxs-lookup"><span data-stu-id="7c61c-161">/TRANSLATE:<translation table></span></span> | <span data-ttu-id="7c61c-162">Traduisez la sortie à l’aide de la table de traduction nommée par la commande.</span><span class="sxs-lookup"><span data-stu-id="7c61c-162">Translate the output using the translation table named by the command.</span></span> <span data-ttu-id="7c61c-163">Les tables de traduction BasicXml et novirgule sont incluses avec WMIC.</span><span class="sxs-lookup"><span data-stu-id="7c61c-163">The translation tables BasicXml and NoComma are included with WMIC.</span></span> |
| <span data-ttu-id="7c61c-164">Chaque<interval></span><span class="sxs-lookup"><span data-stu-id="7c61c-164">/EVERY:<interval></span></span>              | <span data-ttu-id="7c61c-165">Répétez la commande toutes les <interval> secondes.</span><span class="sxs-lookup"><span data-stu-id="7c61c-165">Repeat the command every <interval> seconds.</span></span>                                                                                         |
| <span data-ttu-id="7c61c-166">FORMAT<format specifier></span><span class="sxs-lookup"><span data-stu-id="7c61c-166">/FORMAT:<format specifier></span></span>     | <span data-ttu-id="7c61c-167">Spécifie un mot clé ou un nom de fichier XSL pour mettre en forme les données.</span><span class="sxs-lookup"><span data-stu-id="7c61c-167">Specifies a key word or XSL file name to format the data.</span></span>                                                                                  |



 

<span data-ttu-id="7c61c-168">Exemple : **traiter demander un nom**</span><span class="sxs-lookup"><span data-stu-id="7c61c-168">Example: **PROCESS GET NAME**</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-169"><span id="LIST"></span><span id="list"></span>TARIFS</span><span class="sxs-lookup"><span data-stu-id="7c61c-169"><span id="LIST"></span><span id="list"></span>LIST</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-170">Affiche les données.</span><span class="sxs-lookup"><span data-stu-id="7c61c-170">Shows data.</span></span> <span data-ttu-id="7c61c-171">LIST est le verbe par défaut.</span><span class="sxs-lookup"><span data-stu-id="7c61c-171">LIST is the default verb.</span></span>

<span data-ttu-id="7c61c-172">La liste comporte les adverbes suivants.</span><span class="sxs-lookup"><span data-stu-id="7c61c-172">LIST has the following adverbs.</span></span>



| <span data-ttu-id="7c61c-173">Verbe</span><span class="sxs-lookup"><span data-stu-id="7c61c-173">Adverb</span></span>   | <span data-ttu-id="7c61c-174">Description</span><span class="sxs-lookup"><span data-stu-id="7c61c-174">Description</span></span>                                                  |
|----------|--------------------------------------------------------------|
| <span data-ttu-id="7c61c-175">BRIEF</span><span class="sxs-lookup"><span data-stu-id="7c61c-175">BRIEF</span></span>    | <span data-ttu-id="7c61c-176">Ensemble principal des propriétés.</span><span class="sxs-lookup"><span data-stu-id="7c61c-176">Core set of the properties.</span></span>                                  |
| <span data-ttu-id="7c61c-177">FULL</span><span class="sxs-lookup"><span data-stu-id="7c61c-177">FULL</span></span>     | <span data-ttu-id="7c61c-178">Ensemble complet de propriétés.</span><span class="sxs-lookup"><span data-stu-id="7c61c-178">Full set of properties.</span></span> <span data-ttu-id="7c61c-179">Il s’agit de l’adverbe par défaut pour la liste.</span><span class="sxs-lookup"><span data-stu-id="7c61c-179">This is the default adverb for LIST.</span></span> |
| <span data-ttu-id="7c61c-180">INSTANCE</span><span class="sxs-lookup"><span data-stu-id="7c61c-180">INSTANCE</span></span> | <span data-ttu-id="7c61c-181">Chemins d’accès d’instance uniquement.</span><span class="sxs-lookup"><span data-stu-id="7c61c-181">Instance paths only.</span></span>                                         |
| <span data-ttu-id="7c61c-182">STATUT</span><span class="sxs-lookup"><span data-stu-id="7c61c-182">STATUS</span></span>   | <span data-ttu-id="7c61c-183">État des objets.</span><span class="sxs-lookup"><span data-stu-id="7c61c-183">Status of the objects.</span></span>                                       |
| <span data-ttu-id="7c61c-184">SYSTEM</span><span class="sxs-lookup"><span data-stu-id="7c61c-184">SYSTEM</span></span>   | <span data-ttu-id="7c61c-185">Propriétés système.</span><span class="sxs-lookup"><span data-stu-id="7c61c-185">System properties.</span></span>                                           |



 

<span data-ttu-id="7c61c-186">La liste comporte les commutateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="7c61c-186">LIST has the following switches.</span></span>



| <span data-ttu-id="7c61c-187">Commutateur</span><span class="sxs-lookup"><span data-stu-id="7c61c-187">Switch</span></span>                               | <span data-ttu-id="7c61c-188">Description</span><span class="sxs-lookup"><span data-stu-id="7c61c-188">Description</span></span>                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c61c-189">Traduire<translation table></span><span class="sxs-lookup"><span data-stu-id="7c61c-189">/TRANSLATE:<translation table></span></span> | <span data-ttu-id="7c61c-190">Traduisez la sortie à l’aide de la table de traduction nommée par la commande.</span><span class="sxs-lookup"><span data-stu-id="7c61c-190">Translate the output using the translation table named by the command.</span></span> <span data-ttu-id="7c61c-191">Les tables de traduction BasicXml et novirgule sont incluses avec WMIC.</span><span class="sxs-lookup"><span data-stu-id="7c61c-191">The translation tables BasicXml and NoComma are included with WMIC.</span></span> |
| <span data-ttu-id="7c61c-192">Chaque<interval></span><span class="sxs-lookup"><span data-stu-id="7c61c-192">/EVERY:<interval></span></span>              | <span data-ttu-id="7c61c-193">Répétez la commande toutes les <interval> secondes.</span><span class="sxs-lookup"><span data-stu-id="7c61c-193">Repeat the command every <interval> seconds.</span></span>                                                                                         |
| <span data-ttu-id="7c61c-194">FORMAT<format specifier></span><span class="sxs-lookup"><span data-stu-id="7c61c-194">/FORMAT:<format specifier></span></span>     | <span data-ttu-id="7c61c-195">Spécifie un mot clé ou un nom de fichier XSL pour mettre en forme les données.</span><span class="sxs-lookup"><span data-stu-id="7c61c-195">Specifies a key word or XSL file name to format the data.</span></span>                                                                                  |



 

<span data-ttu-id="7c61c-196">Exemple : **Brief (liste de processus** )</span><span class="sxs-lookup"><span data-stu-id="7c61c-196">Example: **PROCESS LIST BRIEF**</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-197"><span id="SET"></span><span id="set"></span>DÉFINIE</span><span class="sxs-lookup"><span data-stu-id="7c61c-197"><span id="SET"></span><span id="set"></span>SET</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-198">Affecte des valeurs aux propriétés.</span><span class="sxs-lookup"><span data-stu-id="7c61c-198">Assigns values to properties.</span></span> <span data-ttu-id="7c61c-199">Exemple : **Environment Set Name = "Temp"**, **VARIABLEVALUE = "New"**</span><span class="sxs-lookup"><span data-stu-id="7c61c-199">Example: **ENVIRONMENT SET NAME="TEMP"**, **VARIABLEVALUE="NEW"**</span></span>

</dd> </dl>

## <a name="switches"></a><span data-ttu-id="7c61c-200">Commutateurs</span><span class="sxs-lookup"><span data-stu-id="7c61c-200">Switches</span></span>

<span data-ttu-id="7c61c-201">Les commutateurs globaux sont utilisés pour définir les valeurs par défaut de l’environnement WMIC.</span><span class="sxs-lookup"><span data-stu-id="7c61c-201">Global switches are used to set defaults for the WMIC environment.</span></span> <span data-ttu-id="7c61c-202">Vous pouvez afficher la valeur actuelle des conditions définies par ces commutateurs en entrant la commande de **contexte** .</span><span class="sxs-lookup"><span data-stu-id="7c61c-202">You can view the current value of the conditions set by these switches by entering the **CONTEXT** command.</span></span>

<dl> <dt>

<span data-ttu-id="7c61c-203"><span id="_NAMESPACE"></span><span id="_namespace"></span>/NAMESPACE</span><span class="sxs-lookup"><span data-stu-id="7c61c-203"><span id="_NAMESPACE"></span><span id="_namespace"></span>/NAMESPACE</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-204">Espace de noms utilisé en général par l’alias.</span><span class="sxs-lookup"><span data-stu-id="7c61c-204">Namespace the alias uses typically.</span></span> <span data-ttu-id="7c61c-205">La valeur par défaut est le \\ cimv2 racine.</span><span class="sxs-lookup"><span data-stu-id="7c61c-205">The default is root\\cimv2.</span></span>

<span data-ttu-id="7c61c-206">Exemple : **/Namespace : \\ \\ root**</span><span class="sxs-lookup"><span data-stu-id="7c61c-206">Example: **/NAMESPACE:\\\\root**</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-207"><span id="_ROLE"></span><span id="_role"></span>/ROLE</span><span class="sxs-lookup"><span data-stu-id="7c61c-207"><span id="_ROLE"></span><span id="_role"></span>/ROLE</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-208">L’espace de noms WMIC recherche généralement des alias et d’autres informations WMIC.</span><span class="sxs-lookup"><span data-stu-id="7c61c-208">Namespace WMIC typically looks in for aliases and other WMIC information.</span></span>

<span data-ttu-id="7c61c-209">Exemple : **/Role : \\ \\ root**</span><span class="sxs-lookup"><span data-stu-id="7c61c-209">Example: **/ROLE:\\\\root**</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-210"><span id="_NODE"></span><span id="_node"></span>/NODE</span><span class="sxs-lookup"><span data-stu-id="7c61c-210"><span id="_NODE"></span><span id="_node"></span>/NODE</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-211">Noms d’ordinateur, délimité par des virgules.</span><span class="sxs-lookup"><span data-stu-id="7c61c-211">Computer names, comma delimited.</span></span> <span data-ttu-id="7c61c-212">Toutes les commandes sont exécutées de façon synchrone sur tous les ordinateurs répertoriés dans cette valeur.</span><span class="sxs-lookup"><span data-stu-id="7c61c-212">All commands are synchronously executed against all computers listed in this value.</span></span> <span data-ttu-id="7c61c-213">Les noms de fichiers doivent être précédés de &.</span><span class="sxs-lookup"><span data-stu-id="7c61c-213">File names must be prefixed with &.</span></span> <span data-ttu-id="7c61c-214">Les noms d’ordinateur dans un fichier doivent être séparés par des virgules ou des lignes distinctes.</span><span class="sxs-lookup"><span data-stu-id="7c61c-214">Computer names within a file must be comma delimited or on separate lines.</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-215"><span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL</span><span class="sxs-lookup"><span data-stu-id="7c61c-215"><span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-216">Niveau d'emprunt d'identité.</span><span class="sxs-lookup"><span data-stu-id="7c61c-216">Impersonation level.</span></span>

<span data-ttu-id="7c61c-217">Exemple : **/IMPLEVEL : Anonymous**</span><span class="sxs-lookup"><span data-stu-id="7c61c-217">Example: **/IMPLEVEL:Anonymous**</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-218"><span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL</span><span class="sxs-lookup"><span data-stu-id="7c61c-218"><span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-219">Niveau d’authentification.</span><span class="sxs-lookup"><span data-stu-id="7c61c-219">Authentication level.</span></span>

<span data-ttu-id="7c61c-220">Exemple : **/AUTHLEVEL : PKT**</span><span class="sxs-lookup"><span data-stu-id="7c61c-220">Example: **/AUTHLEVEL:Pkt**</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-221"><span id="_LOCALE"></span><span id="_locale"></span>/LOCALE</span><span class="sxs-lookup"><span data-stu-id="7c61c-221"><span id="_LOCALE"></span><span id="_locale"></span>/LOCALE</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-222">Paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="7c61c-222">Locale.</span></span>

<span data-ttu-id="7c61c-223">Exemple : **/locale : MS \_ 411**</span><span class="sxs-lookup"><span data-stu-id="7c61c-223">Example: **/LOCALE:MS\_411**</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-224"><span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="7c61c-224"><span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-225">Activez ou désactivez tous les privilèges.</span><span class="sxs-lookup"><span data-stu-id="7c61c-225">Enable or disable all privileges.</span></span>

<span data-ttu-id="7c61c-226">Exemple : **/privileges : Enable** ou **/privileges : Disable**</span><span class="sxs-lookup"><span data-stu-id="7c61c-226">Example: **/PRIVILEGES:ENABLE** or **/PRIVILEGES:DISABLE**</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-227"><span id="_TRACE"></span><span id="_trace"></span>/TRACE</span><span class="sxs-lookup"><span data-stu-id="7c61c-227"><span id="_TRACE"></span><span id="_trace"></span>/TRACE</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-228">Affiche la réussite ou l’échec de toutes les fonctions utilisées pour exécuter les commandes WMIC.</span><span class="sxs-lookup"><span data-stu-id="7c61c-228">Display the success or failure of all functions used to execute WMIC commands.</span></span>

<span data-ttu-id="7c61c-229">Exemple : **/trace : on** ou **/trace : OFF**</span><span class="sxs-lookup"><span data-stu-id="7c61c-229">Example: **/TRACE:ON** or **/TRACE:OFF**</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-230"><span id="_RECORD"></span><span id="_record"></span>/RECORD</span><span class="sxs-lookup"><span data-stu-id="7c61c-230"><span id="_RECORD"></span><span id="_record"></span>/RECORD</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-231">Enregistre toute la sortie dans un fichier XML.</span><span class="sxs-lookup"><span data-stu-id="7c61c-231">Records all output to an XML file.</span></span> <span data-ttu-id="7c61c-232">La sortie s’affiche également à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="7c61c-232">Output is also displayed at the command prompt.</span></span>

<span data-ttu-id="7c61c-233">Exemple : **/Record :** _MyOutput.xml_</span><span class="sxs-lookup"><span data-stu-id="7c61c-233">Example: **/RECORD:**_MyOutput.xml_</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-234"><span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="7c61c-234"><span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-235">En règle générale, les commandes DELETE sont confirmées.</span><span class="sxs-lookup"><span data-stu-id="7c61c-235">Typically, delete commands are confirmed.</span></span>

<span data-ttu-id="7c61c-236">Exemple : **/interactive : on** ou **/interactive : OFF**</span><span class="sxs-lookup"><span data-stu-id="7c61c-236">Example: **/INTERACTIVE:ON** or **/INTERACTIVE:OFF**</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-237"><span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FailFast **on** \| **off** \| *TimeoutInMilliseconds*</span><span class="sxs-lookup"><span data-stu-id="7c61c-237"><span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FAILFAST **on**\|**off**\|*TimeoutInMilliseconds*</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-238">Si, sur les ordinateurs/NODE, la commande ping est exécutée avant d’envoyer des commandes WMIC à celles-ci.</span><span class="sxs-lookup"><span data-stu-id="7c61c-238">If ON the /NODE computers are pinged before sending WMIC commands to them.</span></span> <span data-ttu-id="7c61c-239">Si un ordinateur ne répond pas, les commandes WMIC ne sont pas envoyées à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="7c61c-239">If a computer does not respond the WMIC commands are not sent to it.</span></span>

<span data-ttu-id="7c61c-240">Exemple : « /FAILFAST : ON » ou « /FAILFAST : OFF »</span><span class="sxs-lookup"><span data-stu-id="7c61c-240">Example: "/FAILFAST:ON" or "/FAILFAST:OFF"</span></span>

<span data-ttu-id="7c61c-241">**/FAILFAST WMIC : 1000**</span><span class="sxs-lookup"><span data-stu-id="7c61c-241">**WMIC /FAILFAST:1000**</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-242"><span id="_USER"></span><span id="_user"></span>/USER</span><span class="sxs-lookup"><span data-stu-id="7c61c-242"><span id="_USER"></span><span id="_user"></span>/USER</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-243">Nom d’utilisateur utilisé par WMIC lors de l’accès aux ordinateurs/NODE ou aux ordinateurs spécifiés dans les alias.</span><span class="sxs-lookup"><span data-stu-id="7c61c-243">User name used by WMIC when accessing the /NODE computers or computers specified in the aliases.</span></span> <span data-ttu-id="7c61c-244">Vous êtes invité à entrer le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="7c61c-244">You are prompted for the password.</span></span> <span data-ttu-id="7c61c-245">Un nom d’utilisateur ne peut pas être utilisé avec l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7c61c-245">A user name cannot be used with the local computer.</span></span>

<span data-ttu-id="7c61c-246">Exemple : **/User :**_jdupont_</span><span class="sxs-lookup"><span data-stu-id="7c61c-246">Example: **/USER:**_JSMITH_</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-247"><span id="_PASSWORD"></span><span id="_password"></span>/PASSWORD</span><span class="sxs-lookup"><span data-stu-id="7c61c-247"><span id="_PASSWORD"></span><span id="_password"></span>/PASSWORD</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-248">Mot de passe utilisé par WMIC lors de l’accès aux ordinateurs/NPDE.</span><span class="sxs-lookup"><span data-stu-id="7c61c-248">Password used by WMIC when accessing the /NPDE computers.</span></span> <span data-ttu-id="7c61c-249">Le mot de passe est visible sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="7c61c-249">The password is visible at the command line.</span></span>

<span data-ttu-id="7c61c-250">Exemple : **/Password :**_mot_de_passe_</span><span class="sxs-lookup"><span data-stu-id="7c61c-250">Example: **/PASSWORD:**_password_</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-251"><span id="_OUTPUT"></span><span id="_output"></span>/OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c61c-251"><span id="_OUTPUT"></span><span id="_output"></span>/OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-252">Spécifie un mode pour toutes les redirections de sortie.</span><span class="sxs-lookup"><span data-stu-id="7c61c-252">Specifies a mode for all output redirection.</span></span> <span data-ttu-id="7c61c-253">La sortie n’apparaît pas sur la ligne de commande et la destination est effacée avant le début de la sortie.</span><span class="sxs-lookup"><span data-stu-id="7c61c-253">Output does not appear at the command line and the destination is cleared before output begins.</span></span> <span data-ttu-id="7c61c-254">Les valeurs valides sont STDOUT, CLIPBOARD ou un nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="7c61c-254">Valid values are STDOUT, CLIPBOARD or a file name.</span></span>

<span data-ttu-id="7c61c-255">Exemple : **/Output : Clipboard**</span><span class="sxs-lookup"><span data-stu-id="7c61c-255">Example: **/OUTPUT:CLIPBOARD**</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-256"><span id="_APPEND"></span><span id="_append"></span>/APPEND</span><span class="sxs-lookup"><span data-stu-id="7c61c-256"><span id="_APPEND"></span><span id="_append"></span>/APPEND</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-257">Spécifie un mode pour toutes les redirections de sortie.</span><span class="sxs-lookup"><span data-stu-id="7c61c-257">Specifies a mode for all output redirection.</span></span> <span data-ttu-id="7c61c-258">La sortie n’apparaît pas sur la ligne de commande et la destination n’est pas effacée avant le début de la sortie et la sortie est ajoutée à la fin du contenu actuel de la destination.</span><span class="sxs-lookup"><span data-stu-id="7c61c-258">Output does not appear at the command line and the destination is not cleared before output begins and output is appended to the end of the current contents of the destination.</span></span> <span data-ttu-id="7c61c-259">Les valeurs valides sont STDOUT, CLIPBOARD ou un nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="7c61c-259">Valid values are STDOUT, CLIPBOARD or a file name.</span></span>

<span data-ttu-id="7c61c-260">Exemple : **/Append : Clipboard**</span><span class="sxs-lookup"><span data-stu-id="7c61c-260">Example: **/APPEND:CLIPBOARD**</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-261"><span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE</span><span class="sxs-lookup"><span data-stu-id="7c61c-261"><span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-262">Utilisé avec **les commutateurs** **List** et.</span><span class="sxs-lookup"><span data-stu-id="7c61c-262">Used with the **LIST** and **GET /EVERY** switch.</span></span> <span data-ttu-id="7c61c-263">Si agrégat est activé, liste et obtenir affichent leurs résultats lorsque tous les ordinateurs du/NODE ont répondu ou expiré. Si AGGREGATe est désactivé, LIST et affichent les résultats dès qu’ils sont reçus.</span><span class="sxs-lookup"><span data-stu-id="7c61c-263">If AGGREGATE is ON, LIST and GET display their results when all computers in the /NODE have either responded or timed out. If AGGREGATE is OFF, LIST and GET display their results as soon as they are received.</span></span>

<span data-ttu-id="7c61c-264">Exemple : **/Aggregate : OFF** ou **/Aggregate : on**</span><span class="sxs-lookup"><span data-stu-id="7c61c-264">Example: **/AGGREGATE:OFF** or **/AGGREGATE:ON**</span></span>

</dd> </dl>

## <a name="commands"></a><span data-ttu-id="7c61c-265">Commandes</span><span class="sxs-lookup"><span data-stu-id="7c61c-265">Commands</span></span>

<span data-ttu-id="7c61c-266">Les commandes WMIC suivantes sont disponibles à tout moment.</span><span class="sxs-lookup"><span data-stu-id="7c61c-266">The following WMIC commands are available at all times.</span></span> <span data-ttu-id="7c61c-267">Pour plus d’informations, consultez [commandes WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="7c61c-267">For more information, see [WMIC Commands](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).</span></span>

<dl> <dt>

<span data-ttu-id="7c61c-268"><span id="CLASS"></span><span id="class"></span>TYPE</span><span class="sxs-lookup"><span data-stu-id="7c61c-268"><span id="CLASS"></span><span id="class"></span>CLASS</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-269">Quitter le mode d’alias par défaut de WMIC pour accéder directement aux classes dans le schéma WMI.</span><span class="sxs-lookup"><span data-stu-id="7c61c-269">Escape from the default alias mode of WMIC to access classes in the WMI schema directly.</span></span> <span data-ttu-id="7c61c-270">Pour plus d’informations sur les classes WMI disponibles, consultez [classes WMI](wmi-classes.md).</span><span class="sxs-lookup"><span data-stu-id="7c61c-270">For more information on available WMI classes, see [WMI Classes](wmi-classes.md).</span></span>

<span data-ttu-id="7c61c-271">Exemple : **WMIC/output : c : \\ClassOutput.htm classe Win32 \_ SoundDevice**</span><span class="sxs-lookup"><span data-stu-id="7c61c-271">Example: **WMIC /OUTPUT:c:\\ClassOutput.htm CLASS Win32\_SoundDevice**</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-272"><span id="PATH"></span><span id="path"></span>D</span><span class="sxs-lookup"><span data-stu-id="7c61c-272"><span id="PATH"></span><span id="path"></span>PATH</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-273">Quitter le mode d’alias par défaut de WMIC pour accéder directement aux instances dans le schéma WMI.</span><span class="sxs-lookup"><span data-stu-id="7c61c-273">Escape from the default alias mode of WMIC to access instances in the WMI schema directly.</span></span>

<span data-ttu-id="7c61c-274">Exemple : **WMIC/output : c : \\PathOutput.txt Path Win32 \_ SoundDevice/value**</span><span class="sxs-lookup"><span data-stu-id="7c61c-274">Example: **WMIC /OUTPUT:c:\\PathOutput.txt PATH Win32\_SoundDevice GET /VALUE**</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-275"><span id="CONTEXT"></span><span id="context"></span>CONTEXTE</span><span class="sxs-lookup"><span data-stu-id="7c61c-275"><span id="CONTEXT"></span><span id="context"></span>CONTEXT</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-276">Affichez les valeurs actuelles de tous les commutateurs globaux.</span><span class="sxs-lookup"><span data-stu-id="7c61c-276">Display the current values of all global switches.</span></span>

<span data-ttu-id="7c61c-277">Exemple : **contexte WMIC**</span><span class="sxs-lookup"><span data-stu-id="7c61c-277">Example: **WMIC CONTEXT**</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-278"><span id="QUIT"></span><span id="quit"></span>DÉMISSIONN</span><span class="sxs-lookup"><span data-stu-id="7c61c-278"><span id="QUIT"></span><span id="quit"></span>QUIT</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-279">Quittez WMIC.</span><span class="sxs-lookup"><span data-stu-id="7c61c-279">Exit from WMIC.</span></span>

<span data-ttu-id="7c61c-280">Exemple : **WMIC Quit**</span><span class="sxs-lookup"><span data-stu-id="7c61c-280">Example: **WMIC QUIT**</span></span>

</dd> <dt>

<span data-ttu-id="7c61c-281"><span id="EXIT"></span><span id="exit"></span>TERMINER</span><span class="sxs-lookup"><span data-stu-id="7c61c-281"><span id="EXIT"></span><span id="exit"></span>EXIT</span></span>
</dt> <dd>

<span data-ttu-id="7c61c-282">Quittez WMIC.</span><span class="sxs-lookup"><span data-stu-id="7c61c-282">Exit from WMIC.</span></span>

<span data-ttu-id="7c61c-283">Exemple : **sortie WMIC**</span><span class="sxs-lookup"><span data-stu-id="7c61c-283">Example: **WMIC EXIT**</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="7c61c-284">Exemples</span><span class="sxs-lookup"><span data-stu-id="7c61c-284">Examples</span></span>

<span data-ttu-id="7c61c-285">Le [script de définition des paramètres IP/sous-réseau/passerelle/DNS à l’aide de l’exemple WMIC](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) sur la Galerie TechNet décrit comment modifier et mettre à jour les paramètres IP, de sous-réseau, de passerelle et DNS.</span><span class="sxs-lookup"><span data-stu-id="7c61c-285">The [Script for setting IP/Subnet/Gateway/DNS using wmic](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) sample on TechNet Gallery describes how to modify and update IP, Subnet, Gateway, and DNS settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c61c-286">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c61c-286">Requirements</span></span>



| <span data-ttu-id="7c61c-287">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c61c-287">Requirement</span></span> | <span data-ttu-id="7c61c-288">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c61c-288">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="7c61c-289">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c61c-289">Minimum supported client</span></span><br/> | <span data-ttu-id="7c61c-290">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c61c-290">Windows Vista</span></span><br/>       |
| <span data-ttu-id="7c61c-291">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c61c-291">Minimum supported server</span></span><br/> | <span data-ttu-id="7c61c-292">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c61c-292">Windows Server 2008</span></span><br/> |



 

