---
description: Spécifiez une icône et une étiquette personnalisées pour un lecteur.
ms.assetid: B6EF7F84-7747-4689-B740-A91CA8E394D7
title: Affecter une icône et une étiquette personnalisées à une lettre de lecteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848c076db443c502a667d67e0b7b49ce51db4ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973187"
---
# <a name="how-to-assign-a-custom-icon-and-label-to-a-drive-letter"></a><span data-ttu-id="4b20a-103">Comment attribuer une icône et une étiquette personnalisées à une lettre de lecteur</span><span class="sxs-lookup"><span data-stu-id="4b20a-103">How to Assign a Custom Icon and Label to a Drive Letter</span></span>

<span data-ttu-id="4b20a-104">Spécifiez une icône et une étiquette personnalisées pour un lecteur.</span><span class="sxs-lookup"><span data-stu-id="4b20a-104">Specify a custom icon and label for a drive.</span></span>

## <a name="instructions"></a><span data-ttu-id="4b20a-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="4b20a-105">Instructions</span></span>

### <a name="step-1-replacing-the-standard-drive-icon-with-a-custom-icon-in-windows-2000"></a><span data-ttu-id="4b20a-106">Étape 1 : remplacement de l’icône de lecteur standard par une icône personnalisée dans Windows 2000</span><span class="sxs-lookup"><span data-stu-id="4b20a-106">Step 1: Replacing the standard drive icon with a custom icon in Windows 2000</span></span>

<span data-ttu-id="4b20a-107">Pour remplacer l’icône de lecteur standard par une icône personnalisée dans Windows 2000, ajoutez une sous-clé nommée pour la lettre de lecteur à la clé suivante.</span><span class="sxs-lookup"><span data-stu-id="4b20a-107">To replace the standard drive icon with a custom icon in Windows 2000, add a subkey named for the drive letter to the following key.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
```

<span data-ttu-id="4b20a-108">L’exemple suivant spécifie une icône et une étiquette personnalisées pour le lecteur E :.</span><span class="sxs-lookup"><span data-stu-id="4b20a-108">The following example specifies a custom icon and label for the E: drive.</span></span> <span data-ttu-id="4b20a-109">L’icône se trouve dans le fichier C : \\ MyDir \\MyDrive.exe avec un index de base zéro de trois.</span><span class="sxs-lookup"><span data-stu-id="4b20a-109">The icon is in the C:\\MyDir\\MyDrive.exe file with a zero-based index of three.</span></span>

<span data-ttu-id="4b20a-110">Pour Windows 2000 :</span><span class="sxs-lookup"><span data-stu-id="4b20a-110">For Windows 2000:</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
            E
               DefaultIcon
                  (Default) = C:\MyDir\MyDrive.exe,3
               DefaultLabel
                  (Default) = MyDrive
```

### <a name="step-2-replacing-the-standard-drive-icon-with-a-custom-icon-in-all-other-versions-of-windows"></a><span data-ttu-id="4b20a-111">Étape 2 : remplacement de l’icône de lecteur standard par une icône personnalisée dans toutes les autres versions de Windows</span><span class="sxs-lookup"><span data-stu-id="4b20a-111">Step 2: Replacing the standard drive icon with a custom icon in all other versions of Windows</span></span>

<span data-ttu-id="4b20a-112">Pour remplacer l’icône de lecteur standard par une icône personnalisée dans toutes les versions de Windows autres que Windows 2000, ajoutez une sous-clé nommée pour la lettre de lecteur à la clé suivante.</span><span class="sxs-lookup"><span data-stu-id="4b20a-112">To replace the standard drive icon with a custom icon in all versions of Windows other than Windows 2000, add a subkey named for the drive letter to the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
```

<span data-ttu-id="4b20a-113">L’exemple suivant spécifie une icône et une étiquette personnalisées pour le lecteur E :.</span><span class="sxs-lookup"><span data-stu-id="4b20a-113">The following example specifies a custom icon and label for the E: drive.</span></span> <span data-ttu-id="4b20a-114">L’icône se trouve dans le fichier C : \\ MyDir \\MyDrive.exe avec un index de base zéro de trois.</span><span class="sxs-lookup"><span data-stu-id="4b20a-114">The icon is in the C:\\MyDir\\MyDrive.exe file with a zero-based index of three.</span></span>

<span data-ttu-id="4b20a-115">Pour toutes les autres versions de Windows :</span><span class="sxs-lookup"><span data-stu-id="4b20a-115">For all other versions of Windows:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
                     E
                        DefaultIcon
                           (Default) = C:\MyDir\MyDrive.exe,3
                        DefaultLabel
                           (Default) = MyDrive
```

### <a name="step-3-calling-the-shupdateimage-event"></a><span data-ttu-id="4b20a-116">Étape 3 : appel de l’événement SHUpdateImage</span><span class="sxs-lookup"><span data-stu-id="4b20a-116">Step 3: Calling the SHUpdateImage Event</span></span>

<span data-ttu-id="4b20a-117">Dans toutes les versions de Windows, si vous modifiez un type de fichier ou une icône de lecteur, vous devez également appeler SHUpdateImage pour notifier à l’interpréteur de mise à jour toutes les icônes qui sont actuellement affichées.</span><span class="sxs-lookup"><span data-stu-id="4b20a-117">In all versions of Windows, if you change a file type or drive icon you must also call SHUpdateImage to notify the Shell to update any icons that are currently displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b20a-118">Notes</span><span class="sxs-lookup"><span data-stu-id="4b20a-118">Remarks</span></span>

<span data-ttu-id="4b20a-119">La lettre de lecteur ne doit pas être suivie d’un signe deux-points ( :).</span><span class="sxs-lookup"><span data-stu-id="4b20a-119">The drive letter should not be followed by a colon (:).</span></span> <span data-ttu-id="4b20a-120">Ajoutez une sous-clé **DefaultIcon** à la sous-clé de lecteur et définissez sa valeur par défaut sur une chaîne qui contient l’emplacement de l’icône.</span><span class="sxs-lookup"><span data-stu-id="4b20a-120">Add a **DefaultIcon** subkey to the drive letter subkey and set its default value to a string that contains the location of the icon.</span></span> <span data-ttu-id="4b20a-121">La première partie de la chaîne contient le chemin d’accès complet du fichier de l’icône.</span><span class="sxs-lookup"><span data-stu-id="4b20a-121">The first part of the string contains the fully-qualified path of the icon's file.</span></span> <span data-ttu-id="4b20a-122">Si le fichier contient plusieurs icônes, le chemin d’accès est suivi d’une virgule, puis de l’index de base zéro de l’icône.</span><span class="sxs-lookup"><span data-stu-id="4b20a-122">If there is more than one icon in the file, the path is followed by a comma, and then by the zero-based index of the icon.</span></span>

 

 



