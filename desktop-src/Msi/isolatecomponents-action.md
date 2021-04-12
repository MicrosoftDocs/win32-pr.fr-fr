---
description: L’action IsolateComponents installe une copie d’un composant (généralement une DLL partagée) dans un emplacement privé pour une utilisation par une application spécifique (généralement un fichier. exe).
ms.assetid: 3f39ad5d-5539-48cc-8369-bd4d3127fbdd
title: Action IsolateComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fe36f8c30e67591662ca2fce6c0b0ac2150ebb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320569"
---
# <a name="isolatecomponents-action"></a><span data-ttu-id="1186e-103">Action IsolateComponents</span><span class="sxs-lookup"><span data-stu-id="1186e-103">IsolateComponents Action</span></span>

<span data-ttu-id="1186e-104">L’action IsolateComponents installe une copie d’un composant (généralement une DLL partagée) dans un emplacement privé pour une utilisation par une application spécifique (généralement un fichier. exe).</span><span class="sxs-lookup"><span data-stu-id="1186e-104">The IsolateComponents action installs a copy of a component (commonly a shared DLL) into a private location for use by a specific application (typically an .exe).</span></span> <span data-ttu-id="1186e-105">Cela isole l’application des autres copies du composant qui peuvent être installées dans un emplacement partagé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1186e-105">This isolates the application from other copies of the component that may be installed to a shared location on the computer.</span></span> <span data-ttu-id="1186e-106">Pour plus d’informations, consultez [composants isolés](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="1186e-106">For more information, see [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="1186e-107">L’action fait référence à chaque enregistrement de la [table IsolatedComponent](isolatedcomponent-table.md) et associe les fichiers du composant figurant dans le \_ champ composant partagé avec le composant indiqué dans le \_ champ application du composant.</span><span class="sxs-lookup"><span data-stu-id="1186e-107">The action refers to each record of the [IsolatedComponent table](isolatedcomponent-table.md) and associates the files of the component listed in the Component\_Shared field with the component listed in the Component\_Application field.</span></span> <span data-ttu-id="1186e-108">Le programme d’installation installe les fichiers du composant \_ partagé dans le même répertoire que le composant \_ application.</span><span class="sxs-lookup"><span data-stu-id="1186e-108">The installer installs the files of Component\_Shared into the same directory as Component\_Application.</span></span> <span data-ttu-id="1186e-109">Le programme d’installation génère un fichier dans ce répertoire, avec une longueur de zéro octet, avec le nom de fichier Short du fichier de clé pour l’application de composant \_ (généralement, il s’agit du même nom de fichier que le fichier. exe) ajouté avec. local.</span><span class="sxs-lookup"><span data-stu-id="1186e-109">The installer generates a file in this directory, zero bytes in length, having the short filename name of the key file for Component\_Application (typically this is the same file name as the .exe) appended with .local.</span></span> <span data-ttu-id="1186e-110">L’action IsolatedComponent n’affecte pas l’installation de l' \_ application de composant.</span><span class="sxs-lookup"><span data-stu-id="1186e-110">The IsolatedComponent action does not affect the installation of Component\_Application.</span></span> <span data-ttu-id="1186e-111">La désinstallation \_ de l’application de composant supprime également les \_ fichiers partagés du composant et le fichier. local du répertoire.</span><span class="sxs-lookup"><span data-stu-id="1186e-111">Uninstalling Component\_Application also removes the Component\_Shared files and the .local file from the directory.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="1186e-112">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="1186e-112">Sequence Restrictions</span></span>

<span data-ttu-id="1186e-113">L’action IsolateComponents ne peut être utilisée que dans la [table InstallUISequence](installuisequence-table.md) et la [table InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="1186e-113">The IsolateComponents action can be used only in the [InstallUISequence table](installuisequence-table.md) and the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="1186e-114">Cette action doit être postérieure à l’action [CostInitialize](costinitialize-action.md) et avant l' [action CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="1186e-114">This action must come after the [CostInitialize action](costinitialize-action.md) and before the [CostFinalize action](costfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="1186e-115">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="1186e-115">ActionData Messages</span></span>

<span data-ttu-id="1186e-116">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="1186e-116">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="1186e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="1186e-117">Remarks</span></span>

<span data-ttu-id="1186e-118">Si la colonne condition de l’action IsolateComponents prend la valeur true ou si elle est laissée vide, le programme d’installation isole tous les composants listés dans la [table IsolatedComponent](isolatedcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="1186e-118">If the Condition column for the IsolateComponents action evaluates to True, or is left blank, the installer isolates all the components listed in the [IsolatedComponent table](isolatedcomponent-table.md).</span></span> <span data-ttu-id="1186e-119">Si la colonne condition prend la valeur false, le programme d’installation ignore la table IsolatedComponent et partage les composants normalement.</span><span class="sxs-lookup"><span data-stu-id="1186e-119">If the Condition column evaluates to False, the installer ignores the IsolatedComponent table and shares the components usual.</span></span> <span data-ttu-id="1186e-120">La propriété [**RedirectedDllSupport**](redirecteddllsupport.md) peut être utilisée pour conditionner cette action.</span><span class="sxs-lookup"><span data-stu-id="1186e-120">The [**RedirectedDllSupport**](redirecteddllsupport.md) property may be used to condition this action.</span></span> <span data-ttu-id="1186e-121">Pour plus d’informations, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="1186e-121">For more information, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

 

 



