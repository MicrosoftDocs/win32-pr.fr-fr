---
description: Dans Windows 7 et versions ultérieures, vous pouvez ajouter des verbes à un dossier à l’aide de Desktop.ini. Pour plus d’informations sur les fichiers de Desktop.ini, consultez Comment personnaliser des dossiers avec des Desktop.ini.
ms.assetid: F03AB35D-FBFE-46C2-A37F-F70C18219B9A
title: Comment implémenter des verbes personnalisés pour les dossiers via Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133726133abe884863a0b4d2abc0cc76aab1310a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973146"
---
# <a name="how-to-implement-custom-verbs-for-folders-through-desktopini"></a><span data-ttu-id="8f80e-104">Comment implémenter des verbes personnalisés pour les dossiers via Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="8f80e-104">How to Implement Custom Verbs for Folders through Desktop.ini</span></span>

<span data-ttu-id="8f80e-105">Dans Windows 7 et versions ultérieures, vous pouvez ajouter des verbes à un dossier à l’aide de Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="8f80e-105">In Windows 7 and later, you can add verbs to a folder by using Desktop.ini.</span></span> <span data-ttu-id="8f80e-106">Pour plus d’informations sur les fichiers de Desktop.ini, consultez [Comment personnaliser des dossiers avec des Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="8f80e-106">For more information about Desktop.ini files, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span>

> [!Note]  
> <span data-ttu-id="8f80e-107">Desktop.ini fichiers doivent toujours être marqués comme étant  +  **masqués** par le système afin qu’ils ne soient pas affichés aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8f80e-107">Desktop.ini files should always be marked **System** + **Hidden** so they won't be displayed to users.</span></span>

 

<span data-ttu-id="8f80e-108">Pour ajouter des verbes personnalisés pour les dossiers à l’aide d’un fichier Desktop.ini, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="8f80e-108">To add custom verbs for folders through a Desktop.ini file, perform the following steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="8f80e-109">Instructions</span><span class="sxs-lookup"><span data-stu-id="8f80e-109">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="8f80e-110">Étape 1 :</span><span class="sxs-lookup"><span data-stu-id="8f80e-110">Step 1:</span></span>

<span data-ttu-id="8f80e-111">Créez un dossier marqué **en lecture seule** ou **système**.</span><span class="sxs-lookup"><span data-stu-id="8f80e-111">Create a folder that is marked **Read-only** or **System**.</span></span>

### <a name="step-2"></a><span data-ttu-id="8f80e-112">Étape 2 :</span><span class="sxs-lookup"><span data-stu-id="8f80e-112">Step 2:</span></span>

<span data-ttu-id="8f80e-113">Créez un fichier de Desktop.ini qui comprend un \[ . ShellClassInfo \] DirectoryClass = ProgID du dossier.</span><span class="sxs-lookup"><span data-stu-id="8f80e-113">Create a Desktop.ini file that includes a \[.ShellClassInfo\] DirectoryClass=Folder ProgID.</span></span>

### <a name="step-3"></a><span data-ttu-id="8f80e-114">Étape 3 :</span><span class="sxs-lookup"><span data-stu-id="8f80e-114">Step 3:</span></span>

<span data-ttu-id="8f80e-115">Dans le registre, créez le dossier racine de l’identificateur de classe de la **\_ classe \_ HKEY** \\  avec la valeur CanUseForDirectory.</span><span class="sxs-lookup"><span data-stu-id="8f80e-115">In the registry, create **HKEY\_CLASSES\_ROOT**\\**Folder ProgID** with a value of CanUseForDirectory.</span></span> <span data-ttu-id="8f80e-116">La valeur CanUseForDirectory évite l’utilisation abusive des ProgID qui sont définis pour ne pas participer à l’implémentation de verbes personnalisés pour les dossiers par le biais de Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="8f80e-116">The CanUseForDirectory value avoids the misuse of ProgIDs that are set not to participate in implementing custom verbs for folders through Desktop.ini.</span></span>

### <a name="step-4"></a><span data-ttu-id="8f80e-117">Étape 4 :</span><span class="sxs-lookup"><span data-stu-id="8f80e-117">Step 4:</span></span>

<span data-ttu-id="8f80e-118">Ajoutez des verbes dans la sous-clé du **dossier** ProgID, par exemple :</span><span class="sxs-lookup"><span data-stu-id="8f80e-118">Add verbs under the **Folder** ProgID subkey, for example:</span></span>

```
HKEY_CLASSES_ROOT
   CustomFolderType
      Shell
         MyVerb
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
```

## <a name="remarks"></a><span data-ttu-id="8f80e-119">Notes</span><span class="sxs-lookup"><span data-stu-id="8f80e-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8f80e-120">Ces verbes peuvent être les verbes par défaut. dans ce cas, le double-clic sur le dossier active le verbe.</span><span class="sxs-lookup"><span data-stu-id="8f80e-120">These verbs can be the default verbs, in which case double-clicking the folder activates the verb.</span></span>

 

 

 



