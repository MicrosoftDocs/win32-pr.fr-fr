---
description: Le type enum de type sémantique est l’un des types de format texte.
ms.assetid: fff01044-5749-42a5-b026-5b22671870bd
title: Type enum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc582a7f96d8fc91aad66387f579f05f9255346f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951641"
---
# <a name="enum-type"></a><span data-ttu-id="36207-103">Type enum</span><span class="sxs-lookup"><span data-stu-id="36207-103">Enum Type</span></span>

<span data-ttu-id="36207-104">Le type enum de [type sémantique](semantic-types.md) est l’un des [types de format texte](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="36207-104">The Enum Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="36207-105">Ce type est constitué d’une chaîne de texte choisie par l’utilisateur à partir d’un ensemble de choix.</span><span class="sxs-lookup"><span data-stu-id="36207-105">This type consists of a text string chosen by the user from a set of choices.</span></span> <span data-ttu-id="36207-106">L’outil de fusion remplace la chaîne sélectionnée sélectionnée dans les modèles spécifiés dans la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="36207-106">The merge tool substitutes the selected string selected into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="36207-107">Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de la chaîne de texte dans la colonne nom, entrer « 0 » dans la colonne format, entrer « enum » dans la colonne Type, puis entrer la liste des chaînes possibles dans la colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="36207-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "Enum" into the Type column, and enter the list of possible strings in the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="36207-108">La liste des chaînes possibles doit être fournie sous la forme d’une liste de chaînes Deliminated par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="36207-108">The list of possible strings must be provided as a list of strings deliminated by semicolons.</span></span> <span data-ttu-id="36207-109">Chaque choix doit se présenter sous la forme « nom = valeur ».</span><span class="sxs-lookup"><span data-stu-id="36207-109">Each choice must be in the form "Name=Value".</span></span> <span data-ttu-id="36207-110">Un point-virgule littéral peut être ajouté à la valeur en ajoutant un caractère barre oblique inverse au point-virgule.</span><span class="sxs-lookup"><span data-stu-id="36207-110">A literal semicolon can be added to the value by prefixing the semicolon with a backslash character.</span></span> <span data-ttu-id="36207-111">NULL est une valeur valide, sauf si msmConfigItemNonNullable a été inclus dans le champ Attributes de la table ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="36207-111">Null is a valid value unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



