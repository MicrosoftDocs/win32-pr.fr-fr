---
title: Fichier d’extension de service Web
description: Cette section décrit le fichier d’extension du service Web.
ms.assetid: 856d4ff5-2292-4d87-ae7c-19b100fd1cb3
keywords:
- Services Web du fichier d’extension de service Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0802e31895aa5dd5051c94746e774033a1ebe677
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316812"
---
# <a name="web-service-extension-file"></a><span data-ttu-id="0b783-106">Fichier d’extension de service Web</span><span class="sxs-lookup"><span data-stu-id="0b783-106">Web Service Extension File</span></span>

<span data-ttu-id="0b783-107">Cette section décrit le fichier d’extension du service Web.</span><span class="sxs-lookup"><span data-stu-id="0b783-107">This section outlines Web Service extension file.</span></span>


<span data-ttu-id="0b783-108">Le fichier WSX (extension de service WCF) est notre fichier d’extension pour permettre à l’application de manipuler les comportements locaux qui n’affectent pas la représentation des données de transmission.</span><span class="sxs-lookup"><span data-stu-id="0b783-108">WSX file (WCF service extension) is our extension file to allow application to manipulate local behaviors that do not affect wire data representation.</span></span> <span data-ttu-id="0b783-109">Il devrait être extensible que nous pouvons ajouter de nouvelles fonctionnalités à l’avenir sans interrompre l’interopérabilité.</span><span class="sxs-lookup"><span data-stu-id="0b783-109">It should be extensible that we can add new features in the future without breaking interoperability.</span></span>

<span data-ttu-id="0b783-110">La structure globale de WSX imiterait la structure du fichier XSD ou WSDL, qui est un fichier XML qui gère la même structure que le fichier d’entrée principal.</span><span class="sxs-lookup"><span data-stu-id="0b783-110">The overall structure of WSX would mimic the structure of XSD or WSDL file, which is a XML file that maintains the same structure as the main input file.</span></span> <span data-ttu-id="0b783-111">Les attributs supplémentaires sur le même jeton nommé dans le fichier principal spécifient les attributs que l’application veut contrôler sur le comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="0b783-111">Extra attributes on the same named token in main file would specify the attributes that application wants to control over the default behavior.</span></span>

<span data-ttu-id="0b783-112">Il est possible que nous ne puissions rien faire ici dans m3.</span><span class="sxs-lookup"><span data-stu-id="0b783-112">We might not do anything here in M3.</span></span> <span data-ttu-id="0b783-113">Dans v1, je peux voir que nous prenons en charge les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="0b783-113">In V1, I can see we support the following attributes:</span></span>

<span data-ttu-id="0b783-114">Utilisation spécifiant l’argument ou le champ de paramètre count.</span><span class="sxs-lookup"><span data-stu-id="0b783-114">Usage Specifying count argument/parameter field.</span></span>

<span data-ttu-id="0b783-115">Il s’agit d’un attribut d’élément, mais applicable uniquement au type de tableau.</span><span class="sxs-lookup"><span data-stu-id="0b783-115">This is an element attribute but applicable to array type only.</span></span> <span data-ttu-id="0b783-116">L’attribut IsCountOf spécifie l’élément de tableau.</span><span class="sxs-lookup"><span data-stu-id="0b783-116">IsCountOf attribute specifies the array element.</span></span> <span data-ttu-id="0b783-117">Le champ/paramètre Count n’apparaît pas sur le câble.</span><span class="sxs-lookup"><span data-stu-id="0b783-117">The count field/parameter does not appear on wire.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="FooInParam">
  <complexType> 
   <!-- MyArray field is presented in WSDL file as an element -->
    <element name="MyArrayCount" IsCountOf="MyArray"></element>
   </complexType>
  </element>
 </xs:schema>
```

<span data-ttu-id="0b783-118">Spécification d’un rappel de lecture/écriture pour un type personnalisé</span><span class="sxs-lookup"><span data-stu-id="0b783-118">Specifying read/write callback for custom type</span></span>

<span data-ttu-id="0b783-119">Ces attributs forcent wsutil.exe à générer le [**\_ \_ type personnalisé WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type) pour le type spécifié.</span><span class="sxs-lookup"><span data-stu-id="0b783-119">These attributes force wsutil.exe to generate [**WS\_CUSTOM\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type) for specified type.</span></span> <span data-ttu-id="0b783-120">\_l’attribut ReadCallback personnalisé spécifie la routine de [**rappel de lecture**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) et \_ le WriteCallback personnalisé spécifie la routine de [**rappel d’écriture**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) .</span><span class="sxs-lookup"><span data-stu-id="0b783-120">custom\_readcallback attribute specifies the [**read callback**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) routine, and custom\_writecallback specifies the [**write callback**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) routine.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="mytype" custom_readcallback="myreadcallback" custom_writecallback="mywritecallback"> 
 </element>
</xs:schema>
```

<span data-ttu-id="0b783-121">Nous pouvons avoir un fichier WSX correspondant pour décrire son comportement local :</span><span class="sxs-lookup"><span data-stu-id="0b783-121">We can have a matching WSX file to describe its local behavior:</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">

 <element name="FooInParam" DataValidationRoutine="MyArrayValidation">
  <complexType> 
   <element name="MyLocalArrayCount" IsCountOf="MyArray"></element> 
  </complexType>
 </element>
</xs:schema>
```

<span data-ttu-id="0b783-122">WsUtil.exe génère le prototype suivant pour la structure :</span><span class="sxs-lookup"><span data-stu-id="0b783-122">WsUtil.exe generates the following prototype for the structure:</span></span>

``` syntax
typedef struct FooInParam
{
  ULONG MyLocalArrayCount;
  int * MyArray;
};
```

 

 




