---
title: Modification des interfaces utilisateur existantes
description: Le volet des résultats du composant logiciel enfichable MMC Active Directory utilisateurs et ordinateurs affiche plusieurs colonnes de données d’attribut pour les objets d’un conteneur, comme les attributs nom et description.
ms.assetid: 55f4ae82-c380-42a9-beba-047ffd0131eb
ms.tgt_platform: multiple
keywords:
- Modification des interfaces utilisateur existantes Active Directory
- AD du composant logiciel enfichable utilisateurs et ordinateurs, modification de l’affichage
- Composant logiciel enfichable utilisateurs et ordinateurs Active Directory, ajout de colonnes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0765988a9ceed3e98966091ad94b868b96fd88
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839290"
---
# <a name="modifying-existing-user-interfaces"></a><span data-ttu-id="aa53e-106">Modification des interfaces utilisateur existantes</span><span class="sxs-lookup"><span data-stu-id="aa53e-106">Modifying Existing User Interfaces</span></span>

<span data-ttu-id="aa53e-107">Le volet des résultats du composant logiciel enfichable MMC Active Directory utilisateurs et ordinateurs affiche plusieurs colonnes de données d’attribut pour les objets d’un conteneur, comme les attributs **nom** et **Description** .</span><span class="sxs-lookup"><span data-stu-id="aa53e-107">The results pane of the Active Directory Users and Computers MMC snap-in displays several columns of attribute data for objects within a container, such as the **Name** and **Description** attributes.</span></span> <span data-ttu-id="aa53e-108">Le composant logiciel enfichable permet à l’utilisateur d’ajouter et de supprimer les colonnes affichées dans le volet de résultats du composant logiciel enfichable.</span><span class="sxs-lookup"><span data-stu-id="aa53e-108">The snap-in enables the user to add and remove the columns displayed in the results pane of the snap-in.</span></span>

<span data-ttu-id="aa53e-109">Pour modifier l’affichage, l’utilisateur utilise le menu déroulant **vue** et sélectionne **Ajouter/supprimer des colonnes**.</span><span class="sxs-lookup"><span data-stu-id="aa53e-109">To change the display, the user uses the **View** pull-down menu and selects **Add/Remove Columns**.</span></span> <span data-ttu-id="aa53e-110">Dans la boîte de dialogue **Ajouter/supprimer des colonnes** , il existe une liste de colonnes dans laquelle l’utilisateur peut choisir de s’afficher dans le volet des résultats.</span><span class="sxs-lookup"><span data-stu-id="aa53e-110">In the **Add/Remove Columns** dialog box, there is a list of columns that the user can choose from to display in the results pane.</span></span>

<span data-ttu-id="aa53e-111">Le composant logiciel enfichable MMC utilisateurs et ordinateurs Active Directory inclus avec Windows Server 2003, Standard Edition, Windows Server 2003, Enterprise Edition et Windows Server 2003, Datacenter Edition, offre la possibilité de modifier la liste des colonnes qui peuvent être affichées dans le volet des résultats du composant logiciel enfichable pour un conteneur.</span><span class="sxs-lookup"><span data-stu-id="aa53e-111">The Active Directory Users and Computers MMC snap-in that is included with Windows Server 2003, Standard Edition, Windows Server 2003, Enterprise Edition, and Windows Server 2003, Datacenter Edition, provides the ability to modify the list of columns that can be displayed in the results pane of the snap-in for a container.</span></span> <span data-ttu-id="aa53e-112">Cette fonctionnalité existe uniquement si le composant logiciel enfichable est ciblé sur une forêt avec le schéma Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="aa53e-112">This feature only exists if the snap-in is targeted at a forest with Windows Server 2003 schema.</span></span>

<span data-ttu-id="aa53e-113">Pour ajouter une colonne à la liste, ajoutez une valeur à l’attribut **extraColumns** du spécificateur d’affichage du type d’objet auquel l’attribut est associé.</span><span class="sxs-lookup"><span data-stu-id="aa53e-113">To add a column to the list, add a value to the **extraColumns** attribute of the display specifier for the object type that the attribute is associated with.</span></span> <span data-ttu-id="aa53e-114">L’attribut **extraColumns** est un attribut de chaîne à valeurs multiples dans lequel chaque chaîne est au format suivant.</span><span class="sxs-lookup"><span data-stu-id="aa53e-114">The **extraColumns** attribute is a multi-valued string attribute where each string is in the following format.</span></span>


```C++

<ldapdisplayname>,<column header>,<default visibility>,<width>,<unused>

```



<span data-ttu-id="aa53e-115">Le tableau suivant répertorie le contenu de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="aa53e-115">The following table lists the contents of these values.</span></span>



| <span data-ttu-id="aa53e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa53e-116">Value</span></span>                        | <span data-ttu-id="aa53e-117">Description</span><span class="sxs-lookup"><span data-stu-id="aa53e-117">Description</span></span>                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa53e-118">« &lt; ldapDisplayName &gt; »</span><span class="sxs-lookup"><span data-stu-id="aa53e-118">"&lt;ldapdisplayname&gt;"</span></span>    | <span data-ttu-id="aa53e-119">Contient une chaîne qui représente le **ldapDisplayName** de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="aa53e-119">Contains a string that represents the **ldapDisplayName** of the attribute.</span></span>                                                         |
| <span data-ttu-id="aa53e-120">« &lt; en-tête de colonne &gt; »</span><span class="sxs-lookup"><span data-stu-id="aa53e-120">"&lt;column header&gt;"</span></span>      | <span data-ttu-id="aa53e-121">Contient une chaîne qui représente le texte affiché dans l’en-tête de la colonne.</span><span class="sxs-lookup"><span data-stu-id="aa53e-121">Contains a string that represents the text displayed in the header for the column.</span></span>                                                  |
| <span data-ttu-id="aa53e-122">" &lt; visibilité par défaut &gt; "</span><span class="sxs-lookup"><span data-stu-id="aa53e-122">"&lt;default visibility&gt;"</span></span> | <span data-ttu-id="aa53e-123">Contient une valeur numérique égale à 0 si l’attribut est masqué par défaut ou égal à 1 si l’attribut est visible par défaut.</span><span class="sxs-lookup"><span data-stu-id="aa53e-123">Contains a numeric value that is 0 if the attribute is hidden by default or 1 if the attribute is visible by default.</span></span>               |
| <span data-ttu-id="aa53e-124">« &lt; Width &gt; »</span><span class="sxs-lookup"><span data-stu-id="aa53e-124">"&lt;width&gt;"</span></span>              | <span data-ttu-id="aa53e-125">Contient la largeur de la colonne en pixels.</span><span class="sxs-lookup"><span data-stu-id="aa53e-125">Contains the width of the column, in pixels.</span></span> <span data-ttu-id="aa53e-126">Si cette valeur est égale à-1, la largeur de la colonne est définie sur la largeur de l’en-tête de colonne.</span><span class="sxs-lookup"><span data-stu-id="aa53e-126">If this value is -1, the width of the column is set to the width of the column header.</span></span> |
| <span data-ttu-id="aa53e-127">« &lt; inutilisé &gt; »</span><span class="sxs-lookup"><span data-stu-id="aa53e-127">"&lt;unused&gt;"</span></span>             | <span data-ttu-id="aa53e-128">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="aa53e-128">Unused.</span></span> <span data-ttu-id="aa53e-129">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="aa53e-129">Must be zero.</span></span>                                                                                                               |



 

<span data-ttu-id="aa53e-130">Par exemple, pour ajouter une colonne qui affichera le nom canonique des objets d’une unité d’organisation, une valeur pour l’attribut **canonicalName** est ajoutée à l’attribut **extraColumns** de l’objet **OrganizationalUnit-Display** dans le conteneur Spécificateurs d’affichage.</span><span class="sxs-lookup"><span data-stu-id="aa53e-130">For example, to add a column that will display the canonical name for objects in an organizational unit, a value for the **canonicalName** attribute is added to the **extraColumns** attribute of the **organizationalUnit-Display** object in the display specifiers container.</span></span> <span data-ttu-id="aa53e-131">La chaîne ajoutée à l’attribut **extraColumns** de l’objet **OrganizationalUnit-Display** se présente comme suit.</span><span class="sxs-lookup"><span data-stu-id="aa53e-131">The string added to the **extraColumns** attribute of the **organizationalUnit-Display** object will look like the following.</span></span>


```C++
canonicalName,Canonical Name,0,150,0
```



<span data-ttu-id="aa53e-132">La boîte de dialogue **Ajouter/supprimer des colonnes** affiche uniquement les colonnes contenues dans l’attribut **extraColumns** de l’objet **displaySpecifier** du type de conteneur affiché.</span><span class="sxs-lookup"><span data-stu-id="aa53e-132">The **Add/Remove Columns** dialog box displays only the columns that are contained in the **extraColumns** attribute of the **displaySpecifier** object of the container type that is being displayed.</span></span> <span data-ttu-id="aa53e-133">Si l’attribut **extraColumns** ne contient aucune valeur, la boîte de dialogue **Ajouter/supprimer des colonnes** affiche un ensemble fixe de colonnes.</span><span class="sxs-lookup"><span data-stu-id="aa53e-133">If the **extraColumns** attribute does not contain any values, the **Add/Remove Columns** dialog box will display a fixed set of columns.</span></span> <span data-ttu-id="aa53e-134">Une copie de l’ensemble fixe de colonnes est contenue dans l’attribut **extraColumns** de l’objet d' **affichage par défaut** .</span><span class="sxs-lookup"><span data-stu-id="aa53e-134">A copy of the fixed set of columns is contained in the **extraColumns** attribute of the **default-Display** object.</span></span>

<span data-ttu-id="aa53e-135">Pour ajouter une ou plusieurs colonnes à la liste des colonnes d’un objet spécifique, vous devez copier toutes les valeurs **extraColumns** de l’objet d' **affichage par défaut** vers l’objet cible, puis ajouter les colonnes personnalisées.</span><span class="sxs-lookup"><span data-stu-id="aa53e-135">To add one or more columns to the list of columns for a specific object, you must copy all of the **extraColumns** values from the **default-Display** object to the target object and then add the custom columns.</span></span> <span data-ttu-id="aa53e-136">Si vous spécifiez l’attribut **extraColumns** sur une classe donnée, cette classe utilisera ces colonnes et ne les fusionnera pas avec les colonnes spécifiées dans la classe d' **affichage par défaut** .</span><span class="sxs-lookup"><span data-stu-id="aa53e-136">If you specify the **extraColumns** attribute on a given class, then that class will use those columns and will not merge them with the columns that are specified in the **default-Display** class.</span></span> <span data-ttu-id="aa53e-137">Par conséquent, les modifications apportées à la classe d' **affichage par défaut** n’auront aucun effet sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="aa53e-137">Therefore, further changes to the **default-Display** class will have no effect on that object.</span></span>

<span data-ttu-id="aa53e-138">Pour afficher une colonne personnalisée pour tous les types de conteneurs qui n’ont pas de colonnes personnalisées inscrites, ajoutez une valeur pour la colonne à l’attribut **extraColumns** de l’objet d' **affichage par défaut** .</span><span class="sxs-lookup"><span data-stu-id="aa53e-138">To display a custom column for all container types that do not have any custom columns registered, add a value for the column to the **extraColumns** attribute of the **default-Display** object.</span></span>

 

 




