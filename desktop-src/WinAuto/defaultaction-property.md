---
title: DefaultAction, propriété
description: La propriété DefaultAction d’un objet décrit la méthode principale de manipulation de l’objet à partir du point de vue de l’utilisateur. La propriété DefaultAction d’un objet doit être un verbe ou une expression verbale abrégée.
ms.assetid: 8242c0af-b42e-44a4-8807-d6740fa1a24a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc032037c331a2022f227cb8e8547dd8bce9d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309465"
---
# <a name="defaultaction-property"></a><span data-ttu-id="c5529-104">DefaultAction, propriété</span><span class="sxs-lookup"><span data-stu-id="c5529-104">DefaultAction Property</span></span>

<span data-ttu-id="c5529-105">La propriété **DefaultAction** d’un objet décrit la méthode principale de manipulation de l’objet à partir du point de vue de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c5529-105">An object's **DefaultAction** property describes the object's primary method of manipulation from the user's viewpoint.</span></span> <span data-ttu-id="c5529-106">La propriété **DefaultAction** d’un objet doit être un verbe ou une expression verbale abrégée.</span><span class="sxs-lookup"><span data-stu-id="c5529-106">An object's **DefaultAction** property should be a verb or a short verb phrase.</span></span>

<span data-ttu-id="c5529-107">La propriété **DefaultAction** est récupérée en appelant [**IAccessible :: \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction).</span><span class="sxs-lookup"><span data-stu-id="c5529-107">The **DefaultAction** property is retrieved by calling [**IAccessible::get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction).</span></span>

<span data-ttu-id="c5529-108">Pour exécuter l’action par défaut d’un objet, les clients appellent [**IAccessible :: accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction).</span><span class="sxs-lookup"><span data-stu-id="c5529-108">To perform an object's default action, clients call [**IAccessible::accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction).</span></span>

<span data-ttu-id="c5529-109">Certains objets n’ont pas d’actions par défaut, et certains objets ont une action par défaut associée à sa propriété [**value**](value-property.md) , comme dans les exemples suivants :</span><span class="sxs-lookup"><span data-stu-id="c5529-109">Not all objects have default actions, and some objects have a default action that is related to its [**Value**](value-property.md) property, such as in the following examples:</span></span>

-   <span data-ttu-id="c5529-110">Une case à cocher activée a une action par défaut « décocher » et une valeur « activé ».</span><span class="sxs-lookup"><span data-stu-id="c5529-110">A selected check box has a default action of "Uncheck" and a value of "Checked."</span></span>
-   <span data-ttu-id="c5529-111">Une case à cocher désactivée a une action par défaut « vérifier » et une valeur « désactivée ».</span><span class="sxs-lookup"><span data-stu-id="c5529-111">A cleared check box has a default action of "Check" and a value of "Unchecked."</span></span>
-   <span data-ttu-id="c5529-112">Un bouton intitulé « Print » a une action par défaut « Press », sans valeur.</span><span class="sxs-lookup"><span data-stu-id="c5529-112">A button labeled "Print" has a default action of "Press," with no value.</span></span>
-   <span data-ttu-id="c5529-113">Un contrôle de texte statique ou un contrôle d’édition qui affiche « Printer » n’a pas d’action par défaut, mais a la valeur « Printer ».</span><span class="sxs-lookup"><span data-stu-id="c5529-113">A static text control or an edit control that shows "Printer" has no default action, but has a value of "Printer."</span></span>

 

 




