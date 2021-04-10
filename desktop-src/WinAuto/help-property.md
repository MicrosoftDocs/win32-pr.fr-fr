---
title: Help, propriété
description: La propriété Help fournit des informations qui indiquent à l’utilisateur la fonction d’un objet.
ms.assetid: 3df0cc01-cc99-42a1-9d56-591e6e00e53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b240475d4583826e08fd6ee43b5839bdfb451d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309902"
---
# <a name="help-property"></a><span data-ttu-id="474bf-103">Help, propriété</span><span class="sxs-lookup"><span data-stu-id="474bf-103">Help Property</span></span>

<span data-ttu-id="474bf-104">La propriété **Help** fournit des informations qui indiquent à l’utilisateur la fonction d’un objet.</span><span class="sxs-lookup"><span data-stu-id="474bf-104">The **Help** property provides information that tells the user about the function of an object.</span></span>

<span data-ttu-id="474bf-105">La propriété **Help** est récupérée en appelant [**IAccessible :: obtenir \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp).</span><span class="sxs-lookup"><span data-stu-id="474bf-105">The **Help** property is retrieved by calling [**IAccessible::get\_accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp).</span></span>

<span data-ttu-id="474bf-106">Cette propriété contient des informations de style Balloon (telles qu’elles figurent dans les info-bulles) utilisées pour décrire ce que fait l’objet ou comment l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="474bf-106">This property contains balloon-style information (as found in ToolTips) that is used either to describe what the object does or how to use it.</span></span> <span data-ttu-id="474bf-107">Par exemple, la propriété d' **aide** d’un bouton de barre d’outils qui affiche une imprimante peut fournir le texte suivant : « imprime le document actif ».</span><span class="sxs-lookup"><span data-stu-id="474bf-107">For example, the **Help** property for a toolbar button that shows a printer might provide the following text: "Prints the current document."</span></span>

<span data-ttu-id="474bf-108">Le texte de la propriété **d’aide** n’a pas besoin d’être unique au sein de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="474bf-108">The text for the **Help** property does not have to be unique within the user interface.</span></span>

## <a name="when-to-support-the-help-property"></a><span data-ttu-id="474bf-109">Quand prendre en charge la propriété d’aide</span><span class="sxs-lookup"><span data-stu-id="474bf-109">When to Support the Help Property</span></span>

<span data-ttu-id="474bf-110">Les serveurs ne prennent pas en charge la propriété **d’aide** si d’autres propriétés fournissent des informations suffisantes sur le rôle de l’objet et les actions effectuées par l’objet.</span><span class="sxs-lookup"><span data-stu-id="474bf-110">Servers do not support the **Help** property if other properties provide sufficient information about the object's purpose and the actions the object performs.</span></span> <span data-ttu-id="474bf-111">Les objets accessibles qui exposent des contrôles fournis par le système ne prennent pas en charge la propriété **Help** .</span><span class="sxs-lookup"><span data-stu-id="474bf-111">Accessible objects that expose system-provided controls do not support the **Help** property.</span></span>

 

 




