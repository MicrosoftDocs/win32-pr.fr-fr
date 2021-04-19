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
# <a name="make-a-com-component-in-an-existing-package-private"></a><span data-ttu-id="97884-103">Rendre un composant COM dans un package existant privé</span><span class="sxs-lookup"><span data-stu-id="97884-103">Make a COM Component in an Existing Package Private</span></span>

<span data-ttu-id="97884-104">Un administrateur peut forcer une application cliente COM à toujours utiliser la même copie d’un serveur COM dans un package existant, sans affecter d’autres applications, en spécifiant une relation de [composants isolés](isolated-components.md) entre le serveur com et le client.</span><span class="sxs-lookup"><span data-stu-id="97884-104">An administrator can force a COM-client application to always use the same copy of a COM-server in an existing package—without affecting other applications—by specifying an [isolated components](isolated-components.md) relationship between the COM server and client.</span></span> <span data-ttu-id="97884-105">Cette installation installe une copie privée du composant COM-Server dans un emplacement exclusivement utilisé par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="97884-105">This installs a private copy of the COM-server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="97884-106">L’administrateur doit utiliser des transformations ou un outil de création de package pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="97884-106">The administrator needs to use transforms or a package authoring tool to do the following:</span></span>

-   <span data-ttu-id="97884-107">Placez la DLL du serveur COM et le client. exe dans des composants distincts.</span><span class="sxs-lookup"><span data-stu-id="97884-107">Put the COM server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="97884-108">Entrez un enregistrement dans la [table IsolatedComponent](isolatedcomponent-table.md) avec le composant com-client dans la \_ colonne Shared Component et l’application cliente dans la \_ colonne application Component.</span><span class="sxs-lookup"><span data-stu-id="97884-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the COM-client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="97884-109">Inclure l' [action IsolateComponents](isolatecomponents-action.md) dans les tables de séquence.</span><span class="sxs-lookup"><span data-stu-id="97884-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="97884-110">Définissez le bit **msidbComponentAttributesSharedDllRefCount** dans l’enregistrement de la [table de composants](component-table.md) pour le composant \_ partagé.</span><span class="sxs-lookup"><span data-stu-id="97884-110">Set the **msidbComponentAttributesSharedDllRefCount** bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="97884-111">Le programme d’installation requiert ce refcount global sur l’emplacement partagé pour protéger les fichiers partagés et l’inscription dans les cas où il existe un partage avec d’autres technologies d’installation.</span><span class="sxs-lookup"><span data-stu-id="97884-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>

 

 



