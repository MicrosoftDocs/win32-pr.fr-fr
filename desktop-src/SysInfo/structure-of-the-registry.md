---
description: Le Registre est une base de données hiérarchique qui contient des données qui sont essentielles au fonctionnement de Windows et aux applications et services qui s’exécutent sur Windows.
ms.assetid: 4ed60563-73d8-4134-8cb2-8388734fb18d
title: Structure du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bf104806b5e4e10b4be7387018e714a0db8bf37
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386668"
---
# <a name="structure-of-the-registry"></a><span data-ttu-id="4efcb-103">Structure du Registre</span><span class="sxs-lookup"><span data-stu-id="4efcb-103">Structure of the Registry</span></span>

<span data-ttu-id="4efcb-104">Le Registre est une base de données hiérarchique qui contient des données qui sont essentielles au fonctionnement de Windows et aux applications et services qui s’exécutent sur Windows.</span><span class="sxs-lookup"><span data-stu-id="4efcb-104">The registry is a hierarchical database that contains data that is critical for the operation of Windows and the applications and services that run on Windows.</span></span> <span data-ttu-id="4efcb-105">Les données sont structurées dans un format d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="4efcb-105">The data is structured in a tree format.</span></span> <span data-ttu-id="4efcb-106">Chaque nœud de l’arborescence est appelé une *clé*.</span><span class="sxs-lookup"><span data-stu-id="4efcb-106">Each node in the tree is called a *key*.</span></span> <span data-ttu-id="4efcb-107">Chaque clé peut contenir à la fois des *sous-clés* et des entrées de données appelées *valeurs*.</span><span class="sxs-lookup"><span data-stu-id="4efcb-107">Each key can contain both *subkeys* and data entries called *values*.</span></span> <span data-ttu-id="4efcb-108">Parfois, la présence d’une clé correspond à toutes les données requises par une application. dans d’autres cas, une application ouvre une clé et utilise les valeurs associées à la clé.</span><span class="sxs-lookup"><span data-stu-id="4efcb-108">Sometimes, the presence of a key is all the data that an application requires; other times, an application opens a key and uses the values associated with the key.</span></span> <span data-ttu-id="4efcb-109">Une clé peut avoir n’importe quel nombre de valeurs, et les valeurs peuvent se présenter sous n’importe quelle forme.</span><span class="sxs-lookup"><span data-stu-id="4efcb-109">A key can have any number of values, and the values can be in any form.</span></span> <span data-ttu-id="4efcb-110">Pour plus d’informations, consultez [types de valeurs de Registre](registry-value-types.md) et limites de taille des [éléments du registre](registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="4efcb-110">For more information, see [Registry Value Types](registry-value-types.md) and [Registry Element Size Limits](registry-element-size-limits.md).</span></span>

<span data-ttu-id="4efcb-111">Chaque clé a un nom constitué d’un ou de plusieurs caractères imprimables.</span><span class="sxs-lookup"><span data-stu-id="4efcb-111">Each key has a name consisting of one or more printable characters.</span></span> <span data-ttu-id="4efcb-112">Les noms de clés ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="4efcb-112">Key names are not case sensitive.</span></span> <span data-ttu-id="4efcb-113">Les noms de clés ne peuvent pas inclure de barre oblique inverse ( \\ ), mais tout autre caractère imprimable peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="4efcb-113">Key names cannot include the backslash character (\\), but any other printable character can be used.</span></span> <span data-ttu-id="4efcb-114">Les noms de valeur et les données peuvent inclure une barre oblique inverse.</span><span class="sxs-lookup"><span data-stu-id="4efcb-114">Value names and data can include the backslash character.</span></span>

<span data-ttu-id="4efcb-115">Le nom de chaque sous-clé est unique en ce qui concerne la clé qui est immédiatement au-dessus de celle-ci dans la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="4efcb-115">The name of each subkey is unique with respect to the key that is immediately above it in the hierarchy.</span></span> <span data-ttu-id="4efcb-116">Les noms de clés ne sont pas localisés dans d’autres langues, bien que les valeurs puissent être.</span><span class="sxs-lookup"><span data-stu-id="4efcb-116">Key names are not localized into other languages, although values may be.</span></span>

<span data-ttu-id="4efcb-117">L’illustration suivante est un exemple de structure de clé de registre telle qu’elle est affichée par l’éditeur du Registre.</span><span class="sxs-lookup"><span data-stu-id="4efcb-117">The following illustration is an example registry key structure as displayed by the Registry Editor.</span></span>

![fenêtre de l’éditeur du Registre](images/regtree.png)

<span data-ttu-id="4efcb-119">Chaque arborescence sous **poste de travail** est une clé.</span><span class="sxs-lookup"><span data-stu-id="4efcb-119">Each of the trees under **My Computer** is a key.</span></span> <span data-ttu-id="4efcb-120">La clé de l' **\_ \_ ordinateur local HKEY** possède les sous-clés suivantes : **Hardware**, **Sam**, **Security**, **Software** et **System**.</span><span class="sxs-lookup"><span data-stu-id="4efcb-120">The **HKEY\_LOCAL\_MACHINE** key has the following subkeys: **HARDWARE**, **SAM**, **SECURITY**, **SOFTWARE**, and **SYSTEM**.</span></span> <span data-ttu-id="4efcb-121">Chacune de ces clés a des sous-clés.</span><span class="sxs-lookup"><span data-stu-id="4efcb-121">Each of these keys in turn has subkeys.</span></span> <span data-ttu-id="4efcb-122">Par exemple, la clé **matérielle** a les sous-clés **Description**, **DEVICEMAP** et **RESOURCEMAP**; la clé **DEVICEMAP** a plusieurs sous-clés, y compris la **vidéo**.</span><span class="sxs-lookup"><span data-stu-id="4efcb-122">For example, the **HARDWARE** key has the subkeys **DESCRIPTION**, **DEVICEMAP**, and **RESOURCEMAP**; the **DEVICEMAP** key has several subkeys including **VIDEO**.</span></span>

<span data-ttu-id="4efcb-123">Chaque valeur se compose d’un nom de valeur et de ses données associées, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="4efcb-123">Each value consists of a value name and its associated data, if any.</span></span> <span data-ttu-id="4efcb-124">**MaxObjectNumber** et **VgaCompatible** sont des valeurs qui contiennent des données sous la sous-clé **Video** .</span><span class="sxs-lookup"><span data-stu-id="4efcb-124">**MaxObjectNumber** and **VgaCompatible** are values that contain data under the **VIDEO** subkey.</span></span>

<span data-ttu-id="4efcb-125">Une arborescence du Registre peut avoir 512 niveaux de profondeur.</span><span class="sxs-lookup"><span data-stu-id="4efcb-125">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="4efcb-126">Vous pouvez créer jusqu’à 32 niveaux à la fois à l’aide d’un appel d’API de Registre unique.</span><span class="sxs-lookup"><span data-stu-id="4efcb-126">You can create up to 32 levels at a time through a single registry API call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4efcb-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4efcb-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4efcb-128">[Vue d’ensemble du Registre Windows](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="4efcb-128">[Overview of the Windows Registry](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))</span></span>
</dt> </dl>

 

 
