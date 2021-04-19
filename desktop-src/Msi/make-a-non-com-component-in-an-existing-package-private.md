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
# <a name="make-a-non-com-component-in-an-existing-package-private"></a><span data-ttu-id="844a5-103">Rendre un composant non-COM dans un package existant privé</span><span class="sxs-lookup"><span data-stu-id="844a5-103">Make a non-COM Component in an Existing Package Private</span></span>

<span data-ttu-id="844a5-104">Un administrateur peut forcer une application cliente à toujours utiliser la même copie d’un serveur non-COM dans un package existant, sans affecter d’autres applications, en spécifiant une relation de [composants isolés](isolated-components.md) entre le serveur et le client.</span><span class="sxs-lookup"><span data-stu-id="844a5-104">An administrator can force a client application to always use the same copy of a non-COM server in an existing package—without affecting other applications—by specifying an [isolated components](isolated-components.md) relationship between the server and client.</span></span> <span data-ttu-id="844a5-105">Cette installation installe une copie privée du composant serveur dans un emplacement utilisé exclusivement par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="844a5-105">This installs a private copy of the server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="844a5-106">L’administrateur doit utiliser des transformations ou un outil de création de package pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="844a5-106">The administrator needs to use transforms or a package authoring tool to do the following:</span></span>

-   <span data-ttu-id="844a5-107">Placez la DLL du serveur et le client. exe dans des composants distincts.</span><span class="sxs-lookup"><span data-stu-id="844a5-107">Put the server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="844a5-108">Entrez un enregistrement dans la [table IsolatedComponent](isolatedcomponent-table.md) avec le composant client dans la \_ colonne Shared Component et l’application cliente dans la \_ colonne application Component.</span><span class="sxs-lookup"><span data-stu-id="844a5-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="844a5-109">Inclure l' [action IsolateComponents](isolatecomponents-action.md) dans les tables de séquence.</span><span class="sxs-lookup"><span data-stu-id="844a5-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="844a5-110">Définissez le bit **msidbComponentAttributesSharedDllRefCount** dans l’enregistrement de la [table de composants](component-table.md) pour le composant \_ partagé.</span><span class="sxs-lookup"><span data-stu-id="844a5-110">Set the **msidbComponentAttributesSharedDllRefCount** bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="844a5-111">Le programme d’installation requiert ce refcount global sur l’emplacement partagé pour protéger les fichiers partagés et l’inscription dans les cas où il existe un partage avec d’autres technologies d’installation.</span><span class="sxs-lookup"><span data-stu-id="844a5-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>

 

 



