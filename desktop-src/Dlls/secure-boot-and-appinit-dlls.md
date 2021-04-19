---
description: À compter de Windows 8, l' \_ infrastructure des DLL AppInit est désactivée lorsque le démarrage sécurisé est activé.
ms.assetid: 3ADE71C7-7113-4D26-8D6D-5609CAF13397
title: DLL AppInit et démarrage sécurisé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2915dda53959f2a403a62112385fe80e735cbfd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528330"
---
# <a name="appinit-dlls-and-secure-boot"></a><span data-ttu-id="2f658-103">DLL AppInit et démarrage sécurisé</span><span class="sxs-lookup"><span data-stu-id="2f658-103">AppInit DLLs and Secure Boot</span></span>

<span data-ttu-id="2f658-104">À compter de Windows 8, l' \_ infrastructure des DLL AppInit est désactivée lorsque le démarrage sécurisé est activé.</span><span class="sxs-lookup"><span data-stu-id="2f658-104">Starting in Windows 8, the AppInit\_DLLs infrastructure is disabled when secure boot is enabled.</span></span>

## <a name="about-appinit_dlls"></a><span data-ttu-id="2f658-105">À propos des \_ DLL AppInit</span><span class="sxs-lookup"><span data-stu-id="2f658-105">About AppInit\_DLLs</span></span>

<span data-ttu-id="2f658-106">L' \_ infrastructure des DLL AppInit offre un moyen simple de raccorder les API système en autorisant le chargement des dll personnalisées dans l’espace d’adressage de chaque application interactive.</span><span class="sxs-lookup"><span data-stu-id="2f658-106">The AppInit\_DLLs infrastructure provides an easy way to hook system APIs by allowing custom DLLs to be loaded into the address space of every interactive application.</span></span> <span data-ttu-id="2f658-107">Les applications et les programmes malveillants utilisent tous deux des DLL AppInit pour la même raison de base, qui consiste à raccorder des API. une fois la DLL personnalisée chargée, elle peut raccorder une API système connue et implémenter d’autres fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="2f658-107">Applications and malicious software both use AppInit DLLs for the same basic reason, which is to hook APIs; after the custom DLL is loaded, it can hook a well-known system API and implement alternate functionality.</span></span> <span data-ttu-id="2f658-108">Seul un petit ensemble d’applications légitimes modernes utilise ce mécanisme pour charger les dll, tandis qu’un grand ensemble de programmes malveillants utilisent ce mécanisme pour compromettre les systèmes.</span><span class="sxs-lookup"><span data-stu-id="2f658-108">Only a small set of modern legitimate applications use this mechanism to load DLLs, while a large set of malware use this mechanism to compromise systems.</span></span> <span data-ttu-id="2f658-109">Même les DLL AppInit légitimes \_ peuvent provoquer des blocages système et des problèmes de performances, par conséquent, l’utilisation de \_ DLL AppInit n’est pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="2f658-109">Even legitimate AppInit\_DLLs can unintentionally cause system deadlocks and performance problems, therefore usage of AppInit\_DLLs is not recommended.</span></span>

## <a name="appinit_dlls-and-secure-boot"></a><span data-ttu-id="2f658-110">\_DLL appInit et démarrage sécurisé</span><span class="sxs-lookup"><span data-stu-id="2f658-110">AppInit\_DLLs and secure boot</span></span>

<span data-ttu-id="2f658-111">Windows 8 a adopté UEFI et le démarrage sécurisé pour améliorer l’intégrité globale du système et offrir une protection renforcée contre les menaces sophistiquées.</span><span class="sxs-lookup"><span data-stu-id="2f658-111">Windows 8 adopted UEFI and secure boot to improve the overall system integrity and to provide strong protection against sophisticated threats.</span></span> <span data-ttu-id="2f658-112">Lorsque le démarrage sécurisé est activé, le \_ mécanisme des DLL AppInit est désactivé dans le cadre d’une approche sans compromis pour protéger les clients contre les logiciels malveillants et les menaces.</span><span class="sxs-lookup"><span data-stu-id="2f658-112">When secure boot is enabled, the AppInit\_DLLs mechanism is disabled as part of a no-compromise approach to protect customers against malware and threats.</span></span>

<span data-ttu-id="2f658-113">Notez que le démarrage sécurisé est un protocole UEFI et non une fonctionnalité de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2f658-113">Please note that secure boot is a UEFI protocol and not a Windows 8 feature.</span></span> <span data-ttu-id="2f658-114">Pour plus d’informations sur UEFI et sur la spécification du protocole de démarrage sécurisé, consultez [https://www.uefi.org](https://www.uefi.org/) .</span><span class="sxs-lookup"><span data-stu-id="2f658-114">More info on UEFI and the secure boot protocol specification can be found at [https://www.uefi.org](https://www.uefi.org/).</span></span>

## <a name="appinit_dlls-certification-requirement-for-windows-8-desktop-apps"></a><span data-ttu-id="2f658-115">\_Conditions de certification des DLL AppInit pour les applications de bureau Windows 8</span><span class="sxs-lookup"><span data-stu-id="2f658-115">AppInit\_DLLs certification requirement for Windows 8 desktop apps</span></span>

<span data-ttu-id="2f658-116">L’une des conditions de certification pour les applications de bureau Windows 8 est que l’application ne doit pas charger de dll arbitraires pour intercepter les appels d’API Win32 à l’aide du \_ mécanisme de DLL AppInit.</span><span class="sxs-lookup"><span data-stu-id="2f658-116">One of the certification requirements for Windows 8 desktop apps is that the app must not load arbitrary DLLs to intercept Win32 API calls using the AppInit\_DLLs mechanism.</span></span> <span data-ttu-id="2f658-117">Pour plus d’informations sur les conditions requises en matière de certification, reportez-vous à la section 1,1 des [conditions de certification pour les applications de bureau Windows 8](../win_cert/certification-requirements-for-windows-desktop-apps.md).</span><span class="sxs-lookup"><span data-stu-id="2f658-117">For more detailed information about the certification requirements, refer to section 1.1 of [Certification requirements for Windows 8 desktop apps](../win_cert/certification-requirements-for-windows-desktop-apps.md).</span></span>

## <a name="summary"></a><span data-ttu-id="2f658-118">Résumé</span><span class="sxs-lookup"><span data-stu-id="2f658-118">Summary</span></span>

-   <span data-ttu-id="2f658-119">Le \_ mécanisme des DLL AppInit n’est pas une approche recommandée pour les applications légitimes, car cela peut entraîner des blocages système et des problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="2f658-119">The AppInit\_DLLs mechanism is not a recommended approach for legitimate applications because it can lead to system deadlocks and performance problems.</span></span>
-   <span data-ttu-id="2f658-120">Le \_ mécanisme des DLL AppInit est désactivé par défaut lorsque le démarrage sécurisé est activé.</span><span class="sxs-lookup"><span data-stu-id="2f658-120">The AppInit\_DLLs mechanism is disabled by default when secure boot is enabled.</span></span>
-   <span data-ttu-id="2f658-121">L’utilisation \_ de DLL AppInit dans une application de bureau Windows 8 est un échec de certification des applications de bureau Windows.</span><span class="sxs-lookup"><span data-stu-id="2f658-121">Using AppInit\_DLLs in a Windows 8 desktop app is a Windows desktop app certification failure.</span></span>

<span data-ttu-id="2f658-122">Consultez le livre blanc suivant pour plus d’informations sur les \_ DLL AppInit sur Windows 7 et Windows server 2008 R2 : [DLL AppInit dans Windows 7 et windows Server 2008 R2](/previous-versions/windows/hardware/download/dn550976(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2f658-122">See the following whitepaper for info about AppInit\_DLLs on Windows 7 and Windows Server 2008 R2: [AppInit DLLs in Windows 7 and Windows Server 2008 R2](/previous-versions/windows/hardware/download/dn550976(v=vs.85)).</span></span>

 

 
