---
title: Appel du compilateur MIDL
description: Le compilateur MIDL peut générer du code pour différentes plateformes et versions système. Consultez le commutateur/target pour en savoir plus sur les commutateurs suggérés et sur la façon de générer du code optimisé pour une version particulière.
ms.assetid: 57730efa-71c3-4746-83f4-c7e327888efc
keywords:
- Compilateur MIDL MIDL, appeler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7e03abc49007b823f509acb35bd34ce6e47d80
ms.sourcegitcommit: 1e8e6e6f27c909900cfa8be58b042456331a82ad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/15/2019
ms.locfileid: "106510848"
---
# <a name="invoking-the-midl-compiler"></a><span data-ttu-id="b1702-105">Appel du compilateur MIDL</span><span class="sxs-lookup"><span data-stu-id="b1702-105">Invoking the MIDL Compiler</span></span>

<span data-ttu-id="b1702-106">Le compilateur MIDL peut générer du code pour différentes plateformes et versions système.</span><span class="sxs-lookup"><span data-stu-id="b1702-106">The MIDL compiler can generate code for different platforms and system releases.</span></span> <span data-ttu-id="b1702-107">Consultez le commutateur [**/target**](-target.md) pour en savoir plus sur les commutateurs suggérés et sur la façon de générer du code optimisé pour une version particulière.</span><span class="sxs-lookup"><span data-stu-id="b1702-107">Consult the [**/target**](-target.md) switch to learn more about suggested switches and how to generate code optimized for a particular release.</span></span>

<span data-ttu-id="b1702-108">Exécutez le compilateur MIDL à partir de la ligne de commande à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1702-108">Run the MIDL compiler from the command line using the following command:</span></span>

<span data-ttu-id="b1702-109"> *<  options >* MIDL **NomFichier. idl**</span><span class="sxs-lookup"><span data-stu-id="b1702-109">**midl** *<***options***>* **filename.idl**</span></span>

<span data-ttu-id="b1702-110">où *<  options >* représente les options de ligne de commande que vous souhaitez utiliser, et nom_fichier. idl est le nom du fichier MIDL à compiler.</span><span class="sxs-lookup"><span data-stu-id="b1702-110">where *<***options***>* represents the command-line options you want to use, and Filename.idl is the name of the MIDL file to compile.</span></span>

<span data-ttu-id="b1702-111">Une liste complète des commutateurs et options du compilateur MIDL est disponible quand vous utilisez le compilateur MIDL [**/Help**](-help-.md) et/ ?</span><span class="sxs-lookup"><span data-stu-id="b1702-111">A complete listing of MIDL compiler switches and options is available when you use the MIDL compiler [**/help**](-help-.md) and /?</span></span> <span data-ttu-id="b1702-112">Active.</span><span class="sxs-lookup"><span data-stu-id="b1702-112">switches.</span></span> <span data-ttu-id="b1702-113">Les commutateurs sont organisés par catégories.</span><span class="sxs-lookup"><span data-stu-id="b1702-113">The switches are organized by categories.</span></span> <span data-ttu-id="b1702-114">Pour plus d’informations, consultez la [Référence du Command-Line MIDL](midl-command-line-reference.md).</span><span class="sxs-lookup"><span data-stu-id="b1702-114">For details, see the [MIDL Command-Line Reference](midl-command-line-reference.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b1702-115">Le nouvel indicateur global **$ ( \_ optimisation MIDL)** existe dans Win32. mak.</span><span class="sxs-lookup"><span data-stu-id="b1702-115">The new global flag **$(MIDL\_OPTIMIZATION)** exists in win32.mak.</span></span> <span data-ttu-id="b1702-116">Lorsqu’un fichier. idl est compilé à l’aide de cet indicateur, le stub généré peut utiliser les fonctionnalités RPC les plus récentes disponibles sur la plateforme spécifiée et améliorer potentiellement les performances et la stabilité de l’application.</span><span class="sxs-lookup"><span data-stu-id="b1702-116">When an .idl file is compiled using this flag, the generated stub can utilize the latest RPC features available on the specified platform, and potentially improve the application's performance and stability.</span></span> <span data-ttu-id="b1702-117">Il est recommandé que les applications utilisent cet indicateur lors de l’utilisation de MIDL.</span><span class="sxs-lookup"><span data-stu-id="b1702-117">It's recommended that applications use this flag when using MIDL.</span></span>
>
> <span data-ttu-id="b1702-118">**MIDL** **$ ( \_ optimisation MIDL)** **...**</span><span class="sxs-lookup"><span data-stu-id="b1702-118">**midl** **$(MIDL\_OPTIMIZATION)** **...**</span></span>