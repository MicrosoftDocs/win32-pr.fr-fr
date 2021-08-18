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
ms.openlocfilehash: f1b11e8e871399e1a499a6cfbb68a8e66b152d8f07f4fa5f2cda6585678af8e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707229"
---
# <a name="web-service-extension-file"></a>Fichier d’extension de service Web

Cette section décrit le fichier d’extension du service Web.


Le fichier WSX (extension de service WCF) est notre fichier d’extension pour permettre à l’application de manipuler les comportements locaux qui n’affectent pas la représentation des données de transmission. Il devrait être extensible que nous pouvons ajouter de nouvelles fonctionnalités à l’avenir sans interrompre l’interopérabilité.

La structure globale de WSX imiterait la structure du fichier XSD ou WSDL, qui est un fichier XML qui gère la même structure que le fichier d’entrée principal. Les attributs supplémentaires sur le même jeton nommé dans le fichier principal spécifient les attributs que l’application veut contrôler sur le comportement par défaut.

Il est possible que nous ne puissions rien faire ici dans m3. Dans v1, je peux voir que nous prenons en charge les attributs suivants :

Utilisation spécifiant l’argument ou le champ de paramètre count.

Il s’agit d’un attribut d’élément, mais applicable uniquement au type de tableau. L’attribut IsCountOf spécifie l’élément de tableau. Le champ/paramètre Count n’apparaît pas sur le câble.

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

Spécification d’un rappel de lecture/écriture pour un type personnalisé

Ces attributs forcent wsutil.exe à générer le [**\_ \_ type personnalisé WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type) pour le type spécifié. \_l’attribut ReadCallback personnalisé spécifie la routine de [**rappel de lecture**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) et \_ le WriteCallback personnalisé spécifie la routine de [**rappel d’écriture**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) .

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="mytype" custom_readcallback="myreadcallback" custom_writecallback="mywritecallback"> 
 </element>
</xs:schema>
```

Nous pouvons avoir un fichier WSX correspondant pour décrire son comportement local :

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

WsUtil.exe génère le prototype suivant pour la structure :

``` syntax
typedef struct FooInParam
{
  ULONG MyLocalArrayCount;
  int * MyArray;
};
```

 

 




