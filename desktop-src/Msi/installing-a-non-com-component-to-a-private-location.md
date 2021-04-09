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
# <a name="installing-a-non-com-component-to-a-private-location"></a><span data-ttu-id="33238-103">Installation d’un composant non-COM dans un emplacement privé</span><span class="sxs-lookup"><span data-stu-id="33238-103">Installing a non-COM Component to a Private Location</span></span>

<span data-ttu-id="33238-104">Pour forcer une application cliente à toujours utiliser la même copie d’un serveur non-COM, créez le package d’installation de l’application afin de spécifier une relation de [composants isolés](isolated-components.md) entre le serveur et le client.</span><span class="sxs-lookup"><span data-stu-id="33238-104">To force a client application to always use the same copy of a non-COM server, author the application's installation package to specify an [isolated components](isolated-components.md) relationship between the server and client.</span></span> <span data-ttu-id="33238-105">Cette installation installe une copie privée du composant serveur dans un emplacement utilisé exclusivement par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="33238-105">This installs a private copy of the server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="33238-106">Procédez comme suit lors de la création du package :</span><span class="sxs-lookup"><span data-stu-id="33238-106">Do the following when authoring the package:</span></span>

-   <span data-ttu-id="33238-107">Placez la DLL du serveur et le client. exe dans des composants distincts.</span><span class="sxs-lookup"><span data-stu-id="33238-107">Put the server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="33238-108">Entrez un enregistrement dans la [table IsolatedComponent](isolatedcomponent-table.md) avec le composant client dans la \_ colonne Shared Component et l’application cliente dans la \_ colonne application Component.</span><span class="sxs-lookup"><span data-stu-id="33238-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="33238-109">Inclure l' [action IsolateComponents](isolatecomponents-action.md) dans les tables de séquence.</span><span class="sxs-lookup"><span data-stu-id="33238-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="33238-110">Définissez le bit msidbComponentAttributesSharedDllRefCount dans l’enregistrement de la [table de composants](component-table.md) pour le composant \_ partagé.</span><span class="sxs-lookup"><span data-stu-id="33238-110">Set the msidbComponentAttributesSharedDllRefCount bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="33238-111">Le programme d’installation requiert ce refcount global sur l’emplacement partagé pour protéger les fichiers partagés et l’inscription dans les cas où il existe un partage avec d’autres technologies d’installation.</span><span class="sxs-lookup"><span data-stu-id="33238-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>
-   <span data-ttu-id="33238-112">Évitez de créer un chemin d’accès enregistré partagé entre les composants.</span><span class="sxs-lookup"><span data-stu-id="33238-112">Avoid authoring a shared registered path across components.</span></span>

 

 



