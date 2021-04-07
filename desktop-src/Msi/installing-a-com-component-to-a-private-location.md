---
description: Pour forcer une application COM-client à toujours utiliser la même copie d’un serveur COM, créez le package d’installation de l’application afin de spécifier une relation de composants isolés entre le serveur COM et le client.
ms.assetid: 387c1c4d-16f5-4f46-b868-c2be7cb3f942
title: Installation d’un composant COM dans un emplacement privé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838b3f40c513fd0998402893543e88526e4a6d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863282"
---
# <a name="installing-a-com-component-to-a-private-location"></a><span data-ttu-id="128bd-103">Installation d’un composant COM dans un emplacement privé</span><span class="sxs-lookup"><span data-stu-id="128bd-103">Installing a COM Component to a Private Location</span></span>

<span data-ttu-id="128bd-104">Pour forcer une application COM-client à toujours utiliser la même copie d’un serveur COM, créez le package d’installation de l’application afin de spécifier une relation de [composants isolés](isolated-components.md) entre le serveur com et le client.</span><span class="sxs-lookup"><span data-stu-id="128bd-104">To force a COM-client application to always use the same copy of a COM-server, author the application's installation package to specify an [isolated components](isolated-components.md) relationship between the COM server and client.</span></span> <span data-ttu-id="128bd-105">Cette installation installe une copie privée du composant COM-Server dans un emplacement exclusivement utilisé par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="128bd-105">This installs a private copy of the COM-server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="128bd-106">Procédez comme suit lors de la création du package :</span><span class="sxs-lookup"><span data-stu-id="128bd-106">Do the following when authoring the package:</span></span>

-   <span data-ttu-id="128bd-107">Placez la DLL du serveur COM et le client. exe dans des composants distincts.</span><span class="sxs-lookup"><span data-stu-id="128bd-107">Put the COM server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="128bd-108">Entrez un enregistrement dans la [table IsolatedComponent](isolatedcomponent-table.md) avec le composant com-client dans la \_ colonne Shared Component et l’application cliente dans la \_ colonne application Component.</span><span class="sxs-lookup"><span data-stu-id="128bd-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the COM-client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="128bd-109">Inclure l' [action IsolateComponents](isolatecomponents-action.md) dans les tables de séquence.</span><span class="sxs-lookup"><span data-stu-id="128bd-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="128bd-110">Définissez le bit msidbComponentAttributesSharedDllRefCount dans l’enregistrement de la [table de composants](component-table.md) pour le composant \_ partagé.</span><span class="sxs-lookup"><span data-stu-id="128bd-110">Set the msidbComponentAttributesSharedDllRefCount bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="128bd-111">Le programme d’installation requiert ce refcount global sur l’emplacement partagé pour protéger les fichiers partagés et l’inscription dans les cas où il existe un partage avec d’autres technologies d’installation.</span><span class="sxs-lookup"><span data-stu-id="128bd-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>

 

 



