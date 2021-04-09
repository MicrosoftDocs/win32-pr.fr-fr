---
description: Le serveur TAPI (TAPISRV) est le référentiel central des données de téléphonie sur un ordinateur utilisateur.
ms.assetid: 794d230c-abe8-429d-bbf5-91ba364b16ab
title: Serveur TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a6886a5d8e56519f10fc370ed15adc3b1af7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866913"
---
# <a name="tapi-server"></a><span data-ttu-id="33a73-103">Serveur TAPI</span><span class="sxs-lookup"><span data-stu-id="33a73-103">TAPI Server</span></span>

<span data-ttu-id="33a73-104">Le serveur TAPI (TAPISRV) est le référentiel central des données de téléphonie sur un ordinateur utilisateur.</span><span class="sxs-lookup"><span data-stu-id="33a73-104">The TAPI server (TAPISRV) is the central repository of telephony data on a user computer.</span></span> <span data-ttu-id="33a73-105">Ce processus de service effectue le suivi des ressources de téléphonie locales et distantes, des applications inscrites pour gérer les demandes de téléphonie assistées et des fonctions asynchrones en attente, et il permet également une interface cohérente avec les fournisseurs de services de téléphonie (TSPs).</span><span class="sxs-lookup"><span data-stu-id="33a73-105">This service process tracks local and remote telephony resources, applications registered to handle Assisted Telephony requests, and pending asynchronous functions, and it also enables a consistent interface with telephony service providers (TSPs).</span></span> <span data-ttu-id="33a73-106">Pour plus d’informations et pour obtenir un diagramme illustrant la relation du serveur TAPI avec d’autres composants et une vue d’ensemble de leurs rôles, consultez [modèle de programmation Microsoft](microsoft-telephony-programming-model.md)pour la téléphonie.</span><span class="sxs-lookup"><span data-stu-id="33a73-106">For more information and a diagram that illustrates the relationship of the TAPI Server to other components and an overview of their roles, see [Microsoft Telephony Programming Model](microsoft-telephony-programming-model.md).</span></span>

<span data-ttu-id="33a73-107">Pour les ordinateurs qui exécutent les systèmes d’exploitation Windows Server 2003, Windows XP et Windows 2000, TAPISRV s’exécute dans le contexte de Svchost.exe.</span><span class="sxs-lookup"><span data-stu-id="33a73-107">For computers running on Windows Server 2003 operating systems, Windows XP, and Windows 2000, TAPISRV runs within the context of Svchost.exe.</span></span> <span data-ttu-id="33a73-108">Pour les ordinateurs fonctionnant sous Windows NT, il s’exécute en tant que processus de service distinct.</span><span class="sxs-lookup"><span data-stu-id="33a73-108">For computers running on Windows NT, it runs as a separate service process.</span></span> <span data-ttu-id="33a73-109">Quand une application charge une DLL TAPI dans son espace de processus et effectue une opération d’initialisation, la DLL établit une liaison RPC avec le serveur TAPI.</span><span class="sxs-lookup"><span data-stu-id="33a73-109">When an application loads a TAPI DLL into its process space and performs an initialization operation, the DLL establishes an RPC link to the TAPI Server.</span></span> <span data-ttu-id="33a73-110">Le serveur TAPI charge les fournisseurs de services téléphoniques (TSPs) dans son espace de processus.</span><span class="sxs-lookup"><span data-stu-id="33a73-110">The TAPI Server loads telephone service providers (TSPs) into its process space.</span></span> <span data-ttu-id="33a73-111">Quel que soit le nombre d’applications qui accèdent aux appareils d’un fournisseur donné, une seule instance d’un TSP donné existera.</span><span class="sxs-lookup"><span data-stu-id="33a73-111">Regardless of how many applications access a given provider's devices, only one instance of a given TSP will exist.</span></span>

 

 



