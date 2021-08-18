---
title: Accès au cache des propriétés avec des interfaces IADsProperty
description: Les interfaces IADsProperty se composent de IADsPropertyList, IADsPropertyEntry et IADsPropertyValue.
ms.assetid: ff15eb50-01ab-4b45-bcfd-1df01172f274
ms.tgt_platform: multiple
keywords:
- Accès au cache de propriété directement avec l’interface ADSI des interfaces IADsProperty
- interface ADSI du cache de propriétés
- interface ADSI du cache de propriétés, utilisant des interfaces IADsProperty pour accéder au cache de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a68cd77a10d6631b52e48ed19650dd5cd18dff0ee59ba2332db73b7fce1a8bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024117"
---
# <a name="accessing-property-cache-with-iadsproperty-interfaces"></a>Accès au cache des propriétés avec des interfaces IADsProperty

Les interfaces [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) se composent de [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)et [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue). Ces interfaces fournissent des méthodes pour accéder directement aux propriétés d’un cache d’objets et les manipuler. Une propriété est connue comme une entrée de propriété et correspond à un attribut défini dans le schéma. Une entrée de propriété peut avoir une ou plusieurs valeurs de propriété. Un ensemble d’entrées de propriété est organisé comme une liste de propriétés.

L’interface [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) gère la liste des propriétés d’un objet ADSI. L’interface [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) effectue cette opération pour une entrée de propriété. De même, l’interface [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) représente une ou plusieurs valeurs de propriété. Ensemble, ils fournissent un mécanisme permettant aux utilisateurs d’effectuer les opérations suivantes :

-   Travaillez directement avec le cache de propriétés.
-   Utilisez des répertoires qui ne contiennent pas de schémas, tels qu’un serveur LDAP version 2.

Les interfaces [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) \* fonctionnent strictement dans le cache de propriétés et n’effectuent aucune tentative de collaboration avec le serveur pour récupérer ou modifier les données dans le magasin persistant. Par conséquent, ces interfaces sont utilisées uniquement pour examiner et manipuler des propriétés dans le cache du client. Avant d’utiliser ces interfaces, vous devez appeler la méthode [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) ou la méthode [**IADs :: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) explicitement pour charger les propriétés de l’objet dans le cache, si le cache n’a pas été initialisé. Après avoir appelé les méthodes de ces interfaces, vous devez appeler [**IADs :: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) pour conserver les modifications dans le magasin d’annuaires sous-jacent.

Pour plus d’informations et pour obtenir un exemple de code qui peut être utilisé pour implémenter ces interfaces, consultez l' [exemple de code permettant d’utiliser des interfaces IADsProperty pour accéder au cache de propriétés](example-code-for-using-iadsproperty-interfaces-to-access-the-property-cache.md).

 

 




