---
description: Les dll TAPI, ainsi que le serveur TAPI (Tapisvr.exe), sont des abstractions cruciales qui séparent les applications de l’utilisateur final ou du serveur des fournisseurs de services. Une DLL TAPI conjointement avec le serveur TAPI fournit une interface cohérente entre ces deux couches.
ms.assetid: 17937bf1-e0bd-4845-9484-d23190807642
title: DLL TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8482045ec16a999957121aff669e93b34b605069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565141"
---
# <a name="tapi-dll"></a><span data-ttu-id="45660-104">DLL TAPI</span><span class="sxs-lookup"><span data-stu-id="45660-104">TAPI DLL</span></span>

<span data-ttu-id="45660-105">Les dll TAPI, ainsi que le serveur TAPI (Tapisvr.exe), sont des abstractions cruciales qui séparent les applications de l’utilisateur final ou du serveur des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="45660-105">The TAPI DLLs, along with the TAPI Server (Tapisvr.exe), are crucial abstractions separating end-user or server applications from service providers.</span></span> <span data-ttu-id="45660-106">Une DLL TAPI conjointement avec le serveur TAPI fournit une interface cohérente entre ces deux couches.</span><span class="sxs-lookup"><span data-stu-id="45660-106">A TAPI DLL in conjunction with the TAPI Server provides a consistent interface between these two layers.</span></span>

<span data-ttu-id="45660-107">Une application TAPI charge la DLL appropriée dans son espace de processus.</span><span class="sxs-lookup"><span data-stu-id="45660-107">A TAPI application loads the appropriate DLL into its process space.</span></span> <span data-ttu-id="45660-108">Pendant l’initialisation, TAPI établit une liaison RPC avec Tapisvr.exe.</span><span class="sxs-lookup"><span data-stu-id="45660-108">During initialization, TAPI establishes an RPC link with Tapisvr.exe.</span></span> <span data-ttu-id="45660-109">Le serveur TAPI s’exécute dans le contexte de SVCHOST.</span><span class="sxs-lookup"><span data-stu-id="45660-109">The TAPI Server runs in the context of SVCHOST.</span></span>

<span data-ttu-id="45660-110">Il existe trois dll associées à l’interface TAPI : Tapi.dll, Tapi32.dll et Tapi3.dll.</span><span class="sxs-lookup"><span data-stu-id="45660-110">There are three DLLs associated with TAPI: Tapi.dll, Tapi32.dll, and Tapi3.dll.</span></span> <span data-ttu-id="45660-111">Ces dll se trouvent dans% SystemRoot% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="45660-111">These DLLs are located in %SystemRoot%\\system32.</span></span> <span data-ttu-id="45660-112">La figure suivante illustre les rôles de leurs rôles respectifs dans Microsoft Telephony :</span><span class="sxs-lookup"><span data-stu-id="45660-112">The following figure illustrates the roles of their respective roles in Microsoft Telephony:</span></span>

![rôles des trois dll TAPI](images/dllserv.png)

<span data-ttu-id="45660-114">Les applications 16 bits existantes sont liées à Tapi.dll.</span><span class="sxs-lookup"><span data-stu-id="45660-114">Existing 16-bit applications link to Tapi.dll.</span></span> <span data-ttu-id="45660-115">Tapi.dll est simplement une couche de thunk qui mappe les adresses 16 bits aux adresses 32 bits et transmet les demandes à Tapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="45660-115">Tapi.dll is simply a thunk layer that maps 16-bit addresses to 32-bit addresses and pass requests to Tapi32.dll.</span></span>

<span data-ttu-id="45660-116">Les applications TAPI 2. x 32 bits existantes sont liées à Tapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="45660-116">Existing 32-bit TAPI 2.x applications link to Tapi32.dll.</span></span> <span data-ttu-id="45660-117">Tapi32.dll est une couche de marshaling fine qui transfère les demandes de fonction vers le serveur TAPI (TAPISRV) et, si nécessaire, charge et appelle les dll du fournisseur de services multimédia dans le processus de l’application.</span><span class="sxs-lookup"><span data-stu-id="45660-117">Tapi32.dll is a thin marshalling layer that transfers function requests to the TAPI Server (TAPISRV) and, when needed, loads and invokes media service provider DLLs in the application's process.</span></span>

<span data-ttu-id="45660-118">Les applications TAPI 3. x sont liées à Tapi3.dll.</span><span class="sxs-lookup"><span data-stu-id="45660-118">TAPI 3.x applications link to Tapi3.dll.</span></span>

 

 



