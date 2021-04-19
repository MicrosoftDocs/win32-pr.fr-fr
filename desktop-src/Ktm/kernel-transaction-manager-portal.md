---
description: Implémentez le NTFS transactionnel (TxF) et le registre transactionnel (TxR). TxF autorise les opérations de système de fichiers transactionnelles au sein de NTFS. TxR autorise les opérations de Registre transactionnelles. Coordonner les opérations du système de fichiers et du Registre avec une transaction.
ms.assetid: 2f601994-db1e-4aac-8db1-9a36c702664b
title: Gestionnaire de transactions du noyau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281050461163d5fd0cde64af79e70569d613888e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536835"
---
# <a name="kernel-transaction-manager"></a><span data-ttu-id="98977-106">Gestionnaire de transactions du noyau</span><span class="sxs-lookup"><span data-stu-id="98977-106">Kernel Transaction Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="98977-107">Objectif</span><span class="sxs-lookup"><span data-stu-id="98977-107">Purpose</span></span>

<span data-ttu-id="98977-108">Le gestionnaire de transactions KTM (Kernel Transaction Manager) permet le développement d’applications qui utilisent des transactions.</span><span class="sxs-lookup"><span data-stu-id="98977-108">The Kernel Transaction Manager (KTM) enables the development of applications that use transactions.</span></span> <span data-ttu-id="98977-109">Le moteur de transactions se trouve dans le noyau, mais les transactions peuvent être développées pour les transactions en mode noyau ou utilisateur, et au sein d’un seul hôte ou de plusieurs hôtes distribués.</span><span class="sxs-lookup"><span data-stu-id="98977-109">The transaction engine itself is within the kernel, but transactions can be developed for kernel- or user-mode transactions, and within a single host or among distributed hosts.</span></span>

<span data-ttu-id="98977-110">Le KTM est utilisé pour implémenter le NTFS transactionnel (TxF) et le registre transactionnel (TxR).</span><span class="sxs-lookup"><span data-stu-id="98977-110">The KTM is used to implement Transactional NTFS (TxF) and Transactional Registry (TxR).</span></span> <span data-ttu-id="98977-111">TxF autorise les opérations de système de fichiers transactionnelles au sein du système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="98977-111">TxF allows transacted file system operations within the NTFS file system.</span></span> <span data-ttu-id="98977-112">TxR autorise les opérations de Registre transactionnelles.</span><span class="sxs-lookup"><span data-stu-id="98977-112">TxR allows transacted registry operations.</span></span> <span data-ttu-id="98977-113">KTM permet aux applications clientes de coordonner les opérations du système de fichiers et du Registre avec une transaction.</span><span class="sxs-lookup"><span data-stu-id="98977-113">KTM enables client applications to coordinate file system and registry operations with a transaction.</span></span>

<span data-ttu-id="98977-114">Pour développer une application qui coordonne les transactions avec des ressources autres que TxF ou TxR, vous devez d’abord développer un service prenant en charge les transactions Win32, également appelé gestionnaire de ressources.</span><span class="sxs-lookup"><span data-stu-id="98977-114">To develop an application that coordinates transactions with resources other than TxF or TxR, you must first develop a Win32 transaction-aware service, also called a resource manager.</span></span>

<span data-ttu-id="98977-115">Les applications managées et COM+ doivent utiliser leurs gestionnaires de transactions natifs.</span><span class="sxs-lookup"><span data-stu-id="98977-115">Managed and COM+ applications should use their native transaction managers.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="98977-116">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="98977-116">Where applicable</span></span>

<span data-ttu-id="98977-117">KTM peut être utilisé avec des applications et des gestionnaires de ressources hébergés sur Windows Vista ou Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="98977-117">KTM can be used with applications and resource managers hosted on Windows Vista or Windows Server 2008.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="98977-118">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="98977-118">Developer audience</span></span>

<span data-ttu-id="98977-119">L’API KTM est conçue pour être utilisée par les programmeurs C et C++.</span><span class="sxs-lookup"><span data-stu-id="98977-119">The KTM API is designed for use by C and C++ programmers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="98977-120">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="98977-120">Run-time requirements</span></span>

<span data-ttu-id="98977-121">Le KTM est pris en charge à partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="98977-121">KTM is supported starting with Windows Vista.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="98977-122">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="98977-122">In this section</span></span>



| <span data-ttu-id="98977-123">Rubrique</span><span class="sxs-lookup"><span data-stu-id="98977-123">Topic</span></span>                                     | <span data-ttu-id="98977-124">Description</span><span class="sxs-lookup"><span data-stu-id="98977-124">Description</span></span>                                                                                                       |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98977-125">À propos de</span><span class="sxs-lookup"><span data-stu-id="98977-125">About</span></span>](about-ktm.md)<br/>         | <span data-ttu-id="98977-126">Informations générales sur les transactions et les fonctionnalités fournies par KTM.</span><span class="sxs-lookup"><span data-stu-id="98977-126">General information about transactions and the capabilities provided by KTM.</span></span><br/>                           |
| [<span data-ttu-id="98977-127">Référence</span><span class="sxs-lookup"><span data-stu-id="98977-127">Reference</span></span>](ktm-reference.md)<br/> | <span data-ttu-id="98977-128">Documentation pour les fonctions, les structures de données, les énumérations et d’autres éléments de programmation KTM.</span><span class="sxs-lookup"><span data-stu-id="98977-128">Documentation for the functions, data structures, enumerations, and other programming elements of KTM.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="98977-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="98977-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98977-130">Common Log File System</span><span class="sxs-lookup"><span data-stu-id="98977-130">Common Log File System</span></span>](/previous-versions/windows/desktop/clfs/common-log-file-system-portal)
</dt> <dt>

[<span data-ttu-id="98977-131">NTFS transactionnel (TxF)</span><span class="sxs-lookup"><span data-stu-id="98977-131">Transactional NTFS (TxF)</span></span>](/windows/desktop/FileIO/transactional-ntfs-portal)
</dt> <dt>

<span data-ttu-id="98977-132">[Coordinateur de transactions distribuées](/previous-versions/windows/desktop/ms684146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="98977-132">[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))</span></span>
</dt> </dl>

 

