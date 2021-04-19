---
description: Pour sélectionner une carte d’interface réseau (NIC) à partir d’une table d’objets BLOB NPP fournie, appelez la fonction SelectNPPBlobFromTable.
ms.assetid: e75b6bb7-cf21-4e25-80a5-3b35f7ed0d0e
title: Sélection d’une carte d’interface réseau à partir d’une table d’objets BLOB NPP fournie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0215ca258c02745a7e5b4c285d6bf7df98a49e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531879"
---
# <a name="selecting-a-nic-from-a-supplied-npp-blob-table"></a><span data-ttu-id="fc1a8-103">Sélection d’une carte d’interface réseau à partir d’une table d’objets BLOB NPP fournie</span><span class="sxs-lookup"><span data-stu-id="fc1a8-103">Selecting a NIC from a Supplied NPP BLOB table</span></span>

<span data-ttu-id="fc1a8-104">Pour sélectionner une carte d’interface réseau (NIC) à partir d’une table d’objets BLOB NPP fournie, appelez la fonction [**SelectNPPBlobFromTable**](selectnppblobfromtable.md) .</span><span class="sxs-lookup"><span data-stu-id="fc1a8-104">To select a network interface card (NIC) from a supplied NPP BLOB table, call the [**SelectNPPBlobFromTable**](selectnppblobfromtable.md) function.</span></span> <span data-ttu-id="fc1a8-105">Cette fonction utilise l’interface utilisateur Moniteur réseau pour afficher les cartes réseau représentées dans la table d’objets BLOB et retourne l’objet BLOB NPP qui représente la carte réseau sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="fc1a8-105">This function uses the Network Monitor UI to display the NICs represented in the BLOB table and returns the NPP BLOB that represents the selected NIC.</span></span>

<span data-ttu-id="fc1a8-106">Quand vous appelez la fonction [**SelectNPPBlobFromTable**](selectnppblobfromtable.md) , la boîte de dialogue **Sélectionner un réseau** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="fc1a8-106">When you call the [**SelectNPPBlobFromTable**](selectnppblobfromtable.md) function, the **Select a network** dialog box appears.</span></span> <span data-ttu-id="fc1a8-107">À partir de celle-ci, vous pouvez afficher les détails du NPPs représenté dans la table d’objets BLOB NPP, sélectionner une carte réseau spécifique et afficher les détails de sa structure d’objet BLOB NPP associée.</span><span class="sxs-lookup"><span data-stu-id="fc1a8-107">From it, you can view the details of the NPPs represented in the NPP BLOB table, select a specific NIC, and view the details of its associated NPP BLOB structure.</span></span>

<span data-ttu-id="fc1a8-108">L’illustration suivante montre les cartes réseau représentées dans une table d’objets BLOB NPP fournie.</span><span class="sxs-lookup"><span data-stu-id="fc1a8-108">The following illustration shows the NICs represented in a supplied NPP BLOB table.</span></span>

![cartes réseau représentées dans une table d’objets BLOB NPP fournie](images/networkdb2.png)



| <span data-ttu-id="fc1a8-110">Pour plus d’informations sur l’un des sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="fc1a8-110">For more information about</span></span>                        | <span data-ttu-id="fc1a8-111">Consultez</span><span class="sxs-lookup"><span data-stu-id="fc1a8-111">See</span></span>                                                                                                      |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc1a8-112">Sélection d’une carte d’interface réseau inscrite sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="fc1a8-112">Selecting a NIC registered on the local computer.</span></span> | [<span data-ttu-id="fc1a8-113">Comment sélectionner une carte réseau enregistrée</span><span class="sxs-lookup"><span data-stu-id="fc1a8-113">How to select a registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="fc1a8-114">Récupération d’une table d’objets BLOB NPP.</span><span class="sxs-lookup"><span data-stu-id="fc1a8-114">Retrieving an NPP BLOB table.</span></span>                     | [<span data-ttu-id="fc1a8-115">Comment sélectionner une carte réseau à partir d’une table BLOB NPP retournée</span><span class="sxs-lookup"><span data-stu-id="fc1a8-115">How to select a NIC from a Returned NPP BLOB table</span></span>](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



