---
title: Attributs Single et multiple value
description: Les attributs qui peuvent exister dans un répertoire sont généralement définis dans le schéma de l’annuaire.
ms.assetid: ea06ca66-6407-448f-8238-c8de5353663b
ms.tgt_platform: multiple
keywords:
- les attributs de valeur unique ou multiple sont des attributs ADSI
- attributs ADSI, valeurs uniques et attributs à valeurs multiples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfabd985be3446e4f104d300d75f891ef0ce60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028547"
---
# <a name="single-vs-multiple-value-attributes"></a><span data-ttu-id="31331-105">Attributs Single et multiple value</span><span class="sxs-lookup"><span data-stu-id="31331-105">Single vs. Multiple Value Attributes</span></span>

<span data-ttu-id="31331-106">Les attributs qui peuvent exister dans un répertoire sont généralement définis dans le schéma de l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="31331-106">The attributes that can exist in a directory are typically defined in the schema for the directory.</span></span> <span data-ttu-id="31331-107">La définition de schéma d’un attribut spécifie un certain nombre de caractéristiques de l’attribut, telles que le type de données et si une instance de l’attribut peut avoir plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="31331-107">The schema definition of an attribute specifies a number of characteristics of the attribute, such as the data type and whether an instance of the attribute can have multiple values.</span></span>

<span data-ttu-id="31331-108">Une instance d’un attribut à valeur unique peut contenir une seule valeur.</span><span class="sxs-lookup"><span data-stu-id="31331-108">An instance of a single-valued attribute can contain a single value.</span></span> <span data-ttu-id="31331-109">Une instance d’un attribut à valeurs multiples peut contenir une ou plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="31331-109">An instance of a multivalued attribute can contain either a single value or multiple values.</span></span> <span data-ttu-id="31331-110">Active Directory ne crée pas d’attributs avec des valeurs vides, soit l’attribut contient une valeur valide, soit il n’existe pas sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="31331-110">Active Directory does not create attributes with empty values—either the attribute contains a valid value or it does not exist on the object.</span></span>

> [!Note]  
> <span data-ttu-id="31331-111">Dans Active Directory et la plupart des autres serveurs LDAP, l’ordre des valeurs dans un attribut à valeurs multiples n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="31331-111">In Active Directory and most other LDAP servers, the order of values in a multi-valued attribute is undefined.</span></span> <span data-ttu-id="31331-112">En outre, chaque valeur d’un attribut à valeurs multiples doit être unique.</span><span class="sxs-lookup"><span data-stu-id="31331-112">Also, each value of a multi-valued attribute must be unique.</span></span>

 

<span data-ttu-id="31331-113">ADSI charge normalement les données de schéma si votre annuaire prend en charge un schéma, comme le fait Active Directory.</span><span class="sxs-lookup"><span data-stu-id="31331-113">ADSI normally loads schema data if your directory supports a schema, as Active Directory does.</span></span> <span data-ttu-id="31331-114">ADSI connaissant la syntaxe des attributs du schéma, vous n’êtes pas obligé de spécifier le type d’attribut lors de l’accès à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="31331-114">Because ADSI knows the syntax of attributes in the schema, you are not required to specify the attribute type when accessing it.</span></span> <span data-ttu-id="31331-115">ADSI marshale les valeurs d’attribut vers le type de données approprié, tel que défini dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="31331-115">ADSI marshals attribute values to the appropriate data type as defined in the schema.</span></span>

<span data-ttu-id="31331-116">Si votre répertoire n’a pas de schéma, fournissez le type de données lors de l’accès à un attribut.</span><span class="sxs-lookup"><span data-stu-id="31331-116">If your directory has no schema, supply the data type when accessing an attribute.</span></span>

> [!Note]  
> <span data-ttu-id="31331-117">Active Directory, Exchange, Windows NT 4,0 et le serveur de site ont tous un schéma.</span><span class="sxs-lookup"><span data-stu-id="31331-117">Active Directory, Exchange, Windows NT 4.0, and Site Server all have a schema.</span></span> <span data-ttu-id="31331-118">En outre, Active Directory a un schéma extensible.</span><span class="sxs-lookup"><span data-stu-id="31331-118">In addition, Active Directory has an extensible schema.</span></span>

 

 

 




