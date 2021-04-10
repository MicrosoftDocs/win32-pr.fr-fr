---
description: Le type d’identificateur du type sémantique est l’un des types de format texte.
ms.assetid: 137c3ad8-e47c-4cc5-b5c5-ea130236551a
title: Type d’identificateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6d4e63b473c9ba0705c093f1dec5bcdbc1e26f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115366"
---
# <a name="identifier-type"></a><span data-ttu-id="e1a2a-103">Type d’identificateur</span><span class="sxs-lookup"><span data-stu-id="e1a2a-103">Identifier Type</span></span>

<span data-ttu-id="e1a2a-104">Le type d’identificateur du [type sémantique](semantic-types.md) est l’un des [types de format texte](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="e1a2a-104">The Identifier Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="e1a2a-105">Ce type est constitué d’une chaîne de texte fournie par l’utilisateur au format d’un [identificateur](identifier.md)de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e1a2a-105">This type consists of an text string provided by the user in the format of a Windows Installer [Identifier](identifier.md).</span></span> <span data-ttu-id="e1a2a-106">L’outil de fusion remplace cette chaîne dans les modèles spécifiés dans la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="e1a2a-106">The merge tool substitutes this string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="e1a2a-107">Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de la chaîne de texte dans la colonne nom, entrer « 0 » dans la colonne format, entrer « identificateur » dans la colonne type et laisser vide la colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md). La chaîne peut être dans n’importe quel langage compatible avec la page de codes de la base de données.</span><span class="sxs-lookup"><span data-stu-id="e1a2a-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "Identifier" into the Type column, and leave blank the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).The string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="e1a2a-108">Consultez [gestion des pages de codes (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="e1a2a-108">See [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="e1a2a-109">NULL est une valeur valide pour la chaîne de texte, sauf si msmConfigItemNonNullable a été inclus dans le champ Attributes de la table ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e1a2a-109">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



