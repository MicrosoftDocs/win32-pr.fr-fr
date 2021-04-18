---
title: Gestion de l’alimentation (services de base GPC)
description: Le TBS reçoit des événements de gestion de l’alimentation.
ms.assetid: 21f76bea-a313-46b7-99b3-422f17376a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e21f2c6a2292b7d49fae3b15691703fa34667a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2019
ms.locfileid: "106512294"
---
# <a name="power-management-tpm-base-services"></a><span data-ttu-id="6a787-103">Gestion de l’alimentation (services de base GPC)</span><span class="sxs-lookup"><span data-stu-id="6a787-103">Power Management (TPM Base Services)</span></span>

<span data-ttu-id="6a787-104">Le TBS reçoit des événements de gestion de l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="6a787-104">The TBS receives power management events.</span></span> <span data-ttu-id="6a787-105">Lors de la réception d’une indication indiquant que le module de plateforme sécurisée (TPM) ou d’autres parties de la plateforme vont entrer dans un état d’alimentation dans lequel l’exécution est interrompue ou que l’état du module de plateforme sécurisée est perdu, le TBS vérifie si la commande en cours d’exécution est susceptible de se terminer avant que le système ne soit hors tension.</span><span class="sxs-lookup"><span data-stu-id="6a787-105">When an indication is received that the TPM or other parts of the platform are about to enter a power state in which execution will be interrupted or TPM state will be lost, the TBS checks to determine whether the currently executing command is likely to finish before the system powers down.</span></span> <span data-ttu-id="6a787-106">En général, le TBS permet de terminer les commandes de durées courtes et moyennes, mais annule les commandes de longue durée.</span><span class="sxs-lookup"><span data-stu-id="6a787-106">In general, the TBS allows short and medium duration commands to finish, but cancels long duration commands.</span></span> <span data-ttu-id="6a787-107">Une fois que la commande a été retournée, le TBS cesse d’envoyer de nouvelles commandes au module de plateforme sécurisée et se prépare à la mise en veille prolongée.</span><span class="sxs-lookup"><span data-stu-id="6a787-107">After the command has returned, the TBS stops sending new commands to the TPM and prepares itself for hibernation.</span></span> <span data-ttu-id="6a787-108">Lorsque l’alimentation est restaurée, le TBS retourne le résultat de la commande à l’appelant, puis poursuit le traitement des commandes TBS en attente.</span><span class="sxs-lookup"><span data-stu-id="6a787-108">When power is restored, the TBS returns the result of the command to the caller, and then proceeds with processing pending TBS commands.</span></span> <span data-ttu-id="6a787-109">Le code de gestion de l’alimentation TBS s’exécute de manière asynchrone, de sorte qu’il peut gérer les demandes de gestion de l’alimentation, même si le module de plateforme sécurisée traite une longue commande.</span><span class="sxs-lookup"><span data-stu-id="6a787-109">The TBS power management code runs asynchronously, so it can handle power management requests even if the TPM is processing a long command.</span></span>

<span data-ttu-id="6a787-110">Lorsqu’un ordinateur entre en état de veille, y compris S3 (veille) et S4 (mise en veille prolongée), le module de plateforme sécurisée est éteint.</span><span class="sxs-lookup"><span data-stu-id="6a787-110">When a computer enters sleep states, including S3 (sleep) and S4 (hibernation), the TPM is powered off.</span></span> <span data-ttu-id="6a787-111">Par conséquent, tous les États TPM non persistants sont perdus.</span><span class="sxs-lookup"><span data-stu-id="6a787-111">Thus, all nonpersistent TPM states are lost.</span></span> <span data-ttu-id="6a787-112">Avant d’entrer dans ces États, les logiciels d’application sont censés se préparer à la perte des États de module de plateforme sécurisée volatils.</span><span class="sxs-lookup"><span data-stu-id="6a787-112">Before entering these states, application software is expected to prepare for the loss of volatile TPM states.</span></span> <span data-ttu-id="6a787-113">Lorsque le système revient d’un état de veille, le TBS se synchronise avec le module de plateforme sécurisée afin que l’état de TBS soit cohérent avec l’état du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="6a787-113">When the system returns from a sleep state, the TBS synchronizes with the TPM so that the TBS state is consistent with the TPM state.</span></span> <span data-ttu-id="6a787-114">Les logiciels d’application devront peut-être réémettre des commandes qui ont été interrompues.</span><span class="sxs-lookup"><span data-stu-id="6a787-114">Application software may need to reissue commands that were interrupted.</span></span>

 

 




