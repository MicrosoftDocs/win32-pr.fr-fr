---
title: Démarrage mesuré
description: Démarrage mesuré
ms.assetid: D7ED02FA-6D0F-4753-AC07-BD7DCE55B3FD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccbba6e5f96fd91c00c295c4b15cab8849f11dc
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730740"
---
# <a name="measured-boot"></a><span data-ttu-id="c609b-103">Démarrage mesuré</span><span class="sxs-lookup"><span data-stu-id="c609b-103">Measured Boot</span></span>

## <a name="platforms"></a><span data-ttu-id="c609b-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="c609b-104">Platforms</span></span>

 <span data-ttu-id="c609b-105">**Clients** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="c609b-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="c609b-106">**Serveurs** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c609b-106">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="c609b-107">Description</span><span class="sxs-lookup"><span data-stu-id="c609b-107">Description</span></span>

<span data-ttu-id="c609b-108">Comme le logiciel anti-programme malveillant est devenu mieux et mieux adapté à la détection des programmes malveillants du runtime, les attaquants deviennent également mieux adaptés à la création de rootkits qui peuvent masquer la détection.</span><span class="sxs-lookup"><span data-stu-id="c609b-108">As antimalware (AM) software has become better and better at detecting runtime malware, attackers are also becoming better at creating rootkits that can hide from detection.</span></span> <span data-ttu-id="c609b-109">La détection de programmes malveillants qui démarrent tôt au cours du cycle de démarrage est un défi que la plupart des fournisseurs sont tenus de faire face à la diligence.</span><span class="sxs-lookup"><span data-stu-id="c609b-109">Detecting malware that starts early in the boot cycle is a challenge that most AM vendors address diligently.</span></span> <span data-ttu-id="c609b-110">En règle générale, ils créent des piratages système qui ne sont pas pris en charge par le système d’exploitation hôte et qui peuvent entraîner le placement de l’ordinateur dans un état instable.</span><span class="sxs-lookup"><span data-stu-id="c609b-110">Typically, they create system hacks that are not supported by the host operating system and can actually result in placing the computer in an unstable state.</span></span> <span data-ttu-id="c609b-111">Jusqu’à présent, Windows n’a pas fourni un bon moyen de détecter et de résoudre ces menaces de démarrage anticipé.</span><span class="sxs-lookup"><span data-stu-id="c609b-111">Up to this point, Windows has not provided a good way for AM to detect and resolve these early boot threats.</span></span> <span data-ttu-id="c609b-112">Windows 8 introduit une nouvelle fonctionnalité appelée démarrage mesuré, qui mesure chaque composant, du microprogramme au-dessus des pilotes de démarrage de démarrage, stocke ces mesures dans le Module de plateforme sécurisée (TPM) (TPM) sur l’ordinateur, puis met à disposition un journal qui peut être testé à distance pour vérifier l’état de démarrage du client.</span><span class="sxs-lookup"><span data-stu-id="c609b-112">Windows 8 introduces a new feature called Measured Boot, which measures each component, from firmware up through the boot start drivers, stores those measurements in the Trusted Platform Module (TPM) on the machine, and then makes available a log that can be tested remotely to verify the boot state of the client.</span></span>

## <a name="manifestation"></a><span data-ttu-id="c609b-113">Manifestation</span><span class="sxs-lookup"><span data-stu-id="c609b-113">Manifestation</span></span>

<span data-ttu-id="c609b-114">La fonctionnalité de démarrage mesurée fournit aux logiciels un journal approuvé (résistant aux usurpations et falsifications) de tous les composants de démarrage qui ont démarré avant le logiciel.</span><span class="sxs-lookup"><span data-stu-id="c609b-114">The Measured Boot feature provides AM software with a trusted (resistant to spoofing and tampering) log of all boot components that started before AM software.</span></span> <span data-ttu-id="c609b-115">AM Software peut utiliser le journal pour déterminer si les composants qui ont été exécutés avant d’être dignes de confiance ou s’ils sont infectés par des logiciels malveillants.</span><span class="sxs-lookup"><span data-stu-id="c609b-115">AM software can use the log to determine whether components that ran before it are trustworthy or if they are infected with malware.</span></span> <span data-ttu-id="c609b-116">Le logiciel AM sur l’ordinateur local peut envoyer le journal à un serveur distant à des fins d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="c609b-116">The AM software on the local machine can send the log to a remote sever for evaluation.</span></span> <span data-ttu-id="c609b-117">Le serveur distant peut initier des actions de correction en interagissant avec le logiciel sur le client ou par le biais de mécanismes hors bande, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="c609b-117">The remote server may initiate remediation actions either by interacting with software on the client or through out-of-band mechanisms, as appropriate.</span></span>

## <a name="mitigation"></a><span data-ttu-id="c609b-118">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="c609b-118">Mitigation</span></span>

<span data-ttu-id="c609b-119">Dans les scénarios d’entreprise, l’administrateur système contrôle le mode d’utilisation des informations de démarrage mesurées.</span><span class="sxs-lookup"><span data-stu-id="c609b-119">In enterprise scenarios, the system administrator has control of how Measured Boot info is used.</span></span> <span data-ttu-id="c609b-120">Dans les scénarios d’utilisateur final (par exemple, les banques en ligne), le consommateur doit s’inscrire pour utiliser le démarrage mesuré pour le service spécifique.</span><span class="sxs-lookup"><span data-stu-id="c609b-120">In end-user scenarios for example, online banking), the consumer must opt in to use Measured Boot for the specific service.</span></span>

## <a name="solution"></a><span data-ttu-id="c609b-121">Solution</span><span class="sxs-lookup"><span data-stu-id="c609b-121">Solution</span></span>

<span data-ttu-id="c609b-122">Un livre blanc est préparé pour détailler les API et les appels de fonction qui doivent être faits pour différents scénarios de démarrage mesurés.</span><span class="sxs-lookup"><span data-stu-id="c609b-122">A white paper is being prepared that details the APIs and function calls that must be made for various Measured Boot scenarios.</span></span>

 

 




