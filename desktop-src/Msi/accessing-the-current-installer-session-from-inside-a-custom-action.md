---
description: Les actions personnalisées non différées qui appellent des bibliothèques de liens dynamiques ou des scripts peuvent accéder à une installation en cours d’exécution pour interroger ou modifier les attributs de la session d’installation actuelle.
ms.assetid: cf70b0b3-ac81-47ab-a4c8-4db53ed9dc84
title: Accès à la session de programme d’installation actuelle à partir d’une action personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a870247f70742d408c0f5d1d0e67f20cef65d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951803"
---
# <a name="accessing-the-current-installer-session-from-inside-a-custom-action"></a><span data-ttu-id="aba54-103">Accès à la session de programme d’installation actuelle à partir d’une action personnalisée</span><span class="sxs-lookup"><span data-stu-id="aba54-103">Accessing the Current Installer Session from Inside a Custom Action</span></span>

<span data-ttu-id="aba54-104">Les actions personnalisées non différées qui appellent des [bibliothèques de liens dynamiques](dynamic-link-libraries.md) ou des [scripts](scripts.md) peuvent accéder à une installation en cours d’exécution pour interroger ou modifier les attributs de la session d’installation actuelle.</span><span class="sxs-lookup"><span data-stu-id="aba54-104">Nondeferred custom actions that call [dynamic-link libraries](dynamic-link-libraries.md) or [scripts](scripts.md) may access a running installation to query or modify the attributes of the current installation session.</span></span> <span data-ttu-id="aba54-105">Un seul objet de **session** peut exister pour chaque processus, et les scripts d’action personnalisés ne doivent pas essayer de créer une autre session.</span><span class="sxs-lookup"><span data-stu-id="aba54-105">Only one **Session** object can exist for each process, and custom action scripts must not attempt to create another session.</span></span>

<span data-ttu-id="aba54-106">Les actions personnalisées peuvent uniquement ajouter, modifier ou supprimer des lignes, des colonnes ou des tables temporaires dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="aba54-106">Custom actions can only add, modify, or remove temporary rows, columns, or tables from a database.</span></span> <span data-ttu-id="aba54-107">Les actions personnalisées ne peuvent pas modifier les données persistantes dans une base de données, par exemple les données qui font partie de la base de données stockée sur le disque.</span><span class="sxs-lookup"><span data-stu-id="aba54-107">Custom actions cannot modify persistent data in a database, for example, data that is a part of the database stored on disk.</span></span>

[<span data-ttu-id="aba54-108">Bibliothèques de liens dynamiques</span><span class="sxs-lookup"><span data-stu-id="aba54-108">Dynamic-Link Libraries</span></span>](dynamic-link-libraries.md)

<span data-ttu-id="aba54-109">Pour accéder à une installation en cours d’exécution, les actions personnalisées qui appellent des bibliothèques de liens dynamiques (DLL) sont passées à un handle du type MSIHANDLE pour la session active en tant que seul argument du point d’entrée de la DLL nommé dans la colonne cible de la [table CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="aba54-109">To access a running installation, custom actions that call dynamic-link libraries (DLL) are passed a handle of the type MSIHANDLE for the current session as the only argument to the DLL entry point named in the Target column of the [CustomAction Table](customaction-table.md).</span></span> <span data-ttu-id="aba54-110">Étant donné que le programme d’installation fournit ce handle, l’action personnalisée ne doit pas la fermer, par exemple pour recevoir le handle *hInstall* du programme d’installation, la fonction d’action personnalisée est déclarée comme suit.</span><span class="sxs-lookup"><span data-stu-id="aba54-110">Because the installer provides this handle, the custom action should not close it, for example, to receive the handle *hInstall* from the installer, the custom action function is declared as follows.</span></span>


```C++
UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



<span data-ttu-id="aba54-111">Pour un accès en lecture seule à la base de données actuelle, obtenez le handle de base de données en appelant [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase).</span><span class="sxs-lookup"><span data-stu-id="aba54-111">For read-only access to the current database obtain the database handle by calling [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase).</span></span> <span data-ttu-id="aba54-112">Pour plus d’informations, consultez [obtention d’un descripteur de base de données](obtaining-a-database-handle.md).</span><span class="sxs-lookup"><span data-stu-id="aba54-112">For more information, see [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span>

[<span data-ttu-id="aba54-113">Scripts</span><span class="sxs-lookup"><span data-stu-id="aba54-113">Scripts</span></span>](scripts.md)

<span data-ttu-id="aba54-114">Les actions personnalisées écrites en VBScript ou JScript peuvent accéder à la session d’installation actuelle à l’aide de l' [**objet session**](session-object.md).</span><span class="sxs-lookup"><span data-stu-id="aba54-114">Custom actions written in VBScript or JScript can access the current installation session by using the [**Session Object**](session-object.md).</span></span> <span data-ttu-id="aba54-115">Le programme d’installation crée un objet de **session** nommé « session » qui fait référence à l’installation actuelle.</span><span class="sxs-lookup"><span data-stu-id="aba54-115">The installer creates a **Session** object named "Session" that references the current installation.</span></span> <span data-ttu-id="aba54-116">Pour un accès en lecture seule à la base de données actuelle, utilisez la propriété [**Database**](session-database.md) de l’objet **session** .</span><span class="sxs-lookup"><span data-stu-id="aba54-116">For read-only access to the current database use the [**Database**](session-database.md) property of the **Session** object.</span></span>

<span data-ttu-id="aba54-117">Étant donné qu’un script est exécuté à partir du contexte de l’objet [**session**](session-object.md) , il n’est pas toujours nécessaire de qualifier entièrement les propriétés et les méthodes.</span><span class="sxs-lookup"><span data-stu-id="aba54-117">Because a script is run from the context of the [**Session**](session-object.md) object, it is not always necessary to fully qualify properties and methods.</span></span> <span data-ttu-id="aba54-118">Dans l’exemple suivant, quand vous utilisez VBScript, la référence me peut remplacer l’objet de **session** , par exemple, les trois lignes suivantes sont équivalentes.</span><span class="sxs-lookup"><span data-stu-id="aba54-118">In the following example, when using VBScript, the Me reference can replace the **Session** object, for example, the following three lines are equivalent.</span></span>


```VB
Session.SetInstallLevel 1
```




```VB
Me.SetInstallLevel 1
```




```VB
SetInstallLevel 1
```



[<span data-ttu-id="aba54-119">Fichiers exécutables</span><span class="sxs-lookup"><span data-stu-id="aba54-119">Executable Files</span></span>](executable-files.md)

<span data-ttu-id="aba54-120">Vous ne pouvez pas accéder à la session de programme d’installation actuelle à partir d’actions personnalisées qui appellent des fichiers exécutables lancés avec une ligne de commande, par exemple, [type d’action personnalisée 2](custom-action-type-2.md) et [type d’action personnalisé 18](custom-action-type-18.md).</span><span class="sxs-lookup"><span data-stu-id="aba54-120">You cannot access the current installer session from custom actions that call executable files launched with a command-line, for example, [Custom Action Type 2](custom-action-type-2.md) and [Custom Action Type 18](custom-action-type-18.md).</span></span>

[<span data-ttu-id="aba54-121">Actions personnalisées d’exécution différée</span><span class="sxs-lookup"><span data-stu-id="aba54-121">Deferred Execution Custom Actions</span></span>](deferred-execution-custom-actions.md)

<span data-ttu-id="aba54-122">Vous ne pouvez pas accéder à la session du programme d’installation en cours ou à toutes les données de propriété à partir d’une action personnalisée d’exécution différée.</span><span class="sxs-lookup"><span data-stu-id="aba54-122">You cannot access the current installer session or all property data from a deferred execution custom action.</span></span> <span data-ttu-id="aba54-123">Pour plus d’informations, consultez [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="aba54-123">For more information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aba54-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aba54-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aba54-125">Accès à une base de données ou à une session à partir d’une action personnalisée</span><span class="sxs-lookup"><span data-stu-id="aba54-125">Accessing a Database or Session from Inside a Custom Action</span></span>](accessing-a-database-or-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



