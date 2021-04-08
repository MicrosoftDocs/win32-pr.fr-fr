---
description: Les utilisateurs peuvent configurer le débogage automatique pour les aider à déterminer la raison pour laquelle leur système ou une application a cessé de répondre.
ms.assetid: c3c7aa98-c298-452c-b8d0-10a08b4d82a3
title: Configuration du débogage automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2630784d678e08b67a93d00ec52d9bc67c949bc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109999"
---
# <a name="configuring-automatic-debugging"></a><span data-ttu-id="d5635-103">Configuration du débogage automatique</span><span class="sxs-lookup"><span data-stu-id="d5635-103">Configuring Automatic Debugging</span></span>

<span data-ttu-id="d5635-104">Les utilisateurs peuvent configurer le débogage automatique pour les aider à déterminer la raison pour laquelle leur système ou une application a cessé de répondre.</span><span class="sxs-lookup"><span data-stu-id="d5635-104">Users can configure automatic debugging to help them determine why their system or an application has stopped responding.</span></span>

## <a name="configuring-automatic-debugging-for-system-crashes"></a><span data-ttu-id="d5635-105">Configuration du débogage automatique pour les pannes système</span><span class="sxs-lookup"><span data-stu-id="d5635-105">Configuring Automatic Debugging for System Crashes</span></span>

<span data-ttu-id="d5635-106">Pour configurer l’ordinateur cible afin de générer un fichier de vidage sur incident lorsque le système ne répond plus, utilisez l’application **système** dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="d5635-106">To configure the target computer to generate a crash dump file when the system stops responding, use the **System** application in Control Panel.</span></span> <span data-ttu-id="d5635-107">Cliquez sur **paramètres système avancés**, qui affiche la boîte de dialogue **Propriétés système** .</span><span class="sxs-lookup"><span data-stu-id="d5635-107">Click **Advanced system settings**, which displays the **System Properties** dialog box.</span></span> <span data-ttu-id="d5635-108">Sous l’onglet **avancé** de cette zone, cliquez sur **paramètres** sous **démarrage et récupération**, puis utilisez les options de récupération appropriées.</span><span class="sxs-lookup"><span data-stu-id="d5635-108">On the **Advanced** tab of that box, click **Settings** under **Startup and Recovery**, and then use the appropriate recovery options.</span></span> <span data-ttu-id="d5635-109">Vous pouvez également configurer les options de vidage sur incident à l’aide de la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="d5635-109">Alternatively, you can configure crash dump options using the following registry key:</span></span>

<span data-ttu-id="d5635-110">**HKEY \_ \_** \\  \\  \\ **Contrôle** CurrentControlSet du système \\  de l’ordinateur local CrashControl</span><span class="sxs-lookup"><span data-stu-id="d5635-110">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**CrashControl**</span></span>

<span data-ttu-id="d5635-111">Le fichier que vous pouvez spécifier est le fichier de vidage sur incident.</span><span class="sxs-lookup"><span data-stu-id="d5635-111">The file you can specify is the crash dump file.</span></span> <span data-ttu-id="d5635-112">Son nom par défaut est Memory. dmp.</span><span class="sxs-lookup"><span data-stu-id="d5635-112">Its default name is Memory.dmp.</span></span> <span data-ttu-id="d5635-113">Vous pouvez déboguer un vidage sur incident à l’aide d’un débogueur en mode noyau, tel que WinDbg ou KD.</span><span class="sxs-lookup"><span data-stu-id="d5635-113">You can debug a crash dump with a kernel-mode debugger, such as WinDbg or KD.</span></span> <span data-ttu-id="d5635-114">Pour plus d’informations, consultez la documentation fournie avec le débogueur.</span><span class="sxs-lookup"><span data-stu-id="d5635-114">For more information, see the documentation included with the debugger.</span></span>

## <a name="configuring-automatic-debugging-for-application-crashes"></a><span data-ttu-id="d5635-115">Configuration du débogage automatique pour les incidents d’application</span><span class="sxs-lookup"><span data-stu-id="d5635-115">Configuring Automatic Debugging for Application Crashes</span></span>

<span data-ttu-id="d5635-116">Lorsqu’une application cesse de répondre (par exemple, après une violation d’accès), le système appelle automatiquement un débogueur qui est spécifié dans le registre pour le débogage post-mortem, l’ID de processus et le descripteur d’événement sont passés au débogueur si la ligne de commande est correctement configurée.</span><span class="sxs-lookup"><span data-stu-id="d5635-116">When an application stops responding (for example, after an access violation), the system automatically invokes a debugger that is specified in the registry for postmortem debugging, The process ID and event handle are passed to the debugger if the command line is properly configured.</span></span> <span data-ttu-id="d5635-117">La procédure suivante décrit comment spécifier un débogueur dans le registre.</span><span class="sxs-lookup"><span data-stu-id="d5635-117">The following procedure describes how to specify a debugger in the registry.</span></span>

<span data-ttu-id="d5635-118">**Pour définir un débogueur en tant que débogueur post-mortem**</span><span class="sxs-lookup"><span data-stu-id="d5635-118">**To set a debugger as the postmortem debugger**</span></span>

1.  <span data-ttu-id="d5635-119">Accédez à la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="d5635-119">Go to the following registry key:</span></span>

    <span data-ttu-id="d5635-120">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**</span><span class="sxs-lookup"><span data-stu-id="d5635-120">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**AeDebug**</span></span>

2.  <span data-ttu-id="d5635-121">Ajoutez ou modifiez la valeur du **débogueur** à l’aide d’une chaîne de Registre \_ SZ qui spécifie la ligne de commande pour le débogueur.</span><span class="sxs-lookup"><span data-stu-id="d5635-121">Add or edit the **Debugger** value, using a REG\_SZ string that specifies the command line for the debugger.</span></span>

    <span data-ttu-id="d5635-122">La chaîne doit inclure le chemin d’accès complet au fichier exécutable du débogueur.</span><span class="sxs-lookup"><span data-stu-id="d5635-122">The string should include the fully qualified path to the debugger executable.</span></span> <span data-ttu-id="d5635-123">Indiquez l’ID de processus et le descripteur d’événement avec les paramètres « % LD » dans la ligne de commande du débogueur.</span><span class="sxs-lookup"><span data-stu-id="d5635-123">Indicate the process ID and event handle with "%ld" parameters to the debugger command line.</span></span> <span data-ttu-id="d5635-124">Différents débogueurs peuvent avoir leurs propres syntaxes de paramètre pour indiquer ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="d5635-124">Different debuggers may have their own parameter syntaxes for indicating these values.</span></span> <span data-ttu-id="d5635-125">Quand le débogueur est appelé, le premier « % LD » est remplacé par l’ID de processus et le deuxième « % LD » est remplacé par le handle d’événement.</span><span class="sxs-lookup"><span data-stu-id="d5635-125">When the debugger is invoked, the first "%ld" is replaced with the process ID and the second "%ld" is replaced with the event handle.</span></span>

    <span data-ttu-id="d5635-126">Le texte suivant est un exemple de configuration de WinDbg en tant que débogueur.</span><span class="sxs-lookup"><span data-stu-id="d5635-126">The following text is an example of how to setup up WinDbg as the debugger.</span></span>

    ``` syntax
    "C:\debuggers\windbg.exe" -p %ld -e %ld -g
    ```

3.  <span data-ttu-id="d5635-127">Si vous souhaitez que le débogueur soit appelé sans intervention de l’utilisateur, ajoutez ou modifiez la valeur **auto** , à l’aide d’une \_ chaîne sz reg qui spécifie si le système doit afficher une boîte de dialogue à l’utilisateur avant que le débogueur ne soit appelé.</span><span class="sxs-lookup"><span data-stu-id="d5635-127">If you want the debugger to be invoked without user interaction, add or edit the **Auto** value, using a REG\_SZ string that specifies whether the system should display a dialog box to the user before the debugger is invoked.</span></span> <span data-ttu-id="d5635-128">La chaîne « 1 » désactive la boîte de dialogue. la chaîne « 0 » active la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d5635-128">The string "1" disables the dialog box; the string "0" enables the dialog box.</span></span>

## <a name="excluding-an-application-from-automatic-debugging"></a><span data-ttu-id="d5635-129">Exclusion d’une application du débogage automatique</span><span class="sxs-lookup"><span data-stu-id="d5635-129">Excluding an Application from Automatic Debugging</span></span>

<span data-ttu-id="d5635-130">La procédure suivante décrit comment exclure une application du débogage automatique une fois que la valeur **auto** sous la clé **AeDebug** a été définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="d5635-130">The following procedure describes how to exclude an application from automatic debugging after the **Auto** value under the **AeDebug** key has been set to 1.</span></span>

<span data-ttu-id="d5635-131">**Pour exclure une application du débogage automatique**</span><span class="sxs-lookup"><span data-stu-id="d5635-131">**To exclude an application from automatic debugging**</span></span>

1.  <span data-ttu-id="d5635-132">Accédez à la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="d5635-132">Go to the following registry key:</span></span>

    <span data-ttu-id="d5635-133">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**</span><span class="sxs-lookup"><span data-stu-id="d5635-133">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**AeDebug**</span></span>

2.  <span data-ttu-id="d5635-134">Ajoutez une \_ valeur reg DWORD à la sous-clé **AutoExclusionList** , où le nom est le nom du fichier exécutable et la valeur est 1.</span><span class="sxs-lookup"><span data-stu-id="d5635-134">Add a REG\_DWORD value to the **AutoExclusionList** subkey, where the name is the name of the executable file and the value is 1.</span></span> <span data-ttu-id="d5635-135">Par défaut, le Gestionnaire de fenêtrage (Dwm.exe) est exclu du débogage automatique, sinon un blocage du système peut se produire si Dwm.exe cesse de répondre (l’utilisateur ne peut pas voir l’interface affichée par le débogueur, car Dwm.exe ne répond pas, et Dwm.exe ne peut pas se terminer parce qu’il est détenu par le débogueur).</span><span class="sxs-lookup"><span data-stu-id="d5635-135">By default, the Desktop Window Manager (Dwm.exe) is excluded from automatic debugging because otherwise a system deadlock can occur if Dwm.exe stops responding (the user cannot see the interface displayed by the debugger because Dwm.exe isn't responding, and Dwm.exe cannot terminate because it is held by the debugger).</span></span>

    <span data-ttu-id="d5635-136">**Windows Server 2003 et Windows XP :** La sous-clé **AutoExclusionList** n’est pas disponible. vous ne pouvez donc pas exclure une application, y compris Dwm.exe, du débogage automatique.</span><span class="sxs-lookup"><span data-stu-id="d5635-136">**Windows Server 2003 and Windows XP:** The **AutoExclusionList** subkey is not available; thus you cannot exclude any application, including Dwm.exe, from automatic debugging.</span></span>

<span data-ttu-id="d5635-137">Les entrées de Registre **AeDebug** par défaut peuvent être représentées comme suit :</span><span class="sxs-lookup"><span data-stu-id="d5635-137">The default **AeDebug** registry entries can be represented as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               AeDebug
                  Auto = 1
                  AutoExclusionList
                     DWM.exe = 1
```

## <a name="related-topics"></a><span data-ttu-id="d5635-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5635-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5635-139">Activation du débogage post-mortem avec WinDbg</span><span class="sxs-lookup"><span data-stu-id="d5635-139">Enabling Postmortem Debugging with WinDbg</span></span>](/windows-hardware/drivers/debugger/enabling-postmortem-debugging)
</dt> </dl>

 

 
