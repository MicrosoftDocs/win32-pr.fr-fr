---
description: Connectez-vous et communiquez avec une carte à puce spécifique.
ms.assetid: 37d92491-174b-471e-b36e-46d9285dd404
title: Fonctions d’accès aux lecteurs et aux cartes à puce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7202b2d6165b49bfe80e55f15c4d69cb4a6909a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521322"
---
# <a name="smart-card-and-reader-access-functions"></a><span data-ttu-id="4f06f-103">Fonctions d’accès aux lecteurs et aux cartes à puce</span><span class="sxs-lookup"><span data-stu-id="4f06f-103">Smart Card and Reader Access Functions</span></span>

<span data-ttu-id="4f06f-104">Les fonctions suivantes se connectent à une carte à [*puce*](../secgloss/s-gly.md)spécifique et la communiquent avec celle-ci.</span><span class="sxs-lookup"><span data-stu-id="4f06f-104">The following functions connect to and communicate with a specific [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="4f06f-105">Les opérations d’e/s vers la carte utilisent une mémoire tampon pour l’envoi ou la réception de données et une structure qui contient des informations de contrôle de protocole.</span><span class="sxs-lookup"><span data-stu-id="4f06f-105">I/O operations to the card use a buffer for sending or receiving data and a structure that contains protocol control information.</span></span> <span data-ttu-id="4f06f-106">La structure des informations de contrôle de protocole commence toujours par une structure de [**\_ \_ demande d’e/s**](scard-io-request.md) inactive.</span><span class="sxs-lookup"><span data-stu-id="4f06f-106">The protocol control information structure always begins with an [**SCARD\_IO\_REQUEST**](scard-io-request.md) structure.</span></span>



| <span data-ttu-id="4f06f-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="4f06f-107">Topic</span></span>                                                  | <span data-ttu-id="4f06f-108">Description</span><span class="sxs-lookup"><span data-stu-id="4f06f-108">Description</span></span>                                                                                                                                                                                                                                |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f06f-109">**SCardConnect**</span><span class="sxs-lookup"><span data-stu-id="4f06f-109">**SCardConnect**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardconnecta)                   | <span data-ttu-id="4f06f-110">Connectez-vous à une carte.</span><span class="sxs-lookup"><span data-stu-id="4f06f-110">Connect to a card.</span></span>                                                                                                                                                                                                                         |
| [<span data-ttu-id="4f06f-111">**SCardReconnect**</span><span class="sxs-lookup"><span data-stu-id="4f06f-111">**SCardReconnect**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardreconnect)               | <span data-ttu-id="4f06f-112">Rétablissez une connexion.</span><span class="sxs-lookup"><span data-stu-id="4f06f-112">Reestablish a connection.</span></span>                                                                                                                                                                                                                  |
| [<span data-ttu-id="4f06f-113">**SCardDisconnect**</span><span class="sxs-lookup"><span data-stu-id="4f06f-113">**SCardDisconnect**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scarddisconnect)             | <span data-ttu-id="4f06f-114">Mettre fin à une connexion.</span><span class="sxs-lookup"><span data-stu-id="4f06f-114">Terminate a connection.</span></span>                                                                                                                                                                                                                    |
| [<span data-ttu-id="4f06f-115">**SCardBeginTransaction**</span><span class="sxs-lookup"><span data-stu-id="4f06f-115">**SCardBeginTransaction**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardbegintransaction) | <span data-ttu-id="4f06f-116">Démarrer une [*transaction*](../secgloss/t-gly.md), empêchant les autres applications d’accéder à une carte.</span><span class="sxs-lookup"><span data-stu-id="4f06f-116">Start a [*transaction*](../secgloss/t-gly.md), blocking other applications from accessing a card.</span></span>                                                                                            |
| [<span data-ttu-id="4f06f-117">**SCardEndTransaction**</span><span class="sxs-lookup"><span data-stu-id="4f06f-117">**SCardEndTransaction**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardendtransaction)     | <span data-ttu-id="4f06f-118">Mettre fin à une transaction, ce qui permet à d’autres applications d’accéder à une carte.</span><span class="sxs-lookup"><span data-stu-id="4f06f-118">End a transaction, allowing other applications to access a card.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="4f06f-119">**SCardStatus**</span><span class="sxs-lookup"><span data-stu-id="4f06f-119">**SCardStatus**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardstatusa)                     | <span data-ttu-id="4f06f-120">Indiquez l’état actuel du lecteur.</span><span class="sxs-lookup"><span data-stu-id="4f06f-120">Provide the current status of the reader.</span></span>                                                                                                                                                                                                  |
| [<span data-ttu-id="4f06f-121">**SCardTransmit**</span><span class="sxs-lookup"><span data-stu-id="4f06f-121">**SCardTransmit**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)                 | <span data-ttu-id="4f06f-122">Demande le service et reçoit des données à partir d’une carte à l’aide de [*t = 0*](../secgloss/t-gly.md), [*t = 1*](../secgloss/t-gly.md)et des protocoles bruts.</span><span class="sxs-lookup"><span data-stu-id="4f06f-122">Requests service and receives data back from a card using [*T=0*](../secgloss/t-gly.md), [*T=1*](../secgloss/t-gly.md), and raw protocols.</span></span> |



 

 

 
