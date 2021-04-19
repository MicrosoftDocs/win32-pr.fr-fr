---
description: Dans Windows Vista, les compteurs de performances implémentaient une nouvelle architecture (version 2,0) pour fournir des données de compteur.
ms.assetid: c17eda2f-3cf8-40d6-8be6-c1ce190d1a26
title: Fourniture de données de compteur
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: ed5aa4cc505baab9e15d3f69c3fb466712eddbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529834"
---
# <a name="providing-counter-data"></a><span data-ttu-id="f1fab-103">Fourniture de données de compteur</span><span class="sxs-lookup"><span data-stu-id="f1fab-103">Providing Counter Data</span></span>

<span data-ttu-id="f1fab-104">Les composants logiciels qui publient des données par le biais des compteurs de performances Windows sont appelés fournisseurs de données de performances.</span><span class="sxs-lookup"><span data-stu-id="f1fab-104">Software components that publish data via Windows Performance Counters are called performance data providers.</span></span>

<span data-ttu-id="f1fab-105">Windows prend en charge deux types de fournisseurs de données de performances.</span><span class="sxs-lookup"><span data-stu-id="f1fab-105">Windows supports two kinds of performance data providers.</span></span> <span data-ttu-id="f1fab-106">Les fournisseurs de données de performance hérités (**fournisseurs v1**) sont implémentés à l’aide d’un. Fichier INI et une DLL de performance.</span><span class="sxs-lookup"><span data-stu-id="f1fab-106">Legacy performance data providers (**V1 providers**) are implemented using an .INI file and a performance DLL.</span></span> <span data-ttu-id="f1fab-107">Les fournisseurs de données de performances modernes (**fournisseurs v2**) utilisent un. MAN (manifeste XML) et les API du fournisseur de compteurs de performances.</span><span class="sxs-lookup"><span data-stu-id="f1fab-107">Modern performance data providers (**V2 providers**) use a .MAN (XML manifest) and the performance counter provider APIs.</span></span>

## <a name="manifests"></a><span data-ttu-id="f1fab-108">Manifestes</span><span class="sxs-lookup"><span data-stu-id="f1fab-108">Manifests</span></span>

<span data-ttu-id="f1fab-109">Les fournisseurs de données de performances modernes utilisent un. MAN (manifeste XML) pour définir les données de compteur et utiliser les API du fournisseur de compteurs de performance pour gérer les données dans le contexte du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f1fab-109">Modern performance data providers use a .MAN (XML manifest) to define the counter data and use performance counter provider APIs to manage data within the context of the provider.</span></span>

<span data-ttu-id="f1fab-110">Les fournisseurs implémentés à l’aide d’un manifeste et des API du fournisseur de compteurs de performances sont souvent appelés **fournisseurs v2**.</span><span class="sxs-lookup"><span data-stu-id="f1fab-110">Providers implemented using a manifest and performance counter provider APIs are often called **V2 providers**.</span></span>

<span data-ttu-id="f1fab-111">Windows prend en charge les fournisseurs V2 en mode utilisateur sur Windows Vista ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f1fab-111">Windows supports user-mode V2 providers on Windows Vista or later.</span></span> <span data-ttu-id="f1fab-112">Pour plus d’informations sur le mode utilisateur, consultez [fourniture de données de compteurs à l’aide de la Version 2,0](providing-counter-data-using-version-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="f1fab-112">For user-mode details, see [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md).</span></span>

<span data-ttu-id="f1fab-113">Windows prend en charge les fournisseurs V2 en mode noyau sur Windows 7 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f1fab-113">Windows supports kernel-mode V2 providers on Windows 7 or later.</span></span> <span data-ttu-id="f1fab-114">Pour plus d’informations sur le mode noyau, consultez [surveillance des performances en mode noyau](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).</span><span class="sxs-lookup"><span data-stu-id="f1fab-114">For kernel-mode details, see [Kernel Mode Performance Monitoring](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).</span></span>

## <a name="performance-dll-deprecated"></a><span data-ttu-id="f1fab-115">DLL de performance (déconseillée)</span><span class="sxs-lookup"><span data-stu-id="f1fab-115">Performance DLL (deprecated)</span></span>

<span data-ttu-id="f1fab-116">Dans l’architecture du compteur de performances hérité, les fournisseurs ont implémenté une DLL de performance dans qui s’exécutait dans le processus du consommateur pour collecter et fournir les données de compteur lorsqu’un consommateur l’a demandé.</span><span class="sxs-lookup"><span data-stu-id="f1fab-116">In the legacy performance counter architecture, providers implemented a performance DLL to that ran in the consumer's process to collect and provide the counter data when a consumer requested it.</span></span> <span data-ttu-id="f1fab-117">Le fournisseur a utilisé une initialisation (. INI) et les entrées de Registre pour définir les compteurs et configurer la DLL de performance.</span><span class="sxs-lookup"><span data-stu-id="f1fab-117">The provider used an initialization (.INI) file and registry entries to define the counters and to configure the performance DLL.</span></span>

<span data-ttu-id="f1fab-118">Fournisseurs implémentés à l’aide d’un. Les fichiers INI et les DLL de performance sont souvent appelés **fournisseurs v1**.</span><span class="sxs-lookup"><span data-stu-id="f1fab-118">Providers implemented using an .INI file and a performance DLL are often called **V1 providers**.</span></span>

> [!CAUTION]
> <span data-ttu-id="f1fab-119">Bien que vous puissiez toujours utiliser une DLL de performance pour fournir des données de compteur, cette architecture est dépréciée en raison de limitations de performances et de fiabilité significatives.</span><span class="sxs-lookup"><span data-stu-id="f1fab-119">Although you can still use a performance DLL to provide counter data, this architecture is deprecated due to significant performance and reliability limitations.</span></span> <span data-ttu-id="f1fab-120">En outre, les fournisseurs v1 sont souvent plus difficiles à implémenter, car ils requièrent l’expédition d’une DLL distincte qui doit s’exécuter dans le processus du consommateur.</span><span class="sxs-lookup"><span data-stu-id="f1fab-120">In addition, V1 providers are often harder to implement since they require shipping a separate DLL that must run in the consumer's process.</span></span>

<span data-ttu-id="f1fab-121">Pour plus d’informations, consultez [fourniture de données de compteur à l’aide d’une dll de performance](providing-counter-data-using-a-performance-dll.md).</span><span class="sxs-lookup"><span data-stu-id="f1fab-121">For details, see [Providing Counter Data Using a Performance DLL](providing-counter-data-using-a-performance-dll.md).</span></span>
