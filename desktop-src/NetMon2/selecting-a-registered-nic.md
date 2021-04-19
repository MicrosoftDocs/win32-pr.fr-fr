---
description: Pour sélectionner l’une des cartes réseau inscrites sur l’ordinateur local, appelez la fonction GetNPPBlobFromUI.
ms.assetid: ca1fb07f-7eee-419f-b25d-49718d02fc7d
title: Sélection d’une carte réseau enregistrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b7047d5bbb46797210e18782c672cfd81b9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534453"
---
# <a name="selecting-a-registered-nic"></a><span data-ttu-id="9d7fc-103">Sélection d’une carte réseau enregistrée</span><span class="sxs-lookup"><span data-stu-id="9d7fc-103">Selecting a Registered NIC</span></span>

<span data-ttu-id="9d7fc-104">Pour sélectionner l’une des cartes réseau inscrites sur l’ordinateur local, appelez la fonction [**GetNPPBlobFromUI**](getnppblobfromui.md) .</span><span class="sxs-lookup"><span data-stu-id="9d7fc-104">To select one of the NICs registered on the local computer, call the [**GetNPPBlobFromUI**](getnppblobfromui.md) function.</span></span> <span data-ttu-id="9d7fc-105">Cette fonction utilise l’interface utilisateur Moniteur réseau pour afficher les cartes réseau enregistrées et retourne l’objet BLOB NPP qui représente la carte réseau que vous sélectionnez.</span><span class="sxs-lookup"><span data-stu-id="9d7fc-105">This function uses the Network Monitor UI to display the registered NICs and returns the NPP BLOB that represents the NIC you select.</span></span> <span data-ttu-id="9d7fc-106">Vous pouvez afficher toutes les cartes réseau inscrites sur l’ordinateur local ou un plus petit ensemble de cartes réseau filtrées.</span><span class="sxs-lookup"><span data-stu-id="9d7fc-106">You can display all the NICs registered on the local computer or a smaller set of filtered NICs.</span></span> <span data-ttu-id="9d7fc-107">Pour filtrer les cartes réseau affichées, fournissez un [*objet blob de filtres*](f.md) lorsque l’appel est effectué.</span><span class="sxs-lookup"><span data-stu-id="9d7fc-107">To filter the displayed NICs, provide a [*filter BLOB*](f.md) when the call is made.</span></span>

> [!Note]  
> <span data-ttu-id="9d7fc-108">Lorsque la fonction [**GetNPPBlobFromUI**](getnppblobfromui.md) est appelée, le [*Finder NPP*](n.md) communique avec les dll NPP pour obtenir les structures BLOB NPP qui représentent les cartes réseau inscrites.</span><span class="sxs-lookup"><span data-stu-id="9d7fc-108">When the [**GetNPPBlobFromUI**](getnppblobfromui.md) function is called, the [*NPP Finder*](n.md) communicates with the NPP DLLs to obtain the NPP BLOB structures that represent the registered NICs.</span></span> <span data-ttu-id="9d7fc-109">Pour plus d’informations et pour obtenir une procédure sur l’utilisation directe de l’interface utilisateur du Moniteur réseau, consultez la rubrique « boîte de dialogue Sélectionner un réseau » dans l’aide en ligne de Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="9d7fc-109">For more information, and a procedure about how to use the Network Monitor UI directly, see the "Select a Network Dialog Box" topic in the Network Monitor online help.</span></span>

 

<span data-ttu-id="9d7fc-110">Quand vous appelez la fonction [**GetNPPBlobFromUI**](getnppblobfromui.md) , la boîte de dialogue **Sélectionner un réseau** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="9d7fc-110">When you call the [**GetNPPBlobFromUI**](getnppblobfromui.md) function, the **Select a network** dialog box appears.</span></span> <span data-ttu-id="9d7fc-111">À partir de celle-ci, vous pouvez afficher les détails du NPPs inscrit sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="9d7fc-111">From it, you can view the details of the NPPs registered on the local computer.</span></span> <span data-ttu-id="9d7fc-112">Ces informations incluent les NPPs locaux et les NPPs distants.</span><span class="sxs-lookup"><span data-stu-id="9d7fc-112">This information includes both local NPPs and remote NPPs.</span></span> <span data-ttu-id="9d7fc-113">À partir de la boîte de dialogue, vous pouvez sélectionner une carte réseau spécifique et afficher les détails de sa structure d’objet BLOB NPP associée.</span><span class="sxs-lookup"><span data-stu-id="9d7fc-113">From the dialog box, you can select a specific NIC and view the details of its associated NPP BLOB structure.</span></span>

<span data-ttu-id="9d7fc-114">L’illustration suivante montre les paramètres typiques d’un NPP NDIS fourni par Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="9d7fc-114">The following illustration shows typical settings of an NDIS NPP supplied by Network Monitor.</span></span>

![paramètres standard d’un NPP NDIS fourni par le moniteur réseau](images/networkdb.png)

<span data-ttu-id="9d7fc-116">Le tableau suivant répertorie les rubriques qui décrivent chaque méthode de sélection de carte réseau.</span><span class="sxs-lookup"><span data-stu-id="9d7fc-116">The following table lists topics that describe each NIC selection method.</span></span>



| <span data-ttu-id="9d7fc-117">Pour obtenir des informations sur</span><span class="sxs-lookup"><span data-stu-id="9d7fc-117">For information about</span></span>                                                                          | <span data-ttu-id="9d7fc-118">Consultez</span><span class="sxs-lookup"><span data-stu-id="9d7fc-118">See</span></span>                                                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d7fc-119">Comment spécifier un filtre qui limite les cartes réseau affichées dans la boîte de dialogue **Sélectionner un réseau** .</span><span class="sxs-lookup"><span data-stu-id="9d7fc-119">How to specify a filter that limits the NICs displayed in the **Select a network** dialog box.</span></span> | [<span data-ttu-id="9d7fc-120">Spécification d’un objet BLOB de filtre</span><span class="sxs-lookup"><span data-stu-id="9d7fc-120">Specifying a Filter BLOB</span></span>](specifying-a-filter-blob.md)                                             |
| <span data-ttu-id="9d7fc-121">Comment sélectionner une carte réseau en appelant la fonction [**GetNPPBlobFromUI**](getnppblobfromui.md) .</span><span class="sxs-lookup"><span data-stu-id="9d7fc-121">How to select a NIC by calling the [**GetNPPBlobFromUI**](getnppblobfromui.md) function.</span></span>      | [<span data-ttu-id="9d7fc-122">Sélection d’une carte réseau à l’aide de GetNPPBlobFromUI</span><span class="sxs-lookup"><span data-stu-id="9d7fc-122">Selecting a NIC using GetNPPBlobFromUI</span></span>](getnppblobfromui.md)                                       |
| <span data-ttu-id="9d7fc-123">Comment sélectionner une carte réseau à partir d’une table d’objets BLOB NPP fournie.</span><span class="sxs-lookup"><span data-stu-id="9d7fc-123">How to select a NIC from a supplied NPP BLOB table.</span></span>                                            | [<span data-ttu-id="9d7fc-124">Sélection d’une carte d’interface réseau à partir d’une table d’objets BLOB NPP fournie</span><span class="sxs-lookup"><span data-stu-id="9d7fc-124">Selecting a NIC from a Supplied NPP BLOB Table</span></span>](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



