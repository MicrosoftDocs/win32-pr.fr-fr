---
description: En utilisant le sous-système de carte à puce, vous pouvez communiquer avec des cartes qui peuvent ne pas se conformer aux spécifications ISO 7816.
ms.assetid: ea6cfa5a-2abf-4b7f-b3f4-99655266f030
title: Fonctions d’accès direct aux cartes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad360974210114a1069db3226ee814d08008cc98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861985"
---
# <a name="direct-card-access-functions"></a><span data-ttu-id="9c46b-103">Fonctions d’accès direct aux cartes</span><span class="sxs-lookup"><span data-stu-id="9c46b-103">Direct Card Access Functions</span></span>

<span data-ttu-id="9c46b-104">En utilisant le sous-système de [*carte à puce*](/windows/desktop/SecGloss/s-gly) , vous pouvez communiquer avec des cartes qui peuvent ne pas se conformer aux spécifications ISO 7816.</span><span class="sxs-lookup"><span data-stu-id="9c46b-104">By using the [*smart card*](/windows/desktop/SecGloss/s-gly) subsystem, you can communicate with cards that may not conform to the ISO 7816 specifications.</span></span> <span data-ttu-id="9c46b-105">Pour ce faire, les fonctions suivantes vous permettent de contrôler les attributs des communications entre l’application et la carte en vous donnant une manipulation directe et de bas niveau du [*lecteur*](/windows/desktop/SecGloss/r-gly).</span><span class="sxs-lookup"><span data-stu-id="9c46b-105">To do this, the following functions let you control the attributes of the communications between the application and the card by giving you direct, low-level manipulation of the [*reader*](/windows/desktop/SecGloss/r-gly).</span></span>

<span data-ttu-id="9c46b-106">Pour utiliser ces fonctions, vous devez fournir un identificateur pour l’attribut en question.</span><span class="sxs-lookup"><span data-stu-id="9c46b-106">To use these functions, you have to supply an identifier for the attribute in question.</span></span> <span data-ttu-id="9c46b-107">Pour obtenir des identificateurs et des valeurs d’attributs valides, consultez la table 3-1 dans *Requirements for PC-Connected Interface Devices*.</span><span class="sxs-lookup"><span data-stu-id="9c46b-107">For valid attribute identifiers and values, refer to Table 3-1 in *Requirements for PC-Connected Interface Devices*.</span></span>



| <span data-ttu-id="9c46b-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="9c46b-108">Topic</span></span>                                    | <span data-ttu-id="9c46b-109">Description</span><span class="sxs-lookup"><span data-stu-id="9c46b-109">Description</span></span>                           |
|------------------------------------------|---------------------------------------|
| [<span data-ttu-id="9c46b-110">**SCardControl**</span><span class="sxs-lookup"><span data-stu-id="9c46b-110">**SCardControl**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardcontrol)     | <span data-ttu-id="9c46b-111">Fournissez un contrôle direct du lecteur.</span><span class="sxs-lookup"><span data-stu-id="9c46b-111">Provide direct control of the reader.</span></span> |
| [<span data-ttu-id="9c46b-112">**SCardGetAttrib**</span><span class="sxs-lookup"><span data-stu-id="9c46b-112">**SCardGetAttrib**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardgetattrib) | <span data-ttu-id="9c46b-113">Obtient les attributs de lecteur.</span><span class="sxs-lookup"><span data-stu-id="9c46b-113">Get reader attributes.</span></span>                |
| [<span data-ttu-id="9c46b-114">**SCardSetAttrib**</span><span class="sxs-lookup"><span data-stu-id="9c46b-114">**SCardSetAttrib**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardsetattrib) | <span data-ttu-id="9c46b-115">Définissez l’attribut Reader.</span><span class="sxs-lookup"><span data-stu-id="9c46b-115">Set reader attribute.</span></span>                 |



 

 

 
