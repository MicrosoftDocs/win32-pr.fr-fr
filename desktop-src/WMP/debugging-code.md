---
title: Débogage du code
description: Débogage du code
ms.assetid: 315bc692-86bc-481e-abe4-f35309807a58
keywords:
- Apparences du lecteur Windows Media, code de débogage
- apparences, débogage de code
- débogage de code pour les apparences
- Apparences du lecteur Windows Media, journalisation
- apparences, journalisation
- fonctionnalité de journalisation dans les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e2305020b945d90adc1a47387ab2a13a3536e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311057"
---
# <a name="debugging-code"></a><span data-ttu-id="9282f-109">Débogage du code</span><span class="sxs-lookup"><span data-stu-id="9282f-109">Debugging Code</span></span>

<span data-ttu-id="9282f-110">Vous voudrez souvent voir ce qui se passe dans votre apparence.</span><span class="sxs-lookup"><span data-stu-id="9282f-110">You often will want to see what is happening inside your skin.</span></span> <span data-ttu-id="9282f-111">Pour ce faire, vous pouvez utiliser un contrôle de texte ou un fichier journal.</span><span class="sxs-lookup"><span data-stu-id="9282f-111">You can do this through a text control or through a log file.</span></span>

<span data-ttu-id="9282f-112">Vous pouvez créer un élément de **texte** et le placer temporairement sur une partie de votre apparence.</span><span class="sxs-lookup"><span data-stu-id="9282f-112">You can create a **TEXT** element and place it on a part of your skin temporarily.</span></span> <span data-ttu-id="9282f-113">Par exemple, vous pouvez utiliser le code suivant pour créer votre élément de **texte** :</span><span class="sxs-lookup"><span data-stu-id="9282f-113">For example, you could use the following code to create your **TEXT** element:</span></span>


```C++
<!-- debugging control -- remove later -->        
<TEXT
    id = "debug"
    foregroundColor = "white"
    backgroundColor = "black"
    value = "debug"
    top = "100"
    left = "50"
    height = "15"
    width = "100" 
    z-order = "5" />
<!-- end debugging control -->
```



<span data-ttu-id="9282f-114">Par exemple, si vous souhaitez voir la position actuelle du contenu multimédia numérique dans le lecteur Windows Media, vous pouvez utiliser du code semblable au suivant pour afficher la position actuelle dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="9282f-114">Then, for example, if you want to see the current position of the digital media content in Windows Media Player, you could use code similar to the following to display the current position in the text box.</span></span>


```C++
<PLAYER
    id = "myplayer">
    <CONTROLS
        id = "mycontrols"
        currentPosition_onchange="value=player.controls.currentPosition"/>
</PLAYER>

```



## <a name="to-write-debugging-information-to-a-log-file"></a><span data-ttu-id="9282f-115">Pour écrire des informations de débogage dans un fichier journal</span><span class="sxs-lookup"><span data-stu-id="9282f-115">To Write Debugging Information to a Log File</span></span>

<span data-ttu-id="9282f-116">Pour activer ou désactiver le débogage, modifiez la valeur de la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="9282f-116">To enable or disable debugging, change the value of the following registry key:</span></span>

<span data-ttu-id="9282f-117">**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ MediaPlayer \\ Preferences \\ ScriptDebugging**</span><span class="sxs-lookup"><span data-stu-id="9282f-117">**HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\MediaPlayer\\Preferences\\ScriptDebugging**</span></span>

<span data-ttu-id="9282f-118">Lorsque vous définissez la valeur sur 1, la journalisation est activée.</span><span class="sxs-lookup"><span data-stu-id="9282f-118">When you set the value to 1, logging is enabled.</span></span> <span data-ttu-id="9282f-119">Lorsque vous affectez la valeur 0 (valeur par défaut), la journalisation est désactivée.</span><span class="sxs-lookup"><span data-stu-id="9282f-119">When you set the value to 0 (the default), logging is disabled.</span></span>

<span data-ttu-id="9282f-120">Si la journalisation est activée, un fichier est placé sur l’ordinateur de l’utilisateur dans le même dossier que l’apparence.</span><span class="sxs-lookup"><span data-stu-id="9282f-120">If logging is enabled, a file will be placed on the user's computer in the same folder as the skin.</span></span> <span data-ttu-id="9282f-121">Le fichier est nommé «*filename* \_ 0 \_log.txt », où *filename* est le nom du fichier d’apparence.</span><span class="sxs-lookup"><span data-stu-id="9282f-121">The file will be named "*filename*\_0\_log.txt", where *filename* is the name of the skin file.</span></span> <span data-ttu-id="9282f-122">Le code de votre apparence peut écrire du texte dans ce fichier à l’aide du *thème*. méthode **logString** .</span><span class="sxs-lookup"><span data-stu-id="9282f-122">The code in your skin can write text to this file by using the *Theme*.**logString** method.</span></span> <span data-ttu-id="9282f-123">Cela peut être utile si vous souhaitez déterminer ce qui se passe dans votre code pendant qu’il est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9282f-123">This can be useful if you want to determine what is going on inside your code while it is running.</span></span> <span data-ttu-id="9282f-124">Notez que le fichier texte est encodé à l’aide de caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="9282f-124">Note that the text file is encoded with Unicode characters.</span></span>

<span data-ttu-id="9282f-125">Lorsque la journalisation est activée et que vous avez installé un système de développement qui fournit des fonctionnalités de débogage (par exemple, Microsoft Visual Studio), les exceptions qui ne sont pas gérées par votre code de script entraînent l’ouverture d’une boîte de dialogue d’avertissement du débogueur pour chaque exception.</span><span class="sxs-lookup"><span data-stu-id="9282f-125">When logging is enabled and you have installed a development system that provides debugging capabilities (such as Microsoft Visual Studio), exceptions that are not handled by your script code will cause a debugger warning dialog box to open for each exception.</span></span> <span data-ttu-id="9282f-126">Il s’agit d’une fonctionnalité utile pour vous aider à déboguer votre code de script.</span><span class="sxs-lookup"><span data-stu-id="9282f-126">This is a useful feature to help you debug your script code.</span></span> <span data-ttu-id="9282f-127">En outre, vous pouvez attacher manuellement le processus du lecteur Windows Media à votre débogueur lorsque la journalisation est activée.</span><span class="sxs-lookup"><span data-stu-id="9282f-127">Also, you can manually attach the Windows Media Player process to your debugger when logging is enabled.</span></span>

<span data-ttu-id="9282f-128">Ce kit de développement logiciel (SDK) comprend un exemple d’apparence, appelé « journalisation », qui illustre la fonctionnalité de journalisation dans les apparences.</span><span class="sxs-lookup"><span data-stu-id="9282f-128">This SDK includes a sample skin, called "logging", that demonstrates logging functionality in skins.</span></span> <span data-ttu-id="9282f-129">Pour en savoir plus sur l’utilisation des exemples, consultez [exemples](samples.md).</span><span class="sxs-lookup"><span data-stu-id="9282f-129">To learn more about using the samples, see [Samples](samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9282f-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9282f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9282f-131">**À propos des apparences**</span><span class="sxs-lookup"><span data-stu-id="9282f-131">**About Skins**</span></span>](about-skins.md)
</dt> </dl>

 

 




