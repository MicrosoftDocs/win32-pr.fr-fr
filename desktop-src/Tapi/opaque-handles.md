---
description: Quelques types définis par TSPI sont des handles opaques.
ms.assetid: e52ed691-0479-48da-9e06-c6a0d7a20e10
title: Handles opaques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df2e0b0f608b9cefc8f0f4f538bffd452a8aab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527099"
---
# <a name="opaque-handles"></a><span data-ttu-id="4a782-103">Handles opaques</span><span class="sxs-lookup"><span data-stu-id="4a782-103">Opaque Handles</span></span>

<span data-ttu-id="4a782-104">Quelques types définis par TSPI sont des handles opaques.</span><span class="sxs-lookup"><span data-stu-id="4a782-104">A few types defined by TSPI are opaque handles.</span></span> <span data-ttu-id="4a782-105">Celles-ci sont utilisées dans TSPI comme références publiques à des structures de données privées.</span><span class="sxs-lookup"><span data-stu-id="4a782-105">These are used in TSPI as public references to private data structures.</span></span> <span data-ttu-id="4a782-106">Cela permet de vérifier le type des paramètres fournis aux procédures d’interface tout en donnant une mesure de protection de type.</span><span class="sxs-lookup"><span data-stu-id="4a782-106">This allows type-checking of parameters supplied to the interface procedures while still giving a measure of type protection.</span></span> <span data-ttu-id="4a782-107">Seul le propriétaire de la structure de données privées sait comment interpréter le type opaque comme une référence à sa représentation de structure de données.</span><span class="sxs-lookup"><span data-stu-id="4a782-107">Only the owner of the private data structure knows how to interpret the opaque type as a reference to its data structure representation.</span></span> <span data-ttu-id="4a782-108">À titre d’exemple d’utilisation de handles opaques, envisagez un appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="4a782-108">As an example of how opaque handles are used, consider a phone device.</span></span> <span data-ttu-id="4a782-109">TAPI et le fournisseur de services gèrent généralement les structures de données représentant leurs vues respectives de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4a782-109">Both TAPI and the service provider typically maintain data structures representing their respective views of the device.</span></span>

<span data-ttu-id="4a782-110">Dans les structures de données de téléphone classiques gérées par TAPI et un fournisseur de services, chacun contient un handle opaque pour l’autre structure de données.</span><span class="sxs-lookup"><span data-stu-id="4a782-110">In typical phone data structures maintained by TAPI and a service provider, each contains an opaque handle for the other data structure.</span></span> <span data-ttu-id="4a782-111">Celles-ci ont été échangées lors d’une étape d’initialisation précoce.</span><span class="sxs-lookup"><span data-stu-id="4a782-111">These were exchanged at an early initialization step.</span></span> <span data-ttu-id="4a782-112">Lorsque TAPI appelle une fonction TSPI, il passe le handle opaque pour faire référence à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4a782-112">When TAPI calls a TSPI function, it passes the opaque handle to refer to the device.</span></span> <span data-ttu-id="4a782-113">Le fournisseur de services sait comment le résoudre en tant que référence (flèche) à sa structure de données.</span><span class="sxs-lookup"><span data-stu-id="4a782-113">The service provider knows how to resolve this as a reference (arrow) to its data structure.</span></span> <span data-ttu-id="4a782-114">Un processus similaire se produit lorsque le fournisseur de services appelle une fonction de rappel dans TAPI.</span><span class="sxs-lookup"><span data-stu-id="4a782-114">A similar process occurs when the service provider calls a callback function in TAPI.</span></span>

 

 



