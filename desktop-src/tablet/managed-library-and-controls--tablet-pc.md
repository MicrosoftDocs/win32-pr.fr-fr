---
description: Pour créer des applications Tablet PC en C \# et Visual Basic .net, votre projet dans Microsoft Visual Studio .net doit inclure une référence aux assemblys de la bibliothèque gérée Tablet PC. Cela permet d’accéder au modèle d’objet managé et aux contrôles.
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: Bibliothèque et contrôles managés (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7299a1df0cc1b64d650ec748eb2de01ad4b776f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536585"
---
# <a name="managed-library-and-controls-tablet-pc"></a><span data-ttu-id="0ce13-104">Bibliothèque et contrôles managés (Tablet PC)</span><span class="sxs-lookup"><span data-stu-id="0ce13-104">Managed Library and Controls (Tablet PC)</span></span>

<span data-ttu-id="0ce13-105">Pour créer des applications Tablet PC en C \# et Visual Basic .net, votre projet dans Microsoft Visual Studio .net doit inclure une référence aux assemblys de la bibliothèque gérée Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="0ce13-105">To build Tablet PC applications in C\# and Visual Basic .NET, your project in Microsoft Visual Studio .NET must include a reference to the Tablet PC managed library assemblies.</span></span> <span data-ttu-id="0ce13-106">Cela permet d’accéder au modèle d’objet managé et aux contrôles.</span><span class="sxs-lookup"><span data-stu-id="0ce13-106">This provides access to the managed object model and controls.</span></span>

## <a name="microsoft-visual-c-and-visual-basicnet"></a><span data-ttu-id="0ce13-107">Microsoft Visual C \# et visual Basic.net</span><span class="sxs-lookup"><span data-stu-id="0ce13-107">Microsoft Visual C\# and Visual Basic.NET</span></span>

<span data-ttu-id="0ce13-108">Dans Windows Vista, les assemblys de la bibliothèque gérée Tablet PC sont installés par défaut dans deux répertoires :</span><span class="sxs-lookup"><span data-stu-id="0ce13-108">In Windows Vista, the Tablet PC managed library assemblies are installed by default in two directories:</span></span>

-   <span data-ttu-id="0ce13-109"><systemdrive>: \\ Program Files fichiers \\ communs \\ répertoires Microsoft Shared \\ Ink</span><span class="sxs-lookup"><span data-stu-id="0ce13-109"><systemdrive>:\\Program Files\\Common Files\\Microsoft Shared\\Ink directory</span></span>
-   <span data-ttu-id="0ce13-110"><systemdrive>: \\ Program Files \\ Microsoft SDK \\ Windows \\ v 6.0 \\ bin</span><span class="sxs-lookup"><span data-stu-id="0ce13-110"><systemdrive>:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Bin</span></span>

<span data-ttu-id="0ce13-111">Pour ajouter une référence aux bibliothèques gérées de la plateforme Tablet PC dans Microsoft Visual Studio .NET :</span><span class="sxs-lookup"><span data-stu-id="0ce13-111">To add a reference to the Tablet PC platform managed libraries in Microsoft Visual Studio .NET:</span></span>

1.  <span data-ttu-id="0ce13-112">Ouvrez votre projet Visual Studio .NET.</span><span class="sxs-lookup"><span data-stu-id="0ce13-112">Open your Visual Studio .NET project.</span></span>
2.  <span data-ttu-id="0ce13-113">Dans le menu **Projet**, cliquez sur **Ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="0ce13-113">On the **Project** menu, click **Add Reference**.</span></span>
3.  <span data-ttu-id="0ce13-114">Sous l’onglet **.net** de la boîte de dialogue **Ajouter une référence** , dans la liste des composants, sélectionnez **API Microsoft Tablet PC**.</span><span class="sxs-lookup"><span data-stu-id="0ce13-114">On the **.NET** tab in the **Add Reference** dialog box, on the components list, select **Microsoft Tablet PC API**.</span></span>
4.  <span data-ttu-id="0ce13-115">Cliquez sur **Sélectionner**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ce13-115">Click **Select**, and then click **OK**.</span></span>

<span data-ttu-id="0ce13-116">Pour ajouter une référence aux API d’analyse d’encre dans Visual Studio .NET :</span><span class="sxs-lookup"><span data-stu-id="0ce13-116">To add a reference to the ink analysis APIs in Visual Studio .NET:</span></span>

1.  <span data-ttu-id="0ce13-117">Ouvrez votre projet Microsoft Visual Studio .NET.</span><span class="sxs-lookup"><span data-stu-id="0ce13-117">Open your Microsoft Visual Studio .NET project.</span></span>
2.  <span data-ttu-id="0ce13-118">Dans le menu **Projet**, cliquez sur **Ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="0ce13-118">On the **Project** menu, click **Add Reference**.</span></span>
3.  <span data-ttu-id="0ce13-119">Sous l’onglet **.net** de la boîte de dialogue **Ajouter une référence** , dans la liste des composants, sélectionnez **bibliothèque managée d’analyse Microsoft Tablet PC Ink**.</span><span class="sxs-lookup"><span data-stu-id="0ce13-119">On the **.NET** tab in the **Add Reference** dialog box, on the components list, select **Microsoft Tablet PC Ink Analysis Managed Library**.</span></span>
4.  <span data-ttu-id="0ce13-120">Cliquez sur **Sélectionner**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ce13-120">Click **Select**, and then click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="0ce13-121">Lors de la compilation d’applications qui utilisent Microsoft. Ink sur Visual Studio 2005, vous devez sélectionner **projet**, sélectionner **Propriétés**, puis **générer** et définir la plateforme cible = x86.</span><span class="sxs-lookup"><span data-stu-id="0ce13-121">When compiling applications that use Microsoft.Ink on Visual Studio 2005, you must select **Project**, select **Properties**, select **Build** and set Platform target=x86.</span></span> <span data-ttu-id="0ce13-122">Cette option n’est pas disponible dans les produits Microsoft Visual Studio Express.</span><span class="sxs-lookup"><span data-stu-id="0ce13-122">This option is not available in Microsoft Visual Studio Express products.</span></span>

 

 

 



