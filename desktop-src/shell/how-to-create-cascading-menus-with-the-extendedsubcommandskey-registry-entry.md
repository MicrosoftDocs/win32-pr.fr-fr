---
description: Dans Windows 7 et versions ultérieures, vous pouvez utiliser la sous-clé ExtendedSubCommandsKey pour créer des menus en cascade étendus.
ms.assetid: 6E8B4FB7-D4DB-4DBC-AF6F-59D02CB6AB13
title: Créer des menus en cascade avec l’entrée de Registre ExtendedSubCommandsKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220a38825ae250a0d58d30bc7de93f290f819eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756514"
---
# <a name="how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a><span data-ttu-id="2d44e-103">Comment créer des menus en cascade avec l’entrée de Registre ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="2d44e-103">How to Create Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>

<span data-ttu-id="2d44e-104">Dans Windows 7 et versions ultérieures, vous pouvez utiliser la sous-clé **ExtendedSubCommandsKey** pour créer des menus en cascade étendus.</span><span class="sxs-lookup"><span data-stu-id="2d44e-104">In Windows 7 and later, you can use the **ExtendedSubCommandsKey** subkey to create extended cascading menus.</span></span>

<span data-ttu-id="2d44e-105">La capture d’écran suivante est un exemple de menu en cascade étendu.</span><span class="sxs-lookup"><span data-stu-id="2d44e-105">The following screen shot is an example of an extended cascading menu.</span></span>

![capture d’écran montrant le menu en cascade étendu pour les appareils](images/file-assoc/extendedsubcommandskey.png)

<span data-ttu-id="2d44e-107">Étant donné que **HKEY \_ classes \_ root** est une combinaison de **HKEY \_ Current \_ User** et de **HKEY \_ local \_ machine**, vous pouvez inscrire les sous-verbes sous la sous-clé de classes de logiciels de l' **\_ \_ utilisateur actuel HKEY** \\  \\  .</span><span class="sxs-lookup"><span data-stu-id="2d44e-107">Because **HKEY\_CLASSES\_ROOT** is a combination of **HKEY\_CURRENT\_USER** and **HKEY\_LOCAL\_MACHINE**, you can register the subverbs under the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span> <span data-ttu-id="2d44e-108">L’avantage de cette approche est que les autorisations élevées ne sont pas requises.</span><span class="sxs-lookup"><span data-stu-id="2d44e-108">The advantage of doing so is that elevated permission is not required.</span></span> <span data-ttu-id="2d44e-109">D’autres associations de fichiers peuvent réutiliser cet ensemble complet de verbes en spécifiant la même sous-clé **ExtendedSubCommandsKey** .</span><span class="sxs-lookup"><span data-stu-id="2d44e-109">Other file associations can reuse this entire set of verbs by specifying the same **ExtendedSubCommandsKey** subkey.</span></span> <span data-ttu-id="2d44e-110">Si vous n’avez pas besoin de réutiliser cet ensemble de verbes, vous pouvez répertorier les verbes sous le parent.</span><span class="sxs-lookup"><span data-stu-id="2d44e-110">If you do not need to reuse this set of verbs, you can list the verbs under the parent.</span></span> <span data-ttu-id="2d44e-111">Dans ce cas, assurez-vous que la valeur par défaut du parent est vide, comme illustré dans l’exemple d’entrée de Registre dans cette section.</span><span class="sxs-lookup"><span data-stu-id="2d44e-111">In this case, make sure the default value of the parent is empty, as illustrated in the registry entry example in this section.</span></span>

## <a name="instructions"></a><span data-ttu-id="2d44e-112">Instructions</span><span class="sxs-lookup"><span data-stu-id="2d44e-112">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="2d44e-113">Étape 1 :</span><span class="sxs-lookup"><span data-stu-id="2d44e-113">Step 1:</span></span>

<span data-ttu-id="2d44e-114">Créez une sous-clé sous **HKEY \_ classes \_ racine** \\ *ProgID* \\ **Shell** \\ *CascadeMenuKey* et donnez à CascadeMenuKey un nom tel que *CascadeTest*, par exemple.</span><span class="sxs-lookup"><span data-stu-id="2d44e-114">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell**\\*CascadeMenuKey* and give the CascadeMenuKey a name such as *CascadeTest*, for example.</span></span> <span data-ttu-id="2d44e-115">Ajoutez ensuite une entrée MUIVerb de type de Registre **\_ SZ** et donnez-lui un nom tel que test cascade menu 2, comme illustré dans l’exemple de Registre suivant.</span><span class="sxs-lookup"><span data-stu-id="2d44e-115">Then add a MUIVerb entry of **REG\_SZ** type and give it a name such as Test Cascade Menu 2, as illustrated in the following registry example.</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      shell
         CascadeTest
            MUIVerb = Test Cascade Menu 2
```

### <a name="step-2"></a><span data-ttu-id="2d44e-116">Étape 2 :</span><span class="sxs-lookup"><span data-stu-id="2d44e-116">Step 2:</span></span>

<span data-ttu-id="2d44e-117">Sous la sous-clé *CascadeTest* que vous avez créée, ajoutez une sous-clé **ExtendedSubCommandsKey** , puis ajoutez les sous-commandes du document (de type **reg \_ SZ**), par exemple :</span><span class="sxs-lookup"><span data-stu-id="2d44e-117">Under the *CascadeTest* subkey that you created, add an **ExtendedSubCommandsKey** subkey, and then add the document subcommands (of type **REG\_SZ**); for example:</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Layout
               Properties
               Select all
```

<span data-ttu-id="2d44e-118">Assurez-vous que la valeur par défaut de la sous-clé *menu de test cascade 2* est vide et affichée comme **(valeur non définie)**.</span><span class="sxs-lookup"><span data-stu-id="2d44e-118">Ensure that the default value of the *Test Cascade Menu 2* subkey is empty, and shown as **(value not set)**.</span></span>

### <a name="step-3"></a><span data-ttu-id="2d44e-119">Étape 3 :</span><span class="sxs-lookup"><span data-stu-id="2d44e-119">Step 3:</span></span>

<span data-ttu-id="2d44e-120">Remplissez les sous-verbes à l’aide de l’une des implémentations de verbe statique suivantes.</span><span class="sxs-lookup"><span data-stu-id="2d44e-120">Populate the subverbs using any of the following static verb implementations.</span></span> <span data-ttu-id="2d44e-121">Notez que la sous-clé CommandFlags représente les valeurs EXPCMDFLAGS.</span><span class="sxs-lookup"><span data-stu-id="2d44e-121">Note that the CommandFlags subkey represents EXPCMDFLAGS values.</span></span> <span data-ttu-id="2d44e-122">Si vous souhaitez ajouter un séparateur avant ou après l’élément de menu cascade, utilisez ECF \_ SEPARATORBEFORE (0x20) ou ECF \_ SEPARATORAFTER (0x40).</span><span class="sxs-lookup"><span data-stu-id="2d44e-122">If you want to add a separator before or after the cascade menu item, use ECF\_SEPARATORBEFORE (0x20) or ECF\_SEPARATORAFTER (0x40).</span></span> <span data-ttu-id="2d44e-123">Pour obtenir une description de ces indicateurs Windows 7 et versions ultérieures, consultez [**IExplorerCommand :: GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span><span class="sxs-lookup"><span data-stu-id="2d44e-123">For a description of these Windows 7 and later flags, see [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span></span> <span data-ttu-id="2d44e-124">ECF \_ SEPARATORBEFORE fonctionne uniquement pour les éléments de menu de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="2d44e-124">ECF\_SEPARATORBEFORE works only for the top level menu items.</span></span> <span data-ttu-id="2d44e-125">MUIVerb est de type **reg \_ SZ** et CommandFlags est de type **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="2d44e-125">MUIVerb is of type **REG\_SZ**, and CommandFlags is of type **REG\_DWORD**.</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Shell
                  cmd1
                     MUIVerb = Notepad
                     command
                        (Default) = %SystemRoot%\system32\notepad.exe %1
                  cmd2
                     MUIVerb = Wordpad
                     CommandFlags = 0x20
                     command
                        (Default) = C:\Program Files\Windows NT\Accessories\wordpad.exe %1
```

## <a name="remarks"></a><span data-ttu-id="2d44e-126">Notes</span><span class="sxs-lookup"><span data-stu-id="2d44e-126">Remarks</span></span>

<span data-ttu-id="2d44e-127">La capture d’écran suivante illustre les exemples d’entrée de clé de Registre précédents.</span><span class="sxs-lookup"><span data-stu-id="2d44e-127">The following screen shot is an illustration of the previous registry key entry examples.</span></span>

![capture d’écran montrant un exemple de menu en cascade montrant les choix du bloc-notes et de WordPad](images/file-assoc/testcascademenu2.png)

 

 



