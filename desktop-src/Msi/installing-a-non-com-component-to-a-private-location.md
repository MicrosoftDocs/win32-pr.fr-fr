---
description: Pour forcer une application cliente à toujours utiliser la même copie d’un serveur non-COM, créez le package d’installation de l’application afin de spécifier une relation de composants isolés entre le serveur et le client.
ms.assetid: 3ca9cad7-6848-4483-b5e3-2b7bbdefe605
title: Installation d’un composant non-COM dans un emplacement privé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ea4e10e7a08fd008352a36feca537685ee4390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868878"
---
# <a name="installing-a-non-com-component-to-a-private-location"></a>Installation d’un composant non-COM dans un emplacement privé

Pour forcer une application cliente à toujours utiliser la même copie d’un serveur non-COM, créez le package d’installation de l’application afin de spécifier une relation de [composants isolés](isolated-components.md) entre le serveur et le client. Cette installation installe une copie privée du composant serveur dans un emplacement utilisé exclusivement par l’application cliente. Procédez comme suit lors de la création du package :

-   Placez la DLL du serveur et le client. exe dans des composants distincts.
-   Entrez un enregistrement dans la [table IsolatedComponent](isolatedcomponent-table.md) avec le composant client dans la \_ colonne Shared Component et l’application cliente dans la \_ colonne application Component. Inclure l' [action IsolateComponents](isolatecomponents-action.md) dans les tables de séquence.
-   Définissez le bit msidbComponentAttributesSharedDllRefCount dans l’enregistrement de la [table de composants](component-table.md) pour le composant \_ partagé. Le programme d’installation requiert ce refcount global sur l’emplacement partagé pour protéger les fichiers partagés et l’inscription dans les cas où il existe un partage avec d’autres technologies d’installation.
-   Évitez de créer un chemin d’accès enregistré partagé entre les composants.

 

 



