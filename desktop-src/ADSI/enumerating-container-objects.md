---
title: Énumération des objets conteneurs
description: Par Convention, tous les éléments d’une énumération dans ADSI doivent être du même type de données Automation. Par exemple, une énumération ne doit pas retourner certains éléments sous la forme d’une variante de type VT \_ I4 et d’autres en tant que variante de type VT \_ BSTR.
ms.assetid: 155caa67-05db-432b-b813-0d891a502301
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5514596b02521fa869ffd7c712dcac2cacb40192
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106526519"
---
# <a name="enumerating-container-objects"></a><span data-ttu-id="341e9-104">Énumération des objets conteneurs</span><span class="sxs-lookup"><span data-stu-id="341e9-104">Enumerating Container Objects</span></span>

<span data-ttu-id="341e9-105">Par Convention, tous les éléments d’une énumération dans ADSI doivent être du même type de données Automation.</span><span class="sxs-lookup"><span data-stu-id="341e9-105">By convention, all items in an enumeration in ADSI must be of the same Automation data type.</span></span> <span data-ttu-id="341e9-106">Par exemple, une énumération ne doit pas retourner certains éléments sous la forme d’une **variante** de type **VT \_ I4** et d’autres en tant que **variante** de type **VT \_ BSTR**.</span><span class="sxs-lookup"><span data-stu-id="341e9-106">For example, an enumeration should not return some items as a **VARIANT** of type **VT\_I4** and others as a **VARIANT** of type **VT\_BSTR**.</span></span>

<span data-ttu-id="341e9-107">Pour énumérer une liste d’éléments gérés par un objet, un client demande la création d’un objet d’énumération pour le type spécifique d’informations qui sont répertoriées.</span><span class="sxs-lookup"><span data-stu-id="341e9-107">To enumerate a list of items that an object maintains, a client requests the creation of an enumeration object for the specific type of information being listed.</span></span> <span data-ttu-id="341e9-108">Dans ADSI, le client peut répertorier les objets dans les objets d’espace de noms, les objets conteneurs génériques, les objets de collection, les objets membres ou les objets de schéma.</span><span class="sxs-lookup"><span data-stu-id="341e9-108">In ADSI, the client may list the objects in namespace objects, generic container objects, collection objects, member objects, or schema objects.</span></span> <span data-ttu-id="341e9-109">L’interface ADSI fournit un filtre qui peut être défini et modifié pour limiter les correspondances dans toute énumération par le biais de la propriété [**IADsContainer. Filter**](iadscontainer-property-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="341e9-109">ADSI provides a filter that can be set and modified to limit the matches in any enumeration though the [**IADsContainer.Filter**](iadscontainer-property-methods.md) property.</span></span> <span data-ttu-id="341e9-110">Des exemples d’implémentations d’objets Enumerator se trouvent dans l’exemple de code du composant fournisseur pour les objets conteneur ADs suivants.</span><span class="sxs-lookup"><span data-stu-id="341e9-110">Examples of implementations of enumerator objects can be found in the example provider component code for the following ADs container objects.</span></span>



| <span data-ttu-id="341e9-111">Type d'objet</span><span class="sxs-lookup"><span data-stu-id="341e9-111">Object type</span></span>         | <span data-ttu-id="341e9-112">code</span><span class="sxs-lookup"><span data-stu-id="341e9-112">code</span></span>         |
|---------------------|--------------|
| <span data-ttu-id="341e9-113">Conteneur générique</span><span class="sxs-lookup"><span data-stu-id="341e9-113">Generic Container</span></span>   | <span data-ttu-id="341e9-114">cenumobj. cpp</span><span class="sxs-lookup"><span data-stu-id="341e9-114">cenumobj.cpp</span></span> |
| <span data-ttu-id="341e9-115">Conteneur d’espace de noms</span><span class="sxs-lookup"><span data-stu-id="341e9-115">Namespace Container</span></span> | <span data-ttu-id="341e9-116">cenumns. cpp</span><span class="sxs-lookup"><span data-stu-id="341e9-116">cenumns.cpp</span></span>  |
| <span data-ttu-id="341e9-117">Conteneur de schéma</span><span class="sxs-lookup"><span data-stu-id="341e9-117">Schema Container</span></span>    | <span data-ttu-id="341e9-118">cenumsch. cpp</span><span class="sxs-lookup"><span data-stu-id="341e9-118">cenumsch.cpp</span></span> |



 

<span data-ttu-id="341e9-119">Pour plus d’informations côté client, consultez [collections et groupes](collections-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="341e9-119">For client-side information, see [Collections and Groups](collections-and-groups.md).</span></span>

 

 




