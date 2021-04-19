---
description: Les actions personnalisées peuvent ajouter des informations de temps et de progression à un contrôle ProgressBar. Pour plus d’informations sur la création d’une boîte de dialogue d’affichage des actions avec un ProgressBar, consultez Création d’un contrôle ProgressBar.
ms.assetid: 101e6b59-3791-450c-9dc6-8930bd665a93
title: Ajout d’actions personnalisées au ProgressBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff2b6da9e72a37329b26cfce7590bab5f9792db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531908"
---
# <a name="adding-custom-actions-to-the-progressbar"></a><span data-ttu-id="0df65-104">Ajout d’actions personnalisées au ProgressBar</span><span class="sxs-lookup"><span data-stu-id="0df65-104">Adding Custom Actions to the ProgressBar</span></span>

<span data-ttu-id="0df65-105">Les [actions personnalisées](custom-actions.md) peuvent ajouter des informations de temps et de progression à un contrôle [ProgressBar](progressbar-control.md) .</span><span class="sxs-lookup"><span data-stu-id="0df65-105">[Custom Actions](custom-actions.md) can add time and progress information to a [ProgressBar](progressbar-control.md) control.</span></span> <span data-ttu-id="0df65-106">Pour plus d’informations sur la création d’une boîte de dialogue d’affichage des actions avec un ProgressBar, consultez [création d’un contrôle ProgressBar](authoring-a-progressbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="0df65-106">For more information about creating an action display dialog box having a ProgressBar, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md).</span></span>

<span data-ttu-id="0df65-107">Notez que deux actions personnalisées doivent être ajoutées au package Windows Installer pour signaler avec précision le temps et les informations de progression dans le ProgressBar.</span><span class="sxs-lookup"><span data-stu-id="0df65-107">Note that two custom actions must be added to the Windows Installer package to accurately report time and progress information to the ProgressBar.</span></span> <span data-ttu-id="0df65-108">Une action personnalisée doit être une action personnalisée différée.</span><span class="sxs-lookup"><span data-stu-id="0df65-108">One custom action must be a deferred custom action.</span></span> <span data-ttu-id="0df65-109">Cette action personnalisée doit terminer votre installation personnalisée et envoyer les quantités d’incréments individuels au contrôle [ProgressBar](progressbar-control.md) quand le programme d’installation exécute le script d’installation.</span><span class="sxs-lookup"><span data-stu-id="0df65-109">This custom action should complete your custom installation and send the amounts of individual increments to the [ProgressBar](progressbar-control.md) control when the installer runs the installation script.</span></span> <span data-ttu-id="0df65-110">La deuxième action personnalisée doit être une action personnalisée d’exécution immédiate qui informe le ProgressBar du nombre de graduations à ajouter au nombre total lors de la phase d’acquisition et de génération de script de l’installation.</span><span class="sxs-lookup"><span data-stu-id="0df65-110">The second custom action must be an immediate execution custom action that informs the ProgressBar how many ticks to add to the total count during the acquisition and script generation phase of the installation.</span></span>

<span data-ttu-id="0df65-111">**Pour ajouter une action personnalisée au ProgressBar**</span><span class="sxs-lookup"><span data-stu-id="0df65-111">**To add a custom action to the ProgressBar**</span></span>

1.  <span data-ttu-id="0df65-112">Décidez comment l’action personnalisée décrira sa progression.</span><span class="sxs-lookup"><span data-stu-id="0df65-112">Decide how the custom action will describe its progress.</span></span> <span data-ttu-id="0df65-113">Par exemple, une action personnalisée qui installe des clés de Registre peut afficher un message de progression et mettre à jour le [ProgressBar](progressbar-control.md) chaque fois que le programme d’installation écrit une clé de registre.</span><span class="sxs-lookup"><span data-stu-id="0df65-113">For example, a custom action that installs registry keys could display a progress message and update the [ProgressBar](progressbar-control.md) each time the installer writes one registry key.</span></span>
2.  <span data-ttu-id="0df65-114">Chaque mise à jour effectuée par l’action personnalisée modifie la longueur du [ProgressBar](progressbar-control.md) à l’aide d’un incrément de constante.</span><span class="sxs-lookup"><span data-stu-id="0df65-114">Each update by the custom action changes the length of the [ProgressBar](progressbar-control.md) by a constant increment.</span></span> <span data-ttu-id="0df65-115">Spécifiez ou calculez le nombre de graduations dans chaque incrément.</span><span class="sxs-lookup"><span data-stu-id="0df65-115">Specify or calculate the number of ticks in each increment.</span></span> <span data-ttu-id="0df65-116">En général, une modification de la longueur du ProgressBar d’un battement correspond à l’installation d’un octet.</span><span class="sxs-lookup"><span data-stu-id="0df65-116">Typically a change in ProgressBar length of one tick corresponds to the installation of one byte.</span></span> <span data-ttu-id="0df65-117">Par exemple, si le programme d’installation installe environ 10000 octets lorsqu’il écrit une clé de Registre, vous pouvez spécifier qu’il y a 10000 graduations dans un intervalle.</span><span class="sxs-lookup"><span data-stu-id="0df65-117">For example, if the installer installs approximately 10000 bytes when it writes one registry key, you can specify that there are 10000 ticks in an increment.</span></span>
3.  <span data-ttu-id="0df65-118">Spécifiez ou calculez le nombre total de graduations que l’action personnalisée ajoute à la longueur du [ProgressBar](progressbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="0df65-118">Specify or calculate the total number of ticks the custom action adds to the length of the [ProgressBar](progressbar-control.md).</span></span> <span data-ttu-id="0df65-119">Le nombre de graduations ajoutées par l’action personnalisée est généralement calculé comme suit : (incrément de graduation) x (nombre d’éléments).</span><span class="sxs-lookup"><span data-stu-id="0df65-119">The number of ticks added by the custom action is usually calculated as: (tick increment) x (number of items).</span></span> <span data-ttu-id="0df65-120">Par exemple, si l’action personnalisée écrit 10 clés de Registre, le programme d’installation installe environ 100000 octets et le programme d’installation doit donc augmenter l’estimation de la longueur totale finale du ProgressBar de 100000 cycles.</span><span class="sxs-lookup"><span data-stu-id="0df65-120">For example, if the custom action writes 10 registry keys, the installer installs approximately 100000 bytes and the installer therefore must increase the estimate of the final total length of the ProgressBar by 100000 ticks.</span></span>
    > [!Note]  
    > <span data-ttu-id="0df65-121">Pour calculer cette valeur dynamiquement, l’action personnalisée doit contenir une section qui est immédiatement exécutée pendant la génération du script.</span><span class="sxs-lookup"><span data-stu-id="0df65-121">To calculate this dynamically, the custom action must contain a section that is immediately executed during script generation.</span></span> <span data-ttu-id="0df65-122">La quantité de cycles signalée par votre action personnalisée d’exécution différée doit être égale au nombre de graduations ajoutées au nombre total de cycles par l’action d’exécution immédiate.</span><span class="sxs-lookup"><span data-stu-id="0df65-122">The amount of ticks reported by your deferred execution custom action must be equal to the number of ticks added to the total tick count by the immediate execution action.</span></span> <span data-ttu-id="0df65-123">Si ce n’est pas le cas, le temps restant indiqué par le contrôle de texte TimeRemaining sera inexact.</span><span class="sxs-lookup"><span data-stu-id="0df65-123">If this is not the case, the time remaining as reported by the TimeRemaining text control will be inaccurate.</span></span>

     

4.  <span data-ttu-id="0df65-124">Séparez votre action personnalisée en deux sections de code : une section qui s’exécute pendant la phase de génération de script et une section qui s’exécute pendant la phase d’exécution de l’installation.</span><span class="sxs-lookup"><span data-stu-id="0df65-124">Separate your custom action into two sections of code: a section that runs during the script generation phase and a section that runs during the execution phase of the installation.</span></span> <span data-ttu-id="0df65-125">Pour ce faire, vous pouvez utiliser deux fichiers ou un fichier par conditionnement sur le mode d’exécution du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="0df65-125">You can do this using two files or you can use one file by conditioning on the run mode of the installer.</span></span> <span data-ttu-id="0df65-126">L’exemple suivant utilise un fichier et vérifie l’état de l’installation.</span><span class="sxs-lookup"><span data-stu-id="0df65-126">The following sample uses one file and checks the installation state.</span></span> <span data-ttu-id="0df65-127">Les sections de l’exemple sont conditionnées pour s’exécuter selon que le programme d’installation est dans la phase d’exécution ou de génération de script de l’installation.</span><span class="sxs-lookup"><span data-stu-id="0df65-127">Sections of the sample are conditioned to run depending on whether the installer is in the execution or script generation phase of the installation.</span></span>
5.  <span data-ttu-id="0df65-128">La section qui s’exécute pendant la génération du script doit augmenter l’estimation de la longueur totale finale du [ProgressBar](progressbar-control.md) par le nombre total de graduations de l’action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="0df65-128">The section that runs during script generation should increase the estimate of the final total length of the [ProgressBar](progressbar-control.md) by the total number of ticks in the custom action.</span></span> <span data-ttu-id="0df65-129">Pour ce faire, envoyez un message de progression **ProgressAddition** .</span><span class="sxs-lookup"><span data-stu-id="0df65-129">This is done by sending a **ProgressAddition** progress message.</span></span>
6.  <span data-ttu-id="0df65-130">La section qui s’exécute pendant la phase d’exécution de l’installation doit configurer le texte et les modèles de message pour informer l’utilisateur de ce que fait l’action personnalisée et pour indiquer au programme d’installation de mettre à jour le contrôle [ProgressBar](progressbar-control.md) .</span><span class="sxs-lookup"><span data-stu-id="0df65-130">The section that runs during the execution phase of installation should set up message text and templates to inform the user about what the custom action is doing and to direct the installer on updating the [ProgressBar](progressbar-control.md) control.</span></span> <span data-ttu-id="0df65-131">Par exemple, informez le programme d’installation de déplacer le ProgressBar d’un incrément vers le bas et d’envoyer un message de progression explicite avec chaque mise à jour.</span><span class="sxs-lookup"><span data-stu-id="0df65-131">For example, inform the installer to move the ProgressBar forward one increment and send an explicit progress message with each update.</span></span> <span data-ttu-id="0df65-132">Il y a généralement une boucle dans cette section si l’action personnalisée installe un.</span><span class="sxs-lookup"><span data-stu-id="0df65-132">There is usually a loop in this section if the custom action is installing something.</span></span> <span data-ttu-id="0df65-133">À chaque étape de cette boucle, le programme d’installation peut installer un élément de référence tel qu’une clé de Registre et mettre à jour le contrôle ProgressBar</span><span class="sxs-lookup"><span data-stu-id="0df65-133">With each pass through this loop, the installer can install one reference item such as a registry key and update the ProgressBar control</span></span>
7.  <span data-ttu-id="0df65-134">Ajoutez une action personnalisée d’exécution immédiate à votre package Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="0df65-134">Add an immediate execution custom action to your Windows Installer package.</span></span> <span data-ttu-id="0df65-135">Cette action personnalisée indique à [ProgressBar](progressbar-control.md) le montant à avancer pendant les phases d’acquisition et de génération de script de l’installation.</span><span class="sxs-lookup"><span data-stu-id="0df65-135">This custom action informs the [ProgressBar](progressbar-control.md) how much to advance during the aquisition and script generation phases of the installation.</span></span> <span data-ttu-id="0df65-136">Pour l’exemple suivant, la source est la DLL créée en compilant l’exemple de code et la cible est le point d’entrée, caprogress.</span><span class="sxs-lookup"><span data-stu-id="0df65-136">For the following sample, the source is the DLL created by compiling the sample code and the target is the entry point, CAProgress.</span></span>
8.  <span data-ttu-id="0df65-137">Ajoutez une action personnalisée d’exécution différée à votre package Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="0df65-137">Add a deferred execution custom action to your Windows Installer package.</span></span> <span data-ttu-id="0df65-138">Cette action personnalisée termine les étapes de l’installation proprement dite et informe le [ProgressBar](progressbar-control.md) de l’avancement de la barre au moment où le programme d’installation exécute le script d’installation.</span><span class="sxs-lookup"><span data-stu-id="0df65-138">This custom action completes the steps of the actual installation and informs the [ProgressBar](progressbar-control.md) how much to advance the bar at the time when the installer runs the installation script.</span></span> <span data-ttu-id="0df65-139">Pour l’exemple suivant, la source est la DLL créée en compilant l’exemple de code et la cible est le point d’entrée, caprogress.</span><span class="sxs-lookup"><span data-stu-id="0df65-139">For the following sample, the source is the DLL created by compiling the sample code and the target is the entry point, CAProgress.</span></span>
9.  <span data-ttu-id="0df65-140">Planifiez les actions personnalisées entre [InstallInitialize](installinitialize-action.md) et [InstallFinalize](installfinalize-action.md) dans la table [InstallExecuteSequence](installexecutesequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="0df65-140">Schedule both custom actions between [InstallInitialize](installinitialize-action.md) and [InstallFinalize](installfinalize-action.md) in the [InstallExecuteSequence](installexecutesequence-table.md) table.</span></span> <span data-ttu-id="0df65-141">L’action personnalisée différée doit être planifiée immédiatement après l’action personnalisée d’exécution immédiate.</span><span class="sxs-lookup"><span data-stu-id="0df65-141">The deferred custom action should be scheduled immediately after the immediate execution custom action.</span></span> <span data-ttu-id="0df65-142">Le programme d’installation n’exécutera pas l’action personnalisée différée tant que le script n’est pas exécuté.</span><span class="sxs-lookup"><span data-stu-id="0df65-142">The installer will not run the deferred custom action until the script is executed.</span></span>

<span data-ttu-id="0df65-143">L’exemple suivant montre comment une action personnalisée peut être ajoutée au [ProgressBar](progressbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="0df65-143">The following sample shows how a custom action can be added to the [ProgressBar](progressbar-control.md).</span></span> <span data-ttu-id="0df65-144">La source des deux actions personnalisées est la DLL créée en compilant l’exemple de code et la cible des deux actions personnalisées est le point d’entrée, caprogress.</span><span class="sxs-lookup"><span data-stu-id="0df65-144">The source of both custom actions is the DLL created by compiling the sample code and the target of both custom actions is the entry point, CAProgress.</span></span> <span data-ttu-id="0df65-145">Cet exemple n’apporte aucune modification réelle au système, mais utilise le ProgressBar comme si vous installiez 10 éléments de référence dont la taille est d’environ 10 000 octets.</span><span class="sxs-lookup"><span data-stu-id="0df65-145">This sample does not make any actual changes to the system, but operates the ProgressBar as if installing 10 reference items that are each approximately 10,000 bytes in size.</span></span> <span data-ttu-id="0df65-146">Le programme d’installation met à jour le message et le ProgressBar chaque fois qu’il installe un élément de référence.</span><span class="sxs-lookup"><span data-stu-id="0df65-146">The installer updates the message and ProgressBar each time it installs a reference item.</span></span>


```C++
#include <windows.h>
#include <msiquery.h>
#pragma comment(lib, "msi.lib")

// Specify or calculate the number of ticks in an increment
// to the ProgressBar
const UINT iTickIncrement = 10000;
 
// Specify or calculate the total number of ticks the custom 
// action adds to the length of the ProgressBar
const UINT iNumberItems = 10;
const UINT iTotalTicks = iTickIncrement * iNumberItems;
 
UINT __stdcall CAProgress(MSIHANDLE hInstall)
{
    // Tell the installer to check the installation state and execute
    // the code needed during the rollback, acquisition, or
    // execution phases of the installation.
  
    if (MsiGetMode(hInstall,MSIRUNMODE_SCHEDULED) == TRUE)
    {
        PMSIHANDLE hActionRec = MsiCreateRecord(3);
        PMSIHANDLE hProgressRec = MsiCreateRecord(3);

        // Installer is executing the installation script. Set up a
        // record specifying appropriate templates and text for
        // messages that will inform the user about what the custom
        // action is doing. Tell the installer to use this template and 
        // text in progress messages.
 
        MsiRecordSetString(hActionRec, 1, TEXT("MyCustomAction"));
        MsiRecordSetString(hActionRec, 2, TEXT("Incrementing the Progress Bar..."));
        MsiRecordSetString(hActionRec, 3, TEXT("Incrementing tick [1] of [2]"));
        UINT iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_ACTIONSTART, hActionRec);
        if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;
              
        // Tell the installer to use explicit progress messages.
        MsiRecordSetInteger(hProgressRec, 1, 1);
        MsiRecordSetInteger(hProgressRec, 2, 1);
        MsiRecordSetInteger(hProgressRec, 3, 0);
        iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
        if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;
              
        //Specify that an update of the progress bar's position in
        //this case means to move it forward by one increment.
        MsiRecordSetInteger(hProgressRec, 1, 2);
        MsiRecordSetInteger(hProgressRec, 2, iTickIncrement);
        MsiRecordSetInteger(hProgressRec, 3, 0);
 
        // The following loop sets up the record needed by the action
        // messages and tells the installer to send a message to update
        // the progress bar.

        MsiRecordSetInteger(hActionRec, 2, iTotalTicks);
       
        for( int i = 0; i < iTotalTicks; i+=iTickIncrement)
        {
            MsiRecordSetInteger(hActionRec, 1, i);

            iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_ACTIONDATA, hActionRec);
            if ((iResult == IDCANCEL))
                return ERROR_INSTALL_USEREXIT;
          
            iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
            if ((iResult == IDCANCEL))
                return ERROR_INSTALL_USEREXIT;
   
            //A real custom action would have code here that does a part
            //of the installation. For this sample, code that installs
            //10 registry keys.
            Sleep(1000);
                    
        }
        return ERROR_SUCCESS;
    }
    else
    {
        // Installer is generating the installation script of the
        // custom action.
  
        // Tell the installer to increase the value of the final total
        // length of the progress bar by the total number of ticks in
        // the custom action.
        PMSIHANDLE hProgressRec = MsiCreateRecord(2);

         MsiRecordSetInteger(hProgressRec, 1, 3);
            MsiRecordSetInteger(hProgressRec, 2, iTotalTicks);
        UINT iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
           if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;     
        return ERROR_SUCCESS;
     }
}
```



 

 



