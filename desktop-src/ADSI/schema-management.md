---
title: Gestion des schémas
description: Le composant fournisseur d’exemples ADSI définit les classes de schéma \ 0034 ; unité d’organisation \ 0034 ; et \ 0034 ; Utilisateur \ 0034 ; et gère ces classes de schéma de la façon suivante.
ms.assetid: c3e07846-a11e-46d4-9863-a89810896ad7
ms.tgt_platform: multiple
keywords:
- Gestion des schémas (ADSI)
- gestion des schémas (ADSI)
- gestion des schémas ADSI
- schémas, gérer ADSI
- gestion d’un schéma ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d398f8eb056498977f886e836c0f97c95f0b9b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104550578"
---
# <a name="schema-management"></a><span data-ttu-id="795f6-108">Gestion des schémas</span><span class="sxs-lookup"><span data-stu-id="795f6-108">Schema Management</span></span>

<span data-ttu-id="795f6-109">Le composant fournisseur d’exemples ADSI définit les classes de schéma « unité d’organisation » et « utilisateur » et gère ces classes de schéma de la façon suivante.</span><span class="sxs-lookup"><span data-stu-id="795f6-109">The ADSI example provider component defines the schema classes "Organizational Unit" and "User" and manages these schema classes in the following way.</span></span>

<span data-ttu-id="795f6-110">La classe de schéma « unité d’organisation » est représentée par un objet conteneur ADs et peut contenir d’autres « unités organisationnelles » et « utilisateurs ».</span><span class="sxs-lookup"><span data-stu-id="795f6-110">The "Organizational Unit" schema class is represented by an ADs container object and can contain other "Organizational Units" and "Users".</span></span> <span data-ttu-id="795f6-111">L’objet conteneur prend en charge les interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)et [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span><span class="sxs-lookup"><span data-stu-id="795f6-111">The container object supports the interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), and [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span></span> <span data-ttu-id="795f6-112">La classe de schéma « User » est représentée par un objet Active Directory générique et ne contient pas d’autres types d’objets.</span><span class="sxs-lookup"><span data-stu-id="795f6-112">The "User" schema class is represented by a generic Active Directory object and does not contain other types of objects.</span></span> <span data-ttu-id="795f6-113">Dans l’exemple de composant fournisseur, l’objet utilisateur est implémenté en tant qu’objet Active Directory générique qui prend en charge les interfaces **IUnknown**, **IDispatch** et **IADs**.</span><span class="sxs-lookup"><span data-stu-id="795f6-113">In the example provider component, the User object is implemented as a generic Active Directory object that supports the interfaces **IUnknown**, **IDispatch**, and **IADs**.</span></span> <span data-ttu-id="795f6-114">N’oubliez pas que l’objet utilisateur, dans ce cas, ne prend pas en charge l’interface [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) .</span><span class="sxs-lookup"><span data-stu-id="795f6-114">Be aware that the User object, in this case, does not support the [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) interface.</span></span>

<span data-ttu-id="795f6-115">L’exemple de composant de fournisseur doit également implémenter l’objet espace de noms ADs, qui prend en charge les interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)et [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span><span class="sxs-lookup"><span data-stu-id="795f6-115">The example provider component must also implement the ADs namespace object, which supports the interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject), and [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span></span>

<span data-ttu-id="795f6-116">L’illustration suivante montre les détails du schéma qui représente les deux exemples de classes de schéma de composant fournisseur.</span><span class="sxs-lookup"><span data-stu-id="795f6-116">The following figure shows the details of the schema that represents the two example provider component schema classes.</span></span>

![schéma du composant fournisseur de l’exemple ADSI](images/dssmsch.png)

<span data-ttu-id="795f6-118">Notez que dans la figure précédente, la classe de schéma « unité d’organisation » définit trois propriétés : « description », « effectifs » et « ID ».</span><span class="sxs-lookup"><span data-stu-id="795f6-118">Be aware that in the preceding figure the "Organizational Unit" schema class defines three properties: "Description," "Headcounts," and "ID."</span></span> <span data-ttu-id="795f6-119">La classe de schéma « User » définit quatre propriétés : « ID », « Name », « PhoneNumber » et « title ».</span><span class="sxs-lookup"><span data-stu-id="795f6-119">The "User" schema class defines four properties: "ID," "Name," "PhoneNumber," and "Title."</span></span> <span data-ttu-id="795f6-120">La propriété « ID » est partagée par les deux classes de schéma.</span><span class="sxs-lookup"><span data-stu-id="795f6-120">The "ID" property is shared by both schema classes.</span></span> <span data-ttu-id="795f6-121">Chaque propriété est définie par l’objet de syntaxe « String » ou « Integer ».</span><span class="sxs-lookup"><span data-stu-id="795f6-121">Each property is defined by either the "String" or the "Integer" syntax object.</span></span>

> [!Note]  
> <span data-ttu-id="795f6-122">Les objets de syntaxe ne sont pas présents dans la première version de l’exemple de composant fournisseur.</span><span class="sxs-lookup"><span data-stu-id="795f6-122">Syntax objects are not present in the first release of the example provider component.</span></span> <span data-ttu-id="795f6-123">Toutefois, dans la plupart des implémentations de schéma Microsoft ADSI, les objets de syntaxe sont inclus dans l’objet de conteneur de schéma, tout comme les objets de classe et de propriété de schéma.</span><span class="sxs-lookup"><span data-stu-id="795f6-123">However, in most Microsoft ADSI schema implementations, the syntax objects are included in the schema container object, just as the schema class and property objects are.</span></span> <span data-ttu-id="795f6-124">Pour cette raison, elles s’affichent ici.</span><span class="sxs-lookup"><span data-stu-id="795f6-124">For this reason, they are shown here.</span></span>

 

<span data-ttu-id="795f6-125">Ce composant de fournisseur rend les données de schéma accessibles à l’application cliente ADSI sous la forme d’objets de classe ADs, d’objets de propriété ADs et d’objets de syntaxe ADs, le tout au sein d’un objet conteneur de classe de schéma, afin que les données de schéma puissent être récupérées au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="795f6-125">This provider component makes schema data accessible to the ADSI client application in the form of ADs class objects, ADs property objects, and ADs syntax objects, all within a schema class container object, so that schema data can be retrieved at run time.</span></span>

<span data-ttu-id="795f6-126">Les ADsPaths pour les objets de conteneur de classe de schéma définis pour le composant de fournisseur d’exemple sont « Sample://Seattle/schema » et « Sample://Toronto/schema ».</span><span class="sxs-lookup"><span data-stu-id="795f6-126">The ADsPaths for the schema class container objects defined for the example provider component are "Sample://Seattle/schema" and "Sample://Toronto/schema".</span></span> <span data-ttu-id="795f6-127">Dans cet exemple, le contenu des schémas est identique.</span><span class="sxs-lookup"><span data-stu-id="795f6-127">In this example, the contents of the schemas are identical.</span></span>

 

 