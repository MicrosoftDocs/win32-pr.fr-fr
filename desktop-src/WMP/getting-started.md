---
title: Prise en main avec le kit de développement logiciel (SDK) Windows Media Player
description: Prise en main avec le kit de développement logiciel (SDK) Windows Media Player
ms.assetid: 47c333dc-dad3-4430-a053-016d2c931f74
keywords:
- Windows Media Player Mobile, plug-ins
- Windows Media Player Mobile, plug-ins d’interface utilisateur
- Plug-ins Windows Media Player Mobile
- plug-ins, interface utilisateur
- plug-ins, Windows Media Player Mobile
- plug-ins d’interface utilisateur, Windows Media Player Mobile
- Plug-ins d’interface utilisateur, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a962c1f815f820a0b2e8125872baf9d02e301dc
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739301"
---
# <a name="getting-started-with-the-windows-media-player-sdk"></a><span data-ttu-id="3e626-110">Prise en main avec le kit de développement logiciel (SDK) Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="3e626-110">Getting Started with the Windows Media Player SDK</span></span>

<span data-ttu-id="3e626-111">Pour créer votre plug-in, vous devez d’abord installer Microsoft eMbedded Visual C++ 4,0 et Visual Studio 2003.</span><span class="sxs-lookup"><span data-stu-id="3e626-111">To create your plug-in, you first need to install Microsoft eMbedded Visual C++ 4.0 and Visual Studio 2003.</span></span> <span data-ttu-id="3e626-112">Vous devez également installer le kit de développement logiciel (SDK) Pocket PC 2003 ou le kit de développement logiciel (SDK) Smartphone 2003, qui sont des téléchargements distincts.</span><span class="sxs-lookup"><span data-stu-id="3e626-112">You must also install the Pocket PC 2003 SDK or the Smartphone 2003 SDK, which are separate downloads.</span></span> <span data-ttu-id="3e626-113">Pour compiler et exécuter le projet, un Pocket PC ou un appareil smartphone exécutant le système d’exploitation Windows Mobile 2003 deuxième édition doit être synchronisé avec l’ordinateur de développement à l’aide de Microsoft ActiveSync® 3.7.1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3e626-113">To compile and run the project, a Pocket PC or Smartphone device running the Windows Mobile 2003 Second Edition operating system must be synchronized with the development computer by using Microsoft ActiveSync® 3.7.1 or later.</span></span>

<span data-ttu-id="3e626-114">Étant donné que les plug-ins d’IU sur les périphériques Windows Mobile utilisent le même modèle de plug-in que les versions de bureau, vous pouvez utiliser l’Assistant de plug-in du lecteur Windows Media comme point de départ lors de la création d’un plug-in d’interface utilisateur d’arrière-plan qui fonctionne avec le lecteur Windows Media 10 mobile.</span><span class="sxs-lookup"><span data-stu-id="3e626-114">Because UI plug-ins on Windows Mobile devices use the same plug-in model as the desktop versions, you can use the Windows Media Player Plug-in Wizard as a starting point when creating a background UI plug-in that will work with Windows Media Player 10 Mobile.</span></span>

<span data-ttu-id="3e626-115">Pour créer un code de plug-in d’interface utilisateur, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="3e626-115">To create UI plug-in code, do the following:</span></span>

1.  <span data-ttu-id="3e626-116">Ouvrez Visual Studio 2003 et démarrez un nouveau projet dans Visual C++.</span><span class="sxs-lookup"><span data-stu-id="3e626-116">Open Visual Studio 2003, and start a new project in Visual C++.</span></span>
2.  <span data-ttu-id="3e626-117">Sélectionnez l' **Assistant de plug-in du lecteur Windows Media** dans le volet **modèles** .</span><span class="sxs-lookup"><span data-stu-id="3e626-117">Select **Windows Media Player Plug-in Wizard** from the **Templates** pane.</span></span>
3.  <span data-ttu-id="3e626-118">Nommez votre projet NetworkPlugin, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e626-118">Name your project NetworkPlugin and click **OK**.</span></span>
4.  <span data-ttu-id="3e626-119">Sélectionnez **plug-in d’interface utilisateur** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="3e626-119">Select **UI Plug-in** and click **Next**.</span></span>
5.  <span data-ttu-id="3e626-120">Sélectionnez **arrière-plan** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="3e626-120">Select **Background** and click **Next**.</span></span>
6.  <span data-ttu-id="3e626-121">Cliquez sur **Suivant** pour terminer l'Assistant.</span><span class="sxs-lookup"><span data-stu-id="3e626-121">Click **Next** to finish the wizard.</span></span> <span data-ttu-id="3e626-122">Si vous envisagez de surveiller les événements avec votre plug-in, vous devez activer la case à cocher **écouter les événements** avant de terminer l’Assistant et vous devez lire la documentation de l’interface **IWMPEvents** pour connaître les événements pris en charge sur le lecteur Windows Media 10 mobile.</span><span class="sxs-lookup"><span data-stu-id="3e626-122">If you are going to monitor events with your plug-in, you must check **Listen to events** before finishing the wizard, and you should read the documentation for the **IWMPEvents** interface to find out which events are supported on Windows Media Player 10 Mobile.</span></span>

<span data-ttu-id="3e626-123">Maintenant que vous avez créé votre code de plug-in d’interface utilisateur, vous devez créer un projet de DLL Windows CE vide dans Embedded Visual C++ 4,0.</span><span class="sxs-lookup"><span data-stu-id="3e626-123">Now that you have created your UI plug-in code, you need to create an empty Windows CE DLL project in eMbedded Visual C++ 4.0.</span></span> <span data-ttu-id="3e626-124">Copiez ensuite vos fichiers sources générés par l’Assistant dans ce nouveau projet afin qu’ils se compilent avec le compilateur ARM4.</span><span class="sxs-lookup"><span data-stu-id="3e626-124">Then copy your wizard-generated source files to that new project so that they will compile with the ARM4 compiler.</span></span>

<span data-ttu-id="3e626-125">Pour créer un projet vide</span><span class="sxs-lookup"><span data-stu-id="3e626-125">To create an empty project</span></span>

1.  <span data-ttu-id="3e626-126">Démarrez un nouveau projet dans le Visual C++ incorporé, puis sélectionnez **bibliothèque de Dynamic-Link WCE** dans le volet **projets** .</span><span class="sxs-lookup"><span data-stu-id="3e626-126">Start a new project in eMbedded Visual C++, and then select **WCE Dynamic-Link Library** from the **Projects** pane.</span></span>
2.  <span data-ttu-id="3e626-127">Nommez votre projet et cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e626-127">Name your project and click **OK**.</span></span>
3.  <span data-ttu-id="3e626-128">Assurez-vous qu' **un projet Windows ce dll vide** est sélectionné, puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="3e626-128">Make sure **An empty Windows CE DLL project** is selected, and then click **Finish**.</span></span>
4.  <span data-ttu-id="3e626-129">Cliquez sur l’élément de menu **projet** .</span><span class="sxs-lookup"><span data-stu-id="3e626-129">Click the **Project** menu item.</span></span>
5.  <span data-ttu-id="3e626-130">Sélectionnez **Ajouter au projet**, puis cliquez sur **fichiers**.</span><span class="sxs-lookup"><span data-stu-id="3e626-130">Select **Add to Project**, and then click **Files**.</span></span>
6.  <span data-ttu-id="3e626-131">Sélectionnez les fichiers C++ que vous avez créés à l’aide de l’Assistant de plug-in, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e626-131">Select the C++ files you created with the plug-in wizard, and then click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e626-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3e626-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e626-133">**Création d’un plug-in d’interface utilisateur pour Windows Media Player 10 mobile**</span><span class="sxs-lookup"><span data-stu-id="3e626-133">**Creating a User Interface Plug-in for Windows Media Player 10 Mobile**</span></span>](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> <dt>

[<span data-ttu-id="3e626-134">**Interface IWMPEvents**</span><span class="sxs-lookup"><span data-stu-id="3e626-134">**IWMPEvents Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> </dl>

 

 




