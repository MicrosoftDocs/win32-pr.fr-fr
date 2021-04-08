---
description: Les fonctions de message de bas niveau encodent les données pour transmettre et décoder les données qui ont été reçues. Les fonctions de message de bas niveau déchiffrent et vérifient également les signatures des messages reçus.
ms.assetid: 42c19920-c7f7-4a4d-9de3-3de9a34fbe0c
title: Fonctions de message de bas niveau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22654f19dfe5178dfb98006c17c2d0536f78cd46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752132"
---
# <a name="low-level-message-functions"></a><span data-ttu-id="6c828-104">Fonctions de message de bas niveau</span><span class="sxs-lookup"><span data-stu-id="6c828-104">Low-level Message Functions</span></span>

<span data-ttu-id="6c828-105">Les [*fonctions de message de bas niveau*](../secgloss/l-gly.md) encodent les données pour transmettre et décoder les données qui ont été reçues.</span><span class="sxs-lookup"><span data-stu-id="6c828-105">The [*low-level message functions*](../secgloss/l-gly.md) encode data for transmission and decode data that has been received.</span></span> <span data-ttu-id="6c828-106">Les fonctions de message de bas niveau déchiffrent et vérifient également les signatures des messages reçus.</span><span class="sxs-lookup"><span data-stu-id="6c828-106">Low-level message functions also decrypt and verify the signatures of received messages.</span></span>

<span data-ttu-id="6c828-107">Lorsqu’un message est ouvert à l’aide d’une fonction d’ouverture de message de bas niveau, il reste ouvert et disponible (conserve son [*État*](../secgloss/s-gly.md)) jusqu’à ce qu’il soit fermé.</span><span class="sxs-lookup"><span data-stu-id="6c828-107">When a message is opened using a low-level message open function, it remains open and available (maintains its [*state*](../secgloss/s-gly.md)) until it is closed.</span></span> <span data-ttu-id="6c828-108">Cela permet de construire un message fragmentaire à l’aide de plusieurs appels à la fonction [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) .</span><span class="sxs-lookup"><span data-stu-id="6c828-108">This allows a message to be constructed piecemeal using multiple calls to the [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) function.</span></span>

<span data-ttu-id="6c828-109">L’utilisation de fonctions de message de bas niveau requiert davantage d’appels de fonction que l’utilisation de fonctions de message simplifiées (voir [messages simplifiés](simplified-messages.md)).</span><span class="sxs-lookup"><span data-stu-id="6c828-109">Using low-level message functions requires more function calls than using simplified message functions (see [Simplified Messages](simplified-messages.md)).</span></span> <span data-ttu-id="6c828-110">Si les fonctions de message simplifiées sont utilisées, une plus grande partie du travail est effectuée à l’intérieur des fonctions de l’API.</span><span class="sxs-lookup"><span data-stu-id="6c828-110">If the simplified message functions are used, more of the work is done inside the functions of the API.</span></span>

<span data-ttu-id="6c828-111">L’utilisation de fonctions de message de bas niveau implique l’exécution d’appels à d’autres fonctions de certificat ou de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="6c828-111">Using low-level message functions involves the additional work of making calls to other certificate or cryptographic functions.</span></span> <span data-ttu-id="6c828-112">Par exemple, les données des appels aux fonctions de certificat peuvent être nécessaires pour initialiser les structures utilisées par ces fonctions de message de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="6c828-112">For example, data from calls to certificate functions may be needed to initialize structures used by these low-level message functions.</span></span> <span data-ttu-id="6c828-113">Les fonctions de message simplifiées initialisent un grand nombre de ces structures en interne.</span><span class="sxs-lookup"><span data-stu-id="6c828-113">Simplified message functions initialize many of these structures internally.</span></span>

<span data-ttu-id="6c828-114">Le tableau suivant répertorie les sections avec des descriptions de procédure et des exemples de code C qui utilisent les fonctions de message de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="6c828-114">The following table lists sections with procedure descriptions and C code examples of using the low-level message functions.</span></span>



| <span data-ttu-id="6c828-115">Section</span><span class="sxs-lookup"><span data-stu-id="6c828-115">Section</span></span>                                                                               | <span data-ttu-id="6c828-116">Contents</span><span class="sxs-lookup"><span data-stu-id="6c828-116">Contents</span></span>                                           |
|---------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="6c828-117">Fonctions de message de bas niveau</span><span class="sxs-lookup"><span data-stu-id="6c828-117">Low-level Message Functions</span></span>](cryptography-functions.md) | <span data-ttu-id="6c828-118">Répertorie les fonctions de message de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="6c828-118">Lists the low-level message functions.</span></span>             |
| [<span data-ttu-id="6c828-119">Signature des données</span><span class="sxs-lookup"><span data-stu-id="6c828-119">Signing Data</span></span>](signing-data.md)                                                      | <span data-ttu-id="6c828-120">Détaille les tâches nécessaires à la signature des données.</span><span class="sxs-lookup"><span data-stu-id="6c828-120">Details the tasks needed to sign data.</span></span>             |
| [<span data-ttu-id="6c828-121">Encodage de données enveloppées</span><span class="sxs-lookup"><span data-stu-id="6c828-121">Encoding Enveloped Data</span></span>](encoding-enveloped-data.md)                                | <span data-ttu-id="6c828-122">Détaille les tâches nécessaires pour encoder les données enveloppées.</span><span class="sxs-lookup"><span data-stu-id="6c828-122">Details the tasks needed to encode enveloped data.</span></span> |
| [<span data-ttu-id="6c828-123">Décodage des données enveloppées</span><span class="sxs-lookup"><span data-stu-id="6c828-123">Decoding Enveloped Data</span></span>](decoding-enveloped-data.md)                                | <span data-ttu-id="6c828-124">Détaille les tâches nécessaires pour décoder les données enveloppées.</span><span class="sxs-lookup"><span data-stu-id="6c828-124">Details the tasks needed to decode enveloped data.</span></span> |



 

 

 
