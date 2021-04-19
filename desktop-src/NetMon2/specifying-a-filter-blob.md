---
description: Lorsque vous sélectionnez une carte d’interface réseau (NIC) inscrite répertoriée sur un ordinateur local, vous pouvez utiliser un objet BLOB de filtre pour ignorer les cartes réseau qui ne vous intéressent pas.
ms.assetid: fa87bb7d-c481-4eb1-b116-b22643a7c9da
title: Spécification d’un objet BLOB de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8754b8f7ea5388b730fd2dfb65e26e24a906d648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529670"
---
# <a name="specifying-a-filter-blob"></a><span data-ttu-id="0faeb-103">Spécification d’un objet BLOB de filtre</span><span class="sxs-lookup"><span data-stu-id="0faeb-103">Specifying a Filter BLOB</span></span>

<span data-ttu-id="0faeb-104">Lorsque vous sélectionnez une carte d’interface réseau (NIC) inscrite répertoriée sur un ordinateur local, vous pouvez utiliser un [*objet blob de filtre*](f.md) pour ignorer les cartes réseau qui ne vous intéressent pas.</span><span class="sxs-lookup"><span data-stu-id="0faeb-104">When you select a registered network interface card (NIC) listed on a local computer, you can use a [*filter BLOB*](f.md) to disregard the NICs you are not interested in.</span></span> <span data-ttu-id="0faeb-105">Par exemple, vous pouvez limiter la recherche pour un type spécifique de carte (comme ETHERNET) ou une adresse MAC spécifique.</span><span class="sxs-lookup"><span data-stu-id="0faeb-105">For example, you could restrict the search for a specific type of card (such as ETHERNET) or a specific MAC address.</span></span>

<span data-ttu-id="0faeb-106">Lors de la recherche d’une carte réseau, chaque entrée de l’objet BLOB de filtre doit correspondre à une entrée équivalente dans l’objet BLOB NPP qui représente la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="0faeb-106">During the search for a NIC, every entry in the filter BLOB must match an equivalent entry in the NPP BLOB that represents the NIC.</span></span> <span data-ttu-id="0faeb-107">Les objets BLOB de filtres peuvent également être des [*objets BLOB spéciaux*](s.md).</span><span class="sxs-lookup"><span data-stu-id="0faeb-107">Filter BLOBs can also be [*special BLOBs*](s.md).</span></span>

<span data-ttu-id="0faeb-108">Lorsque la fonction [**GetNPPBlobFromUI**](getnppblobfromui.md) est appelée, l’objet blob de filtres restreint les cartes réseau affichées dans la boîte de dialogue **Sélectionner un réseau** .</span><span class="sxs-lookup"><span data-stu-id="0faeb-108">When the [**GetNPPBlobFromUI**](getnppblobfromui.md) function is called, the filter BLOB restricts the NICs displayed in the **Select a network** dialog box.</span></span> <span data-ttu-id="0faeb-109">Lorsque la fonction [**GetNPPBlobTable**](getnppblobtable.md) est appelée, l’objet blob de filtres restreint les cartes réseau retournées dans la table d’objets BLOB.</span><span class="sxs-lookup"><span data-stu-id="0faeb-109">When the [**GetNPPBlobTable**](getnppblobtable.md) function is called, the filter BLOB restricts the NICs returned in the BLOB table.</span></span>

<span data-ttu-id="0faeb-110">Pour utiliser le filtre, vous devez créer un objet BLOB de filtre, définir les valeurs des propriétés que vous souhaitez filtrer (y compris les entrées d’objets BLOB spéciales), puis spécifier le filtre d’objet BLOB et un appel à la fonction [**GetNPPBlobTable**](getnppblobtable.md) ou [**GetNPPBlobFromUI**](getnppblobfromui.md) .</span><span class="sxs-lookup"><span data-stu-id="0faeb-110">To use the filter, you must create a filter BLOB, set the values of the properties you want to filter on (including any special BLOB entries), and then specify the BLOB filter and a call to the [**GetNPPBlobTable**](getnppblobtable.md) or [**GetNPPBlobFromUI**](getnppblobfromui.md) function.</span></span>



| <span data-ttu-id="0faeb-111">Pour plus d’informations sur</span><span class="sxs-lookup"><span data-stu-id="0faeb-111">For information on</span></span>                                 | <span data-ttu-id="0faeb-112">Consultez</span><span class="sxs-lookup"><span data-stu-id="0faeb-112">See</span></span>                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0faeb-113">Comment sélectionner une carte réseau inscrite sur un ordinateur local</span><span class="sxs-lookup"><span data-stu-id="0faeb-113">How to select a NIC registered on a local computer</span></span> | [<span data-ttu-id="0faeb-114">Sélection d’une carte réseau enregistrée</span><span class="sxs-lookup"><span data-stu-id="0faeb-114">Selecting a Registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="0faeb-115">Récupération d’une table d’objets BLOB NPP</span><span class="sxs-lookup"><span data-stu-id="0faeb-115">Retrieving an NPP BLOB table</span></span>                       | [<span data-ttu-id="0faeb-116">Sélection d’une carte d’interface réseau à partir d’une table BLOB NPP retournée</span><span class="sxs-lookup"><span data-stu-id="0faeb-116">Selecting a NIC from a Returned NPP BLOB table</span></span>](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



