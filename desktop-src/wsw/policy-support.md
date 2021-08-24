---
title: Prise en charge des stratégies
description: Wsutil traite la stratégie spécifiée dans les métadonnées d’entrée et génère des routines d’assistance pour la prise en charge du modèle de service.
ms.assetid: 9c4fb485-2392-4117-b4a7-7a51786d60b9
keywords:
- Services Web de prise en charge des stratégies pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 347265d4081216a227b5040fc73f272181bdccfe09ca7500b81078a6a57ed7bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838639"
---
# <a name="policy-support"></a>Prise en charge des stratégies

Wsutil traite la stratégie spécifiée dans les métadonnées d’entrée et génère des routines d’assistance pour la prise en charge du modèle de service.

## <a name="how-to-use-policy-support-in-wsutil"></a>Utilisation de la prise en charge des stratégies dans Wsutil

Les développeurs doivent suivre les étapes suivantes pour utiliser la prise en charge des stratégies dans le compilateur Wsutil :

-   Collectez tous les fichiers de métadonnées d’entrée nécessaires pour le service Web ciblé.
-   Compilez tous les fichiers WSDL/XSD/de stratégie collectés à l’aide de wsutil.exe. Wsutil génère un ensemble de fichiers stub et d’en-tête pour chaque fichier WSDL et XSD d’entrée.
-   Inspecter le fichier d’en-tête généré, tous les noms de routines d’assistance de la stratégie sont répertoriés dans la section des commentaires au début du fichier d’en-tête.
-   Utilisez la \_ routine d’assistance BindingName CreateServiceProxy pour créer un proxy de service.
-   Utilisez la \_ routine d’assistance BindingName CreateServiceEndpoint du pour créer un point de terminaison de service.
-   Renseignez \_ \_ la structure de modèle de liaison WS bindingTemplateType \_ spécifiée dans la signature de la méthode. Les développeurs peuvent fournir des propriétés de canal supplémentaires et/ou des propriétés de sécurité en fonction des besoins.
-   Appelez les routines d’assistance, en cas de création d’un proxy de service ou d’un point de terminaison de service réussi.

Les sections suivantes décrivent en détail les rubriques connexes.

## <a name="handle-policy-input"></a>Gérer l’entrée de stratégie

Voici les [Options du compilateur](web-service-compiler-tool.md) liées au traitement de la stratégie.

Par défaut, Wsutil génère toujours des modèles de stratégie, sauf s’ils sont appelés avec l’option « /nopolicy ». La stratégie peut être incorporée dans le cadre d’un fichier WSDL ou être créée séparément en tant que fichier de métadonnées de stratégie que Wsutil prend comme entrée. L’option de compilateur « /wsp : » est utilisée pour indiquer que les métadonnées d’entrée spécifiées sont un fichier de stratégie. Wsutil génère des applications d’assistance associées à la stratégie potentielles avec la compilation suivante :

**Wsutil/wsdl : Trusted. wsdl/wsdl : TRUSTED1. wsdl**

**wstuil/wsdl : Input. wsdl/wsp : Policy. wsp**

Aucune assistance de stratégie n’est générée lorsque l’option « /nopolicy » est utilisée comme dans l’exemple suivant.

**Wsutil/nopolicy/wsdl : Trusted. wsdl/wsdl : TRUSTED1. wsdl**

## <a name="policy-related-code-generated-by-the-wsutil-compiler"></a>Code lié à la stratégie généré par le compilateur Wsutil

La page de [mappage des métadonnées](metadata-mapping.md) détaille le mappage entre les constructions de métadonnées avec différents types de liaison.

Trois catégories de paramètres de stratégie peuvent être spécifiées dans les paramètres de stratégie :

-   Propriétés du canal. Actuellement, seules les propriétés de canal suivantes sont prises en charge : l' [**\_ \_ \_ encodage de propriété WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id), la **\_ \_ \_ \_ version d’adressage de propriété WS** Channel et la **\_ \_ \_ \_ version d’enveloppe de propriété WS Channel**.
-   Propriétés de sécurité. Actuellement, seules les propriétés de sécurité suivantes sont prises en charge : utilisation de l' [**\_ horodatage de \_ propriété \_ \_ WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id), **\_ \_ \_ \_ \_ disposition des en-têtes de sécurité** de la propriété WS Security, **\_ \_ niveau de \_ \_ protection \_ du transport** et version de l' **\_ \_ \_ \_ en-tête \_** de sécurité de propriété WS Security.
-   Liaison de sécurité. Actuellement, seules les liaisons de sécurité suivantes sont prises en charge : liaison de sécurité d' [**\_ \_ authentification d’en-tête \_ \_ \_ WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding), liaison de [**\_ \_ sécurité de transport WS \_ \_ SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding), liaison de [**\_ \_ sécurité de \_ transport \_ \_ SSPI TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding), liaison de [**sécurité de \_ \_ message WS \_ \_ username**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding), liaison de sécurité de message WS [**\_ Kerberos \_ \_ \_ \_ APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)et liaison de [**\_ sécurité de message de \_ contexte \_ \_ \_ WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding).

Type de modèle de liaison

Il existe un nombre limité de liaisons prises en charge dans Wsutil. Toutes les combinaisons prises en charge de ces liaisons sont répertoriées dans la définition de [**\_ type de \_ modèle \_ de liaison WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) . Par exemple, pour la liaison suivante dans WSDL

``` syntax
<soap:binding style="document" transport="http://schemas.xmlsoap.org/soap/http" />
```

Wsutil génère le type de modèle de liaison de modèle de liaison [**WS \_ http \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) pour cette liaison.

Descriptions des stratégies

Avec le paramètre de stratégie d’entrée, Wsutil génère un ensemble de descriptions de stratégie décrivant la stratégie d’entrée, y compris le type de modèle, ainsi que les valeurs spécifiées dans la stratégie. Par exemple, pour l’entrée

``` syntax
<wsdl:binding...>
  <soap11:binding.../> =< WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

Wsutil génère la description de la propriété de canal comme suit :

``` syntax
WS_ENVELOPE_VERSION_SOAP_1_1,
{
  WS_CHANNEL_PROPERTY_ENVELOPE_VERSION,
  (void*)&locaDefinitions.policies.bindHostedClientSoap.envelopeVersion, //points to the WS_ENVELOPE_VERSION_SOAP_1_1 value above
  sizeof(&localDefinitions.policies.bindHostedClientSoap.envelopeVersion),
},
```

Tous les paramètres de stratégie (propriétés de canal, propriétés de sécurité et propriétés de liaison de sécurité) dans une liaison sont regroupés dans une seule structure de description de la \_ stratégie WS bindingTemplateType \_ \_ . [**WS \_ \_ \_ Type de modèle de liaison**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) spécifie les différentes combinaisons de stratégie de liaison prises en charge par Wsutil.

Structure de modèle à remplir par l’application

La description de la stratégie contient toutes les informations de stratégie spécifiées dans les métadonnées d’entrée pour une liaison donnée, mais il existe des informations qui ne peuvent pas être représentées dans la stratégie, mais nécessitent une entrée utilisateur lors de l’utilisation de ces stratégies pour créer un proxy de service et/ou un point de terminaison de service. Par exemple, l’application doit fournir des informations d’identification pour l’authentification d’en-tête HTTP.

L’application doit remplir la structure de modèle, appelée \_ modèle de liaison WS bindingTemplateType \_ \_ pour chaque type de modèle de liaison différent, défini dans WebServices. h :

``` syntax
struct WS_bindingTemplateType_BINDING_TEMPLATE
{
  WS_CHANNEL_PROPERTIES channelProperties;
  WS_SECURITY_PROPERTIES securityProperties;
  possible_list_of_SECURITY_BINDING_TEMPLATEs;
  ...
};
```

La liste des modèles de liaison de sécurité est facultative dépend de la liaison de sécurité correspondante. Par exemple, le champ [**modèle de liaison de \_ sécurité de \_ transport \_ \_ \_ WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_template) est présenté dans le [**modèle de \_ liaison WS http \_ SSL \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template) pour que l’application fournisse des informations de liaison de sécurité liées à SSL, y compris les informations d’identification.

L’application doit remplir tous les champs de cette structure avant d’appeler des API de modèle WebServices. Des propriétés de sécurité supplémentaires, ainsi que des propriétés de liaison de sécurité qui ne peuvent pas être représentées dans la stratégie doivent être remplies, et les API WebServices fusionnent les deux jeux de propriétés dans le Runtime. Les champs peuvent être mis à zéro s’ils ne sont pas applicables. Par exemple, securityProperties peut être mis à zéro si aucune propriété de sécurité supplémentaire n’est nécessaire.

Routines d’assistance et déclaration de description de stratégie dans les fichiers d’en-tête

Wsutil crée une routine d’assistance pour faciliter la prise en charge de la couche de modèle de service, de sorte que l’application peut créer plus facilement le proxy de service et le point de terminaison de service. La description de la stratégie est également exposée de telle sorte que l’application puisse les utiliser directement. Une routine d’aide CreateSerivceProxy ressemble à ceci :

``` syntax
HRESULT bindingName_CreateServiceProxy(
  __in_ecount_opt(propertyCount) const WS_PROXY_PROPERTY* properties,
  __in const ULONG propertyCount,
  __in WS_constraintName_BINDING_TEMPLATE* templateValue,
  __deref_out WS_SERVICE_PROXY** serviceProxy,
  __in_opt WS_ERROR* error);
```

Les développeurs sont encouragés à utiliser ces routines d’assistance, bien qu’elles puissent également utiliser directement la routine d’exécution sous-jacente fournie par webservices.dll. Les développeurs ne sont pas encouragés à utiliser directement les descriptions de stratégie lors de la programmation à l’aide de la couche de [modèle de service](service-model-layer-overview.md) .

Les références de description de stratégie sont également générées dans l’en-tête de l’utilisateur avancé. Si les développeurs n’utilisent pas de fonctionnalités de modèle de service, ils peuvent utiliser directement les descriptions de stratégie.

``` syntax
struct {
  ...
  struct {
    ...
    } contracts;
  struct {
    WS_bindingTemplateType_POLICY_DESCRIPTION bindingName;
    ...
    } policies;
  }
```

Prototypes de définition dans des fichiers stub

Un champ de structure de description de stratégie unique par liaison et ses descriptions d’assistance référencées en interne sont créés dans la structure de prototype locale. Les descriptions de stratégie sont générées dans le fichier où la [**\_ \_ Description de contrat WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) est générée. En général, les développeurs n’ont pas besoin d’inspecter le fichier stub pendant le développement, bien que le fichier stub contienne tous les détails sur les spécifications de stratégie.

``` syntax
struct {
  ...
  struct {
  ... } contracts;
  ...
 struct {
      struct {
        hierarchy of policy template descriptions;
        } bindingName;
      ...
      list of bindings in the input wsdl file.
  } policies;
} fileNameLocalDefinitions;
```

Implémentation des routines d’assistance dans les fichiers stub

Wsutil génère des routines d’assistance pour simplifier les appels d’application à [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) et la création de base de [**point de \_ \_ terminaison de service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) sur les informations fournies dans les paramètres de stratégie.

Dépend des contraintes de liaison spécifiées pour le port donné, le premier argument est différent en fonction de la structure du modèle. L’exemple suivant suppose que le transport HTTP, la signature pour la création du proxy de service est similaire à un paramètre de type de canal supplémentaire.

``` syntax
HRESULT bindingName_CreateServiceProxy(
    __in WS_bindingTemplateType_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(propertyCount) const WS_PROXY_PROPERTY* properties,
    __in const ULONG propertyCount,
    __deref_out WS_SERVICE_PROXY** serviceProxy,
    __in_opt WS_ERROR* error)
{
    return WsCreateServiceProxyFromTemplate(
      WS_CHANNEL_TYPE_REQUEST,    // this is fixed for http, requires input for TCP
      properties,     
      propertyCount, 
      WS_bindingTemplateType_BINDING_TEMPLATE_TYPE,
      templateValue,
      sizeof(WS_bindingTemplateType_BINDING_TEMPLATE),  
      &fileName.policies.bindingName,   // template description as generated in the stub file
      sizeof(WS_constraintName_POLICY_DESCRIPTION),
      serviceProxy,     
      error);     
}
```

``` syntax
HRESULT bindingName_CreateServiceEndpoint(
__in WS_bindingTemplateType_BINDING_TEMPLATE* templateValue,
__in_opt const WS_STRING* addressUrl,
__in bindingNameFunctionTable* functionTable,
__in WS_SERVICE_SECURITY_CALLBACK authorizationCallback,
__in const WS_SERVICE_ENDPOINT_PROPERTY* properties,
__in ULONG propertyCount,
__in WS_HEAP* heap,
  __deref_out WS_SERVICE_ENDPOINT** serviceEndpoint,
  __in_opt WS_ERROR* error)
{
  WS_SERVICE_CONTRACT serviceContract;
  serviceContract.contractDescription = &fileName.contracts.bindingName;
  serviceContract.defaultMessageHandlerCallback = NULL;
  serviceContract.methodTable = (const void *)functionTable;

  return WsCreateServiceEndpointFromTemplate(
      properties,
      propertyCount,
      addressUrl,    // service endpoint address
      WS_CHANNEL_TYPE_RESPONSE,    // this is fixed for http, requires input for TCP
      &serviceContract,
      authorizationCallback,
      heap,
      WS_bindingTemplateType_BINDING_TEMPLATE_TYPE,
      templateValue,
      sizeof(WS_bindingTemplateType_BINDING_TEMPLATE),
      &fileName.policies.bindingName,   // template description as generated in the stub file
      sizeof(WS_bindingTemplateType_POLICY_DESCRIPTION),
      serviceEndpoint,
      error);
}
```

## <a name="supported-policy-settings"></a>Paramètres de stratégie pris en charge

Tableau suivant répertorie tous les types de modèles de liaison pris en charge, les liaisons de sécurité correspondantes requises dans le type, la structure de modèle à remplir par l’application pour le type et le type de description correspondante. L’application doit remplir la structure du modèle, tandis que le développeur d’applications doit comprendre quelles sont les liaisons de sécurité requises dans la stratégie donnée.



| [**\_type de \_ modèle de liaison WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                                | Combinaisons de liaisons de sécurité                                                                                                                                                                                                                                                                                                               | structure de modèle à remplir par l’application                                                                                            | Description de la stratégie                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_type de \_ modèle de liaison http \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                          |                                                                                                                                                                                                                                                                                                                                             | [**\_modèle de \_ liaison WS http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_binding_template)                                                                              | [**Description de la \_ stratégie WS http \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_policy_description)                                                                              |
| [**\_type de \_ \_ modèle de liaison SSL WS http \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                     | [**\_liaison de \_ sécurité de transport WS SSL \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)                                                                                                                                                                                                                                                          | [**\_modèle de \_ \_ liaison SSL WS http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template)                                                                     | [**\_Description de \_ la \_ stratégie \_ SSL WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description)                                                                     |
| [**\_type de \_ \_ modèle de liaison d’authentification d’en-tête http \_ \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                            | [**\_liaison de \_ sécurité d’authentification d’en-tête WS http \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)                                                                                                                                                                                                                                                   | [**\_modèle de \_ liaison d’authentification d’en-tête http WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_binding_template)                                                    | [**Description de la \_ \_ stratégie d’authentification d’en-tête http \_ \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_policy_description)                                                    |
| [**\_type de \_ \_ modèle de \_ liaison d’authentification d’en-tête SSL \_ \_ WS \_ http**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                       | [**WS \_ Liaison \_ de \_ sécurité \_ de transport SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) et [ **\_ \_ \_ \_ \_ liaison de sécurité d’en-tête WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)                                                                                                                                                            | [**\_modèle de \_ \_ liaison d’authentification d’en-tête SSL \_ \_ WS http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_binding_template)                                           | [**Description de la \_ \_ stratégie d' \_ authentification d’en-tête SSL \_ \_ WS http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_policy_description)                                           |
| [**\_type de \_ \_ modèle de liaison de nom d’utilisateur SSL \_ \_ WS http \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                           | [**WS \_ Liaison \_ de \_ sécurité \_ de transport SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) et [ **liaison de sécurité de \_ \_ message \_ \_ WS username**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)                                                                                                                                                             | [**\_modèle de \_ \_ liaison de nom d’utilisateur SSL WS \_ http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_binding_template)                                                  | [**Description de la \_ \_ \_ stratégie de nom d’utilisateur SSL \_ WS http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_policy_description)                                                  |
| [**\_type de \_ \_ modèle de \_ \_ liaison APREQ \_ Kerberos \_ WS http SSL**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                    | [**WS \_ Liaison \_ de \_ sécurité \_ de transport SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) et [ **liaison de sécurité de \_ message WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)                                                                                                                                                | [**\_modèle de \_ \_ \_ \_ liaison APREQ \_ du protocole Kerberos SSL WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_binding_template)                                     | [**\_Description de \_ la \_ \_ stratégie APREQ \_ \_ WS http SSL Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_policy_description)                                     |
| [**\_type de \_ modèle de liaison WS TCP \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                           |                                                                                                                                                                                                                                                                                                                                             | [**\_modèle de \_ liaison WS TCP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_binding_template)                                                                                | [**Description de la \_ stratégie WS TCP \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_policy_description)                                                                                |
| [**TYPE de modèle de liaison de WS \_ TCP \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                     | [**liaison de sécurité de transport de WS \_ TCP \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)                                                                                                                                                                                                                                               | [**modèle de liaison de WS \_ TCP \_ SSPI \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_binding_template)                                                                     | [**Description de la \_ \_ stratégie SSPI TCP SSPI \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_policy_description)                                                                     |
| [**\_type de \_ \_ modèle de liaison de nom d’utilisateur SSPI \_ \_ TCP \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                           | [**WS \_ Liaison \_ de \_ \_ sécurité de \_ transport TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) et [ **\_ \_ \_ \_ liaison de sécurité de message WS username**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)                                                                                                                                                  | [**\_modèle de \_ \_ liaison de nom d’utilisateur SSPI TCP \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_binding_template)                                                  | [**Description de la \_ \_ \_ stratégie de nom d’utilisateur SSPI \_ TCP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_policy_description)                                                  |
| [**\_type de \_ \_ modèle de \_ \_ liaison APREQ \_ WS TCP SSPI Kerberos \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                    | [**WS \_ \_Liaison de \_ \_ sécurité \_ de transport TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) et [ **\_ \_ \_ \_ \_ liaison de sécurité de message WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)                                                                                                                                     | [**\_modèle de \_ \_ \_ \_ liaison APREQ \_ WS TCP SSPI Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_binding_template)                                     | [**\_Description de \_ la \_ \_ stratégie APREQ \_ \_ WS TCP SSPI Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_policy_description)                                     |
| [**\_type de \_ \_ modèle de \_ \_ liaison de contexte de sécurité du \_ \_ nom d’utilisateur \_ WS http SSL**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)        | [**WS \_ Liaison de sécurité de \_ transport \_ \_ SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) et [**liaison de sécurité de \_ message de \_ contexte \_ \_ \_ WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) avec [**WS \_ nom_utilisateur \_ message \_ Security \_ Binding**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) dans le canal bootstrap                         | [**\_modèle de \_ \_ liaison de \_ contexte de sécurité du nom d’utilisateur SSL \_ \_ WS \_ http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_binding_template)              | [**Description de la \_ stratégie de contexte de \_ sécurité du \_ nom d’utilisateur SSL WS \_ \_ http \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_policy_description)              |
| [**TYPE de modèle de liaison de contexte de sécurité de WS \_ http \_ SSL \_ \_ APREQ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) | [**WS \_ Liaison de sécurité de \_ transport \_ \_ SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) et [**liaison de sécurité de \_ message de \_ contexte WS \_ \_ \_ Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) avec la liaison de [**\_ sécurité de message WS Kerberos \_ \_ \_ \_ APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) dans le canal bootstrap            | [**modèle de liaison de contexte de sécurité de WS \_ http \_ SSL \_ \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_binding_template) | [**Description de la \_ \_ stratégie de \_ \_ \_ contexte de sécurité APREQ \_ \_ WS http SSL \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_policy_description) |
| [**\_type de \_ \_ modèle de \_ \_ liaison de contexte de sécurité du \_ \_ nom d’utilisateur \_ de WS TCP SSPI**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)        | [**WS \_ Liaison de sécurité de \_ transport TCP SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) et liaison de [**sécurité de \_ message de \_ contexte \_ \_ \_ WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) avec [**WS \_ nom_utilisateur \_ message \_ Security \_ Binding**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) dans le canal bootstrap              | [**\_modèle de \_ \_ liaison de \_ contexte de sécurité du nom d’utilisateur \_ \_ de WS TCP SSPI \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_binding_template)              | [**Description de la \_ stratégie de contexte de \_ sécurité du \_ nom d’utilisateur SSPI TCP \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_policy_description)              |
| [**TYPE de modèle de liaison de contexte de sécurité de WS \_ TCP \_ SSPI \_ Kerberos \_ APREQ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) | [**WS \_ Liaison de sécurité de \_ transport TCP SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) et liaison de [**sécurité de \_ message de \_ contexte \_ \_ \_ WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) avec [**WS \_ Kerberos \_ APREQ \_ \_ \_ liaison**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) de sécurité de message dans le canal bootstrap | [**modèle de liaison de contexte de sécurité de WS \_ TCP \_ SSPI \_ Kerberos \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_binding_template) | [**Description de la stratégie de contexte de sécurité de WS \_ TCP \_ SSPI \_ Kerberos \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_policy_description) |



 

Par exemple, [**le \_ \_ type de \_ \_ modèle de \_ liaison SSL WS http**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) indique que la stratégie d’entrée pour la liaison spécifie le transport http et la [**\_ \_ \_ \_ liaison de sécurité de transport WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). L’application doit remplir la structure du [**\_ modèle de liaison WS http \_ SSL \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template) avant d’appeler les routines d’assistance, et la description de la stratégie de correspondance est la description de la [**\_ stratégie WS http \_ SSL \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description). Plus précisément, la section de liaison dans WSDL contient les segments suivants :

``` syntax
<wsp:Policy...>
  <sp:TransportBinding...>
    <wsp:Policy...>
      <sp:TransportToken...>
        <wsp:Policy...>
          <sp:HttpsToken.../>
        </wsp:Policy...>
      </sp:TransportToken...>
    </wsp:Policy>
  </sp:TransportBinding...>
</wsp:Policy>
```

``` syntax
<wsdl:binding...>
<soap11:binding.../> => WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

## <a name="security-context-support"></a>Prise en charge du contexte de sécurité

Dans le [contexte de sécurité](security-context.md), le canal bootstrap est créé pour établir la conversation sécurisée dans le canal de service. Wsutil prend uniquement en charge le scénario dans lequel le canal bootstrap est le même que le canal de service, avec les mêmes propriétés de canal et propriétés de sécurité. La sécurité de transport est requise pour la liaison de message de contexte de sécurité. Wsutil prend en charge les canaux d’amorçage avec d’autres liaisons de sécurité de message, mais ne prend en charge que le contexte de sécurité comme seule liaison de sécurité de message dans le canal de service, sans combinaison avec d’autres liaisons de sécurité de message. Les développeurs peuvent prendre en charge ces combinaisons en dehors de la prise en charge des modèles de stratégie.

L’énumération suivante fait partie de la prise en charge des stratégies :

-   [**\_type de \_ modèle de liaison WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)

Les fonctions suivantes font partie de la prise en charge des stratégies :

-   [**WsCreateServiceEndpointFromTemplate**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceendpointfromtemplate)
-   [**WsCreateServiceProxyFromTemplate**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxyfromtemplate)

Les structures suivantes font partie de la prise en charge des stratégies :

-   [**\_modèle de \_ liaison WS http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_binding_template)
-   [**\_modèle de \_ liaison d’authentification d’en-tête http WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_binding_template)
-   [**Description de la \_ \_ stratégie d’authentification d’en-tête http \_ \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_policy_description)
-   [**Description de la \_ \_ stratégie de \_ liaison de \_ sécurité \_ \_ d' \_ en-tête http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_policy_description)
-   [**\_modèle de \_ \_ liaison de sécurité d’authentification d’en-tête WS \_ http \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_template)
-   [**Description de la \_ stratégie WS http \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_policy_description)
-   [**\_modèle de \_ \_ liaison SSL WS http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template)
-   [**\_modèle de \_ \_ liaison d’authentification d’en-tête SSL \_ \_ WS http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_binding_template)
-   [**Description de la \_ \_ stratégie d' \_ authentification d’en-tête SSL \_ \_ WS http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_policy_description)
-   [**\_modèle de \_ \_ \_ \_ liaison APREQ \_ du protocole Kerberos SSL WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_binding_template)
-   [**\_Description de \_ la \_ \_ stratégie APREQ \_ \_ WS http SSL Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_policy_description)
-   [**modèle de liaison de contexte de sécurité de WS \_ http \_ SSL \_ \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_binding_template)
-   [**Description de la \_ \_ stratégie de \_ \_ \_ contexte de sécurité APREQ \_ \_ WS http SSL \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_policy_description)
-   [**\_Description de \_ la \_ stratégie \_ SSL WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description)
-   [**\_modèle de \_ \_ liaison de nom d’utilisateur SSL WS \_ http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_binding_template)
-   [**Description de la \_ \_ \_ stratégie de nom d’utilisateur SSL \_ WS http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_policy_description)
-   [**\_modèle de \_ \_ liaison de \_ contexte de sécurité du nom d’utilisateur SSL \_ \_ WS \_ http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_binding_template)
-   [**Description de la \_ stratégie de contexte de \_ sécurité du \_ nom d’utilisateur SSL WS \_ \_ http \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_policy_description)
-   [**Description de la \_ stratégie de liaison de sécurité des messages WS Kerberos \_ APREQ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_policy_description)
-   [**\_modèle de \_ \_ liaison de \_ sécurité de message \_ \_ WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_template)
-   [**Description de la \_ stratégie de liaison de sécurité des messages du contexte de sécurité WS \_ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_policy_description)
-   [**\_modèle de \_ \_ liaison de sécurité de message de contexte \_ de \_ sécurité WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_template)
-   [**Description de la stratégie de \_ sécurité du contexte WS Security \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_security_binding_policy_description)
-   [**\_modèle de \_ liaison de sécurité du contexte de sécurité WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_security_binding_template)
-   [**Description de la \_ stratégie de liaison de sécurité de transport WS SSL \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_policy_description)
-   [**\_modèle de \_ liaison de sécurité de transport WS SSL \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_template)
-   [**Description de la \_ stratégie de liaison de sécurité de transport WS SSPI \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_sspi_transport_security_binding_policy_description)
-   [**\_modèle de \_ liaison WS TCP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_binding_template)
-   [**Description de la \_ stratégie WS TCP \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_policy_description)
-   [**modèle de liaison de WS \_ TCP \_ SSPI \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_binding_template)
-   [**\_modèle de \_ \_ \_ \_ liaison APREQ \_ WS TCP SSPI Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_binding_template)
-   [**\_Description de \_ la \_ \_ stratégie APREQ \_ \_ WS TCP SSPI Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_policy_description)
-   [**modèle de liaison de contexte de sécurité de WS \_ TCP \_ SSPI \_ Kerberos \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_binding_template)
-   [**Description de la stratégie de contexte de sécurité de WS \_ TCP \_ SSPI \_ Kerberos \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_policy_description)
-   [**Description de la \_ \_ stratégie SSPI TCP SSPI \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_policy_description)
-   [**modèle de liaison de sécurité de transport de WS \_ TCP \_ SSPI \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_template)
-   [**\_modèle de \_ \_ liaison de nom d’utilisateur SSPI TCP \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_binding_template)
-   [**Description de la \_ \_ \_ stratégie de nom d’utilisateur SSPI \_ TCP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_policy_description)
-   [**\_modèle de \_ \_ liaison de \_ contexte de sécurité du nom d’utilisateur \_ \_ de WS TCP SSPI \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_binding_template)
-   [**Description de la \_ stratégie de contexte de \_ sécurité du \_ nom d’utilisateur SSPI TCP \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_policy_description)
-   [**Description de la \_ stratégie de liaison de sécurité de message WS username \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_policy_description)
-   [**\_modèle de \_ liaison de sécurité de message WS username \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_template)

 

 




