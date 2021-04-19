---
description: Un administrateur peut forcer une application cliente COM à toujours utiliser la même copie d’un serveur COM dans un package existant&\# 8212 ; sans affecter d’autres applications&\# 8212 ; en spécifiant une relation de composants isolés entre le serveur com et le client.
ms.assetid: 814eca94-2bb5-4aff-8de3-473da71d4400
title: Rendre un composant COM dans un package existant privé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4935d20c5034af81a52c18d35454553b04cfb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534042"
---
# <a name="make-a-com-component-in-an-existing-package-private"></a>Rendre un composant COM dans un package existant privé

Un administrateur peut forcer une application cliente COM à toujours utiliser la même copie d’un serveur COM dans un package existant, sans affecter d’autres applications, en spécifiant une relation de [composants isolés](isolated-components.md) entre le serveur com et le client. Cette installation installe une copie privée du composant COM-Server dans un emplacement exclusivement utilisé par l’application cliente. L’administrateur doit utiliser des transformations ou un outil de création de package pour effectuer les opérations suivantes :

-   Placez la DLL du serveur COM et le client. exe dans des composants distincts.
-   Entrez un enregistrement dans la [table IsolatedComponent](isolatedcomponent-table.md) avec le composant com-client dans la \_ colonne Shared Component et l’application cliente dans la \_ colonne application Component. Inclure l' [action IsolateComponents](isolatecomponents-action.md) dans les tables de séquence.
-   Définissez le bit **msidbComponentAttributesSharedDllRefCount** dans l’enregistrement de la [table de composants](component-table.md) pour le composant \_ partagé. Le programme d’installation requiert ce refcount global sur l’emplacement partagé pour protéger les fichiers partagés et l’inscription dans les cas où il existe un partage avec d’autres technologies d’installation.

 

 



