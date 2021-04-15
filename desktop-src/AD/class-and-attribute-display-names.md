---
title: Noms complets des classes et des attributs
description: Cette rubrique contient des informations et des instructions pour les noms d’affichage des classes et des attributs.
ms.assetid: c85905b2-ed8b-4032-8c54-fd4de8b34ecf
ms.tgt_platform: multiple
keywords:
- spécificateurs d’affichage noms d’affichage AD, de classe et d’attribut
- noms complets des classes AD
- noms d’affichage des attributs AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d65cd6ac6fc3077ff0d2bba15ffa9904b147654
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462922"
---
# <a name="class-and-attribute-display-names"></a><span data-ttu-id="4aa72-106">Noms complets des classes et des attributs</span><span class="sxs-lookup"><span data-stu-id="4aa72-106">Class and Attribute Display Names</span></span>

<span data-ttu-id="4aa72-107">Le spécificateur d’affichage d’une classe d’objet contient les attributs suivants qui peuvent être utilisés pour spécifier les noms d’affichage localisés utilisés dans l’interface utilisateur pour les objets de cette classe :</span><span class="sxs-lookup"><span data-stu-id="4aa72-107">The display specifier for an object class contains the following attributes that can be used to specify the localized display names used in the UI for objects of that class:</span></span>

-   <span data-ttu-id="4aa72-108">L’attribut **classDisplayName** est une chaîne Unicode à valeur unique qui spécifie le nom complet de la classe.</span><span class="sxs-lookup"><span data-stu-id="4aa72-108">The **classDisplayName** attribute is a single-value Unicode string that specifies the class display name.</span></span>
-   <span data-ttu-id="4aa72-109">L’attribut **attributeDisplayNames** est une propriété à valeurs multiples qui spécifie les noms à utiliser dans l’interface utilisateur pour les attributs de la classe d’objet.</span><span class="sxs-lookup"><span data-stu-id="4aa72-109">The **attributeDisplayNames** attribute is a multi-value property that specifies the names to use in the UI for attributes of the object class.</span></span>

<span data-ttu-id="4aa72-110">Les valeurs **attributeDisplayNames** sont des chaînes Unicode ; chaque élément se compose d’une paire de noms délimitée par des virgules :</span><span class="sxs-lookup"><span data-stu-id="4aa72-110">The **attributeDisplayNames** values are Unicode strings; each element consists of a comma-delimited name pair:</span></span>


```C++
<attribute name>,<display text>
```



<span data-ttu-id="4aa72-111">Dans cet exemple, « &lt; nom &gt; d’attribut » est le **lDAPDisplayName** de l’attribut et « &lt; texte affiché &gt; » est le texte à afficher comme nom de cet attribut dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4aa72-111">In this example, "&lt;attribute name&gt;" is the **lDAPDisplayName** of the attribute and "&lt;display text&gt;" is the text to display as the name of that attribute in the user interface.</span></span>

## <a name="guidelines-for-class-and-attribute-display-names"></a><span data-ttu-id="4aa72-112">Instructions pour les noms d’affichage de classes et d’attributs</span><span class="sxs-lookup"><span data-stu-id="4aa72-112">Guidelines for Class and Attribute Display Names</span></span>

<span data-ttu-id="4aa72-113">Étant donné que de nombreux fournisseurs peuvent étendre des classes avec de nouveaux attributs ou créer des classes entièrement nouvelles, il est important que les noms complets de la classe et de l’attribut ne soient pas ambigus et n’entraînent pas de conflits.</span><span class="sxs-lookup"><span data-stu-id="4aa72-113">Because many vendors may extend classes with new attributes or creating entirely new classes, it is important that the class and attribute display names are unambiguous and do not result in conflicts.</span></span>

<span data-ttu-id="4aa72-114">Chaque fournisseur doit préfixer le nom complet de la classe avec un identificateur convivial unique basé sur le nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4aa72-114">Each vendor should prefix the class display name with a unique friendly identifier based on the vendor name.</span></span> <span data-ttu-id="4aa72-115">Par exemple, si la société fictive Fabrikam Inc., crée une nouvelle classe dérivée de la classe « contact », elle peut avoir un nom d’affichage de classe unique « Fabrikam contact ».</span><span class="sxs-lookup"><span data-stu-id="4aa72-115">For example, if the fictitious company, Fabrikam Inc., creates a new class derived from the "contact" class, they can have a unique class display name "Fabrikam Contact."</span></span>

<span data-ttu-id="4aa72-116">Si un fournisseur étend une classe existante avec de nouveaux attributs, il doit de nouveau identifier de manière unique le nom complet de l’attribut afin qu’aucun conflit ne se produise avec d’autres noms d’affichage d’attribut.</span><span class="sxs-lookup"><span data-stu-id="4aa72-116">If a vendor extends an existing class with new attributes, they should again uniquely identify the attribute display name so that no conflicts occur with other attribute display names.</span></span> <span data-ttu-id="4aa72-117">Là encore, le fait de préfixer le nom d’affichage de l’attribut avec un identificateur convivial unique basé sur le nom du fournisseur est une bonne pratique.</span><span class="sxs-lookup"><span data-stu-id="4aa72-117">Again, prefixing the attribute display name with unique friendly identifier based on the vendor name is good practice.</span></span> <span data-ttu-id="4aa72-118">Par exemple, si la société Fabrikam étend la classe utilisateur avec un nouvel attribut RH, elle peut afficher de manière unique l’attribut « informations sur les RH fabrikam ».</span><span class="sxs-lookup"><span data-stu-id="4aa72-118">For example, if the Fabrikam company extends the user class with a new HR attribute, they could uniquely display the attribute as "Fabrikam HR Information."</span></span>

<span data-ttu-id="4aa72-119">En outre, du point de vue de la localisation, chaque fournisseur doit localiser les noms d’affichage des classes et des attributs dans chaque langue prise en charge par Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4aa72-119">In addition, from a localization perspective, each vendor should localize the class and attribute display names into each language supported by Windows 2000.</span></span>

## <a name="adding-a-value-to-the-attributedisplaynames-attribute"></a><span data-ttu-id="4aa72-120">Ajout d’une valeur à l’attribut attributeDisplayNames</span><span class="sxs-lookup"><span data-stu-id="4aa72-120">Adding a Value to the attributeDisplayNames Attribute</span></span>

<span data-ttu-id="4aa72-121">\*\*Pour ajouter une valeur de mappage de nom à l’attribut \*\*attributeDisplayNames\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4aa72-121">**To add a name mapping value to the **attributeDisplayNames** attribute**</span></span>

1.  <span data-ttu-id="4aa72-122">Déterminez si la valeur de mappage de nom de l’attribut existe.</span><span class="sxs-lookup"><span data-stu-id="4aa72-122">Determine if the name mapping value for the attribute exists.</span></span> <span data-ttu-id="4aa72-123">Si une valeur de mappage de nom doit être remplacée, supprimez d’abord la valeur existante, à l’aide de la méthode [**IADs ::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) , avec le paramètre *LnControlCode* défini sur **publicités \_ Property \_ Delete** et le paramètre *vProp* défini sur la valeur à supprimer.</span><span class="sxs-lookup"><span data-stu-id="4aa72-123">If a name mapping value is to be replaced, first deleted the existing value, using the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method, with the *lnControlCode* parameter set to **ADS\_PROPERTY\_DELETE** and the *vProp* parameter set to the value to be removed.</span></span> <span data-ttu-id="4aa72-124">N’utilisez pas **les \_ Propriétés ad \_ Clear** ou **ADS \_ Property \_ Update** pour *lnControlCode*.</span><span class="sxs-lookup"><span data-stu-id="4aa72-124">Do not use **ADS\_PROPERTY\_CLEAR** or **ADS\_PROPERTY\_UPDATE** for *lnControlCode*.</span></span>
2.  <span data-ttu-id="4aa72-125">Créez la chaîne qui représente le nom complet de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="4aa72-125">Create the string that represents the attribute display name.</span></span> <span data-ttu-id="4aa72-126">Pour obtenir un exemple, consultez le format ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="4aa72-126">For an example, see the format above.</span></span>
3.  <span data-ttu-id="4aa72-127">Utilisez la méthode [**IADs ::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) avec le paramètre *LnControlCode* défini sur **publicité \_ propriété \_ Append** pour ajouter la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="4aa72-127">Use the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method with the *lnControlCode* parameter set to **ADS\_PROPERTY\_APPEND** to add the new value.</span></span>
4.  <span data-ttu-id="4aa72-128">Appelez [**IADs :: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) pour valider les modifications apportées au répertoire.</span><span class="sxs-lookup"><span data-stu-id="4aa72-128">Call [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the changes to the directory.</span></span>

<span data-ttu-id="4aa72-129">Pour plus d’informations sur l’affectation de noms aux nouvelles classes et attributs, consultez [Naming Attributes and classes](naming-attributes-and-classes.md).</span><span class="sxs-lookup"><span data-stu-id="4aa72-129">For more information about naming new classes and attributes, see [Naming Attributes and Classes](naming-attributes-and-classes.md).</span></span>

 

 