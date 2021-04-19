---
description: L’action SelfUnregModules annule l’inscription de tous les modules répertoriés dans la table SelfReg qui sont planifiés pour être désinstallés. Le programme d’installation ne s’inscrit pas automatiquement. Fichiers EXE.
ms.assetid: fa5a5abb-ecd4-434c-b176-83cdca280a13
title: Action SelfUnregModules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3a0d98d8a8afe45b9b78f5c8af8ca2f84b2244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535041"
---
# <a name="selfunregmodules-action"></a><span data-ttu-id="4976a-104">Action SelfUnregModules</span><span class="sxs-lookup"><span data-stu-id="4976a-104">SelfUnregModules Action</span></span>

<span data-ttu-id="4976a-105">L’action SelfUnregModules annule l’inscription de tous les modules répertoriés dans la [table Selfreg](selfreg-table.md) qui sont planifiés pour être désinstallés.</span><span class="sxs-lookup"><span data-stu-id="4976a-105">The SelfUnregModules action unregisters all modules listed in the [SelfReg table](selfreg-table.md) that are scheduled to be uninstalled.</span></span> <span data-ttu-id="4976a-106">Le programme d’installation ne s’inscrit pas automatiquement. Fichiers EXE.</span><span class="sxs-lookup"><span data-stu-id="4976a-106">The installer does not self-register .EXE files.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="4976a-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="4976a-107">Sequence Restrictions</span></span>

<span data-ttu-id="4976a-108">L’action [InstallValidate](installvalidate-action.md) doit apparaître avant l’action SelfUnregModules dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="4976a-108">The [InstallValidate](installvalidate-action.md) action must appear before the SelfUnregModules action in the sequence.</span></span> <span data-ttu-id="4976a-109">Si une action [SelfRegModules](selfregmodules-action.md) est utilisée, elle doit apparaître après l’action SelfUnregModules dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="4976a-109">If a [SelfRegModules](selfregmodules-action.md) action is used it must appear after the SelfUnregModules action in the sequence.</span></span> <span data-ttu-id="4976a-110">Si une [action RemoveFiles](removefiles-action.md) est utilisée, elle doit apparaître après l’action SelfUnregModules dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="4976a-110">If a [RemoveFiles action](removefiles-action.md) is used it must appear after the SelfUnregModules action in the sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="4976a-111">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="4976a-111">ActionData Messages</span></span>



| <span data-ttu-id="4976a-112">Champ</span><span class="sxs-lookup"><span data-stu-id="4976a-112">Field</span></span> | <span data-ttu-id="4976a-113">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="4976a-113">Description of action data</span></span>                             |
|-------|--------------------------------------------------------|
| <span data-ttu-id="4976a-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="4976a-114">\[1\]</span></span> | <span data-ttu-id="4976a-115">Identificateur du fichier de module non inscrit.</span><span class="sxs-lookup"><span data-stu-id="4976a-115">Identifier of unregistered module file.</span></span>                |
| <span data-ttu-id="4976a-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="4976a-116">\[2\]</span></span> | <span data-ttu-id="4976a-117">Identificateur du dossier contenant le fichier de module non inscrit.</span><span class="sxs-lookup"><span data-stu-id="4976a-117">Identifier of folder holding unregistered module file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4976a-118">Notes</span><span class="sxs-lookup"><span data-stu-id="4976a-118">Remarks</span></span>

<span data-ttu-id="4976a-119">L’action SelfUnregModules tente d’appeler la fonction [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) du module dont l’inscription doit être annulée.</span><span class="sxs-lookup"><span data-stu-id="4976a-119">The SelfUnregModules action attempts to call the [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) function of the module that is to be unregistered.</span></span> <span data-ttu-id="4976a-120">Cette action s’exécute avec des privilèges élevés lorsque l’installation est exécutée avec des privilèges élevés, par exemple lors d’une installation par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4976a-120">This action runs with elevated privileges when the installation is being run with elevated privileges, such as during a per-machine installation.</span></span> <span data-ttu-id="4976a-121">Pendant une installation par utilisateur, le programme d’installation exécute cette action avec des privilèges d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4976a-121">During a per-user installation, the installer runs this action with user privileges.</span></span>

<span data-ttu-id="4976a-122">Notez que vous ne pouvez pas spécifier l’ordre dans lequel le programme d’installation annule l’inscription automatique des dll à l’aide de l’action SelfUnRegModules.</span><span class="sxs-lookup"><span data-stu-id="4976a-122">Note that you cannot specify the order in which the installer unregisters self-registering DLLs by using the SelfUnRegModules action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4976a-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4976a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4976a-124">Spécification de l’ordre d’inscription automatique</span><span class="sxs-lookup"><span data-stu-id="4976a-124">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
