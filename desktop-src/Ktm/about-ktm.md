---
description: Le gestionnaire de transactions KTM (Kernel Transaction Manager) est un service de gestion des transactions. Il rend les transactions disponibles en tant qu’objets noyau et fournit des services de gestion des transactions aux composants système tels que le NTFS transactionnel (TxF).
ms.assetid: 85a79698-a1ae-45a4-805e-25175034fa65
title: À propos de KTM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1c477c7f9ae54b86fcee03435310416b38ea8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035220"
---
# <a name="about-ktm"></a><span data-ttu-id="948a0-104">À propos de KTM</span><span class="sxs-lookup"><span data-stu-id="948a0-104">About KTM</span></span>

<span data-ttu-id="948a0-105">Le gestionnaire de transactions KTM (Kernel Transaction Manager) est un service de gestion des transactions.</span><span class="sxs-lookup"><span data-stu-id="948a0-105">Kernel Transaction Manager (KTM) is a transaction management service.</span></span> <span data-ttu-id="948a0-106">Il rend les transactions disponibles en tant qu’objets noyau et fournit des services de gestion des transactions aux composants système tels que le [NTFS transactionnel](/windows/desktop/FileIO/transactional-ntfs-portal) (TxF).</span><span class="sxs-lookup"><span data-stu-id="948a0-106">It makes transactions available as kernel objects and provides transaction management services to system components such as [Transactional NTFS](/windows/desktop/FileIO/transactional-ntfs-portal) (TxF).</span></span>

<span data-ttu-id="948a0-107">Les rubriques suivantes décrivent les utilisations et les fonctionnalités de KTM :</span><span class="sxs-lookup"><span data-stu-id="948a0-107">The following topics describe the uses and features of KTM:</span></span>

-   [<span data-ttu-id="948a0-108">Qu’est-ce qu’une transaction ?</span><span class="sxs-lookup"><span data-stu-id="948a0-108">What is a Transaction?</span></span>](what-is-a-transaction.md)
-   [<span data-ttu-id="948a0-109">Utilisation des transactions</span><span class="sxs-lookup"><span data-stu-id="948a0-109">Working With Transactions</span></span>](programming-model.md)
-   [<span data-ttu-id="948a0-110">Écriture d’un Gestionnaire des ressources</span><span class="sxs-lookup"><span data-stu-id="948a0-110">Writing a Resource Manager</span></span>](writing-a-resource-manager.md)
-   [<span data-ttu-id="948a0-111">Interopérabilité avec d’autres fonctionnalités Windows</span><span class="sxs-lookup"><span data-stu-id="948a0-111">Interoperability With Other Windows Features</span></span>](interoperability-with-other-windows-features.md)
-   [<span data-ttu-id="948a0-112">Sécurité KTM et droits d’accès</span><span class="sxs-lookup"><span data-stu-id="948a0-112">KTM Security and Access Rights</span></span>](ktm-security-and-access-rights.md)

<span data-ttu-id="948a0-113">KTM s’appuie sur le [Common Log File System](/previous-versions/windows/desktop/clfs/common-log-file-system-portal) pour son fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="948a0-113">KTM relies on the [Common Log File System](/previous-versions/windows/desktop/clfs/common-log-file-system-portal) for its operation.</span></span> <span data-ttu-id="948a0-114">CLFS est un système de journalisation qui est capable d’activer des transactions.</span><span class="sxs-lookup"><span data-stu-id="948a0-114">CLFS is a logging system that is capable of enabling transactions.</span></span>

 

 
