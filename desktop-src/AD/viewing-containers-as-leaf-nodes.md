---
title: Affichage des conteneurs en tant que nœuds terminaux
description: Tout objet dans Active Directory Domain Services peut être un conteneur d’autres objets.
ms.assetid: 38300ca5-745a-4640-9723-6052a9843f45
ms.tgt_platform: multiple
keywords:
- Affichage des conteneurs en tant que nœuds terminaux
- conteneurs Active Directory, afficher en tant que nœuds terminaux
- feuille Active Directory, affichage des conteneurs en tant que nœuds terminaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1631526ed78132829a7576960a997b13cc232b5f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314598"
---
# <a name="viewing-containers-as-leaf-nodes"></a><span data-ttu-id="491af-106">Affichage des conteneurs en tant que nœuds terminaux</span><span class="sxs-lookup"><span data-stu-id="491af-106">Viewing Containers as Leaf Nodes</span></span>

<span data-ttu-id="491af-107">Tout objet dans Active Directory Domain Services peut être un conteneur d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="491af-107">Any object in Active Directory Domain Services can be a container of other objects.</span></span> <span data-ttu-id="491af-108">Cela peut encombrer l’interface utilisateur. il est donc possible de déclarer qu’un objet d’une classe spécifique ne doit être affiché qu’en tant que feuille dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="491af-108">This can clutter the user interface, so it is possible to declare that an object of a specific class be only be displayed as a leaf in the user interface.</span></span> <span data-ttu-id="491af-109">L’attribut **treatAsLeaf** est un attribut spécificateur d’affichage à valeur unique qui détermine si les objets de cette classe doivent être affichés uniquement en tant qu’objets feuille.</span><span class="sxs-lookup"><span data-stu-id="491af-109">The **treatAsLeaf** attribute is a single-valued display specifier attribute that determines if objects of that class should be only be displayed as leaf objects.</span></span> <span data-ttu-id="491af-110">Cet attribut est une valeur booléenne qui, si la **valeur est true**, indique que les objets de la classe doivent être affichés uniquement en tant qu’éléments feuille.</span><span class="sxs-lookup"><span data-stu-id="491af-110">This attribute is a Boolean value that, if **TRUE**, indicates that objects of the class should only be displayed as leaf elements.</span></span> <span data-ttu-id="491af-111">Si la **valeur est false**, indique que les objets de la classe peuvent être affichés sous la forme d’un conteneur ou d’une feuille.</span><span class="sxs-lookup"><span data-stu-id="491af-111">If **FALSE**, indicates that objects of the class can be displayed as a container or a leaf.</span></span> <span data-ttu-id="491af-112">Comme tous les attributs de spécificateur d’affichage, l’attribut **treatAsLeaf** est défini par paramètres régionaux. cet attribut peut donc être localisé en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="491af-112">Like all display specifier attributes, the **treatAsLeaf** attribute is set on a per-locale basis, so this attribute can be localized as required.</span></span> <span data-ttu-id="491af-113">Par exemple, l’attribut **treatAsLeaf** **du spécificateur d’affichage de paramètres** régionaux anglais (0409) est défini sur **true** par défaut.</span><span class="sxs-lookup"><span data-stu-id="491af-113">For example, the **User-Display** for the English locale (0409) display specifier has the **treatAsLeaf** attribute set to **TRUE** by default.</span></span> <span data-ttu-id="491af-114">Ainsi, l’interface utilisateur affiche tous les objets **utilisateur** en tant qu’objets feuille.</span><span class="sxs-lookup"><span data-stu-id="491af-114">This causes the user interface to display all **User** objects as leaf objects.</span></span>

<span data-ttu-id="491af-115">\*\*Pour définir la valeur de l’attribut \*\*treatAsLeaf\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="491af-115">**To set the value of the **treatAsLeaf** attribute**</span></span>

1.  <span data-ttu-id="491af-116">Établissez une liaison avec l’attribut d’affichage souhaité dans les paramètres régionaux souhaités.</span><span class="sxs-lookup"><span data-stu-id="491af-116">Bind to the desired display attribute in the desired locale.</span></span> <span data-ttu-id="491af-117">Pour plus d’informations et pour obtenir un exemple de code, consultez [conteneur DisplaySpecifiers](displayspecifiers-container.md).</span><span class="sxs-lookup"><span data-stu-id="491af-117">For more information and a code example, see [DisplaySpecifiers Container](displayspecifiers-container.md).</span></span>
2.  <span data-ttu-id="491af-118">Utilisez la [**méthode IADs ::P ut**](/windows/desktop/api/iads/nf-iads-iads-put) pour affecter la valeur **true** ou **false** à l’attribut **treatAsLeaf** .</span><span class="sxs-lookup"><span data-stu-id="491af-118">Use the [**IADs::Put**](/windows/desktop/api/iads/nf-iads-iads-put) method to set the **treatAsLeaf** attribute to either **TRUE** or **FALSE**.</span></span>
3.  <span data-ttu-id="491af-119">Pour valider les modifications apportées à l’annuaire, appelez la méthode [**IADs :: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="491af-119">To commit changes to the directory, call the [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) method.</span></span>

 

 