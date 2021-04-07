---
title: Désactivation des classes et attributs existants
description: Les ajouts de schéma sont permanents.
ms.assetid: 13ffd2f5-cf1d-4cde-a3d5-74cb5a44b6fc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74863d0d3c72f383259cfe262f4b7aa6fa27774a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671342"
---
# <a name="disabling-existing-classes-and-attributes"></a><span data-ttu-id="89487-103">Désactivation des classes et attributs existants</span><span class="sxs-lookup"><span data-stu-id="89487-103">Disabling Existing Classes and Attributes</span></span>

<span data-ttu-id="89487-104">Les ajouts de schéma sont permanents.</span><span class="sxs-lookup"><span data-stu-id="89487-104">Schema additions are permanent.</span></span> <span data-ttu-id="89487-105">Vous ne pouvez pas supprimer les objets **attributeSchema** et **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="89487-105">You cannot delete **attributeSchema** and **classSchema** objects.</span></span> <span data-ttu-id="89487-106">Dans un système distribué, il est difficile de garantir qu’il n’y a pas d’instance d’une classe ou d’un attribut donné.</span><span class="sxs-lookup"><span data-stu-id="89487-106">In a distributed system, it is difficult to guarantee that there are no instances of a given class or attribute.</span></span> <span data-ttu-id="89487-107">La suppression de la définition d’une classe ou d’un attribut endommage les instances existantes de cette classe ou de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="89487-107">Removing the definition of a class or attribute damages existing instances of that class or attribute.</span></span>

<span data-ttu-id="89487-108">Vous pouvez désactiver une classe ou un attribut existant en le marquant comme « défunt ».</span><span class="sxs-lookup"><span data-stu-id="89487-108">You can disable an existing class or attribute by marking it as "defunct".</span></span> <span data-ttu-id="89487-109">Cela n’affecte pas les instances existantes de la classe ou de l’attribut, ainsi marqué, mais empêche la création de nouvelles instances.</span><span class="sxs-lookup"><span data-stu-id="89487-109">This does not affect existing instances of the class or attribute so marked, but it prevents the creation of new instances.</span></span>

<span data-ttu-id="89487-110">Les restrictions suivantes s’appliquent lors de la désactivation des classes de schéma et des attributs :</span><span class="sxs-lookup"><span data-stu-id="89487-110">The following restrictions apply when disabling schema classes and attributes:</span></span>

-   <span data-ttu-id="89487-111">Vous ne pouvez pas désactiver une classe ou un attribut Category 1.</span><span class="sxs-lookup"><span data-stu-id="89487-111">You cannot disable a Category 1 class or attribute.</span></span>
-   <span data-ttu-id="89487-112">Vous ne pouvez pas désactiver un attribut qui est membre d’une classe qui n’est pas également désactivée.</span><span class="sxs-lookup"><span data-stu-id="89487-112">You cannot disable an attribute that is a member of a class that is not also disabled.</span></span> <span data-ttu-id="89487-113">Cela est dû au fait qu’un attribut peut être requis pour la classe (non désactivé) et que la désactivation de l’attribut empêche la création de nouvelles instances de la classe.</span><span class="sxs-lookup"><span data-stu-id="89487-113">This is because an attribute might be required for the (not disabled) class, and disabling the attribute prevents new instances of the class from being created.</span></span>

<span data-ttu-id="89487-114">Pour désactiver un attribut, affectez à l’attribut **IsDefunct** de son objet **attributeSchema** la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="89487-114">To disable an attribute, set the **isDefunct** attribute of its **attributeSchema** object to **TRUE**.</span></span> <span data-ttu-id="89487-115">Lorsqu’un attribut est désactivé, il n’est pas possible de créer de nouvelles instances de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="89487-115">When an attribute is disabled, new instances of the attribute cannot be created.</span></span> <span data-ttu-id="89487-116">Pour réactiver l’attribut, affectez la valeur **false** à l’attribut **IsDefunct** .</span><span class="sxs-lookup"><span data-stu-id="89487-116">To re-enable the attribute set the **isDefunct** attribute to **FALSE**.</span></span>

<span data-ttu-id="89487-117">Pour désactiver une classe, affectez à l’attribut **IsDefunct** de son objet **classSchema** la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="89487-117">To disable a class, set the **isDefunct** attribute of its **classSchema** object to **TRUE**.</span></span> <span data-ttu-id="89487-118">Lorsqu’une classe est désactivée, les nouvelles instances de la classe ne peuvent pas être créées.</span><span class="sxs-lookup"><span data-stu-id="89487-118">When a class is disabled, new instances of the class cannot be created.</span></span> <span data-ttu-id="89487-119">Pour réactiver la classe, affectez à l’attribut **IsDefunct** la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="89487-119">To re-enable the class set the **isDefunct** attribute to **FALSE**.</span></span>

<span data-ttu-id="89487-120">La définition des objets de schéma comme défunts peut être utile dans les environnements de production.</span><span class="sxs-lookup"><span data-stu-id="89487-120">Setting schema objects as defunct can be useful in production environments.</span></span> <span data-ttu-id="89487-121">Lorsqu’une version de test d’une extension de schéma n’est plus nécessaire, marquez-la comme défunt.</span><span class="sxs-lookup"><span data-stu-id="89487-121">When a test version of a schema extension is no longer required, mark it as defunct.</span></span> <span data-ttu-id="89487-122">Vous pouvez la restaurer en supprimant l’attribut **IsDefunct** ou en affectant à la valeur de l’attribut la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="89487-122">You can restore it by removing the **isDefunct** attribute or setting the attribute value to **FALSE**.</span></span> <span data-ttu-id="89487-123">Cela protège également contre la suppression involontaire d’un objet de schéma en le définissant sur défunt, car l’opération peut être facilement inversée.</span><span class="sxs-lookup"><span data-stu-id="89487-123">This also protects against an unintended removal of a schema object by setting it to defunct because the operation can be easily reversed.</span></span>

<span data-ttu-id="89487-124">N’oubliez pas que le serveur Active Directory ne nettoie pas les instances existantes d’un attribut ou d’une classe lorsque vous rendez un objet de schéma défunt.</span><span class="sxs-lookup"><span data-stu-id="89487-124">Be aware that the Active Directory server does not clean up existing instances of an attribute or class when you make a schema object defunct.</span></span> <span data-ttu-id="89487-125">Si vous supprimez la propriété **IsDefunct** , toutes les instances deviennent valides et les objets normaux.</span><span class="sxs-lookup"><span data-stu-id="89487-125">If you remove the **isDefunct** property, any instances become valid, normal objects again.</span></span>

<span data-ttu-id="89487-126">La liste suivante comprend d’autres conséquences du marquage d’un objet **attributeSchema** ou **classSchema** défunt :</span><span class="sxs-lookup"><span data-stu-id="89487-126">The following list includes other consequences of marking an **attributeSchema** or **classSchema** object defunct:</span></span>

-   <span data-ttu-id="89487-127">L’ajout ou la modification d’une instance échoue.</span><span class="sxs-lookup"><span data-stu-id="89487-127">Addition or modification of an instance fails.</span></span>
-   <span data-ttu-id="89487-128">Les codes d’erreur se comportent comme si une classe défunte n’existait jamais.</span><span class="sxs-lookup"><span data-stu-id="89487-128">Error codes behave as if a defunct class never existed.</span></span>
-   <span data-ttu-id="89487-129">La recherche et la suppression se comportent comme si aucun objet de schéma n’avait été rendu obsolète.</span><span class="sxs-lookup"><span data-stu-id="89487-129">Search and delete behave as if no schema objects have been made defunct.</span></span>
-   <span data-ttu-id="89487-130">Autorise uniquement la suppression de l’attribut entier de l’objet.</span><span class="sxs-lookup"><span data-stu-id="89487-130">Only allow deleting entire attribute from object.</span></span>

<span data-ttu-id="89487-131">La liste suivante comprend des options supplémentaires dans un environnement de production pour réduire l’impact des extensions de schéma obsolètes :</span><span class="sxs-lookup"><span data-stu-id="89487-131">The following list includes additional options in a production environment for reducing the impact of defunct schema extensions:</span></span>

-   <span data-ttu-id="89487-132">Supprimez toutes les valeurs d’attribut **mayHave** d’une classe défunte.</span><span class="sxs-lookup"><span data-stu-id="89487-132">Remove all **mayHave** attribute values from a defunct class.</span></span>
-   <span data-ttu-id="89487-133">Réduisez la taille de toutes les valeurs d’attribut **musthave** d’une classe défunte.</span><span class="sxs-lookup"><span data-stu-id="89487-133">Reduce the size of all **mustHave** attribute values from a defunct class.</span></span>
-   <span data-ttu-id="89487-134">Supprimer un attribut défunt du catalogue global.</span><span class="sxs-lookup"><span data-stu-id="89487-134">Remove a defunct attribute from the global catalog.</span></span>
-   <span data-ttu-id="89487-135">Supprimer un attribut défunt de n’importe quel index.</span><span class="sxs-lookup"><span data-stu-id="89487-135">Remove a defunct attribute from any index.</span></span>

<span data-ttu-id="89487-136">D’autres options de suppression des modifications de schéma indésirables dans un environnement de production sont destinées aux développeurs qui utilisent un contrôleur de domaine privé pour le test.</span><span class="sxs-lookup"><span data-stu-id="89487-136">Other options for removing unwanted schema changes in a production environment are for developers to use a private domain controller for testing.</span></span> <span data-ttu-id="89487-137">Dans ce cas, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="89487-137">In this case, you can:</span></span>

-   <span data-ttu-id="89487-138">« Réinitialisez » le serveur Active Directory en utilisant Dcpromo.exe pour rétrograder le contrôleur de périphérique.</span><span class="sxs-lookup"><span data-stu-id="89487-138">"Reset" the Active Directory server by using Dcpromo.exe to demote the DC.</span></span> <span data-ttu-id="89487-139">Une fois la rétrogradation terminée, utilisez Dcpromo.exe à nouveau pour réactiver le serveur sur un contrôleur de périphérique.</span><span class="sxs-lookup"><span data-stu-id="89487-139">After the demote completes, use Dcpromo.exe again to promote the server back to a DC.</span></span> <span data-ttu-id="89487-140">Le développeur peut ensuite utiliser des scripts LDIF pour recharger les classes, les attributs et les instances d’objet requis.</span><span class="sxs-lookup"><span data-stu-id="89487-140">The developer can then use LDIF scripts to reload any required classes, attributes, and object instances.</span></span>
-   <span data-ttu-id="89487-141">Utilisez Ntbackup.exe pour effectuer une sauvegarde de l’état du système sur une partition de disque disponible.</span><span class="sxs-lookup"><span data-stu-id="89487-141">Use Ntbackup.exe to perform a system-state backup to an available disk partition.</span></span> <span data-ttu-id="89487-142">Redémarrez le mode de restauration du service d’annuaire sécurisé/sécurisé.</span><span class="sxs-lookup"><span data-stu-id="89487-142">Reboot to Safe/Directory Service Restore mode to restore.</span></span>

<span data-ttu-id="89487-143">Pour les systèmes d’exploitation Windows Server 2003, lorsque vous définissez une classe ou un attribut sur défunt, vous pouvez réutiliser immédiatement les valeurs **ldapDisplayName**, **schemaIDGUID**, **OID** et **mapiId** de l’élément de schéma défunt lorsque vous créez une classe ou un attribut pour le remplacer.</span><span class="sxs-lookup"><span data-stu-id="89487-143">For Windows Server 2003 operating systems, when you set a class or attribute to defunct, you can immediately reuse the **ldapDisplayName**, **schemaIdGuid**, **OID** and **mapiID** values of the defunct schema element when you create a new class or attribute to replace it.</span></span> <span data-ttu-id="89487-144">La version défunte de la classe ou de l’attribut est conservée dans le conteneur de schéma, mais elle est masquée dans le composant logiciel enfichable MMC.</span><span class="sxs-lookup"><span data-stu-id="89487-144">The defunct version of the class or attribute is maintained in the Schema container, but it is hidden in the MMC snap-in.</span></span> <span data-ttu-id="89487-145">Pour réactiver l’ancien élément de schéma, affectez la valeur **false** à **IsDefunct** .</span><span class="sxs-lookup"><span data-stu-id="89487-145">To reactivate the old schema element, set **isDefunct** to **FALSE**.</span></span>

<span data-ttu-id="89487-146">L’exemple de code LDIF suivant montre comment modifier l’attribut **IsDefunct** et modifier le RDN afin qu’il ne soit pas confondu avec la nouvelle classe que vous créez pour le remplacer.</span><span class="sxs-lookup"><span data-stu-id="89487-146">The following LDIF code example shows how to modify the **isDefunct** attribute and change the RDN so that it is not confused with the new class that you create to replace it.</span></span>

``` syntax
 dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modify
   replace: isDefunct
   isDefunct: TRUE
   -

   dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modrdn
   newrdn: cn=MyClassOld
   deleteoldrdn: 1

   dn:
   changetype: modify
   add: schemaUpdateNow
   schemaUpdateNow: 1
   -
```

<span data-ttu-id="89487-147">Utilisez la commande suivante pour exécuter l’exemple de code LDIF sur une forêt pour un ordinateur s’exécutant sur des systèmes d’exploitation Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="89487-147">Use the following command to run the LDIF code example against a forest for a computer running on Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="89487-148">**ldifde/i/f RDN. ldf/c "DC = X" "DC = MyDomain, DC = com"**</span><span class="sxs-lookup"><span data-stu-id="89487-148">**ldifde /i /f rdn.ldf /c "DC=X" "dc=mydomain,dc=com"**</span></span>

<span data-ttu-id="89487-149">(Où « DC = X » est une constante)</span><span class="sxs-lookup"><span data-stu-id="89487-149">(Where "DC=X" is a constant)</span></span>

 

 




