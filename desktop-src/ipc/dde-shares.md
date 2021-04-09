---
description: Les partages DDE sont des ressources de machine.
ms.assetid: 98d24300-52cc-4f0d-b74f-c58b823ac5f3
title: Partages DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 012c219897187c9e68b5b9e662b93678b77974c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865590"
---
# <a name="dde-shares"></a><span data-ttu-id="41457-103">Partages DDE</span><span class="sxs-lookup"><span data-stu-id="41457-103">DDE Shares</span></span>

<span data-ttu-id="41457-104">\[Le DDE réseau n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="41457-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="41457-105">Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]</span><span class="sxs-lookup"><span data-stu-id="41457-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="41457-106">Les partages DDE sont des ressources de machine.</span><span class="sxs-lookup"><span data-stu-id="41457-106">DDE shares are a machine resource.</span></span> <span data-ttu-id="41457-107">Ils sont similaires aux partages de fichiers, car ils permettent de contrôler l’accès à une ressource.</span><span class="sxs-lookup"><span data-stu-id="41457-107">They are similar to file shares because they are used to control access to a resource.</span></span> <span data-ttu-id="41457-108">Avec les partages de fichiers, la ressource est un fichier.</span><span class="sxs-lookup"><span data-stu-id="41457-108">With file shares, the resource is a file.</span></span> <span data-ttu-id="41457-109">Avec les partages DDE, la ressource est des données échangées dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="41457-109">With DDE shares, the resource is dynamically exchanged data.</span></span> <span data-ttu-id="41457-110">Le type de données échangées est déterminé par l’application serveur qui fournit les données et l’application cliente qui demande les données.</span><span class="sxs-lookup"><span data-stu-id="41457-110">The type of data exchanged is determined by the server application that supplies the data and the client application that requests the data.</span></span>

<span data-ttu-id="41457-111">Le serveur appelle la fonction [**NDdeShareAdd**](nddeshareadd.md) pour créer le partage DDE, qui est stocké dans le gestionnaire de base de données du partage DDE (DSDM).</span><span class="sxs-lookup"><span data-stu-id="41457-111">The server calls the [**NDdeShareAdd**](nddeshareadd.md) function to create the DDE share, which is stored in the DDE share database manager (DSDM).</span></span>

<span data-ttu-id="41457-112">Le client démarre la conversation DDE en se connectant au partage DDE.</span><span class="sxs-lookup"><span data-stu-id="41457-112">The client starts the DDE conversation by connecting to the DDE share.</span></span> <span data-ttu-id="41457-113">Le client doit appeler la fonction [**DdeInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) pour initialiser Ddeml et appeler la fonction [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) pour se connecter au partage DDE.</span><span class="sxs-lookup"><span data-stu-id="41457-113">The client must call the [**DdeInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) function to initialize DDEML and call the [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) function to connect to the DDE share.</span></span> <span data-ttu-id="41457-114">Dans l’appel **DdeConnect** , le client spécifie le nom du service comme suit :</span><span class="sxs-lookup"><span data-stu-id="41457-114">In the **DdeConnect** call, the client specifies the service name as follows:</span></span>

<span data-ttu-id="41457-115">\\\\*Nom de l’ordinateur* \\ NDDE $</span><span class="sxs-lookup"><span data-stu-id="41457-115">\\\\*ComputerName*\\NDDE$</span></span>

<span data-ttu-id="41457-116">où *nom_ordinateur* est le nom de l’ordinateur qui exécute l’application serveur.</span><span class="sxs-lookup"><span data-stu-id="41457-116">where *ComputerName* is the name of the computer running the server application.</span></span> <span data-ttu-id="41457-117">NDDE $ indique que la rubrique fournie à [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) est le nom de partage DDE sur l’ordinateur distant nommé *ComputerName*.</span><span class="sxs-lookup"><span data-stu-id="41457-117">The NDDE$ indicates that the topic provided to [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) is the DDE share name on the remote computer named *ComputerName*.</span></span>

<span data-ttu-id="41457-118">Il existe trois types de partages DDE : ancien style, nouveau style et statique.</span><span class="sxs-lookup"><span data-stu-id="41457-118">There are three types of DDE shares: old style, new style, and static.</span></span> <span data-ttu-id="41457-119">Il est courant de prendre uniquement en charge le type statique.</span><span class="sxs-lookup"><span data-stu-id="41457-119">It is typical to support only the static type.</span></span> <span data-ttu-id="41457-120">Les noms des partages statiques utilisent la Convention suivante : *Nom_Partage*$.</span><span class="sxs-lookup"><span data-stu-id="41457-120">The names of static shares use the following convention: *ShareName*$.</span></span>

 

 
