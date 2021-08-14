---
title: Liaison à un objet Active Directory
description: La méthode la plus courante pour effectuer une liaison à un objet Active Directory consiste à utiliser la fonction GetObject entre un client ADSI et un fournisseur ADSI.
ms.assetid: d278ea26-2fd5-4343-8d87-ff85515325fb
ms.tgt_platform: multiple
keywords:
- Liaison à un objet Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc788ed9eb124e1da6c21848f02393d46608f00dd3a9e779788fa54429922400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429131"
---
# <a name="binding-to-an-active-directory-object"></a>Liaison à un objet Active Directory

La méthode la plus courante pour effectuer une liaison à un objet Active Directory consiste à utiliser la fonction **GetObject** entre un client ADSI et un fournisseur ADSI. Il s’agit également du moyen le plus simple pour montrer comment le composant fournisseur reçoit les requêtes et les services. la fonction d’API ADSI [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) ou la fonction Visual Basic **GetObject** suivent les mêmes étapes pour la liaison.

Pour cet exemple, supposons que le client ADSI est une application de la visionneuse ADSI qui a reçu l’ADsPath « Sample://Seattle/Redmond/Shelly » de son interface utilisateur (1). La figure suivante détaille la séquence d’événements en numérotant les flèches de Flow.

![vue détaillée des composants ADSI](images/dscsex.png)

Dans l’illustration précédente, le client lance la demande d’un pointeur d’interface sur l’objet Active Directory représenté par l’ADsPath « Sample://Seattle/Redmond/Shelly » à partir des services ADSI (2). Pendant l’initialisation, le logiciel de services a rempli une table des identificateurs programmatiques (ProgID) du fournisseur installés à partir du Registre (« LDAP : », « Sample : », « Winnt : », etc.) et les a associés au **CLSID** correspondant qui identifient le module logiciel approprié.

Le serveur ADSI vérifie que le ProgID, dans le cas présent « Sample : », existe dans le ADsPath. Il crée ensuite un contexte de liaison pour optimiser les références supplémentaires à cet objet, et appelle la fonction COM standard [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) pour créer un moniker com qui peut être utilisé pour rechercher et effectuer une liaison à l’objet qui représente l’utilisateur « Shelly ».

Dans la section suivante, les noms de fichiers de l’exemple de code source du composant fournisseur sont inclus entre parenthèses, le cas échéant.

Comme dans d’autres implémentations de serveur COM, [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) examine le ProgID et recherche le **CLSID** approprié dans le registre (3) pour rechercher le code de fabrique de classe (Cprovcf. cpp) fourni par le fournisseur correspondant dans l’implémentation de fournisseur appropriée (4). Ce code crée un objet de niveau supérieur initial qui implémente la méthode [**IParseDisplayName ::P arsedisplayname**](/windows/win32/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname) (Cprov. cpp). L’implémentation du fournisseur de **ParseDisplayName** résout le chemin d’accès dans le propre espace de noms du fournisseur. Cela appelle ensuite ADsObject et appelle l’analyseur fourni avec le composant fournisseur (Parse. cpp) pour vérifier que l’ADsPath est syntaxiquement correct pour cet espace de noms.

**GetObject**, qui est défini dans Getobj. cpp, détermine si l’objet demandé est un objet d’espace de noms, un objet de schéma ou un autre type d’objet. Si l’un des deux premiers, ce type d’objet de classe de schéma est créé et le pointeur d’interface approprié a été récupéré. Dans le cas contraire, le chemin d’accès de l’exemple de répertoire est créé à partir de l’ADsPath (par exemple, « \\ Seattle \\ Redmond \\ Shelly », mais dans un autre service d’annuaire, il peut s’agir de « \\ ou = Seattle \\ ou = Redmond \\ CN = Shelly ») et le contrôle passe à SampleDSOpenObject qui ouvre l’objet dans l’exemple de stockage de données et récupère également son type d’objet

Une fois les données collectées, un nouvel objet est créé (6) pour représenter l’élément décrit par l’ADsPath, et un pointeur vers l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) sur cet objet est récupéré. Dans ce cas, un objet Active Directory générique est créé et prend en charge les méthodes **IUnknown** et [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) (Cgenobj. cpp, Core. cpp). La routine CSampleDSGenObject :: AllocateGenObject lit les données de la bibliothèque de types pour créer les entrées de dispatch appropriées pour ces nouveaux objets afin de prendre en charge [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).

L’encapsulation de ce pointeur d’interface dans un moniker termine la fonction ResolvePathName (Cprov. cpp) et analyse le nom complet.

Tous les objets COM créés pendant ce processus sont mis en cache pour des raisons de performances et gérés par le contexte de liaison. Cela améliore les performances d’autres opérations sur le même objet qui suit immédiatement la liaison de moniker.

Cet objet Active Directory correctement construit est désormais interrogé pour l’identificateur d’interface demandé pour l’appel initial [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) et un pointeur vers cette interface est récupéré (7) et transmis par le serveur ADSI au client (8&9). À partir de là, le client fonctionne directement avec le composant fournisseur via les méthodes d’interface jusqu’à ce que la demande initiale soit satisfaite (10).

En outre, les demandes de données d’objet provenant du client prennent généralement la forme de requêtes pour les acquisitions et les acquisitions de propriétés, toutes optimisées par le biais de l’implémentation du fournisseur d’un cache de propriétés (cProps. cpp). La compression et la décompression intelligentes des données, notamment la copie et la libération de structures et de chaînes, entre les types de données natifs sur le système d’exploitation de l’exemple de composant fournisseur et le type [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) Automation pris en charge par ADSI ont lieu avant le chargement des propriétés dans le cache (Smpoper. cpp).

L’exemple de composant fournisseur est conçu de sorte que les appels réels au système d’exploitation soient logiquement isolés du composant fournisseur, créant ainsi un logiciel portable pour plusieurs systèmes d’exploitation (RegDSAPI. cpp).

 

 