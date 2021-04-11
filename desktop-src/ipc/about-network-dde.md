---
description: Le service DDE réseau est utilisé pour initier et maintenir les connexions réseau nécessaires aux conversations DDE entre les applications qui s’exécutent sur des ordinateurs différents d’un réseau.
ms.assetid: f9eee391-2b4a-4c17-bea5-72cda5124e1c
title: À propos de DDE réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412971f6bef8d2782dce38b5aef413e4d073f6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319010"
---
# <a name="about-network-dde"></a><span data-ttu-id="4e625-103">À propos de DDE réseau</span><span class="sxs-lookup"><span data-stu-id="4e625-103">About Network DDE</span></span>

<span data-ttu-id="4e625-104">\[Le DDE réseau n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4e625-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="4e625-105">Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]</span><span class="sxs-lookup"><span data-stu-id="4e625-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="4e625-106">Le service DDE réseau est utilisé pour initier et maintenir les connexions réseau nécessaires aux conversations DDE entre les applications qui s’exécutent sur des ordinateurs différents d’un réseau.</span><span class="sxs-lookup"><span data-stu-id="4e625-106">Network DDE is used to initiate and maintain the network connections needed for DDE conversations between applications running on different computers in a network.</span></span> <span data-ttu-id="4e625-107">Une *conversation* DDE est l’interaction entre les applications client et serveur.</span><span class="sxs-lookup"><span data-stu-id="4e625-107">A DDE *conversation* is the interaction between client and server applications.</span></span> <span data-ttu-id="4e625-108">Vous utilisez le DDE réseau avec DDE et la bibliothèque de gestion DDE (DDEML) dans votre application.</span><span class="sxs-lookup"><span data-stu-id="4e625-108">You use network DDE along with DDE and the DDE management library (DDEML) in your application.</span></span>

<span data-ttu-id="4e625-109">DDE est une forme de communication interprocessus qui utilise la mémoire partagée pour échanger des données entre des applications.</span><span class="sxs-lookup"><span data-stu-id="4e625-109">DDE is a form of interprocess communication that uses shared memory to exchange data between applications.</span></span> <span data-ttu-id="4e625-110">Les applications peuvent utiliser DDE pour les transferts de données à usage unique ou pour les échanges en cours et la mise à jour des données.</span><span class="sxs-lookup"><span data-stu-id="4e625-110">Applications can use DDE for one time data transfers or for ongoing exchanges and updating data.</span></span> <span data-ttu-id="4e625-111">Pour plus d’informations sur les échanges de données, consultez [échange dynamique de données](../dataxchg/dynamic-data-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="4e625-111">For more information on DDE, see [Dynamic Data Exchange](../dataxchg/dynamic-data-exchange.md).</span></span>

<span data-ttu-id="4e625-112">DDEML simplifie la tâche d’ajout de la fonctionnalité DDE à une application.</span><span class="sxs-lookup"><span data-stu-id="4e625-112">DDEML simplifies the task of adding DDE capability to an application.</span></span> <span data-ttu-id="4e625-113">Au lieu d’envoyer, de publier et de traiter des messages DDE directement, une application utilise les fonctions fournies par le DDEML pour gérer les conversations DDE.</span><span class="sxs-lookup"><span data-stu-id="4e625-113">Instead of sending, posting, and processing DDE messages directly, an application uses the functions provided by the DDEML to manage DDE conversations.</span></span> <span data-ttu-id="4e625-114">Pour plus d’informations sur DDEML, consultez [bibliothèque de gestion des échange dynamique de données](../dataxchg/dynamic-data-exchange-management-library.md).</span><span class="sxs-lookup"><span data-stu-id="4e625-114">For more information on DDEML, see [Dynamic Data Exchange Management Library](../dataxchg/dynamic-data-exchange-management-library.md).</span></span>

## <a name="network-dde-files"></a><span data-ttu-id="4e625-115">Fichiers DDE réseau</span><span class="sxs-lookup"><span data-stu-id="4e625-115">Network DDE Files</span></span>

<span data-ttu-id="4e625-116">Pour utiliser les éléments d’API du DDE réseau, vous devez inclure le fichier d’en-tête NDDEApi. h dans vos fichiers sources et inclure le fichier NDDEApi. lib sur la ligne de votre lien.</span><span class="sxs-lookup"><span data-stu-id="4e625-116">To use the API elements of network DDE, you must include the NDDEApi.h header file in your source files and include NDDEApi.lib file on your link line.</span></span> <span data-ttu-id="4e625-117">Vous devez également vous assurer que le fichier NDDEApi.dll est chargé.</span><span class="sxs-lookup"><span data-stu-id="4e625-117">You must also make sure that the NDDEApi.dll file is loaded.</span></span>

<span data-ttu-id="4e625-118">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="4e625-118">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="4e625-119">Agent DDE réseau</span><span class="sxs-lookup"><span data-stu-id="4e625-119">Network DDE Agent</span></span>](network-dde-agent.md)
-   [<span data-ttu-id="4e625-120">Partages DDE</span><span class="sxs-lookup"><span data-stu-id="4e625-120">DDE Shares</span></span>](dde-shares.md)
-   [<span data-ttu-id="4e625-121">Partages et sécurité approuvés</span><span class="sxs-lookup"><span data-stu-id="4e625-121">Trusted Shares and Security</span></span>](trusted-shares-and-security.md)
-   [<span data-ttu-id="4e625-122">Gestion des partages DDE</span><span class="sxs-lookup"><span data-stu-id="4e625-122">Managing DDE Shares</span></span>](managing-dde-shares.md)

 

 
