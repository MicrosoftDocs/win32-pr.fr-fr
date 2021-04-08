---
description: L’action RegisterUser enregistre les informations utilisateur avec le programme d’installation pour identifier l’utilisateur d’un produit.
ms.assetid: da615cb4-d36d-4180-8f97-c9f83c0df1c6
title: Action RegisterUser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686628d29094f951994b072ad4451a383a405965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756465"
---
# <a name="registeruser-action"></a><span data-ttu-id="509b4-103">Action RegisterUser</span><span class="sxs-lookup"><span data-stu-id="509b4-103">RegisterUser Action</span></span>

<span data-ttu-id="509b4-104">L’action RegisterUser enregistre les informations utilisateur avec le programme d’installation pour identifier l’utilisateur d’un produit.</span><span class="sxs-lookup"><span data-stu-id="509b4-104">The RegisterUser action registers the user information with the installer to identify the user of a product.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="509b4-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="509b4-105">Sequence Restrictions</span></span>

<span data-ttu-id="509b4-106">Il n’existe aucune restriction de séquence.</span><span class="sxs-lookup"><span data-stu-id="509b4-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="509b4-107">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="509b4-107">ActionData Messages</span></span>



| <span data-ttu-id="509b4-108">Champ</span><span class="sxs-lookup"><span data-stu-id="509b4-108">Field</span></span> | <span data-ttu-id="509b4-109">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="509b4-109">Description of action data</span></span>   |
|-------|------------------------------|
| <span data-ttu-id="509b4-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="509b4-110">\[1\]</span></span> | <span data-ttu-id="509b4-111">Informations sur l’utilisateur inscrit.</span><span class="sxs-lookup"><span data-stu-id="509b4-111">Registered user information.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="509b4-112">Notes</span><span class="sxs-lookup"><span data-stu-id="509b4-112">Remarks</span></span>

<span data-ttu-id="509b4-113">L’action RegisterUser n’est pas effectuée au cours d’une installation d’administration.</span><span class="sxs-lookup"><span data-stu-id="509b4-113">The RegisterUser action is not performed during an administrative installation.</span></span> <span data-ttu-id="509b4-114">Si l’identificateur de produit entré par l’utilisateur n’a pas été validé par l' [Action ValidateProductID](validateproductid-action.md), la propriété [**ProductID**](productid.md) n’est pas définie et cette action n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="509b4-114">If the product identifier entered by the user has not been validated by the [ValidateProductID action](validateproductid-action.md), the [**ProductID**](productid.md) property is not set and this action does nothing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="509b4-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="509b4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="509b4-116">**NOM d’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="509b4-116">**USERNAME**</span></span>](username.md)
</dt> <dt>

[<span data-ttu-id="509b4-117">**PRENNENT**</span><span class="sxs-lookup"><span data-stu-id="509b4-117">**COMPANYNAME**</span></span>](companyname.md)
</dt> <dt>

[<span data-ttu-id="509b4-118">**Réf**</span><span class="sxs-lookup"><span data-stu-id="509b4-118">**ProductID**</span></span>](productid.md)
</dt> </dl>

 

 



