---
description: Le type de texte arbitraire du type sémantique est l’un des types de format texte.
ms.assetid: 503ad2db-0875-4d8b-90f7-3d04318a6b62
title: Type de texte arbitraire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9709a560398472fe79a2c77db827acdfa7994148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517033"
---
# <a name="arbitrary-text-type"></a><span data-ttu-id="e7ad1-103">Type de texte arbitraire</span><span class="sxs-lookup"><span data-stu-id="e7ad1-103">Arbitrary Text Type</span></span>

<span data-ttu-id="e7ad1-104">Le type de texte arbitraire du [type sémantique](semantic-types.md) est l’un des [types de format texte](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="e7ad1-104">The Arbitrary Text Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="e7ad1-105">Ce type est constitué d’une chaîne de texte arbitraire de n’importe quelle longueur fournie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e7ad1-105">This type consists of an arbitrary text string of any length provided by the user.</span></span> <span data-ttu-id="e7ad1-106">L’outil de fusion remplace cette chaîne arbitraire dans les modèles spécifiés dans la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="e7ad1-106">The merge tool substitutes this arbitrary string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="e7ad1-107">Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de la chaîne de texte dans la colonne nom, entrer « 0 » dans la colonne format et laisser vides les colonnes type et ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md). La chaîne de texte arbitraire peut être dans n’importe quel langage compatible avec la page de codes de la base de données.</span><span class="sxs-lookup"><span data-stu-id="e7ad1-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, and leave blank the Type and ContextData columns of the [ModuleConfiguration table](moduleconfiguration-table.md).The arbitrary text string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="e7ad1-108">Pour plus d’informations, consultez [gestion des pages de codes (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="e7ad1-108">For details, see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="e7ad1-109">NULL est une valeur valide pour la chaîne de texte, sauf si msmConfigItemNonNullable a été inclus dans le champ Attributes de la table ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e7ad1-109">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



