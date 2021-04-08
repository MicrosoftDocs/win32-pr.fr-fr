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
# <a name="wsdl-and-service-contracts"></a><span data-ttu-id="b9bcb-106">WSDL et contrats de service</span><span class="sxs-lookup"><span data-stu-id="b9bcb-106">WSDL and Service Contracts</span></span>

<span data-ttu-id="b9bcb-107">L’utilitaire [Wsutil.exe](web-service-compiler-tool.md) génère un stub de langage C en fonction des métadonnées WSDL fournies, ainsi que des définitions de type de données et des descriptions pour les types de données décrits par les schémas XML créés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-107">The [Wsutil.exe](web-service-compiler-tool.md) utility generates a C language stub according to supplied WSDL metadata, as well as data type definitions and descriptions for data types described by user-authored XML schemas.</span></span>


<span data-ttu-id="b9bcb-108">Voici un exemple de document WSDL et de schéma XML qui sert de base à la discussion suivante :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-108">The following is an example WSDL document and XML schema that serves as a basis for the discussion that follows:</span></span>

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

<span data-ttu-id="b9bcb-109">Cet exemple fournit un contrat, ISimpleService, avec une méthode unique, SimpleMethod.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-109">This example provides a contract, ISimpleService, with a single method, SimpleMethod.</span></span> <span data-ttu-id="b9bcb-110">« SimpleMethod » a deux paramètres d’entrée de type **entier**, *a* et *b*, qui sont envoyés du client au service.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-110">"SimpleMethod" has two input parameters of type **integer**, *a* and *b*, that are sent from the client to the service.</span></span> <span data-ttu-id="b9bcb-111">De même, SimpleMethod a deux paramètres de sortie de type **entier**, *b* et *c*, qui sont retournés au client après l’achèvement de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-111">Likewise, SimpleMethod has two output parameters of type **integer**, *b* and *c*, which are returned to the client after successful completion.</span></span> <span data-ttu-id="b9bcb-112">Dans la syntaxe C annotée par SAL, la définition de la méthode se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-112">In SAL-annotated C syntax, the method definition appears as follows:</span></span>

``` syntax
void SimpleMethod(__in int a, __inout int *  b, __out int * c );
```

<span data-ttu-id="b9bcb-113">Dans cette définition, ISimpleService est un contrat de service avec une seule opération de service : SimpleMethod.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-113">In this definition, ISimpleService is a service contract with a single service operation: SimpleMethod.</span></span>

<span data-ttu-id="b9bcb-114">Le fichier d’en-tête de sortie contient des définitions et des descriptions pour la référence externe.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-114">The output header file contains definitions and descriptions for external reference.</span></span> <span data-ttu-id="b9bcb-115">notamment :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-115">This includes:</span></span>

-   <span data-ttu-id="b9bcb-116">Définitions de structure C pour les types d’éléments globaux.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-116">C structure definitions for global element types.</span></span>
-   <span data-ttu-id="b9bcb-117">Un prototype d’opération tel que défini dans le fichier actuel.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-117">An operation prototype as defined in current file.</span></span>
-   <span data-ttu-id="b9bcb-118">Un prototype de table de fonction pour les contrats spécifiés dans le fichier WSDL.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-118">A function table prototype for the contracts specified in the WSDL file.</span></span>
-   <span data-ttu-id="b9bcb-119">Le proxy client et les prototypes stub de service pour toutes les fonctions spécifiées dans le fichier actuel.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-119">Client proxy and service stub prototypes for all the functions specified in current file.</span></span>
-   <span data-ttu-id="b9bcb-120">Structure de données de [**\_ \_ Description de l’élément WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) pour les éléments de schéma globaux définis dans le fichier actuel.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-120">A [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) data structure for the global schema elements defined in current file.</span></span>
-   <span data-ttu-id="b9bcb-121">Structure de données de [**\_ \_ Description de message WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) pour tous les messages spécifiés dans le fichier actuel.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-121">A [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) data structure for all the messages specified in current file.</span></span>
-   <span data-ttu-id="b9bcb-122">Structure de données de [**\_ \_ Description de contrat WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) pour tous les contrats spécifiés dans le fichier actuel.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-122">A [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) data structure for all the contracts specified in current file.</span></span>

<span data-ttu-id="b9bcb-123">Une structure globale est générée pour encapsuler toutes les descriptions globales pour les types de schémas et les types de modèles de service auxquels l’application peut faire référence.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-123">One global structure is generated to encapsulate all the global descriptions for the schema types and service model types to which the application can refer.</span></span> <span data-ttu-id="b9bcb-124">La structure est nommée à l’aide d’un nom de fichier normalisé.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-124">The structure is named using a normalized file name.</span></span> <span data-ttu-id="b9bcb-125">Dans cet exemple, Wsutil.exe génère une structure de définitions globale nommée « example \_ WSDL » qui contient toutes les descriptions de service Web.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-125">In this example, Wsutil.exe generates a global definitions structure named "example\_wsdl" that contains all the web service descriptions.</span></span> <span data-ttu-id="b9bcb-126">La définition de la structure est générée dans le fichier stub.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-126">The structure definition is generated in the stub file.</span></span>

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

<span data-ttu-id="b9bcb-127">Pour les définitions d’éléments globaux dans le document de schéma XML (XSD), un prototype de [**\_ \_ Description d’élément WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) , ainsi que la définition de type C correspondante, sont générés pour chacun des éléments.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-127">For global element definitions in the XML schema document (XSD), one [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) prototype, as well as the corresponding C type definition, are generated for each of the elements.</span></span> <span data-ttu-id="b9bcb-128">Les prototypes pour les descriptions d’éléments pour SimpleMethod et SimpleMethodResponse sont générés en tant que membres dans la structure ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-128">The prototypes for the element descriptions for SimpleMethod and SimpleMethodResponse are generated as members in the structure above.</span></span> <span data-ttu-id="b9bcb-129">Les structures C sont générées comme suit :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-129">The C structures are generated as follows:</span></span>

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

<span data-ttu-id="b9bcb-130">De même que pour les types complexes globaux, Wsutil.exe génère des définitions de structure de type C comme ci-dessus, sans les descriptions d’éléments correspondantes.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-130">Similarly for global complex types, Wsutil.exe generates type C structure definitions like above, without matching element descriptions.</span></span>

<span data-ttu-id="b9bcb-131">Pour une entrée WSDL, Wsutil.exe génère les définitions et les prototypes suivants :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-131">For WSDL input, Wsutil.exe generates the following prototypes and definitions:</span></span>

-   <span data-ttu-id="b9bcb-132">Un prototype de [**\_ \_ Description de message WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) est généré pour la description du message.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-132">A [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) prototype is generated for the message description.</span></span> <span data-ttu-id="b9bcb-133">Cette description peut être utilisée par le modèle de service, ainsi que par la couche de message.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-133">This description can be used by the service model as well as the message layer.</span></span> <span data-ttu-id="b9bcb-134">Les structures de description de message sont des champs nommés « MessageName » dans la structure globale.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-134">Message description structures are fields named "messagename" in the global structure.</span></span> <span data-ttu-id="b9bcb-135">Dans cet exemple, la description du message est générée en tant \_ que \_ champ ISimpleService SimpleMethod InputMessage dans la \_ structure ISimpleService SimpleMethod InputMessage \_ , comme spécifié dans le fichier WSDL.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-135">In this example, the message description is generated as the ISimpleService\_SimpleMethod\_InputMessage field in the ISimpleService\_SimpleMethod\_InputMessage structure as specified in the WSDL file.</span></span>
-   <span data-ttu-id="b9bcb-136">[**WS \_ Le \_**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) prototype de description de contrat est généré pour la description de contrat.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-136">[**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) prototype is generated for the contract description.</span></span> <span data-ttu-id="b9bcb-137">Cette description est utilisée par le modèle de service.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-137">This description is used by service model.</span></span> <span data-ttu-id="b9bcb-138">Les structures de description de contrat sont des champs nommés « ContractName » dans la structure globale.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-138">Contract description structures are fields named "contractname" in the global structure.</span></span> <span data-ttu-id="b9bcb-139">Dans cet exemple, la description de contrat est générée en tant que \_ champ DefaultBinding ISimpleService dans la structure « \_ example \_ WSDL ».</span><span class="sxs-lookup"><span data-stu-id="b9bcb-139">In this example, the contract description is generated as the DefaultBinding\_ISimpleService field in the structure "\_example\_wsdl".</span></span>

<span data-ttu-id="b9bcb-140">Les spécifications de type et d’opération sont communes à la fois au proxy et au stub, et elles sont générées dans les deux fichiers.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-140">Operation and type specifications are common to both proxy and stub and they are generated in both files.</span></span> <span data-ttu-id="b9bcb-141">Wsutil.exe génère une copie uniquement si le proxy et le stub sont générés dans le même fichier.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-141">Wsutil.exe generates one copy only if both the proxy and stub are generated in the same file.</span></span>

## <a name="identifier-generation"></a><span data-ttu-id="b9bcb-142">Génération de l’identificateur</span><span class="sxs-lookup"><span data-stu-id="b9bcb-142">Identifier generation</span></span>

<span data-ttu-id="b9bcb-143">Les structures C générées automatiquement répertoriées ci-dessus sont créées en fonction du nom spécifié dans le fichier WSDL.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-143">The autogenerated C structures listed above are created based on the name specified in WSDL file.</span></span> <span data-ttu-id="b9bcb-144">Un NCName XML n’est généralement pas considéré comme un identificateur C valide et les noms sont normalisés en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-144">An XML NCName is not commonly considered a valid C identifier, and the names are normalized as needed.</span></span> <span data-ttu-id="b9bcb-145">Les valeurs hexadécimales ne sont pas converties et les lettres courantes telles que «  : », « / » et « . » sont converties en caractères de soulignement « \_ » pour améliorer la lisibilité.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-145">Hex values are not converted, and common letters like ':', '/' and '.' are converted to the underscore '\_' character to improve readability.</span></span>

## <a name="header-for-the-stub"></a><span data-ttu-id="b9bcb-146">En-tête pour le stub</span><span class="sxs-lookup"><span data-stu-id="b9bcb-146">Header for the stub</span></span>

<span data-ttu-id="b9bcb-147">Pour chaque opération dans le contrat de service, une routine de rappel nommée « <operationname> callback » est générée.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-147">For each operation in the service contract, one callback routine named "<operationname>Callback" is generated.</span></span> <span data-ttu-id="b9bcb-148">(Par exemple, l’opération « SimpleMethod » dans l’exemple de contrat de service a un rappel généré nommé « SimpleMethodCallback ».)</span><span class="sxs-lookup"><span data-stu-id="b9bcb-148">(For example, the operation "SimpleMethod" in the example service contract has a generated callback named "SimpleMethodCallback".)</span></span>

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT * context,
  int a, int *b, int *c,
  const WS_ASYNC_CONTEXT *asyncContext,
  WS_ERROR * error);
```

<span data-ttu-id="b9bcb-149">Pour chaque **portType** de table WSDL Wsutil.exe génère une table de fonctions représentant **portType**.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-149">For each WSDL **portType** Wsutil.exe generates a function table representing **portType**.</span></span> <span data-ttu-id="b9bcb-150">Chaque opération sur **portType** a un pointeur de fonction correspondant vers le rappel présent dans la table de fonctions.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-150">Each operation on the **portType** has a corresponding function pointer to the callback present in the function table.</span></span>

``` syntax
struct ISimpleServiceMethodTable
{
  ISimpleService_SimpleMethodCallback SimpleMethod;
};
```

<span data-ttu-id="b9bcb-151">Les prototypes de proxy sont générés pour toutes les opérations.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-151">Proxy prototypes are generated for all operations.</span></span> <span data-ttu-id="b9bcb-152">Le nom du prototype est le nom de l’opération (dans ce cas, « SimpleMethod ») spécifié dans le fichier WSDL pour le contrat de service.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-152">The prototype name is the operation name (in this case, "SimpleMethod") specified in WSDL file for the service contract.</span></span>

``` syntax
HRESULT WINAPI SimpleMethod(WS_CHANNEL *channel,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error );
```

## <a name="local-only-description-prototype-generation"></a><span data-ttu-id="b9bcb-153">Génération de prototype de description locale uniquement</span><span class="sxs-lookup"><span data-stu-id="b9bcb-153">Local-only Description Prototype Generation</span></span>

<span data-ttu-id="b9bcb-154">Les fichiers andstub de proxy contiennent la définition de la structure de définitions globale, y compris les prototypes et les définitions pour les structures contenant des descriptions locales uniquement et des implémentations de proxy/service stub client.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-154">The proxy andstub files contain the definition for the global definitions structure, including prototypes and definitions for the structures containing local-only descriptions and client proxy/service stub implementations.</span></span>

<span data-ttu-id="b9bcb-155">Tous les prototypes et définitions qui sont locaux au fichier stub sont générés dans le cadre d’une structure d’encapsulation.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-155">All prototypes and definitions that are local to the stub file are generated as part of an encapsulating structure.</span></span> <span data-ttu-id="b9bcb-156">Cette structure de description locale globale fournit une hiérarchie claire des descriptions requises par la couche de sérialisation et le modèle de service.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-156">This overarching local description structure provides a clear hierarchy of the descriptions required by the serialization layer and the service model.</span></span> <span data-ttu-id="b9bcb-157">La structure de description locale a des prototypes similaires à ceux indiqués ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-157">The local description structure has prototypes similar to the one shown below:</span></span>

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

## <a name="referencing-definitions-from-other-files"></a><span data-ttu-id="b9bcb-158">Référencement de définitions à partir d’autres fichiers</span><span class="sxs-lookup"><span data-stu-id="b9bcb-158">Referencing definitions from other files</span></span>

<span data-ttu-id="b9bcb-159">Les définitions locales peuvent référencer des descriptions générées dans un autre fichier.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-159">Local definitions can reference descriptions generated in another file.</span></span> <span data-ttu-id="b9bcb-160">Par exemple, le message peut être défini dans le fichier de code C généré à partir du fichier WSDL, mais l’élément message peut être défini ailleurs dans le fichier de code C généré à partir du fichier XSD.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-160">For example, the message may be defined in the C code file generated from the WSDL file but the message element may be defined elsewhere in the C code file generated from the XSD file.</span></span> <span data-ttu-id="b9bcb-161">Dans ce cas, Wsutil.exe génère une référence à l’élément global à partir du fichier qui contient la définition de message, comme illustré ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-161">In this case, Wsutil.exe generates reference to the global element from the file that contains the message definition, as demonstrated below:</span></span>

``` syntax
{  // WS_MESSAGE_DESCRIPTION
...
(WS_ELEMENT_DESRIPTION *)b_xsd.globalElement.<elementname>
  };
```

## <a name="global-element-descriptions"></a><span data-ttu-id="b9bcb-162">Descriptions des éléments globaux</span><span class="sxs-lookup"><span data-stu-id="b9bcb-162">Global element descriptions</span></span>

<span data-ttu-id="b9bcb-163">Pour chaque élément global défini dans un wsdl : type ou un fichier XSD, il existe un champ correspondant nommé **ElementName** dans le champ **GlobalElement** .</span><span class="sxs-lookup"><span data-stu-id="b9bcb-163">For each global element defined in a wsdl:type or XSD file, there is a matching field named **elementName** inside the **GlobalElement** field.</span></span> <span data-ttu-id="b9bcb-164">Dans cet exemple, une structure nommée SimpleMethod est générée :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-164">In this example, a structure named SimpleMethod is generated:</span></span>

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

<span data-ttu-id="b9bcb-165">Les autres descriptions requises par la description de l’élément sont générées dans le cadre de la structure conteneur.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-165">Other descriptions required by the element description are generated as part of the containing structure.</span></span> <span data-ttu-id="b9bcb-166">Si l’élément est un élément de type simple, il n’y a qu’un seul champ de [**\_ \_ Description d’élément WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) .</span><span class="sxs-lookup"><span data-stu-id="b9bcb-166">If the element is a simple type element, there is only one [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) field.</span></span> <span data-ttu-id="b9bcb-167">Si le type d’élément est une structure, tous les champs et descriptions de structure associés sont générés dans le cadre de la structure de l’élément.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-167">If the element type is a structure, all of the related fields and structure descriptions are generated as part of the element structure.</span></span> <span data-ttu-id="b9bcb-168">Dans cet exemple, l’élément SimpleMethod est une structure contenant deux champs, **a** et **b**.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-168">In this example, SimpleMethod element is a structure containing two fields, **a** and **b**.</span></span> <span data-ttu-id="b9bcb-169">Wsutil.exe génère la structure comme suit :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-169">Wsutil.exe generates the structure as follows:</span></span>

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

<span data-ttu-id="b9bcb-170">Les structures incorporées et les éléments incorporés sont générés sous la forme de sous-structures en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-170">Embedded structures and embedded elements are generated as sub-structures as needed.</span></span>

## <a name="wsdl-related-definitions"></a><span data-ttu-id="b9bcb-171">Définitions associées à WSDL</span><span class="sxs-lookup"><span data-stu-id="b9bcb-171">WSDL related definitions</span></span>

<span data-ttu-id="b9bcb-172">Wsutil.exe génère un champ sous la section WSDL pour chaque valeur **portType** définie sous le service WSDL : service spécifié.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-172">Wsutil.exe generates a field under WSDL section for each of the **portType** values defined under the specified wsdl:service.</span></span>

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

<span data-ttu-id="b9bcb-173">Wsutil.exe génère un champ f qui contient toutes les descriptions nécessaires pour l’opération, un tableau authentification unique de pointeurs vers chacune des descriptions d’opérations pour chaque méthode, et une [**\_ \_ Description de contrat WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) pour le **portType** spécifié.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-173">Wsutil.exe generates one field f that contains all the descriptions needed for the operation, a signle array of pointers to each of the operation descriptions for each method, and one [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) for the specified **portType**.</span></span>

<span data-ttu-id="b9bcb-174">Toutes les descriptions requises par les opérations sont générées dans le champ **NomOpération** sous le **portType** spécifié.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-174">All the descriptions needed by operations are generated inside the **operationName** field under the specified **portType**.</span></span> <span data-ttu-id="b9bcb-175">Celles-ci incluent le champ de [**\_ \_ Description de l’élément WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) ainsi que la sous-structure des paramètres d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-175">These include the [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) field as well as the sub-structure for input and output parameter s.</span></span> <span data-ttu-id="b9bcb-176">De même, les champs de [**\_ \_ Description du message WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) pour le message d’entrée et le message de sortie facultatif sont inclus avec le ; [**WS \_ Champ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) de liste de description de paramètre pour tous les paramètres d’opération et le champ de [**\_ \_ Description d’opération WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) pour l’opération elle-même.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-176">Likewise, the [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) fields for the input message and the optional output message are included along with the; [**WS\_PARAMETER\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) list field for all of the operation parameters and the [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) field for the operation itself.</span></span> <span data-ttu-id="b9bcb-177">Dans cet exemple, la structure de code de la description SimpleMethod est générée comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-177">In this example, the code structure for the SimpleMethod description is generated as seen below:</span></span>

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

## <a name="xml-dictionary-related-definitions"></a><span data-ttu-id="b9bcb-178">Définitions associées au dictionnaire XML</span><span class="sxs-lookup"><span data-stu-id="b9bcb-178">XML dictionary related definitions</span></span>

<span data-ttu-id="b9bcb-179">Les noms et les espaces de noms utilisés dans différentes descriptions sont générés sous la forme de champs de type [**WS \_ XML \_ String**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string).</span><span class="sxs-lookup"><span data-stu-id="b9bcb-179">Names and namespaces used in various descriptions are generated as fields of type [**WS\_XML\_STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string).</span></span> <span data-ttu-id="b9bcb-180">Toutes ces chaînes sont générées dans le cadre d’un dictionnaire de constantes par fichier.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-180">All of these strings are generated as part a per-file constant dictionary.</span></span> <span data-ttu-id="b9bcb-181">La liste de chaînes et le champ de [**\_ \_ dictionnaire XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary) (nommé **dict** dans l’exemple ci-dessous) sont générés dans le cadre du champ dictionary de la structure **fileNameLocal** .</span><span class="sxs-lookup"><span data-stu-id="b9bcb-181">The list of strings and the [**WS\_XML\_DICTIONARY**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary) field (named **dict** in the example below) are generated as part of the dictionary field of the **fileNameLocal** structure.</span></span>

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

<span data-ttu-id="b9bcb-182">Le tableau de [**la \_ \_ chaîne WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)s est généré sous la forme d’une série de champs de type **WS \_ XML \_ String**, nommés avec avec des noms conviviaux.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-182">The array of [**WS\_XML\_STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)s are generated as a series of fields of type **WS\_XML\_STRING**, named with with user-friendly names.</span></span> <span data-ttu-id="b9bcb-183">Le stub généré utilise les noms conviviaux dans différentes descriptions pour une meilleure lisibilité.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-183">The generated stub uses the user-friendly names in various descriptions for better readability.</span></span>

<span data-ttu-id="b9bcb-184">Proxy client pour les opérations WSDL</span><span class="sxs-lookup"><span data-stu-id="b9bcb-184">Client proxy for WSDL operations</span></span>

<span data-ttu-id="b9bcb-185">Wsutil.exe génère un proxy client pour toutes les opérations.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-185">Wsutil.exe generates a client proxy for all of the operations.</span></span> <span data-ttu-id="b9bcb-186">Les applications peuvent remplacer la signature de la méthode à l’aide d’une option de ligne de commande de préfixe.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-186">Applications can overwrite the method signature using a prefix command-line option.</span></span>

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

<span data-ttu-id="b9bcb-187">L’appelant de l’opération doit passer un paramètre de *segment de mémoire* valide.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-187">The operation caller must pass in a valid *heap* parameter.</span></span> <span data-ttu-id="b9bcb-188">Les paramètres de sortie sont alloués à l’aide de la \_ valeur du tas WS spécifiée dans le paramètre *Heap* .</span><span class="sxs-lookup"><span data-stu-id="b9bcb-188">Output parameters are allocated using the WS\_HEAP value specified in the *heap* parameter.</span></span> <span data-ttu-id="b9bcb-189">La fonction appelante peut réinitialiser ou libérer le tas pour libérer de la mémoire pour tous les paramètres de sortie.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-189">The calling function can reset or free the heap to release memory for all of the output parameters.</span></span> <span data-ttu-id="b9bcb-190">En cas d’échec de l’opération, des informations supplémentaires sur l’erreur peuvent être récupérées à partir de l’objet facultatif Error s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-190">If the operation fails, additional detail error information can be retrieved from the optional error object if it is available.</span></span>

<span data-ttu-id="b9bcb-191">Wsutil.exe génère un stub de service pour toutes les opérations décrites dans liaison.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-191">Wsutil.exe generates a service stub for all of the operations described in binding.</span></span>

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

<span data-ttu-id="b9bcb-192">La section ci-dessus décrit le prototype de la structure locale contenant toutes les définitions locales du fichier stub uniquement.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-192">The above section describes the prototype of the local structure containing all of the definitions local to the stub file only.</span></span> <span data-ttu-id="b9bcb-193">Les sections suivantes décrivent les définitions des descriptions.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-193">Subsequent sections describe the definitions of the descriptions.</span></span>

## <a name="wsdl-definition-generation"></a><span data-ttu-id="b9bcb-194">Génération de définition WSDL</span><span class="sxs-lookup"><span data-stu-id="b9bcb-194">WSDL Definition Generation</span></span>

<span data-ttu-id="b9bcb-195">Wsutil.exe génère une structure statique constante (**const static**) nommée *<\_ nom de fichier>* LocalDefinitions de type *<\_ nom de service>* local qui contient toutes les définitions locales uniquement.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-195">Wsutil.exe generates a constant static (**const static**) structure named *<file\_name>* LocalDefinitions of type *<service\_name>* Local that contains all the local only definitions.</span></span>

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

<span data-ttu-id="b9bcb-196">Les descriptions WSDL suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-196">The following WSDL descriptions are supported:</span></span>

-   <span data-ttu-id="b9bcb-197">wsdl : service</span><span class="sxs-lookup"><span data-stu-id="b9bcb-197">wsdl:service</span></span>
-   <span data-ttu-id="b9bcb-198">wsdl : Binding</span><span class="sxs-lookup"><span data-stu-id="b9bcb-198">wsdl:binding</span></span>
-   <span data-ttu-id="b9bcb-199">wsdl : portType</span><span class="sxs-lookup"><span data-stu-id="b9bcb-199">wsdl:portType</span></span>
-   <span data-ttu-id="b9bcb-200">wsdl : opération</span><span class="sxs-lookup"><span data-stu-id="b9bcb-200">wsdl:operation</span></span>
-   <span data-ttu-id="b9bcb-201">wsdl : message</span><span class="sxs-lookup"><span data-stu-id="b9bcb-201">wsdl:message</span></span>

## <a name="processing-wsdloperation-and-wsdlmessage"></a><span data-ttu-id="b9bcb-202">Traitement de wsdl : Operation et WSDL : message</span><span class="sxs-lookup"><span data-stu-id="b9bcb-202">Processing wsdl:operation and wsdl:message</span></span>

<span data-ttu-id="b9bcb-203">Chaque opération spécifiée dans le document WSDL est mappée à une opération de service par [Wsutil.exe](web-service-compiler-tool.md).</span><span class="sxs-lookup"><span data-stu-id="b9bcb-203">Each operation specified in the WSDL document is mapped to a service operation by [Wsutil.exe](web-service-compiler-tool.md).</span></span> <span data-ttu-id="b9bcb-204">L’outil génère des définitions distinctes des opérations de service pour le serveur et le client.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-204">The tool generates separate definitions of the service operations for both the server and the client.</span></span>

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

<span data-ttu-id="b9bcb-205">La disposition des éléments de données de message andOutput d’entrée est évaluée par l’outil pour générer les métadonnées de sérialisation pour l’infrastructure avec la signature réelle de l’opération de service obtenue à laquelle les messages d’entrée et de sortie sont associés.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-205">The layout of the input andoutput message data elements is evaluated by the tool to generate the serialization metadata for the infrastructure along with the actual signature of the resulting service operation to which the input and output messages are associated.</span></span>

<span data-ttu-id="b9bcb-206">Les métadonnées pour chaque opération d’un **portType** spécifique ont une entrée et éventuellement un message de sortie, chacun de ces messages est mappé à [**une \_ \_ Description de message WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description).</span><span class="sxs-lookup"><span data-stu-id="b9bcb-206">The metadata for each operation within a specific **portType** has input and optionally an output message, each of these messages is mapped to a [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description).</span></span> <span data-ttu-id="b9bcb-207">Dans cet exemple, l’entrée et le message de sortie sur l’opération dans portType sont mappés à inputMessageDescription et éventuellement outputMessageDescription sur la description de l' [**\_ \_ opération WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-207">In this example, the input and the output message on the operation in the portType mapped to inputMessageDescription and optionally the outputMessageDescription on the [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) respectively.</span></span>

<span data-ttu-id="b9bcb-208">Pour chaque message WSDL, l’outil génère la [**\_ \_ Description du message WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) qui fait référence à la définition de la description de l' [**\_ élément \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) , comme illustré ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-208">For each WSDL message the tool generates [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) that references the [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) definition, as demonstrated below:</span></span>

``` syntax
... 
{    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

<span data-ttu-id="b9bcb-209">La description du message fait référence à la description de l’élément d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-209">The message description refers to the input element description.</span></span> <span data-ttu-id="b9bcb-210">Étant donné que l’élément est défini globalement, la description du message référence la définition globale au lieu de l’élément statique local.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-210">Because the element is globally defined, the message description references the global definition instead of the local static element.</span></span> <span data-ttu-id="b9bcb-211">De même, si l’élément est défini dans un autre fichier, Wsutil.exe génère une référence à la structure globalement définie dans ce fichier.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-211">Similarly, if the element is defined in another file, Wsutil.exe generates a reference to the globally-defined structure in that file.</span></span> <span data-ttu-id="b9bcb-212">Par exemple, si SimpleMethodResponse est défini dans un autre fichier example. xsd, Wsutil.exe génère le code suivant à la place :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-212">For example, if SimpleMethodResponse is defined in another example.xsd file, Wsutil.exe generates the following instead:</span></span>

``` syntax
...
{    // message description for ISimpleService_SimpleMethod_InputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_xsd.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

<span data-ttu-id="b9bcb-213">Chaque description de message contient l’action et la description de l’élément spécifique (un champ de type [**WS \_ Element \_ Description**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)) pour tous les éléments de données de message.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-213">Each message description contains the action and the specific element description (a field of type [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)) for all the message data elements.</span></span> <span data-ttu-id="b9bcb-214">Dans le cas d’un message de style RPC ou d’un message avec plusieurs parties, un élément wrapper est créé pour encapsuler les informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-214">In the case of an RPC-style message or a message with multiple parts, a wrapper element is created to encapsulate the additional information.</span></span>

## <a name="rpc-style-support"></a><span data-ttu-id="b9bcb-215">Prise en charge du style RPC</span><span class="sxs-lookup"><span data-stu-id="b9bcb-215">RPC style support</span></span>

<span data-ttu-id="b9bcb-216">Wsutil.exe prend en charge les opérations de style document et de style RPC selon l’extension de liaison WSDL 1,1 pour la spécification SOAP 1,2.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-216">Wsutil.exe supports document-style as well as RPC-style operations according to the WSDL 1.1 Binding Extension for SOAP 1.2 specification.</span></span> <span data-ttu-id="b9bcb-217">Les opérations RPC et de style littéral sont marquées en tant qu' \_ opération de LITTÉRAL WS RPC \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b9bcb-217">RPC- and literal-style operations are marked as WS\_RPC\_LITERAL\_OPERATION.</span></span> <span data-ttu-id="b9bcb-218">Le modèle de service ignore le nom de l’élément wrapper du corps de la réponse dans les opérations RPC/littérales.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-218">The service model ignores the name for the response body wrapper element in RPC/literal operations.</span></span>

<span data-ttu-id="b9bcb-219">Wsutil.exe ne prend pas en charge en mode natif les opérations de style encodage.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-219">Wsutil.exe does not natively support encoding-style operations.</span></span> <span data-ttu-id="b9bcb-220">Le \_ \_ paramètre de mémoire tampon XML WS est généré pour l’encodage des messages, et les développeurs doivent remplir directement la mémoire tampon opaque.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-220">The WS\_XML\_BUFFER parameter is generated for encoding messages, and developers must populate the opaque buffer directly.</span></span>

## <a name="multiple-message-parts-support"></a><span data-ttu-id="b9bcb-221">Prise en charge de plusieurs parties de messages</span><span class="sxs-lookup"><span data-stu-id="b9bcb-221">Multiple message parts support</span></span>

<span data-ttu-id="b9bcb-222">Wsutil.exe prend en charge plusieurs parties de message dans un message.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-222">Wsutil.exe supports multiple message parts in one message.</span></span> <span data-ttu-id="b9bcb-223">Un message à parties multiples peut être spécifié comme suit :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-223">A multi-part message can be specified as follows:</span></span>

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

<span data-ttu-id="b9bcb-224">Wsutil.exe génère un champ de [**\_ \_ type du struct WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type) pour l’élément message si le message contient plusieurs parties.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-224">Wsutil.exe generates a [**WS\_STRUCT\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type) field for the message element if the message contains multiple parts.</span></span> <span data-ttu-id="b9bcb-225">Si le message est représenté à l’aide du style de document, Wsutil.exe génère un élément wrapper avec le type struct.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-225">If the message is represented using the document style, Wsutil.exe generates a wrapper element with struct type.</span></span> <span data-ttu-id="b9bcb-226">L’élément wrapper n’a pas de nom ou d’espace de noms spécifique, et la structure Wrapper contient tous les éléments de toutes les parties en tant que champs.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-226">The wrapper element does not have a name or a specific namespace, and the wrapper structure contains all of the elements in all of the parts as fields.</span></span> <span data-ttu-id="b9bcb-227">L’élément wrapper est destiné à un usage interne uniquement et n’est pas sérialisé dans le corps du message.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-227">The wrapper element is for internal use only and it will not be serialized in the message body.</span></span>

<span data-ttu-id="b9bcb-228">Si le message utilise une représentation de type littéral ou RPC, Wsutil.exe crée un élément wrapper avec le nom de l’opération comme nom d’élément et l’espace de noms spécifié en tant qu’espace de noms de service en fonction de la spécification de l’extension SOAP WSDL.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-228">If the message is using RPC or literal style representation , Wsutil.exe creates a wrapper element with the operation name as the element name and the specified namespace as service namespace according to WSDL SOAP extension specification.</span></span> <span data-ttu-id="b9bcb-229">La structure de l’élément contient un tableau de champs représentant les types spécifiés dans les parties de message.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-229">The structure of the element contains an array of fields representing the types specified in the message parts.</span></span> <span data-ttu-id="b9bcb-230">L’élément wrapper est mappé à l’élément supérieur réel dans le corps du message, comme indiqué dans la spécification SOAP.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-230">The wrapper element is mapped to the actual top element in message body as indicated in the SOAP specification.</span></span>

<span data-ttu-id="b9bcb-231">Côté serveur, chaque opération génère un typedef de l’opération de service serveur résultante.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-231">On the server side, each operation results in a typedef of the resulting server service operation.</span></span> <span data-ttu-id="b9bcb-232">Ce typedef est utilisé pour faire référence à l’opération dans la table de fonctions comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-232">This typedef is used to refer to the operation in the function table as described previously.</span></span> <span data-ttu-id="b9bcb-233">Chaque opération entraîne également la génération d’une fonction stub qui nfrastructure a appelle pour le compte du délégué à la méthode réelle.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-233">Every operation also results in the generation of a stub function which nfrastructure calls on behalf of the delegate to the actual method.</span></span>

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

<span data-ttu-id="b9bcb-234">Pour l’opération SimpleMethod, le typedef SimpleMethodOperation est défini ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-234">For the SimpleMethod operation, the SimpleMethodOperation typedef is defined above.</span></span> <span data-ttu-id="b9bcb-235">Notez que la méthode générée a un argument développé listwith la partie de message pour le message d’entrée et de sortie pour l’opération SimpleMethod en tant que paramètres nommés.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-235">Note that the generated method has an expanded argument listwith the message part for the input and output message for SimpleMethod operation as named parameters.</span></span>

<span data-ttu-id="b9bcb-236">Côté client, chaque opération est mappée à une opération de service proxy.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-236">On the client side each operation is mapped to a proxy service operation.</span></span>

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

## <a name="processing-wsdlbinding"></a><span data-ttu-id="b9bcb-237">Traitement de wsdl : Binding</span><span class="sxs-lookup"><span data-stu-id="b9bcb-237">Processing wsdl:binding</span></span>

<span data-ttu-id="b9bcb-238">Le modèle de service WWSAPI prend en charge l’extension de liaison theSOAP.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-238">The WWSAPI service model supports theSOAP binding extension.</span></span> <span data-ttu-id="b9bcb-239">Pour chaque liaison, il existe un **portType** associé.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-239">For each binding there is an associated **portType**.</span></span>

<span data-ttu-id="b9bcb-240">Le transport spécifié dans l’extension de liaison SOAP est un avis uniquement.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-240">The transport specified in soap binding extension is advisory only.</span></span> <span data-ttu-id="b9bcb-241">L’application doit fournir des informations de transport lors de la création d’un canal.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-241">Application needs to provide transport information when creating a channel.</span></span> <span data-ttu-id="b9bcb-242">Actuellement, nous prenons en charge la \_ liaison WS http \_ et les \_ liaisons de liaison WS TCP \_ .</span><span class="sxs-lookup"><span data-stu-id="b9bcb-242">Currently we support the WS\_HTTP\_BINDING and WS\_TCP\_BINDING bindings.</span></span>

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

<span data-ttu-id="b9bcb-243">Dans notre exemple de document WSDL, nous disposons d’un seul **portType** pour ISimpleService.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-243">In our example WSDL document we only have one **portType** for ISimpleService.</span></span> <span data-ttu-id="b9bcb-244">La liaison SOAP fournie indique le transport HTTP, qui est spécifié en tant \_ que \_ liaison WS http.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-244">The provided SOAP binding indicates the HTTP transport, which is specified as WS\_HTTP\_BINDING.</span></span> <span data-ttu-id="b9bcb-245">Notez que cette structure n’a pas de décoration statique, car cette structure doit être disponible pour l’application.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-245">Notice that this structure does not have static decoration as this structure needs to be available to the application.</span></span>

<span data-ttu-id="b9bcb-246">Traitement de wsdl : portType</span><span class="sxs-lookup"><span data-stu-id="b9bcb-246">Processing wsdl:portType</span></span>

<span data-ttu-id="b9bcb-247">Chaque **portType** dans WSDL est constitué d’une ou plusieurs opérations.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-247">Each **portType** in WSDL is made up of one or more operations.</span></span> <span data-ttu-id="b9bcb-248">L’opération doit être cohérente avec l’extension de liaison SOAP indiquée dans WSDL : Binding.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-248">The operation should be consistent with the SOAP binding extension indicated in wsdl:binding.</span></span>

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

<span data-ttu-id="b9bcb-249">Dans cet exemple, ISimpleService **portType** contient uniquement l’opération SimpleMethod.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-249">In this example, the ISimpleService **portType** only contains the SimpleMethod operation.</span></span> <span data-ttu-id="b9bcb-250">Cela est cohérent avec la section de liaison dans laquelle il n’existe qu’une seule opération WSDL qui est mappée à une action SOAP.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-250">This is consistent with the binding section where there is only one WSDL operation that maps to a SOAP action.</span></span>

<span data-ttu-id="b9bcb-251">Étant donné que ISimpleService **portType** n’a qu’une seule opération--SimpleMethod--la table de fonctions correspondante contient uniquement des SimpleMethod en tant qu’opération de service.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-251">Since the ISimpleService **portType** only has one operation -- SimpleMethod -- the corresponding function table only contains SimpleMethod as a service operation.</span></span>

<span data-ttu-id="b9bcb-252">En termes de métadonnées, chaque **portType** est mappé par Wsutil.exe à [**une \_ \_ Description de contrat WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description).</span><span class="sxs-lookup"><span data-stu-id="b9bcb-252">In terms of metadata each **portType** is mapped by Wsutil.exe to a [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description).</span></span> <span data-ttu-id="b9bcb-253">Chaque opération au sein d’un **portType** est mappée à une [**\_ \_ Description d’opération WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).</span><span class="sxs-lookup"><span data-stu-id="b9bcb-253">Each operation within a **portType** is mapped to a [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).</span></span>

<span data-ttu-id="b9bcb-254">Dans cet exemple, **portType** , l’outil génère la [**\_ \_ Description WS Contract**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) pour ISimpleService.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-254">In this example, **portType** the tool generates [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) for ISimpleService.</span></span> <span data-ttu-id="b9bcb-255">Cette description de contrat contient le nombre spécifique d’opérations disponibles sur ISimpleService **portType** , ainsi qu’un tableau [**de \_ \_ Description d’opération WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) représentant les opérations individuelles définies sur PortType pour ISimpleService.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-255">This contract description contains the specific number of operations available on the ISimpleService **portType** along with an array of [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) representing the individual operations defined on the portType for ISimpleService.</span></span> <span data-ttu-id="b9bcb-256">Étant donné qu’il n’existe qu’une seule opération sur ISimpleService portType pour ISimpleService, il n’y a également qu’une seule définition de **\_ \_ Description d’opération WS** .</span><span class="sxs-lookup"><span data-stu-id="b9bcb-256">Since there is only one operation on ISimpleService portType for ISimpleService, there is also only one **WS\_OPERATION\_DESCRIPTION** definition.</span></span>

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

## <a name="processing-wsdlservice"></a><span data-ttu-id="b9bcb-257">Traitement de wsdl : service</span><span class="sxs-lookup"><span data-stu-id="b9bcb-257">Processing wsdl:service</span></span>

<span data-ttu-id="b9bcb-258">WsUtil.exe utilise les services pour rechercher Binding/types et génère une structure de contrat qui décrit les types, les messages, les définitions PortType, etc.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-258">WsUtil.exe uses the services to find binding/porttypes, and generates contract structure that describes types, message, porttype definitions, and so on.</span></span> <span data-ttu-id="b9bcb-259">Les descriptions de contrat sont accessibles en externe et sont générées dans le cadre de la structure de définition globale spécifiée par le biais de l’en-tête généré.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-259">Contract descriptions are externally accessible, and they are generated as part of the global definition structure specified through generated header.</span></span>

<span data-ttu-id="b9bcb-260">WsUtil.exe prend en charge les extensions EndpointReference définies dans WSDL : port.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-260">WsUtil.exe supports EndpointReference extensions defined in wsdl:port.</span></span> <span data-ttu-id="b9bcb-261">La référence de point de terminaison est définie dans WS-Addressing comme un moyen de décrire les informations de [point de terminaison](endpoint-address.md) d’un service.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-261">Endpoint reference is defined in WS-ADDRESSING as a way to describe [endpoint](endpoint-address.md) information of a service.</span></span> <span data-ttu-id="b9bcb-262">Le texte d’extension de référence de point de terminaison d’entrée enregistré sous forme de [**\_ \_ chaîne WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string), ainsi que la description de l' [**adresse de point de \_ terminaison \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) correspondante sont générés dans la section endpointReferences de la structure globale.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-262">The input endpoint reference extension text saved as [**WS\_XML\_STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string), together with matching [**WS\_ENDPOINT\_ADDRESS\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) are generated in endpointReferences section in the global structure.</span></span>

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

<span data-ttu-id="b9bcb-263">Pour créer [**une \_ \_ adresse de point de terminaison WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) à l’aide des métadonnées générées par WsUtil :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-263">To Create [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) using the WsUtil generated metadata:</span></span>

``` syntax
WsCreateReader      // Create a WS_XML_READER
Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput          // Set the encoding and input of the reader to generated endpointReferenceString
WsReadType        // Read WS_ENDPOINT_ADDRESS from the reader
    // Using WS_ELEMENT_TYPE_MAPPING, WS_ENDPOINT_ADDRESS_TYPE and generated endpointAddressDescription, 
```

<span data-ttu-id="b9bcb-264">Les chaînes constantes du proxy client ou du stub de service sont générées en tant que champs de type WS \_ XML \_ String et il existe un dictionnaire constant pour toutes les chaînes du fichier proxy ou stub.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-264">Constant strings in the client proxy or service stub are generated as fields of type WS\_XML\_STRING, and there is a constant dictionary for all the strings in the proxy or stub file.</span></span> <span data-ttu-id="b9bcb-265">Chaque chaîne du dictionnaire est générée sous la forme d’un champ dans la partie dictionnaire de la structure locale pour une meilleure lisibilité.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-265">Each string in the dictionary is generated as a field in the dictionary part of the local structure for better readability.</span></span>

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

## <a name="processing-wsdltype"></a><span data-ttu-id="b9bcb-266">Traitement de wsdl : type</span><span class="sxs-lookup"><span data-stu-id="b9bcb-266">Processing wsdl:type</span></span>

<span data-ttu-id="b9bcb-267">Wsutil.exe prend en charge uniquement les documents de schéma XML (XSD) dans la spécification WSDL : type.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-267">Wsutil.exe only supports XML schema (XSD) documents in wsdl:type specification.</span></span> <span data-ttu-id="b9bcb-268">Un cas particulier est lorsqu’un port de message spécifie une définition d’élément global.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-268">One special case is when a message port specifies a global element definition.</span></span> <span data-ttu-id="b9bcb-269">Pour plus d’informations sur l’heuristique utilisée dans ces cas, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-269">See the following section for more details of the heuristics used in these cases.</span></span>

## <a name="parameter-processing-heuristics"></a><span data-ttu-id="b9bcb-270">Heuristiques de traitement de paramètres</span><span class="sxs-lookup"><span data-stu-id="b9bcb-270">Parameter Processing Heuristics</span></span>

<span data-ttu-id="b9bcb-271">Dans le modèle de service, les messages WSDL sont mappés à des paramètres spécifiques dans une méthode.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-271">In the service model, WSDL messages are mapped to specific parameters in a method.</span></span> <span data-ttu-id="b9bcb-272">Wsutil.exe a deux styles de génération de paramètres : dans le premier style, l’opération a un paramètre pour le message d’entrée et un paramètre pour le message de sortie (si nécessaire); dans le deuxième style, Wsutil.exe utilise une méthode heuristique pour mapper et développer des champs dans les structures pour les messages d’entrée et les messages de sortie vers des paramètres différents dans l’opération.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-272">Wsutil.exe has two styles of parameter generation: in first style, the operation has one parameter for input message, and one parameter for output message (if necessary); in the second style, Wsutil.exe uses a heuristic to map and expand fields in the structures for both input messages and output messages to different parameters in the operation.</span></span> <span data-ttu-id="b9bcb-273">Les messages d’entrée et de sortie doivent avoir des éléments de message de type structure pour générer cette deuxième approche.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-273">Both input and output messages need to have structure type message elements to generate this second approach.</span></span>

<span data-ttu-id="b9bcb-274">Wsutil.exe utilise les règles suivantes lors de la génération de paramètres d’opération à partir des messages d’entrée et de sortie :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-274">Wsutil.exe uses the following rules when generating operation parameters from the input and output messages:</span></span>

-   <span data-ttu-id="b9bcb-275">Pour les messages d’entrée et de sortie avec plusieurs parties de message, chaque partie de message est un paramètre distinct dans l’opération, avec le nom de la partie de message comme nom de paramètre.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-275">For input and output messages with multiple message parts, each message part is a separate parameter in the operation, with the message part name as parameter name.</span></span>
-   <span data-ttu-id="b9bcb-276">Pour un message de style RPC avec une partie de message, la partie de message est un paramètre dans l’opération, avec le nom de la partie de message comme nom de paramètre.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-276">For RPC style message with one message part, the message part is a parameter in the operation, with message part name as parameter name.</span></span>
-   <span data-ttu-id="b9bcb-277">Pour les messages d’entrée et de sortie de style document avec une partie de message :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-277">For document-style input and output messages with one message part:</span></span>
    -   <span data-ttu-id="b9bcb-278">Si le nom d’une partie de message est « Parameters » et que le type d’élément est une structure, chaque champ de la structure est traité comme un paramètre distinct avec le nom de champ comme nom de paramètre.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-278">If the name of a message part is "parameters" and the element type is a structure, each field in the structure is treated as a separate parameter with the field name being the parameter name.</span></span>
    -   <span data-ttu-id="b9bcb-279">Si le nom de la partie de message n’est pas « Parameters », le message est un paramètre dans l’opération avec le nom de message utilisé comme nom de paramètre correspondant.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-279">If the message part name is not "parameters", the message is a parameter in the operation with the message name used as the corresponding parameter name.</span></span>
-   <span data-ttu-id="b9bcb-280">Pour le message d’entrée et de sortie de style de document avec l’élément nillable, le message est mappé à un paramètre, avec le nom de la partie de message comme nom de paramètre.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-280">For document style input and output message with nillable element, the message is mapped to one parameter, with message part name as parameter name.</span></span> <span data-ttu-id="b9bcb-281">Un niveau supplémentaire d’indirection est ajouté pour indiquer que le pointeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-281">One additional level of indirection is added to indicate the pointer can be **NULL**.</span></span>
-   <span data-ttu-id="b9bcb-282">Si un champ apparaît uniquement dans l’élément de message d’entrée, le champ est traité comme un \[ \] paramètre in.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-282">If a field appears in the input message element only, the field is treated as an \[in\] parameter.</span></span>
-   <span data-ttu-id="b9bcb-283">Si un champ s’affiche uniquement dans l’élément de message de sortie, le champ est traité comme un \[ paramètre de sortie \] .</span><span class="sxs-lookup"><span data-stu-id="b9bcb-283">If a field appears in the output message element only, the field is treated as an \[out\] parameter.</span></span>
-   <span data-ttu-id="b9bcb-284">S’il existe un champ avec le même nom et le même type qui apparaît dans le message d’entrée et le message de sortie, le champ est traité comme un \[ paramètre in, out \] .</span><span class="sxs-lookup"><span data-stu-id="b9bcb-284">If there is a field with the same name and same type that appears in both the input message and the output message, the field is treated as an \[in,out\] parameter.</span></span>

<span data-ttu-id="b9bcb-285">Les outils suivants sont utilisés pour déterminer la direction des paramètres :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-285">Following tools are used to determine the direction of parameters:</span></span>

-   <span data-ttu-id="b9bcb-286">Si un champ n’apparaît que dans un élément de message d’entrée, le champ est traité comme dans seul paramètre.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-286">If a field appears in input message element only, the field is treated as in only parameter.</span></span>
-   <span data-ttu-id="b9bcb-287">Si un champ n’apparaît que dans un élément de message de sortie, le champ est traité comme paramètre de sortie uniquement.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-287">If a field appears in output message element only, the field is treated as out only parameter.</span></span>
-   <span data-ttu-id="b9bcb-288">S’il existe un champ avec le même nom et le même type qui apparaît à la fois dans le message d’entrée et le message de sortie, le champ est traité comme un paramètre in, out.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-288">If there is a field with the same name and same type that appears in both input message and output message, the field is treated as an in,out parameter.</span></span>

<span data-ttu-id="b9bcb-289">Wsutil.exe prend en charge uniquement les éléments séquencés.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-289">Wsutil.exe only supports sequenced elements.</span></span> <span data-ttu-id="b9bcb-290">Il rejette l’ordonnancement non valide en ce qui concerne \[ dans, les paramètres de sortie \] si Wsutil.exe ne pouvez pas combiner les paramètres in et out dans une liste de paramètres unique.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-290">It rejects invalid ordering with regard to \[in,out\] parameters if Wsutil.exe cannot combine the in parameters and out parameters into a single parameter list.</span></span> <span data-ttu-id="b9bcb-291">Des suffixes peuvent être ajoutés aux noms de paramètres pour éviter la collision de noms.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-291">Suffixes might be added to parameter names to avoid name collision.</span></span>

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

<span data-ttu-id="b9bcb-292">Wsutil.exe considère les champs de TNS : SimpleMethod et TNS : SimpleMethodResponse ATO comme paramètres, comme indiqué dans les définitions de paramètres ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-292">Wsutil.exe considers fields in tns:SimpleMethod and tns:SimpleMethodResponse ato be parameters, as seen in the parameter definitions below:</span></span>

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

<span data-ttu-id="b9bcb-293">Wsutil.exe développe la liste de paramètres à partir des champs de la liste ci-dessus et génère la structure **ParamStruct** dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-293">Wsutil.exe expands the parameter list from the fields in the list above, and generates the **ParamStruct** structure in the following code example.</span></span> <span data-ttu-id="b9bcb-294">Le temps d’exécution du modèle de service peut utiliser cette structure pour passer des arguments aux stubs du client et du serveur.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-294">The service model run-time can use this structure to pass arguments to the client and server stubs.</span></span>

``` syntax
typedef struct SimpleMethodParamStruct {
  unsigned int   a;  
  unsigned int   b;
  unsigned int   c;
} ;
```

<span data-ttu-id="b9bcb-295">Cette structure est utilisée uniquement pour décrire le frame de pile côté client et côté serveur.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-295">This structure is only used to describe the stack frame on the client and server side.</span></span> <span data-ttu-id="b9bcb-296">Aucune modification n’est apportée à la description du message ou aux descriptions d’éléments référencées par la description du message.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-296">There is no change to the message description, or to the element descriptions referenced by the message description.</span></span>

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

<span data-ttu-id="b9bcb-297">En règle générale, un niveau d’indirection est ajouté pour tous les paramètres out \[ \] et \[ in, out \] .</span><span class="sxs-lookup"><span data-stu-id="b9bcb-297">As a general rule, one level of indirection is added for all the \[out\] and \[in,out\] parameters.</span></span>

## <a name="parameterless-operation"></a><span data-ttu-id="b9bcb-298">Opération sans paramètre</span><span class="sxs-lookup"><span data-stu-id="b9bcb-298">Parameterless operation</span></span>

<span data-ttu-id="b9bcb-299">Pour les opérations de document et de littéral, Wsutil.exe traite l’opération comme ayant un paramètre d’entrée et un paramètre de sortie si :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-299">For document and literal operations, Wsutil.exe treats the operation as having one input parameter and one output parameter if:</span></span>

-   <span data-ttu-id="b9bcb-300">Le message d’entrée ou de sortie a plusieurs parties.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-300">The input or output message has more than one part.</span></span>
-   <span data-ttu-id="b9bcb-301">Il n’existe qu’une seule partie de message et le nom de la partie de message n’est pas « Parameters ».</span><span class="sxs-lookup"><span data-stu-id="b9bcb-301">There is only one message part and the message part name is not "parameters".</span></span>

<span data-ttu-id="b9bcb-302">..</span><span class="sxs-lookup"><span data-stu-id="b9bcb-302">..</span></span> <span data-ttu-id="b9bcb-303">Dans l’exemple ci-dessus, en supposant que les parties de message sont nommées *param* et *ParamOut*, la signature de la méthode devient le code suivant :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-303">In the example above, assuming the message parts are named *ParamIn*" and *ParamOut*, the method signature becomes the following code:</span></span>

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

<span data-ttu-id="b9bcb-304">Wsutil.exe génère une signature de version pour la description de l’opération, de sorte que le moteur de modèle de service WsCall et côté serveur peut vérifier si la description générée est applicable à la plateforme actuelle.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-304">Wsutil.exe generates a version signature for the operation description such that the WsCall and server-side service model engine can check if the generated description is applicable for the current platform.</span></span>

<span data-ttu-id="b9bcb-305">Ces informations de version sont générées dans le cadre de la structure de la [**\_ \_ Description de l’opération WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) .</span><span class="sxs-lookup"><span data-stu-id="b9bcb-305">This version info is generated as part of the [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) structure.</span></span> <span data-ttu-id="b9bcb-306">Le numéro de version peut être traité comme un sélecteur ARM d’Union pour que la structure soit extensible.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-306">The version number can be treated as a union arm selector to make the structure extensible.</span></span> <span data-ttu-id="b9bcb-307">Actuellement, la valeur de **VersionId** est définie sur rétablira sans les champs suivants.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-307">Currently, the **versionID** is set to1 with no subsequent fields.</span></span> <span data-ttu-id="b9bcb-308">Les versiosn ultérieures peuvent incrémenter le numéro de version et inclure plus de champs en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="b9bcb-308">Future versiosn may increment the version number and include more fields as needed.</span></span> <span data-ttu-id="b9bcb-309">Par exemple, Wsutil.exe génère actuellement le code suivant en fonction de l’ID de version :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-309">For example, Wsutil.exe currently generates the following code based on the version ID:</span></span>

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

<span data-ttu-id="b9bcb-310">À l’avenir, il pourrait être développé comme suit :</span><span class="sxs-lookup"><span data-stu-id="b9bcb-310">In the future, it could be expanded as follows:</span></span>

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

## <a name="security"></a><span data-ttu-id="b9bcb-311">Sécurité</span><span class="sxs-lookup"><span data-stu-id="b9bcb-311">Security</span></span>

<span data-ttu-id="b9bcb-312">Consultez la section sécurité dans la rubrique de l' [outil compilateur Wsutil](wsutil-compiler-tool.md) .</span><span class="sxs-lookup"><span data-stu-id="b9bcb-312">See the security section in the [Wsutil Compiler tool](wsutil-compiler-tool.md) topic.</span></span>

 

 




