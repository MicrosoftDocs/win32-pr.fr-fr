---
description: Le type de sémantique mis en forme est l’un des types de format texte.
ms.assetid: 44af5b5c-bbf9-4043-8076-0881680a36c1
title: Type mis en forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b97e0c0c1763352f75424bf54d01f6871604f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034198"
---
# <a name="formatted-type"></a><span data-ttu-id="fb89f-103">Type mis en forme</span><span class="sxs-lookup"><span data-stu-id="fb89f-103">Formatted Type</span></span>

<span data-ttu-id="fb89f-104">Le type de [sémantique](semantic-types.md) mis en forme est l’un des [types de format texte](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="fb89f-104">The Formatted Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="fb89f-105">Ce type est constitué d’une chaîne de texte arbitraire de toute longueur fournie par l’utilisateur et au format texte mis en forme Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="fb89f-105">This type consists of an arbitrary text string of any length provided by the user and in the Windows Installer formatted text format.</span></span> <span data-ttu-id="fb89f-106">Pour plus d’informations, consultez [formatée](formatted.md).</span><span class="sxs-lookup"><span data-stu-id="fb89f-106">For details, see [Formatted](formatted.md).</span></span> <span data-ttu-id="fb89f-107">L’outil de fusion remplace cette chaîne dans les modèles spécifiés dans la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="fb89f-107">The merge tool substitutes this string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="fb89f-108">Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de la chaîne de texte dans la colonne nom, entrer « 0 » dans la colonne format, entrer « formaté » dans la colonne type et laisser vide la colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md). La chaîne peut être dans n’importe quel langage compatible avec la page de codes de la base de données.</span><span class="sxs-lookup"><span data-stu-id="fb89f-108">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "Formatted" into the Type column, and leave blank the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).The string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="fb89f-109">Pour plus d’informations, consultez [gestion des pages de codes (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="fb89f-109">For details, see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="fb89f-110">NULL est une valeur valide pour la chaîne de texte, sauf si msmConfigItemNonNullable a été inclus dans le champ Attributes de la table ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="fb89f-110">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



