---
description: L’Action ValidateProductID définit la propriété ProductID sur l’identificateur complet du produit.
ms.assetid: 31b2f9d2-98d5-4cf3-af02-f12de2740bb8
title: Action ValidateProductID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d0f9f58641e8e24d73a1acae0b79cc0b875aba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519348"
---
# <a name="validateproductid-action"></a><span data-ttu-id="cc423-103">Action ValidateProductID</span><span class="sxs-lookup"><span data-stu-id="cc423-103">ValidateProductID Action</span></span>

<span data-ttu-id="cc423-104">L’Action ValidateProductID définit la propriété [**ProductID**](productid.md) sur l’identificateur complet du produit.</span><span class="sxs-lookup"><span data-stu-id="cc423-104">The ValidateProductID action sets the [**ProductID**](productid.md) property to the full product identifier.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="cc423-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="cc423-105">Sequence Restrictions</span></span>

<span data-ttu-id="cc423-106">Cette action doit être séquencée avant l’Assistant interface utilisateur dans la [table InstallUISequence](installuisequence-table.md) et avant l' [action RegisterUser](registeruser-action.md) dans la [table InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="cc423-106">This action must be sequenced before the user interface wizard in the [InstallUISequence table](installuisequence-table.md) and before the [RegisterUser action](registeruser-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="cc423-107">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="cc423-107">ActionData Messages</span></span>

<span data-ttu-id="cc423-108">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="cc423-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc423-109">Notes</span><span class="sxs-lookup"><span data-stu-id="cc423-109">Remarks</span></span>

<span data-ttu-id="cc423-110">Le programme d’installation vérifie si un produit a été validé avec succès en vérifiant la propriété [**ProductID**](productid.md) .</span><span class="sxs-lookup"><span data-stu-id="cc423-110">The installer checks whether a product has validated successfully by checking the [**ProductID**](productid.md) property.</span></span> <span data-ttu-id="cc423-111">Le programme d’installation définit la propriété **ProductID** sur l’identificateur de produit complet après une validation réussie.</span><span class="sxs-lookup"><span data-stu-id="cc423-111">The installer sets the **ProductID** property to the full product identifier after a successful validation.</span></span> <span data-ttu-id="cc423-112">L’Action ValidateProductID ne fait rien si la propriété **ProductID** a déjà été définie par une validation réussie ou par une autre méthode.</span><span class="sxs-lookup"><span data-stu-id="cc423-112">The ValidateProductID action does nothing if the **ProductID** property has already been set by a successful validation or by another method.</span></span>

<span data-ttu-id="cc423-113">L’Action ValidateProductID retourne toujours un succès, que l’identificateur de produit soit valide ou non, afin que l’identificateur de produit puisse être entré sur la ligne de commande lors de la première exécution du produit.</span><span class="sxs-lookup"><span data-stu-id="cc423-113">The ValidateProductID action always returns a success, whether or not the product identifier is valid, so that the product identifier can be entered on the command line the first time the product is run.</span></span>

<span data-ttu-id="cc423-114">L’identificateur de produit peut être validé sans que l’utilisateur ne resaisisse ces informations en définissant la propriété [**PIDKEY**](pidkey.md) sur la ligne de commande ou en utilisant une transformation.</span><span class="sxs-lookup"><span data-stu-id="cc423-114">The product identifier can be validated without having the user reenter this information by setting the [**PIDKEY**](pidkey.md) property on the command line or by using a transform.</span></span> <span data-ttu-id="cc423-115">L’affichage de la boîte de dialogue demandant à l’utilisateur d’entrer l’identificateur de produit peut ensuite être rendu conditionnel sur la présence de la propriété [**ProductID**](productid.md) , qui est définie lorsque la propriété **PIDKEY** est validée.</span><span class="sxs-lookup"><span data-stu-id="cc423-115">The display of the dialog box requesting the user to enter the product identifier can then be made conditional upon the presence of the [**ProductID**](productid.md) property, which is set when the **PIDKEY** property is validated.</span></span>

 

 



