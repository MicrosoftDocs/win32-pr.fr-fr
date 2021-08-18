---
title: Implémentation principale
description: 'Un fournisseur ADSI prend en charge les fonctionnalités suivantes :'
ms.assetid: 39798237-a181-43b4-8441-ac711f923d4d
ms.tgt_platform: multiple
keywords:
- implémentation principale d’ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78487b701cac0409745ed3a7776dd882f2c37a878dec1d144c3b52a426db487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962088"
---
# <a name="core-implementation"></a>Implémentation principale

Un fournisseur ADSI prend en charge les fonctionnalités suivantes :

-   Chaînes ADsPath à la fois dans les formats COM et URL. Par définition, vous pouvez récupérer un objet Active Directory à l’aide d’un ADsPath. Les fournisseurs prennent en charge la syntaxe requise par le service d’annuaire à l’aide de l’implémentation **ParseDisplayName** .
-   Un objet d’espace de noms de niveau supérieur qui prend en charge [**IParseDisplayName ::P arsedisplayname**](/windows/win32/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname) et [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject). Cet objet contient les nœuds racines de cet espace de noms. Une partie de l’implémentation de **ParseDisplayName** doit inclure un analyseur qui recherche les erreurs de syntaxe pour son propre espace de noms. Cet objet doit également prendre en charge [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) et **IADsOpenDSObject**.
-   Interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . Cela comprend une implémentation de cache de propriété simple via [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) et [**IADs :: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo). Les opérations qui obtiennent ou définissent des propriétés d’objet se produisent en mode mis en cache. Les valeurs de cache sont écrites dans le magasin d’annuaires sous-jacent pendant **IADs :: setinfo**. Toutefois, une méthode ADSI n’est pas mise en cache, mais s’exécute immédiatement.
-   Interfaces [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) et [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) pour accéder directement aux propriétés dans le cache de propriétés et les énumérer. Pour les services d’annuaire qui n’exposent pas de schéma, cette interface vous permet de manipuler les propriétés d’un objet.
-   Interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) pour les clients non-Automation. Cela utilise le protocole Out-The-Wire pour des performances maximales et contourne le cache de propriétés.
-   Interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) . Chaque objet Active Directory a un conteneur parent qui contrôle sa durée de vie. N’oubliez pas que pour les objets conteneur ADs, [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) affecte uniquement les propriétés de conteneur et non son contenu. SetInfo sur les objets de conteneur ADs affecte uniquement les propriétés de conteneur et n’affecte pas les objets ou objets nouvellement créés qui existent déjà dans le conteneur.
-   Interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . il s’agit de l’interface d’automatisation pour les langages tels que Visual Basic édition de script, qui n’utilisent pas la liaison au moment de la compilation. Il s’agit des données de bibliothèque de types que doit fournir un fournisseur. Pour plus d’informations, consultez [problèmes d’implémentation pour les fournisseurs ADSI](implementation-issues-for-adsi-providers.md).
-   Un objet conteneur de classe de schéma et les objets de syntaxe, de propriété et de classe de schéma appropriés qui prennent en charge respectivement [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax), [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)et [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) . Au minimum, chaque nœud racine doit contenir son propre objet conteneur de classe de schéma.
-   L’interface [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) , si des attributs pris en charge sont des collections d’objets ADSI, tels que des groupes de sécurité.
-   L’interface [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection) , si des attributs pris en charge sont des collections du même type d’élément de répertoire avec [**IADsCollection :: Add**](/windows/desktop/api/Iads/nf-iads-iadscollection-add) et [**IADsCollection :: Remove**](/windows/desktop/api/Iads/nf-iads-iadscollection-remove) , fonctionnalité.
-   L’énumération **IEnumXXXX** prend en charge tous les objets énumérateur spécifiques.
-   Routines pour mapper la syntaxe et convertir les données natives en type de données [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .
-   Suivez les conventions ADSI pour les objets ADSI fournis par le fournisseur. Incluez les fichiers d’aide et les bibliothèques de types documentant les propriétés et les méthodes de l’interface.

Comme pour toute implémentation COM, les appels à [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) doivent retourner **e \_ nointerface** pour les interfaces non implémentées, **e \_ NOTIMPL** pour les méthodes non implémentées des interfaces qui, sinon, sont implémentées et retournent la **\_ propriété e ADS \_ \_ non \_ prise en charge** pour les propriétés non implémentées. Pour plus d’informations sur les interfaces doubles et sur leur impact sur l’implémentation des propriétés, consultez [interfaces doubles](dual-interfaces.md).

 

 