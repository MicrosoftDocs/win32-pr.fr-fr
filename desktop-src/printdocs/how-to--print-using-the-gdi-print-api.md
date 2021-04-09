---
description: Cette rubrique explique comment imprimer à partir d’un programme Windows natif à l’aide du GDI&\# 160 ; Imprimer&\# 160 ; MobileVBActiveX.
ms.assetid: C212DD92-2B90-45BC-8746-29C193FBDF69
title: 'Comment : imprimer à l’aide de l’API d’impression GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d6351e228297b5378b54879548b823f81894b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868534"
---
# <a name="how-to-print-using-the-gdi-print-api"></a><span data-ttu-id="042f8-103">Comment : imprimer à l’aide de l’API d’impression GDI</span><span class="sxs-lookup"><span data-stu-id="042f8-103">How To: Print Using the GDI Print API</span></span>

<span data-ttu-id="042f8-104">Cette rubrique explique comment imprimer à partir d’un programme Windows natif à l’aide de l' [API d’impression GDI](gdi-printing.md).</span><span class="sxs-lookup"><span data-stu-id="042f8-104">This topic introduces how to print from a native Windows program using the [GDI Print API](gdi-printing.md).</span></span>

## <a name="overview"></a><span data-ttu-id="042f8-105">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="042f8-105">Overview</span></span>

<span data-ttu-id="042f8-106">L’impression fait généralement partie intégrante d’un programme Windows natif. il ne s’agit donc pas d’une fonctionnalité que vous pouvez ajouter facilement après avoir écrit le programme.</span><span class="sxs-lookup"><span data-stu-id="042f8-106">Printing is usually an integral part of a native Windows program, so it is not a feature that you can add easily after you have written the program.</span></span> <span data-ttu-id="042f8-107">Lors de la conception d’un programme pour Windows 7, vous devez envisager d’utiliser l' [API d’impression XPS](xps-printing.md) pour fournir la fonctionnalité d’impression, car elle offre la plus grande compatibilité à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="042f8-107">When designing a program for Windows 7, you should consider using the [XPS Print API](xps-printing.md) to provide the printing functionality because it provides the most compatibility for the future.</span></span> <span data-ttu-id="042f8-108">Les programmes qui doivent s’exécuter sous Windows Vista et les versions antérieures de Windows utiliseront très probablement l' [API d’impression GDI](gdi-printing.md) pour fournir des fonctionnalités d’impression.</span><span class="sxs-lookup"><span data-stu-id="042f8-108">Programs that must run on Windows Vista and earlier versions of Windows will most likely use the [GDI Print API](gdi-printing.md) to provide printing functionality.</span></span> <span data-ttu-id="042f8-109">L’API d’impression GDI est également prise en charge dans Windows 7, mais elle est plus limitée que l’API d’impression XPS.</span><span class="sxs-lookup"><span data-stu-id="042f8-109">The GDI Print API is also supported in Windows 7, but it is more limited than the XPS Print API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="042f8-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="042f8-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="042f8-111">Utilisation de l’impression</span><span class="sxs-lookup"><span data-stu-id="042f8-111">Using Printing</span></span>](using-printing.md)
</dt> <dt>

[<span data-ttu-id="042f8-112">Comment imprimer à partir d’une application Windows</span><span class="sxs-lookup"><span data-stu-id="042f8-112">How to print from a Windows application</span></span>](how-to--print-from-a-windows-application.md)
</dt> </dl>

 

 



