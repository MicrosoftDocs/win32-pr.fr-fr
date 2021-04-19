---
title: Nommer des classes et des attributs
description: Cette rubrique contient des instructions pour nommer des attributs et des classes.
ms.assetid: ccbc2859-332f-4ded-9125-5bf507cad960
ms.tgt_platform: multiple
keywords:
- Nommer des classes et des attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bfd2614033e12f68ba2727cc7aec689c16071e
ms.sourcegitcommit: 02e6e0b58720bf6b77797dd7a9ddc11c95f42b33
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "106511110"
---
# <a name="naming-attributes-and-classes"></a><span data-ttu-id="829a7-104">Nommer des classes et des attributs</span><span class="sxs-lookup"><span data-stu-id="829a7-104">Naming Attributes and Classes</span></span>

<span data-ttu-id="829a7-105">Cette rubrique contient des instructions pour nommer des attributs et des classes.</span><span class="sxs-lookup"><span data-stu-id="829a7-105">This topic includes guidelines for naming attributes and classes.</span></span>

<span data-ttu-id="829a7-106">Pour créer une classe ou un attribut, respectez les règles d’affectation de noms suivantes :</span><span class="sxs-lookup"><span data-stu-id="829a7-106">To create a new class or attribute, adhere to the following naming rules:</span></span>

-   <span data-ttu-id="829a7-107">Utilisez le même nom pour les propriétés **CN** et **lDAPDisplayName** d’un nouvel objet **attributeSchema** ou **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="829a7-107">Use the same name for both the **cn** and **lDAPDisplayName** properties of a new **attributeSchema** or **classSchema** object.</span></span>
-   <span data-ttu-id="829a7-108">Identifiez la société avec un préfixe en minuscules dans la première section du nom.</span><span class="sxs-lookup"><span data-stu-id="829a7-108">Identify the company with a lower-case prefix in the first section of the name.</span></span> <span data-ttu-id="829a7-109">Ce préfixe peut être un nom DNS, un acronyme ou toute autre chaîne qui identifie de façon unique l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="829a7-109">This prefix can be a DNS name, acronym, or other string that uniquely identifies the company.</span></span> <span data-ttu-id="829a7-110">Le préfixe garantit que tous les attributs et classes d’une société spécifique s’affichent consécutivement lors de la navigation dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="829a7-110">The prefix ensures that all attributes and classes for a specific company are displayed consecutively when browsing the schema.</span></span>
-   <span data-ttu-id="829a7-111">Si vous développez une extension de schéma en tant que fournisseur de logiciels indépendant, ajoutez une abréviation du nom de produit du préfixe.</span><span class="sxs-lookup"><span data-stu-id="829a7-111">If you are developing a schema extension as an independent software vendor, add an abbreviation of the product name of the prefix.</span></span> <span data-ttu-id="829a7-112">Cela permet d’ajouter une distinction entre plusieurs produits qui contiennent des extensions de schéma LDAP.</span><span class="sxs-lookup"><span data-stu-id="829a7-112">This adds distinction between multiple products that contain LDAP schema extensions.</span></span>
-   <span data-ttu-id="829a7-113">Utilisez un trait d’Union comme caractère suivant après le préfixe.</span><span class="sxs-lookup"><span data-stu-id="829a7-113">Use a hyphen as the next character after the prefix.</span></span>
-   <span data-ttu-id="829a7-114">Spécifiez un attribut ou un nom de classe qui est unique dans les attributs de la société après le trait d’Union.</span><span class="sxs-lookup"><span data-stu-id="829a7-114">Specify an attribute or class name that is unique within the company's attributes after the hyphen.</span></span> <span data-ttu-id="829a7-115">Cette partie du nom commun doit être descriptive.</span><span class="sxs-lookup"><span data-stu-id="829a7-115">This part of the common-name should be descriptive.</span></span> <span data-ttu-id="829a7-116">N’utilisez pas de noms illogique qui n’ont pas de sens pour les développeurs et les observateurs du schéma.</span><span class="sxs-lookup"><span data-stu-id="829a7-116">Do not use illogical names that are meaningless to developers and viewers of the schema.</span></span>

<span data-ttu-id="829a7-117">Par exemple, si la société fictive Fabrikam a étendu le schéma en ajoutant un attribut pour stocker un identificateur de courrier vocal, le nom **commun** et le **lDAPDisplayName** du nouvel attribut peuvent être « Fabrikam-VoiceMailID ».</span><span class="sxs-lookup"><span data-stu-id="829a7-117">For example, if the fictitious Fabrikam company extended the schema by adding an attribute for storing a voice-mail identifier, the **cn** and **lDAPDisplayName** of the new attribute could be "fabrikam-VoiceMailID".</span></span>

<span data-ttu-id="829a7-118">Si le **lDAPDisplayName** d’un attribut ou d’une classe n’est pas spécifié, le système utilise le **CN** pour en générer un.</span><span class="sxs-lookup"><span data-stu-id="829a7-118">If the **lDAPDisplayName** of an attribute or class is not specified, the system uses the **cn** to generate one.</span></span> <span data-ttu-id="829a7-119">Toutefois, l’algorithme système utilisé pour générer le nom peut entraîner des collisions de noms ou des noms difficiles à lire.</span><span class="sxs-lookup"><span data-stu-id="829a7-119">However, the system algorithm for generating the name may result in name collisions or names that are difficult to read.</span></span> <span data-ttu-id="829a7-120">Pour éviter ces problèmes, il est recommandé de spécifier explicitement **lDAPDisplayName** pour tous les attributs et les classes.</span><span class="sxs-lookup"><span data-stu-id="829a7-120">To avoid these problems, it is recommended that an **lDAPDisplayName** be explicitly specified for all attributes and classes.</span></span>

<span data-ttu-id="829a7-121">À des fins de développement et de test, il peut être souhaitable d’ajouter un suffixe de version au **CN** et à **lDAPDisplayName**, par exemple, « Fabrikam-VoiceMailID-001 ».</span><span class="sxs-lookup"><span data-stu-id="829a7-121">For development and testing purposes, it may be desirable to append a version suffix to the **cn** and **lDAPDisplayName**, for example, "fabrikam-VoiceMailID-001".</span></span> <span data-ttu-id="829a7-122">Dans un environnement de développement/test distribué, un suffixe de version permet aux développeurs d’exécuter simultanément plusieurs versions de leurs logiciels.</span><span class="sxs-lookup"><span data-stu-id="829a7-122">In a distributed development/test environment, a version suffix enables developers to run multiple versions of their software simultaneously.</span></span> <span data-ttu-id="829a7-123">Une fois le test terminé, renommez l’attribut ou la classe pour supprimer le suffixe.</span><span class="sxs-lookup"><span data-stu-id="829a7-123">After testing is complete, rename the attribute or class to remove the suffix.</span></span>

<span data-ttu-id="829a7-124">Il n’est pas possible de supprimer les versions obsolètes d’extensions de schéma, mais il est possible de les désactiver et de les renommer avec des noms obscurs.</span><span class="sxs-lookup"><span data-stu-id="829a7-124">It is not possible to delete defunct versions of a schema extensions, but it is possible to disable them and rename them with obscure names.</span></span> <span data-ttu-id="829a7-125">Pour plus d’informations, consultez [désactivation des classes et attributs existants](disabling-existing-classes-and-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="829a7-125">For more information, see [Disabling Existing Classes and Attributes](disabling-existing-classes-and-attributes.md).</span></span>

 

 




