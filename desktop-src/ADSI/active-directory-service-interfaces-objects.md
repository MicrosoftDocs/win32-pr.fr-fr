---
title: Objets interfaces du service Active Directory
description: Le modèle objet ADSI se compose d’objets COM. Les clients manipulent des objets avec des interfaces. Les fournisseurs ADSI implémentent les objets et leurs interfaces.
ms.assetid: 3c9fd08e-47d6-4b71-8259-7c831d7d95c9
ms.tgt_platform: multiple
keywords:
- objets ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e356d9b1212b448d16bb6bba081f6141a877b0b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842722"
---
# <a name="active-directory-service-interfaces-objects"></a>Objets interfaces du service Active Directory

Le modèle objet ADSI se compose d’objets COM. Les clients manipulent des objets avec des interfaces. Les fournisseurs ADSI implémentent les objets et leurs interfaces.

Les objets ADSI sont des objets COM qui représentent un élément au sein d’un service d’annuaire : les ordinateurs, les utilisateurs, les fichiers, les serveurs, les imprimantes, les files d’attente à l’impression, etc. autrement dit, les éléments que les administrateurs réseau utilisent quotidiennement. ADSI définit différents genres d’objets pour représenter différents genres d’éléments. Chaque objet, comme illustré dans la figure suivante, prend en charge une ou plusieurs interfaces COM qui permettent l’accès aux données d’objet, souvent appelées métadonnées.

![objets des interfaces de service Active Directory](images/ds2objex.png)

Étant donné que les interfaces COM sont des ensembles de propriétés et de méthodes connectés de manière logique, vous pouvez considérer chaque interface comme un handle de l’objet qui fournit l’accès à un seul ensemble de fonctions logiques à la fois. Le tableau suivant répertorie les éléments ADSI fondamentaux.



| Interface            | Description                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IADs**             | Utilisé pour l’identification de l’objet. Comme l’interface fondamentale requise sur tous les objets ADSI, [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) fournit l’accès aux métadonnées de l’objet, y compris sa définition dans le schéma ADSI. Les IADs fournissent également l’accès aux propriétés et aux méthodes qui gèrent les données d’objet dans le cache de propriétés.                                                                                   |
| **IADsContainer**    | Utilisé pour la gestion et la détection d’objets. Tous les objets conteneurs ADSI requièrent l’interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) pour gérer la création, la suppression, la copie et le déplacement d’objets, la liaison et l’énumération.                                                                                                                                                                      |
| **IADsPropertyList** | Utilisé pour la gestion des propriétés de l’objet. L’interface [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) optimise la gestion des données d’objet dans le cache de propriétés.                                                                                                                                                                                                                                |
| **IDirectoryObject** | Utilisé pour l’accès direct aux objets. L’interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) fournit un accès aux objets de bas niveau pour les clients qui n’utilisent pas Automation. Cette interface contourne le cache des propriétés de l’objet et fournit un accès direct aux propriétés de l’objet. Pour plus d’informations, consultez [les interfaces IADs et IDirectoryObject](the-iads-and-idirectoryobject-interfaces.md). |
| **IUnknown**         | Utilisé pour la gestion des objets COM. L’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) est requise pour tous les objets com.                                                                                                                                                                                                                                                                              |
| **IDispatch**        | Utilisé pour les données de la bibliothèque de types et l’appel de méthode. L’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) est requise pour tous les objets Automation.                                                                                                                                                                                                                             |



 

Des objets ADSI plus complexes peuvent exposer des interfaces supplémentaires. Par exemple, [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection) prend en charge les méthodes qui gèrent des collections d’éléments de répertoire du même type de données. Les méthodes [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) gèrent les collections de cas spéciaux d’objets qui prennent en charge l’interface [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) . Pour les fournisseurs qui le prennent en charge, l’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) prend en charge les méthodes d’interrogation des services d’annuaire. En outre, ADSI fournit des interfaces qui représentent des éléments logiques et physiques bien connus. Par exemple, les objets ADSI qui représentent des utilisateurs prennent en charge [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), ceux qui représentent des ordinateurs qui prennent en charge [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer), etc. Pour plus d’informations sur les objets ADSI, consultez [les interfaces IADs et IDirectoryObject](the-iads-and-idirectoryobject-interfaces.md). Tous les fournisseurs n’implémentent pas toutes les interfaces ou toutes les méthodes et propriétés sur toutes les interfaces. Pour plus d’informations, consultez [référence ADSI](adsi-reference.md).

 

 