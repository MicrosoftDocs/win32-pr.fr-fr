---
title: Utilisation des interfaces IADs
description: ADSI, chaque élément d’un service d’annuaire est représenté par un objet ADSI, qui est un objet COM (Component Object Model) qui prend en charge l’interface IUnknown COM standard, ainsi que les interfaces IDispatch et IADs.
ms.assetid: bdbf2012-6863-4611-8173-6a3cd9c4960f
ms.tgt_platform: multiple
keywords:
- IADs ADSI, utilisation
- ADSI ADSI, utilisation de, à l’aide des interfaces IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9759833e538292c6d6f472b05448d197a88164fadbb2ea2df64c4fe48669f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637507"
---
# <a name="using-the-iads-interfaces"></a>Utilisation des interfaces IADs

ADSI, chaque élément d’un service d’annuaire est représenté par un objet ADSI, qui est un objet COM (Component Object Model) qui prend en charge l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) com standard, ainsi que les interfaces [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) et [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . **IADs** fournit les fonctions de maintenance de base pour les objets ADSI.

Chaque objet ADSI doit prendre en charge cette interface, qui sert à :

-   Indiquez l’identification de l’objet par nom, classe ou ADsPath.
-   Identifiez le conteneur d’objets qui gère la création et la suppression d’objets.
-   Obtenez la définition du schéma de l’objet.
-   Chargez les attributs d’objet dans le cache de propriétés et validez les modifications dans le magasin d’annuaires persistant.
-   Accédez aux valeurs d’attribut d’objet dans le cache de propriétés et modifiez-les.

L’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) est conçue pour garantir que les objets ADSI fournissent aux administrateurs réseau et aux fournisseurs de services d’annuaire une représentation efficace et cohérente de différents services d’annuaire sous-jacents.

![objet ADSI prenant en charge l’interface IADs](images/ds2iads.png)

La figure précédente montre un objet ADSI générique qui prend en charge les interfaces fondamentales [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)et [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch). Un objet ADSI, tel que celui-ci, gère des données à partir du magasin de données du service d’annuaire sous-jacent via les interfaces qu’il prend en charge. Ces données sont connues comme les propriétés de l’objet, et les routines qui obtiennent et définissent ces propriétés sont appelées méthodes de propriété. Les propriétés en lecture seule ont une méthode de propriété qui obtient la valeur de la propriété. Les propriétés en lecture/écriture ont deux méthodes : méthode qui définit la valeur et une qui obtient la valeur. Les propriétés sont implémentées sur chaque objet ADSI à l’aide d’un [cache de propriétés](the-adsi-attribute-cache.md). [**IADs :: obtient \_ ADsPath**](iads-property-methods.md) et **IADs ::p ut \_ ADsPath** sont des exemples de méthodes de propriété. les méthodes de propriété ne sont pas visibles pour Visual Basic et d’autres clients Automation qui activent des références directes à la propriété. par exemple, Visual Basic fait référence à **IADs :: adspath** directement à l’aide de la syntaxe **Object. ADsPath** . Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).

En outre, un objet ADSI interagit avec d’autres objets ADSI et directement à un espace de noms via des méthodes. Les méthodes s’exécutent immédiatement. Les exemples de méthodes sont les suivants [**: IADs :: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) et [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).

Les propriétés, les méthodes de propriété et les méthodes sont accessibles via des interfaces COM standard.

Un objet ADSI est identifié de manière unique par son ADsPath. Par exemple, un ADsPath pour l’espace de noms LDAP est « LDAP://MyServer/DC=Fabrikam,DC=COM ». Pour plus d’informations sur ADsPaths, consultez [liaison ADSI](binding-to-an-adsi-object.md). Pour les programmeurs familiers avec les monikers COM, ce concept est similaire au nom complet du moniker COM.

Tout objet ADSI qui contient d’autres objets ADSI, appelé objet conteneur ADSI, prend également en charge l’interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) , qui fournit des méthodes et des propriétés qui gèrent la création, la suppression et l’énumération des objets ADSI contenus dans l’objet. L’illustration suivante montre un objet conteneur ADSI.

![objet conteneur ADSI](images/dsiadsc.png)

La plupart des objets ADSI sont contenus dans d’autres objets. Le seul objet ADSI sans conteneur parent est l’objet des **espaces de noms** ADSI de niveau supérieur (« ADS : »).

La méthode [**IADs :: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) sur un objet conteneur stocke de manière permanente les propriétés mises en cache de l’objet conteneur ADSI dans le stockage, en plus des objets créés avec la méthode [**IADsContainer :: Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) . [**IADsContainer ::D supprim**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete) n’affecte pas le cache de propriétés, mais supprime l’élément de répertoire d’espace de noms sous-jacent représenté par cet objet.

 

 