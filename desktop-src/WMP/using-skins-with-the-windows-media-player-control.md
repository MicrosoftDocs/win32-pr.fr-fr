---
title: Utilisation d’habillages avec le contrôle du lecteur Windows Media
description: Utilisation d’habillages avec le contrôle du lecteur Windows Media
ms.assetid: 0381e0e4-c686-4ab4-b947-b883b6f4e06e
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX, incorporation
- Lecteur Windows Media, C++
- Windows Media Player Object Model, C++
- modèle objet, C++
- Windows Media Player Mobile, C++
- Contrôle ActiveX du lecteur Windows Media, C++
- Windows Media Player Mobile, contrôle ActiveX, C++
- Contrôle ActiveX, C++
- Incorporation de programmes C++
- incorporation, programmes C++
- Contrôle ActiveX du lecteur Windows Media, apparences
- Windows Media Player Mobile contrôle ActiveX, Skins
- Contrôle ActiveX, apparences
- apparences, incorporer un contrôle ActiveX
- Apparences du lecteur Windows Media, incorporer un contrôle ActiveX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3714a8be9e471541d008fcb76a4b0398dba2162b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196811"
---
# <a name="using-skins-with-the-windows-media-player-control"></a><span data-ttu-id="3baf7-124">Utilisation d’habillages avec le contrôle du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="3baf7-124">Using Skins with the Windows Media Player Control</span></span>

<span data-ttu-id="3baf7-125">Lorsque vous incorporez le contrôle du lecteur Windows Media dans un programme C++, vous pouvez personnaliser l’interface utilisateur du lecteur en lui appliquant un fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="3baf7-125">When you embed the Windows Media Player control in a C++ program, you can customize the Player user interface (UI) by applying a skin definition file to it.</span></span> <span data-ttu-id="3baf7-126">Un fichier de définition d’apparence est un document XML qui spécifie la disposition des composants d’interface utilisateur standard et personnalisables, ainsi que les graphiques qui l’accompagnent.</span><span class="sxs-lookup"><span data-stu-id="3baf7-126">A skin definition file is an XML-based document specifying the layout of standard and customizable UI components and any accompanying graphics.</span></span> <span data-ttu-id="3baf7-127">À l’aide de Microsoft JScript, vous pouvez spécifier le comportement de ces composants et manipuler le contrôle du lecteur Windows Media sans la surcharge de la syntaxe C++ et COM.</span><span class="sxs-lookup"><span data-stu-id="3baf7-127">Using Microsoft JScript, you can specify the behavior of these components and manipulate the Windows Media Player control without the overhead of C++ and COM syntax.</span></span>

<span data-ttu-id="3baf7-128">Les apparences permettent de conserver facilement votre code d’interface utilisateur et votre code de programme principal afin qu’ils puissent être gérés et développés indépendamment.</span><span class="sxs-lookup"><span data-stu-id="3baf7-128">Skins provide an easy way to keep your user interface code and your main program code separate so that they can be maintained and developed independently.</span></span> <span data-ttu-id="3baf7-129">Vous pouvez également réutiliser des apparences conçues à l’origine pour une utilisation par le lecteur autonome en mode apparence.</span><span class="sxs-lookup"><span data-stu-id="3baf7-129">You can also reuse skins originally designed for use by the standalone Player in skin mode.</span></span> <span data-ttu-id="3baf7-130">Le code d’apparence que vous concevez spécifiquement pour les programmes C++ peut interagir avec vos programmes par le biais d’un objet scriptable que votre programme peut fournir.</span><span class="sxs-lookup"><span data-stu-id="3baf7-130">Skin code that you design specifically for C++ programs can interact with your programs through a scriptable object that your program can provide.</span></span>

<span data-ttu-id="3baf7-131">Pour activer le mode apparence pour le contrôle du lecteur Windows Media, votre programme doit implémenter l’interface **IWMPRemoteMediaServices** .</span><span class="sxs-lookup"><span data-stu-id="3baf7-131">To enable skin mode for the Windows Media Player control, your program must implement the **IWMPRemoteMediaServices** interface.</span></span> <span data-ttu-id="3baf7-132">Bien que vous puissiez utiliser les apparences avec le contrôle et le contrôle à distance en même temps, vous pouvez utiliser cette interface pour activer l’une ou l’autre des fonctionnalités sans activer l’autre.</span><span class="sxs-lookup"><span data-stu-id="3baf7-132">Although you can use skins with the control and remote the control at the same time, you can use this interface to enable either feature without enabling the other.</span></span> <span data-ttu-id="3baf7-133">Pour désactiver la communication à distance, transmettez simplement une valeur « local » comme paramètre de sortie de la méthode **GetServiceType** et retournez un HRESULT de E \_ NOTIMPL à partir de la méthode **GetApplicationName** .</span><span class="sxs-lookup"><span data-stu-id="3baf7-133">To disable remoting, simply pass a value of "Local" as the out parameter of the **GetServiceType** method, and return an HRESULT of E\_NOTIMPL from the **GetApplicationName** method.</span></span>

<span data-ttu-id="3baf7-134">Pour basculer le contrôle du lecteur Windows Media en mode apparence, appelez la méthode **IWMPPlayer ::p ut \_ UIMODE** , en passant la valeur « Custom ».</span><span class="sxs-lookup"><span data-stu-id="3baf7-134">To switch the Windows Media Player control to skin mode, call the **IWMPPlayer::put\_uiMode** method, passing in a value of "custom".</span></span> <span data-ttu-id="3baf7-135">Spécifiez le chemin d’accès et le nom de fichier du fichier de définition d’apparence à utiliser en le renvoyant à partir de la méthode **IWMPRemoteMediaServices :: GetCustomUIMode** .</span><span class="sxs-lookup"><span data-stu-id="3baf7-135">Specify the path and file name of the skin definition file to use by returning it from the **IWMPRemoteMediaServices::GetCustomUIMode** method.</span></span>

<span data-ttu-id="3baf7-136">Si vous souhaitez fournir un objet scriptable pour la communication entre votre apparence et votre programme, transmettez un nom et un pointeur vers un pointeur **IDispatch** en tant que deux paramètres de sortie de la méthode **IWMPRemoteMediaServices :: GetScriptableObject** .</span><span class="sxs-lookup"><span data-stu-id="3baf7-136">If you want to provide a scriptable object for communication between your skin and your program, pass a name and a pointer to an **IDispatch** pointer as the two out parameters of the **IWMPRemoteMediaServices::GetScriptableObject** method.</span></span> <span data-ttu-id="3baf7-137">Votre apparence peut ensuite effectuer des appels à l’objet scriptable en utilisant le nom spécifié comme s’il s’agissait d’un attribut global similaire à l’attribut global **Player** .</span><span class="sxs-lookup"><span data-stu-id="3baf7-137">Your skin can then make calls to the scriptable object by using the name specified as though it were a global attribute similar to the **player** global attribute.</span></span>

<span data-ttu-id="3baf7-138">Une apparence appliquée à un contrôle du lecteur Windows Media distant peut accéder à l’objet **PlayerApplication** à l’aide d’un autre attribut global appelé **PlayerApplication**.</span><span class="sxs-lookup"><span data-stu-id="3baf7-138">A skin applied to a remoted Windows Media Player control can access the **PlayerApplication** object using another global attribute called **playerApplication**.</span></span> <span data-ttu-id="3baf7-139">Étant donné que la propriété **Player. playerApplication** n’est pas accessible par les apparences, vous devez utiliser cet attribut global lorsque vous souhaitez que votre code de peau gère l’ancrage et la déconnexion.</span><span class="sxs-lookup"><span data-stu-id="3baf7-139">Because the **Player.playerApplication** property cannot be accessed by skins, you must use this global attribute when you want your skin code to manage docking and undocking.</span></span>

## <a name="samples"></a><span data-ttu-id="3baf7-140">Exemples</span><span class="sxs-lookup"><span data-stu-id="3baf7-140">Samples</span></span>

<span data-ttu-id="3baf7-141">Le package d’installation du kit de développement logiciel (SDK) Windows Media Player installe un exemple qui illustre l’application d’une apparence au contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3baf7-141">The Windows Media Player SDK setup package installs a sample that demonstrates applying a skin to the Windows Media Player control.</span></span> <span data-ttu-id="3baf7-142">Pour plus d’informations, consultez l’exemple RemoteSkin.</span><span class="sxs-lookup"><span data-stu-id="3baf7-142">See the RemoteSkin sample for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3baf7-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3baf7-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3baf7-144">**Exemples**</span><span class="sxs-lookup"><span data-stu-id="3baf7-144">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="3baf7-145">**Utilisation du contrôle du lecteur Windows Media dans un programme C++**</span><span class="sxs-lookup"><span data-stu-id="3baf7-145">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




