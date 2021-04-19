---
description: Mergemod.dll fournit un objet COM qui implémente les opérations de fusion et la génération d’image source pour les modules de fusion. L’objet principal implémente des interfaces pour les programmes C/C++ et les clients Automation, y compris Visual Basic et VBScript.
ms.assetid: 877d3691-948f-4aea-89d8-0ff008126ccc
title: Automatisation des modules de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ae27370b2ad898cf9413567285afc41d117815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524709"
---
# <a name="merge-module-automation"></a><span data-ttu-id="afefa-104">Automatisation des modules de fusion</span><span class="sxs-lookup"><span data-stu-id="afefa-104">Merge Module Automation</span></span>

<span data-ttu-id="afefa-105">Mergemod.dll fournit un objet COM qui implémente les opérations de fusion et la génération d’image source pour les modules de fusion.</span><span class="sxs-lookup"><span data-stu-id="afefa-105">Mergemod.dll provides a COM object that implements merge operations and source image generation for merge modules.</span></span> <span data-ttu-id="afefa-106">L’objet principal implémente des interfaces pour les programmes C/C++ et les clients Automation, y compris Visual Basic et VBScript.</span><span class="sxs-lookup"><span data-stu-id="afefa-106">The main object implements interfaces for C/C++ programs and automation clients, including Visual Basic and VBScript.</span></span>

<span data-ttu-id="afefa-107">La méthode recommandée pour installer Mergemod.dll consiste à utiliser l’Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="afefa-107">The preferred method for installing Mergemod.dll is by using the Windows Installer.</span></span> <span data-ttu-id="afefa-108">L’ID du composant contenant l’interface COM Mergemod.dll est {FD153241-37EC-11D2-8892-00A0C981B015}.</span><span class="sxs-lookup"><span data-stu-id="afefa-108">The Component ID for the component containing the Mergemod.dll COM interface is {FD153241-37EC-11D2-8892-00A0C981B015}.</span></span> <span data-ttu-id="afefa-109">Le même binaire peut être utilisé sur tous les systèmes Windows et la dll s’inscrit automatiquement par le biais de regsvr32 sur les systèmes antérieurs.</span><span class="sxs-lookup"><span data-stu-id="afefa-109">The same binary can be used on all Windows systems and the dll will self-register through regsvr32 on older systems.</span></span>

<span data-ttu-id="afefa-110">Notez que Mergemod.dll exige que le Msvcrt.dll soit installé sur le système.</span><span class="sxs-lookup"><span data-stu-id="afefa-110">Note that Mergemod.dll requires that the Msvcrt.dll be installed on the system.</span></span>

<span data-ttu-id="afefa-111">Notez que Mergemod.dll 2,0 est requis pour créer des [modules de fusion configurables](configurable-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="afefa-111">Note that Mergemod.dll 2.0 is required to create [Configurable Merge Modules](configurable-merge-modules.md).</span></span> <span data-ttu-id="afefa-112">Mergemod.dll version 2,0 fournit des fonctionnalités étendues au moment de la génération par le biais de l’interface [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) .</span><span class="sxs-lookup"><span data-stu-id="afefa-112">Mergemod.dll version 2.0 provides extended functionality at build time through the [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) Interface.</span></span> <span data-ttu-id="afefa-113">Ce CLSID prend en charge toutes les fonctionnalités existantes de l’interface [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) fournie par Mergemod.dll version 1,0.</span><span class="sxs-lookup"><span data-stu-id="afefa-113">This CLSID supports all the existing functionality of the [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) Interface provided by Mergemod.dll version 1.0.</span></span> <span data-ttu-id="afefa-114">L’interface par défaut sur l’objet [**Merge**](merge-object.md) de Mergemod.dll 2,0 est l’interface **IMsmMerge2** au lieu de l’interface **IMsmMerge** .</span><span class="sxs-lookup"><span data-stu-id="afefa-114">The default interface on the [**Merge**](merge-object.md) object of Mergemod.dll 2.0 is the **IMsmMerge2** interface instead of the **IMsmMerge** interface.</span></span>

[<span data-ttu-id="afefa-115">Modèle objet pour Mergemod.dll version 1,0</span><span class="sxs-lookup"><span data-stu-id="afefa-115">Object Model for Mergemod.dll Version 1.0</span></span>](object-model-for-mergemod-dll-version-1-0.md)

[<span data-ttu-id="afefa-116">Modèle objet pour Mergemod.dll version 2,0</span><span class="sxs-lookup"><span data-stu-id="afefa-116">Object Model for Mergemod.dll Version 2.0</span></span>](object-model-for-mergemod-dll-version-2-0.md)

 

 
