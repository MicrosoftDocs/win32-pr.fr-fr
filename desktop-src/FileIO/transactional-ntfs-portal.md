---
description: Le NTFS transactionnel (TxF) autorise l’exécution d’opérations de fichiers sur un volume de système de fichiers NTFS dans une transaction.
ms.assetid: e8c3ceed-d391-4934-b3f7-12c2123c8c23
title: NTFS transactionnel (TxF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7553bfc7cae0b5389762527f0ac726c674a6a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524927"
---
# <a name="transactional-ntfs-txf"></a><span data-ttu-id="cefc0-103">NTFS transactionnel (TxF)</span><span class="sxs-lookup"><span data-stu-id="cefc0-103">Transactional NTFS (TxF)</span></span>

<span data-ttu-id="cefc0-104">\[Microsoft recommande vivement aux développeurs d’utiliser d’autres moyens pour répondre aux besoins de votre application.</span><span class="sxs-lookup"><span data-stu-id="cefc0-104">\[Microsoft strongly recommends developers utilize alternative means to achieve your application s needs.</span></span> <span data-ttu-id="cefc0-105">De nombreux scénarios pour lesquels TxF a été développé peuvent être obtenus à l’aide de techniques plus simples et plus facilement disponibles.</span><span class="sxs-lookup"><span data-stu-id="cefc0-105">Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques.</span></span> <span data-ttu-id="cefc0-106">En outre, TxF peut ne pas être disponible dans les versions futures de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="cefc0-106">Furthermore, TxF may not be available in future versions of Microsoft Windows.</span></span> <span data-ttu-id="cefc0-107">Pour plus d’informations et pour obtenir des alternatives à TxF, consultez [alternatives à l’utilisation de NTFS transactionnel](deprecation-of-txf.md).\]</span><span class="sxs-lookup"><span data-stu-id="cefc0-107">For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](deprecation-of-txf.md).\]</span></span>

## <a name="purpose"></a><span data-ttu-id="cefc0-108">Objectif</span><span class="sxs-lookup"><span data-stu-id="cefc0-108">Purpose</span></span>

<span data-ttu-id="cefc0-109">Le NTFS transactionnel (TxF) autorise l’exécution d’opérations de fichiers sur un volume de système de fichiers NTFS dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="cefc0-109">Transactional NTFS (TxF) allows file operations on an NTFS file system volume to be performed in a transaction.</span></span> <span data-ttu-id="cefc0-110">Les transactions TxF augmentent la fiabilité des applications en protégeant l’intégrité des données des défaillances et simplifient le développement d’applications en réduisant considérablement la quantité de code de gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="cefc0-110">TxF transactions increase application reliability by protecting data integrity across failures and simplify application development by greatly reducing the amount of error handling code.</span></span>

<span data-ttu-id="cefc0-111">TxF utilise l’infrastructure de transaction fournie par le gestionnaire de transactions KTM ( [Kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal) ).</span><span class="sxs-lookup"><span data-stu-id="cefc0-111">TxF uses the transaction framework provided by the [Kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal) (KTM).</span></span> <span data-ttu-id="cefc0-112">Cela permet aux opérations de fichier TxF de faire partie d’une transaction impliquant d’autres sources de données telles que SQL Server et le registre transactionnel (TxR).</span><span class="sxs-lookup"><span data-stu-id="cefc0-112">This allows TxF file operations to be part of a transaction involving other data sources such as SQL Server and Transacted Registry (TxR).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="cefc0-113">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="cefc0-113">Where applicable</span></span>

<span data-ttu-id="cefc0-114">Une application peut utiliser TxF pour préserver l’intégrité des données sur le disque suite à des conditions d’erreur inattendues et aider à résoudre des scénarios d’utilisateur de système de fichiers simultanés en isolant les modifications apportées par d’autres utilisateurs pendant les modifications.</span><span class="sxs-lookup"><span data-stu-id="cefc0-114">An application can use TxF to preserve the integrity of data on disk caused by unexpected error conditions and help resolve concurrent file-system user scenarios by isolating your changes from others while the changes are being made.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="cefc0-115">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="cefc0-115">Developer audience</span></span>

<span data-ttu-id="cefc0-116">Avant d’utiliser TxF, vous devez avoir une connaissance opérationnelle des transactions à l’aide de KTM ou [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cefc0-116">Before using TxF, you should have a working knowledge of transactions using either KTM or [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="cefc0-117">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="cefc0-117">Run-time requirements</span></span>

<span data-ttu-id="cefc0-118">TxF est disponible à partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cefc0-118">TxF is available starting with Windows Vista.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cefc0-119">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="cefc0-119">In this section</span></span>



| <span data-ttu-id="cefc0-120">Rubrique</span><span class="sxs-lookup"><span data-stu-id="cefc0-120">Topic</span></span>                                                    | <span data-ttu-id="cefc0-121">Description</span><span class="sxs-lookup"><span data-stu-id="cefc0-121">Description</span></span>                                                                                                |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cefc0-122">À propos de</span><span class="sxs-lookup"><span data-stu-id="cefc0-122">About</span></span>](about-transactional-ntfs.md)<br/>         | <span data-ttu-id="cefc0-123">Informations générales sur le NTFS transactionnel.</span><span class="sxs-lookup"><span data-stu-id="cefc0-123">General information about Transactional NTFS.</span></span><br/>                                                   |
| [<span data-ttu-id="cefc0-124">Référence</span><span class="sxs-lookup"><span data-stu-id="cefc0-124">Reference</span></span>](transactional-ntfs-reference.md)<br/> | <span data-ttu-id="cefc0-125">Documentation pour les fonctions, les structures de données, les énumérations et d’autres éléments de programmation.</span><span class="sxs-lookup"><span data-stu-id="cefc0-125">Documentation for the functions, data structures, enumerations, and other programming elements.</span></span><br/> |



 

 

