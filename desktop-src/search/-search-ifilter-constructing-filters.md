---
description: Il est important de comprendre la structure de DLL requise d’un gestionnaire de filtres (une implémentation de l’interface IFilter).
ms.assetid: a2b5a813-573a-44d3-8780-99603e3246c1
title: Implémentation de gestionnaires de filtres dans Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5f326440b31b62ff5697274962f4d4a2cfe7c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515214"
---
# <a name="implementing-filter-handlers-in-windows-search"></a>Implémentation de gestionnaires de filtres dans Windows Search

Il est important de comprendre la structure de DLL requise d’un gestionnaire de filtres (une implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ).

Cette rubrique est organisée comme suit :

- [Implémentation et exportation des points d’entrée de DLL](#implementing-and-exporting-the-dll-entry-points)
- [Implémentation de la classe IFilter et de la fabrique de classes](#implementing-the-ifilter-class-and-class-factory)
- [Héritage des interfaces COM](#inheriting-the-com-interfaces)
- [Implémentation des méthodes de l’interface COM](#implementing-the-com-interface-methods)
  - [Méthodes COM non implémentées](#com-methods-that-are-not-implemented)
- [Ressources supplémentaires](#additional-resources)
- [Rubriques connexes](#related-topics)

## <a name="implementing-and-exporting-the-dll-entry-points"></a>Implémentation et exportation des points d’entrée de DLL

Chaque dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) (dénotée par Ifilter.dll dans cette section) doit implémenter et exporter les points d’entrée suivants. Ces points d’entrée sont généralement exportés à l’aide d’un fichier de définition de module (. def) pour l’interface **IFilter** ou à l’aide du mot clé **\_ \_ declspec (dllexport)** . Le fichier DLL peut être inscrit dans n’importe quel dossier, mais il se trouve généralement dans le dossier% SystemRoot% \\ system32.

Les points d’entrée de DLL sont répertoriés et décrits dans le tableau suivant.

| Nom de la DLL                                                                                     | Description de la DLL                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Accompli](/windows/win32/api/olectl/nf-olectl-dllregisterserver)            | Le point d’entrée [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) inscrit la dll en tant que filtre dans le registre. Vous inscrivez la DLL en exécutant le programme regsvr32.exe avec le nom de fichier DLL de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) en tant qu’argument : `regsvr32.exe %SystemRoot%\system32\Ifilter.dll`                                              |
| [Fonction DllUnregisterServer](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) | Le point d’entrée de la [fonction DllUnregisterServer](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) supprime la dll en tant que gestionnaire persistant dans le registre. Pour annuler l’inscription de la DLL, exécutez le programme regsvr32.exe avec l' `/u` indicateur : `regsvr32.exe /u %SystemRoot%\system32\Ifilter.dll`                                                                                    |
| [DllGetClassObject, fonction](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)   | Le client d’indexation de contenu appelle le point d’entrée de la [fonction DllGetClassObject](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) , par le biais du modèle COM (Component Object Model), pour créer un objet de fabrique de classes pour l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) et obtenir un pointeur vers l’interface de fabrique de classes de cet objet.                                               |
| [DllCanUnloadNow, fonction](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)     | Le client d’indexation de contenu appelle le point d’entrée de la [fonction DllCanUnloadNow](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) via com pour déterminer s’il est possible de décharger la dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  . L’interface **IFilter** est déchargée une fois qu’elle est inutilisée pendant un intervalle de temps, comme spécifié par la valeur de Registre FilterIdleTimeOut. |

## <a name="implementing-the-ifilter-class-and-class-factory"></a>Implémentation de la classe IFilter et de la fabrique de classes

Au moins deux classes, telles que CFilter et CFilterCF, sont généralement implémentées par chaque dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . La classe CFilter produit l’objet interface **IFilter** qui implémente la fonctionnalité de filtrage de contenu. Ses fonctions membres implémentent les méthodes d’interface de l’interface **IFilter** . Chaque classe **IFilter** requiert un identificateur de classe unique (CLSID), généré par l’implémentation de l’interface **IFilter** .

La classe CFilterCF produit l’objet de fabrique de classe pour l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . La fabrique de classes est appelée, via son interface d' [interface IClassFactory](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) , par le point d’entrée de la [fonction DLLGETCLASSOBJECT](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) de la dll. La classe CFilterCF crée l’objet CFilter et retourne un pointeur vers [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown). Dans les cas plus complexes, un **IFilter** peut implémenter une hiérarchie de classes à la place de la classe cfilter unique.

## <a name="inheriting-the-com-interfaces"></a>Héritage des interfaces COM

Windows Search 3,0 et versions ultérieures requièrent que vous utilisiez [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) pour les raisons suivantes :

- Pour garantir les performances et la compatibilité future.
- Pour renforcer la sécurité. Les IFilters implémentés avec [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) sont plus sécurisées, car le contexte dans lequel l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) s’exécute n’a pas besoin des droits pour ouvrir des fichiers sur le disque ou sur le réseau.
- Alors que Windows Search utilise uniquement [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), la classe d’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) peut également hériter de l' [interface IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) et/ou des implémentations de l’interface d’interface [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) pour la compatibilité descendante.

Ces interfaces sont déclarées dans des fichiers inclus dans le \\ répertoire include Mssdk et ont des identificateurs d’interface prédéfinis (IID). Le client d’indexation du contenu interroge l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) via [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) pour déterminer les interfaces à utiliser lors du filtrage du contenu.

## <a name="implementing-the-com-interface-methods"></a>Implémentation des méthodes de l’interface COM

L’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) implémente les méthodes [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) pour la classe d’interface **IFilter** et la fabrique de classe d’interface **IFilter** . Le tableau suivant répertorie, dans l’ordre vtable, les interfaces et les méthodes spécifiques à l’interface **IFilter** que l’interface **IFilter** doit implémenter. L’interface **IFilter** doit implémenter au moins [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), mais peut implémenter des interfaces supplémentaires dérivées de IPersist.

| Interface COM                                                                             | Méthode                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IClassFactory, interface](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)   | CreateInstance, LockServer,                                                                                                                                                                                                                                                     |
| [Interface IClassFactory2](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2)  | GetLicInfo, RequestLicKey, CreateInstanceLic                                                                                                                                                                                                                                   |
| [**Filtres**](/windows/win32/api/filter/nn-filter-ifilter)                                                        | [**IFilter :: init**](/windows/win32/api/filter/nf-filter-ifilter-init), [**IFilter :: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk), [**IFilter :: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext), [**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue), [**IFilter :: BindRegion**](/windows/win32/api/filter/nf-filter-ifilter-bindregion) |
| [Interface IPersist](/windows/desktop/api/objidl/nn-objidl-ipersist)               | GetClassID                                                                                                                                                                                                                                                                     |
| [IPersistFile, interface](/windows/win32/api/objidl/nn-objidl-ipersistfile)    | IsDirty, Load, Save, SaveCompleted, GetCurFile                                                                                                                                                                                                                                 |
| [IPersistStorage, interface](/windows/win32/api/objidl/nn-objidl-ipersiststorage) | IsDirty, charger, enregistrer, GetSizeMax                                                                                                                                                                                                                                                |
| [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)            | IsDirty, charger, enregistrer, GetSizeMax                                                                                                                                                                                                                                                |

La page de référence de chaque méthode spécifie les paramètres et le comportement fonctionnel de cette méthode. Chaque page de référence donne également les codes de résultat à implémenter pour cette méthode. Les pages de référence pour les méthodes [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) fournissent les codes spécifiques à l’interface dans les codes de résultats [ \_ ITF d’installation](../com/codes-in-facility-itf.md) à implémenter, et le client d’indexation du contenu peut également gérer tous les codes de résultat génériques, tels que la valeur null de l’installation \_ et la fonction \_ Win32. Pour plus d’informations, consultez [structure of com Error Codes](../com/structure-of-com-error-codes.md).

### <a name="com-methods-that-are-not-implemented"></a>Méthodes COM non implémentées

L’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) doit implémenter au moins [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), mais elle n’a pas besoin d’implémenter des interfaces dérivées de IPersist supplémentaires.

Windows Search n’a pas besoin d’implémenter les méthodes COM listées dans le tableau suivant.

| Méthode non requise                               | Description                       |
|-----------------------------------------------------------|-----------------------------------|
| IPersistStream :: IsDirty                                   | Les filtres doivent retourner E \_ NOTIMPL. |
| IPersistStream :: Save                                      | Les filtres doivent retourner E \_ NOTIMPL. |
| IPersistStream :: GetSizeMax                                | Les filtres doivent retourner E \_ NOTIMPL. |
| [**IFilter :: BindRegion**](/windows/win32/api/filter/nf-filter-ifilter-bindregion) | Les filtres doivent retourner E \_ NOTIMPL. |

## <a name="additional-resources"></a>Ressources supplémentaires

- L’exemple de code [IFilterSample](-search-sample-ifiltersample.md) , disponible sur [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), montre comment créer une classe de base IFilter pour l’implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Pour obtenir une vue d’ensemble du processus d’indexation, consultez [processus d’indexation](-search-indexing-process-overview.md).
- Pour obtenir une vue d’ensemble des types de fichiers, consultez [types de fichiers](../shell/fa-file-types.md).
- Pour interroger des attributs d’association de fichiers pour un type de fichier, consultez [PerceivedTypes, SystemFileAssociations et inscription d’application](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Rubriques connexes

[Développement de gestionnaires de filtres](-search-ifilter-conceptual.md)

[Fonctionnement des gestionnaires de filtres dans la recherche Windows](-search-ifilter-about.md)

[Meilleures pratiques pour la création de gestionnaires de filtres dans Windows Search](-search-3x-wds-extidx-filters.md)

[Retour des propriétés d’un gestionnaire de filtres](-search-ifilter-property-filtering.md)

[Gestionnaires de filtres fournis avec Windows](-search-ifilter-implementations.md)

[Inscription des gestionnaires de filtres](-search-ifilter-registering-filters.md)

[Test des gestionnaires de filtres](-search-ifilter-testing-filters.md)
