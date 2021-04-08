---
description: Le modèle CIM (Common Information Model) est un modèle de données extensible et orienté objet qui contient des informations sur différentes parties d’une entreprise.
ms.assetid: 3e619cb7-18a9-40ff-82fe-c10eb5090a93
ms.tgt_platform: multiple
title: Common Information Model (CIM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53e4e2dc06e03a1f19b5b47ba0b94d7a866a5e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034937"
---
# <a name="common-information-model"></a>Common Information Model (CIM)

Le modèle CIM (Common Information Model) est un modèle de données extensible et orienté objet qui contient des informations sur différentes parties d’une entreprise. Le [modèle CIM](https://www.dmtf.org/standards/cim) est une norme multiplateforme gérée par Distributed Management Task Force ([DMTF](https://www.dmtf.org/)). Via WMI, un développeur peut utiliser le modèle CIM pour créer des classes qui représentent les lecteurs de disque dur, les applications, les routeurs réseau et même des technologies définies par l’utilisateur, par exemple des climatiseurs réseau. En affichant et en modifiant une classe CIM, un responsable peut contrôler différents aspects de l’entreprise. Par exemple, il peut interroger une instance de classe CIM représentant une station de travail de bureau. Il peut ensuite exécuter un script pour modifier l’instance de station de travail CIM. WMI traduit les modifications apportées à l’instance de classe CIM de la station de travail en modifications de la station de travail.

Le modèle CIM est un modèle de programmation indépendant du langage qui utilise des techniques orientées objet pour décrire une entreprise. À l’aide de trois niveaux d’héritage parent/enfant, le modèle CIM peut décrire des aspects généraux et spécifiques d’une entreprise. Le CIM utilise également une technique appelée « Association » pour lier différentes parties du modèle d’entreprise et utilise des schémas pour distinguer différents environnements de gestion.

Le modèle CIM est conçu pour présenter une vue cohérente des objets logiques et physiques dans un environnement de gestion. Le CIM représente des objets managés à l’aide d’une construction orientée objet appelée « classe ». À l’instar d’une classe C++ ou COM, une classe CIM peut inclure des propriétés pour décrire des données et des méthodes pour décrire le comportement. À l’instar d’un ensemble de classes COM, le CIM n’est lié à aucune plate-forme. Toutefois, WMI comprend une extension du modèle CIM qui décrit les plateformes du système d’exploitation Microsoft Windows.

Le CIM définit trois niveaux de classes :

-   Core

    Les classes principales représentent des objets managés qui s’appliquent à toutes les zones de gestion. Ces classes fournissent un vocabulaire de base pour l’analyse et la description des systèmes gérés. Les classes [**\_ \_ Parameters**](--parameters.md) et [**\_ \_ SystemSecurity**](--systemsecurity.md) sont des exemples de classes principales.

-   Courant

    Les classes communes représentent des objets managés qui s’appliquent à des zones de gestion spécifiques. Toutefois, les classes communes sont indépendantes d’une implémentation ou d’une technologie particulière. Les classes courantes sont une extension des classes principales. La classe [**CIM \_ UnitaryComputerSystem**](/windows/desktop/CIMWin32Prov/cim-unitarycomputersystem) est un exemple de classe commune.

-   Étendu

    Les classes étendues représentent des objets managés qui sont des ajouts spécifiques à la technologie aux classes communes. Une classe étendue s’applique généralement à une plateforme spécifique, telle qu’UNIX ou l’environnement Microsoft Win32. La classe [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) est un exemple de classe étendue.

Un développeur peut dériver une classe d’une autre classe. Une classe dérivée représente un cas spécial de la classe parente et hérite de toutes les propriétés et méthodes du parent. Par exemple, [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) hérite de [**CIM \_ UnitaryComputerSystem**](/windows/desktop/CIMWin32Prov/cim-unitarycomputersystem). Les relations d’héritage peuvent être déterminées à l’aide des propriétés système **\_ \_ dérivation**, **\_ \_ Dynasty** et **\_ \_ superclasse**. La propriété système de **\_ \_ dérivation** est un tableau de chaînes répertoriant l’ensemble de la chaîne d’héritage jusqu’à la classe racine, y compris la classe racine, qui est également incluse dans **\_ \_ Dynasty**. La propriété système de la **\_ \_ superclasse** affiche le parent immédiat de la classe actuelle.

WMI prend également en charge les associations. Une association est une relation entre deux ou plusieurs classes WMI différentes. Par exemple, une station de travail en cours d’exécution a généralement un processeur. La classe d’association WMI [Win32 \_ ComputerSystemProcessor](/windows/desktop/CIMWin32Prov/win32-computersystemprocessor) associe la classe de station de travail [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) au [**\_ processeur**](/windows/desktop/CIMWin32Prov/win32-processor)de classe de processeur Win32. Toutefois, une classe d’association n’a pas à lier deux classes dépendantes ensemble. En fait, l’objectif principal d’une classe d’association est d’afficher les relations entre les classes qui ne sont pas nécessairement dépendantes les unes des autres. Pour plus d’informations, consultez [déclaration d’une classe d’association](declaring-an-association-class.md).

Enfin, WMI prend en charge le concept de schéma. Dans le contexte de WMI, un schéma est un groupe de classes qui décrivent un environnement de gestion particulier. Le kit de développement logiciel (SDK) Microsoft Windows utilise deux schémas : le schéma CIM et le schéma Win32. Les noms de classe de schéma CIM commencent par [CIM \_](cimclas.md)et les noms de classe de schéma Win32 commencent par [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-provider). Le schéma CIM contient les définitions des classes centrales et communes, tandis que le schéma Win32 contient les définitions des classes étendues qui sont communes à l’environnement Win32. Toutefois, un fournisseur tiers peut créer ses propres schémas pour décrire les exigences spécifiques au fournisseur. Étant donné que les schémas sont conçus pour être extensibles à l’infini, un développeur peut toujours ajouter de nouvelles classes pour décrire les nouveaux objets managés dans un environnement existant. Toutefois, pour des raisons de simplicité, la plupart des fournisseurs choisissent de créer des schémas qui héritent des propriétés des schémas CIM ou Win32.

 

 
