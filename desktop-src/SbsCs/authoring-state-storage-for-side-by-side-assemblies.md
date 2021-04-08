---
description: Lorsque vous créez vos propres assemblys côte à côte, suivez les instructions pour créer des assemblys côte à côte et créer n’importe quelle DLL à inclure dans l’assembly conformément aux instructions de création d’une DLL pour un assembly côte à côte.
ms.assetid: 0e98bbcd-7e23-4a33-b0fa-1f936d0ef96b
title: Création d’un stockage d’État pour des assemblys côte à côte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee388cf680ee3a186a225ca7e3bde8b6eae625d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757311"
---
# <a name="authoring-state-storage-for-side-by-side-assemblies"></a>Création d’un stockage d’État pour des assemblys côte à côte

Lorsque vous créez vos propres assemblys côte à côte, suivez les [instructions pour créer des assemblys côte à côte](guidelines-for-creating-side-by-side-assemblies.md) et créer n’importe quelle dll à inclure dans l’assembly conformément aux instructions de [création d’une dll pour un assembly côte à côte](authoring-a-dll-for-a-side-by-side-assembly.md).

Respectez les instructions suivantes pour le stockage de l’État :

-   Concevez le stockage de l’État pour une compatibilité ascendante et descendante. Attendez-vous à ce que les versions soient utilisées dans n’importe quel ordre : par exemple, v1, puis v3, puis v2.
-   Initialisez et définissez les paramètres par défaut de l’assembly dans le code de l’assembly. N’enregistrez pas les paramètres par défaut dans le registre.
-   Les paramètres du Registre doivent être écrits sur la base d’une version individuelle pour isoler plusieurs versions d’assembly qui peuvent être exécutées en même temps. Concevez votre assembly côte à côte pour stocker et gérer correctement l’état de l’assembly pendant les scénarios de partage côte à côte.
-   Les assemblys stockent généralement les informations d’État dans les clés de registre. Créez un ensemble de fichiers d’en-tête et de fonctions d’assistance pour fournir un moyen simple aux clés de registre de version contenant l’état de l’assembly.
-   Toutes les informations sur l’état de l’assembly enregistrées dans le registre doivent être isolées des autres versions de l’assembly. Les paramètres d’État stockés dans le registre doivent être enregistrés dans des sections de la version individuelle du Registre. Cela est requis dans les parties HKLM et HKCU du Registre. Par exemple, stockez les paramètres d’État HKCU de la version d’assembly XXXX sous la clé de Registre suivante :

    **HKCU** \\ **Société** \\ **MyComponent** \\ **VersionXXXX**

-   Toutes les informations d’État stockées dans le registre par les assemblys partagés doivent être enregistrées dans des sections de version individuelles du Registre. Par exemple, un paramètre d’état appelé EnableSuperCoolFeature peut avoir la valeur **true** ou **false**. Stockez la valeur d’un [*assembly côte à côte partagé*](s-sbscs-gly.md) comme suit :

    **HKEY \_ CurrentUser** \\ **Software** \\ **MyCompany** \\ **MyComponent** \\ **version 01.01** \\ **EnableSuperCoolFeature = true**

-   Toutes les informations d’État stockées dans le registre par des assemblys privés doivent être enregistrées dans les sections d’application individuelles du Registre. Cela isole les paramètres d’état de l’assembly de l’application. Vous pouvez utiliser la fonction [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) pour configurer une racine virtuelle. Par exemple, si la version d’assembly XXYY est un assembly privé de « SomeApplication », un appel à **GetModuleFileName** retourne « SomeApplication » et tous les paramètres d’État privé de l’assembly doivent être écrits sous la clé suivante :

    **HKCU** \\ **Société** \\ **MyComponent** \\ **VersionXXYY** \\ **SomeApplication**

-   Rendez les paramètres d’état partagé stockés dans le registre privés dans le contexte de l’assembly qui s’exécute. Vous pouvez utiliser la fonction [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) pour configurer une racine virtuelle. Cela doit être fait pour les branches HKLM et HKCU.
-   Idéalement, vous devez adopter un modèle de persistance dans lequel l’application conserve l’État et ne modifie pas le registre. Une application ne doit pas avoir à toucher directement les entrées de Registre du composant. Au lieu de cela, l’assembly doit proposer des fonctions API qui enregistrent ou restaurent les paramètres qui sont compatibles côte à côte.
-   Les assemblys peuvent enregistrer les paramètres d’État dans les magasins en dehors du Registre pour permettre à l’assembly d’interagir avec l’état global. Les assemblys côte à côte peuvent utiliser les magasins compatibles côte à côte suivants :
    -   Un magasin protégé (*Pstore*)
    -   Un cache WinInet
    -   Microsoft SQL Server

 

 
