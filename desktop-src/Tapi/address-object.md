---
description: L’objet Address représente une entité qui peut émettre ou recevoir des appels.
ms.assetid: ab6db262-f99e-4027-9525-7597fcf02e72
title: Objet Address
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ae91e70d6d8efb56321ca4619c6eb973799024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866614"
---
# <a name="address-object"></a><span data-ttu-id="9beb1-103">Objet Address</span><span class="sxs-lookup"><span data-stu-id="9beb1-103">Address Object</span></span>

<span data-ttu-id="9beb1-104">L’objet Address représente une entité qui peut émettre ou recevoir des appels.</span><span class="sxs-lookup"><span data-stu-id="9beb1-104">The Address object represents an entity that can make or receive calls.</span></span> <span data-ttu-id="9beb1-105">Cet objet expose des interfaces et des méthodes qui permettent à une application d’effectuer un certain nombre d’opérations, telles que :</span><span class="sxs-lookup"><span data-stu-id="9beb1-105">This object exposes interfaces and methods that allow an application to perform a number of operations, such as:</span></span>

-   <span data-ttu-id="9beb1-106">Détecte si une adresse spécifiée peut prendre en charge un ensemble particulier de besoins de type de média.</span><span class="sxs-lookup"><span data-stu-id="9beb1-106">Discover whether a specified address can support a particular set of media type needs.</span></span>
-   <span data-ttu-id="9beb1-107">Énumérer les appels actuellement associés à l’adresse.</span><span class="sxs-lookup"><span data-stu-id="9beb1-107">Enumerate calls currently associated with the address.</span></span>
-   <span data-ttu-id="9beb1-108">Créer ou transférer des appels.</span><span class="sxs-lookup"><span data-stu-id="9beb1-108">Create or forward calls.</span></span>
-   <span data-ttu-id="9beb1-109">Obtient le nom du fournisseur de services associé.</span><span class="sxs-lookup"><span data-stu-id="9beb1-109">Get the name of the associated service provider.</span></span>
-   <span data-ttu-id="9beb1-110">Si un fournisseur de services multimédia existe, récupérez les pointeurs d’interface qui autorisent la manipulation détaillée des terminaux.</span><span class="sxs-lookup"><span data-stu-id="9beb1-110">If a media service provider exists, get interface pointers that allow detailed terminal manipulation.</span></span>
-   <span data-ttu-id="9beb1-111">Récupérez et définissez d’autres informations, par exemple si un message est en attente.</span><span class="sxs-lookup"><span data-stu-id="9beb1-111">Get and set other information, such as whether a message is waiting.</span></span>

<span data-ttu-id="9beb1-112">La plupart des adresses sont associées à un terminal, mais cela n’est pas uniformément le cas.</span><span class="sxs-lookup"><span data-stu-id="9beb1-112">Most addresses are associated with a terminal, but this is not uniformly the case.</span></span> <span data-ttu-id="9beb1-113">Par exemple, un TSP distant qui fournit l’accès à l’équipement sur un serveur aura une adresse sur l’ordinateur local, mais pas sur un terminal.</span><span class="sxs-lookup"><span data-stu-id="9beb1-113">For example, a remote TSP that provides access to equipment on a server will have an address on the local machine but not a terminal.</span></span> <span data-ttu-id="9beb1-114">Un modem sans conférencier n’a pas non plus de terminal associé à son adresse.</span><span class="sxs-lookup"><span data-stu-id="9beb1-114">A speakerless modem also has no terminal associated with its address.</span></span>

<span data-ttu-id="9beb1-115">Si une adresse n’est pas associée à un terminal, l’interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) n’est pas exposée sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="9beb1-115">If an address does not have an associated terminal, the [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) interface is not exposed on the object.</span></span>

<span data-ttu-id="9beb1-116">L’exemple de code de [sélection d’adresse](select-an-address.md) illustre le processus de base pour l’acquisition d’un pointeur d’objet d’adresse.</span><span class="sxs-lookup"><span data-stu-id="9beb1-116">The [Select an Address](select-an-address.md) code example shows the basic process for acquiring an address object pointer.</span></span>

<span data-ttu-id="9beb1-117">Pour obtenir la liste de toutes les interfaces associées à l’objet Address, consultez [interfaces d’objet Address](address-object-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="9beb1-117">See [Address Object Interfaces](address-object-interfaces.md) for a list of all interfaces associated with the Address object.</span></span>

 

 
