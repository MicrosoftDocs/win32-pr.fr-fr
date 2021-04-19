---
title: Vue d’ensemble de l’entrée Service Name
description: L’entrée service de nom se compose de trois sections distinctes.
ms.assetid: 3059a9a9-174d-4d04-8565-e4558f17f465
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efc3855f586582b013bc47b11eb058ae461014f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106536879"
---
# <a name="an-overview-of-the-name-service-entry"></a><span data-ttu-id="772cc-103">Vue d’ensemble de l’entrée Service Name</span><span class="sxs-lookup"><span data-stu-id="772cc-103">An Overview of the Name Service Entry</span></span>

<span data-ttu-id="772cc-104">L’entrée service de nom se compose de trois sections distinctes.</span><span class="sxs-lookup"><span data-stu-id="772cc-104">The name service entry consists of three distinct sections.</span></span> <span data-ttu-id="772cc-105">La première section concerne les interfaces (UUID + version), la deuxième section contient les UUID d’objet, et la troisième section concerne les handles de liaison.</span><span class="sxs-lookup"><span data-stu-id="772cc-105">The first section is for interfaces (UUID + version), the second section contains the object UUIDs, and the third section is for binding handles.</span></span> <span data-ttu-id="772cc-106">Vous devez fournir un nom pour l’entrée qui servira de méthode pour l’identifier.</span><span class="sxs-lookup"><span data-stu-id="772cc-106">You provide a name for the entry that will serve as a way to identify it.</span></span>

<span data-ttu-id="772cc-107">Lors de l’appel de [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta), le serveur spécifie le nom de l’entrée dans laquelle placer les informations exportées.</span><span class="sxs-lookup"><span data-stu-id="772cc-107">When calling [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta), the server specifies the name of the entry in which to place the exported information.</span></span> <span data-ttu-id="772cc-108">Cette interface récemment exportée est ensuite ajoutée à la section interface de l’entrée Service Name.</span><span class="sxs-lookup"><span data-stu-id="772cc-108">This newly exported interface is then added to the interface section of the name service entry.</span></span> <span data-ttu-id="772cc-109">Toutes les interfaces déjà présentes dans l’entrée de service de nom sont également conservées.</span><span class="sxs-lookup"><span data-stu-id="772cc-109">Any interfaces that are already present in the name service entry remain as well.</span></span> <span data-ttu-id="772cc-110">Ce même processus est suivi pour les UUID d’objet et les handles de liaison.</span><span class="sxs-lookup"><span data-stu-id="772cc-110">This same process is followed for object UUIDs and binding handles.</span></span>

<span data-ttu-id="772cc-111">Le client appelle [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (ou [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)) pour rechercher un handle de liaison approprié.</span><span class="sxs-lookup"><span data-stu-id="772cc-111">The client calls [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (or [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)) to search for an appropriate binding handle.</span></span> <span data-ttu-id="772cc-112">Le nom de l’entrée, le descripteur d’interface et l’UUID de l’objet sont extraits.</span><span class="sxs-lookup"><span data-stu-id="772cc-112">The entry name, interface handle, and an object UUID are extracted.</span></span> <span data-ttu-id="772cc-113">Celles-ci restreignent les entrées à partir desquelles les handles de liaison sont retournés.</span><span class="sxs-lookup"><span data-stu-id="772cc-113">These restrict the entries from which binding handles are returned.</span></span> <span data-ttu-id="772cc-114">Si une entrée correspond aux critères de recherche, tous les descripteurs de liaison de cette entrée sont retournés à partir de [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span><span class="sxs-lookup"><span data-stu-id="772cc-114">If an entry matches the search criteria, all the binding handles in that entry are returned from [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span></span>

 

 




