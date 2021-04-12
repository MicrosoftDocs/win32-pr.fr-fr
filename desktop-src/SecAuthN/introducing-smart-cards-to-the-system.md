---
description: Pour que le sous-système de carte à puce puisse trouver une carte à puce, la carte à puce doit être introduite sur le système.
ms.assetid: 5b331d7d-9440-4e0d-a73b-48a2a556c31c
title: Présentation des cartes à puce au système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9134dd9efce17b60f3495bf7bfc36b03c34ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210014"
---
# <a name="introducing-smart-cards-to-the-system"></a><span data-ttu-id="6295e-103">Présentation des cartes à puce au système</span><span class="sxs-lookup"><span data-stu-id="6295e-103">Introducing Smart Cards to the System</span></span>

<span data-ttu-id="6295e-104">Pour que le [*sous-système de carte à*](../secgloss/s-gly.md) puce puisse trouver une [*carte*](../secgloss/s-gly.md)à puce, la carte à puce doit être introduite sur le système.</span><span class="sxs-lookup"><span data-stu-id="6295e-104">Before the [*smart card subsystem*](../secgloss/s-gly.md) can find a [*smart card*](../secgloss/s-gly.md), the smart card must be introduced to the system.</span></span> <span data-ttu-id="6295e-105">Cette opération est généralement effectuée à l’aide d’un outil de configuration de carte à puce fourni par le fabricant de la carte.</span><span class="sxs-lookup"><span data-stu-id="6295e-105">This is typically done with a smart card setup tool provided by the card manufacturer.</span></span> <span data-ttu-id="6295e-106">L’outil peut être un programme sur une disquette (avec la carte à puce), un contrôle ActiveX disponible sur un site Web, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="6295e-106">The tool could come as a program on a floppy disk (with the smart card), an ActiveX control available on a website, and so on.</span></span>

<span data-ttu-id="6295e-107">L’outil d’installation doit fournir les informations suivantes sur la carte :</span><span class="sxs-lookup"><span data-stu-id="6295e-107">The setup tool must provide the following pieces of information about the card:</span></span>

-   <span data-ttu-id="6295e-108">Sa [*chaîne ATR*](../secgloss/a-gly.md)et un masque facultatif à utiliser comme aide pour identifier la carte.</span><span class="sxs-lookup"><span data-stu-id="6295e-108">Its [*ATR string*](../secgloss/a-gly.md), and an optional mask to use as an aid in identifying the card.</span></span>
-   <span data-ttu-id="6295e-109">Liste des interfaces de carte à puce prises en charge par la carte.</span><span class="sxs-lookup"><span data-stu-id="6295e-109">A list of smart card interfaces supported by the card.</span></span>
-   <span data-ttu-id="6295e-110">Nom complet de la carte, à utiliser pour identifier la carte à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6295e-110">A display name for the card, to be used in identifying the card to the user.</span></span> <span data-ttu-id="6295e-111">Dans la plupart des cas, l’utilisateur le fournira à l’outil d’installation.</span><span class="sxs-lookup"><span data-stu-id="6295e-111">In most cases, the user will supply this to the setup tool.</span></span>
-   <span data-ttu-id="6295e-112">[*Fournisseur de services principal*](../secgloss/p-gly.md) associé à la carte (facultatif) à utiliser lors de l’accès à la carte via des interfaces com.</span><span class="sxs-lookup"><span data-stu-id="6295e-112">The [*primary service provider*](../secgloss/p-gly.md) associated with the card (optional), to be used when accessing the card through COM interfaces.</span></span>

<span data-ttu-id="6295e-113">Pour simplifier les outils d’installation et garantir l’intégrité de la [*base de données des cartes à puce*](../secgloss/s-gly.md), le sous-système de carte à puce fournit les deux fonctions suivantes.</span><span class="sxs-lookup"><span data-stu-id="6295e-113">To simplify setup tools, and to ensure the integrity of the [*smart card database*](../secgloss/s-gly.md), the smart card subsystem provides the following two functions.</span></span> <span data-ttu-id="6295e-114">[**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) introduit une carte à puce dans la base de données et [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) le supprime de la base de données.</span><span class="sxs-lookup"><span data-stu-id="6295e-114">[**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) introduces a smart card into the database and [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) removes it from the database.</span></span>

 

 
