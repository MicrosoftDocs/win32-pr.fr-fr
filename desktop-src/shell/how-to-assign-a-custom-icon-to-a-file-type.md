---
description: Une icône personnalisée doit être affectée à un type de fichier pour fournir une indication visuelle à l’utilisateur de ce type de fichier ou à l’application à laquelle ce type de fichier est associé.
ms.assetid: 84F293C2-BAB1-4BF8-9F89-122B6DAB29C3
title: Comment assigner une icône personnalisée à un type de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf625eb6177471702096f462846b8035772177ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973182"
---
# <a name="how-to-assign-a-custom-icon-to-a-file-type"></a><span data-ttu-id="99843-103">Comment assigner une icône personnalisée à un type de fichier</span><span class="sxs-lookup"><span data-stu-id="99843-103">How to Assign a Custom Icon to a File Type</span></span>

<span data-ttu-id="99843-104">Quand aucune icône par défaut personnalisée n’est assignée à un type de fichier, le bureau et l’Explorateur Windows affichent tous les fichiers de ce type avec une icône générique par défaut.</span><span class="sxs-lookup"><span data-stu-id="99843-104">When no custom default icon is assigned to a file type, the desktop and Windows Explorer display all files of that type with a generic default icon.</span></span> <span data-ttu-id="99843-105">Par exemple, la capture d’écran suivante montre cette icône par défaut utilisée avec le fichier MyDocs4. MYP.</span><span class="sxs-lookup"><span data-stu-id="99843-105">For example, the following screen shot shows this default icon used with the MyDocs4.myp file.</span></span>

![capture d’écran de l’icône par défaut](images/icon.png)

<span data-ttu-id="99843-107">Bien que tous les fichiers affichés dans cette capture d’écran soient des fichiers texte simples, seul MyDocs4. MYP affiche l’icône par défaut de Windows.</span><span class="sxs-lookup"><span data-stu-id="99843-107">While all the files displayed in this screen shot are simple text files, only MyDocs4.myp displays the Windows default icon.</span></span> <span data-ttu-id="99843-108">Cela est dû au fait que l’extension. txt est un type de fichier inscrit qui a une icône par défaut personnalisée.</span><span class="sxs-lookup"><span data-stu-id="99843-108">This is because the .txt extension is a registered file type that has a custom default icon.</span></span>

<span data-ttu-id="99843-109">La capture d’écran suivante montre une icône personnalisée qui a été affectée au type de fichier. MYP.</span><span class="sxs-lookup"><span data-stu-id="99843-109">The following screen shot shows a custom icon that has been assigned to the .myp file type.</span></span>

![capture d’écran de l’icône personnalisée pour les fichiers. MYP](images/context4.png)

> [!Note]  
> <span data-ttu-id="99843-111">Les icônes peuvent également être affectées sur la base d’une application spécifique.</span><span class="sxs-lookup"><span data-stu-id="99843-111">Icons can also be assigned on an application-specific basis.</span></span>

 

## <a name="instructions"></a><span data-ttu-id="99843-112">Instructions</span><span class="sxs-lookup"><span data-stu-id="99843-112">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="99843-113">Étape 1 :</span><span class="sxs-lookup"><span data-stu-id="99843-113">Step 1:</span></span>

<span data-ttu-id="99843-114">Créez une sous-clé nommée **DefaultIcon** dans l’un des deux emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="99843-114">Create a subkey named **DefaultIcon** in one of the following two locations:</span></span>

-   <span data-ttu-id="99843-115">Pour une assignation de type de fichier, **HKEY \_ classes \_ root** \\ *. extension*</span><span class="sxs-lookup"><span data-stu-id="99843-115">For a file-type assignment, **HKEY\_CLASSES\_ROOT**\\ *.extension*</span></span>
-   <span data-ttu-id="99843-116">Pour une assignation d’application **, \_ classe \_** de l’identificateur racine de la racine de HKEY \\ </span><span class="sxs-lookup"><span data-stu-id="99843-116">For an application assignment, **HKEY\_CLASSES\_ROOT**\\*ProgID*</span></span>

### <a name="step-2"></a><span data-ttu-id="99843-117">Étape 2 :</span><span class="sxs-lookup"><span data-stu-id="99843-117">Step 2:</span></span>

<span data-ttu-id="99843-118">Affectez à la sous-clé **DefaultIcon** une valeur par défaut de type **reg \_ SZ** qui spécifie le chemin d’accès complet au fichier qui contient l’icône.</span><span class="sxs-lookup"><span data-stu-id="99843-118">Assign the **DefaultIcon** subkey a default value of type **REG\_SZ** that specifies the fully qualified path for the file that contains the icon.</span></span>

### <a name="step-3"></a><span data-ttu-id="99843-119">Étape 3 :</span><span class="sxs-lookup"><span data-stu-id="99843-119">Step 3:</span></span>

<span data-ttu-id="99843-120">Appelez la fonction [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) pour notifier à l’interpréteur de mise à jour son cache d’icône.</span><span class="sxs-lookup"><span data-stu-id="99843-120">Call the [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) function to notify the Shell to update its icon cache.</span></span>

## <a name="remarks"></a><span data-ttu-id="99843-121">Notes</span><span class="sxs-lookup"><span data-stu-id="99843-121">Remarks</span></span>

<span data-ttu-id="99843-122">L’exemple suivant montre une vue détaillée des entrées de Registre requises pour l’affectation d’une icône de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="99843-122">The following example shows a detailed view of the registry entries that are required for a file-type icon assignment.</span></span> <span data-ttu-id="99843-123">L’extension de nom de fichier est associée à une application, mais l’affectation d’icône correspond à l’extension de nom de fichier proprement dite afin que l’application associée ne dicte pas l’icône par défaut.</span><span class="sxs-lookup"><span data-stu-id="99843-123">The file name extension is associated with an application, but the icon assignment is to the file name extension itself so that the associated application does not dictate the default icon.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

<span data-ttu-id="99843-124">L’exemple suivant montre une vue détaillée des entrées de Registre requises pour l’affectation d’une icône d’application.</span><span class="sxs-lookup"><span data-stu-id="99843-124">The following example shows a detailed view of the registry entries that are required for an application icon assignment.</span></span> <span data-ttu-id="99843-125">L’extension de nom de fichier. MYP est d’abord associée à l’application MyProgram. 1.</span><span class="sxs-lookup"><span data-stu-id="99843-125">The .myp file name extension is first associated with the MyProgram.1 application.</span></span> <span data-ttu-id="99843-126">La sous-clé ProgID MyProgram. 1 est ensuite affectée à l’icône par défaut personnalisée.</span><span class="sxs-lookup"><span data-stu-id="99843-126">The MyProgram.1 ProgID subkey is then assigned the custom default icon.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

<span data-ttu-id="99843-127">Tout fichier qui contient une icône est acceptable, y compris les fichiers. ico,. exe et. dll.</span><span class="sxs-lookup"><span data-stu-id="99843-127">Any file that contains an icon is acceptable, including .ico, .exe, and .dll files.</span></span> <span data-ttu-id="99843-128">Si le fichier contient plusieurs icônes, le chemin d’accès doit être suivi d’une virgule, puis de l’index de l’icône.</span><span class="sxs-lookup"><span data-stu-id="99843-128">If there is more than one icon in the file, the path should be followed by a comma, and then the index of the icon.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99843-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="99843-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99843-130">Types de fichiers</span><span class="sxs-lookup"><span data-stu-id="99843-130">File Types</span></span>](fa-file-types.md)
</dt> </dl>

 

 



