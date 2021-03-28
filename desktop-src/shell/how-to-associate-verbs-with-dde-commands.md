---
description: Illustre l’appel d’une commande DDE à l’aide d’un verbe de Shell.
ms.assetid: 65DDD992-5E96-447E-9151-2CCA740822A1
title: Comment associer des verbes à des commandes DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7174a22c993d93c347c8a0368fa7d1798362070f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973175"
---
# <a name="how-to-associate-verbs-with-dde-commands"></a><span data-ttu-id="699b3-103">Comment associer des verbes à des commandes DDE</span><span class="sxs-lookup"><span data-stu-id="699b3-103">How to Associate Verbs with DDE Commands</span></span>

<span data-ttu-id="699b3-104">L’appel d’un verbe lance normalement l’application spécifiée par la sous-clé de commande du verbe.</span><span class="sxs-lookup"><span data-stu-id="699b3-104">Invoking a verb ordinarily launches the application that is specified by the verb's command subkey.</span></span> <span data-ttu-id="699b3-105">Toutefois, si votre application prend en charge les échange dynamique de données (DDE), vous pouvez à la place demander à l’interpréteur de commandes DDE de lancer une conversation DDE.</span><span class="sxs-lookup"><span data-stu-id="699b3-105">However, if your application supports Dynamic Data Exchange (DDE), you can instead have the Shell initiate a DDE conversation.</span></span>

<span data-ttu-id="699b3-106">Pour spécifier que l’appel d’un verbe doit initier une conversation DDE, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="699b3-106">To specify that invoking a verb should initiate a DDE conversation, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="699b3-107">Instructions</span><span class="sxs-lookup"><span data-stu-id="699b3-107">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="699b3-108">Étape 1 :</span><span class="sxs-lookup"><span data-stu-id="699b3-108">Step 1:</span></span>

<span data-ttu-id="699b3-109">Ajoutez une sous-clé **ddeexec** à la clé du verbe.</span><span class="sxs-lookup"><span data-stu-id="699b3-109">Add a **ddeexec** subkey to the verb's key.</span></span>

### <a name="step-2"></a><span data-ttu-id="699b3-110">Étape 2 :</span><span class="sxs-lookup"><span data-stu-id="699b3-110">Step 2:</span></span>

<span data-ttu-id="699b3-111">Définissez la valeur par défaut de **ddeexec** sur la chaîne de commande DDE.</span><span class="sxs-lookup"><span data-stu-id="699b3-111">Set the default value of **ddeexec** to the DDE command string.</span></span>

## <a name="remarks"></a><span data-ttu-id="699b3-112">Notes</span><span class="sxs-lookup"><span data-stu-id="699b3-112">Remarks</span></span>

<span data-ttu-id="699b3-113">La clé **ddeexec** a trois sous-clés facultatives qui fournissent un certain contrôle sur le processus DDE :</span><span class="sxs-lookup"><span data-stu-id="699b3-113">The **ddeexec** key has three optional subkeys that provide some control over the DDE process:</span></span>

-   <span data-ttu-id="699b3-114">**application**.</span><span class="sxs-lookup"><span data-stu-id="699b3-114">**application**.</span></span> <span data-ttu-id="699b3-115">Définissez la valeur par défaut de cette sous-clé sur le nom de l’application à utiliser pour établir la conversation DDE.</span><span class="sxs-lookup"><span data-stu-id="699b3-115">Set the default value of this subkey to the application name to be used to establish the DDE conversation.</span></span> <span data-ttu-id="699b3-116">S’il n’existe aucune sous-clé d' **application** , la valeur par défaut de la sous-clé de **commande** du verbe est utilisée comme nom d’application.</span><span class="sxs-lookup"><span data-stu-id="699b3-116">If there is no **application** subkey, the default value of the verb's **command** subkey is used as the application name.</span></span>
-   <span data-ttu-id="699b3-117">**rubrique**.</span><span class="sxs-lookup"><span data-stu-id="699b3-117">**topic**.</span></span> <span data-ttu-id="699b3-118">Définissez la valeur par défaut de cette sous-clé sur le nom de la rubrique de la conversation DDE.</span><span class="sxs-lookup"><span data-stu-id="699b3-118">Set the default value of this subkey to the topic name of the DDE conversation.</span></span> <span data-ttu-id="699b3-119">S’il n’existe aucune sous-clé de **rubrique** , System est utilisé comme nom de rubrique.</span><span class="sxs-lookup"><span data-stu-id="699b3-119">If there is no **topic** subkey, System is used as the topic name.</span></span>
-   <span data-ttu-id="699b3-120">**ifexec**.</span><span class="sxs-lookup"><span data-stu-id="699b3-120">**ifexec**.</span></span> <span data-ttu-id="699b3-121">Définissez la valeur par défaut de cette sous-clé sur la commande DDE à utiliser si la conversation DDE ne peut pas être lancée.</span><span class="sxs-lookup"><span data-stu-id="699b3-121">Set the default value of this subkey to the DDE command to be used if DDE conversation cannot be initiated.</span></span> <span data-ttu-id="699b3-122">Lorsque l’initialisation échoue, l’application qui est spécifiée par la valeur par défaut de la sous-clé de **commande** du verbe est lancée.</span><span class="sxs-lookup"><span data-stu-id="699b3-122">When initiation fails, the application that is specified by the default value of the verb's **command** subkey is launched.</span></span> <span data-ttu-id="699b3-123">Si une clé **ifexec** existe, sa valeur par défaut est utilisée comme commande DDE.</span><span class="sxs-lookup"><span data-stu-id="699b3-123">If an **ifexec** key exists, its default value will then be used as the DDE command.</span></span> <span data-ttu-id="699b3-124">S’il n’existe aucune sous-clé **ifexec** , la valeur par défaut de la clé **ddeexec** est réutilisée comme commande DDE.</span><span class="sxs-lookup"><span data-stu-id="699b3-124">If there is no **ifexec** subkey, the default value of the **ddeexec** key will be used again as the DDE command.</span></span>

<span data-ttu-id="699b3-125">L’exemple suivant spécifie que l’appel du verbe Open pour MyProgram. 1 lance une conversation DDE avec la commande DDE Open (« %1 ») et le nom d’application MyProgram.</span><span class="sxs-lookup"><span data-stu-id="699b3-125">The following example specifies that invoking the open verb for MyProgram.1 initiates a DDE conversation with a DDE command of Open("%1") and an application name of MyProgram.</span></span>

```
HKEY_CLASSES_ROOT
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
            ddeexec
               (Default) = Open("%1")
               application
                  (Default) = MyProgram
```

 

 



