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
ms.openlocfilehash: 8c0f55c5ea3828c72456989f7053e2ff008e524e41552b281b88839653229863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962898"
---
# <a name="schema-support"></a>Prise en charge des schémas

WsUtil.exe prend en charge le schéma XSD spécifié au niveau du [schéma XML](https://www.w3.org/XML/Schema). le fichier XSD et WSDL : type doivent être traités dans la même catégorie, à l’exception de wsdl : type lorsqu’un élément global peut être une liste de paramètres. Wsutil.exe génère des descriptions d’éléments pour toutes les définitions d’éléments globaux qui peuvent être utilisées dans le sérialiseur, avec une sortie supplémentaire pour la structure de paramètres spécifiée dans la [prise en charge WSDL](wsdl-support.md).

## <a name="xsd-schema-support-level"></a>Niveau de prise en charge du schéma XSD

WsUtil.exe ne prend pas en charge l’étendue complète du schéma XSD. Le niveau de support actuel est défini dans le [niveau de prise en charge du schéma](schema-support-level.md).

Génération de l’identificateur

Le nom d’élément ou le nom de type dans le schéma n’est peut-être pas un identificateur C valide et les noms sont normalisés en noms C valides générés. Les caractères d’identificateur C non valides sont convertis en nom hexadécimal, et un trait de soulignement « \_ » peut être préfixé au nom si nécessaire. Les types anonymes sont nommés à la suite du nom de l’élément englobant mais avec le trait de soulignement « \_ » pour éviter la collision de noms. Les noms de types globaux sont conservés, car ils sont normalisés après la normalisation des caractères non valides. Les types anonymes imbriqués sont préfixés avec le nom du type parent.

Pour chaque définition d’élément global, wsutil.exe génère [**une \_ \_ Description d’élément WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) dans la structure de description globale. Pour chaque définition de type global, wsutil.exe génère une description de type dans la structure de description globale à référencer par l’application.

Pour chaque champ de la structure, wsutil.exe génère une [**\_ \_ Description de champ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description) incorporée dans le cadre de la structure du boîtier.

## <a name="simple-types"></a>Types simples

Les types valeur, tels qu’ils sont répertoriés dans le [**\_ \_ type de valeur WS**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type), sont traités comme des types simples. Notez que \_ \_ le type de valeur WS est véritablement un sous-ensemble du [**\_ type WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type). Il comprend des types de données intégraux et flottants de base, ainsi que des valeurs DECIMAL, WS \_ DateTime et UUID.

Dans le modèle de service, dans les types simples sont passés par valeur, tandis que les types simples out et in, out sont passés par référence.

Wsutil crée une description d’élément simple comme ci-dessous pour l’élément global contenant des types simples.

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="helloworld" type="xs:int"></xs:element>
</xs:schema>
```

Wsutil génère la description de l’élément ci-dessous :

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

Cette structure est générée dans le cadre de la structure de description globale générée dans le fichier d’en-tête :

``` syntax
typedef struct _example_wsdl
{
WS_ELEMENT_DESCRIPTION helloworld;
} _example_wsdl;
```

## <a name="arrays"></a>Tableaux

L’élément avec maxOccurs supérieur à 1, ou séquence avec un seul élément, et l’élément enfant a maxOccurs supérieur à 1, est traité comme un tableau. Pour un élément de tableau dans le schéma, wsutil.exe génère deux champs : un champ de nombre qui ne passe pas en mode filaire et un champ de pointeur contenant le type de tableau.

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

Le fichier d’en-tête contient la définition de structure C pour le tableau, avec un compte de champ spécifiant le nombre de tableaux.

``` syntax
typedef struct SimpleArray
{
  unsigned int  aCount ;
  int  * a;
} SimpleArray;
```

L’exemple suivant fait partie du prototype LocalDefinition décrivant le tableau :

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

Voici les définitions générées des descriptions ci-dessus, notez le \_ mappage de champs de l’élément répété WS \_ \_ \_ qui indique le champ en tant que champ de tableau.

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

Si le tableau est un champ de paramètre dans un message d’entrée/sortie, deux paramètres réels sont générés pour la méthode. Si le tableau est un paramètre out ou in, out, il y aura un niveau supplémentaire d’indirection pour les deux champs dans paramStruct.

## <a name="range-on-array"></a>Plage sur le tableau

Nous vous recommandons de ne pas spécifier maxOccur = "unbounded" pour les tableaux. Au lieu de cela, un nombre entier fixe doit être spécifié pour définir une limite supérieure du nombre de tableaux autorisé. la plage est prise en charge pour les types intégraux, ainsi que les chaînes, les tableaux d’octets et les tableaux génériques.

## <a name="heuristic-for-wrapped-as-opposed-to-unwrapped-array"></a>Heuristique pour encapsulée au lieu du tableau non encapsulé

Parfois, les tableaux sont encapsulés dans une autre structure pour être incorporés dans une structure de niveau supérieur. Dans ce cas, nous devrions supprimer la couche de wrapper intermédiaire. WsUtil.exe génère le même prototype et les mêmes descriptions que SimpleArray décrit ci-dessus.

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

Wsutil détecte que SimpleArrayWrapper est un wrapper autour de SimpleArray et génère uniquement des structures suivantes, avec une structure distincte pour SimpleArray

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

wsutil.exe génère les définitions suivantes pour le prototype correspondant ci-dessus, remarque que dans la description du champ, les champs nom du wrapper et espace de noms du wrapper sont renseignés

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

## <a name="structures"></a>Structures

Un complexType avec plusieurs éléments dans une séquence est une structure. Par exemple,

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

Wsutil.exe génère un prototype de structure en tant que :

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

Wsutil génère le prototype suivant pour LocalDefinition :

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

La définition de la structure ressemble à l’exemple ci-dessous, avec deux descriptions de champ dans la structure.

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

Pour prendre en charge l’extensibilité, les structures incorporées sont toujours définies passées par référence. En service, toutes les structures out ou in, out ou out, sont passées par le pointeur double pour permettre une extension future de la structure, ainsi que l’autorisation de la structure nillable.

## <a name="recursive-structures"></a>Structures récursives

Les structures récursives sont prises en charge, et les types incorporés sont passés par référence. Pour le WSDL suivant :

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

Wsutil génère les définitions de type follow, ainsi que les descriptions de type :

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

La définition est générée comme suit :

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

## <a name="structure-inheritence"></a>Héritage de la structure

Wsutil prend en charge l’extension de type complexe où un type complexe est une extension d’un autre type complexe.

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

Le fragment XSD ci-dessus indique que DerivedLinkList dérive de LinkList.

Wsutil.exe génère des routines d’assistance pour C et C++ afin de faciliter la configuration des informations de type du type de base et des types dérivés pour l’application. Dans le code suivant, \_ la \_ macro WS CPLUSPLUS est utilisée pour différencier la définition du langage C et C++ :

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

Dans l’application auxiliaire du style C, avant serialiation, l’application appelle Wsutil routine LinkList \_ init générée pour initialiser la structure et définir la description du type sur linklist type Description. Après la désérialisation, l’application peut appeler LinkList \_ en tant que \_ DerivedLinkList pour récupérer le type dérivé.

Pour récupérer des informations de type dans le runtime, Wsutil génère le premier champ de type de base avec [**WS \_ struct \_ Description**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description) type et le mappage de champs d' \* [**\_ attribut de type \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping) pour décrire les informations xsi : type. L’application peut directement définir ou vérifier le champ pour déterminer le type réel de structures. Par exemple, le code suivant définit le type de la structure à DrivedLinkList :

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

Une fois que la structure est désérialisée, l’application peut comparer directement la description de type pour déterminer le type désérialisé :

``` syntax
if (derviedLinkList._base._type == (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription)
{
    // the deserialized type is of type _DerivedLinkList
    ...
}
```

Wsutil génère la classe pour la structure de base et la structure dérivée. Le constructeur par défaut initialise le type et la description de type correspondant. La routine AsDerivedType permet d’effectuer un cast de type sécurisé entre les types.

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

## <a name="nillable"></a>nillable

l’attribut nillable est pris en charge pour les chaînes, les structures et les tableaux d’octets. L' \_ \_ attribut nillable de champ WS sera ajouté aux champs avec l’attribut nillable. Le pointeur est défini sur **null** si un élément est nillable. Un champ nillable dans une structure est traité comme un pointeur. Une structure de paramètre avec l’attribut nillable sera passée par référence.

## <a name="pointers"></a>pointeurs

Le type valeur doit être passé par valeur ou par référence pour les paramètres out. Le pointeur double n’est pas autorisé, sauf pour les structures out uniquement.

## <a name="parameterless"></a>Sans paramètre

Souvenez-vous de notre discussion précédente concernant le nom « Parameters » pour la partie de message. Si cette valeur est spécifiée, nous essaierons de générer un frame combiné pour le message d’entrée et de sortie pour l’opération de service résultante. Si ce paramètre n’est pas spécifié, l’opération de service résultante contiendra alors des messages d’entrée et de sortie en tant que paramètres.

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

Par conséquent, pour notre opération SimpleMethod, la signature du service et du client doit ressembler à.

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

## <a name="security"></a>Sécurité

Consultez la section sécurité dans l' [outil compilateur Wsutil](wsutil-compiler-tool.md) et [sérialisation](serialization.md)

 

 




