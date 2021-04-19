---
description: MFTrace est un outil permettant de générer des journaux de suivi pour les applications Media Foundation.
ms.assetid: 55b421c8-e87c-4dd2-8649-93832c93f999
title: MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4a216f225141ceccf3f1357025dd069afa494d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540945"
---
# <a name="mftrace"></a><span data-ttu-id="e9aec-103">MFTrace</span><span class="sxs-lookup"><span data-stu-id="e9aec-103">MFTrace</span></span>

<span data-ttu-id="e9aec-104">MFTrace est un outil permettant de générer des journaux de suivi pour les applications Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e9aec-104">MFTrace is a tool for generating trace logs for Media Foundation applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e9aec-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="e9aec-105">In this section</span></span>

-   [<span data-ttu-id="e9aec-106">Utilisation de MFTrace</span><span class="sxs-lookup"><span data-stu-id="e9aec-106">Using MFTrace</span></span>](using-mftrace.md)
-   [<span data-ttu-id="e9aec-107">Mots clés MFTrace</span><span class="sxs-lookup"><span data-stu-id="e9aec-107">MFTrace Keywords</span></span>](mftrace-keywords.md)
-   [<span data-ttu-id="e9aec-108">Fichier de configuration MFTrace</span><span class="sxs-lookup"><span data-stu-id="e9aec-108">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)

## <a name="requirements"></a><span data-ttu-id="e9aec-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9aec-109">Requirements</span></span>



| <span data-ttu-id="e9aec-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9aec-110">Requirement</span></span> | <span data-ttu-id="e9aec-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9aec-111">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9aec-112">Version minimale du kit de développement logiciel</span><span class="sxs-lookup"><span data-stu-id="e9aec-112">Minimum SDK version</span></span>      | <span data-ttu-id="e9aec-113">Kit de développement logiciel (SDK) Microsoft Windows pour Windows 7 et .NET Framework 4,0</span><span class="sxs-lookup"><span data-stu-id="e9aec-113">Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0</span></span> |
| <span data-ttu-id="e9aec-114">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="e9aec-114">Minimum operating system</span></span> | <span data-ttu-id="e9aec-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9aec-115">Windows Vista</span></span>                                                                         |



 

<span data-ttu-id="e9aec-116">MFTrace requiert les dll suivantes, qui sont également fournies dans le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="e9aec-116">MFTrace requires the following DLLs, which are also provided in the SDK.</span></span>

-   <span data-ttu-id="e9aec-117">detoured.dll</span><span class="sxs-lookup"><span data-stu-id="e9aec-117">detoured.dll</span></span>
-   <span data-ttu-id="e9aec-118">mfdetours.dll</span><span class="sxs-lookup"><span data-stu-id="e9aec-118">mfdetours.dll</span></span>

<span data-ttu-id="e9aec-119">Le kit de développement logiciel (SDK) fournit des versions 32 bits et 64 bits de MFTrace.</span><span class="sxs-lookup"><span data-stu-id="e9aec-119">The SDK provides both 32-bit and 64-bit versions of MFTrace.</span></span> <span data-ttu-id="e9aec-120">MFTrace ne prend pas en charge WOW64 ; pour suivre un processus 32 bits s’exécutant sur Windows 64 bits, utilisez la version 32 bits de MFTrace.</span><span class="sxs-lookup"><span data-stu-id="e9aec-120">MFTrace does not support WOW64; to trace a 32-bit process running on 64-bit Windows, use the 32-bit version of MFTrace.</span></span>

<span data-ttu-id="e9aec-121">SDK-root sur les systèmes 32 bits : \Program Files\Windows Kits\10 SDK-root on 64 bit System : \Program Files (x86) \Windows Kits\10 vous trouverez mftrace <à la racine> \bin du kit de développement logiciel (SDK) \<sdk-version> \<architecture>\mftrace.exe</span><span class="sxs-lookup"><span data-stu-id="e9aec-121">sdk-root on 32 bit systems: \Program Files\Windows Kits\10 sdk-root on 64 bit system: \Program Files (x86)\Windows Kits\10 You will find mftrace at <sdk-root>\bin\<sdk-version>\<architecture>\mftrace.exe</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9aec-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e9aec-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9aec-123">Outils de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e9aec-123">Media Foundation Tools</span></span>](media-foundation-tools.md)
</dt> </dl>

 

 



