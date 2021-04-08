---
title: Prise en charge des schémas
description: WsUtil.exe prend en charge le schéma XSD spécifié au niveau du schéma XML.
ms.assetid: 33096cda-9dbe-44d2-8d08-410bc33ae81c
keywords:
- Services Web de prise en charge de schéma pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dcf9d192c999333ee8b4e341e7722cd6bd59ff5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103940717"
---
# <a name="schema-support"></a><span data-ttu-id="068b2-106">Prise en charge des schémas</span><span class="sxs-lookup"><span data-stu-id="068b2-106">Schema support</span></span>

<span data-ttu-id="068b2-107">WsUtil.exe prend en charge le schéma XSD spécifié au niveau du [schéma XML](https://www.w3.org/XML/Schema).</span><span class="sxs-lookup"><span data-stu-id="068b2-107">WsUtil.exe supports the XSD schema specified at [XML Schema](https://www.w3.org/XML/Schema).</span></span> <span data-ttu-id="068b2-108">le fichier XSD et WSDL : type doivent être traités dans la même catégorie, à l’exception de wsdl : type lorsqu’un élément global peut être une liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="068b2-108">xsd file and wsdl:type should be treated in the same category, with the exception in wsdl:type when a global element could be a parameter list.</span></span> <span data-ttu-id="068b2-109">Wsutil.exe génère des descriptions d’éléments pour toutes les définitions d’éléments globaux qui peuvent être utilisées dans le sérialiseur, avec une sortie supplémentaire pour la structure de paramètres spécifiée dans la [prise en charge WSDL](wsdl-support.md).</span><span class="sxs-lookup"><span data-stu-id="068b2-109">Wsutil.exe generates element descriptions for all global element definitions that can be used in serializer, with additional output for parameter structure specified in [WSDL support](wsdl-support.md).</span></span>

## <a name="xsd-schema-support-level"></a><span data-ttu-id="068b2-110">Niveau de prise en charge du schéma XSD</span><span class="sxs-lookup"><span data-stu-id="068b2-110">XSD Schema Support Level</span></span>

<span data-ttu-id="068b2-111">WsUtil.exe ne prend pas en charge l’étendue complète du schéma XSD.</span><span class="sxs-lookup"><span data-stu-id="068b2-111">WsUtil.exe does not support the full extent of XSD schema.</span></span> <span data-ttu-id="068b2-112">Le niveau de support actuel est défini dans le [niveau de prise en charge du schéma](schema-support-level.md).</span><span class="sxs-lookup"><span data-stu-id="068b2-112">The current support level is defined in [Schema support level](schema-support-level.md).</span></span>

<span data-ttu-id="068b2-113">Génération de l’identificateur</span><span class="sxs-lookup"><span data-stu-id="068b2-113">Identifier generation</span></span>

<span data-ttu-id="068b2-114">Le nom d’élément ou le nom de type dans le schéma n’est peut-être pas un identificateur C valide et les noms sont normalisés en noms C valides générés.</span><span class="sxs-lookup"><span data-stu-id="068b2-114">Element name or type name in the schema might not be valid C identifier, and the names are normalized to generated valid C names.</span></span> <span data-ttu-id="068b2-115">Les caractères d’identificateur C non valides sont convertis en nom hexadécimal, et un trait de soulignement « \_ » peut être préfixé au nom si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="068b2-115">Invalid C identifier characters are converted to the hex name, and a underscore '\_' might be prefixed to the name if necessary.</span></span> <span data-ttu-id="068b2-116">Les types anonymes sont nommés à la suite du nom de l’élément englobant mais avec le trait de soulignement « \_ » pour éviter la collision de noms.</span><span class="sxs-lookup"><span data-stu-id="068b2-116">Anonymous types are named after the enclosing element name but prefixed with underscore "\_" to avoid name collision.</span></span> <span data-ttu-id="068b2-117">Les noms de types globaux sont conservés, car ils sont normalisés après la normalisation des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="068b2-117">Global type names are preserved as it is after invalid characters are normalized.</span></span> <span data-ttu-id="068b2-118">Les types anonymes imbriqués sont préfixés avec le nom du type parent.</span><span class="sxs-lookup"><span data-stu-id="068b2-118">Nested anonymous types are prefixed with the parent type name.</span></span>

<span data-ttu-id="068b2-119">Pour chaque définition d’élément global, wsutil.exe génère [**une \_ \_ Description d’élément WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) dans la structure de description globale.</span><span class="sxs-lookup"><span data-stu-id="068b2-119">For every global element definition, wsutil.exe generates a [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) in the global description structure.</span></span> <span data-ttu-id="068b2-120">Pour chaque définition de type global, wsutil.exe génère une description de type dans la structure de description globale à référencer par l’application.</span><span class="sxs-lookup"><span data-stu-id="068b2-120">For every global type definition, wsutil.exe generates a type description in the global description structure to be referenced by application.</span></span>

<span data-ttu-id="068b2-121">Pour chaque champ de la structure, wsutil.exe génère une [**\_ \_ Description de champ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description) incorporée dans le cadre de la structure du boîtier.</span><span class="sxs-lookup"><span data-stu-id="068b2-121">For each field in the structure, wsutil.exe generates a [**WS\_FIELD\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description) embedded as part of the enclosure structure.</span></span>

## <a name="simple-types"></a><span data-ttu-id="068b2-122">Types simples</span><span class="sxs-lookup"><span data-stu-id="068b2-122">Simple Types</span></span>

<span data-ttu-id="068b2-123">Les types valeur, tels qu’ils sont répertoriés dans le [**\_ \_ type de valeur WS**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type), sont traités comme des types simples.</span><span class="sxs-lookup"><span data-stu-id="068b2-123">Value types, as listed in [**WS\_VALUE\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type), are treated as simple types.</span></span> <span data-ttu-id="068b2-124">Notez que \_ \_ le type de valeur WS est véritablement un sous-ensemble du [**\_ type WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span><span class="sxs-lookup"><span data-stu-id="068b2-124">Notice that WS\_VALUE\_TYPE is really a subset of [**WS\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span></span> <span data-ttu-id="068b2-125">Il comprend des types de données intégraux et flottants de base, ainsi que des valeurs DECIMAL, WS \_ DateTime et UUID.</span><span class="sxs-lookup"><span data-stu-id="068b2-125">It includes basic integral and float data types, as well as DECIMAL, WS\_DATETIME, and UUID.</span></span>

<span data-ttu-id="068b2-126">Dans le modèle de service, dans les types simples sont passés par valeur, tandis que les types simples out et in, out sont passés par référence.</span><span class="sxs-lookup"><span data-stu-id="068b2-126">In service model, in simple types are passed by value, while out and in,out simple types are passed by reference.</span></span>

<span data-ttu-id="068b2-127">Wsutil crée une description d’élément simple comme ci-dessous pour l’élément global contenant des types simples.</span><span class="sxs-lookup"><span data-stu-id="068b2-127">Wsutil create simple element description like below for global element containing simple types.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="helloworld" type="xs:int"></xs:element>
</xs:schema>
```

<span data-ttu-id="068b2-128">Wsutil génère la description de l’élément ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="068b2-128">Wsutil generates the element description below:</span></span>

``` syntax
...  // global elements
{ // helloworld
{
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.helloworldTypeName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.helloworldTypeNamespace,
WS_INT32_TYPE,
0,
},
}, // helloworld
... 
```

<span data-ttu-id="068b2-129">Cette structure est générée dans le cadre de la structure de description globale générée dans le fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="068b2-129">This structure is generated as part of the global description structure generated in header file:</span></span>

``` syntax
typedef struct _example_wsdl
{
WS_ELEMENT_DESCRIPTION helloworld;
} _example_wsdl;
```

## <a name="arrays"></a><span data-ttu-id="068b2-130">Tableaux</span><span class="sxs-lookup"><span data-stu-id="068b2-130">Arrays</span></span>

<span data-ttu-id="068b2-131">L’élément avec maxOccurs supérieur à 1, ou séquence avec un seul élément, et l’élément enfant a maxOccurs supérieur à 1, est traité comme un tableau.</span><span class="sxs-lookup"><span data-stu-id="068b2-131">Element with maxOccurs larger than 1, or sequence with only one item, and the child element has maxOccurs larger than 1, is treated as array.</span></span> <span data-ttu-id="068b2-132">Pour un élément de tableau dans le schéma, wsutil.exe génère deux champs : un champ de nombre qui ne passe pas en mode filaire et un champ de pointeur contenant le type de tableau.</span><span class="sxs-lookup"><span data-stu-id="068b2-132">For an array element in schema, wsutil.exe generates two fields: one count field that does not go on wire, and one pointer field containing the array type.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="SimpleArray">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" maxOccurs="50" name="a" nillable="true" type="xs:int" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema>
```

<span data-ttu-id="068b2-133">Le fichier d’en-tête contient la définition de structure C pour le tableau, avec un compte de champ spécifiant le nombre de tableaux.</span><span class="sxs-lookup"><span data-stu-id="068b2-133">Header file contains the C structure definition for the array, with field aCount specifying the count of the array.</span></span>

``` syntax
typedef struct SimpleArray
{
  unsigned int  aCount ;
  int  * a;
} SimpleArray;
```

<span data-ttu-id="068b2-134">L’exemple suivant fait partie du prototype LocalDefinition décrivant le tableau :</span><span class="sxs-lookup"><span data-stu-id="068b2-134">Following is part of the LocalDefinition prototype describing the array:</span></span>

``` syntax
... // globalElement part of the LocalDefinitions.
struct // SimpleArray
{
  struct // SimpleArray
  {
    WS_FIELD_DESCRIPTION a;
    WS_FIELD_DESCRIPTION * SimpleArrayFields [1];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleArraydescs; // SimpleArray
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleArray;

// Method with array parameters.
  typedef HRESULT (CALLBACK *SimpleMethodCallback)(
    const WS_OPERATION_CONTEXT* context,
    unsigned int aCount,
    int* a,
    unsigned int *bCount,
    int** b,
    unsigned int* cCount,
    int** c,
    const WS_ASYNC_CONTEXT* asyncContext,
    WS_ERROR* error);

  HRESULT CALLBACK SimpleMethod (
    WS_SERVICE_PROXY* serviceProxy,
    WS_HEAP* heap,
    unsigned int aCount,
    int* a,
    unsigned int *bCount,
    int** b,
    unsigned int* cCount,
    int** c,
    const WS_ASYNC_CONTEXT* asyncContext,
    WS_ERROR* error);
```

<span data-ttu-id="068b2-135">Voici les définitions générées des descriptions ci-dessus, notez le \_ mappage de champs de l’élément répété WS \_ \_ \_ qui indique le champ en tant que champ de tableau.</span><span class="sxs-lookup"><span data-stu-id="068b2-135">Following is the generated definitions of the above descriptions, notice the WS\_REPEATING\_ELEMENT\_FIELD\_MAPPING which indicates the field as an array field.</span></span>

``` syntax
...
{ // SimpleArray
  {   // SimpleArray
    { // field description for a
      WS_REPEATING_ELEMENT_FIELD_MAPPING,
      0,
      0,
      WS_INT32_TYPE,
      0,
      WsOffsetOf(SimpleArray, a),
      0,
      0,
      WsOffsetOf(SimpleArray, aCount),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    },    // end of field description for a
    {    // fields description for SimpleArray
      (WS_FIELD_DESCRIPTION*)&example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.a,
    },
    {
      sizeof(SimpleArray),
      __alignof(SimpleArray),
      (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.
      SimpleArrayFields,
      WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.SimpleArrayFields),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayTypeName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    },   // struct description for SimpleArray
  },    // SimpleArray
  {
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    WS_STRUCT_TYPE,
    (void *)&example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.structDesc,
  },
}, // SimpleArray
...
```

<span data-ttu-id="068b2-136">Si le tableau est un champ de paramètre dans un message d’entrée/sortie, deux paramètres réels sont générés pour la méthode.</span><span class="sxs-lookup"><span data-stu-id="068b2-136">If the array is a parameter field in input/output message, there would be two actual parameters generated for the method.</span></span> <span data-ttu-id="068b2-137">Si le tableau est un paramètre out ou in, out, il y aura un niveau supplémentaire d’indirection pour les deux champs dans paramStruct.</span><span class="sxs-lookup"><span data-stu-id="068b2-137">If the array is an out or in,out parameter, there would be one additional level of indirection for both fields in paramStruct.</span></span>

## <a name="range-on-array"></a><span data-ttu-id="068b2-138">Plage sur le tableau</span><span class="sxs-lookup"><span data-stu-id="068b2-138">Range on Array</span></span>

<span data-ttu-id="068b2-139">Nous vous recommandons de ne pas spécifier maxOccur = "unbounded" pour les tableaux.</span><span class="sxs-lookup"><span data-stu-id="068b2-139">We recommend the best practice of not specifying maxOccur="unbounded" for arrays.</span></span> <span data-ttu-id="068b2-140">Au lieu de cela, un nombre entier fixe doit être spécifié pour définir une limite supérieure du nombre de tableaux autorisé.</span><span class="sxs-lookup"><span data-stu-id="068b2-140">Instead, a fixed integer number should be specified to set a upper bound of array counts allowed.</span></span> <span data-ttu-id="068b2-141">la plage est prise en charge pour les types intégraux, ainsi que les chaînes, les tableaux d’octets et les tableaux génériques.</span><span class="sxs-lookup"><span data-stu-id="068b2-141">range is supported for integral types, as well as strings, byte arrays, and generic arrays.</span></span>

## <a name="heuristic-for-wrapped-as-opposed-to-unwrapped-array"></a><span data-ttu-id="068b2-142">Heuristique pour encapsulée au lieu du tableau non encapsulé</span><span class="sxs-lookup"><span data-stu-id="068b2-142">Heuristic for Wrapped as Opposed to Unwrapped array</span></span>

<span data-ttu-id="068b2-143">Parfois, les tableaux sont encapsulés dans une autre structure pour être incorporés dans une structure de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="068b2-143">Sometimes arrays are wrapped inside another structure to be embedded in a top level structure.</span></span> <span data-ttu-id="068b2-144">Dans ce cas, nous devrions supprimer la couche de wrapper intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="068b2-144">In that case, we should remove the intermediate wrapper layer.</span></span> <span data-ttu-id="068b2-145">WsUtil.exe génère le même prototype et les mêmes descriptions que SimpleArray décrit ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="068b2-145">WsUtil.exe generates the same prototype and descriptions as SimpleArray described above.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:complexType name="SimpleArray">
  <xs:sequence>
   <xs:element minOccurs="0" maxOccurs="50" name="aa" type="xs:int" />
  </xs:sequence>
 </xs:complexType>
 <xs:element name="SimpleArrayWrapper">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="SimpleArray" type="tns:SimpleArray" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema>
```

<span data-ttu-id="068b2-146">Wsutil détecte que SimpleArrayWrapper est un wrapper autour de SimpleArray et génère uniquement des structures suivantes, avec une structure distincte pour SimpleArray</span><span class="sxs-lookup"><span data-stu-id="068b2-146">Wsutil detects that SimpleArrayWrapper is a wrapper around SimpleArray, and generates following structures only, with separate structure for SimpleArray</span></span>

``` syntax
typedef struct SimpleArrayWrapper
{
  unsigned int  SimpleArrayCount ;
  int  * SimpleArray;
} SimpleArrayWrapper;

.. // global element inside the LocalDefinitions prototype
struct // SimpleArrayWrapper
{
  struct // SimpleArrayWrapper
  {
    WS_FIELD_DESCRIPTION SimpleArray;
    WS_FIELD_DESCRIPTION * SimpleArrayWrapperFields [1];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleArrayWrapperdescs; // SimpleArrayWrapper
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleArrayWrapper;
...
```

<span data-ttu-id="068b2-147">wsutil.exe génère les définitions suivantes pour le prototype correspondant ci-dessus, remarque que dans la description du champ, les champs nom du wrapper et espace de noms du wrapper sont renseignés</span><span class="sxs-lookup"><span data-stu-id="068b2-147">wsutil.exe generates the following definitions for the matching prototype above, notices that in the field description, the wrapper name and wrapper namespace fields are filled in</span></span>

``` syntax
... // global element part of the LocalDefinitions structure:
{ // SimpleArrayWrapper
  {   // SimpleArrayWrapper
    { // WS_FIELD_DESCRIPTION  for SimpleArray
      WS_REPEATING_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayWrapperName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
      WS_INT32_TYPE,
      0,
      WsOffsetOf(SimpleArrayWrapper, SimpleArray),
      0,
      0,
      WsOffsetOf(SimpleArrayWrapper, SimpleArrayCount),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
    },    // end of field description for SimpleArray
    {    // array of field descriptions for SimpleArrayWrapper
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.SimpleArray,
    },
    {  // WS_STRUCT_DESCRIPTION for SimpleArrayWrapper
      sizeof(SimpleArrayWrapper),
      __alignof(SimpleArrayWrapper),
      (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.SimpleArrayWrapperFields,
      WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.SimpleArrayWrapperFields),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayWrapperTypeName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
    },   // struct description for SimpleArrayWrapper
    },    // SimpleArrayWrapper
  {  // WS_ELEMENT_DESCRIPTION for SimpleArrayWrapper
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayWrapperTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
    WS_STRUCT_TYPE,
    (void *)&example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.structDesc,
  },
}, // SimpleArrayWrapper
```

## <a name="structures"></a><span data-ttu-id="068b2-148">Structures</span><span class="sxs-lookup"><span data-stu-id="068b2-148">Structures</span></span>

<span data-ttu-id="068b2-149">Un complexType avec plusieurs éléments dans une séquence est une structure.</span><span class="sxs-lookup"><span data-stu-id="068b2-149">A complexType with multiple elements in a sequence is a structure.</span></span> <span data-ttu-id="068b2-150">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="068b2-150">For example,</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:complexType name="StructType">
  <xs:sequence>
   <xs:element minOccurs="0" name="FirstName" nillable="true" type="xs:string" />
   <xs:element minOccurs="0" name="LastName" nillable="true" type="xs:string" />
  </xs:sequence>
 </xs:complexType>
 <xs:element name="StructType" nillable="true" type="tns:StructType" />
</xs:schema>
```

<span data-ttu-id="068b2-151">Wsutil.exe génère un prototype de structure en tant que :</span><span class="sxs-lookup"><span data-stu-id="068b2-151">Wsutil.exe generates a structure prototype as:</span></span>

``` syntax
struct StructType
{
  WS_STRING FirstName;
  WS_STRING LastName;
};

// methods using structure parameters.
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT* context,
  StructType* a,
  StructType** b,
  StructType** c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);

HRESULT CALLBACK SimpleMethod (WS_SERVICE_PROXY* serviceProxy,
  WS_HEAP* heap,
  StructType* a,
  StructType** b,
  StructType** c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);
```

<span data-ttu-id="068b2-152">Wsutil génère le prototype suivant pour LocalDefinition :</span><span class="sxs-lookup"><span data-stu-id="068b2-152">wsutil generates the following prototype for LocalDefinition:</span></span>

``` syntax
struct // StructType
{
  struct // StructType
  {
    WS_FIELD_DESCRIPTION FirstName;
    WS_FIELD_DESCRIPTION LastName;
    WS_FIELD_DESCRIPTION * StructTypeFields [2];
    WS_STRUCT_DESCRIPTION structDesc;
  } StructTypedescs; // StructType
WS_ELEMENT_DESCRIPTION elementDesc;
}
```

<span data-ttu-id="068b2-153">La définition de la structure ressemble à l’exemple ci-dessous, avec deux descriptions de champ dans la structure.</span><span class="sxs-lookup"><span data-stu-id="068b2-153">The definition for the structure looks like below, with two field descriptions in the structure.</span></span>

``` syntax
// global element inside LocalDefinitions.
{ // StructType
  {   // StructType
    { // field description for FirstName
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
      WS_STRING_TYPE,
      0,
      WsOffsetOf(StructType, FirstName),
      0,
      0,
    },    // end of field description for FirstName
    { // field description for LastName
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.LastNameLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
      WS_STRING_TYPE,
      0,
      WsOffsetOf(StructType, LastName),
      0,
      0,
    },    // end of field description for LastName
    {    // fields description for StructType
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.FirstName,
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.LastName,
    },
    { // WS_STRUCT_DESCRIPTION for StructType
      sizeof(StructType),
      __alignof(StructType),
      (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.StructTypeFields,
      WsCountOf(example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.StructTypeFields),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.StructTypeTypeName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
    },   // struct description for StructType
  },    // StructType
  {
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.StructTypeTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
    WS_STRUCT_TYPE,
    (void *)&example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.structDesc,
  },
}, // StructType
```

<span data-ttu-id="068b2-154">Pour prendre en charge l’extensibilité, les structures incorporées sont toujours définies passées par référence.</span><span class="sxs-lookup"><span data-stu-id="068b2-154">To support extensibility, embedded structures are always defined passed by reference.</span></span> <span data-ttu-id="068b2-155">En service, toutes les structures out ou in, out ou out, sont passées par le pointeur double pour permettre une extension future de la structure, ainsi que l’autorisation de la structure nillable.</span><span class="sxs-lookup"><span data-stu-id="068b2-155">In service, all out or in,out structures are passed by double pointer to allow future extension of the structure, as well as allowing nillable structure.</span></span>

## <a name="recursive-structures"></a><span data-ttu-id="068b2-156">Structures récursives</span><span class="sxs-lookup"><span data-stu-id="068b2-156">Recursive Structures</span></span>

<span data-ttu-id="068b2-157">Les structures récursives sont prises en charge, et les types incorporés sont passés par référence.</span><span class="sxs-lookup"><span data-stu-id="068b2-157">Recursive structures are supported, and the embedded types is passed by reference.</span></span> <span data-ttu-id="068b2-158">Pour le WSDL suivant :</span><span class="sxs-lookup"><span data-stu-id="068b2-158">For the following wsdl:</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="SimpleMethod">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="a" type="xs:int" />
    <xs:element minOccurs="0" name="b" type="tns:example" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
 <xs:complexType name="example">
  <xs:sequence>
   <xs:element minOccurs="0" name="d" type="tns:example" />
   <xs:element minOccurs="0" name="c" type="xs:int" />
  </xs:sequence>
 </xs:complexType>
</xs:schema>
```

<span data-ttu-id="068b2-159">Wsutil génère les définitions de type follow, ainsi que les descriptions de type :</span><span class="sxs-lookup"><span data-stu-id="068b2-159">Wsutil generates the follow type definitions, as well as the type descriptions:</span></span>

``` syntax
typedef struct example
{
  struct example  * d;
  int32   c;
} example;

typedef struct SimpleMethod
{
  unsigned __int32   a;
  struct example  * b;
} SimpleMethod;

// global element part of the LocalDefinitions.
...
struct // SimpleMethod
{
  struct // SimpleMethod
  {
    WS_FIELD_DESCRIPTION a;
    struct // example
    {
      WS_FIELD_DESCRIPTION d;
      WS_FIELD_DESCRIPTION c;
      WS_FIELD_DESCRIPTION * exampleFields [2];
      WS_STRUCT_DESCRIPTION structDesc;
    } exampledescs; // example
    WS_FIELD_DESCRIPTION b;
    WS_FIELD_DESCRIPTION * SimpleMethodFields [2];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleMethoddescs; // SimpleMethod
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleMethod;
...
```

<span data-ttu-id="068b2-160">La définition est générée comme suit :</span><span class="sxs-lookup"><span data-stu-id="068b2-160">The definition is generated as below:</span></span>

``` syntax
{   // SimpleMethod
  { // field description for a
    WS_ELEMENT_FIELD_MAPPING,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aLocalName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    WS_INT32_TYPE,
    0,
    WsOffsetOf(SimpleMethod, a),
    0,
    0,
  },    // end of field description for a
  {   // example
    { // field description for d
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.dLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
      WS_STRUCT_TYPE,
      (WS_STRUCT_DESCRIPTION*)&example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.structDesc,
      WsOffsetOf(example, d),
      WS_FIELD_POINTER,
      0,
    },    // end of field description for d
    { // field description for c
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.cLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
      WS_INT32_TYPE,
      0,
      WsOffsetOf(example, c),
      0,
      0,
    },    // end of field description for c
    {    // fields description for example
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.d,
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.c,
    },
  {
    sizeof(example),
    __alignof(example),
    (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.exampleFields,
    WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.exampleFields),
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.exampleTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  },   // struct description for example
}
```

## <a name="structure-inheritence"></a><span data-ttu-id="068b2-161">Héritage de la structure</span><span class="sxs-lookup"><span data-stu-id="068b2-161">Structure inheritence</span></span>

<span data-ttu-id="068b2-162">Wsutil prend en charge l’extension de type complexe où un type complexe est une extension d’un autre type complexe.</span><span class="sxs-lookup"><span data-stu-id="068b2-162">wsutil supports complex type extension where one complex type is an extension to another complex type.</span></span>

``` syntax
<s:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:s="http://www.w3.org/2001/XMLSchema">
 <s:complexType name="LinkList">
  <s:sequence>
   <s:element minOccurs="0" name="d" type="tns:LinkList" />
   <s:element minOccurs="0" name="c" type="s:int" />
  </s:sequence>
 </s:complexType> 
 <s:element name="DerivedLinkList">
  <s:complexType>
   <s:complexContent>
    <s:extension base="tns:LinkList">
     <s:sequence>
      <s:element name="derive1" type="s:int" />
     </s:sequence>
    </s:extension>
   </s:complexContent>
  </s:complexType>
 </s:element>
</s:schema>
```

<span data-ttu-id="068b2-163">Le fragment XSD ci-dessus indique que DerivedLinkList dérive de LinkList.</span><span class="sxs-lookup"><span data-stu-id="068b2-163">The above xsd fragment indicates that DerivedLinkList derives from LinkList.</span></span>

<span data-ttu-id="068b2-164">Wsutil.exe génère des routines d’assistance pour C et C++ afin de faciliter la configuration des informations de type du type de base et des types dérivés pour l’application.</span><span class="sxs-lookup"><span data-stu-id="068b2-164">Wsutil.exe generates helper routines for both C and C++ to make it easier for application to set up the type information of base type and derived types.</span></span> <span data-ttu-id="068b2-165">Dans le code suivant, \_ la \_ macro WS CPLUSPLUS est utilisée pour différencier la définition du langage C et C++ :</span><span class="sxs-lookup"><span data-stu-id="068b2-165">In the following code, \_WS\_CPLUSPLUS macro is used to differentiate definition for C and C++ language:</span></span>

``` syntax
#if defined(_WS_CPLUSPLUS)
typedef struct LinkList
{
  LinkList();
  LinkList(WS_STRUCT_DESCRIPTION*);
  struct _DerivedLinkList* WINAPI As_DerivedLinkList();
  const struct _WS_STRUCT_DESCRIPTION* _type;
  struct LinkList * d;
  int  c;
} LinkList;
#endif

#if !defined(_WS_CPLUSPLUS)
typedef struct LinkList
{
  const struct _WS_STRUCT_DESCRIPTION* _type;
  struct LinkList * d;
  int  c;
} LinkList;

void WINAPI LinkList_Init(LinkList*);
#endif

#if defined(_WS_CPLUSPLUS)
typedef struct _DerivedLinkList:LinkList
{
  _DerivedLinkList();
  int  derive1;
} _DerivedLinkList;
#endif

#if !defined(_WS_CPLUSPLUS)
typedef struct _DerivedLinkList
{
  struct LinkList _base;
  int  derive1;
} _DerivedLinkList;

struct _DerivedLinkList* WINAPI LinkList_As_DerivedLinkList(LinkList*);
#endif
```

<span data-ttu-id="068b2-166">Dans l’application auxiliaire du style C, avant serialiation, l’application appelle Wsutil routine LinkList \_ init générée pour initialiser la structure et définir la description du type sur linklist type Description.</span><span class="sxs-lookup"><span data-stu-id="068b2-166">In C style helper, before serialiation, application calls wsutil generated routine LinkList\_Init to initialize the structure and set the type description to LinkList type description.</span></span> <span data-ttu-id="068b2-167">Après la désérialisation, l’application peut appeler LinkList \_ en tant que \_ DerivedLinkList pour récupérer le type dérivé.</span><span class="sxs-lookup"><span data-stu-id="068b2-167">After deserialization, application can call LinkList\_As\_DerivedLinkList to get the derived type.</span></span>

<span data-ttu-id="068b2-168">Pour récupérer des informations de type dans le runtime, Wsutil génère le premier champ de type de base avec [**WS \_ struct \_ Description**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description) type et le mappage de champs d' \* [**\_ attribut de type \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping) pour décrire les informations xsi : type.</span><span class="sxs-lookup"><span data-stu-id="068b2-168">To retrieve type information in runtime, wsutil generates the first field of base type with [**WS\_STRUCT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)\* type and [**WS\_TYPE\_ATTRIBUTE\_FIELD\_MAPPING**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping) field mapping to describe the xsi:type information.</span></span> <span data-ttu-id="068b2-169">L’application peut directement définir ou vérifier le champ pour déterminer le type réel de structures.</span><span class="sxs-lookup"><span data-stu-id="068b2-169">Application can directly set or check the field to determine the actual type of structures.</span></span> <span data-ttu-id="068b2-170">Par exemple, le code suivant définit le type de la structure à DrivedLinkList :</span><span class="sxs-lookup"><span data-stu-id="068b2-170">For example, the following code set the type of the structure to be DrivedLinkList:</span></span>

``` syntax
_DerivedLinkList derivedLinkList;
derivedLinkList._base._type = (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription;
WsWriteType(
    writer,
    WS_ELEMENT_TYPE_MAPPING,
    WS_STRUCT_TYPE,
    (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription,
    ...);
```

<span data-ttu-id="068b2-171">Une fois que la structure est désérialisée, l’application peut comparer directement la description de type pour déterminer le type désérialisé :</span><span class="sxs-lookup"><span data-stu-id="068b2-171">After the structure is deserialized, application can directly compares the type description to determine the deserialized type:</span></span>

``` syntax
if (derviedLinkList._base._type == (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription)
{
    // the deserialized type is of type _DerivedLinkList
    ...
}
```

<span data-ttu-id="068b2-172">Wsutil génère la classe pour la structure de base et la structure dérivée.</span><span class="sxs-lookup"><span data-stu-id="068b2-172">wsutil generate class for both base structure and derived structure.</span></span> <span data-ttu-id="068b2-173">Le constructeur par défaut initialise le type et la description de type correspondant.</span><span class="sxs-lookup"><span data-stu-id="068b2-173">The default constructor initialize the type and matching type description.</span></span> <span data-ttu-id="068b2-174">La routine AsDerivedType permet d’effectuer un cast de type sécurisé entre les types.</span><span class="sxs-lookup"><span data-stu-id="068b2-174">The AsDerivedType routine helps to do safe type casting between types.</span></span>

``` syntax
  { // field description for typeOfLinkList
  WS_TYPE_ATTRIBUTE_FIELD_MAPPING,
  0,
  0,
  WS_DESCRIPTION_TYPE,
  0,
  WsOffsetOf(LinkList, typeOfLinkList),
  0,
  0,
  },    // end of field description for typeOfLinkList        ...
  {
  sizeof(LinkList),
  __alignof(LinkList),
  (WS_FIELD_DESCRIPTION**)&test_xsdLocalDefinitions.globalTypes.LinkListdescs.LinkListFields,
WsCountOf(test_xsdLocalDefinitions.globalTypes.LinkListdescs.LinkListFields),
(WS_XML_STRING*)&test_xsdLocalDefinitions.dictionary.xmlStrings.LinkListTypeName,
(WS_XML_STRING*)&test_xsdLocalDefinitions.dictionary.xmlStrings.LinkListTypeNamespace,
0,
(WS_STRUCT_DESCRIPTION**)&test_xsdLocalDefinitions.globalTypes.LinkListdescs.SubTypes,
  1,
  },   // struct description for LinkList
```

## <a name="nillable"></a><span data-ttu-id="068b2-175">nillable</span><span class="sxs-lookup"><span data-stu-id="068b2-175">nillable</span></span>

<span data-ttu-id="068b2-176">l’attribut nillable est pris en charge pour les chaînes, les structures et les tableaux d’octets.</span><span class="sxs-lookup"><span data-stu-id="068b2-176">nillable attribute is supported for strings, structs, and byte arrays.</span></span> <span data-ttu-id="068b2-177">L' \_ \_ attribut nillable de champ WS sera ajouté aux champs avec l’attribut nillable.</span><span class="sxs-lookup"><span data-stu-id="068b2-177">WS\_FIELD\_NILLABLE attribute will be added to fields with nillable attribute.</span></span> <span data-ttu-id="068b2-178">Le pointeur est défini sur **null** si un élément est nillable.</span><span class="sxs-lookup"><span data-stu-id="068b2-178">The pointer will be set to **NULL** if an element is nillable.</span></span> <span data-ttu-id="068b2-179">Un champ nillable dans une structure est traité comme un pointeur.</span><span class="sxs-lookup"><span data-stu-id="068b2-179">A nillable field in a structure is treated as a pointer.</span></span> <span data-ttu-id="068b2-180">Une structure de paramètre avec l’attribut nillable sera passée par référence.</span><span class="sxs-lookup"><span data-stu-id="068b2-180">A parameter structure with nillable attribute will be passed by reference.</span></span>

## <a name="pointers"></a><span data-ttu-id="068b2-181">pointeurs</span><span class="sxs-lookup"><span data-stu-id="068b2-181">pointers</span></span>

<span data-ttu-id="068b2-182">Le type valeur doit être passé par valeur ou par référence pour les paramètres out.</span><span class="sxs-lookup"><span data-stu-id="068b2-182">Value type must be passed by value or by reference for out parameters.</span></span> <span data-ttu-id="068b2-183">Le pointeur double n’est pas autorisé, sauf pour les structures out uniquement.</span><span class="sxs-lookup"><span data-stu-id="068b2-183">Double pointer is not allowed except for out only structures.</span></span>

## <a name="parameterless"></a><span data-ttu-id="068b2-184">Sans paramètre</span><span class="sxs-lookup"><span data-stu-id="068b2-184">Parameterless</span></span>

<span data-ttu-id="068b2-185">Souvenez-vous de notre discussion précédente concernant le nom « Parameters » pour la partie de message.</span><span class="sxs-lookup"><span data-stu-id="068b2-185">Recall our prior discussion for the "parameters" name for the message part.</span></span> <span data-ttu-id="068b2-186">Si cette valeur est spécifiée, nous essaierons de générer un frame combiné pour le message d’entrée et de sortie pour l’opération de service résultante.</span><span class="sxs-lookup"><span data-stu-id="068b2-186">If this is specified we will attempt to generate a combined frame for input and output message for the resulting service operation.</span></span> <span data-ttu-id="068b2-187">Si ce paramètre n’est pas spécifié, l’opération de service résultante contiendra alors des messages d’entrée et de sortie en tant que paramètres.</span><span class="sxs-lookup"><span data-stu-id="068b2-187">If this is not specified the resulting service operation would then contain input and output messages as structs as parameters.</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://Sapphire.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="http://www.w3.org/2005/08/addressing" 
xmlns:wsx="http://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="http://Sapphire.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="noparameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="noparameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
</wsdl:definitions>
```

<span data-ttu-id="068b2-188">Par conséquent, pour notre opération SimpleMethod, la signature du service et du client doit ressembler à.</span><span class="sxs-lookup"><span data-stu-id="068b2-188">Thus for our SimpleMethod operation the signature for the service and the client will look like.</span></span>

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback)
  (const WS_OPERATION_CONTEXT* context,
  SimpleMethodRequest* inMessage,
  SimpleMethodResponse** outMessage,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);

HRESULT CALLBACK SimpleMethod (
  WS_SERVICE_PROXY* serviceProxy,
  WS_HEAP* heap,
  SimpleMethodRequest* inMessage,
  SimpleMethodResponse** outMessage,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);
```

## <a name="security"></a><span data-ttu-id="068b2-189">Sécurité</span><span class="sxs-lookup"><span data-stu-id="068b2-189">Security</span></span>

<span data-ttu-id="068b2-190">Consultez la section sécurité dans l' [outil compilateur Wsutil](wsutil-compiler-tool.md) et [sérialisation](serialization.md)</span><span class="sxs-lookup"><span data-stu-id="068b2-190">See security section in [Wsutil Compiler tool](wsutil-compiler-tool.md) as well as [Serialization](serialization.md)</span></span>

 

 




