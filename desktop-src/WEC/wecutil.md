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
# <a name="wecutilexe"></a>Wecutil.exe

Wecutil.exe est un utilitaire de collecte d’événements Windows qui permet à un administrateur de créer et de gérer des abonnements à des événements transférés à partir de sources d’événements distantes qui prennent en charge le protocole WS-Management. Les commandes, les options et les valeurs d’option ne respectent pas la casse pour cet utilitaire.

Si vous recevez un message indiquant « le serveur RPC n’est pas disponible » ou « l’interface est inconnue » lorsque vous essayez d’exécuter wecutil, vous devez démarrer le service collecteur d’événements Windows (wecsvc). Pour démarrer wecsvc, à partir d’une invite de commandes avec élévation de privilèges, tapez **net start wecsvc**.

## <a name="list-existing-subscriptions"></a>Répertorier les abonnements existants

La syntaxe suivante est utilisée pour répertorier les abonnements aux événements distants existants.

``` syntax
wecutil { es | enum-subscription }
```

Si vous utilisez un script pour obtenir les noms des abonnements à partir de la sortie, vous devrez contourner les caractères de la nomenclature UTF-8 sur la première ligne de la sortie. Le script suivant montre un exemple de la façon dont vous pouvez ignorer les caractères de la nomenclature.

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

## <a name="get-subscription-configuration"></a>Récupération de la configuration de l’abonnement

La syntaxe suivante est utilisée pour afficher les données de configuration de l’abonnement aux événements à distance.

``` syntax
wecutil { gs | get-subscription } SUBSCRIPTION_ID [/f:VALUE 
[/u:VALUE] ...]
```

## <a name="get-configuration-parameters"></a>Obtient les paramètres de configuration

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID d’abonnement \_**
</dt> <dd>

Chaîne qui identifie de façon unique un abonnement. Cet identificateur est spécifié dans l’élément **SubscriptionId** dans le fichier de configuration XML utilisé pour créer l’abonnement.

</dd> <dt>

<span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f : * valeur***
</dt> <dd>

Valeur qui spécifie la sortie des données de configuration de l’abonnement. La valeur peut être « XML » ou « laconique », et la *valeur* par défaut est « laconique ». Si la *valeur* est « XML », la sortie est imprimée au format « XML ». Si la *valeur* est « laconique », la sortie est imprimée dans les paires nom-valeur.

</dd> <dt>

<span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u : *valeur***
</dt> <dd>

Valeur qui spécifie si la sortie est au format Unicode. La *valeur* peut être « true » ou « false ». Si la *valeur* est « true », la sortie est au format Unicode et si la *valeur* est « false », la sortie n’est pas au format Unicode.

</dd> </dl>

## <a name="get-subscription-runtime-status"></a>Obtient l’état d’exécution de l’abonnement

La syntaxe suivante est utilisée pour afficher l’état d’exécution de l’abonnement.

``` syntax
wecutil { gr | get-subscriptionruntimestatus } SUBSCRIPTION_ID
 [EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="get-status-parameters"></a>Afficher les paramètres d’État

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID d’abonnement \_**
</dt> <dd>

Chaîne qui identifie de façon unique un abonnement. Cet identificateur est spécifié dans l’élément **SubscriptionId** dans le fichier de configuration XML utilisé pour créer l’abonnement.

</dd> <dt>

<span id="EVENT_SOURCE"></span><span id="event_source"></span>**SOURCE de l’événement \_**
</dt> <dd>

Valeur qui identifie un ordinateur qui est une source d’événements pour un abonnement aux événements. Cette valeur peut être le nom de domaine complet pour l’ordinateur, le nom NetBIOS ou l’adresse IP.

</dd> </dl>

## <a name="set-subscription-configuration-information"></a>Définir les informations de configuration de l’abonnement

La syntaxe suivante est utilisée pour définir les données de configuration d’abonnement en modifiant les paramètres d’abonnement à partir de la ligne de commande ou à l’aide d’un fichier de configuration XML.

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

### <a name="remarks"></a>Notes

Lorsqu’un nom d’utilisateur ou un mot de passe incorrect est spécifié dans la commande **wecutil SS** , aucune erreur n’est signalée tant que vous n’avez pas affiché l’état d’exécution de l’abonnement à l’aide de la commande **wecutil gr** .

## <a name="set-configuration-parameters"></a>Définir les paramètres de configuration

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID d’abonnement \_**
</dt> <dd>

Chaîne qui identifie de façon unique un abonnement. Cet identificateur est spécifié dans l’élément **SubscriptionId** dans le fichier de configuration XML utilisé pour créer l’abonnement.

</dd> <dt>

<span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>***\_ fichier* /c : CONGIG**
</dt> <dd>

Valeur qui spécifie le chemin d’accès au fichier XML qui contient les informations de configuration de l’abonnement. Le chemin d’accès peut être absolu ou relatif au répertoire actif. Ce paramètre ne peut être utilisé qu’avec les paramètres facultatifs/CUS et/Cup, et s’exclut mutuellement avec tous les autres paramètres.

</dd> <dt>

<span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e : *valeur***
</dt> <dd>

Valeur qui détermine s’il faut activer ou désactiver l’abonnement. La valeur peut être true ou false. La valeur par défaut est true, ce qui active l’abonnement.

> [!Note]  
> Lorsque vous désactivez un abonnement initié par le collecteur, la source de l’événement devient inactive au lieu d’être désactivée. Dans un abonnement initié par le collecteur, vous pouvez désactiver une source d’événements indépendante de l’abonnement.

 

</dd> <dt>

<span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d : *Description***
</dt> <dd>

Valeur qui spécifie une description de l’abonnement aux événements.

</dd> <dt>

<span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ex : *date/ \_ heure***
</dt> <dd>

Valeur qui spécifie le délai d’expiration de l’abonnement. *Date \_ L’heure* est une valeur spécifiée au format de date et d’heure standard XML ou ISO8601 : « yyyy-mm-ddThh : mm : SS \[ . sss \] \[ Z \] » où « T » est le séparateur d’heure et « Z » indique l’heure UTC. Par exemple, si la date et l' *\_ heure* sont « 2007-01-12T01:20:00 », l’heure d’expiration de l’abonnement est le 12 janvier 2007, 01:20.

</dd> <dt>

<span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/URI : *URI***
</dt> <dd>

Valeur qui spécifie le type d’événements consommés par l’abonnement. L’adresse de l’ordinateur source de l’événement avec l’URI (Uniform Resource Identifier) identifie de façon unique la source des événements. La chaîne d’URI est utilisée pour toutes les adresses de la source d’événements dans l’abonnement.

</dd> <dt>

<span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm : *\_ mode de configuration***
</dt> <dd>

Valeur qui spécifie le mode de configuration de l’abonnement aux événements. *Configuration \_ de Le MODE* peut être l’une des chaînes suivantes : « normal », « Custom », « MinLatency » ou « MinBandwidth ». L’énumération du mode de configuration de l' [**\_ abonnement \_ \_ EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) définit les modes de configuration. Les paramètres/DM,/DMI,/Hi et/DMLT ne peuvent être spécifiés que si le mode de configuration est défini sur personnalisé.

</dd> <dt>

<span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q : *requête***
</dt> <dd>

Valeur qui spécifie la chaîne de requête pour l’abonnement. Le format de cette chaîne peut être différent pour différentes valeurs d’URI et s’applique à toutes les sources d’événements de l’abonnement.

</dd> <dt>

<span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/Dia : *dialecte***
</dt> <dd>

Valeur qui spécifie le dialecte utilisé par la chaîne de requête.

</dd> <dt>

<span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/CF : *format***
</dt> <dd>

Valeur qui spécifie le format des événements retournés. Le *format* peut être « Events » ou « RenderedText ». Lorsque la valeur est « RenderedText », les événements sont retournés avec les chaînes localisées (telles que les chaînes de description d’événement) attachées aux événements. La valeur par défaut du *format* est « RenderedText ».

</dd> <dt>

<span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l : *paramètres régionaux***
</dt> <dd>

Valeur qui spécifie les paramètres régionaux pour la remise des chaînes localisées au format de texte rendu. Les *paramètres régionaux* sont un identificateur de culture de langue/pays, par exemple « en-US ». Ce paramètre est valide uniquement lorsque le paramètre/CF est défini sur « RenderedText ».

</dd> <dt>

<span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/REE : \[ *valeur*\]**
</dt> <dd>

Valeur qui spécifie les événements qui doivent être remis pour l’abonnement. La *valeur* peut être true ou false. Lorsque la *valeur* est true, tous les événements existants sont lus à partir des sources d’événements d’abonnement. Quand la *valeur* est false, seuls les événements futurs (arrivant) sont remis. La valeur par défaut est true quand/REE est spécifié sans valeur, et la valeur par défaut est false si/REE n’est pas spécifié.

</dd> <dt>

<span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/LF : *nom de fichier***
</dt> <dd>

Valeur qui spécifie le journal des événements local utilisé pour stocker les événements reçus de l’abonnement aux événements.

</dd> <dt>

<span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/PN : serveur de *publication***
</dt> <dd>

Valeur qui spécifie le nom de l’éditeur d’événements (fournisseur). Il doit s’agir d’un serveur de publication qui possède ou importe le journal spécifié par le paramètre/LF.

</dd> <dt>

<span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/DM : *mode***
</dt> <dd>

Valeur qui spécifie le mode de remise de l’abonnement. Le *mode* peut avoir la valeur push ou pull. Cette option n’est valide que si le paramètre/cm est défini sur Custom.

</dd> <dt>

<span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/DMI : *nombre***
</dt> <dd>

Valeur qui spécifie le nombre maximal d’éléments pour la remise par lot dans l’abonnement aux événements. Cette option n’est valide que si le paramètre/cm est défini sur Custom.

</dd> <dt>

<span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/DMLT : *MS***
</dt> <dd>

Valeur qui spécifie la latence maximale autorisée dans la transmission d’un lot d’événements. MS est le nombre de millisecondes autorisées. Ce paramètre n’est valide que si le paramètre/cm est défini sur Custom.

</dd> <dt>

<span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/HI : *MS***
</dt> <dd>

Valeur qui spécifie l’intervalle de vérification des pulsations pour l’abonnement. *MS* est le nombre de millisecondes utilisées dans l’intervalle. Ce paramètre n’est valide que si le paramètre/cm est défini sur Custom.

</dd> <dt>

<span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/TN : *TRANSPORTNAME***
</dt> <dd>

Valeur qui spécifie le nom du transport utilisé pour se connecter à l’ordinateur source de l’événement distant.

</dd> <dt>

<span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/ESA : *\_ source* de l’événement**
</dt> <dd>

Valeur qui spécifie l’adresse d’un ordinateur source d’événement. *Événement \_ La SOURCE* est une chaîne qui identifie un ordinateur source d’événements à l’aide du nom de domaine complet pour l’ordinateur, le nom NetBIOS ou l’adresse IP. Ce paramètre peut être utilisé avec les paramètres/ESE,/AES,/res, ou/un et/up.

</dd> <dt>

<span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ESE : *valeur***
</dt> <dd>

Valeur qui détermine s’il faut activer ou désactiver une source d’événement. La *valeur* peut être true ou false. La valeur par défaut est true, ce qui active la source de l’événement. Ce paramètre est utilisé uniquement si le paramètre/ESA est utilisé.

</dd> <dt>

<span id="_aes"></span><span id="_AES"></span>**/aes**
</dt> <dd>

Valeur qui ajoute la source d’événements spécifiée par le paramètre/ESA si la source d’événements ne fait pas déjà partie de l’abonnement aux événements. Si l’ordinateur spécifié par le paramètre/ESA fait déjà partie de l’abonnement, une erreur s’affiche. Ce paramètre est autorisé uniquement si le paramètre/ESA est utilisé.

</dd> <dt>

<span id="_res"></span><span id="_RES"></span>**/res**
</dt> <dd>

Valeur qui supprime la source d’événements spécifiée par le paramètre/ESA si la source de l’événement fait déjà partie de l’abonnement aux événements. Si l’ordinateur spécifié par le paramètre/ESA ne fait pas partie de l’abonnement, une erreur s’affiche. Ce paramètre est autorisé uniquement si le paramètre/ESA est utilisé.

</dd> <dt>

<span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/un : *nom d’utilisateur***
</dt> <dd>

Valeur qui spécifie le nom d’utilisateur utilisé dans les informations d’identification pour se connecter à la source d’événements spécifiée dans le paramètre/ESA. Ce paramètre est autorisé uniquement si le paramètre/ESA est utilisé.

</dd> <dt>

<span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/Up : *mot de passe***
</dt> <dd>

Valeur qui spécifie le mot de passe pour le nom d’utilisateur spécifié dans le paramètre/un. Les informations d’identification de nom d’utilisateur et de mot de passe sont utilisées pour la connexion à la source d’événements spécifiée dans le paramètre/ESA. Ce paramètre est autorisé uniquement si le paramètre/un est utilisé.

</dd> <dt>

<span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/TP : *TRANSPORTPORT***
</dt> <dd>

Valeur qui spécifie le numéro de port utilisé par le transport lors de la connexion à un ordinateur source d’événement distant.

</dd> <dt>

<span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/HN : *nom***
</dt> <dd>

Valeur qui spécifie le nom DNS de l’ordinateur local. Ce nom est utilisé par les sources d’événements distantes pour effectuer un push des événements et doit être utilisé uniquement pour les abonnements par envoi de notification.

</dd> <dt>

<span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/CT : *type***
</dt> <dd>

Valeur qui spécifie le type d’informations d’identification utilisé pour accéder aux sources d’événements distantes. Le *type* peut être « default », « Negotiate », « Digest », « Basic » ou « LocalMachine ». La valeur par défaut est « default ». Ces valeurs sont définies dans l’énumération de [**\_ \_ \_ type des informations d’identification de l’abonnement EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) .

</dd> <dt>

<span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/CUN : *nom d’utilisateur***
</dt> <dd>

Valeur qui définit les informations d’identification de l’utilisateur partagé utilisées pour les sources d’événements qui n’ont pas leurs propres informations d’identification de l’utilisateur.

> [!Note]  
> Si ce paramètre est utilisé avec l’option/c, les paramètres de nom d’utilisateur et de mot de passe pour les sources d’événements individuels à partir du fichier de configuration sont ignorés. Si vous souhaitez utiliser des informations d’identification différentes pour une source d’événement spécifique, vous pouvez remplacer cette valeur en spécifiant les paramètres/un et/up pour une source d’événement spécifique sur la ligne de commande d’une autre commande Set-Subscription.

 

</dd> <dt>

<span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/Cup : *mot de passe***
</dt> <dd>

Valeur qui définit le mot de passe de l’utilisateur pour les informations d’identification de l’utilisateur partagé. Lorsque le *mot de passe* est défini sur \* (astérisque), le mot de passe est lu à partir de la console. Cette option n’est valide que si le paramètre/cun est spécifié.

</dd> <dt>

<span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ICA : *empreintes numériques***
</dt> <dd>

Valeur qui définit la liste des empreintes du certificat de l’émetteur, dans une liste séparée par des virgules.

> [!Note]  
> Cette option est spécifique uniquement aux abonnements initiés par la source.

 

</dd> <dt>

<span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/As : *autorisé***
</dt> <dd>

Valeur qui définit une liste de chaînes séparées par des virgules qui spécifient les noms DNS des ordinateurs qui n’appartiennent pas à un domaine et qui sont autorisés à initier des abonnements. Les noms peuvent être spécifiés à l’aide de caractères génériques, tels que « \* . mydomain.com ». Par défaut, cette liste est vide.

> [!Note]  
> Cette option est spécifique uniquement aux abonnements initiés par la source.

 

</dd> <dt>

<span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/DS : *refusé***
</dt> <dd>

Valeur qui définit une liste de chaînes séparées par des virgules qui spécifient les noms DNS des ordinateurs n’appartenant pas à un domaine qui ne sont pas autorisés à initier des abonnements. Les noms peuvent être spécifiés à l’aide de caractères génériques, tels que « \* . mydomain.com ». Par défaut, cette liste est vide.

> [!Note]  
> Cette option est spécifique uniquement aux abonnements initiés par la source.

 

</dd> <dt>

<span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/ADC : *SDDL***
</dt> <dd>

Valeur qui définit une chaîne, au format SDDL, qui spécifie les ordinateurs de domaine qui sont autorisés ou non à initier des abonnements. La valeur par défaut consiste à autoriser tous les ordinateurs du domaine à initier des abonnements.

> [!Note]  
> Cette option est spécifique uniquement aux abonnements initiés par la source.

 

</dd> </dl>

## <a name="create-a-new-subscription"></a>Créer un abonnement

La syntaxe suivante est utilisée pour créer un abonnement aux événements sur un ordinateur distant.

``` syntax
wecutil {cs | create-subscription } CONFIGURATION_FILE [/cun:USERNAME]
[/cup:PASSWORD] 
```

### <a name="remarks"></a>Notes

Lorsqu’un nom d’utilisateur ou un mot de passe incorrect est spécifié dans la commande **wecutil CS** , aucune erreur n’est signalée tant que vous n’avez pas affiché l’état d’exécution de l’abonnement à l’aide de la commande **wecutil gr** .

## <a name="creation-parameters"></a>Paramètres de création

<dl> <dt>

<span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**fichier de CONFIGURATION \_**
</dt> <dd>

Valeur qui spécifie le chemin d’accès au fichier XML qui contient les informations de configuration de l’abonnement. Le chemin d’accès peut être absolu ou relatif au répertoire actif.

Le code XML suivant est un exemple de fichier de configuration d’abonnement qui crée un abonnement initié par le collecteur pour transférer des événements du journal des événements d’application d’un ordinateur distant vers le journal ForwardedEvents.


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



Le code XML suivant est un exemple de fichier de configuration d’abonnement qui crée un abonnement initié par la source pour transférer les événements du journal des événements d’application d’un ordinateur distant vers le journal ForwardedEvents.


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
> Lors de la création d’un abonnement initié par la source, si **AllowedSourceDomainComputers**, **AllowedSourceNonDomainComputers** / **IssuerCAList**, **AllowedSubjectList** et **DeniedSubjectList** sont tous vides, une valeur par défaut est fournie pour **AllowedSourceDomainComputers** -"O :NSG : NSD : (a ;; GA ;;;D C) (A ;; GA ;;; NS)». Cette valeur SDDL accorde par défaut les membres du groupe de domaine ordinateurs du domaine, ainsi que le groupe de service réseau local (pour le redirecteur local), la possibilité de déclencher des événements pour cet abonnement.

 

</dd> <dt>

<span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/CUN : *nom d’utilisateur***
</dt> <dd>

Valeur qui définit les informations d’identification de l’utilisateur partagé utilisées pour les sources d’événements qui n’ont pas leurs propres informations d’identification de l’utilisateur. Cette valeur s’applique uniquement aux abonnements initiés par le collecteur.

> [!Note]  
> Si ce paramètre est spécifié, les paramètres de nom d’utilisateur et de mot de passe pour les sources d’événements individuels à partir du fichier de configuration sont ignorés. Si vous souhaitez utiliser des informations d’identification différentes pour une source d’événement spécifique, vous pouvez remplacer cette valeur en spécifiant les paramètres/un et/up pour une source d’événement spécifique sur la ligne de commande d’une autre commande Set-Subscription.

 

</dd> <dt>

<span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/Cup : *mot de passe***
</dt> <dd>

Valeur qui définit le mot de passe de l’utilisateur pour les informations d’identification de l’utilisateur partagé. Lorsque le *mot de passe* est défini sur « \* » (astérisque), le mot de passe est lu à partir de la console. Cette option n’est valide que si le paramètre/cun est spécifié.

</dd> </dl>

## <a name="delete-a-subscription"></a>Supprimer un abonnement

La syntaxe suivante est utilisée pour supprimer un abonnement aux événements.

``` syntax
wecutil { ds | delete-subscription } SUBSCRIPTION_ID
```

## <a name="deletion-parameters"></a>Paramètres de suppression

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID d’abonnement \_**
</dt> <dd>

Chaîne qui identifie de façon unique un abonnement. Cet identificateur est spécifié dans l’élément **SubscriptionId** dans le fichier de configuration XML utilisé pour créer l’abonnement. L’abonnement identifié dans ce paramètre sera supprimé.

</dd> </dl>

## <a name="retry-a-subscription"></a>Réessayer un abonnement

La syntaxe suivante est utilisée pour réessayer un abonnement inactif en tentant de réactiver toutes les sources d’événements ou spécifiées en établissant une connexion à chaque source d’événement et en envoyant une demande d’abonnement à distance à la source de l’événement. Les sources d’événements désactivées ne sont pas retentées.

``` syntax
wecutil { rs | retry-subscription } SUBSCRIPTION_ID 
[EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="retry-parameters"></a>Paramètres de nouvelle tentative

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID d’abonnement \_**
</dt> <dd>

Chaîne qui identifie de façon unique un abonnement. Cet identificateur est spécifié dans l’élément **SubscriptionId** dans le fichier de configuration XML utilisé pour créer l’abonnement. L’abonnement identifié dans ce paramètre sera retenté.

</dd> <dt>

<span id="EVENT_SOURCE"></span><span id="event_source"></span>**SOURCE de l’événement \_**
</dt> <dd>

Valeur qui identifie un ordinateur qui est une source d’événements pour un abonnement aux événements. Cette valeur peut être le nom de domaine complet pour l’ordinateur, le nom NetBIOS ou l’adresse IP.

</dd> </dl>

## <a name="configure-the-windows-event-collector-service"></a>Configurer le service collecteur d’événements Windows

La syntaxe suivante est utilisée pour configurer le service collecteur d’événements Windows afin de s’assurer que les abonnements d’événements peuvent être créés et maintenus au redémarrage de l’ordinateur. Cela comprend la procédure suivante :

**Pour configurer le service collecteur d’événements Windows**

1.  Activez le canal ForwardedEvents s’il est désactivé.
2.  Retardez le démarrage du service collecteur d’événements Windows.
3.  Démarrez le service collecteur d’événements Windows s’il n’est pas en cours d’exécution.

``` syntax
wecutil { qc | quick-config } /q:VALUE
```

## <a name="configure-event-collector-parameters"></a>Configurer les paramètres du collecteur d’événements

<dl> <dt>

<span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q : *valeur***
</dt> <dd>

Valeur qui détermine si la commande de configuration rapide demande une confirmation. La valeur peut être true ou false. Si la valeur est true, la commande vous invite à confirmer l’opération. La valeur par défaut est false.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



 

 





