---
title: Conditions requises pour la signature de la fonctionnalité de démarrage sécurisé pour les pilotes en mode noyau
description: Conditions requises pour la signature de la fonctionnalité de démarrage sécurisé pour les pilotes en mode noyau
ms.assetid: 7FF64BA2-89E3-4E6F-B542-7BC7BF7F4FB2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a63a8b1fca1677aa125bac96dfec290dcd736b5
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "106510911"
---
# <a name="secure-boot-feature-signing-requirements-for-kernel-mode-drivers"></a><span data-ttu-id="01503-103">Conditions requises pour la signature de la fonctionnalité de démarrage sécurisé pour les pilotes en mode noyau</span><span class="sxs-lookup"><span data-stu-id="01503-103">Secure boot feature signing requirements for kernel-mode drivers</span></span>

## <a name="platforms"></a><span data-ttu-id="01503-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="01503-104">Platforms</span></span>

<span data-ttu-id="01503-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="01503-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="01503-106">**Serveurs** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="01503-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="01503-107">Description</span><span class="sxs-lookup"><span data-stu-id="01503-107">Description</span></span>

<span data-ttu-id="01503-108">Dans Windows 8 et Windows Server 2012, y compris WinPE, le noyau a été verrouillé pour empêcher les logiciels malveillants introduits par les kits de démarrage ou racine de contourner les exigences de sécurité du système d’exploitation Windows pour les pilotes signés.</span><span class="sxs-lookup"><span data-stu-id="01503-108">In Windows 8 and Windows Server 2012, including WinPE, the kernel has been locked down to prevent malware introduced by boot or root kits from circumventing Windows operating system security requirements for signed drivers.</span></span>

<span data-ttu-id="01503-109">Ce changement affecte tous les pilotes en mode noyau pour les appareils qui prennent en charge le démarrage sécurisé UEFI (Unified Extensible Firmware Interface). Le démarrage sécurisé UEFI est requis pour la certification Windows 8 pour les ordinateurs clients, et facultatif pour les serveurs.</span><span class="sxs-lookup"><span data-stu-id="01503-109">This change affects all kernel-mode drivers for devices that support unified extensible firmware interface (UEFI) Secure Boot; UEFI Secure Boot is required for Windows 8 certification for client machines, and optional for servers.</span></span> <span data-ttu-id="01503-110">Elle n’affecte pas les pilotes en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="01503-110">It does not affect user-mode drivers.</span></span>

<span data-ttu-id="01503-111">Le développement standard pour les pilotes en mode noyau implique soit l’utilisation du débogage en mode noyau, soit le paramètre de données de configuration de démarrage (BCD) <testsigning> .</span><span class="sxs-lookup"><span data-stu-id="01503-111">Standard development for kernel-mode drivers involves either the use of kernel mode debugging or the boot configuration data (BCD) <testsigning> setting.</span></span> <span data-ttu-id="01503-112">Ces deux options sont désactivées lorsque le démarrage sécurisé est activé.</span><span class="sxs-lookup"><span data-stu-id="01503-112">Both of these are disabled when Secured Boot is on.</span></span>

## <a name="manifestation"></a><span data-ttu-id="01503-113">Manifestation</span><span class="sxs-lookup"><span data-stu-id="01503-113">Manifestation</span></span>

<span data-ttu-id="01503-114">Les pilotes en mode noyau ne sont pas exécutés s’ils ne sont pas correctement signés par une autorité de certification approuvée.</span><span class="sxs-lookup"><span data-stu-id="01503-114">Kernel-mode drivers will not run if they are not properly signed by a trusted certification authority (CA).</span></span> <span data-ttu-id="01503-115">Le système d’exploitation n’autorise pas l’exécution des pilotes non autorisés et les mécanismes standard tels que le débogage du noyau et testsigning ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="01503-115">The operating system will not allow untrusted drivers to run and standard mechanisms like kernel debugging and testsigning will not be permitted.</span></span>

## <a name="mitigation"></a><span data-ttu-id="01503-116">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="01503-116">Mitigation</span></span>

<span data-ttu-id="01503-117">Pour tester des pilotes, vous devez désactiver le démarrage sécurisé dans le BIOS et répondre aux autres exigences de signature de test (voir ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="01503-117">To test drivers, you must disable Secure Boot in BIOS as well as meet the other test-signing requirements (see below).</span></span>

<span data-ttu-id="01503-118">Lorsque vous distribuez plus largement des pilotes, ceux-ci doivent être correctement signés par une autorité de certification approuvée.</span><span class="sxs-lookup"><span data-stu-id="01503-118">When distributing drivers more widely they must be properly signed by a trusted CA.</span></span>

## <a name="resources"></a><span data-ttu-id="01503-119">Ressources</span><span class="sxs-lookup"><span data-stu-id="01503-119">Resources</span></span>

-   <span data-ttu-id="01503-120">[Signature des pilotes](/previous-versions/windows/hardware/design/dn653563(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="01503-120">[Signing Drivers](/previous-versions/windows/hardware/design/dn653563(v=vs.85))</span></span>

 

 