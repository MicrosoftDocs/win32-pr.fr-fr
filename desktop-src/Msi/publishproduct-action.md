---
description: L’action PublishProduct gère la publication des informations sur le produit avec le système. Cette action publie le produit si le produit est en mode publication ou si une fonctionnalité est en cours d’installation ou de réinstallation.
ms.assetid: aba1baf2-d282-4f76-87aa-67188b779535
title: Action PublishProduct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9edf95ccb736bb4a4388f36d87bfbfbe299573e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519095"
---
# <a name="publishproduct-action"></a><span data-ttu-id="8face-104">Action PublishProduct</span><span class="sxs-lookup"><span data-stu-id="8face-104">PublishProduct Action</span></span>

<span data-ttu-id="8face-105">L’action PublishProduct gère la publication des informations sur le produit avec le système.</span><span class="sxs-lookup"><span data-stu-id="8face-105">The PublishProduct action manages the advertisement of the product information with the system.</span></span> <span data-ttu-id="8face-106">Cette action publie le produit si le produit est en mode publication ou si une fonctionnalité est en cours d’installation ou de réinstallation.</span><span class="sxs-lookup"><span data-stu-id="8face-106">This action publishes the product if the product is in advertise mode or if any feature is being installed or reinstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="8face-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="8face-107">Sequence Restrictions</span></span>

<span data-ttu-id="8face-108">L’action PublishProduct doit venir après l’action [PublishFeatures](publishfeatures-action.md) .</span><span class="sxs-lookup"><span data-stu-id="8face-108">The PublishProduct action must come after the [PublishFeatures](publishfeatures-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="8face-109">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="8face-109">ActionData Messages</span></span>



| <span data-ttu-id="8face-110">Champ</span><span class="sxs-lookup"><span data-stu-id="8face-110">Field</span></span> | <span data-ttu-id="8face-111">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="8face-111">Description of Action Data</span></span>        |
|-------|-----------------------------------|
| <span data-ttu-id="8face-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="8face-112">\[1\]</span></span> | <span data-ttu-id="8face-113">Identificateur du produit publié.</span><span class="sxs-lookup"><span data-stu-id="8face-113">Identifier of advertised product.</span></span> |



 

 

 



