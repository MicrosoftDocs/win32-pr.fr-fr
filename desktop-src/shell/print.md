---
description: L’API Shell fournit des fonctions que vous pouvez utiliser pour gérer des imprimantes en réseau. Si le verbe Print est associé à un fichier, vous pouvez utiliser la commande ShellExecuteEx pour l’imprimer.
ms.assetid: b94fca60-237a-43b1-a75a-faccf9dc63fb
title: Gestion des imprimantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e9625fbe17c0dd350a10c0c71dcd5332fb9154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973350"
---
# <a name="managing-printers"></a><span data-ttu-id="b1f26-104">Gestion des imprimantes</span><span class="sxs-lookup"><span data-stu-id="b1f26-104">Managing Printers</span></span>

<span data-ttu-id="b1f26-105">L’API Shell fournit des fonctions que vous pouvez utiliser pour gérer des imprimantes en réseau.</span><span class="sxs-lookup"><span data-stu-id="b1f26-105">The Shell API provides functions that you can use to manage networked printers.</span></span> <span data-ttu-id="b1f26-106">Si le verbe **Print** est associé à un fichier, vous pouvez utiliser la commande [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) pour l’imprimer.</span><span class="sxs-lookup"><span data-stu-id="b1f26-106">If a file has the **print** verb associated with it, you can use the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) command to print it.</span></span>

-   [<span data-ttu-id="b1f26-107">Gestion des imprimantes</span><span class="sxs-lookup"><span data-stu-id="b1f26-107">Printer Management</span></span>](#printer-management)
-   [<span data-ttu-id="b1f26-108">Impression de fichiers avec ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="b1f26-108">Printing Files with ShellExecuteEx</span></span>](#printing-files-with-shellexecuteex)

## <a name="printer-management"></a><span data-ttu-id="b1f26-109">Gestion des imprimantes</span><span class="sxs-lookup"><span data-stu-id="b1f26-109">Printer Management</span></span>

<span data-ttu-id="b1f26-110">Vous pouvez gérer les imprimantes sur un système à l’aide de la fonction [**SHInvokePrinterCommand**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) .</span><span class="sxs-lookup"><span data-stu-id="b1f26-110">You can manage printers on a system with the [**SHInvokePrinterCommand**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) function.</span></span> <span data-ttu-id="b1f26-111">Cette fonction vous permet d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b1f26-111">This function allows you to:</span></span>

-   <span data-ttu-id="b1f26-112">Installez les imprimantes.</span><span class="sxs-lookup"><span data-stu-id="b1f26-112">Install printers.</span></span>
-   <span data-ttu-id="b1f26-113">Ouvrez imprimantes.</span><span class="sxs-lookup"><span data-stu-id="b1f26-113">Open printers.</span></span>
-   <span data-ttu-id="b1f26-114">Obtient les propriétés de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="b1f26-114">Get printer properties.</span></span>
-   <span data-ttu-id="b1f26-115">Créer des liens d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="b1f26-115">Create printer links.</span></span>
-   <span data-ttu-id="b1f26-116">Imprimez une page de test.</span><span class="sxs-lookup"><span data-stu-id="b1f26-116">Print a test page.</span></span>

## <a name="printing-files-with-shellexecuteex"></a><span data-ttu-id="b1f26-117">Impression de fichiers avec ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="b1f26-117">Printing Files with ShellExecuteEx</span></span>

<span data-ttu-id="b1f26-118">Si un type de fichier est associé à une commande d’impression, vous pouvez imprimer le fichier en appelant [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) avec **Print** comme verbe.</span><span class="sxs-lookup"><span data-stu-id="b1f26-118">If a file type has a print command associated with it, you can print the file by calling [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) with **print** as the verb.</span></span> <span data-ttu-id="b1f26-119">Cette commande est souvent la même que celle utilisée pour le verbe **Open** , avec l’ajout d’un indicateur pour indiquer à l’application d’imprimer le fichier.</span><span class="sxs-lookup"><span data-stu-id="b1f26-119">This command is often the same as that used for the **open** verb, with the addition of a flag to tell the application to print the file.</span></span> <span data-ttu-id="b1f26-120">Par exemple, les fichiers. txt peuvent être imprimés par Microsoft WordPad.</span><span class="sxs-lookup"><span data-stu-id="b1f26-120">For instance, .txt files can be printed by Microsoft WordPad.</span></span> <span data-ttu-id="b1f26-121">Le verbe **Open** d’un fichier. txt correspond donc à une commande semblable à la suivante :</span><span class="sxs-lookup"><span data-stu-id="b1f26-121">The **open** verb for a .txt file would thus correspond to something like the following command:</span></span>


```C++
"C:\Program Files\Windows NT\Accessories\Wordpad.exe" /p "%1"
```



<span data-ttu-id="b1f26-122">Quand vous utilisez [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) pour imprimer un fichier. txt, WordPad ouvre le fichier, l’imprime, puis ferme le contrôle à l’application.</span><span class="sxs-lookup"><span data-stu-id="b1f26-122">When you use [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to print a .txt file, WordPad opens the file, prints it, and then closes, returning control to the application.</span></span> <span data-ttu-id="b1f26-123">L’exemple de fonction suivant prend un chemin d’accès complet et utilise **ShellExecuteEx** pour l’imprimer, à l’aide de la commande Imprimer associée à son extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="b1f26-123">The following sample function takes a fully qualified path, and uses **ShellExecuteEx** to print it, using the print command associated with its file name extension.</span></span>


```C++
#include <shlobj.h>

HINSTANCE PrintFile(LPCTSTR pszFileName)
{
    SHELLEXECUTEINFO ShExecInfo;
    HINSTANCE hInst;

    // Fill the SHELLEXECUTEINFO array.

    ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
    ShExecInfo.fMask = NULL;
    ShExecInfo.hwnd = NULL;
    ShExecInfo.lpVerb = "print";
    ShExecInfo.lpFile = pszFileName;  // a fully qualified path
    ShExecInfo.lpParameters = NULL;
    ShExecInfo.lpDirectory = NULL;    
    ShExecInfo.nShow = SW_MAXIMIZE;
    ShExecInfo.hInstApp = NULL;

    hInst = ShellExecuteEx(&ShExecInfo);
    
    return hInst;
}
```



 

 



