---
description: Vous n’avez pas besoin d’un Tablet PC pour développer des applications Tablet PC, mais vous avez besoin d’un ordinateur personnel qui peut exécuter les logiciels listés plus loin dans cette rubrique.
ms.assetid: 82034950-78a7-4bab-b449-1b8ea7d90676
title: L’environnement de développement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fefa29a518beaf21aa8b2457abf17d9581075f73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953101"
---
# <a name="the-development-environment"></a><span data-ttu-id="66526-103">L’environnement de développement</span><span class="sxs-lookup"><span data-stu-id="66526-103">The Development Environment</span></span>

<span data-ttu-id="66526-104">Vous n’avez pas besoin d’un Tablet PC pour développer des applications Tablet PC, mais vous avez besoin d’un ordinateur personnel qui peut exécuter les logiciels listés plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="66526-104">You do not need a Tablet PC to develop Tablet PC applications, but you do need a personal computer capable of running the software listed later in this topic.</span></span>

<span data-ttu-id="66526-105">Nous vous recommandons vivement de tester votre application sur un Tablet PC réel pour vous assurer que toutes les différences de matériel, telles que le digitaliseur de résolution supérieur, sont comptabilisées.</span><span class="sxs-lookup"><span data-stu-id="66526-105">We strongly recommend that you test your application on an actual Tablet PC to ensure that all differences in hardware, such as the higher resolution digitizer, are accounted for.</span></span>

<span data-ttu-id="66526-106">Un système de développement minimal standard est constitué du matériel et des logiciels suivants.</span><span class="sxs-lookup"><span data-stu-id="66526-106">A typical, minimal development system consists of the following hardware and software.</span></span>

## <a name="hardware"></a><span data-ttu-id="66526-107">Matériel</span><span class="sxs-lookup"><span data-stu-id="66526-107">Hardware</span></span>

-   <span data-ttu-id="66526-108">8 Mo d’espace disque dur pour une installation complète.</span><span class="sxs-lookup"><span data-stu-id="66526-108">8 MB of hard disk space for a complete installation.</span></span>
-   <span data-ttu-id="66526-109">Un dispositif de pointage pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="66526-109">A pointing device for input.</span></span> <span data-ttu-id="66526-110">Cela comprend les appareils tels qu’une souris, une tablette externe ou un Tablet PC avec un digitaliseur HID.</span><span class="sxs-lookup"><span data-stu-id="66526-110">This includes devices such as a mouse, an external tablet, or a Tablet PC with an HID digitizer.</span></span>

<span data-ttu-id="66526-111">HID est l’acronyme de Human Interface Device, une norme pour les périphériques d’entrée.</span><span class="sxs-lookup"><span data-stu-id="66526-111">HID stands for Human Interface Device, a standard for input devices.</span></span> <span data-ttu-id="66526-112">Les numériseurs non conformes à HID sont traités comme une souris normale, tandis que les numériseurs conformes aux HID ont une résolution plus élevée et davantage de métadonnées sur les traits, tels que la pression, similaires à ceux installés sur le matériel Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="66526-112">Non-HID compliant digitizers are treated like a regular mouse, while HID compliant digitizers have higher resolution and more metadata on strokes, such as pressure, similar to those that are installed on Tablet PC hardware.</span></span>

## <a name="software"></a><span data-ttu-id="66526-113">Logiciel</span><span class="sxs-lookup"><span data-stu-id="66526-113">Software</span></span>

<span data-ttu-id="66526-114">Les systèmes d’exploitation suivants peuvent être utilisés pour développer des applications Tablet PC :</span><span class="sxs-lookup"><span data-stu-id="66526-114">The following operating systems can be used to develop Tablet PC applications:</span></span>

-   <span data-ttu-id="66526-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="66526-115">Windows 7</span></span>
-   <span data-ttu-id="66526-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66526-116">Windows Vista</span></span>
-   <span data-ttu-id="66526-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66526-117">Windows Server 2008</span></span>
-   <span data-ttu-id="66526-118">Windows XP Édition Tablet PC 2005</span><span class="sxs-lookup"><span data-stu-id="66526-118">Windows XP Tablet PC Edition 2005</span></span>
-   <span data-ttu-id="66526-119">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="66526-119">Windows Server 2003</span></span>
-   <span data-ttu-id="66526-120">Windows XP Professionnel</span><span class="sxs-lookup"><span data-stu-id="66526-120">Windows XP Professional</span></span>

<span data-ttu-id="66526-121">Vous aurez également besoin des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="66526-121">You also need:</span></span>

-   <span data-ttu-id="66526-122">Visual Studio version 6 avec Service Pack 5, ou Visual Studio .NET, ou Visual Studio .NET 2005</span><span class="sxs-lookup"><span data-stu-id="66526-122">Visual Studio version 6 with Service Pack 5, or Visual Studio .NET, or Visual Studio .NET 2005</span></span>
-   <span data-ttu-id="66526-123">Microsoft Internet Explorer 6 ou version ultérieure (recommandé)</span><span class="sxs-lookup"><span data-stu-id="66526-123">Microsoft Internet Explorer 6, or higher (recommended)</span></span>

### <a name="details-on-developing-on-non-tablet-pc-skus-of-windows"></a><span data-ttu-id="66526-124">Détails sur le développement sur des références SKU non-Tablet PC de Windows</span><span class="sxs-lookup"><span data-stu-id="66526-124">Details on Developing on Non-Tablet PC SKUs of Windows</span></span>

<span data-ttu-id="66526-125">Les composants de la plateforme Tablet PC peuvent être installés sur Windows XP Professionnel avec Service Pack 2 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="66526-125">The Tablet PC platform components can be installed on Windows XP Professional with Service Pack 2 or Windows Server 2003.</span></span> <span data-ttu-id="66526-126">Sur ces systèmes d’exploitation, votre application peut collecter de l’encre avec la classe [**InkCollector**](inkcollector-class.md) et peut être testée et déboguée.</span><span class="sxs-lookup"><span data-stu-id="66526-126">On these operating systems, your application can collect ink with the [**InkCollector**](inkcollector-class.md) class and can be tested and debugged.</span></span> <span data-ttu-id="66526-127">Toutefois, aucune reconnaissance n’est disponible, sauf si vous installez également le Pack de reconnaissance 2005 de Microsoft Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="66526-127">However, no recognition is available unless you also install the Microsoft Windows XP Tablet PC Edition 2005 Recognizer Pack.</span></span> <span data-ttu-id="66526-128">Vous pouvez télécharger ce pack à partir du centre de téléchargement sur MSDN.</span><span class="sxs-lookup"><span data-stu-id="66526-128">You can download that pack from the Download Center on MSDN.</span></span>

<span data-ttu-id="66526-129">Après l’installation de l’SDK Windows sur un système Windows XP professionnel ou Windows Server 2003, vous disposerez de tous les fichiers de développement nécessaires pour générer des applications manuscrites (telles que msinkaut. h pour un développeur COM).</span><span class="sxs-lookup"><span data-stu-id="66526-129">After installing the Windows SDK on to a Windows XP Professional or Windows Server 2003 system, you will have all the development files necessary to build ink applications (such as msinkaut.h for a COM developer).</span></span> <span data-ttu-id="66526-130">Toutefois, vous ne pourrez pas exécuter ou déboguer votre application sur ce système tant que vous n’aurez pas installé les fichiers du Runtime.</span><span class="sxs-lookup"><span data-stu-id="66526-130">However, you will be unable to run or debug your application on that system until you install the runtime files.</span></span> <span data-ttu-id="66526-131">Par exemple, dans le cas d’un développeur COM, inkobj.dll doit être installé et inscrit.</span><span class="sxs-lookup"><span data-stu-id="66526-131">For instance, in the case of a COM developer, inkobj.dll must be installed and registered.</span></span> <span data-ttu-id="66526-132">Étant donné que vous n’êtes pas sur un système où ces fichiers de plateforme existent, vous devez installer les composants de plateforme Tablet PC à partir du module de fusion redistribuable, mstpcrt. msm, pour obtenir les fichiers du Runtime sur votre système.</span><span class="sxs-lookup"><span data-stu-id="66526-132">Because you are not on a system where these platform files exist, you must install the Tablet PC platform components from the redistributable merge module, mstpcrt.msm, to get the runtime files on your system.</span></span>

<span data-ttu-id="66526-133">La façon la plus simple d’obtenir les runtimes de plateforme installés sur un système Windows XP professionnel ou Windows 2000 à des fins de développement est de compiler l’exemple de projet d’installation fourni avec les exemples d’ordinateurs portables et Tablet PC et de les déployer sur l’ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="66526-133">The simplest way to get the platform runtimes installed on a Windows XP Professional or Windows 2000 system for development purposes is to compile the sample setup project provided with the Mobile PC and Tablet PC Samples and deploy it to the development machine.</span></span>

> [!Note]  
> <span data-ttu-id="66526-134">Windows Vista et Windows XP Édition Tablet PC 2005 disposent déjà des composants de plateforme installés. ils ne nécessitent donc pas d’étapes supplémentaires pour exécuter et déboguer des applications Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="66526-134">Windows Vista and Windows XP Tablet PC Edition 2005 already have the platform components installed, so they do not require additional steps to run and debug Tablet PC applications.</span></span>

 

<span data-ttu-id="66526-135">Les contrôles [InkEdit](inkedit-control-reference.md) et [InkPicture](inkpicture-control-reference.md) peuvent être utilisés pour collecter l’encre sur Windows 2000 avec Service Pack 4 ou Windows XP Professionnel avec Service Pack 2 lorsque les composants de plateforme Tablet PC sont présents en installant le kit de développement logiciel (SDK) Tablet PC version 1,7, mais ne peuvent pas collecter l’encre sur les systèmes non-Tablet PC sur lesquels les composants de plateforme Tablet PC ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="66526-135">The [InkEdit](inkedit-control-reference.md) and [InkPicture](inkpicture-control-reference.md) controls can be used to collect ink on Windows 2000 with Service Pack 4 or Windows XP Professional with Service Pack 2 when the Tablet PC platform components are present by installing the Tablet PC SDK version 1.7, but are not able to collect ink on non-Tablet PC systems that do not have the Tablet PC platform components installed.</span></span>

<span data-ttu-id="66526-136">Le SDK Windows fournit tous les composants nécessaires pour développer des applications Tablet PC sur des références SKU non-Tablet de Windows.</span><span class="sxs-lookup"><span data-stu-id="66526-136">The Windows SDK provides all the necessary components to develop Tablet PC applications on non-Tablet SKUs of Windows.</span></span> <span data-ttu-id="66526-137">Affectez la valeur 1 à la clé de Registre **DWORD** suivante afin de collecter l’encre sur les références SKU non-tablette de Windows :</span><span class="sxs-lookup"><span data-stu-id="66526-137">Set the following **DWORD** registry key to 1 in order to collect ink on non-Tablet SKUs of Windows:</span></span>

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\TabletPC\Controls\EnableInkCollectionOnNonTablets`

<span data-ttu-id="66526-138">Cette clé est conçue uniquement à des fins de développement.</span><span class="sxs-lookup"><span data-stu-id="66526-138">This key is intended for development purposes only.</span></span>

 

 



