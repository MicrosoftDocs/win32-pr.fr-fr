---
title: Paramètres du registre de surveillance des dossiers
description: Paramètres du registre de surveillance des dossiers
ms.assetid: 563aeaec-0759-4b0c-a8e9-a9a2b3092515
keywords:
- Lecteur Windows Media, paramètres du registre de surveillance des dossiers
- Lecteur Windows Media, paramètres du registre de surveillance du dossier de fichiers
- Lecteur Windows Media, registre
- Registre, paramètres de surveillance des dossiers
- Registre, paramètres d’analyse des dossiers de fichiers
- Registre, paramètres pour le lecteur Windows Media
- paramètres du registre de surveillance des dossiers
- paramètres du registre de surveillance du dossier de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233076d1fc807dd5cdd79e9b4985ef752fba0815
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383088"
---
# <a name="folder-monitoring-registry-settings"></a><span data-ttu-id="771c1-111">Paramètres du registre de surveillance des dossiers</span><span class="sxs-lookup"><span data-stu-id="771c1-111">Folder Monitoring Registry Settings</span></span>

<span data-ttu-id="771c1-112">Le lecteur Windows Media série 9 ou une version ultérieure peut surveiller les dossiers de fichiers pour les nouveaux fichiers multimédias numériques.</span><span class="sxs-lookup"><span data-stu-id="771c1-112">Windows Media Player 9 Series or later can monitor file folders for new digital media files.</span></span> <span data-ttu-id="771c1-113">Lorsque le lecteur détecte un nouveau fichier dans un dossier surveillé, il ajoute automatiquement le fichier à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="771c1-113">When the Player detects a new file in a monitored folder, it automatically adds the file to the library.</span></span> <span data-ttu-id="771c1-114">Pour le lecteur Windows Media 9 jusqu’au lecteur Windows Media 11, les utilisateurs peuvent modifier la liste des dossiers surveillés en cliquant sur **surveiller les dossiers** sous l’onglet Bibliothèque de la boîte de dialogue **options** .</span><span class="sxs-lookup"><span data-stu-id="771c1-114">For Windows Media Player 9 through Windows Media Player 11, users can change the list of monitored folders by clicking **Monitor Folders** on the library tab of the **Options** dialog box.</span></span> <span data-ttu-id="771c1-115">Pour le lecteur Windows Media 12, un utilisateur peut modifier la liste des dossiers surveillés en suivant les instructions de la rubrique [Ajouter des éléments à la bibliothèque du lecteur Windows Media](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library).</span><span class="sxs-lookup"><span data-stu-id="771c1-115">For Windows Media Player 12, a user can change the list of monitored folders by following the instructions in the topic [Add items to the Windows Media Player Library](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library).</span></span> <span data-ttu-id="771c1-116">Pour le lecteur Windows Media 9 jusqu’au lecteur Windows Media 11, vous pouvez ajouter par programmation un dossier à analyser en ajoutant une valeur au registre.</span><span class="sxs-lookup"><span data-stu-id="771c1-116">For Windows Media Player 9 through Windows Media Player 11, you can programmatically add a folder to be monitored by adding a value to the registry.</span></span> <span data-ttu-id="771c1-117">Pour le lecteur Windows Media 12, vous ne pouvez pas utiliser le registre pour ajouter ou supprimer par programmation des dossiers à analyser.</span><span class="sxs-lookup"><span data-stu-id="771c1-117">For Windows Media Player 12, you cannot use the registry to programmatically add or remove folders to be monitored.</span></span>

<span data-ttu-id="771c1-118">Pour le lecteur Windows Media 9 jusqu’au lecteur Windows Media 11, pour ajouter un dossier à surveiller, vous devez d’abord créer ou modifier deux valeurs dans la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="771c1-118">For Windows Media Player 9 through Windows Media Player 11, to add a folder for monitoring you must first create or modify two values in the following registry key:</span></span>

<span data-ttu-id="771c1-119">**HKEY \_ \_ logiciel utilisateur \\ actuel \\ \\ Préférences Microsoft MediaPlayer \\\\**</span><span class="sxs-lookup"><span data-stu-id="771c1-119">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Preferences\\**</span></span>

<span data-ttu-id="771c1-120">Les nouvelles valeurs doivent être nommées comme suit.</span><span class="sxs-lookup"><span data-stu-id="771c1-120">The new values must be named as follows.</span></span>



| <span data-ttu-id="771c1-121">Nom</span><span class="sxs-lookup"><span data-stu-id="771c1-121">Name</span></span>                           | <span data-ttu-id="771c1-122">Type</span><span class="sxs-lookup"><span data-stu-id="771c1-122">Type</span></span>           | <span data-ttu-id="771c1-123">Description</span><span class="sxs-lookup"><span data-stu-id="771c1-123">Description</span></span>                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="771c1-124">**TrackFoldersDirectories**</span><span class="sxs-lookup"><span data-stu-id="771c1-124">**TrackFoldersDirectories**</span></span>    | <span data-ttu-id="771c1-125">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="771c1-125">**REG\_DWORD**</span></span> | <span data-ttu-id="771c1-126">Valeur **DWORD** qui représente le nombre de dossiers à surveiller.</span><span class="sxs-lookup"><span data-stu-id="771c1-126">A **DWORD** value that represents the count of folders to monitor.</span></span> <span data-ttu-id="771c1-127">Cela doit correspondre au nombre de valeurs \*\*TrackFoldersDirectories \*\* \* \* X.</span><span class="sxs-lookup"><span data-stu-id="771c1-127">This must match the count of \**TrackFoldersDirectories\*\*\*X* values.</span></span>                                                                                                                                         |
| <span data-ttu-id="771c1-128">\**TrackFoldersDirectories \* \* \* X*</span><span class="sxs-lookup"><span data-stu-id="771c1-128">\**TrackFoldersDirectories\*\*\*X*</span></span> | <span data-ttu-id="771c1-129">**SZ de REG \_**</span><span class="sxs-lookup"><span data-stu-id="771c1-129">**REG\_SZ**</span></span>    | <span data-ttu-id="771c1-130">Valeur de chaîne qui représente le chemin d’accès du dossier à surveiller.</span><span class="sxs-lookup"><span data-stu-id="771c1-130">A string value that represents the path of the folder to monitor.</span></span> <span data-ttu-id="771c1-131">Chaque dossier à surveiller requiert une valeur distincte.</span><span class="sxs-lookup"><span data-stu-id="771c1-131">Each folder to monitor requires a separate value.</span></span> <span data-ttu-id="771c1-132">Le suffixe *X* est un entier qui doit toujours commencer à 0, puis être incrémenté de 1.</span><span class="sxs-lookup"><span data-stu-id="771c1-132">The suffix *X* is an integer that should always begin at 0 and then increment by 1.</span></span> <span data-ttu-id="771c1-133">Le lecteur Windows Media surveille également les sous-dossiers du dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="771c1-133">Windows Media Player also monitors subfolders of the specified folder.</span></span> |



 

<span data-ttu-id="771c1-134">Par exemple, pour ajouter le premier dossier à surveiller, ajoutez la valeur suivante :</span><span class="sxs-lookup"><span data-stu-id="771c1-134">For example, to add the first folder to monitor, add the following value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories0" = "c:\MyPath\MyFolder"

```



<span data-ttu-id="771c1-135">Ensuite, créez la valeur de nombre :</span><span class="sxs-lookup"><span data-stu-id="771c1-135">Then, create the count value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000001

```



<span data-ttu-id="771c1-136">Pour ajouter un deuxième dossier à surveiller, ajoutez la valeur suivante :</span><span class="sxs-lookup"><span data-stu-id="771c1-136">To add a second folder to monitor, add the following value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories1" = "c:\MyPath\MyFolder2"

```



<span data-ttu-id="771c1-137">Incrémentez ensuite la valeur Count :</span><span class="sxs-lookup"><span data-stu-id="771c1-137">Then, increment the count value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000002

```



## <a name="related-topics"></a><span data-ttu-id="771c1-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="771c1-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="771c1-139">**Paramètres du Registre**</span><span class="sxs-lookup"><span data-stu-id="771c1-139">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




