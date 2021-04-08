---
title: WSDL et contrats de service
description: L’utilitaire Wsutil.exe génère un stub de langage C en fonction des métadonnées WSDL fournies, ainsi que des définitions de type de données et des descriptions pour les types de données décrits par les schémas XML créés par l’utilisateur.
ms.assetid: d3c147d6-e370-4e8a-96d8-6660f3a2b996
keywords:
- Prise en charge WSDL
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19661e487c1a0dde871333376336bede239f9825
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734837"
---
# <a name="wsdl-and-service-contracts"></a>WSDL et contrats de service

L’utilitaire [Wsutil.exe](web-service-compiler-tool.md) génère un stub de langage C en fonction des métadonnées WSDL fournies, ainsi que des définitions de type de données et des descriptions pour les types de données décrits par les schémas XML créés par l’utilisateur.


Voici un exemple de document WSDL et de schéma XML qui sert de base à la discussion suivante :

``` syntax
<?xml version="1.0" encoding="utf-8"?>
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
  targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
   <xs:element name="SimpleMethod">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="a" type="xs:int" />
      <xs:element name="b" type="xs:int" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
   <xs:element name="SimpleMethodResponse">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="b" type="xs:int" />
      <xs:element name="c" type="xs:int" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
  </xs:schema>
 </wsdl:types>
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
 <wsdl:portType name="ISimpleService">
  <wsdl:operation name="SimpleMethod">
   <wsdl:input wsaw:Action="http://Example.org/ISimpleService/SimpleMethod" 
   message="tns:ISimpleService_SimpleMethod_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ISimpleService/SimpleMethodResponse" 
   message="tns:ISimpleService_SimpleMethod_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
 <wsdl:binding name="DefaultBinding_ISimpleService" type="tns:ISimpleService">
  <soap:binding transport="http://schemas.xmlsoap.org/soap/http" />
  <wsdl:operation name="SimpleMethod">
   <soap:operation soapAction="http://Example.org/ISimpleService/SimpleMethod" 
   style="document" />
   <wsdl:input>
    <soap:body use="literal" />
   </wsdl:input>
   <wsdl:output>
    <soap:body use="literal" />
   </wsdl:output>
  </wsdl:operation>
 </wsdl:binding>
 <wsdl:service name="SimpleService">
  <wsdl:port name="ISimpleService" binding="tns:DefaultBinding_ISimpleService">
   <soap:address location="http://Example.org/ISimpleService" />
  </wsdl:port>
 </wsdl:service>
</wsdl:definitions>
```

Cet exemple fournit un contrat, ISimpleService, avec une méthode unique, SimpleMethod. « SimpleMethod » a deux paramètres d’entrée de type **entier**, *a* et *b*, qui sont envoyés du client au service. De même, SimpleMethod a deux paramètres de sortie de type **entier**, *b* et *c*, qui sont retournés au client après l’achèvement de l’opération. Dans la syntaxe C annotée par SAL, la définition de la méthode se présente comme suit :

``` syntax
void SimpleMethod(__in int a, __inout int *  b, __out int * c );
```

Dans cette définition, ISimpleService est un contrat de service avec une seule opération de service : SimpleMethod.

Le fichier d’en-tête de sortie contient des définitions et des descriptions pour la référence externe. notamment :

-   Définitions de structure C pour les types d’éléments globaux.
-   Un prototype d’opération tel que défini dans le fichier actuel.
-   Un prototype de table de fonction pour les contrats spécifiés dans le fichier WSDL.
-   Le proxy client et les prototypes stub de service pour toutes les fonctions spécifiées dans le fichier actuel.
-   Structure de données de [**\_ \_ Description de l’élément WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) pour les éléments de schéma globaux définis dans le fichier actuel.
-   Structure de données de [**\_ \_ Description de message WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) pour tous les messages spécifiés dans le fichier actuel.
-   Structure de données de [**\_ \_ Description de contrat WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) pour tous les contrats spécifiés dans le fichier actuel.

Une structure globale est générée pour encapsuler toutes les descriptions globales pour les types de schémas et les types de modèles de service auxquels l’application peut faire référence. La structure est nommée à l’aide d’un nom de fichier normalisé. Dans cet exemple, Wsutil.exe génère une structure de définitions globale nommée « example \_ WSDL » qui contient toutes les descriptions de service Web. La définition de la structure est générée dans le fichier stub.

``` syntax
typedef struct _example_wsdl
{
  struct {
    WS_ELEMENT_DESCRIPTION SimpleMethod;
    WS_ELEMENT_DESCRIPTION SimpleMethodResponse;
  } elements;
  struct {
    WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_InputMessage;
    WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_OutputMessage;
  } messages;
  struct {
    WS_CONTRACT_DESCRIPTION DefaultBinding_ISimpleService;
  } contracts;
} _example_wsdl;

extern const _stockquote_wsdl stockquote_wsdl;
```

Pour les définitions d’éléments globaux dans le document de schéma XML (XSD), un prototype de [**\_ \_ Description d’élément WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) , ainsi que la définition de type C correspondante, sont générés pour chacun des éléments. Les prototypes pour les descriptions d’éléments pour SimpleMethod et SimpleMethodResponse sont générés en tant que membres dans la structure ci-dessus. Les structures C sont générées comme suit :

``` syntax
typedef struct SimpleMethod
{
  int   a;
  int   b;
} SimpleMethod;

typedef struct SimpleMethodResponse
{
  int   b;
  int   c;
} SimpleMethodResponse;
```

De même que pour les types complexes globaux, Wsutil.exe génère des définitions de structure de type C comme ci-dessus, sans les descriptions d’éléments correspondantes.

Pour une entrée WSDL, Wsutil.exe génère les définitions et les prototypes suivants :

-   Un prototype de [**\_ \_ Description de message WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) est généré pour la description du message. Cette description peut être utilisée par le modèle de service, ainsi que par la couche de message. Les structures de description de message sont des champs nommés « MessageName » dans la structure globale. Dans cet exemple, la description du message est générée en tant \_ que \_ champ ISimpleService SimpleMethod InputMessage dans la \_ structure ISimpleService SimpleMethod InputMessage \_ , comme spécifié dans le fichier WSDL.
-   [**WS \_ Le \_**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) prototype de description de contrat est généré pour la description de contrat. Cette description est utilisée par le modèle de service. Les structures de description de contrat sont des champs nommés « ContractName » dans la structure globale. Dans cet exemple, la description de contrat est générée en tant que \_ champ DefaultBinding ISimpleService dans la structure « \_ example \_ WSDL ».

Les spécifications de type et d’opération sont communes à la fois au proxy et au stub, et elles sont générées dans les deux fichiers. Wsutil.exe génère une copie uniquement si le proxy et le stub sont générés dans le même fichier.

## <a name="identifier-generation"></a>Génération de l’identificateur

Les structures C générées automatiquement répertoriées ci-dessus sont créées en fonction du nom spécifié dans le fichier WSDL. Un NCName XML n’est généralement pas considéré comme un identificateur C valide et les noms sont normalisés en fonction des besoins. Les valeurs hexadécimales ne sont pas converties et les lettres courantes telles que «  : », « / » et « . » sont converties en caractères de soulignement « \_ » pour améliorer la lisibilité.

## <a name="header-for-the-stub"></a>En-tête pour le stub

Pour chaque opération dans le contrat de service, une routine de rappel nommée « <operationname> callback » est générée. (Par exemple, l’opération « SimpleMethod » dans l’exemple de contrat de service a un rappel généré nommé « SimpleMethodCallback ».)

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT * context,
  int a, int *b, int *c,
  const WS_ASYNC_CONTEXT *asyncContext,
  WS_ERROR * error);
```

Pour chaque **portType** de table WSDL Wsutil.exe génère une table de fonctions représentant **portType**. Chaque opération sur **portType** a un pointeur de fonction correspondant vers le rappel présent dans la table de fonctions.

``` syntax
struct ISimpleServiceMethodTable
{
  ISimpleService_SimpleMethodCallback SimpleMethod;
};
```

Les prototypes de proxy sont générés pour toutes les opérations. Le nom du prototype est le nom de l’opération (dans ce cas, « SimpleMethod ») spécifié dans le fichier WSDL pour le contrat de service.

``` syntax
HRESULT WINAPI SimpleMethod(WS_CHANNEL *channel,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error );
```

## <a name="local-only-description-prototype-generation"></a>Génération de prototype de description locale uniquement

Les fichiers andstub de proxy contiennent la définition de la structure de définitions globale, y compris les prototypes et les définitions pour les structures contenant des descriptions locales uniquement et des implémentations de proxy/service stub client.

Tous les prototypes et définitions qui sont locaux au fichier stub sont générés dans le cadre d’une structure d’encapsulation. Cette structure de description locale globale fournit une hiérarchie claire des descriptions requises par la couche de sérialisation et le modèle de service. La structure de description locale a des prototypes similaires à ceux indiqués ci-dessous :

``` syntax
struct _filenameLocalDefinitions
{
  struct {
  // schema related output for all the embedded 
  // descriptions that needs to describe global complex types.
  } globalTypes;
  // global elements.
  struct {
  // schema related output, like field description
  // structure description, element description etc.
  ...
  } globalElements;
  struct {
  // messages and related descriptions
  } messages;
  struct {
  // contract and related descriptions.
  } contracts;
  struct {
  // XML dictionary entries.
  } dictionary;
} _filenameLocalDefinitions;
```

## <a name="referencing-definitions-from-other-files"></a>Référencement de définitions à partir d’autres fichiers

Les définitions locales peuvent référencer des descriptions générées dans un autre fichier. Par exemple, le message peut être défini dans le fichier de code C généré à partir du fichier WSDL, mais l’élément message peut être défini ailleurs dans le fichier de code C généré à partir du fichier XSD. Dans ce cas, Wsutil.exe génère une référence à l’élément global à partir du fichier qui contient la définition de message, comme illustré ci-dessous :

``` syntax
{  // WS_MESSAGE_DESCRIPTION
...
(WS_ELEMENT_DESRIPTION *)b_xsd.globalElement.<elementname>
  };
```

## <a name="global-element-descriptions"></a>Descriptions des éléments globaux

Pour chaque élément global défini dans un wsdl : type ou un fichier XSD, il existe un champ correspondant nommé **ElementName** dans le champ **GlobalElement** . Dans cet exemple, une structure nommée SimpleMethod est générée :

``` syntax
typedef struct _SimpleServiceLocal
{
  struct  // global elements
  {
    struct // SimpleMethod
    {
    ...
    WS_ELEMENT_DESCRIPTION SimpleMethod;
    } SimpleMethod;
    ...
  } globalElements;
}
```

Les autres descriptions requises par la description de l’élément sont générées dans le cadre de la structure conteneur. Si l’élément est un élément de type simple, il n’y a qu’un seul champ de [**\_ \_ Description d’élément WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) . Si le type d’élément est une structure, tous les champs et descriptions de structure associés sont générés dans le cadre de la structure de l’élément. Dans cet exemple, l’élément SimpleMethod est une structure contenant deux champs, **a** et **b**. Wsutil.exe génère la structure comme suit :

``` syntax
...
struct // SimpleMethod
{
  struct // SimpleMethod structure
  {
    WS_FIELD_DESCRIPTION a;
    WS_FIELD_DESCRIPTION b;
    WS_FIELD_DESCRIPTION * SimpleMethodFields [2];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleMethoddescs; // SimpleMethod
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleMethod;
...
```

Les structures incorporées et les éléments incorporés sont générés sous la forme de sous-structures en fonction des besoins.

## <a name="wsdl-related-definitions"></a>Définitions associées à WSDL

Wsutil.exe génère un champ sous la section WSDL pour chaque valeur **portType** définie sous le service WSDL : service spécifié.

``` syntax
...
struct { // WSDL
    struct { // portTypeName
        struct { // operationName
        } operationName;
    ...
    WS_OPERATION_DESCRIPTION* operations[numOperations];
    WS_CONTRACT_DESCRIPTION contractDesc;
    } portTypeName;
}
...
```

Wsutil.exe génère un champ f qui contient toutes les descriptions nécessaires pour l’opération, un tableau authentification unique de pointeurs vers chacune des descriptions d’opérations pour chaque méthode, et une [**\_ \_ Description de contrat WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) pour le **portType** spécifié.

Toutes les descriptions requises par les opérations sont générées dans le champ **NomOpération** sous le **portType** spécifié. Celles-ci incluent le champ de [**\_ \_ Description de l’élément WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) ainsi que la sous-structure des paramètres d’entrée et de sortie. De même, les champs de [**\_ \_ Description du message WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) pour le message d’entrée et le message de sortie facultatif sont inclus avec le ; [**WS \_ Champ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) de liste de description de paramètre pour tous les paramètres d’opération et le champ de [**\_ \_ Description d’opération WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) pour l’opération elle-même. Dans cet exemple, la structure de code de la description SimpleMethod est générée comme indiqué ci-dessous :

``` syntax
...
struct // messages
{
  WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_InputMessage;
  WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_OutputMessage;
} messages;
struct // contracts
{
  struct // DefaultBinding_ISimpleService
  {
    struct // SimpleMethod
    {
      WS_PARAMETER_DESCRIPTION params[3];
      WS_OPERATION_DESCRIPTION SimpleMethod;
    } SimpleMethod;
    WS_OPERATION_DESCRIPTION* operations[1];
    WS_CONTRACT_DESCRIPTION contractDesc;
  } DefaultBinding_ISimpleService;
} contracts;
...
```

## <a name="xml-dictionary-related-definitions"></a>Définitions associées au dictionnaire XML

Les noms et les espaces de noms utilisés dans différentes descriptions sont générés sous la forme de champs de type [**WS \_ XML \_ String**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string). Toutes ces chaînes sont générées dans le cadre d’un dictionnaire de constantes par fichier. La liste de chaînes et le champ de [**\_ \_ dictionnaire XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary) (nommé **dict** dans l’exemple ci-dessous) sont générés dans le cadre du champ dictionary de la structure **fileNameLocal** .

``` syntax
struct { // fileNameLocal
...
  struct { // dictionary
    struct { // XML string list
      WS_XML_STRING firstFieldName;
      WS_XML_STRING firstFieldNS;
      ...
    } xmlStrings;
  WS_XML_DICTIONARY dict;
  } dictionary;
}; // fileNameLocal;
```

Le tableau de [**la \_ \_ chaîne WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)s est généré sous la forme d’une série de champs de type **WS \_ XML \_ String**, nommés avec avec des noms conviviaux. Le stub généré utilise les noms conviviaux dans différentes descriptions pour une meilleure lisibilité.

Proxy client pour les opérations WSDL

Wsutil.exe génère un proxy client pour toutes les opérations. Les applications peuvent remplacer la signature de la méthode à l’aide d’une option de ligne de commande de préfixe.

``` syntax
HRESULT WINAPI bindingName_SimpleMethod(WS_SERVICE_PROXY *serviceProxy,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_CALL_PROPERTY* callProperties,
  ULONG callPropertyCount,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error )
{
  void* argList[] = {&a, &b, &c};
  return WsCall(_serviceProxy,
    (WS_OPERATION_DESCRIPTION*)&example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.SimpleMethod.SimpleMethod,
    (void **)&_argList,
    callProperties,
    callPropertyCount,
    heap,
    asyncContext,
    error
  );      
}
```

L’appelant de l’opération doit passer un paramètre de *segment de mémoire* valide. Les paramètres de sortie sont alloués à l’aide de la \_ valeur du tas WS spécifiée dans le paramètre *Heap* . La fonction appelante peut réinitialiser ou libérer le tas pour libérer de la mémoire pour tous les paramètres de sortie. En cas d’échec de l’opération, des informations supplémentaires sur l’erreur peuvent être récupérées à partir de l’objet facultatif Error s’il est disponible.

Wsutil.exe génère un stub de service pour toutes les opérations décrites dans liaison.

``` syntax
HRESULT CALLBACK ISimpleService_SimpleMethodStub(
  const WS_OPERATION_CONTEXT *context,
  void * stackStruct,
  void * callback,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR *error )
{
  SimpleMethodParamStruct *pstack = (SimpleMethodParamStruct *) stackstruct;
  SimpleMethodOperation operation = (SimpleMethodOperation)callback;
  return operation(context, pstack->a, &(pstack->b), &(pstack->c ), asyncContext, error );
}
```

La section ci-dessus décrit le prototype de la structure locale contenant toutes les définitions locales du fichier stub uniquement. Les sections suivantes décrivent les définitions des descriptions.

## <a name="wsdl-definition-generation"></a>Génération de définition WSDL

Wsutil.exe génère une structure statique constante (**const static**) nommée *<\_ nom de fichier>* LocalDefinitions de type *<\_ nom de service>* local qui contient toutes les définitions locales uniquement.

``` syntax
const static _SimpleServiceLocal example_wsdlLocalDefinitions =
{
  {  // global types
  ...
  }, // global types
  {  // global elements
  ...
  }, // global elements
  {  // messages
  ...
  }, //messages
  ...
  {  // dictionary
  ...
  }, // dictionary
},
```

Les descriptions WSDL suivantes sont prises en charge :

-   wsdl : service
-   wsdl : Binding
-   wsdl : portType
-   wsdl : opération
-   wsdl : message

## <a name="processing-wsdloperation-and-wsdlmessage"></a>Traitement de wsdl : Operation et WSDL : message

Chaque opération spécifiée dans le document WSDL est mappée à une opération de service par [Wsutil.exe](web-service-compiler-tool.md). L’outil génère des définitions distinctes des opérations de service pour le serveur et le client.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ISimpleService">
  <wsdl:operation name="SimpleMethod">
   <wsdl:input wsaw:Action="http://Example.org/ISimpleService/SimpleMethod" 
   message="tns:ISimpleService_SimpleMethod_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ISimpleService/SimpleMethodResponse" 
   message="tns:ISimpleService_SimpleMethod_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
</wsdl:definitions>
```

La disposition des éléments de données de message andOutput d’entrée est évaluée par l’outil pour générer les métadonnées de sérialisation pour l’infrastructure avec la signature réelle de l’opération de service obtenue à laquelle les messages d’entrée et de sortie sont associés.

Les métadonnées pour chaque opération d’un **portType** spécifique ont une entrée et éventuellement un message de sortie, chacun de ces messages est mappé à [**une \_ \_ Description de message WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description). Dans cet exemple, l’entrée et le message de sortie sur l’opération dans portType sont mappés à inputMessageDescription et éventuellement outputMessageDescription sur la description de l' [**\_ \_ opération WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) , respectivement.

Pour chaque message WSDL, l’outil génère la [**\_ \_ Description du message WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) qui fait référence à la définition de la description de l' [**\_ élément \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) , comme illustré ci-dessous :

``` syntax
... 
{    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

La description du message fait référence à la description de l’élément d’entrée. Étant donné que l’élément est défini globalement, la description du message référence la définition globale au lieu de l’élément statique local. De même, si l’élément est défini dans un autre fichier, Wsutil.exe génère une référence à la structure globalement définie dans ce fichier. Par exemple, si SimpleMethodResponse est défini dans un autre fichier example. xsd, Wsutil.exe génère le code suivant à la place :

``` syntax
...
{    // message description for ISimpleService_SimpleMethod_InputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_xsd.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

Chaque description de message contient l’action et la description de l’élément spécifique (un champ de type [**WS \_ Element \_ Description**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)) pour tous les éléments de données de message. Dans le cas d’un message de style RPC ou d’un message avec plusieurs parties, un élément wrapper est créé pour encapsuler les informations supplémentaires.

## <a name="rpc-style-support"></a>Prise en charge du style RPC

Wsutil.exe prend en charge les opérations de style document et de style RPC selon l’extension de liaison WSDL 1,1 pour la spécification SOAP 1,2. Les opérations RPC et de style littéral sont marquées en tant qu' \_ opération de LITTÉRAL WS RPC \_ \_ . Le modèle de service ignore le nom de l’élément wrapper du corps de la réponse dans les opérations RPC/littérales.

Wsutil.exe ne prend pas en charge en mode natif les opérations de style encodage. Le \_ \_ paramètre de mémoire tampon XML WS est généré pour l’encodage des messages, et les développeurs doivent remplir directement la mémoire tampon opaque.

## <a name="multiple-message-parts-support"></a>Prise en charge de plusieurs parties de messages

Wsutil.exe prend en charge plusieurs parties de message dans un message. Un message à parties multiples peut être spécifié comme suit :

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:message name="ISimpleService_MutipleParts_InputMessage">
  <wsdl:part name="part1" element="tns:SimpleElement1" />
  <wsdl:part name="part2" element="tns:SimpleElement2" />
 </wsdl:message>
</wsdl:definitions>
```

Wsutil.exe génère un champ de [**\_ \_ type du struct WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type) pour l’élément message si le message contient plusieurs parties. Si le message est représenté à l’aide du style de document, Wsutil.exe génère un élément wrapper avec le type struct. L’élément wrapper n’a pas de nom ou d’espace de noms spécifique, et la structure Wrapper contient tous les éléments de toutes les parties en tant que champs. L’élément wrapper est destiné à un usage interne uniquement et n’est pas sérialisé dans le corps du message.

Si le message utilise une représentation de type littéral ou RPC, Wsutil.exe crée un élément wrapper avec le nom de l’opération comme nom d’élément et l’espace de noms spécifié en tant qu’espace de noms de service en fonction de la spécification de l’extension SOAP WSDL. La structure de l’élément contient un tableau de champs représentant les types spécifiés dans les parties de message. L’élément wrapper est mappé à l’élément supérieur réel dans le corps du message, comme indiqué dans la spécification SOAP.

Côté serveur, chaque opération génère un typedef de l’opération de service serveur résultante. Ce typedef est utilisé pour faire référence à l’opération dans la table de fonctions comme décrit précédemment. Chaque opération entraîne également la génération d’une fonction stub qui nfrastructure a appelle pour le compte du délégué à la méthode réelle.

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT* context,
  unsigned int  a,
  unsigned int * b,
  unsigned int * c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error
  );
```

Pour l’opération SimpleMethod, le typedef SimpleMethodOperation est défini ci-dessus. Notez que la méthode générée a un argument développé listwith la partie de message pour le message d’entrée et de sortie pour l’opération SimpleMethod en tant que paramètres nommés.

Côté client, chaque opération est mappée à une opération de service proxy.

``` syntax
HRESULT WINAPI SimpleMethod (
  WS_SERVICE_PROXY* serviceProxy,
  ws_heap *heap,
  unsigned int  a,
  unsigned int * b,
  unsigned int * c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);
```

## <a name="processing-wsdlbinding"></a>Traitement de wsdl : Binding

Le modèle de service WWSAPI prend en charge l’extension de liaison theSOAP. Pour chaque liaison, il existe un **portType** associé.

Le transport spécifié dans l’extension de liaison SOAP est un avis uniquement. L’application doit fournir des informations de transport lors de la création d’un canal. Actuellement, nous prenons en charge la \_ liaison WS http \_ et les \_ liaisons de liaison WS TCP \_ .

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:binding name="DefaultBinding_ISimpleService" type="tns:ISimpleService">
  <soap:binding transport="http://schemas.xmlsoap.org/soap/http" />
  <wsdl:operation name="SimpleMethod">
   <soap:operation soapAction="http://Example.org/ISimpleService/SimpleMethod" 
   style="document" />
   <wsdl:input>
    <soap:body use="literal" />
   </wsdl:input>
   <wsdl:output>
    <soap:body use="literal" />
   </wsdl:output>
  </wsdl:operation>
 </wsdl:binding>
</wsdl:definitions>
```

Dans notre exemple de document WSDL, nous disposons d’un seul **portType** pour ISimpleService. La liaison SOAP fournie indique le transport HTTP, qui est spécifié en tant \_ que \_ liaison WS http. Notez que cette structure n’a pas de décoration statique, car cette structure doit être disponible pour l’application.

Traitement de wsdl : portType

Chaque **portType** dans WSDL est constitué d’une ou plusieurs opérations. L’opération doit être cohérente avec l’extension de liaison SOAP indiquée dans WSDL : Binding.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ISimpleService">
  <wsdl:operation name="SimpleMethod">
   ...
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

Dans cet exemple, ISimpleService **portType** contient uniquement l’opération SimpleMethod. Cela est cohérent avec la section de liaison dans laquelle il n’existe qu’une seule opération WSDL qui est mappée à une action SOAP.

Étant donné que ISimpleService **portType** n’a qu’une seule opération--SimpleMethod--la table de fonctions correspondante contient uniquement des SimpleMethod en tant qu’opération de service.

En termes de métadonnées, chaque **portType** est mappé par Wsutil.exe à [**une \_ \_ Description de contrat WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description). Chaque opération au sein d’un **portType** est mappée à une [**\_ \_ Description d’opération WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).

Dans cet exemple, **portType** , l’outil génère la [**\_ \_ Description WS Contract**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) pour ISimpleService. Cette description de contrat contient le nombre spécifique d’opérations disponibles sur ISimpleService **portType** , ainsi qu’un tableau [**de \_ \_ Description d’opération WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) représentant les opérations individuelles définies sur PortType pour ISimpleService. Étant donné qu’il n’existe qu’une seule opération sur ISimpleService portType pour ISimpleService, il n’y a également qu’une seule définition de **\_ \_ Description d’opération WS** .

``` syntax
...  part of LocalDefinitions structure
{    // array of operations for DefaultBinding_ISimpleService
(WS_OPERATION_DESCRIPTION*)&example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.SimpleMethod.SimpleMethod,
},    // array of operations for DefaultBinding_ISimpleService
{    // contract description for DefaultBinding_ISimpleService
1,
(WS_OPERATION_DESCRIPTION**)example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.operations,
WS_HTTP_CHANNEL_BINDING,
},  // end of contract description for DefaultBinding_ISimpleService
},    // DefaultBinding_ISimpleService       ...
```

## <a name="processing-wsdlservice"></a>Traitement de wsdl : service

WsUtil.exe utilise les services pour rechercher Binding/types et génère une structure de contrat qui décrit les types, les messages, les définitions PortType, etc. Les descriptions de contrat sont accessibles en externe et sont générées dans le cadre de la structure de définition globale spécifiée par le biais de l’en-tête généré.

WsUtil.exe prend en charge les extensions EndpointReference définies dans WSDL : port. La référence de point de terminaison est définie dans WS-Addressing comme un moyen de décrire les informations de [point de terminaison](endpoint-address.md) d’un service. Le texte d’extension de référence de point de terminaison d’entrée enregistré sous forme de [**\_ \_ chaîne WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string), ainsi que la description de l' [**adresse de point de \_ terminaison \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) correspondante sont générés dans la section endpointReferences de la structure globale.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:service name="SimpleService">
  <wsdl:port name="ISimpleService" binding="tns:DefaultBinding_ISimpleService">
   <soap:address location="http://Example.org/ISimpleService" />
   <wsa:EndpointReference>
    <wsa:Address>http://example.org/wcfmetadata/WSHttpNon</wsa:Address>
   </wsa:EndpointReference> 
  </wsdl:port>
 </wsdl:service>
</wsdl:definitions>
```

``` syntax
  const _example_wsdl example_wsdl =
  {
  ... // global element description
  {// messages
  {    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.ISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethod,
},    // message description for ISimpleService_SimpleMethod_InputMessage
{    // message description for ISimpleService_SimpleMethod_OutputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.ISimpleService_SimpleMethod_OutputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodResponse,
},    // message description for ISimpleService_SimpleMethod_OutputMessage
}, // messages
{// contracts
{   // DefaultBinding_ISimpleService
1,
(WS_OPERATION_DESCRIPTION**)example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.operations,
WS_HTTP_CHANNEL_BINDING,
},    // end of DefaultBinding_ISimpleService
    }, // contracts
    {
        {
            {   // endpointAddressDescription
                WS_ADDRESSING_VERSION_0_9,
            },                    
            (WS_XML_STRING*)&xml_string_generated_in_stub // endpointReferenceString
        }, //DefaultBinding_ISimpleService
    }, // endpointReferences
}
```

Pour créer [**une \_ \_ adresse de point de terminaison WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) à l’aide des métadonnées générées par WsUtil :

``` syntax
WsCreateReader      // Create a WS_XML_READER
Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput          // Set the encoding and input of the reader to generated endpointReferenceString
WsReadType        // Read WS_ENDPOINT_ADDRESS from the reader
    // Using WS_ELEMENT_TYPE_MAPPING, WS_ENDPOINT_ADDRESS_TYPE and generated endpointAddressDescription, 
```

Les chaînes constantes du proxy client ou du stub de service sont générées en tant que champs de type WS \_ XML \_ String et il existe un dictionnaire constant pour toutes les chaînes du fichier proxy ou stub. Chaque chaîne du dictionnaire est générée sous la forme d’un champ dans la partie dictionnaire de la structure locale pour une meilleure lisibilité.

``` syntax
... // dictionary part of LocalDefinitions structure
{    // xmlStrings
  { // xmlStrings
    WS_XML_STRING_DICTIONARY_VALUE("a",&example_wsdlLocalDefinitions.dictionary.dict, 0), 
    WS_XML_STRING_DICTIONARY_VALUE("http://Sapphire.org",&example_wsdlLocalDefinitions.dictionary.dict, 1), 
    WS_XML_STRING_DICTIONARY_VALUE("b",&example_wsdlLocalDefinitions.dictionary.dict, 2), 
    WS_XML_STRING_DICTIONARY_VALUE("SimpleMethod",&example_wsdlLocalDefinitions.dictionary.dict, 3),
    ...
  },  // end of xmlStrings
  {   // SimpleServicedictionary
    // 45026280-d5dc-4570-8195-4d66d13bfa34
    { 0x45026280, 0xd5dc, 0x4570, { 0x81, 0x95, 0x4d,0x66, 0xd1, 0x3b, 0xfa, 0x34 } },
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings,
    stringCount,
    TRUE,
  },
}
...
```

## <a name="processing-wsdltype"></a>Traitement de wsdl : type

Wsutil.exe prend en charge uniquement les documents de schéma XML (XSD) dans la spécification WSDL : type. Un cas particulier est lorsqu’un port de message spécifie une définition d’élément global. Pour plus d’informations sur l’heuristique utilisée dans ces cas, consultez la section suivante.

## <a name="parameter-processing-heuristics"></a>Heuristiques de traitement de paramètres

Dans le modèle de service, les messages WSDL sont mappés à des paramètres spécifiques dans une méthode. Wsutil.exe a deux styles de génération de paramètres : dans le premier style, l’opération a un paramètre pour le message d’entrée et un paramètre pour le message de sortie (si nécessaire); dans le deuxième style, Wsutil.exe utilise une méthode heuristique pour mapper et développer des champs dans les structures pour les messages d’entrée et les messages de sortie vers des paramètres différents dans l’opération. Les messages d’entrée et de sortie doivent avoir des éléments de message de type structure pour générer cette deuxième approche.

Wsutil.exe utilise les règles suivantes lors de la génération de paramètres d’opération à partir des messages d’entrée et de sortie :

-   Pour les messages d’entrée et de sortie avec plusieurs parties de message, chaque partie de message est un paramètre distinct dans l’opération, avec le nom de la partie de message comme nom de paramètre.
-   Pour un message de style RPC avec une partie de message, la partie de message est un paramètre dans l’opération, avec le nom de la partie de message comme nom de paramètre.
-   Pour les messages d’entrée et de sortie de style document avec une partie de message :
    -   Si le nom d’une partie de message est « Parameters » et que le type d’élément est une structure, chaque champ de la structure est traité comme un paramètre distinct avec le nom de champ comme nom de paramètre.
    -   Si le nom de la partie de message n’est pas « Parameters », le message est un paramètre dans l’opération avec le nom de message utilisé comme nom de paramètre correspondant.
-   Pour le message d’entrée et de sortie de style de document avec l’élément nillable, le message est mappé à un paramètre, avec le nom de la partie de message comme nom de paramètre. Un niveau supplémentaire d’indirection est ajouté pour indiquer que le pointeur peut être **null**.
-   Si un champ apparaît uniquement dans l’élément de message d’entrée, le champ est traité comme un \[ \] paramètre in.
-   Si un champ s’affiche uniquement dans l’élément de message de sortie, le champ est traité comme un \[ paramètre de sortie \] .
-   S’il existe un champ avec le même nom et le même type qui apparaît dans le message d’entrée et le message de sortie, le champ est traité comme un \[ paramètre in, out \] .

Les outils suivants sont utilisés pour déterminer la direction des paramètres :

-   Si un champ n’apparaît que dans un élément de message d’entrée, le champ est traité comme dans seul paramètre.
-   Si un champ n’apparaît que dans un élément de message de sortie, le champ est traité comme paramètre de sortie uniquement.
-   S’il existe un champ avec le même nom et le même type qui apparaît à la fois dans le message d’entrée et le message de sortie, le champ est traité comme un paramètre in, out.

Wsutil.exe prend en charge uniquement les éléments séquencés. Il rejette l’ordonnancement non valide en ce qui concerne \[ dans, les paramètres de sortie \] si Wsutil.exe ne pouvez pas combiner les paramètres in et out dans une liste de paramètres unique. Des suffixes peuvent être ajoutés aux noms de paramètres pour éviter la collision de noms.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
</wsdl:definitions>
```

Wsutil.exe considère les champs de TNS : SimpleMethod et TNS : SimpleMethodResponse ATO comme paramètres, comme indiqué dans les définitions de paramètres ci-dessous :

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
  targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
   <xs:import namespace="http://Example.org" />
   <xs:element name="SimpleMethod">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="a" type="xs:unsignedInt" />
      <xs:element name="b" type="xs:unsignedInt" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
   <xs:element name="SimpleMethodResponse">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="b" type="xs:unsignedInt" />
      <xs:element name="c" type="xs:unsignedInt" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
  </xs:schema>
 </wsdl:types>
</wsdl:definitions>
```

Wsutil.exe développe la liste de paramètres à partir des champs de la liste ci-dessus et génère la structure **ParamStruct** dans l’exemple de code suivant. Le temps d’exécution du modèle de service peut utiliser cette structure pour passer des arguments aux stubs du client et du serveur.

``` syntax
typedef struct SimpleMethodParamStruct {
  unsigned int   a;  
  unsigned int   b;
  unsigned int   c;
} ;
```

Cette structure est utilisée uniquement pour décrire le frame de pile côté client et côté serveur. Aucune modification n’est apportée à la description du message ou aux descriptions d’éléments référencées par la description du message.

``` syntax
  // following are local definitions for the complex type
  { // field description for a
  WS_ELEMENT_FIELD_MAPPING,
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aLocalName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  WS_INT32_TYPE,
  0,
  WsOffsetOf(_SimpleMethod, a),
  0,
  0,
  },    // end of field description for a
  { // field description for b
  WS_ELEMENT_FIELD_MAPPING,
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.bLocalName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  WS_INT32_TYPE,
  0,
  WsOffsetOf(_SimpleMethod, b),
  0,
  0,
  },    // end of field description for b
  {    // fields description for _SimpleMethod
  (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs.a,
  (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs.b,
  },
  {  // structure definition
  sizeof(_SimpleMethod),
  __alignof(_SimpleMethod),
  (WS_FIELD_DESCRIPTION**)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs._SimpleMethodFields,
  WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs._SimpleMethodFields),
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings._SimpleMethodTypeName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  0,
  },   // struct description for _SimpleMethod
  // following are global definitions for the out parameter
  ...
  {  // element description
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings._SimpleMethodTypeName,
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  WS_STRUCT_TYPE,
  (void *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs.structDesc,
  },
  {    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.ISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethod,
  },    // message description for ISimpleService_SimpleMethod_InputMessage
```

En règle générale, un niveau d’indirection est ajouté pour tous les paramètres out \[ \] et \[ in, out \] .

## <a name="parameterless-operation"></a>Opération sans paramètre

Pour les opérations de document et de littéral, Wsutil.exe traite l’opération comme ayant un paramètre d’entrée et un paramètre de sortie si :

-   Le message d’entrée ou de sortie a plusieurs parties.
-   Il n’existe qu’une seule partie de message et le nom de la partie de message n’est pas « Parameters ».

.. Dans l’exemple ci-dessus, en supposant que les parties de message sont nommées *param* et *ParamOut*, la signature de la méthode devient le code suivant :

``` syntax
typedef struct SimpleMethod{
unsigned int a;
unsigned int b;
};

typedef struct SimpleMethodResponse {
unsigned int b;
unsigned int c;
};

typedef  struct ISimpleService_SimpleMethodParamStruct
{
SimpleMethod  * SimpleMethod;
SimpleMethodResponse  * SimpleMethodResponse;
} ISimpleService_SimpleMethodParamStruct;
```

Wsutil.exe génère une signature de version pour la description de l’opération, de sorte que le moteur de modèle de service WsCall et côté serveur peut vérifier si la description générée est applicable à la plateforme actuelle.

Ces informations de version sont générées dans le cadre de la structure de la [**\_ \_ Description de l’opération WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) . Le numéro de version peut être traité comme un sélecteur ARM d’Union pour que la structure soit extensible. Actuellement, la valeur de **VersionId** est définie sur rétablira sans les champs suivants. Les versiosn ultérieures peuvent incrémenter le numéro de version et inclure plus de champs en fonction des besoins. Par exemple, Wsutil.exe génère actuellement le code suivant en fonction de l’ID de version :

``` syntax
{ // SimpleMethod
{ // parameter descriptions for SimpleMethod
{ WS_PARAMETER_TYPE_NORMAL, (USHORT)0, (USHORT)-1 },
{ WS_PARAMETER_TYPE_NORMAL, (USHORT)1, (USHORT)-1 },
{ WS_PARAMETER_TYPE_NORMAL, (USHORT)-1, (USHORT)1 },
},    // parameter descriptions for SimpleMethod
{    // operation description for SimpleMethod
1,
(WS_MESSAGE_DESCRIPTION*)&example_wsdl.messages.ISimpleService_SimpleMethod_InputMessage,
(WS_MESSAGE_DESCRIPTION*)&example_wsdl.messages.ISimpleService_SimpleMethod_OutputMessage,
3,
(WS_PARAMETER_DESCRIPTION*)example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.SimpleMethod.params,
SimpleMethodOperationStub
}, //operation description for SimpleMethod
},  // SimpleMethod
```

À l’avenir, il pourrait être développé comme suit :

``` syntax
WS_OPERATION_DESCRIPTION simpleMethodOperationDesc =
{
  2,
  &ISimpleService_SimpleMethod_InputputMessageDesc,
  &ISimpleService_SimpleMethod_OutputMessageDesc,
  WsCountOf(SimpleMethodParameters),
  SimpleMethodParameters,
  ISimpleService_SimpleMethod_Stub,
  &forwardToString;   // just as an example.
};
```

## <a name="security"></a>Sécurité

Consultez la section sécurité dans la rubrique de l' [outil compilateur Wsutil](wsutil-compiler-tool.md) .

 

 




