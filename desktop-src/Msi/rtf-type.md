---
description: Le type RTF du type sémantique est l’un des types de format texte.
ms.assetid: 91fc47c1-520a-4002-9dbe-4ee2b56f84b3
title: Type RTF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81c708183596d794f20e38bf89c073472e3affb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534313"
---
# <a name="rtf-type"></a><span data-ttu-id="d7dc9-103">Type RTF</span><span class="sxs-lookup"><span data-stu-id="d7dc9-103">RTF Type</span></span>

<span data-ttu-id="d7dc9-104">Le type RTF du [type sémantique](semantic-types.md) est l’un des [types de format texte](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="d7dc9-104">The RTF Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="d7dc9-105">Ce type est constitué d’une chaîne de texte arbitraire au format RTF (Rich Text Format), quelle que soit la longueur fournie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d7dc9-105">This type consists of an arbitrary text string in the Rich Text Format (RTF) of any length provided by the user.</span></span> <span data-ttu-id="d7dc9-106">L’outil de fusion remplace cette chaîne dans les modèles spécifiés dans la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="d7dc9-106">The merge tool substitutes this string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="d7dc9-107">Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de la chaîne de texte dans la colonne nom, entrer « 0 » dans la colonne format, entrer « RTF » dans la colonne type et laisser vide la colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md). La chaîne peut être dans n’importe quel langage compatible avec la page de codes de la base de données.</span><span class="sxs-lookup"><span data-stu-id="d7dc9-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "RTF" into the Type column, and leave blank the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).The string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="d7dc9-108">Consultez [gestion des pages de codes (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="d7dc9-108">See [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="d7dc9-109">NULL est une valeur valide pour la chaîne de texte, sauf si msmConfigItemNonNullable a été inclus dans le champ Attributes de la table ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d7dc9-109">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



