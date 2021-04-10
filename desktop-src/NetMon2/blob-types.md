---
description: Moniteur réseau utilise trois types d’objets BLOB (Binary Large Objects) pour sélectionner et connecter des cartes d’interface réseau (NIC), capturer des données et manipuler des données NPP.
ms.assetid: f7cbceb1-1a85-4a05-8420-90b32c9c9b61
title: Types d’objets BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029c375c446d53074cc0c9797dfa2992b2b2d933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210582"
---
# <a name="blob-types"></a><span data-ttu-id="4dc4c-103">Types d’objets BLOB</span><span class="sxs-lookup"><span data-stu-id="4dc4c-103">BLOB Types</span></span>

<span data-ttu-id="4dc4c-104">Moniteur réseau utilise trois types d’objets BLOB (Binary Large Objects) pour sélectionner et connecter des cartes d’interface réseau (NIC), capturer des données et manipuler des données NPP.</span><span class="sxs-lookup"><span data-stu-id="4dc4c-104">Network Monitor uses three types of binary large objects (BLOBs) to select and connect network interface cards (NICs), capture data, and manipulate NPP data.</span></span>

## <a name="npp-blob"></a><span data-ttu-id="4dc4c-105">OBJET BLOB NPP</span><span class="sxs-lookup"><span data-stu-id="4dc4c-105">NPP BLOB</span></span>

<span data-ttu-id="4dc4c-106">Les applications utilisent des objets BLOB NPP pour se connecter à une carte réseau spécifique via un NPP.</span><span class="sxs-lookup"><span data-stu-id="4dc4c-106">Applications use NPP BLOBs to connect to a specific NIC through an NPP.</span></span> <span data-ttu-id="4dc4c-107">(L’application établit la connexion avec un appel à **CreateNPPInterface** et les données d’emplacement dans l’objet BLOB NPP.) Une application peut également stocker ses données de configuration dans l’objet BLOB NPP pour configurer le NPP.</span><span class="sxs-lookup"><span data-stu-id="4dc4c-107">(The application makes the connection with a call to **CreateNPPInterface** and location data in the NPP BLOB.) An application can also store its configuration data in the NPP BLOB to configure the NPP.</span></span> <span data-ttu-id="4dc4c-108">En outre, une application qui enregistre son objet BLOB NPP n’est pas obligée de parcourir le Finder pour réutiliser cet objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="4dc4c-108">Also, an application that saves its NPP BLOB is not required to go through the Finder to reuse that BLOB.</span></span>

## <a name="filter-blob"></a><span data-ttu-id="4dc4c-109">Filtrer l’objet BLOB</span><span class="sxs-lookup"><span data-stu-id="4dc4c-109">Filter BLOB</span></span>

<span data-ttu-id="4dc4c-110">Un objet BLOB de filtres contient des critères définis par l’application que vous pouvez utiliser pour sélectionner un NPP et une carte réseau.</span><span class="sxs-lookup"><span data-stu-id="4dc4c-110">A filter BLOB contains application-defined criteria that you can use to select an NPP and a NIC.</span></span> <span data-ttu-id="4dc4c-111">Par exemple, une application peut demander une carte réseau spécifique, uniquement des cartes Ethernet ou des cartes qui prennent en charge une fréquence de capture de frame spécifique.</span><span class="sxs-lookup"><span data-stu-id="4dc4c-111">For example, an application can request a specific NIC, only Ethernet cards, or cards that support a specific frame capture rate.</span></span>

## <a name="special-blob"></a><span data-ttu-id="4dc4c-112">Objet BLOB spécial</span><span class="sxs-lookup"><span data-stu-id="4dc4c-112">Special BLOB</span></span>

<span data-ttu-id="4dc4c-113">Lorsqu’un NPP requiert des données supplémentaires avant de pouvoir retourner un objet BLOB NPP à une application, le NPP utilise un objet BLOB spécial.</span><span class="sxs-lookup"><span data-stu-id="4dc4c-113">When an NPP requires additional data before it can return an NPP BLOB to an application, the NPP uses a special BLOB.</span></span> <span data-ttu-id="4dc4c-114">Le plus souvent, l’application n’a pas besoin ou n’utilise pas d’objets BLOB spéciaux afin qu’ils ne soient pas renvoyés à une application, sauf si un indicateur spécifique est défini dans un appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="4dc4c-114">Most often, the application will not need or use special BLOBs so they are not returned to an application unless a specific flag is set in one function call.</span></span> <span data-ttu-id="4dc4c-115">Par exemple, un NPP distant utilise un objet BLOB spécial, car un nom de chemin d’accès est requis pour établir une connexion.</span><span class="sxs-lookup"><span data-stu-id="4dc4c-115">For example, a remote NPP uses a special BLOB because a path name is required to make a connection.</span></span> <span data-ttu-id="4dc4c-116">Une application qui reçoit un objet BLOB spécial NPP distant peut ajouter la chaîne et effectuer un rappel dans le Finder pour obtenir une table BLOB NPP.</span><span class="sxs-lookup"><span data-stu-id="4dc4c-116">An application that receives a remote NPP special BLOB could add the string and call back into the Finder to get an NPP BLOB table.</span></span> <span data-ttu-id="4dc4c-117">Pour plus d’informations, consultez [entrées d’objets BLOB spéciaux](special-blob-entries.md).</span><span class="sxs-lookup"><span data-stu-id="4dc4c-117">For more information, see [Special BLOB Entries](special-blob-entries.md).</span></span>

 

 



