---
title: À propos de TBS
description: Service système qui permet le partage transparent des ressources du Module de plateforme sécurisée (TPM) (GPC).
ms.assetid: 5ab3f514-dea9-48f7-97d9-abc774e2a273
keywords:
- Services de base TPM (TBS), à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a5d40b1fca688676978f274cb976afedb6e6a56
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104198744"
---
# <a name="about-tbs"></a><span data-ttu-id="fb02b-104">À propos de TBS</span><span class="sxs-lookup"><span data-stu-id="fb02b-104">About TBS</span></span>

<span data-ttu-id="fb02b-105">La fonctionnalité des services de base du module de plateforme sécurisée (TBS) est un service système qui permet le partage transparent des ressources du Module de plateforme sécurisée (TPM) (GPC).</span><span class="sxs-lookup"><span data-stu-id="fb02b-105">The TPM Base Services (TBS) feature is a system service that allows transparent sharing of the Trusted Platform Module (TPM) resources.</span></span> <span data-ttu-id="fb02b-106">Il partage simultanément les ressources TPM entre plusieurs applications sur le même ordinateur physique, même si ces applications s’exécutent sur des machines virtuelles différentes.</span><span class="sxs-lookup"><span data-stu-id="fb02b-106">It simultaneously shares the TPM resources among multiple applications on the same physical machine, even if those applications run on different virtual machines.</span></span> <span data-ttu-id="fb02b-107">À compter de Windows 8 et de Windows Server 2012, TBS est préinstallé sur tous les systèmes avec un module de plateforme sécurisée (TPM).</span><span class="sxs-lookup"><span data-stu-id="fb02b-107">Starting with Windows 8 and Windows Server 2012, TBS comes pre-installed on all systems with a TPM.</span></span>

<span data-ttu-id="fb02b-108">Le Trusted Computing Group (TCG) définit un Module de plateforme sécurisée (TPM) qui fournit des fonctions de chiffrement conçues pour fournir une confiance dans la plateforme.</span><span class="sxs-lookup"><span data-stu-id="fb02b-108">The Trusted Computing Group (TCG) defines a Trusted Platform Module that provides cryptographic functions designed to provide trust in the platform.</span></span> <span data-ttu-id="fb02b-109">Étant donné que le module de plateforme sécurisée est implémenté dans le matériel, il dispose de ressources limitées.</span><span class="sxs-lookup"><span data-stu-id="fb02b-109">Because the TPM is implemented in hardware, it has finite resources.</span></span> <span data-ttu-id="fb02b-110">Le TCG définit également une pile de logiciels qui utilise ces ressources pour fournir des opérations approuvées pour les logiciels d’application.</span><span class="sxs-lookup"><span data-stu-id="fb02b-110">The TCG also defines a software stack that makes use of these resources to provide trusted operations for application software.</span></span> <span data-ttu-id="fb02b-111">Toutefois, il n’est pas possible d’exécuter une implémentation TSS côte à côte avec des logiciels de système d’exploitation qui peuvent également utiliser des ressources TPM.</span><span class="sxs-lookup"><span data-stu-id="fb02b-111">However, no provision is made for running a TSS implementation side-by-side with operating system software that may also be using TPM resources.</span></span> <span data-ttu-id="fb02b-112">La fonctionnalité TBS résout ce problème en permettant à chaque pile logicielle qui communique avec TBS d’utiliser la vérification des ressources TPM pour toutes les autres piles logicielles qui peuvent s’exécuter sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fb02b-112">The TBS feature solves this problem by enabling each software stack that communicates with TBS to use TPM resources checking for any other software stacks that may be running on the machine.</span></span>

<span data-ttu-id="fb02b-113">La spécification TPM et la spécification de la pile de logiciels TCG (TSS) sont disponibles à l’adresse [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/) .</span><span class="sxs-lookup"><span data-stu-id="fb02b-113">The TPM specification and TCG Software Stack (TSS) specification are available at [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/).</span></span>

<span data-ttu-id="fb02b-114">TBS est implémenté en tant que service hors processus qui accepte les commandes qui utilisent un service RPC.</span><span class="sxs-lookup"><span data-stu-id="fb02b-114">TBS is implemented as an out-of-process service that accepts commands that use an RPC service.</span></span> <span data-ttu-id="fb02b-115">Une bibliothèque liée de manière dynamique présente l’interface du langage C et communique avec le service TBS.</span><span class="sxs-lookup"><span data-stu-id="fb02b-115">A dynamically linked library presents the C language interface and communicates with the TBS service.</span></span>

> [!Note]  
> <span data-ttu-id="fb02b-116">Le service TBS accepte uniquement les demandes RPC de la part de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="fb02b-116">The TBS service only accepts RPC requests from the local machine.</span></span>

 

<span data-ttu-id="fb02b-117">Les principaux objectifs du TBS sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="fb02b-117">The primary goals of the TBS are to:</span></span>

-   <span data-ttu-id="fb02b-118">Fournir un partage efficace des ressources TPM limitées, telles que des emplacements de clés, des emplacements de sessions d’autorisation et des emplacements de transport.</span><span class="sxs-lookup"><span data-stu-id="fb02b-118">Provide efficient sharing of limited TPM resources, such as key slots, authorization sessions slots, and transport slots.</span></span>
-   <span data-ttu-id="fb02b-119">Fournir un accès par ordre de priorité et synchronisé aux ressources du module de plateforme sécurisée entre plusieurs instances de piles de logiciels TPM.</span><span class="sxs-lookup"><span data-stu-id="fb02b-119">Provide prioritized and synchronized access to TPM resources between multiple instances of TPM software stacks.</span></span>
-   <span data-ttu-id="fb02b-120">Fournir une gestion appropriée des ressources du module de plateforme sécurisée dans les États d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="fb02b-120">Provide appropriate management of TPM resources across power states.</span></span>
-   <span data-ttu-id="fb02b-121">Empêcher les piles de logiciels du module de plateforme sécurisée d’accéder aux commandes du module de plateforme sécurisée qui doivent être limitées, en raison des limitations de la plateforme ou des exigences administratives.</span><span class="sxs-lookup"><span data-stu-id="fb02b-121">Prevent TPM software stacks from accessing TPM commands that should be restricted, either because of platform limitations or administrative requirements.</span></span>

<span data-ttu-id="fb02b-122">L’illustration suivante montre la relation entre le TBS et le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="fb02b-122">The following illustration shows the relationship of the TBS to the TPM.</span></span>

![relation entre le TBS en mode utilisateur et le module de plateforme sécurisée en mode noyau](images/tbs-block-diagram-as11601.png)

 

 




