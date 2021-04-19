---
description: Un administrateur peut forcer une application cliente à toujours utiliser la même copie d’un serveur non-COM dans un package existant&\# 8212 ; sans affecter d’autres applications&\# 8212 ; en spécifiant une relation de composants isolés entre le serveur et le client.
ms.assetid: e10d7942-b13c-46a3-a8ca-cb7bc021c76b
title: Rendre un composant non-COM dans un package existant privé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d87a74a4f9fe7c3770100f78dd0fcd154772943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534356"
---
# <a name="make-a-non-com-component-in-an-existing-package-private"></a>Rendre un composant non-COM dans un package existant privé

Un administrateur peut forcer une application cliente à toujours utiliser la même copie d’un serveur non-COM dans un package existant, sans affecter d’autres applications, en spécifiant une relation de [composants isolés](isolated-components.md) entre le serveur et le client. Cette installation installe une copie privée du composant serveur dans un emplacement utilisé exclusivement par l’application cliente. L’administrateur doit utiliser des transformations ou un outil de création de package pour effectuer les opérations suivantes :

-   Placez la DLL du serveur et le client. exe dans des composants distincts.
-   Entrez un enregistrement dans la [table IsolatedComponent](isolatedcomponent-table.md) avec le composant client dans la \_ colonne Shared Component et l’application cliente dans la \_ colonne application Component. Inclure l' [action IsolateComponents](isolatecomponents-action.md) dans les tables de séquence.
-   Définissez le bit **msidbComponentAttributesSharedDllRefCount** dans l’enregistrement de la [table de composants](component-table.md) pour le composant \_ partagé. Le programme d’installation requiert ce refcount global sur l’emplacement partagé pour protéger les fichiers partagés et l’inscription dans les cas où il existe un partage avec d’autres technologies d’installation.

 

 



