---
title: Préparer votre environnement de développement
description: Préparer votre environnement de développement
ms.assetid: 5a3fd27e-ec8f-41eb-9d31-86d6d9f70862
ms.topic: article
ms.date: 10/03/2019
ms.openlocfilehash: ec42509ea81efce4bb17365d3bf08d36c2a4f415
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314933"
---
# <a name="prepare-your-development-environment"></a><span data-ttu-id="66e13-103">Préparer votre environnement de développement</span><span class="sxs-lookup"><span data-stu-id="66e13-103">Prepare Your Development Environment</span></span>

<span data-ttu-id="66e13-104">Pour écrire un programme Windows en C ou C++, vous devez installer le kit de développement logiciel (SDK) Microsoft Windows ou Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="66e13-104">To write a Windows program in C or C++, you must install the Microsoft Windows Software Development Kit (SDK) or Microsoft Visual Studio.</span></span> <span data-ttu-id="66e13-105">Le SDK Windows contient les en-têtes et les bibliothèques nécessaires à la compilation et à la liaison de votre application.</span><span class="sxs-lookup"><span data-stu-id="66e13-105">The Windows SDK contains the headers and libraries necessary to compile and link your application.</span></span> <span data-ttu-id="66e13-106">Le SDK Windows contient également des outils en ligne de commande pour la génération d’applications Windows, notamment le compilateur Visual C++ et l’éditeur de liens.</span><span class="sxs-lookup"><span data-stu-id="66e13-106">The Windows SDK also contains command-line tools for building Windows applications, including the Visual C++ compiler and linker.</span></span> <span data-ttu-id="66e13-107">Bien que vous puissiez compiler et générer des programmes Windows avec les outils en ligne de commande, nous vous recommandons d’utiliser Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="66e13-107">Although you can compile and build Windows programs with the command-line tools, we recommend using Microsoft Visual Studio.</span></span> <span data-ttu-id="66e13-108">Vous pouvez télécharger un téléchargement gratuit de Visual Studio Community ou des versions d’évaluation gratuites d’autres versions de Visual Studio [ici](https://visualstudio.microsoft.com/downloads/).</span><span class="sxs-lookup"><span data-stu-id="66e13-108">You can download a free download of Visual Studio Community or free trials of other versions of Visual Studio [here](https://visualstudio.microsoft.com/downloads/).</span></span>

<span data-ttu-id="66e13-109">Chaque version de la SDK Windows cible la version la plus récente de Windows, ainsi que plusieurs versions précédentes.</span><span class="sxs-lookup"><span data-stu-id="66e13-109">Each release of the Windows SDK targets the latest version of Windows as well as several previous versions.</span></span> <span data-ttu-id="66e13-110">Les notes de publication répertorient les plateformes prises en charge, mais sauf si vous gérez une application pour une très ancienne version de Windows, vous devez installer la dernière version de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="66e13-110">The release notes list the specific platforms that are supported, but unless you are maintaining an application for a very old version of Windows, you should install the latest release of the Windows SDK.</span></span> <span data-ttu-id="66e13-111">Vous pouvez télécharger les SDK Windows les plus récentes [ici](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span><span class="sxs-lookup"><span data-stu-id="66e13-111">You can download the latest Windows SDK [here](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span>

<span data-ttu-id="66e13-112">Le SDK Windows prend en charge le développement d’applications 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="66e13-112">The Windows SDK supports development of both 32-bit and 64-bit applications.</span></span> <span data-ttu-id="66e13-113">Les API Windows sont conçues de façon à ce que le même code puisse être compilé pour 32 bits ou 64 bits sans modification.</span><span class="sxs-lookup"><span data-stu-id="66e13-113">The Windows APIs are designed so that the same code can compile for 32-bit or 64-bit without changes.</span></span>

> [!Note]  
> <span data-ttu-id="66e13-114">Le SDK Windows ne prend pas en charge le développement de pilotes matériels, et cette série ne traite pas du développement des pilotes.</span><span class="sxs-lookup"><span data-stu-id="66e13-114">The Windows SDK does not support hardware driver development, and this series will not discuss driver development.</span></span> <span data-ttu-id="66e13-115">Pour plus d’informations sur l’écriture d’un pilote matériel, consultez [prise en main avec les pilotes Windows](/windows-hardware/drivers/gettingstarted/).</span><span class="sxs-lookup"><span data-stu-id="66e13-115">For information about writing a hardware driver, see [Getting Started with Windows Drivers](/windows-hardware/drivers/gettingstarted/).</span></span>

## <a name="next"></a><span data-ttu-id="66e13-116">Suivant</span><span class="sxs-lookup"><span data-stu-id="66e13-116">Next</span></span>

[<span data-ttu-id="66e13-117">Conventions de codage Windows</span><span class="sxs-lookup"><span data-stu-id="66e13-117">Windows Coding Conventions</span></span>](windows-coding-conventions.md)

## <a name="related-topics"></a><span data-ttu-id="66e13-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="66e13-118">Related topics</span></span>

* [<span data-ttu-id="66e13-119">Télécharger Visual Studio</span><span class="sxs-lookup"><span data-stu-id="66e13-119">Download Visual Studio</span></span>](https://visualstudio.microsoft.com/downloads/)
* [<span data-ttu-id="66e13-120">Télécharger SDK Windows</span><span class="sxs-lookup"><span data-stu-id="66e13-120">Download Windows SDK</span></span>](https://developer.microsoft.com/windows/downloads/windows-10-sdk)