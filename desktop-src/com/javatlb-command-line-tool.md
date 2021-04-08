---
title: Utilitaire de Command-Line JavaTLB
description: Utilitaire de Command-Line JavaTLB
ms.assetid: b46d7bcc-ccd9-4242-9b19-f398d2cb8f91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a0214648f7ad86613d6b35e3084021e2be24aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675818"
---
# <a name="javatlb-command-line-tool"></a><span data-ttu-id="075d1-103">Utilitaire de Command-Line JavaTLB</span><span class="sxs-lookup"><span data-stu-id="075d1-103">JavaTLB Command-Line Tool</span></span>

<span data-ttu-id="075d1-104">JavaTLB est un composant de Visual J++ 5,0.</span><span class="sxs-lookup"><span data-stu-id="075d1-104">JavaTLB is a component of Visual J++ 5.0.</span></span> <span data-ttu-id="075d1-105">JavaTLB est une application de ligne de commande qui génère des fichiers de classe pour un objet COM.</span><span class="sxs-lookup"><span data-stu-id="075d1-105">JavaTLB is a command-line application that generates class files for a COM object.</span></span> <span data-ttu-id="075d1-106">Les méthodes qui contiennent des types de données qui ne peuvent pas être représentés avec précision et en toute sécurité dans Java ne sont pas converties.</span><span class="sxs-lookup"><span data-stu-id="075d1-106">Methods that contain data types that cannot be accurately and safely represented in Java are not converted.</span></span>

<span data-ttu-id="075d1-107">Contrairement à l' [Assistant bibliothèque de types Java](java-type-library-wizard.md), JavaTLB ne génère pas de fichier Résumé contenant les informations de la bibliothèque de types Java.</span><span class="sxs-lookup"><span data-stu-id="075d1-107">Unlike the [Java Type Library Wizard](java-type-library-wizard.md), JavaTLB does not generate a summary file containing the Java type library information.</span></span>

<span data-ttu-id="075d1-108">Pour générer des fichiers de classe Java pour un objet COM unique, à partir de l’invite de commandes, exécutez :</span><span class="sxs-lookup"><span data-stu-id="075d1-108">To generate Java class files for a single COM object, from the command prompt run:</span></span>

<span data-ttu-id="075d1-109"> *nom du fichier* JavaTLB</span><span class="sxs-lookup"><span data-stu-id="075d1-109">**javatlb** *filename*</span></span>

<span data-ttu-id="075d1-110">où *filename* est le nom du fichier qui contient la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="075d1-110">where *filename* is the name of the file that contains the type library.</span></span> <span data-ttu-id="075d1-111">Ce fichier peut avoir l’une des extensions de nom de fichier suivantes :. tlb,. olb,. ocx,. dll ou. exe.</span><span class="sxs-lookup"><span data-stu-id="075d1-111">This file may have any of the following file name extensions: .tlb, .olb, .ocx, .dll, or .exe.</span></span>

<span data-ttu-id="075d1-112">Pour générer des fichiers de classe Java pour plusieurs objets COM, à partir de l’invite de commandes, exécutez :</span><span class="sxs-lookup"><span data-stu-id="075d1-112">To generate Java class files for multiple COM objects, from the command prompt run:</span></span>

<span data-ttu-id="075d1-113">\**JavaTLB @ \* \* \* TextFile*</span><span class="sxs-lookup"><span data-stu-id="075d1-113">\**javatlb @\*\*\*TextFile*</span></span>

<span data-ttu-id="075d1-114">où *TextFile* est le nom d’un fichier texte qui contient une liste des fichiers contenant les bibliothèques de types de l’objet com.</span><span class="sxs-lookup"><span data-stu-id="075d1-114">where *TextFile* is the name of a text file that contains a list of the files containing the COM object's type libraries.</span></span>

> [!Note]  
> <span data-ttu-id="075d1-115">Dans Visual J++ 6,0, l’outil en ligne de commande JavaTLB est remplacé par l' [outil JActiveX](jactivex-command-line-tool.md).</span><span class="sxs-lookup"><span data-stu-id="075d1-115">In Visual J++ 6.0, the JavaTLB command-line tool is replaced by the [JActiveX tool](jactivex-command-line-tool.md).</span></span> <span data-ttu-id="075d1-116">Pour plus d’informations, consultez la documentation de Visual J++ 6,0.</span><span class="sxs-lookup"><span data-stu-id="075d1-116">For more information, see the Visual J++ 6.0 documentation.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="075d1-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="075d1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="075d1-118">Conversion en Java</span><span class="sxs-lookup"><span data-stu-id="075d1-118">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




