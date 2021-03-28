---
description: Les applications, les processus et les fenêtres peuvent choisir de ne pas être disponibles pour épingler à la barre des tâches ou d’être incluses dans la liste la plus fréquemment utilisée (MFU) du menu Démarrer.
title: Comment exclure des éléments de l’épinglage de la barre des tâches et des listes récentes/fréquentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7f32ad641832703804f94b8cc28f47ea9cabb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973154"
---
# <a name="how-to-exclude-items-from-taskbar-pinning-and-recentfrequent-lists"></a><span data-ttu-id="881e4-103">Comment exclure des éléments de l’épinglage de la barre des tâches et des listes récentes/fréquentes</span><span class="sxs-lookup"><span data-stu-id="881e4-103">How to Exclude Items from Taskbar Pinning and Recent/Frequent Lists</span></span>

<span data-ttu-id="881e4-104">Les applications, les processus et les fenêtres peuvent choisir de ne pas être disponibles pour épingler à la barre des tâches ou d’être incluses dans la liste la plus fréquemment utilisée (MFU) du menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="881e4-104">Applications, processes, and windows can opt to make themselves unavailable for pinning to the taskbar or for inclusion in the **Start** menu's Most Frequently Used (MFU) list.</span></span>

## <a name="instructions"></a><span data-ttu-id="881e4-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="881e4-105">Instructions</span></span>


<span data-ttu-id="881e4-106">Il existe trois mécanismes pour accomplir l’exclusion des éléments de l’épinglage de la barre des tâches et des listes récentes/fréquentes :</span><span class="sxs-lookup"><span data-stu-id="881e4-106">There are three mechanisms to accomplish the exclusion of items from taskbar pinning and recent/frequent lists:</span></span>

-   <span data-ttu-id="881e4-107">Ajoutez l’entrée NoStartPage à l’inscription de l’application, comme illustré dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="881e4-107">Add the NoStartPage entry to the application's registration as shown in this example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    <span data-ttu-id="881e4-108">Les données associées à l’entrée NoStartPage sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="881e4-108">The data associated with the NoStartPage entry is ignored.</span></span> <span data-ttu-id="881e4-109">Seule la présence de l’entrée est requise.</span><span class="sxs-lookup"><span data-stu-id="881e4-109">Only the presence of the entry is required.</span></span> <span data-ttu-id="881e4-110">Par conséquent, le type idéal pour NoStartPage est **reg \_ None**.</span><span class="sxs-lookup"><span data-stu-id="881e4-110">Therefore, the ideal type for NoStartPage is **REG\_NONE**.</span></span>

    <span data-ttu-id="881e4-111">Notez que toute utilisation d’un ID de modèle utilisateur d’application explicite (AppUserModelID) remplace l’entrée NoStartPage.</span><span class="sxs-lookup"><span data-stu-id="881e4-111">Note that any use of an explicit Application User Model ID (AppUserModelID) overrides the NoStartPage entry.</span></span> <span data-ttu-id="881e4-112">Si un AppUserModelID explicite est appliqué à un raccourci, à un processus ou à une fenêtre, il devient regroupement et éligible pour la liste MFU du menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="881e4-112">If an explicit AppUserModelID is applied to a shortcut, process, or window, it becomes pinnable and eligible for the **Start** menu MFU list.</span></span>

-   <span data-ttu-id="881e4-113">Définissez la propriété [System. AppUserModel. PreventPinning](../properties/props-system-appusermodel-preventpinning.md) sur les fenêtres et les raccourcis.</span><span class="sxs-lookup"><span data-stu-id="881e4-113">Set the [System.AppUserModel.PreventPinning](../properties/props-system-appusermodel-preventpinning.md) property on windows and shortcuts.</span></span> <span data-ttu-id="881e4-114">Cette propriété doit être définie sur une fenêtre avant que la propriété AppUserModel de la valeur de la propriété de l’ID du groupe de [ \_ \_ sécurité](../properties/props-system-appusermodel-id.md) .</span><span class="sxs-lookup"><span data-stu-id="881e4-114">This property must be set on a window before the [PKEY\_AppUserModel\_ID](../properties/props-system-appusermodel-id.md) property is set.</span></span>
-   <span data-ttu-id="881e4-115">Ajoutez une valeur AppUserModelID explicite sous la forme d’une valeur sous la sous-clé de Registre suivante, comme indiqué dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="881e4-115">Add an explicit AppUserModelID as a value under the following registry subkey as shown in this example:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      FileAssociation
                         NoStartPageAppUserModelIDs
                            AppUserModelID1
                            AppUserModelID2
                            AppUserModelID3
    ```

    <span data-ttu-id="881e4-116">Chaque entrée est une valeur **reg \_ null** avec le nom de AppUserModelID.</span><span class="sxs-lookup"><span data-stu-id="881e4-116">Each entry is a **REG\_NULL** value with the name of the AppUserModelID.</span></span> <span data-ttu-id="881e4-117">Toute AppUserModelID trouvée dans cette liste n’est pas regroupement et n’est pas éligible pour l’inclusion dans la liste des listes les plus fréquemment dans le menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="881e4-117">Any AppUserModelID that is found in this list is not pinnable and not eligible for inclusion in the **Start** menu MFU list.</span></span>

## <a name="remarks"></a><span data-ttu-id="881e4-118">Notes</span><span class="sxs-lookup"><span data-stu-id="881e4-118">Remarks</span></span>

<span data-ttu-id="881e4-119">N’oubliez pas que certains fichiers exécutables, ainsi que les raccourcis contenant certaines chaînes dans leurs noms, sont automatiquement exclus de l’épinglage et de l’inclusion dans la liste des MFU.</span><span class="sxs-lookup"><span data-stu-id="881e4-119">Be aware that certain executable files, as well as shortcuts that contain certain strings in their names, are automatically excluded from pinning and inclusion in the MFU list.</span></span>

> [!Note]  
> <span data-ttu-id="881e4-120">Cette exclusion automatique peut être remplacée en appliquant une AppUserModelID explicite.</span><span class="sxs-lookup"><span data-stu-id="881e4-120">This automatic exclusion can be overridden by applying an explicit AppUserModelID.</span></span>

 

<span data-ttu-id="881e4-121">Si l’une des chaînes suivantes, quelle que soit la casse, est incluse dans le nom du raccourci, le programme n’est pas regroupement et ne s’affiche pas dans la liste des plus fréquemment utilisés (non applicable à Windows 10) :</span><span class="sxs-lookup"><span data-stu-id="881e4-121">If any of the following strings, regardless of case, are included in the shortcut name, the program is not pinnable and is not displayed in the most frequently used list (not applicable to Windows 10):</span></span>

-   <span data-ttu-id="881e4-122">Documentation</span><span class="sxs-lookup"><span data-stu-id="881e4-122">Documentation</span></span>
-   <span data-ttu-id="881e4-123">Aide</span><span class="sxs-lookup"><span data-stu-id="881e4-123">Help</span></span>
-   <span data-ttu-id="881e4-124">Installer</span><span class="sxs-lookup"><span data-stu-id="881e4-124">Install</span></span>
-   <span data-ttu-id="881e4-125">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="881e4-125">More Info</span></span>
-   <span data-ttu-id="881e4-126">Lisez-moi</span><span class="sxs-lookup"><span data-stu-id="881e4-126">Read me</span></span>
-   <span data-ttu-id="881e4-127">Lire en premier</span><span class="sxs-lookup"><span data-stu-id="881e4-127">Read First</span></span>
-   <span data-ttu-id="881e4-128">Fichier Lisezmoi</span><span class="sxs-lookup"><span data-stu-id="881e4-128">Readme</span></span>
-   <span data-ttu-id="881e4-129">Supprimer</span><span class="sxs-lookup"><span data-stu-id="881e4-129">Remove</span></span>
-   <span data-ttu-id="881e4-130">Programme d’installation</span><span class="sxs-lookup"><span data-stu-id="881e4-130">Setup</span></span>
-   <span data-ttu-id="881e4-131">Support</span><span class="sxs-lookup"><span data-stu-id="881e4-131">Support</span></span>
-   <span data-ttu-id="881e4-132">What's New</span><span class="sxs-lookup"><span data-stu-id="881e4-132">What's New</span></span>

<span data-ttu-id="881e4-133">La liste de programmes suivante n’est pas regroupement et est exclue de la liste des plus fréquemment utilisées :</span><span class="sxs-lookup"><span data-stu-id="881e4-133">The following list of programs are not pinnable and are excluded from the most frequently used list:</span></span>

-   <span data-ttu-id="881e4-134">Applaunch.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-134">Applaunch.exe</span></span>
-   <span data-ttu-id="881e4-135">Control.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-135">Control.exe</span></span>
-   <span data-ttu-id="881e4-136">Dfsvc.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-136">Dfsvc.exe</span></span>
-   <span data-ttu-id="881e4-137">Dllhost.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-137">Dllhost.exe</span></span>
-   <span data-ttu-id="881e4-138">Guestmodemsg.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-138">Guestmodemsg.exe</span></span>
-   <span data-ttu-id="881e4-139">Hh.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-139">Hh.exe</span></span>
-   <span data-ttu-id="881e4-140">Install.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-140">Install.exe</span></span>
-   <span data-ttu-id="881e4-141">Isuninst.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-141">Isuninst.exe</span></span>
-   <span data-ttu-id="881e4-142">Lnkstub.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-142">Lnkstub.exe</span></span>
-   <span data-ttu-id="881e4-143">Mmc.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-143">Mmc.exe</span></span>
-   <span data-ttu-id="881e4-144">Mshta.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-144">Mshta.exe</span></span>
-   <span data-ttu-id="881e4-145">Msiexec.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-145">Msiexec.exe</span></span>
-   <span data-ttu-id="881e4-146">Msoobe.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-146">Msoobe.exe</span></span>
-   <span data-ttu-id="881e4-147">Rundll32.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-147">Rundll32.exe</span></span>
-   <span data-ttu-id="881e4-148">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-148">Setup.exe</span></span>
-   <span data-ttu-id="881e4-149">St5unst.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-149">St5unst.exe</span></span>
-   <span data-ttu-id="881e4-150">Unwise.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-150">Unwise.exe</span></span>
-   <span data-ttu-id="881e4-151">Unwise32.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-151">Unwise32.exe</span></span>
-   <span data-ttu-id="881e4-152">Werfault.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-152">Werfault.exe</span></span>
-   <span data-ttu-id="881e4-153">Winhlp32.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-153">Winhlp32.exe</span></span>
-   <span data-ttu-id="881e4-154">Wlrmdr.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-154">Wlrmdr.exe</span></span>
-   <span data-ttu-id="881e4-155">Wuapp.exe</span><span class="sxs-lookup"><span data-stu-id="881e4-155">Wuapp.exe</span></span>

<span data-ttu-id="881e4-156">Les listes précédentes sont stockées dans les valeurs de Registre suivantes.</span><span class="sxs-lookup"><span data-stu-id="881e4-156">The preceding lists are stored in the following registry values.</span></span>

> [!Note]  
> <span data-ttu-id="881e4-157">Ces listes ne doivent pas être modifiées par les applications.</span><span class="sxs-lookup"><span data-stu-id="881e4-157">These lists should not be modified by applications.</span></span> <span data-ttu-id="881e4-158">Utilisez l’une des méthodes de liste d’exclusion décrites précédemment dans cette rubrique pour la même expérience.</span><span class="sxs-lookup"><span data-stu-id="881e4-158">Use one of the exclusion list methods described earlier in this topic for the same experience.</span></span>

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FileAssociation
                     AddRemoveApps
                     HostApps
```

## <a name="related-topics"></a><span data-ttu-id="881e4-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="881e4-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="881e4-160">La barre des tâches</span><span class="sxs-lookup"><span data-stu-id="881e4-160">The Taskbar</span></span>](taskbar.md)
</dt> <dt>

[<span data-ttu-id="881e4-161">Extensions de la barre des tâches</span><span class="sxs-lookup"><span data-stu-id="881e4-161">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 
