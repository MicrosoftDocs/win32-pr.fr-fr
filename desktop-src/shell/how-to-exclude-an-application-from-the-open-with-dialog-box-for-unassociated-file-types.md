---
description: Comment exclure une application de la boîte de dialogue Ouvrir avec pour le type de fichier non associé.
title: Comment exclure une application de la boîte de dialogue Ouvrir avec pour les types de fichiers non associés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9443416e95fca112623d487bf58f4fce1d51d13d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556613"
---
# <a name="how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types"></a><span data-ttu-id="e4675-103">Comment exclure une application de la boîte de dialogue Ouvrir avec pour les types de fichiers non associés</span><span class="sxs-lookup"><span data-stu-id="e4675-103">How to Exclude an Application from the Open With Dialog Box for Unassociated File Types</span></span>

<span data-ttu-id="e4675-104">Lorsqu’un utilisateur tente d’ouvrir un fichier qui n’est pas membre d’un type de fichier inscrit (autrement dit, un type de fichier inconnu), ou lorsqu’un utilisateur sélectionne **Ouvrir avec** ou **ouvrir avec-> choisir le programme par défaut** dans le menu contextuel d’un fichier, le shell présente un sous-menu ou une boîte de dialogue qui permet à l’utilisateur de spécifier le programme utilisé pour ouvrir</span><span class="sxs-lookup"><span data-stu-id="e4675-104">When a user attempts to open a file that is not a member of any registered file type (that is, an unknown file type), or when a user selects **Open with** or **Open with -> Choose default program** from a file's shortcut menu, the Shell presents a submenu or dialog box that enables the user to specify the program used to open the file.</span></span>

<span data-ttu-id="e4675-105">Par défaut, toute application inscrite en tant que sous-clé de la **\_ classe HKEY classes \_ racine** \\  est présentée dans la boîte de dialogue **Ouvrir avec** .</span><span class="sxs-lookup"><span data-stu-id="e4675-105">By default, any application registered as a subkey of **HKEY\_CLASSES\_ROOT**\\**Applications** is presented in the **Open with** dialog box.</span></span> <span data-ttu-id="e4675-106">Ces applications sont présentées dans **Open avec** , que l’application soit inscrite ou non pour gérer le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="e4675-106">These applications are presented in **Open with** regardless of whether the application is registered to handle the file type.</span></span>

<span data-ttu-id="e4675-107">Pour empêcher qu’une application n’apparaisse dans la boîte de dialogue **Ouvrir avec** lorsque l’application ne doit pas ou ne peut pas être utilisée pour ouvrir certains types de fichiers, utilisez l’une des deux techniques décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="e4675-107">To prevent an application from appearing in the **Open with** dialog box when the application should not or cannot be used to open certain file types, use one of the two techniques described in this topic.</span></span>

## <a name="instructions"></a><span data-ttu-id="e4675-108">Instructions</span><span class="sxs-lookup"><span data-stu-id="e4675-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="e4675-109">Étape 1 :</span><span class="sxs-lookup"><span data-stu-id="e4675-109">Step 1:</span></span>

<span data-ttu-id="e4675-110">Ajoutez une entrée NoOpenWith à la sous-clé de l’application.</span><span class="sxs-lookup"><span data-stu-id="e4675-110">Add a NoOpenWith entry to the application's subkey.</span></span> <span data-ttu-id="e4675-111">Quand une application utilise un type de fichier, Windows enregistre ces informations pour créer la liste des **Programmes recommandés** .</span><span class="sxs-lookup"><span data-stu-id="e4675-111">When an application uses a file type, Windows records that information to build the **Recommended Programs** list.</span></span> <span data-ttu-id="e4675-112">Cette liste est présentée dans le sous-menu **Ouvrir avec** , comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="e4675-112">This list is presented in the **Open with** submenu as shown in the following screen shot.</span></span>

![capture d’écran du menu contextuel avec le sous-menu Ouvrir avec affiché](images/file-assoc/openwithsubmenu.png)

<span data-ttu-id="e4675-114">Ces applications recommandées sont également affichées dans la partie **Programmes recommandés** de la boîte de dialogue **Ouvrir avec** , comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="e4675-114">These recommended applications are also shown in the **Recommended Programs** portion of the **Open with** dialog box as shown in the following screen shot.</span></span>

![capture d’écran de la boîte de dialogue Ouvrir avec avec les programmes recommandés](images/file-assoc/openwithdialog.png)

> [!Note]  
> <span data-ttu-id="e4675-116">Si une application s’est inscrite dans [OpenWithList](fa-file-types.md) ou OpenWithProgIDs pour le type de fichier, elle apparaît dans la liste des **Programmes recommandés** , même si l’entrée NoOpenWith est définie.</span><span class="sxs-lookup"><span data-stu-id="e4675-116">If an application has registered itself in the [OpenWithList](fa-file-types.md) or OpenWithProgIDs for the file type, it will appear in the **Recommended Programs** list even if the NoOpenWith entry is set.</span></span> <span data-ttu-id="e4675-117">En outre, n’oubliez pas que, qu’une application soit proposée dans une liste de programmes recommandés, un utilisateur peut accéder manuellement à n’importe quel fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="e4675-117">Also, remember that regardless of whether an application is offered in a list of recommended programs, a user can manually browse to any executable file.</span></span>

 

<span data-ttu-id="e4675-118">Les applications peuvent désactiver ce suivi en spécifiant une valeur NoOpenWith sous la sous-clé de l’application.</span><span class="sxs-lookup"><span data-stu-id="e4675-118">Applications can disable this tracking by specifying a NoOpenWith value under the application's subkey.</span></span>

<span data-ttu-id="e4675-119">L’entrée NoOpenWith est une valeur **reg \_ SZ** vide, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="e4675-119">The NoOpenWith entry is an empty **REG\_SZ** value as shown in the following example.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         NoOpenWith
```

<span data-ttu-id="e4675-120">La définition de l’entrée NoOpenWith a également les effets suivants :</span><span class="sxs-lookup"><span data-stu-id="e4675-120">Setting the NoOpenWith entry also has these effects:</span></span>

-   <span data-ttu-id="e4675-121">Empêche l’épinglage d’un fichier à la liste de liens de l’application par le biais du glisser-déplacer, sauf si l’application est inscrite spécifiquement pour gérer ce type de fichier.</span><span class="sxs-lookup"><span data-stu-id="e4675-121">Prevents pinning a file to the application's Jump List through drag-and-drop, unless the application is specifically registered to handle that file type.</span></span>
-   <span data-ttu-id="e4675-122">Empêche la boîte de dialogue de fichier commune et tout appel à la fonction [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) d’ajouter n’importe quel fichier à la liste de raccourcis de l’application, sauf si l’application est inscrite spécifiquement pour gérer ce type de fichier.</span><span class="sxs-lookup"><span data-stu-id="e4675-122">Prevents the common file dialog box and any call to the [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) function from adding any file to the application's Jump List, unless the application is specifically registered to handle that file type.</span></span>

### <a name="step-2"></a><span data-ttu-id="e4675-123">Étape 2 :</span><span class="sxs-lookup"><span data-stu-id="e4675-123">Step 2:</span></span>

<span data-ttu-id="e4675-124">La deuxième façon d’empêcher une application d’apparaître dans la boîte de dialogue **Ouvrir avec** consiste à utiliser la sous-clé **SupportedTypes** pour répertorier explicitement les extensions des types de fichiers que l’application peut ouvrir.</span><span class="sxs-lookup"><span data-stu-id="e4675-124">The second way to prevent an application from appearing in the **Open with** dialog box is to use the **SupportedTypes** subkey to explicitly list the extensions of file types that the application can open.</span></span> <span data-ttu-id="e4675-125">Cela empêche l’application d’apparaître dans la boîte de dialogue **Ouvrir avec** pour les types de fichiers qu’elle ne peut pas ouvrir.</span><span class="sxs-lookup"><span data-stu-id="e4675-125">This prevents the application from appearing in the **Open with** dialog box for file types that it cannot open.</span></span> <span data-ttu-id="e4675-126">Cela entraîne également l’affichage de l’application dans la liste des **Programmes recommandés** , comme indiqué précédemment.</span><span class="sxs-lookup"><span data-stu-id="e4675-126">It also causes the application to appear in the **Recommended Programs** list as discussed previously.</span></span>

<span data-ttu-id="e4675-127">Cette méthode est particulièrement utile si une application peut enregistrer un fichier sous un certain type de fichier, mais ne peut pas ouvrir ce type de fichier.</span><span class="sxs-lookup"><span data-stu-id="e4675-127">This method is particularly useful if an application can save a file as a certain file type but cannot open that file type.</span></span> <span data-ttu-id="e4675-128">Une application doit également définir l' \_ indicateur Fos DONTADDTORECENT par le biais de [**IFileDialog :: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) lors de l’appel de la boîte de dialogue **Enregistrer** .</span><span class="sxs-lookup"><span data-stu-id="e4675-128">An application should also set the FOS\_DONTADDTORECENT flag through [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) when calling the **Save** dialog box.</span></span> <span data-ttu-id="e4675-129">Cela empêche l’ajout de l’élément aux portions **récentes** ou **fréquentes** d’une liste de raccourcis.</span><span class="sxs-lookup"><span data-stu-id="e4675-129">This keeps the item from being added to the **Recent** or **Frequent** portions of a Jump List.</span></span> <span data-ttu-id="e4675-130">Il empêche également le suivi de l’application sous [OpenWithList](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="e4675-130">It also blocks the application from being tracked under [OpenWithList](fa-file-types.md).</span></span>

<span data-ttu-id="e4675-131">Chaque extension prise en charge est ajoutée sous la forme d’une entrée sous la sous-clé **SupportedTypes** , comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="e4675-131">Each supported extension is added as an entry under the **SupportedTypes** subkey as shown in the following example.</span></span> <span data-ttu-id="e4675-132">Les entrées sont de type **reg \_ SZ** ou **reg \_ null**, sans valeurs associées.</span><span class="sxs-lookup"><span data-stu-id="e4675-132">The entries are of type **REG\_SZ** or **REG\_NULL**, with no associated values.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      ApplicationName
         SupportedTypes
            .ext1
            .ext2
            .ext3
```

<span data-ttu-id="e4675-133">Si une sous-clé **SupportedTypes** est fournie, seuls les fichiers avec ces extensions sont éligibles à l’épinglage à la liste de raccourcis de l’application ou au suivi dans la liste des destinations **récentes** ou **fréquentes** d’une application.</span><span class="sxs-lookup"><span data-stu-id="e4675-133">If a **SupportedTypes** subkey is provided, only files with those extensions are eligible for pinning to the application's Jump List or for being tracked in an application's **Recent** or **Frequent** destinations list.</span></span>

<span data-ttu-id="e4675-134">L’entrée NoOpenWith remplace la sous-clé **SupportedTypes** et masque l’application dans la boîte de dialogue **Ouvrir avec** .</span><span class="sxs-lookup"><span data-stu-id="e4675-134">The NoOpenWith entry overrides the **SupportedTypes** subkey and hides the application in the **Open with** dialog box.</span></span>

 

 
