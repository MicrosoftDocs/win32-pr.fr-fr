---
title: Modèle d’association de type de fichier et d’URI
description: Modèle d’association de type de fichier et d’URI
ms.assetid: 4DE7DD08-088A-4E09-B1C7-AE9033EA533D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aabcdb40bd38aeee24ee0e5d86f11651633a7eead1748810e8c1c6a846827690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028857"
---
# <a name="file-type-and-uri-associations-model"></a>Modèle d’association de type de fichier et d’URI

## <a name="platforms"></a>Plateformes

 **Clients** -Windows 8  
**serveurs** -Windows Server 2012  



## <a name="description"></a>Description

Le type de fichier et le modèle d’association d’URI ont été modifiés dans Windows 8. Les applications ne sont plus en mesure de se définir elles-mêmes par programmation en tant que gestionnaire par défaut pour un type de fichier ou un URI. À la place, l’utilisateur contrôle toujours le gestionnaire par défaut pour un type de fichier ou un schéma d’URI.

## <a name="manifestation"></a>Manifestation

La façon dont cette modification est présentée à l’utilisateur dépend de la façon dont l’application est conçue, par exemple :

-   De nombreuses applications vérifient s’il s’agit de la valeur par défaut chaque fois qu’elles s’exécutent et, si elles ne le sont pas, elles invitent l’utilisateur à les définir comme valeur par défaut. Toutefois, étant donné que les applications ne peuvent pas interroger avec précision pour déterminer quelle application est le gestionnaire par défaut pour un type de fichier ou un schéma d’URI, aucune de ces opérations ne fonctionne.
-   De nombreuses applications ont une boîte de dialogue ou un menu intégré ou, dans leur programme d’installation, qui spécifie les types de fichiers pour lesquels l’application doit servir de valeur par défaut. Toutefois, étant donné que les applications ne peuvent plus être définies par programmation comme gestionnaire par défaut pour un type de fichier ou un schéma d’URI, cela ne fonctionne plus.

## <a name="mitigation"></a>Limitation des risques

Les utilisateurs peuvent effectuer plusieurs tâches pour prendre en compte les modifications suivantes :

-   Les utilisateurs sont invités à choisir une application par défaut pour gérer les types de fichiers, les schémas d’URI ou les deux quand aucun n’a été spécifié.
-   Les utilisateurs ont la possibilité de modifier leur gestionnaire par défaut après l’installation de nouvelles applications capables de gérer un type de fichier ou un schéma d’URI
-   Le panneau de configuration programmes par défaut permet aux utilisateurs de définir des valeurs par défaut pour une application, ou pour un type de fichier, un modèle d’URI, ou les deux. les applications peuvent être liées au panneau de configuration
-   les valeurs par défaut peuvent être modifiées à partir de l’explorateur de Windows

## <a name="solution"></a>Solution

Suite à ces modifications, cette recommandation d’API est fournie :

-   La fonctionnalité de certains appels de méthode au sein de l’API [IApplicationAssociationRegistration](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) a changé et ne doit plus être utilisée.

    -   **N'** appelez pas [QueryAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) / [QueryAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall) pour déterminer si une application est la valeur par défaut
    -   **N'** appelez pas [QueryCurrentDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault) pour déterminer quelle application (le cas échéant) est la valeur par défaut actuelle
    -   **N'** appelez pas [SetAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault) / [SetAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall) pour définir l’application par défaut

-   Les instructions à suivre sont les suivantes :

    -   **Ne pas** interroger pour voir quelle application est le gestionnaire par défaut pour les types de fichiers ou les schémas d’URI

    -   **N’essayez pas** de surveiller les modifications dans le gestionnaire par défaut pour les types de fichiers ou les schémas d’URI

    -   **N’essayez pas** de définir une application en tant que gestionnaire par défaut pour les types de fichiers ou les schémas d’URI

    -   **N’essayez pas** de gérer les valeurs par défaut pour les types de fichiers ou les schémas d’URI à partir d’une application

    -   **S’intègrent** au panneau de [configuration définir les programmes par défaut](../shell/default-programs.md) si vous souhaitez autoriser les utilisateurs de votre application à accéder à l’interface utilisateur de gestion par défaut (l’interface utilisateur de gestion dans l’application n’est plus prise en charge)

        -   L’appel de [IApplicationAssociationRegistrationUI :: LaunchAdvancedAssociationUI](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) permet à l’utilisateur d’accéder à la page «[définir les programmes par défaut](../shell/default-programs.md)» du panneau de configuration pour l’application spécifiée

## <a name="tests"></a>Tests

-   Test pour vérifier que les applications s’inscrivent correctement dans le panneau de configuration des programmes par défaut
-   Testez pour vérifier que les applications s’inscrivent correctement dans la liste OpenWith pour les types de fichiers, les schémas d’URI, ou les deux, qu’ils inscrivent pour gérer
-   Test pour vérifier que les nouvelles notifications de l’application s’affichent après l’installation de votre application et que l’utilisateur appelle un type de fichier, un modèle d’URI, ou les deux, que votre application s’est inscrite pour gérer

## <a name="resources"></a>Ressources

-   [meilleures pratiques pour les Associations de Type de fichier et d’URI dans les applications de bureau Windows 8](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))
-   [Associations de types de fichier et présentation de la Conférence génération d’exécution automatique](https://channel9.msdn.com/events/BUILD/BUILD2011/PLAT-282T)

 

 