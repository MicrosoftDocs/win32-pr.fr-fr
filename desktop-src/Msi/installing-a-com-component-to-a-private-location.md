---
description: Pour forcer une application COM-client à toujours utiliser la même copie d’un serveur COM, créez le package d’installation de l’application afin de spécifier une relation de composants isolés entre le serveur COM et le client.
ms.assetid: 387c1c4d-16f5-4f46-b868-c2be7cb3f942
title: Installation d’un composant COM dans un emplacement privé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733f8a261401f53c09253b9c239a8daacc34b99bb49f299ee2d305a6e360cb6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105129"
---
# <a name="installing-a-com-component-to-a-private-location"></a>Installation d’un composant COM dans un emplacement privé

Pour forcer une application COM-client à toujours utiliser la même copie d’un serveur COM, créez le package d’installation de l’application afin de spécifier une relation de [composants isolés](isolated-components.md) entre le serveur com et le client. Cette installation installe une copie privée du composant COM-Server dans un emplacement exclusivement utilisé par l’application cliente. Procédez comme suit lors de la création du package :

-   Placez la DLL du serveur COM et le client .exe dans des composants distincts.
-   Entrez un enregistrement dans la [table IsolatedComponent](isolatedcomponent-table.md) avec le composant com-client dans la \_ colonne Shared Component et l’application cliente dans la \_ colonne application Component. Inclure l' [action IsolateComponents](isolatecomponents-action.md) dans les tables de séquence.
-   Définissez le bit msidbComponentAttributesSharedDllRefCount dans l’enregistrement de la [table de composants](component-table.md) pour le composant \_ partagé. Le programme d’installation requiert ce refcount global sur l’emplacement partagé pour protéger les fichiers partagés et l’inscription dans les cas où il existe un partage avec d’autres technologies d’installation.

 

 



