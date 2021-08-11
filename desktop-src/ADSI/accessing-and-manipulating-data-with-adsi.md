---
title: Accès et manipulation de données avec ADSI
description: Tous les objets ont des propriétés.
ms.assetid: 366a1fbc-3089-406a-9819-cf2ba7636c5f
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, accès et manipulation des données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ed09c1717f4f9a9c1c75372e7efdc23d2cce1adb39242197346061ae4df00f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181629"
---
# <a name="accessing-and-manipulating-data-with-adsi"></a>Accès et manipulation de données avec ADSI

Tous les objets ont des propriétés. Tous les objets COM de l’interface de service Active Directory (ADSI) possèdent une ou plusieurs interfaces avec des méthodes qui récupèrent les propriétés de l’objet d’annuaire représenté par l’objet COM. Vous pouvez lire les propriétés d’un objet de plusieurs façons :

-   Obtenir une propriété spécifique par nom : l’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) a deux méthodes [**IADs :: obten**](/windows/desktop/api/Iads/nf-iads-iads-get) et [**IADs :: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) pour lire une propriété spécifique. Chaque objet COM ADSI a une interface **IADs** .
-   Obtient une liste de propriétés spécifiée : l’interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) a la méthode [**IDirectoryObject :: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) qui vous permet de spécifier une liste contenant les noms des propriétés à lire et de retourner un tableau de structures contenant les valeurs de propriété demandées.
-   Énumérer toutes les propriétés de l’objet : l’interface [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) vous permet d’énumérer toutes les propriétés sur un objet.
-   Obtenir des propriétés spéciales : les interfaces d’automatisation ([**IADs**](/windows/desktop/api/Iads/nn-iads-iads) \* ) ont des méthodes de propriété qui vous permettent d’obtenir des propriétés spéciales qui ne sont pas stockées dans un objet. Ou les méthodes de propriété peuvent vous permettre d’obtenir une propriété d’objet dans un format de données qui diffère du type de données réel stocké. Par exemple, l’interface **IADs** a des méthodes de propriété telles que [**IADs :: obtenir le \_ nom**](iads-property-methods.md), qui récupère le nom unique relatif (RDN) d’un objet ; **IADs :: obtient \_ Classe**, qui récupère la classe d’un objet et **IADs :: obtenir le \_ parent**, qui récupère l’ADsPath sur le parent de l’objet.

ADSI vous permet de mettre en cache les propriétés localement après qu’elles ont été lues à partir du serveur d’annuaire. Cela vous permet de choisir de lire les propriétés à partir du cache de propriétés local ou de récupérer les propriétés directement à partir du serveur d’annuaire. ADSI possède également des méthodes pour mettre à jour le cache et spécifier si toutes les propriétés d’un objet sont mises en cache ou uniquement celles que vous avez spécifiées.

Une fois que vous avez récupéré une propriété, vous devez lire sa valeur. Le type de données d’une propriété dépend de la définition de la propriété (également appelée attribut) dans le schéma Active Directory. Pour chaque type de propriété qui peut exister dans Active Directory, il existe un objet **attributeSchema** dans le schéma Active Directory. Un objet **attributeSchema** définit les caractéristiques de l’attribut. L’une de ces caractéristiques est la syntaxe de l’attribut, qui détermine le type de données des valeurs de l’attribut. Pour plus d’informations, consultez [caractéristiques des attributs](/windows/desktop/AD/characteristics-of-attributes) et des [syntaxes pour les attributs Active Directory](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services).

Les interfaces d’automatisation ([**IADs**](/windows/desktop/api/Iads/nn-iads-iads) \* ) retournent une valeur de propriété sous la forme d’un [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) ou d’un pointeur vers une interface Automation sur un objet com qui représente la propriété. Les interfaces [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) et [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) retournent une propriété en tant que pointeur vers une structure contenant une valeur de propriété typée ou un pointeur vers une chaîne d’octets. En outre, **IDirectoryObject** et **IDirectorySearch** récupèrent les propriétés directement à partir du serveur d’annuaire au lieu d’utiliser un cache de propriétés local.

Cette section décrit les rubriques suivantes :

-   [Les interfaces IADs et IDirectoryObject](the-iads-and-idirectoryobject-interfaces.md)
-   [Accès aux attributs avec ADSI](accessing-attributes-with-adsi.md)
-   [Modification d’attributs avec ADSI](modifying-attributes-with-adsi.md)
-   [Accès au cache de propriété directement avec les interfaces IADsProperty](accessing-the-property-cache-directly-with-the-iadsproperty-interfaces.md)
-   [Syntaxe d’attribut ADSI](adsi-attribute-syntax.md)

 

 