---
description: Le qualificateur de clé indique si la propriété fait partie du handle d’espace de noms.
ms.assetid: 838d295f-e812-4e46-99a4-d2714a0ae8dc
ms.tgt_platform: multiple
title: Qualificateur de clé
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Key
api_type:
- NA
api_location: ''
ms.openlocfilehash: affc9f4be594723700a65c9c92f8ae37ffead265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758325"
---
# <a name="key-qualifier"></a><span data-ttu-id="45820-103">Qualificateur de clé</span><span class="sxs-lookup"><span data-stu-id="45820-103">Key Qualifier</span></span>

<span data-ttu-id="45820-104">Le qualificateur de **clé** indique si la propriété fait partie du handle d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="45820-104">The **Key** qualifier indicates whether the property is part of the namespace handle.</span></span> <span data-ttu-id="45820-105">Si plusieurs propriétés ont le qualificateur de **clé** , toutes ces propriétés forment collectivement la clé (une clé composée).</span><span class="sxs-lookup"><span data-stu-id="45820-105">If more than one property has the **Key** qualifier, then all such properties collectively form the key (a compound key).</span></span> <span data-ttu-id="45820-106">Lorsqu’elles sont prises en compte, les propriétés de clé doivent fournir une référence unique pour chaque instance de classe.</span><span class="sxs-lookup"><span data-stu-id="45820-106">When taken together, the key properties must supply a unique reference for each class instance.</span></span> <span data-ttu-id="45820-107">Si ce qualificateur est placé sur une propriété, seule la valeur **true** est autorisée.</span><span class="sxs-lookup"><span data-stu-id="45820-107">If this qualifier is placed on a property, only the value **TRUE** is allowed.</span></span>

<span data-ttu-id="45820-108">Vous pouvez utiliser n’importe quel type de propriété, à l’exception des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="45820-108">You can use any property type except for the following:</span></span>

-   <span data-ttu-id="45820-109">Tableaux</span><span class="sxs-lookup"><span data-stu-id="45820-109">Arrays</span></span>
-   <span data-ttu-id="45820-110">Nombres réels et à virgule flottante</span><span class="sxs-lookup"><span data-stu-id="45820-110">Real and floating-point numbers</span></span>
-   <span data-ttu-id="45820-111">Objets incorporés</span><span class="sxs-lookup"><span data-stu-id="45820-111">Embedded objects</span></span>
-   <span data-ttu-id="45820-112">Caractères inférieurs à ASCII 32 (autrement dit, les caractères d’espace blanc)</span><span class="sxs-lookup"><span data-stu-id="45820-112">Characters lower than ASCII 32 (that is, white space characters)</span></span>
-   <span data-ttu-id="45820-113">Les chaînes de caractères de type **char16** ou les chaînes de caractères définies en tant que clés doivent contenir des valeurs supérieures à U + 0020.</span><span class="sxs-lookup"><span data-stu-id="45820-113">Character strings of type **char16** or character strings that are defined as keys must contain values greater than U+0020.</span></span> <span data-ttu-id="45820-114">Cela est dû au fait que WMI utilise des valeurs de clés dans les chemins d’accès aux objets et que vous ne pouvez pas utiliser de caractères non imprimables dans un chemin d’accès à un objet.</span><span class="sxs-lookup"><span data-stu-id="45820-114">This is because WMI uses key values in object paths, and you cannot use nonprinting characters in an object path.</span></span>

<span data-ttu-id="45820-115">Quand une classe parente spécifie une clé, toutes les classes dérivées de la classe parente héritent de cette clé.</span><span class="sxs-lookup"><span data-stu-id="45820-115">When a parent class specifies a key, all classes derived from the parent class inherit that key.</span></span> <span data-ttu-id="45820-116">Les classes dérivées ne peuvent pas modifier la clé héritée ou définir une nouvelle propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="45820-116">The derived classes cannot alter the inherited key or define any new key property.</span></span> <span data-ttu-id="45820-117">Toutefois, lorsque vous dérivez une sous-classe d’une classe abstraite sans clé, vous pouvez introduire une clé dans la sous-classe.</span><span class="sxs-lookup"><span data-stu-id="45820-117">However, when you derive a subclass from an abstract class without a key, you can introduce a key in the subclass.</span></span>

<span data-ttu-id="45820-118">Toutes les classes qui définissent plus d’une instance doivent spécifier une clé.</span><span class="sxs-lookup"><span data-stu-id="45820-118">All classes that define more than one instance must specify a key.</span></span> <span data-ttu-id="45820-119">Étant donné que les classes abstraites ne définissent pas d’instances, elles n’ont pas besoin de spécifier des clés.</span><span class="sxs-lookup"><span data-stu-id="45820-119">Because abstract classes do not define any instances, they do not need to specify keys.</span></span> <span data-ttu-id="45820-120">Étant donné que les classes Singleton ne définissent qu’une seule instance, elles ne peuvent pas spécifier de clés.</span><span class="sxs-lookup"><span data-stu-id="45820-120">Because singleton classes define only one instance, they cannot specify keys.</span></span>

<span data-ttu-id="45820-121">Les clés sont écrites une fois à l’instanciation de l’objet et ne doivent pas être modifiées ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="45820-121">Keys are written one time at object instantiation and must not be modified later.</span></span> <span data-ttu-id="45820-122">Il n’est pas judicieux d’appliquer une valeur par défaut à une propriété qualifiée de clé.</span><span class="sxs-lookup"><span data-stu-id="45820-122">It does not make sense to apply a default value to a key-qualified property.</span></span>

## <a name="requirements"></a><span data-ttu-id="45820-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45820-123">Requirements</span></span>



| <span data-ttu-id="45820-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45820-124">Requirement</span></span> | <span data-ttu-id="45820-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="45820-125">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="45820-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45820-126">Minimum supported client</span></span><br/> | <span data-ttu-id="45820-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45820-127">Windows Vista</span></span><br/>       |
| <span data-ttu-id="45820-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45820-128">Minimum supported server</span></span><br/> | <span data-ttu-id="45820-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45820-129">Windows Server 2008</span></span><br/> |



 

 




