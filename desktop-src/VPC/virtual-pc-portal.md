---
title: Windows Virtual PC
description: Utiliser les interfaces COM de Windows Virtual PC pour créer un ordinateur virtuel et installer un ordinateur virtuel ; Windows Virtual PC est la toute dernière technologie de virtualisation Microsoft.
ms.assetid: d47eee76-059b-43dc-a51f-7c08d932a1c7
keywords:
- PC virtuels Windows Virtual PC
- PC virtuel Windows Virtual PC, page d’hébergement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf9dbe0d05100876ae54d327d1fe7ac8cb53d40c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509034"
---
# <a name="windows-virtual-pc"></a><span data-ttu-id="5f044-105">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5f044-105">Windows Virtual PC</span></span>

<span data-ttu-id="5f044-106">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5f044-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5f044-107">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](../hyperv_v2/windows-virtualization-portal.md).\]</span><span class="sxs-lookup"><span data-stu-id="5f044-107">Instead, use the [Hyper-V WMI provider (V2)](../hyperv_v2/windows-virtualization-portal.md).\]</span></span>

## <a name="purpose"></a><span data-ttu-id="5f044-108">Objectif</span><span class="sxs-lookup"><span data-stu-id="5f044-108">Purpose</span></span>

<span data-ttu-id="5f044-109">Cette documentation fournit des informations sur l’interface COM de Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="5f044-109">This documentation provides information about the Windows Virtual PC COM interface.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="5f044-110">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="5f044-110">Where applicable</span></span>

<span data-ttu-id="5f044-111">Windows Virtual PC est la dernière technologie de virtualisation de Microsoft. elle vous permet d’exécuter de nombreuses applications de productivité sur un environnement Windows virtuel, en un seul clic, directement à partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5f044-111">Windows Virtual PC is the latest Microsoft virtualization technology; it enables you to run many productivity applications on a virtual Windows environment, with a single click, directly from Windows 7.</span></span> <span data-ttu-id="5f044-112">Vous pouvez créer des machines virtuelles distinctes en plus de votre bureau Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5f044-112">You can create separate virtual machines on top of your Windows 7 desktop.</span></span> <span data-ttu-id="5f044-113">Chaque ordinateur virtuel émule un système matériel complet, du processeur à la carte réseau, dans un environnement de logiciel autonome et isolé, ce qui permet le fonctionnement simultané de systèmes incompatibles autrement.</span><span class="sxs-lookup"><span data-stu-id="5f044-113">Each virtual machine emulates a complete hardware system—from processor to network card—in a self-contained, isolated software environment, enabling the simultaneous operation of otherwise incompatible systems.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="5f044-114">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="5f044-114">Developer audience</span></span>

<span data-ttu-id="5f044-115">Les interfaces COM de Windows Virtual PC sont destinées aux développeurs qui créent des applications clientes qui automatisent le déploiement et le fonctionnement des ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="5f044-115">The Windows Virtual PC COM interfaces are for developers who are creating client applications that automate the deployment and operation of virtual machines.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="5f044-116">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="5f044-116">Run-time requirements</span></span>

<span data-ttu-id="5f044-117">Windows Virtual PC requiert l’une des éditions suivantes de Windows 7 : édition familiale basique, édition familiale Premium, professionnel, édition intégrale ou entreprise.</span><span class="sxs-lookup"><span data-stu-id="5f044-117">Windows Virtual PC requires one of the following Windows 7 editions - Home Basic, Home Premium, Professional, Ultimate, or Enterprise edition.</span></span>

<span data-ttu-id="5f044-118">Pour obtenir les fichiers d’en-tête et de bibliothèque associés, installez le SDK Windows pour Windows 7 à partir du [Centre de téléchargement Microsoft](https://www.microsoft.com/download/details.aspx?id=8279).</span><span class="sxs-lookup"><span data-stu-id="5f044-118">To obtain the related header and library files, install the Windows SDK for Windows 7 from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=8279).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5f044-119">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="5f044-119">In this section</span></span>

-   [<span data-ttu-id="5f044-120">Informations de référence sur les PC virtuels Windows</span><span class="sxs-lookup"><span data-stu-id="5f044-120">Windows Virtual PC Reference</span></span>](virtual-pc-reference.md)

## <a name="related-topics"></a><span data-ttu-id="5f044-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5f044-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f044-122">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5f044-122">Windows Virtual PC</span></span>](https://www.microsoft.com/windows/virtual-pc/)
</dt> </dl>

 

 