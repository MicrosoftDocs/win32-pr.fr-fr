---
description: Les évaluateurs de cohérence internes, également appelés « ICEs », sont des actions personnalisées écrites en VBScript, JScript, ou en tant que DLL ou EXE.
ms.assetid: 0789103d-ae34-46be-a9fb-093e066d6d4b
title: Évaluateurs de cohérence internes-CIEM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77be6e2bf33bbe348acab45191782a211ea4663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535649"
---
# <a name="internal-consistency-evaluators---ices"></a>Évaluateurs de cohérence internes-CIEM

Les évaluateurs de cohérence internes, également appelés « ICEs », sont des actions personnalisées écrites en VBScript, JScript, ou en tant que DLL ou EXE. Lorsque ces actions personnalisées sont exécutées, elles analysent la base de données à la recherche d’entrées dans les enregistrements de base de données qui sont valides lorsqu’elles sont examinées individuellement, mais qui peuvent provoquer un comportement incorrect dans le contexte de la base de données entière Notez que cela est différent de la validation effectuée sur des enregistrements individuels à l’aide de [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify).

Par exemple, la [table des composants](component-table.md) peut répertorier plusieurs composants qui sont tous valides lorsqu’ils sont testés individuellement avec [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify). Toutefois, **MsiViewModify** n’intercepte pas l’erreur lorsque deux composants utilisent le même [GUID](guid.md) que leur code de composant. L’action personnalisée [ICE08](ice08.md) est conçue pour valider que la table des composants ne contient pas de GUID de code de composant en double.

Les actions personnalisées ICE retournent quatre types de messages :

-   [**Erreurs**](merge-errors.md) Les messages d’erreur signalent la création de base de données qui provoque un comportement incorrect. Par exemple, les GUID de composant en double provoquent l’inscription incorrecte des composants par le programme d’installation.
-   **Avertissements** Les messages d’avertissement signalent la création de base de données qui provoque un comportement incorrect dans certains cas. Les avertissements peuvent également signaler des effets secondaires inattendus de la création de bases de données. Par exemple, si vous entrez le même nom de propriété dans deux conditions qui diffèrent uniquement par la casse des lettres du nom. Étant donné que le programme d’installation respecte la casse, le programme d’installation traite ces derniers comme des propriétés différentes.
-   **Échecs** Les messages d’échec signalent l’échec de l’action personnalisée ICE. L’échec est généralement dû à une base de données avec des problèmes graves que la glace ne peut même pas exécuter.
-   **Informations** Les messages d’information fournissent des informations à partir de la glace et n’indiquent pas de problème avec la base de données. Il s’agit souvent d’informations sur la glace elle-même, par exemple une brève description. Ils peuvent également fournir des informations de progression au fur et à mesure de l’exécution de la glace.

Pour plus d’informations, consultez [utilisation des évaluateurs de cohérence internes](using-internal-consistency-evaluators.md).

 

 



