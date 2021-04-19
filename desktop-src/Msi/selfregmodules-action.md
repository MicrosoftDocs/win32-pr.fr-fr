---
description: L’action SelfRegModules traite tous les modules listés dans la table SelfReg et inscrit tous les modules installés sur le système. Le programme d’installation n’enregistre pas automatiquement les fichiers EXE.
ms.assetid: b139ae28-e479-4915-909d-2449244e9fd6
title: Action SelfRegModules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75895b1886fad51f36113ce6e677ba6a534ab0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535040"
---
# <a name="selfregmodules-action"></a><span data-ttu-id="43c3d-104">Action SelfRegModules</span><span class="sxs-lookup"><span data-stu-id="43c3d-104">SelfRegModules Action</span></span>

<span data-ttu-id="43c3d-105">L’action SelfRegModules traite tous les modules listés dans la table [Selfreg](selfreg-table.md) et inscrit tous les modules installés sur le système.</span><span class="sxs-lookup"><span data-stu-id="43c3d-105">The SelfRegModules action processes all modules listed in the [SelfReg](selfreg-table.md) table and registers all installed modules with the system.</span></span> <span data-ttu-id="43c3d-106">Le programme d’installation n’enregistre pas automatiquement les fichiers EXE.</span><span class="sxs-lookup"><span data-stu-id="43c3d-106">The installer does not self-register EXE files.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="43c3d-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="43c3d-107">Sequence Restrictions</span></span>

<span data-ttu-id="43c3d-108">L’action [InstallValidate](installvalidate-action.md) doit être appelée avant d’appeler l’action SelfRegModules.</span><span class="sxs-lookup"><span data-stu-id="43c3d-108">The [InstallValidate](installvalidate-action.md) action must be called before calling the SelfRegModules action.</span></span> <span data-ttu-id="43c3d-109">Si une action [InstallFiles](installfiles-action.md) est utilisée, elle doit apparaître avant l’action SelfRegModules dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="43c3d-109">If an [InstallFiles](installfiles-action.md) action is used, it must appear before the SelfRegModules action in the sequence.</span></span> <span data-ttu-id="43c3d-110">Étant donné que l’action SelfRegModules change le système, SelfRegModules doit venir après l' [action InstallInitialize](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="43c3d-110">Because the SelfRegModules action changes the system, SelfRegModules should come after the [InstallInitialize action](installinitialize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="43c3d-111">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="43c3d-111">ActionData Messages</span></span>



| <span data-ttu-id="43c3d-112">Champ</span><span class="sxs-lookup"><span data-stu-id="43c3d-112">Field</span></span> | <span data-ttu-id="43c3d-113">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="43c3d-113">Description of action data</span></span>                           |
|-------|------------------------------------------------------|
| <span data-ttu-id="43c3d-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="43c3d-114">\[1\]</span></span> | <span data-ttu-id="43c3d-115">Identificateur du fichier de module inscrit.</span><span class="sxs-lookup"><span data-stu-id="43c3d-115">Identifier of registered module file.</span></span>                |
| <span data-ttu-id="43c3d-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="43c3d-116">\[2\]</span></span> | <span data-ttu-id="43c3d-117">Identificateur du dossier contenant le fichier de module inscrit.</span><span class="sxs-lookup"><span data-stu-id="43c3d-117">Identifier of folder holding registered module file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="43c3d-118">Notes</span><span class="sxs-lookup"><span data-stu-id="43c3d-118">Remarks</span></span>

<span data-ttu-id="43c3d-119">L’action SelfRegModules tente d’appeler la fonction [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) du module planifié pour être inscrit.</span><span class="sxs-lookup"><span data-stu-id="43c3d-119">The SelfRegModules action attempts to call the [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) function of the module scheduled to be registered.</span></span> <span data-ttu-id="43c3d-120">Cette action s’exécute avec des privilèges élevés lorsque l’installation est exécutée avec des privilèges élevés, par exemple lors d’une installation par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="43c3d-120">This action runs with elevated privileges when the installation is being run with elevated privileges, such as during a per-machine installation.</span></span> <span data-ttu-id="43c3d-121">Au cours d’une installation par utilisateur, le programme d’installation exécute cette action avec des privilèges d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="43c3d-121">During a per-user installation the installer runs this action with user privileges.</span></span>

<span data-ttu-id="43c3d-122">Notez que vous ne pouvez pas spécifier l’ordre dans lequel le programme d’installation inscrit des dll à inscription automatique à l’aide de l' [action SelfUnRegModules](selfunregmodules-action.md).</span><span class="sxs-lookup"><span data-stu-id="43c3d-122">Note that you cannot specify the order in which the installer registers self-registering DLLs by using the [SelfUnRegModules action](selfunregmodules-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="43c3d-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="43c3d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43c3d-124">Spécification de l’ordre d’inscription automatique</span><span class="sxs-lookup"><span data-stu-id="43c3d-124">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
