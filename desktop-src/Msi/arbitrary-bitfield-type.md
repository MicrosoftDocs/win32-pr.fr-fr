---
description: '&\# 0034 ; Le champ \# de bits&0034 ; type sans demande de contexte que l’utilisateur fournisse un entier dont la valeur est utilisée pour définir un ou plusieurs bits dans un champ de bits. Ce texte peut être dans n’importe quelle langue compatible avec la page de codes de la base de données.'
ms.assetid: 28e1bdb9-a42d-46ce-ad24-71bc22e2d92a
title: Type de champ de type binaire arbitraire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6571b8585c94577927df8cfedaded802a67d125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115379"
---
# <a name="arbitrary-bitfield-type"></a><span data-ttu-id="fa0a2-104">Type de champ de type binaire arbitraire</span><span class="sxs-lookup"><span data-stu-id="fa0a2-104">Arbitrary Bitfield Type</span></span>

<span data-ttu-id="fa0a2-105">Le type « champ de bits » sans demande de contexte indique que l’utilisateur fournit un entier dont la valeur est utilisée pour définir un ou plusieurs bits dans un champ de bits.</span><span class="sxs-lookup"><span data-stu-id="fa0a2-105">The "Bitfield" type with no context requests that the user provide an integer whose value is used to set one or more bits in a bitfield.</span></span> <span data-ttu-id="fa0a2-106">Ce texte peut être dans n’importe quelle langue compatible avec la page de codes de la base de données.</span><span class="sxs-lookup"><span data-stu-id="fa0a2-106">This text may be in any language compatible with the code page of the database.</span></span>

<span data-ttu-id="fa0a2-107">Le type de champ de type binaire aléatoire du [type de sémantique](semantic-types.md) est l’un des types de champ de type binaire.</span><span class="sxs-lookup"><span data-stu-id="fa0a2-107">The Arbitrary Bitfield Type of [semantic type](semantic-types.md) is one of the Bitfield Types.</span></span> <span data-ttu-id="fa0a2-108">Ce type est constitué d’un entier choisi par l’utilisateur à partir d’un ensemble de choix.</span><span class="sxs-lookup"><span data-stu-id="fa0a2-108">This type consists of an integer chosen by the user from a set of choices.</span></span> <span data-ttu-id="fa0a2-109">L’outil de fusion remplace l’entier sélectionné dans les modèles spécifiés dans la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="fa0a2-109">The merge tool substitutes the selected integer into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="fa0a2-110">Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de l’élément dans la colonne nom, entrer « 3 » dans la colonne format, laisser la colonne type vide et entrer la liste des entiers possibles dans la colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="fa0a2-110">To specify a configurable item of this type, module authors should enter the name of the item into the Name column, enter "3" into the Format column, leave the Type column blank, and enter the list of possible integers in the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="fa0a2-111">La colonne de type est réservée et doit avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="fa0a2-111">The Type column is reserved and must be null.</span></span> <span data-ttu-id="fa0a2-112">L’entrée dans la colonne ContextData pour tous les types de format de champ de format binaire doit se présenter sous la forme " <mask> ;<Name>=</span><span class="sxs-lookup"><span data-stu-id="fa0a2-112">The entry in the ContextData column for all Bitfield Format types must be in the form "<mask>;<Name>=</span></span><value><span data-ttu-id="fa0a2-113">;<Name>=</span><span class="sxs-lookup"><span data-stu-id="fa0a2-113">;<Name>=</span></span><value><span data-ttu-id="fa0a2-114">....», où <mask> est une valeur entière indiquant les bits d’intérêt, <Name> est un nom complet localisable pour le choix, et</span><span class="sxs-lookup"><span data-stu-id="fa0a2-114">....", where <mask> is an integer value indicating the bits of interest, <Name> is a localizable display name for the choice, and</span></span> <value> <span data-ttu-id="fa0a2-115">valeur entière décimale.</span><span class="sxs-lookup"><span data-stu-id="fa0a2-115">is a decimal integer value.</span></span> <span data-ttu-id="fa0a2-116">La colonne de contexte est en cours d’utilisation [CMSM spécial format](cmsm-special-format.md) et pour tous les types de champ de type champ.</span><span class="sxs-lookup"><span data-stu-id="fa0a2-116">The context column is in use [CMSM Special Format](cmsm-special-format.md) and for all bitfield types.</span></span> <span data-ttu-id="fa0a2-117">Un caractère littéral « = » ou « ; » peut être entré dans le <Name> champ en le faisant précéder d’une barre oblique inverse (« \\ »).</span><span class="sxs-lookup"><span data-stu-id="fa0a2-117">A literal "=" or ";" character can be entered in the <Name> field by prefixing it with a backslash ('\\') character.</span></span>

 

 



