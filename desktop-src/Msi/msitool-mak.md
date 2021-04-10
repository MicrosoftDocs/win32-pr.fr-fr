---
description: Msitool. Mak est un Makefile que vous pouvez utiliser pour générer des outils et des actions personnalisées.
ms.assetid: c05da933-7e0e-4fbb-a936-517902a363c4
title: Msitool. Mak
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3dad9fd65aaa880e9fdb38369843907104dea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115191"
---
# <a name="msitoolmak"></a><span data-ttu-id="f6ef4-103">Msitool. Mak</span><span class="sxs-lookup"><span data-stu-id="f6ef4-103">Msitool.mak</span></span>

<span data-ttu-id="f6ef4-104">Msitool. Mak est un Makefile que vous pouvez utiliser pour générer des outils et des actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="f6ef4-104">Msitool.mak is a makefile that you can use to build tools and custom actions.</span></span> <span data-ttu-id="f6ef4-105">Il peut être utilisé avec Visual C++ version 4,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f6ef4-105">It may be used with Visual C++ version 4.0 or later.</span></span> <span data-ttu-id="f6ef4-106">Pour plus d’informations, consultez le fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="f6ef4-106">For more information, see the header file.</span></span> <span data-ttu-id="f6ef4-107">Un ensemble de valeurs doit être défini avant d’inclure ce fichier.</span><span class="sxs-lookup"><span data-stu-id="f6ef4-107">It requires a set of values to be defined before including this file.</span></span> <span data-ttu-id="f6ef4-108">En général, les développeurs placent ceux-ci au début du. cpp, ifdef devant être ignorés par le compilateur C.</span><span class="sxs-lookup"><span data-stu-id="f6ef4-108">Typically developers put those at the start of the .cpp, ifdef'd to be skipped by the C compiler.</span></span> <span data-ttu-id="f6ef4-109">De même, les ressources sont ajoutées à la fin du fichier. cpp.</span><span class="sxs-lookup"><span data-stu-id="f6ef4-109">Likewise resources are added to the end of the .cpp file.</span></span> <span data-ttu-id="f6ef4-110">Pour plus d’informations, consultez les exemples.</span><span class="sxs-lookup"><span data-stu-id="f6ef4-110">See samples for details.</span></span>

<span data-ttu-id="f6ef4-111">VCBIN peut être défini dans le répertoire où se trouvent les outils de Visual C++ ou le Makefile utilise MSVCDIR et MSDEVDIR.</span><span class="sxs-lookup"><span data-stu-id="f6ef4-111">VCBIN can be defined to the directory where the Visual C++ tools are found or the makefile uses MSVCDIR and MSDEVDIR.</span></span> <span data-ttu-id="f6ef4-112">Si ces derniers ne sont pas définis, ils ne spécifient pas d’emplacement, en supposant que les outils se trouvent sur le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="f6ef4-112">If those are not defined, it does not specify a location, assuming the tools to be on the PATH.</span></span> <span data-ttu-id="f6ef4-113">Un problème avec les variables d’environnement dans Visual C++ version 5,0 est que si les deux ne se trouvent pas sur votre chemin d’accès, l’éditeur de liens ne trouve pas Msdis100.dll.</span><span class="sxs-lookup"><span data-stu-id="f6ef4-113">An issue with the environment variables in Visual C++ version 5.0 is that if both are not on you path, the linker cannot find Msdis100.dll.</span></span> <span data-ttu-id="f6ef4-114">Si vous la copiez à partir de MSDEVDIR vers MSVCDIR, cela fonctionne.</span><span class="sxs-lookup"><span data-stu-id="f6ef4-114">If you copy that from MSDEVDIR to MSVCDIR, it works.</span></span> <span data-ttu-id="f6ef4-115">L’autre option consiste à copier Msdis100.dll et Rc.exe et Rcdll.dll vers MSVCDIR, et à définir VCBIN sur ce.</span><span class="sxs-lookup"><span data-stu-id="f6ef4-115">The other option is to copy Msdis100.dll and Rc.exe and Rcdll.dll to MSVCDIR, and set VCBIN to that.</span></span>

<span data-ttu-id="f6ef4-116">Cet outil est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="f6ef4-116">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6ef4-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f6ef4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6ef4-118">Outils de développement Windows Installer</span><span class="sxs-lookup"><span data-stu-id="f6ef4-118">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="f6ef4-119">Versions, outils et redistribuables publiés</span><span class="sxs-lookup"><span data-stu-id="f6ef4-119">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



