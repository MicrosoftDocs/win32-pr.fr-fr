---
title: Problèmes d’implémentation pour les fournisseurs ADSI
description: Problèmes d’implémentation pour les fournisseurs ADSI
ms.assetid: 0be772aa-e7d8-4d34-b55a-162abfb0bfd4
ms.tgt_platform: multiple
keywords:
- Problèmes d’implémentation pour les fournisseurs ADSI ADSI
- fournisseurs ADSI, implémenter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c362b04244580e448e7bb7bd78889e66db12fe
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382876"
---
# <a name="implementation-issues-for-adsi-providers"></a>Problèmes d’implémentation pour les fournisseurs ADSI

Pour implémenter des interfaces ADSI, commencez par implémenter l’interface COM [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). En fournissant cette interface comme couche de surcharge minimale, vous fournissez aux applications clientes le contrôle requis pour accéder aux objets d’annuaire directement à partir de l’annuaire plutôt que via le cache ADSI, ce qui optimise les performances du réseau. L’utilisation de cette interface fournira également votre propre implémentation avec la plus grande flexibilité.

Ensuite, implémentez les interfaces ADSI fondamentales, [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection)et les interfaces du cache de propriétés [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry), [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) . [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) et [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) sont également des interfaces fréquemment sollicitées par les logiciels d’administration de système.

Troisièmement, implémentez les interfaces de gestion de schéma si votre service d’annuaire a un schéma sous-jacent : [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty), [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax). S’il n’existe pas de schéma sous-jacent, utilisez ces interfaces pour extraire les classes et les propriétés utilisées par le service d’annuaire. Les schémas peuvent être utilisés pour publier les fonctionnalités de votre service d’annuaire sur les clients ADSI.

## <a name="collections"></a>Regroupements

Les composants du fournisseur ADSI peuvent suivre l’un des trois modèles pour la mise en cache des collections pendant l’énumération. Le choix d’un modèle de mise en cache détermine le comportement d’ADSI lorsqu’un objet d’une collection est supprimé du service d’annuaire sous-jacent externe à ADSI.

Les modèles de mise en cache sont les suivants :

-   Collections mises en cache à l’avance. La collection d’instances d’objet est récupérée à partir du service d’annuaire sous-jacent dans son intégralité quand [**IADsCollection :: obtenir \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscollection-get__newenum) est appelé pour créer un nouvel objet énumérateur. Si l’objet source d’une instance d’objet Active Directory dans la collection Récupérée est supprimé du service d’annuaire sous-jacent, le client ne reconnaît pas la suppression tant qu’un [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) ou [**IADs :: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) ne tente pas d’accéder à la collection.
-   Collections mises en cache de façon incrémentielle. La collection est récupérée à partir du service d’annuaire sous-jacent, un objet à la fois lorsque [**IEnumVARIANT :: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) est appelé. [**IEnumVARIANT :: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) retourne au début de la collection dans le cache et **IEnumVARIANT :: Next** retourne les objets mis en cache jusqu’à ce que la fin du cache soit atteinte. les nouveaux objets sont alors ajoutés à partir du magasin sous-jacent. Lorsqu’une instance d’objet Active Directory se trouve dans le cache, le client ne prend pas connaissance de sa suppression du service d’annuaire sous-jacent jusqu’à ce qu’un [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) ou [**IADs :: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) tente d’accéder à l’objet.
-   Collections non mises en cache. La collection est récupérée à partir du service d’annuaire sous-jacent, un objet à la fois lorsque [**IEnumVARIANT :: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) est appelé. [**IEnumVARIANT :: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) retourne au début de la collection dans le magasin sous-jacent. **IEnumVARIANT :: Next** et **IEnumVARIANT :: Reset** Operations ne peuvent pas récupérer les objets supprimés, car les objets sont récupérés à la demande à partir du service d’annuaire sous-jacent. Seul l’objet actuel est mis en cache ; Si l’objet actuel est supprimé, le client ne prend pas connaissance de sa suppression du service d’annuaire sous-jacent jusqu’à ce qu’un [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) ou [**IADs :: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) tente d’accéder à l’objet.

Quel que soit le modèle de mise en cache, sachez que l’énumération ADSI retourne Active Directory interfaces de service à l’appelant. Pour éviter la surcharge liée à l’obtention d’un nouveau pointeur d’interface, les applications ADSI doivent mettre en cache les pointeurs d’interface renvoyés pour les objets qu’ils envisagent de manipuler. Par exemple, une Visual Basic application qui énumère un conteneur et remplit une zone de liste avec des noms peut mettre en cache les pointeurs d’interface associés aux noms pour une utilisation ultérieure. Cette approche offre de meilleures performances que le remplissage de la zone de liste pendant l’énumération et l’obtention d’un nouveau pointeur d’interface lorsque l’utilisateur effectue une sélection.

## <a name="about-dispatch-ids"></a>À propos des ID de dispatch

[**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) est une interface d’automatisation définie par com pour les contrôleurs qui n’utilisent pas directement les interfaces com. L’accès à un objet via **IDispatch** est appelé accès lié au nom ou à liaison tardive, car il se produit au moment de l’exécution (« tardif ») et utilise des noms de chaîne de propriétés et de méthodes pour résoudre les références (« Name »). Au moment de l’exécution, les clients transmettent le nom de chaîne de la propriété ou de la méthode qu’ils souhaitent appeler dans la méthode [**IDispatch :: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames)(). Si la propriété ou la méthode existe sur l’objet, l’identificateur de dispatch (dispID) de la fonction correspondante est récupéré. Le dispID est ensuite utilisé pour exécuter la fonction par le biais de [**IDispatch :: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke)(). L’utilisation de **IDispatch**, les propriétés et les méthodes sur les interfaces exposées par un objet unique s’affichent sous la forme d’une liste plate. Étant donné que l’accès lié au nom requiert deux appels de fonction, il est moins efficace que l’utilisation directe d’une interface COM. Les clients sont encouragés à utiliser les interfaces COM ADSI sur les objets lorsque les performances sont à prendre en compte. Les contrôleurs Automation avancés tels que Visual Basic 4,0 peuvent appeler d’autres interfaces COM et **IDispatch**, si les interfaces sont conformes aux contraintes d’automatisation pour les types de données et le passage de paramètres.

Les fournisseurs ADSI génèrent des DISPID de manière dynamique pour chaque objet Active Directory. Les DISPID récupérés par le biais de [**IDispatch :: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) pour un objet donné sont les valeurs générées, mais pas les valeurs qui se trouvent dans le IDL de l’objet. Les utilisateurs [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) doivent appeler **GetIDsOfNames** pour obtenir des DISPID valides au moment de l’exécution.

## <a name="type-information-and-type-libraries"></a>Informations de type et bibliothèques de types

Le kit de développement logiciel (SDK) ADSI fournit une bibliothèque de types, activeds. tlb, qui documente toutes les interfaces standard prises en charge par ADSI. Un fournisseur doit fournir une bibliothèque de types similaire pour toutes les interfaces trouvées dans activeds. tlb, ainsi que toutes les données de type supplémentaires pour les interfaces implémentées dans le composant du fournisseur.

Voici un exemple de code IDL.

``` syntax
[ object, uuid(IID_IADsXYZ), oleautomation, dual ]
interface IADsXYZ: IDispatch
{
// Read-only properties.
[propget]
HRESULT AReadOnlyProp ([out, retval]BSTR *pbstrAReadOnlyProp);
 
// Read/write properties.
[propget]
HRESULT AReadWriteProp ([out, retval]long *plAReadWriteProp);
[propput]
HRESULT AReadWriteProp ([in]long lAReadWriteProp);
 
// Methods.
HRESULT AMethod ([in]DATE dateInParameter,
[out, retval]BSTR *pbstrReturnValue);
};
```

## <a name="thread-safety"></a>Cohérence de thread

Le modèle COM (Component Object Model) décrit les trois modèles de threads suivants. Les applications COM indiquent quel modèle est en cours d’utilisation lors de l’initialisation de la bibliothèque COM à l’aide des fonctions [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) et [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) :

-   Thread unique. Le modèle à thread unique suppose un seul thread d’exécution dans un processus, en supposant que les structures de données COM d’un processus n’ont pas besoin de sérialisation d’accès.
-   Threads cloisonnés. Un objet COM est associé au thread qui l’a créé. Les appels à un objet sur un autre thread doivent être exécutés par le thread qui a créé cet objet. Pour ce faire, le thread source appelle un proxy client qui organise l’appel de méthode et le remet à une fonction de stub serveur dans le thread de destination via la file d’attente de messages Win32 associée au thread de destination.
-   Threading libre. Les objets COM sont supposés être thread-safe. Plusieurs threads sont autorisés à accéder à n’importe quel objet dans le processus sans aucune sérialisation imposée.

ADSI ne prend pas en part un modèle de thread particulier. Les rédacteurs des composants fournisseurs doivent assumer le modèle de thread libre et garantir la cohérence de leurs structures de données internes en les protégeant des threads non sécurisés, c’est-à-dire, des mises à jour non coordonnées via l’utilisation d’objets de synchronisation, tels que des sections critiques ou des sémaphores.

## <a name="object-locking"></a>Verrouillage d’objet

ADSI n’impose pas ou ne définit pas de schéma de verrouillage d’objets. Les fournisseurs pour les espaces de noms qui prennent en charge la sérialisation de l’accès à l’aide du verrouillage peuvent exposer le schéma de verrouillage sous-jacent via des extensions spécifiques du fournisseur à ADSI.

## <a name="property-names-within-a-schema"></a>Noms de propriétés dans un schéma

ADSI représente des propriétés en tant qu’objets de propriété dans le conteneur de schéma ADSI. Cela requiert que les noms de propriété soient uniques dans chaque conteneur de schéma. Le fournisseur doit s’assurer qu’il n’y a pas de collisions de noms.

## <a name="primary-interface"></a>Interface principale

Lorsqu’un fournisseur ne peut pas identifier l’interface qui doit être retournée en tant qu’interface principale, les **\_ IAD IID** doivent être retournées. Cela fournit un accès lié au nom à toutes les propriétés d’un objet via [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) et les méthodes [**IADs :: obten**](/windows/desktop/api/Iads/nf-iads-iads-get), [**IADs :: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**iads ::P ut**](/windows/desktop/api/Iads/nf-iads-iads-put)et [**IADs ::P Utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) .

 

 