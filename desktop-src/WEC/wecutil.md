---
title: Wecutil.exe
description: Wecutil.exe est un utilitaire de collecte d’événements Windows qui permet à un administrateur de créer et de gérer des abonnements à des événements transférés à partir de sources d’événements distantes qui prennent en charge le protocole WS-Management.
ms.assetid: 93ce25df-f829-43b9-96f2-7f2f291d100e
ms.tgt_platform: multiple
keywords:
- Wecutil.exe
topic_type:
- apiref
api_name:
- Wecutil.exe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf6f74007b56cff85c28c4106fd4345c5627d4e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104322569"
---
# <a name="wecutilexe"></a><span data-ttu-id="8e96d-104">Wecutil.exe</span><span class="sxs-lookup"><span data-stu-id="8e96d-104">Wecutil.exe</span></span>

<span data-ttu-id="8e96d-105">Wecutil.exe est un utilitaire de collecte d’événements Windows qui permet à un administrateur de créer et de gérer des abonnements à des événements transférés à partir de sources d’événements distantes qui prennent en charge le protocole WS-Management.</span><span class="sxs-lookup"><span data-stu-id="8e96d-105">Wecutil.exe is a Windows Event Collector utility that enables an administrator to create and manage subscriptions to events forwarded from remote event sources that support the WS-Management protocol.</span></span> <span data-ttu-id="8e96d-106">Les commandes, les options et les valeurs d’option ne respectent pas la casse pour cet utilitaire.</span><span class="sxs-lookup"><span data-stu-id="8e96d-106">Commands, options, and option values are case-insensitive for this utility.</span></span>

<span data-ttu-id="8e96d-107">Si vous recevez un message indiquant « le serveur RPC n’est pas disponible » ou « l’interface est inconnue » lorsque vous essayez d’exécuter wecutil, vous devez démarrer le service collecteur d’événements Windows (wecsvc).</span><span class="sxs-lookup"><span data-stu-id="8e96d-107">If you receive a message that says "The RPC server is unavailable" or "The interface is unknown" when you try to run wecutil, then you need to start the Windows Event Collector service (wecsvc).</span></span> <span data-ttu-id="8e96d-108">Pour démarrer wecsvc, à partir d’une invite de commandes avec élévation de privilèges, tapez **net start wecsvc**.</span><span class="sxs-lookup"><span data-stu-id="8e96d-108">To start wecsvc, at an elevated command prompt type **net start wecsvc**.</span></span>

## <a name="list-existing-subscriptions"></a><span data-ttu-id="8e96d-109">Répertorier les abonnements existants</span><span class="sxs-lookup"><span data-stu-id="8e96d-109">List existing subscriptions</span></span>

<span data-ttu-id="8e96d-110">La syntaxe suivante est utilisée pour répertorier les abonnements aux événements distants existants.</span><span class="sxs-lookup"><span data-stu-id="8e96d-110">The following syntax is used to list existing remote event subscriptions.</span></span>

``` syntax
wecutil { es | enum-subscription }
```

<span data-ttu-id="8e96d-111">Si vous utilisez un script pour obtenir les noms des abonnements à partir de la sortie, vous devrez contourner les caractères de la nomenclature UTF-8 sur la première ligne de la sortie.</span><span class="sxs-lookup"><span data-stu-id="8e96d-111">If you use a script to get the names of the subscriptions from the output, you will need to bypass the UTF-8 BOM characters in the first line of the output.</span></span> <span data-ttu-id="8e96d-112">Le script suivant montre un exemple de la façon dont vous pouvez ignorer les caractères de la nomenclature.</span><span class="sxs-lookup"><span data-stu-id="8e96d-112">The following script shows an example of how you might skip the BOM characters.</span></span>

``` syntax
setlocal enabledelayedexpansion

set bomskipped=
for /f %%i in ('wecutil es') do (
    set sub=%%i
    if not defined bomskipped (
        set sub=!sub:~3!
        set bomskipped=yes
    )
    echo !sub!
)
goto :eof

endlocal
```

## <a name="get-subscription-configuration"></a><span data-ttu-id="8e96d-113">Récupération de la configuration de l’abonnement</span><span class="sxs-lookup"><span data-stu-id="8e96d-113">Get subscription configuration</span></span>

<span data-ttu-id="8e96d-114">La syntaxe suivante est utilisée pour afficher les données de configuration de l’abonnement aux événements à distance.</span><span class="sxs-lookup"><span data-stu-id="8e96d-114">The following syntax is used to display remote event subscription configuration data.</span></span>

``` syntax
wecutil { gs | get-subscription } SUBSCRIPTION_ID [/f:VALUE 
[/u:VALUE] ...]
```

## <a name="get-configuration-parameters"></a><span data-ttu-id="8e96d-115">Obtient les paramètres de configuration</span><span class="sxs-lookup"><span data-stu-id="8e96d-115">Get Configuration Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e96d-116"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID d’abonnement \_**</span><span class="sxs-lookup"><span data-stu-id="8e96d-116"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-117">Chaîne qui identifie de façon unique un abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-117">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="8e96d-118">Cet identificateur est spécifié dans l’élément **SubscriptionId** dans le fichier de configuration XML utilisé pour créer l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-118">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-119"><span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f : \* valeur**\*</span><span class="sxs-lookup"><span data-stu-id="8e96d-119"><span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f:\*VALUE**\*</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-120">Valeur qui spécifie la sortie des données de configuration de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-120">A value that specifies the output of the subscription configuration data.</span></span> <span data-ttu-id="8e96d-121">La valeur peut être « XML » ou « laconique », et la *valeur* par défaut est « laconique ».</span><span class="sxs-lookup"><span data-stu-id="8e96d-121">*VALUE* can be "XML" or "Terse", and the default is "Terse".</span></span> <span data-ttu-id="8e96d-122">Si la *valeur* est « XML », la sortie est imprimée au format « XML ».</span><span class="sxs-lookup"><span data-stu-id="8e96d-122">If *VALUE* is "XML", then the output is printed in "XML" format.</span></span> <span data-ttu-id="8e96d-123">Si la *valeur* est « laconique », la sortie est imprimée dans les paires nom-valeur.</span><span class="sxs-lookup"><span data-stu-id="8e96d-123">If *VALUE* is "Terse", then the output is printed in name-value pairs.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-124"><span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u : *valeur***</span><span class="sxs-lookup"><span data-stu-id="8e96d-124"><span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-125">Valeur qui spécifie si la sortie est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="8e96d-125">A value that specifies whether the output is in Unicode format.</span></span> <span data-ttu-id="8e96d-126">La *valeur* peut être « true » ou « false ».</span><span class="sxs-lookup"><span data-stu-id="8e96d-126">*VALUE* can be "true" or "false".</span></span> <span data-ttu-id="8e96d-127">Si la *valeur* est « true », la sortie est au format Unicode et si la *valeur* est « false », la sortie n’est pas au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="8e96d-127">If *VALUE* is "true", then the output is in Unicode format, and if *VALUE* is "false", then the output is not in Unicode format.</span></span>

</dd> </dl>

## <a name="get-subscription-runtime-status"></a><span data-ttu-id="8e96d-128">Obtient l’état d’exécution de l’abonnement</span><span class="sxs-lookup"><span data-stu-id="8e96d-128">Get subscription runtime status</span></span>

<span data-ttu-id="8e96d-129">La syntaxe suivante est utilisée pour afficher l’état d’exécution de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-129">The following syntax is used to display the subscription runtime status.</span></span>

``` syntax
wecutil { gr | get-subscriptionruntimestatus } SUBSCRIPTION_ID
 [EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="get-status-parameters"></a><span data-ttu-id="8e96d-130">Afficher les paramètres d’État</span><span class="sxs-lookup"><span data-stu-id="8e96d-130">Get Status Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e96d-131"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID d’abonnement \_**</span><span class="sxs-lookup"><span data-stu-id="8e96d-131"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-132">Chaîne qui identifie de façon unique un abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-132">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="8e96d-133">Cet identificateur est spécifié dans l’élément **SubscriptionId** dans le fichier de configuration XML utilisé pour créer l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-133">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-134"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**SOURCE de l’événement \_**</span><span class="sxs-lookup"><span data-stu-id="8e96d-134"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**EVENT\_SOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-135">Valeur qui identifie un ordinateur qui est une source d’événements pour un abonnement aux événements.</span><span class="sxs-lookup"><span data-stu-id="8e96d-135">A value that identifies a computer that is an event source for an event subscription.</span></span> <span data-ttu-id="8e96d-136">Cette valeur peut être le nom de domaine complet pour l’ordinateur, le nom NetBIOS ou l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="8e96d-136">This value can be the fully qualified domain name for the computer, NetBIOS name, or IP address.</span></span>

</dd> </dl>

## <a name="set-subscription-configuration-information"></a><span data-ttu-id="8e96d-137">Définir les informations de configuration de l’abonnement</span><span class="sxs-lookup"><span data-stu-id="8e96d-137">Set Subscription Configuration Information</span></span>

<span data-ttu-id="8e96d-138">La syntaxe suivante est utilisée pour définir les données de configuration d’abonnement en modifiant les paramètres d’abonnement à partir de la ligne de commande ou à l’aide d’un fichier de configuration XML.</span><span class="sxs-lookup"><span data-stu-id="8e96d-138">The following syntax is used to set subscription configuration data by changing subscription parameters from the command line or using an XML configuration file.</span></span>

``` syntax
wecutil { ss | set_subscription } SUBSCRIPTION_ID [/e:VALUE] 
[/esa:EVENT_SOURCE [/ese:VALUE] [/aes] [/res] [/un:USERNAME] [/up:PASSWORD]] 
[/d:DESCRIPTION] [/uri:URI] [/cm:CONFIGURATION_MODE] [/ex:DATE_TIME] 
[/q:QUERY] [/dia:DIALECT] [/tn:TRANSPORTNAME] [/tp:TRANSPORTPORT] [/dm:MODE] 
[/dmi:NUMBER] [/dmlt:MS] [/hi:MS] [/cf:FORMAT] [/l:LOCALE] [/ree:[VALUE]] 
[/lf:FILENAME] [/pn:PUBLISHER] [/hn:NAME] [/ct:TYPE] 
[/cun:USERNAME] [/cup:PASSWORD] 
[/ica:THUMBPRINTS] [/as:ALLOWED] [/ds:DENIED] [/adc:SDDL]

wecutil {ss | set_subscription } /c:CONGIG_FILE [/cun:USERNAME] 
[/cup:PASSWORD]
```

### <a name="remarks"></a><span data-ttu-id="8e96d-139">Notes</span><span class="sxs-lookup"><span data-stu-id="8e96d-139">Remarks</span></span>

<span data-ttu-id="8e96d-140">Lorsqu’un nom d’utilisateur ou un mot de passe incorrect est spécifié dans la commande **wecutil SS** , aucune erreur n’est signalée tant que vous n’avez pas affiché l’état d’exécution de l’abonnement à l’aide de la commande **wecutil gr** .</span><span class="sxs-lookup"><span data-stu-id="8e96d-140">When an incorrect username or password is specified in the **wecutil ss** command, no error is reported until you view the runtime status of the subscription using the **wecutil gr** command.</span></span>

## <a name="set-configuration-parameters"></a><span data-ttu-id="8e96d-141">Définir les paramètres de configuration</span><span class="sxs-lookup"><span data-stu-id="8e96d-141">Set Configuration Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e96d-142"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID d’abonnement \_**</span><span class="sxs-lookup"><span data-stu-id="8e96d-142"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-143">Chaîne qui identifie de façon unique un abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-143">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="8e96d-144">Cet identificateur est spécifié dans l’élément **SubscriptionId** dans le fichier de configuration XML utilisé pour créer l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-144">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-145"><span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>***\_ fichier* /c : CONGIG**</span><span class="sxs-lookup"><span data-stu-id="8e96d-145"><span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c: *CONGIG\_FILE***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-146">Valeur qui spécifie le chemin d’accès au fichier XML qui contient les informations de configuration de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-146">A value that specifies the path to the XML file that contains subscription configuration information.</span></span> <span data-ttu-id="8e96d-147">Le chemin d’accès peut être absolu ou relatif au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="8e96d-147">The path can be absolute or relative to the current directory.</span></span> <span data-ttu-id="8e96d-148">Ce paramètre ne peut être utilisé qu’avec les paramètres facultatifs/CUS et/Cup, et s’exclut mutuellement avec tous les autres paramètres.</span><span class="sxs-lookup"><span data-stu-id="8e96d-148">This parameter can only be used with the optional /cus and /cup parameters, and is mutually exclusive with all the other parameters.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-149"><span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e : *valeur***</span><span class="sxs-lookup"><span data-stu-id="8e96d-149"><span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-150">Valeur qui détermine s’il faut activer ou désactiver l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-150">A value that determines whether to enable or disable the subscription.</span></span> <span data-ttu-id="8e96d-151">La valeur peut être true ou false.</span><span class="sxs-lookup"><span data-stu-id="8e96d-151">VALUE can be true or false.</span></span> <span data-ttu-id="8e96d-152">La valeur par défaut est true, ce qui active l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-152">The default value is true, which enables the subscription.</span></span>

> [!Note]  
> <span data-ttu-id="8e96d-153">Lorsque vous désactivez un abonnement initié par le collecteur, la source de l’événement devient inactive au lieu d’être désactivée.</span><span class="sxs-lookup"><span data-stu-id="8e96d-153">When you disable a collector initiated subscription, the event source becomes inactive instead of disabled.</span></span> <span data-ttu-id="8e96d-154">Dans un abonnement initié par le collecteur, vous pouvez désactiver une source d’événements indépendante de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-154">In a collector initiated subscription, you can disable an event source independent of the subscription.</span></span>

 

</dd> <dt>

<span data-ttu-id="8e96d-155"><span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d : *Description***</span><span class="sxs-lookup"><span data-stu-id="8e96d-155"><span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d: *DESCRIPTION***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-156">Valeur qui spécifie une description de l’abonnement aux événements.</span><span class="sxs-lookup"><span data-stu-id="8e96d-156">A value that specifies a description for the event subscription.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-157"><span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ex : *date/ \_ heure***</span><span class="sxs-lookup"><span data-stu-id="8e96d-157"><span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ex: *DATE\_TIME***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-158">Valeur qui spécifie le délai d’expiration de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-158">A value that specifies the subscription expiration time.</span></span> <span data-ttu-id="8e96d-159">*Date \_ L’heure* est une valeur spécifiée au format de date et d’heure standard XML ou ISO8601 : « yyyy-mm-ddThh : mm : SS \[ . sss \] \[ Z \] » où « T » est le séparateur d’heure et « Z » indique l’heure UTC.</span><span class="sxs-lookup"><span data-stu-id="8e96d-159">*DATE\_TIME* is a value specified in standard XML or ISO8601 date-time format: "yyyy-MM-ddThh:mm:ss\[.sss\]\[Z\]" where "T" is the time separator and "Z" indicates UTC time.</span></span> <span data-ttu-id="8e96d-160">Par exemple, si la date et l' *\_ heure* sont « 2007-01-12T01:20:00 », l’heure d’expiration de l’abonnement est le 12 janvier 2007, 01:20.</span><span class="sxs-lookup"><span data-stu-id="8e96d-160">For example, if *DATE\_TIME* is "2007-01-12T01:20:00", then the subscription expiration time is January 12th, 2007, 01:20.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-161"><span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/URI : *URI***</span><span class="sxs-lookup"><span data-stu-id="8e96d-161"><span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/uri: *URI***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-162">Valeur qui spécifie le type d’événements consommés par l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-162">A value that specifies the type of events consumed by the subscription.</span></span> <span data-ttu-id="8e96d-163">L’adresse de l’ordinateur source de l’événement avec l’URI (Uniform Resource Identifier) identifie de façon unique la source des événements.</span><span class="sxs-lookup"><span data-stu-id="8e96d-163">The address of the event source computer along with the uniform resource identifier (URI) uniquely identifies the source of the events.</span></span> <span data-ttu-id="8e96d-164">La chaîne d’URI est utilisée pour toutes les adresses de la source d’événements dans l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-164">The URI string is used for all event source addresses in the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-165"><span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm : *\_ mode de configuration***</span><span class="sxs-lookup"><span data-stu-id="8e96d-165"><span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm: *CONFIGURATION\_MODE***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-166">Valeur qui spécifie le mode de configuration de l’abonnement aux événements.</span><span class="sxs-lookup"><span data-stu-id="8e96d-166">A value that specifies the configuration mode of the event subscription.</span></span> <span data-ttu-id="8e96d-167">*Configuration \_ de Le MODE* peut être l’une des chaînes suivantes : « normal », « Custom », « MinLatency » ou « MinBandwidth ».</span><span class="sxs-lookup"><span data-stu-id="8e96d-167">*CONFIGURATION\_MODE* can be one of the following strings: "Normal", "Custom", "MinLatency", or "MinBandwidth".</span></span> <span data-ttu-id="8e96d-168">L’énumération du mode de configuration de l' [**\_ abonnement \_ \_ EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) définit les modes de configuration.</span><span class="sxs-lookup"><span data-stu-id="8e96d-168">The [**EC\_SUBSCRIPTION\_CONFIGURATION\_MODE**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) enumeration defines the configuration modes.</span></span> <span data-ttu-id="8e96d-169">Les paramètres/DM,/DMI,/Hi et/DMLT ne peuvent être spécifiés que si le mode de configuration est défini sur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="8e96d-169">The /dm, /dmi, /hi, and /dmlt parameters can only be specified if the configuration mode is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-170"><span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q : *requête***</span><span class="sxs-lookup"><span data-stu-id="8e96d-170"><span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q: *QUERY***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-171">Valeur qui spécifie la chaîne de requête pour l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-171">A value that specifies the query string for the subscription.</span></span> <span data-ttu-id="8e96d-172">Le format de cette chaîne peut être différent pour différentes valeurs d’URI et s’applique à toutes les sources d’événements de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-172">The format of this string can be different for different URI values and applies to all event sources in the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-173"><span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/Dia : *dialecte***</span><span class="sxs-lookup"><span data-stu-id="8e96d-173"><span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/dia: *DIALECT***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-174">Valeur qui spécifie le dialecte utilisé par la chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="8e96d-174">A value that specifies the dialect the query string uses.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-175"><span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/CF : *format***</span><span class="sxs-lookup"><span data-stu-id="8e96d-175"><span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/cf: *FORMAT***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-176">Valeur qui spécifie le format des événements retournés.</span><span class="sxs-lookup"><span data-stu-id="8e96d-176">A value that specifies the format of the returned events.</span></span> <span data-ttu-id="8e96d-177">Le *format* peut être « Events » ou « RenderedText ».</span><span class="sxs-lookup"><span data-stu-id="8e96d-177">*FORMAT* can be "Events" or "RenderedText".</span></span> <span data-ttu-id="8e96d-178">Lorsque la valeur est « RenderedText », les événements sont retournés avec les chaînes localisées (telles que les chaînes de description d’événement) attachées aux événements.</span><span class="sxs-lookup"><span data-stu-id="8e96d-178">When the value is "RenderedText", the events are returned with the localized strings (such as event description strings) attached to the events.</span></span> <span data-ttu-id="8e96d-179">La valeur par défaut du *format* est « RenderedText ».</span><span class="sxs-lookup"><span data-stu-id="8e96d-179">The default value of *FORMAT* is "RenderedText".</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-180"><span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l : *paramètres régionaux***</span><span class="sxs-lookup"><span data-stu-id="8e96d-180"><span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l: *LOCALE***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-181">Valeur qui spécifie les paramètres régionaux pour la remise des chaînes localisées au format de texte rendu.</span><span class="sxs-lookup"><span data-stu-id="8e96d-181">A value that specifies the locale for delivery of the localized strings in rendered text format.</span></span> <span data-ttu-id="8e96d-182">Les *paramètres régionaux* sont un identificateur de culture de langue/pays, par exemple « en-US ».</span><span class="sxs-lookup"><span data-stu-id="8e96d-182">*LOCALE* is a language/country culture identifier, for example, "EN-us".</span></span> <span data-ttu-id="8e96d-183">Ce paramètre est valide uniquement lorsque le paramètre/CF est défini sur « RenderedText ».</span><span class="sxs-lookup"><span data-stu-id="8e96d-183">This parameter is only valid when the /cf parameter is set to "RenderedText".</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-184"><span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/REE : \[ *valeur*\]**</span><span class="sxs-lookup"><span data-stu-id="8e96d-184"><span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/ree:\[*VALUE*\]**</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-185">Valeur qui spécifie les événements qui doivent être remis pour l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-185">A value that specifies which events are to be delivered for the subscription.</span></span> <span data-ttu-id="8e96d-186">La *valeur* peut être true ou false.</span><span class="sxs-lookup"><span data-stu-id="8e96d-186">*VALUE* can be true or false.</span></span> <span data-ttu-id="8e96d-187">Lorsque la *valeur* est true, tous les événements existants sont lus à partir des sources d’événements d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-187">When *VALUE* is true, all existing events are read from the subscription event sources.</span></span> <span data-ttu-id="8e96d-188">Quand la *valeur* est false, seuls les événements futurs (arrivant) sont remis.</span><span class="sxs-lookup"><span data-stu-id="8e96d-188">When *VALUE* is false, only future (arriving) events are delivered.</span></span> <span data-ttu-id="8e96d-189">La valeur par défaut est true quand/REE est spécifié sans valeur, et la valeur par défaut est false si/REE n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="8e96d-189">The default is true when /ree is specified without a value, and the default is false if /ree is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-190"><span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/LF : *nom de fichier***</span><span class="sxs-lookup"><span data-stu-id="8e96d-190"><span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/lf: *FILENAME***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-191">Valeur qui spécifie le journal des événements local utilisé pour stocker les événements reçus de l’abonnement aux événements.</span><span class="sxs-lookup"><span data-stu-id="8e96d-191">A value that specifies the local event log that is used to store events received from the event subscription.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-192"><span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/PN : serveur de *publication***</span><span class="sxs-lookup"><span data-stu-id="8e96d-192"><span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/pn: *PUBLISHER***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-193">Valeur qui spécifie le nom de l’éditeur d’événements (fournisseur).</span><span class="sxs-lookup"><span data-stu-id="8e96d-193">A value that specifies the event publisher (provider) name.</span></span> <span data-ttu-id="8e96d-194">Il doit s’agir d’un serveur de publication qui possède ou importe le journal spécifié par le paramètre/LF.</span><span class="sxs-lookup"><span data-stu-id="8e96d-194">It must be a publisher which owns or imports the log specified by the /lf parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-195"><span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/DM : *mode***</span><span class="sxs-lookup"><span data-stu-id="8e96d-195"><span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/dm: *MODE***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-196">Valeur qui spécifie le mode de remise de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-196">A value that specifies the subscription delivery mode.</span></span> <span data-ttu-id="8e96d-197">Le *mode* peut avoir la valeur push ou pull.</span><span class="sxs-lookup"><span data-stu-id="8e96d-197">*MODE* can be either push or pull.</span></span> <span data-ttu-id="8e96d-198">Cette option n’est valide que si le paramètre/cm est défini sur Custom.</span><span class="sxs-lookup"><span data-stu-id="8e96d-198">This option is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-199"><span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/DMI : *nombre***</span><span class="sxs-lookup"><span data-stu-id="8e96d-199"><span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/dmi: *NUMBER***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-200">Valeur qui spécifie le nombre maximal d’éléments pour la remise par lot dans l’abonnement aux événements.</span><span class="sxs-lookup"><span data-stu-id="8e96d-200">A value that specifies the maximum number of items for batched delivery in the event subscription.</span></span> <span data-ttu-id="8e96d-201">Cette option n’est valide que si le paramètre/cm est défini sur Custom.</span><span class="sxs-lookup"><span data-stu-id="8e96d-201">This option is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-202"><span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/DMLT : *MS***</span><span class="sxs-lookup"><span data-stu-id="8e96d-202"><span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/dmlt: *MS***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-203">Valeur qui spécifie la latence maximale autorisée dans la transmission d’un lot d’événements.</span><span class="sxs-lookup"><span data-stu-id="8e96d-203">A value that specifies the maximum latency allowed in delivering a batch of events.</span></span> <span data-ttu-id="8e96d-204">MS est le nombre de millisecondes autorisées.</span><span class="sxs-lookup"><span data-stu-id="8e96d-204">MS is the number of milliseconds allowed.</span></span> <span data-ttu-id="8e96d-205">Ce paramètre n’est valide que si le paramètre/cm est défini sur Custom.</span><span class="sxs-lookup"><span data-stu-id="8e96d-205">This parameter is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-206"><span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/HI : *MS***</span><span class="sxs-lookup"><span data-stu-id="8e96d-206"><span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/hi: *MS***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-207">Valeur qui spécifie l’intervalle de vérification des pulsations pour l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-207">A value that specifies the heartbeat interval for the subscription.</span></span> <span data-ttu-id="8e96d-208">*MS* est le nombre de millisecondes utilisées dans l’intervalle.</span><span class="sxs-lookup"><span data-stu-id="8e96d-208">*MS* is the number of milliseconds used in the interval.</span></span> <span data-ttu-id="8e96d-209">Ce paramètre n’est valide que si le paramètre/cm est défini sur Custom.</span><span class="sxs-lookup"><span data-stu-id="8e96d-209">This parameter is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-210"><span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/TN : *TRANSPORTNAME***</span><span class="sxs-lookup"><span data-stu-id="8e96d-210"><span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/tn: *TRANSPORTNAME***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-211">Valeur qui spécifie le nom du transport utilisé pour se connecter à l’ordinateur source de l’événement distant.</span><span class="sxs-lookup"><span data-stu-id="8e96d-211">A value that specifies the name of the transport used to connect to the remote event source computer.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-212"><span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/ESA : *\_ source* de l’événement**</span><span class="sxs-lookup"><span data-stu-id="8e96d-212"><span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/esa: *EVENT\_SOURCE***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-213">Valeur qui spécifie l’adresse d’un ordinateur source d’événement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-213">A value that specifies the address of an event source computer.</span></span> <span data-ttu-id="8e96d-214">*Événement \_ La SOURCE* est une chaîne qui identifie un ordinateur source d’événements à l’aide du nom de domaine complet pour l’ordinateur, le nom NetBIOS ou l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="8e96d-214">*EVENT\_SOURCE* is a string that identifies an event source computer using the fully qualified domain name for the computer, NetBIOS name, or IP address.</span></span> <span data-ttu-id="8e96d-215">Ce paramètre peut être utilisé avec les paramètres/ESE,/AES,/res, ou/un et/up.</span><span class="sxs-lookup"><span data-stu-id="8e96d-215">This parameter can be used with the /ese, /aes, /res, or /un and /up parameters.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-216"><span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ESE : *valeur***</span><span class="sxs-lookup"><span data-stu-id="8e96d-216"><span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ese: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-217">Valeur qui détermine s’il faut activer ou désactiver une source d’événement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-217">A value that determines whether to enable or disable an event source.</span></span> <span data-ttu-id="8e96d-218">La *valeur* peut être true ou false.</span><span class="sxs-lookup"><span data-stu-id="8e96d-218">*VALUE* can be true or false.</span></span> <span data-ttu-id="8e96d-219">La valeur par défaut est true, ce qui active la source de l’événement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-219">The default value is true, which enables the event source.</span></span> <span data-ttu-id="8e96d-220">Ce paramètre est utilisé uniquement si le paramètre/ESA est utilisé.</span><span class="sxs-lookup"><span data-stu-id="8e96d-220">This parameter is only used if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-221"><span id="_aes"></span><span id="_AES"></span>**/aes**</span><span class="sxs-lookup"><span data-stu-id="8e96d-221"><span id="_aes"></span><span id="_AES"></span>**/aes**</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-222">Valeur qui ajoute la source d’événements spécifiée par le paramètre/ESA si la source d’événements ne fait pas déjà partie de l’abonnement aux événements.</span><span class="sxs-lookup"><span data-stu-id="8e96d-222">A value that adds the event source specified by the /esa parameter if the event source is not already part of the event subscription.</span></span> <span data-ttu-id="8e96d-223">Si l’ordinateur spécifié par le paramètre/ESA fait déjà partie de l’abonnement, une erreur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8e96d-223">If the computer specified by the /esa parameter is already a part of the subscription, then an error is displayed.</span></span> <span data-ttu-id="8e96d-224">Ce paramètre est autorisé uniquement si le paramètre/ESA est utilisé.</span><span class="sxs-lookup"><span data-stu-id="8e96d-224">This parameter is allowed only if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-225"><span id="_res"></span><span id="_RES"></span>**/res**</span><span class="sxs-lookup"><span data-stu-id="8e96d-225"><span id="_res"></span><span id="_RES"></span>**/res**</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-226">Valeur qui supprime la source d’événements spécifiée par le paramètre/ESA si la source de l’événement fait déjà partie de l’abonnement aux événements.</span><span class="sxs-lookup"><span data-stu-id="8e96d-226">A value that removes the event source specified by the /esa parameter if the event source is already part of the event subscription.</span></span> <span data-ttu-id="8e96d-227">Si l’ordinateur spécifié par le paramètre/ESA ne fait pas partie de l’abonnement, une erreur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8e96d-227">If the computer specified by the /esa parameter is not part of the subscription, then an error is displayed.</span></span> <span data-ttu-id="8e96d-228">Ce paramètre est autorisé uniquement si le paramètre/ESA est utilisé.</span><span class="sxs-lookup"><span data-stu-id="8e96d-228">This parameter is allowed only if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-229"><span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/un : *nom d’utilisateur***</span><span class="sxs-lookup"><span data-stu-id="8e96d-229"><span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/un: *USERNAME***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-230">Valeur qui spécifie le nom d’utilisateur utilisé dans les informations d’identification pour se connecter à la source d’événements spécifiée dans le paramètre/ESA.</span><span class="sxs-lookup"><span data-stu-id="8e96d-230">A value that specifies the user name used in the credentials to connect to the event source specified in the /esa parameter.</span></span> <span data-ttu-id="8e96d-231">Ce paramètre est autorisé uniquement si le paramètre/ESA est utilisé.</span><span class="sxs-lookup"><span data-stu-id="8e96d-231">This parameter is allowed only if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-232"><span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/Up : *mot de passe***</span><span class="sxs-lookup"><span data-stu-id="8e96d-232"><span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/up: *PASSWORD***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-233">Valeur qui spécifie le mot de passe pour le nom d’utilisateur spécifié dans le paramètre/un.</span><span class="sxs-lookup"><span data-stu-id="8e96d-233">A value that specifies the password for the user name specified in the /un parameter.</span></span> <span data-ttu-id="8e96d-234">Les informations d’identification de nom d’utilisateur et de mot de passe sont utilisées pour la connexion à la source d’événements spécifiée dans le paramètre/ESA.</span><span class="sxs-lookup"><span data-stu-id="8e96d-234">The user name and password credentials are used to connect to the event source specified in the /esa parameter.</span></span> <span data-ttu-id="8e96d-235">Ce paramètre est autorisé uniquement si le paramètre/un est utilisé.</span><span class="sxs-lookup"><span data-stu-id="8e96d-235">This parameter is allowed only if the /un parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-236"><span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/TP : *TRANSPORTPORT***</span><span class="sxs-lookup"><span data-stu-id="8e96d-236"><span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/tp: *TRANSPORTPORT***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-237">Valeur qui spécifie le numéro de port utilisé par le transport lors de la connexion à un ordinateur source d’événement distant.</span><span class="sxs-lookup"><span data-stu-id="8e96d-237">A value that specifies the port number used by the transport when connecting to a remote event source computer.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-238"><span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/HN : *nom***</span><span class="sxs-lookup"><span data-stu-id="8e96d-238"><span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/hn: *NAME***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-239">Valeur qui spécifie le nom DNS de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="8e96d-239">A value that specifies the DNS name of the local computer.</span></span> <span data-ttu-id="8e96d-240">Ce nom est utilisé par les sources d’événements distantes pour effectuer un push des événements et doit être utilisé uniquement pour les abonnements par envoi de notification.</span><span class="sxs-lookup"><span data-stu-id="8e96d-240">This name is used by remote event sources to push back events and must be used for push subscriptions only.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-241"><span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/CT : *type***</span><span class="sxs-lookup"><span data-stu-id="8e96d-241"><span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/ct: *TYPE***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-242">Valeur qui spécifie le type d’informations d’identification utilisé pour accéder aux sources d’événements distantes.</span><span class="sxs-lookup"><span data-stu-id="8e96d-242">A value that specifies the credential type used for accessing remote event sources.</span></span> <span data-ttu-id="8e96d-243">Le *type* peut être « default », « Negotiate », « Digest », « Basic » ou « LocalMachine ».</span><span class="sxs-lookup"><span data-stu-id="8e96d-243">*TYPE* can be "default", "negotiate", "digest", "basic", or "localmachine".</span></span> <span data-ttu-id="8e96d-244">La valeur par défaut est « default ».</span><span class="sxs-lookup"><span data-stu-id="8e96d-244">The default is "default".</span></span> <span data-ttu-id="8e96d-245">Ces valeurs sont définies dans l’énumération de [**\_ \_ \_ type des informations d’identification de l’abonnement EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) .</span><span class="sxs-lookup"><span data-stu-id="8e96d-245">These values are defined in the [**EC\_SUBSCRIPTION\_CREDENTIALS\_TYPE**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-246"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/CUN : *nom d’utilisateur***</span><span class="sxs-lookup"><span data-stu-id="8e96d-246"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *USERNAME***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-247">Valeur qui définit les informations d’identification de l’utilisateur partagé utilisées pour les sources d’événements qui n’ont pas leurs propres informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8e96d-247">A value that sets the shared user credentials used for event sources that do not have their own user credentials.</span></span>

> [!Note]  
> <span data-ttu-id="8e96d-248">Si ce paramètre est utilisé avec l’option/c, les paramètres de nom d’utilisateur et de mot de passe pour les sources d’événements individuels à partir du fichier de configuration sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="8e96d-248">If this parameter is used with the /c option, then user name and password settings for individual event sources from the configuration file are ignored.</span></span> <span data-ttu-id="8e96d-249">Si vous souhaitez utiliser des informations d’identification différentes pour une source d’événement spécifique, vous pouvez remplacer cette valeur en spécifiant les paramètres/un et/up pour une source d’événement spécifique sur la ligne de commande d’une autre commande Set-Subscription.</span><span class="sxs-lookup"><span data-stu-id="8e96d-249">If you want to use different credentials for a specific event source, you can override this value by specifying the /un and /up parameters for a specific event source on the command line of another set-subscription command.</span></span>

 

</dd> <dt>

<span data-ttu-id="8e96d-250"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/Cup : *mot de passe***</span><span class="sxs-lookup"><span data-stu-id="8e96d-250"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup: *PASSWORD***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-251">Valeur qui définit le mot de passe de l’utilisateur pour les informations d’identification de l’utilisateur partagé.</span><span class="sxs-lookup"><span data-stu-id="8e96d-251">A value that sets the user password for the shared user credentials.</span></span> <span data-ttu-id="8e96d-252">Lorsque le *mot de passe* est défini sur \* (astérisque), le mot de passe est lu à partir de la console.</span><span class="sxs-lookup"><span data-stu-id="8e96d-252">When *PASSWORD* is set to \* (asterisk), then the password is read from the console.</span></span> <span data-ttu-id="8e96d-253">Cette option n’est valide que si le paramètre/cun est spécifié.</span><span class="sxs-lookup"><span data-stu-id="8e96d-253">This option is only valid when the /cun parameter is specified.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-254"><span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ICA : *empreintes numériques***</span><span class="sxs-lookup"><span data-stu-id="8e96d-254"><span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ica: *THUMBPRINTS***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-255">Valeur qui définit la liste des empreintes du certificat de l’émetteur, dans une liste séparée par des virgules.</span><span class="sxs-lookup"><span data-stu-id="8e96d-255">A value that sets the list of issuer certificate thumb prints, in a comma-separated list.</span></span>

> [!Note]  
> <span data-ttu-id="8e96d-256">Cette option est spécifique uniquement aux abonnements initiés par la source.</span><span class="sxs-lookup"><span data-stu-id="8e96d-256">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> <dt>

<span data-ttu-id="8e96d-257"><span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/As : *autorisé***</span><span class="sxs-lookup"><span data-stu-id="8e96d-257"><span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/as: *ALLOWED***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-258">Valeur qui définit une liste de chaînes séparées par des virgules qui spécifient les noms DNS des ordinateurs qui n’appartiennent pas à un domaine et qui sont autorisés à initier des abonnements.</span><span class="sxs-lookup"><span data-stu-id="8e96d-258">A value that sets a comma-separated list of string that specify the DNS names of non-domain computers that are allowed to initiate subscriptions.</span></span> <span data-ttu-id="8e96d-259">Les noms peuvent être spécifiés à l’aide de caractères génériques, tels que « \* . mydomain.com ».</span><span class="sxs-lookup"><span data-stu-id="8e96d-259">The names can be specified using wildcards, such as "\*.mydomain.com".</span></span> <span data-ttu-id="8e96d-260">Par défaut, cette liste est vide.</span><span class="sxs-lookup"><span data-stu-id="8e96d-260">By default, this list is empty.</span></span>

> [!Note]  
> <span data-ttu-id="8e96d-261">Cette option est spécifique uniquement aux abonnements initiés par la source.</span><span class="sxs-lookup"><span data-stu-id="8e96d-261">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> <dt>

<span data-ttu-id="8e96d-262"><span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/DS : *refusé***</span><span class="sxs-lookup"><span data-stu-id="8e96d-262"><span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/ds: *DENIED***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-263">Valeur qui définit une liste de chaînes séparées par des virgules qui spécifient les noms DNS des ordinateurs n’appartenant pas à un domaine qui ne sont pas autorisés à initier des abonnements.</span><span class="sxs-lookup"><span data-stu-id="8e96d-263">A value that sets a comma-separated list of string that specify the DNS names of non-domain computers that are not allowed to initiate subscriptions.</span></span> <span data-ttu-id="8e96d-264">Les noms peuvent être spécifiés à l’aide de caractères génériques, tels que « \* . mydomain.com ».</span><span class="sxs-lookup"><span data-stu-id="8e96d-264">The names can be specified using wildcards, such as "\*.mydomain.com".</span></span> <span data-ttu-id="8e96d-265">Par défaut, cette liste est vide.</span><span class="sxs-lookup"><span data-stu-id="8e96d-265">By default, this list is empty.</span></span>

> [!Note]  
> <span data-ttu-id="8e96d-266">Cette option est spécifique uniquement aux abonnements initiés par la source.</span><span class="sxs-lookup"><span data-stu-id="8e96d-266">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> <dt>

<span data-ttu-id="8e96d-267"><span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/ADC : *SDDL***</span><span class="sxs-lookup"><span data-stu-id="8e96d-267"><span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/adc: *SDDL***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-268">Valeur qui définit une chaîne, au format SDDL, qui spécifie les ordinateurs de domaine qui sont autorisés ou non à initier des abonnements.</span><span class="sxs-lookup"><span data-stu-id="8e96d-268">A value that sets a string, in SDDL format, that specifies which domain computers are allowed or not allowed to initiate subscriptions.</span></span> <span data-ttu-id="8e96d-269">La valeur par défaut consiste à autoriser tous les ordinateurs du domaine à initier des abonnements.</span><span class="sxs-lookup"><span data-stu-id="8e96d-269">The default is to allow all domain computers to initiate subscriptions.</span></span>

> [!Note]  
> <span data-ttu-id="8e96d-270">Cette option est spécifique uniquement aux abonnements initiés par la source.</span><span class="sxs-lookup"><span data-stu-id="8e96d-270">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> </dl>

## <a name="create-a-new-subscription"></a><span data-ttu-id="8e96d-271">Créer un abonnement</span><span class="sxs-lookup"><span data-stu-id="8e96d-271">Create a New Subscription</span></span>

<span data-ttu-id="8e96d-272">La syntaxe suivante est utilisée pour créer un abonnement aux événements sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="8e96d-272">The following syntax is used to create an event subscription for events on a remote computer.</span></span>

``` syntax
wecutil {cs | create-subscription } CONFIGURATION_FILE [/cun:USERNAME]
[/cup:PASSWORD] 
```

### <a name="remarks"></a><span data-ttu-id="8e96d-273">Notes</span><span class="sxs-lookup"><span data-stu-id="8e96d-273">Remarks</span></span>

<span data-ttu-id="8e96d-274">Lorsqu’un nom d’utilisateur ou un mot de passe incorrect est spécifié dans la commande **wecutil CS** , aucune erreur n’est signalée tant que vous n’avez pas affiché l’état d’exécution de l’abonnement à l’aide de la commande **wecutil gr** .</span><span class="sxs-lookup"><span data-stu-id="8e96d-274">When an incorrect username or password is specified in the **wecutil cs** command, no error is reported until you view the runtime status of the subscription using the **wecutil gr** command.</span></span>

## <a name="creation-parameters"></a><span data-ttu-id="8e96d-275">Paramètres de création</span><span class="sxs-lookup"><span data-stu-id="8e96d-275">Creation Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e96d-276"><span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**fichier de CONFIGURATION \_**</span><span class="sxs-lookup"><span data-stu-id="8e96d-276"><span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**CONFIGURATION\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-277">Valeur qui spécifie le chemin d’accès au fichier XML qui contient les informations de configuration de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-277">A value that specifies the path to the XML file that contains subscription configuration information.</span></span> <span data-ttu-id="8e96d-278">Le chemin d’accès peut être absolu ou relatif au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="8e96d-278">The path can be absolute or relative to the current directory.</span></span>

<span data-ttu-id="8e96d-279">Le code XML suivant est un exemple de fichier de configuration d’abonnement qui crée un abonnement initié par le collecteur pour transférer des événements du journal des événements d’application d’un ordinateur distant vers le journal ForwardedEvents.</span><span class="sxs-lookup"><span data-stu-id="8e96d-279">The following XML is an example of a subscription configuration file that creates a collector initiated subscription to forward events from the Application event log of a remote computer to the ForwardedEvents log.</span></span>


```XML
<Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
    <SubscriptionId>SampleCISubscription</SubscriptionId>
    <SubscriptionType>CollectorInitiated</SubscriptionType>
    <Description>Collector Initiated Subscription Sample</Description>
    <Enabled>true</Enabled>
    <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

    <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
    <ConfigurationMode>Custom</ConfigurationMode>

    <Delivery Mode="Push">
        <Batching>
            <MaxItems>20</MaxItems>
            <MaxLatencyTime>60000</MaxLatencyTime>
        </Batching>
        <PushSettings>
            <HostName>thisMachine.myDomain.com</HostName>
            <Heartbeat Interval="60000"/>
        </PushSettings>
    </Delivery>

    <Expires>2010-01-01T00:00:00.000Z</Expires>

    <Query>
        <![CDATA[
            <QueryList>
                <Query Path="Application">
                    <Select>*</Select>
                </Query>
            </QueryList>
        ]]>
    </Query>

    <ReadExistingEvents>false</ReadExistingEvents>
    <TransportName>http</TransportName>
    <ContentFormat>RenderedText</ContentFormat>
    <Locale Language="en-US"/>
    <LogFile>ForwardedEvents</LogFile>
    <CredentialsType>Default</CredentialsType>

    <EventSources>
        <EventSource Enabled="true">
            <Address>mySource.myDomain.com</Address>
            <UserName>myUserName</UserName>
        </EventSource>
    </EventSources>
</Subscription>
```



<span data-ttu-id="8e96d-280">Le code XML suivant est un exemple de fichier de configuration d’abonnement qui crée un abonnement initié par la source pour transférer les événements du journal des événements d’application d’un ordinateur distant vers le journal ForwardedEvents.</span><span class="sxs-lookup"><span data-stu-id="8e96d-280">The following XML is an example of a subscription configuration file that creates a source initiated subscription to forward events from the Application event log of a remote computer to the ForwardedEvents log.</span></span>


```XML
<Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
    <SubscriptionId>SampleSISubscription</SubscriptionId>
    <SubscriptionType>SourceInitiated</SubscriptionType>
    <Description>Source Initiated Subscription Sample</Description>
    <Enabled>true</Enabled>
    <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

    <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
    <ConfigurationMode>Custom</ConfigurationMode>

    <Delivery Mode="Push">
        <Batching>
            <MaxItems>1</MaxItems>
            <MaxLatencyTime>1000</MaxLatencyTime>
        </Batching>
        <PushSettings>
            <Heartbeat Interval="60000"/>
        </PushSettings>
    </Delivery>

    <Expires>2018-01-01T00:00:00.000Z</Expires>

    <Query>
        <![CDATA[
            <QueryList>
                <Query Path="Application">
                    <Select>Event[System/EventID='999']</Select>
                </Query>
            </QueryList>
        ]]>
    </Query>

    <ReadExistingEvents>true</ReadExistingEvents>
    <TransportName>http</TransportName>
    <ContentFormat>RenderedText</ContentFormat>
    <Locale Language="en-US"/>
    <LogFile>ForwardedEvents</LogFile>
    <AllowedSourceNonDomainComputers></AllowedSourceNonDomainComputers>
    <AllowedSourceDomainComputers>O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)</AllowedSourceDomainComputers>
</Subscription>
```



> [!Note]  
> <span data-ttu-id="8e96d-281">Lors de la création d’un abonnement initié par la source, si **AllowedSourceDomainComputers**, **AllowedSourceNonDomainComputers** / **IssuerCAList**, **AllowedSubjectList** et **DeniedSubjectList** sont tous vides, une valeur par défaut est fournie pour **AllowedSourceDomainComputers** -"O :NSG : NSD : (a ;; GA ;;;D C) (A ;; GA ;;; NS)».</span><span class="sxs-lookup"><span data-stu-id="8e96d-281">When creating a source initiated subscription, if **AllowedSourceDomainComputers**, **AllowedSourceNonDomainComputers**/**IssuerCAList**, **AllowedSubjectList**, and **DeniedSubjectList** are all empty, then a default will be provided for **AllowedSourceDomainComputers** - "O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)".</span></span> <span data-ttu-id="8e96d-282">Cette valeur SDDL accorde par défaut les membres du groupe de domaine ordinateurs du domaine, ainsi que le groupe de service réseau local (pour le redirecteur local), la possibilité de déclencher des événements pour cet abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-282">This SDDL default grants members of the Domain Computers domain group, as well as the local Network Service group (for the local forwarder), the ability to raise events for this subscription.</span></span>

 

</dd> <dt>

<span data-ttu-id="8e96d-283"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/CUN : *nom d’utilisateur***</span><span class="sxs-lookup"><span data-stu-id="8e96d-283"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *USERNAME***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-284">Valeur qui définit les informations d’identification de l’utilisateur partagé utilisées pour les sources d’événements qui n’ont pas leurs propres informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8e96d-284">A value that sets the shared user credentials used for event sources that do not have their own user credentials.</span></span> <span data-ttu-id="8e96d-285">Cette valeur s’applique uniquement aux abonnements initiés par le collecteur.</span><span class="sxs-lookup"><span data-stu-id="8e96d-285">This value applies to collector initiated subscriptions only.</span></span>

> [!Note]  
> <span data-ttu-id="8e96d-286">Si ce paramètre est spécifié, les paramètres de nom d’utilisateur et de mot de passe pour les sources d’événements individuels à partir du fichier de configuration sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="8e96d-286">If this parameter is specified, then user name and password settings for individual event sources from the configuration file are ignored.</span></span> <span data-ttu-id="8e96d-287">Si vous souhaitez utiliser des informations d’identification différentes pour une source d’événement spécifique, vous pouvez remplacer cette valeur en spécifiant les paramètres/un et/up pour une source d’événement spécifique sur la ligne de commande d’une autre commande Set-Subscription.</span><span class="sxs-lookup"><span data-stu-id="8e96d-287">If you want to use different credentials for a specific event source, you can override this value by specifying the /un and /up parameters for a specific event source on the command line of another set-subscription command.</span></span>

 

</dd> <dt>

<span data-ttu-id="8e96d-288"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/Cup : *mot de passe***</span><span class="sxs-lookup"><span data-stu-id="8e96d-288"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup: *PASSWORD***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-289">Valeur qui définit le mot de passe de l’utilisateur pour les informations d’identification de l’utilisateur partagé.</span><span class="sxs-lookup"><span data-stu-id="8e96d-289">A value that sets the user password for the shared user credentials.</span></span> <span data-ttu-id="8e96d-290">Lorsque le *mot de passe* est défini sur « \* » (astérisque), le mot de passe est lu à partir de la console.</span><span class="sxs-lookup"><span data-stu-id="8e96d-290">When *PASSWORD* is set to "\*" (asterisk), then the password is read from the console.</span></span> <span data-ttu-id="8e96d-291">Cette option n’est valide que si le paramètre/cun est spécifié.</span><span class="sxs-lookup"><span data-stu-id="8e96d-291">This option is only valid when the /cun parameter is specified.</span></span>

</dd> </dl>

## <a name="delete-a-subscription"></a><span data-ttu-id="8e96d-292">Supprimer un abonnement</span><span class="sxs-lookup"><span data-stu-id="8e96d-292">Delete a Subscription</span></span>

<span data-ttu-id="8e96d-293">La syntaxe suivante est utilisée pour supprimer un abonnement aux événements.</span><span class="sxs-lookup"><span data-stu-id="8e96d-293">The following syntax is used to delete an event subscription.</span></span>

``` syntax
wecutil { ds | delete-subscription } SUBSCRIPTION_ID
```

## <a name="deletion-parameters"></a><span data-ttu-id="8e96d-294">Paramètres de suppression</span><span class="sxs-lookup"><span data-stu-id="8e96d-294">Deletion Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e96d-295"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID d’abonnement \_**</span><span class="sxs-lookup"><span data-stu-id="8e96d-295"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-296">Chaîne qui identifie de façon unique un abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-296">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="8e96d-297">Cet identificateur est spécifié dans l’élément **SubscriptionId** dans le fichier de configuration XML utilisé pour créer l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-297">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span> <span data-ttu-id="8e96d-298">L’abonnement identifié dans ce paramètre sera supprimé.</span><span class="sxs-lookup"><span data-stu-id="8e96d-298">The subscription identified in this parameter will be deleted.</span></span>

</dd> </dl>

## <a name="retry-a-subscription"></a><span data-ttu-id="8e96d-299">Réessayer un abonnement</span><span class="sxs-lookup"><span data-stu-id="8e96d-299">Retry a subscription</span></span>

<span data-ttu-id="8e96d-300">La syntaxe suivante est utilisée pour réessayer un abonnement inactif en tentant de réactiver toutes les sources d’événements ou spécifiées en établissant une connexion à chaque source d’événement et en envoyant une demande d’abonnement à distance à la source de l’événement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-300">The following syntax is used to retry an inactive subscription by attempting to reactivate all or specified event sources by establishing a connection to each event source and sending a remote subscription request to the event source.</span></span> <span data-ttu-id="8e96d-301">Les sources d’événements désactivées ne sont pas retentées.</span><span class="sxs-lookup"><span data-stu-id="8e96d-301">Disabled event sources are not retried.</span></span>

``` syntax
wecutil { rs | retry-subscription } SUBSCRIPTION_ID 
[EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="retry-parameters"></a><span data-ttu-id="8e96d-302">Paramètres de nouvelle tentative</span><span class="sxs-lookup"><span data-stu-id="8e96d-302">Retry Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e96d-303"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID d’abonnement \_**</span><span class="sxs-lookup"><span data-stu-id="8e96d-303"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-304">Chaîne qui identifie de façon unique un abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-304">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="8e96d-305">Cet identificateur est spécifié dans l’élément **SubscriptionId** dans le fichier de configuration XML utilisé pour créer l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e96d-305">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span> <span data-ttu-id="8e96d-306">L’abonnement identifié dans ce paramètre sera retenté.</span><span class="sxs-lookup"><span data-stu-id="8e96d-306">The subscription identified in this parameter will be retried.</span></span>

</dd> <dt>

<span data-ttu-id="8e96d-307"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**SOURCE de l’événement \_**</span><span class="sxs-lookup"><span data-stu-id="8e96d-307"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**EVENT\_SOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-308">Valeur qui identifie un ordinateur qui est une source d’événements pour un abonnement aux événements.</span><span class="sxs-lookup"><span data-stu-id="8e96d-308">A value that identifies a computer that is an event source for an event subscription.</span></span> <span data-ttu-id="8e96d-309">Cette valeur peut être le nom de domaine complet pour l’ordinateur, le nom NetBIOS ou l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="8e96d-309">This value can be the fully qualified domain name for the computer, NetBIOS name, or IP address.</span></span>

</dd> </dl>

## <a name="configure-the-windows-event-collector-service"></a><span data-ttu-id="8e96d-310">Configurer le service collecteur d’événements Windows</span><span class="sxs-lookup"><span data-stu-id="8e96d-310">Configure the Windows Event Collector Service</span></span>

<span data-ttu-id="8e96d-311">La syntaxe suivante est utilisée pour configurer le service collecteur d’événements Windows afin de s’assurer que les abonnements d’événements peuvent être créés et maintenus au redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8e96d-311">The following syntax is used to configure the Windows Event Collector service to ensure event subscriptions can be created and sustained through computer restarts.</span></span> <span data-ttu-id="8e96d-312">Cela comprend la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="8e96d-312">This includes the following procedure:</span></span>

<span data-ttu-id="8e96d-313">**Pour configurer le service collecteur d’événements Windows**</span><span class="sxs-lookup"><span data-stu-id="8e96d-313">**To configure the Windows Event Collector service**</span></span>

1.  <span data-ttu-id="8e96d-314">Activez le canal ForwardedEvents s’il est désactivé.</span><span class="sxs-lookup"><span data-stu-id="8e96d-314">Enable the ForwardedEvents channel if it is disabled.</span></span>
2.  <span data-ttu-id="8e96d-315">Retardez le démarrage du service collecteur d’événements Windows.</span><span class="sxs-lookup"><span data-stu-id="8e96d-315">Delay the start of the Windows Event Collector service.</span></span>
3.  <span data-ttu-id="8e96d-316">Démarrez le service collecteur d’événements Windows s’il n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="8e96d-316">Start the Windows Event Collector service if it is not running.</span></span>

``` syntax
wecutil { qc | quick-config } /q:VALUE
```

## <a name="configure-event-collector-parameters"></a><span data-ttu-id="8e96d-317">Configurer les paramètres du collecteur d’événements</span><span class="sxs-lookup"><span data-stu-id="8e96d-317">Configure Event Collector Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e96d-318"><span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q : *valeur***</span><span class="sxs-lookup"><span data-stu-id="8e96d-318"><span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="8e96d-319">Valeur qui détermine si la commande de configuration rapide demande une confirmation.</span><span class="sxs-lookup"><span data-stu-id="8e96d-319">A value that determines whether the quick-config command will prompt for confirmation.</span></span> <span data-ttu-id="8e96d-320">La valeur peut être true ou false.</span><span class="sxs-lookup"><span data-stu-id="8e96d-320">VALUE can be true or false.</span></span> <span data-ttu-id="8e96d-321">Si la valeur est true, la commande vous invite à confirmer l’opération.</span><span class="sxs-lookup"><span data-stu-id="8e96d-321">If VALUE is true, then the command will prompt for confirmation.</span></span> <span data-ttu-id="8e96d-322">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="8e96d-322">The default value is false.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e96d-323">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e96d-323">Requirements</span></span>



| <span data-ttu-id="8e96d-324">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e96d-324">Requirement</span></span> | <span data-ttu-id="8e96d-325">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e96d-325">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8e96d-326">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e96d-326">Minimum supported client</span></span><br/> | <span data-ttu-id="8e96d-327">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e96d-327">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8e96d-328">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e96d-328">Minimum supported server</span></span><br/> | <span data-ttu-id="8e96d-329">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e96d-329">Windows Server 2008</span></span><br/> |



 

 





