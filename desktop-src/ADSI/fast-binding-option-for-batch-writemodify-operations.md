---
title: Option de liaison rapide pour les opérations d’écriture/modification par lots
description: Lorsqu’un objet de service d’annuaire est lié à, ADSI crée un objet COM qui représente l’objet d’annuaire spécifié.
ms.assetid: cf41b0c4-7459-49cf-945b-8462c7d19947
ms.tgt_platform: multiple
keywords:
- Option de liaison rapide pour les opérations d’écriture/modification par lots ADSI
- ADSI ADSI, avec l’option de liaison rapide pour les opérations d’écriture/modification par lots
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322cf3c8b5f40dc43304f95d08ff53a7c5c14217
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104508133"
---
# <a name="fast-binding-option-for-batch-writemodify-operations"></a>Option de liaison rapide pour les opérations d’écriture/modification par lots

Lorsqu’un objet de service d’annuaire est lié à, ADSI crée un objet COM qui représente l’objet d’annuaire spécifié. Lors de la liaison, ADSI récupère généralement l’attribut **objectClass** afin que l’interface ADSI puisse exposer les interfaces com appropriées pour cette classe d’objet. Par exemple, un objet utilisateur expose l’interface [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) en plus des interfaces ADSI de base prises en charge pour tous les objets. Pour une opération unique, cela ne doit avoir aucun effet sur les performances. Toutefois, si des opérations de traitement nécessitent des centaines ou des milliers de liaisons sur une connexion lente et que ces opérations écrivent des données dans le service d’annuaire, il peut être souhaitable d’échanger la prise en charge complète des objets pour une liaison plus rapide. C’est ce qu’on appelle une liaison rapide et est accompli en spécifiant l’indicateur de **\_ \_ liaison rapide ADS** quand [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) est appelé.

La liaison rapide a les restrictions suivantes :

-   L’opération de liaison doit être effectuée à l’aide de la fonction [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou de la méthode [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) . L’opération de liaison accède à nouveau au serveur d’annuaire au lieu de deux fois. ADSI ne récupère pas l’attribut **objectClass** et, par conséquent, expose uniquement les interfaces ADSI de base pour l’objet.
-   Les interfaces suivantes sont prises en charge pour l’objet COM :

    -   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
    -   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
    -   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
    -   [**Rubrique IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
    -   [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
    -   [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)
    -   [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)
    -   [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)

-   Si la méthode [**IADsContainer :: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) est utilisée pour effectuer une liaison à des objets enfants, l’objet enfant a les mêmes caractéristiques de liaison rapide que le parent.
-   L’existence de l’objet lié à n’est pas vérifiée lors de l’opération de liaison. par conséquent, les appels de méthode suivants échouent si l’objet n’existe pas. Pour cette raison, la liaison rapide doit uniquement être utilisée pour les objets connus pour exister, par exemple, directement après l’exécution d’une requête qui a retourné les noms uniques des objets en cours de liaison.
-   Les extensions ADSI sont exposées pour les objets de la classe **Top**. Par conséquent, seules les extensions pour les interfaces ADSI de base répertoriées ci-dessus sont exposées.

 

 