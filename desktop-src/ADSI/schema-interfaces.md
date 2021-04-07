---
title: Interfaces de schéma
description: Interfaces de schéma
ms.assetid: b3427202-352b-4b35-877e-d28fb3d3906a
ms.tgt_platform: multiple
keywords:
- interfaces ADSI des interfaces de schéma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f414fdea2418fb92a0a3c8c9e8bf88eb6d7f00b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939581"
---
# <a name="schema-interfaces"></a><span data-ttu-id="4e0aa-104">Interfaces de schéma</span><span class="sxs-lookup"><span data-stu-id="4e0aa-104">Schema Interfaces</span></span>

<span data-ttu-id="4e0aa-105">Le conteneur de schéma contient un ensemble de définitions de schéma qui sont attachées à une partie de l’arborescence d’espace de noms du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4e0aa-105">The schema container contains a set of schema definitions that are attached to part of the namespace tree of the provider.</span></span> <span data-ttu-id="4e0aa-106">En règle générale, chaque instance d’un espace de noms a son propre schéma.</span><span class="sxs-lookup"><span data-stu-id="4e0aa-106">Typically, each instance of a namespace has its own schema.</span></span> <span data-ttu-id="4e0aa-107">Par exemple, dans l’illustration suivante, l’exemple de fournisseur ADSI définit un conteneur de schéma dans chacun des nœuds racine « Seattle » et « Toronto ».</span><span class="sxs-lookup"><span data-stu-id="4e0aa-107">For example, in the following figure, the ADSI example provider defines a schema container in each of the root nodes "Seattle" and "Toronto".</span></span>

![relation contenant-contenu de schéma](images/schemacont.png)

<span data-ttu-id="4e0aa-109">Pour créer une implémentation ADSI pour un fournisseur, vous devez fournir des objets de gestion de schéma qui reflètent l’espace de noms sous-jacent du fournisseur et qui prennent en charge les interfaces de schéma ADSI.</span><span class="sxs-lookup"><span data-stu-id="4e0aa-109">To create an ADSI implementation for a provider, you need to supply schema management objects that reflect the underlying namespace of the provider and which support ADSI schema interfaces.</span></span> <span data-ttu-id="4e0aa-110">La liste suivante répertorie les interfaces de schéma ADSI qui sont contenues dans le conteneur de schéma.</span><span class="sxs-lookup"><span data-stu-id="4e0aa-110">The following is a list of the ADSI schema interfaces, which are contained in the schema container.</span></span>

-   <span data-ttu-id="4e0aa-111">[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) représente des classes de service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="4e0aa-111">[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) represents directory service classes.</span></span>
-   <span data-ttu-id="4e0aa-112">[**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) représente les propriétés du service d’annuaire qui ont une ou plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="4e0aa-112">[**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) represents directory service properties that have single or multiple values.</span></span>
-   <span data-ttu-id="4e0aa-113">[**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) représente le type Variant unique.</span><span class="sxs-lookup"><span data-stu-id="4e0aa-113">[**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) represents the single VARIANT type.</span></span>

<span data-ttu-id="4e0aa-114">Les interfaces définies par ADSI peuvent prendre en charge des propriétés spécifiques et des syntaxes pour votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4e0aa-114">Interfaces defined by ADSI can support specific properties and syntaxes for your provider.</span></span> <span data-ttu-id="4e0aa-115">Les fournisseurs peuvent choisir d’étendre une définition ADSI à l’aide des méthodes qui créent et accèdent aux propriétés, par exemple, vous pouvez utiliser les méthodes de l’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) , telles que [**obtenir**](/windows/desktop/api/Iads/nf-iads-iads-get), [**GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**put**](/windows/desktop/api/Iads/nf-iads-iads-put) [**et.**](/windows/desktop/api/Iads/nf-iads-iads-putex)</span><span class="sxs-lookup"><span data-stu-id="4e0aa-115">Providers can choose to extend an ADSI definition by using the methods that create and access properties, for example, you can use the methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface such as [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex).</span></span> <span data-ttu-id="4e0aa-116">Les fournisseurs peuvent également prendre en charge des propriétés supplémentaires via des interfaces supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4e0aa-116">Providers can also support additional properties through additional interfaces.</span></span> <span data-ttu-id="4e0aa-117">Pour obtenir la liste complète des interfaces ADSI, consultez [interfaces ADSI](adsi-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="4e0aa-117">For a complete list of ADSI interfaces, see [ADSI Interfaces](adsi-interfaces.md).</span></span>

<span data-ttu-id="4e0aa-118">Un composant fournisseur ADSI avec un espace de noms complexe peut permettre l’existence de plusieurs schémas dans une instance d’espace de noms, chacun d’entre eux ayant une autre partie de l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="4e0aa-118">An ADSI provider component with a complex namespace might allow multiple schemas to exist in a namespace instance, each at a different part of the tree.</span></span> <span data-ttu-id="4e0aa-119">Toutefois, la propriété [**IADs :: Schema**](iads-property-methods.md) d’un objet nomme toujours sa propre définition de schéma.</span><span class="sxs-lookup"><span data-stu-id="4e0aa-119">The [**IADs::Schema**](iads-property-methods.md) property of an object, however, always names its own schema definition.</span></span>

 

 




