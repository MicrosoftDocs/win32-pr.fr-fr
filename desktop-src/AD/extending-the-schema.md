---
title: Extension du schéma
description: Le schéma de service Active Directory Directory définit les attributs et les classes utilisés dans Active Directory Domain Services.
ms.assetid: 1c7c1fa7-56d9-4b2d-9c48-aa10464064bc
ms.tgt_platform: multiple
keywords:
- Active Directory, utilisation de, schéma, extension du schéma
- schéma AD, extension du schéma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c03d57468fb5275c55ce0d725a2decd7cfbf0f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "106510456"
---
# <a name="extending-the-schema"></a><span data-ttu-id="1ca83-105">Extension du schéma</span><span class="sxs-lookup"><span data-stu-id="1ca83-105">Extending the Schema</span></span>

<span data-ttu-id="1ca83-106">Le schéma de service Active Directory Directory définit les attributs et les classes utilisés dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="1ca83-106">The Active Directory directory service schema defines the attributes and classes used in Active Directory Domain Services.</span></span> <span data-ttu-id="1ca83-107">Le schéma de base inclus dans le système contient un ensemble complet de définitions de classe, telles que **User**, **Computer** et **OrganizationalUnit**, ainsi que des définitions d’attributs, telles que **userPrincipalName**, **telephoneNumber** et **objectSID**.</span><span class="sxs-lookup"><span data-stu-id="1ca83-107">The base schema that is included the system contains a rich set of class definitions, such as **user**, **computer**, and **organizationalUnit**, and attribute definitions, such as **userPrincipalName**, **telephoneNumber**, and **objectSid**.</span></span> <span data-ttu-id="1ca83-108">L’ensemble existant de classes et d’attributs sera suffisant pour la plupart des applications.</span><span class="sxs-lookup"><span data-stu-id="1ca83-108">The existing set of classes and attributes will be sufficient for most applications.</span></span> <span data-ttu-id="1ca83-109">Toutefois, le schéma est extensible, ce qui signifie que vous pouvez définir de nouvelles classes et attributs.</span><span class="sxs-lookup"><span data-stu-id="1ca83-109">However, the schema is extensible, which means that you can define new classes and attributes.</span></span> <span data-ttu-id="1ca83-110">Cette section explique comment étendre le schéma Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1ca83-110">This section discusses how to extend the Active Directory schema.</span></span>

## <a name="when-to-extend-the-schema"></a><span data-ttu-id="1ca83-111">Quand étendre le schéma</span><span class="sxs-lookup"><span data-stu-id="1ca83-111">When to Extend the Schema</span></span>

<span data-ttu-id="1ca83-112">Si les classes et les attributs existants ne correspondent pas au type de données que vous souhaitez stocker, vous devez étendre le schéma.</span><span class="sxs-lookup"><span data-stu-id="1ca83-112">If the existing classes and attributes do not fit with the type of data you want to store, you should extend the schema.</span></span> <span data-ttu-id="1ca83-113">Il est important de noter que les ajouts de schéma sont permanents ; vous pouvez désactiver des classes et des attributs, mais vous ne pouvez jamais les supprimer du schéma.</span><span class="sxs-lookup"><span data-stu-id="1ca83-113">It is important to note that schema additions are permanent; you can disable classes and attributes, but you can never remove them from the schema.</span></span> <span data-ttu-id="1ca83-114">Gardez cela à l’esprit lorsque vous testez du code.</span><span class="sxs-lookup"><span data-stu-id="1ca83-114">Keep this in mind when you are testing code.</span></span>

<span data-ttu-id="1ca83-115">Tenez également compte de la taille des données que vous souhaitez stocker.</span><span class="sxs-lookup"><span data-stu-id="1ca83-115">Also consider the size of the data that you want to store.</span></span> <span data-ttu-id="1ca83-116">Microsoft recommande qu’aucune valeur d’attribut ne dépasse 500 kilo-octets, y compris la somme des attributs à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="1ca83-116">Microsoft recommends that no attribute value exceed 500 kilobytes, including the sum of multivalued attributes.</span></span> <span data-ttu-id="1ca83-117">En outre, la taille des objets ne doit pas dépasser 1 Mo.</span><span class="sxs-lookup"><span data-stu-id="1ca83-117">Also, objects should not exceed 1 megabyte in size.</span></span> <span data-ttu-id="1ca83-118">Tenez également compte du nombre d’instances des données ; Si vous ajoutez un nouvel attribut à la classe [**utilisateur**](/windows/desktop/ADSchema/c-user) sur un système qui a 100 000 utilisateurs, cela peut consommer un espace considérable.</span><span class="sxs-lookup"><span data-stu-id="1ca83-118">Consider also the number of instances of the data; if you add a new attribute to the [**User**](/windows/desktop/ADSchema/c-user) class on a system that has 100,000 users, this can use up considerable space.</span></span>

<span data-ttu-id="1ca83-119">Les rubriques de cette section sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1ca83-119">Topics in this section include:</span></span>

-   <span data-ttu-id="1ca83-120">Comment effectuer une liaison au conteneur de schéma et lire les propriétés des classes et attributs existants.</span><span class="sxs-lookup"><span data-stu-id="1ca83-120">How to bind to the schema container and read the properties of existing classes and attributes.</span></span>
-   <span data-ttu-id="1ca83-121">Comment et quand étendre le schéma en définissant de nouveaux attributs et classes.</span><span class="sxs-lookup"><span data-stu-id="1ca83-121">How and when to extend the schema by defining new attributes and classes.</span></span>
-   <span data-ttu-id="1ca83-122">Comment installer des extensions de schéma à l’aide de LDIFDE, CSVDE ou par programmation avec ADSI.</span><span class="sxs-lookup"><span data-stu-id="1ca83-122">How to install schema extensions using LDIFDE, CSVDE, or programmatically with ADSI.</span></span>

<span data-ttu-id="1ca83-123">Pour plus d’informations et pour obtenir une vue d’ensemble du schéma Active Directory, y compris des informations sur l’implémentation de schéma, les définitions de classe et les définitions d’attributs, consultez [Active Directory schéma](active-directory-schema.md).</span><span class="sxs-lookup"><span data-stu-id="1ca83-123">For more information and an overview of the Active Directory schema, including information about the schema implementation, class definitions, and attribute definitions, see [Active Directory Schema](active-directory-schema.md).</span></span>

<span data-ttu-id="1ca83-124">Pour plus d’informations, notamment des pages de référence pour les classes de schéma prédéfinies, les attributs et les syntaxes d’attribut, consultez la référence de schéma Active Directory dans la [référence de Active Directory Domain Services](active-directory-domain-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="1ca83-124">For more information, including reference pages for the predefined schema classes, attributes, and attribute syntaxes, see the Active Directory Schema Reference in the [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span></span>

 

 