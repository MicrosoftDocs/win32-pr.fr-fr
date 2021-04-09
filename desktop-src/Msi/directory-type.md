---
description: Le type de répertoire de type sémantique est l’un des types de format de clé, qui se compose d’une clé étrangère dans la table de répertoires fournie par l’utilisateur.
ms.assetid: b5a0ed38-1dda-4c33-9429-0cbe87e13aef
title: Type de répertoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3ba336dd5de7cd45ef9215f0397ba51ce544d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866337"
---
# <a name="directory-type"></a><span data-ttu-id="7524d-103">Type de répertoire</span><span class="sxs-lookup"><span data-stu-id="7524d-103">Directory Type</span></span>

<span data-ttu-id="7524d-104">Le type de répertoire de [type sémantique](semantic-types.md) est l’un des [types de format de clé](key-format-types.md), qui se compose d’une clé étrangère dans la table de [répertoires](directory-table.md) fournie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7524d-104">The Directory Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md), which consists of a foreign key into the [Directory table](directory-table.md) provided by the user.</span></span>

<span data-ttu-id="7524d-105">L’outil de fusion doit substituer un [identificateur](identifier.md) de Windows Installer valide pour les éléments de ce type.</span><span class="sxs-lookup"><span data-stu-id="7524d-105">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="7524d-106">Mergemod.dll n’applique pas cette restriction et c’est à l’outil de fusion de s’assurer que l’utilisateur fournit une clé valide dans la table de répertoires.</span><span class="sxs-lookup"><span data-stu-id="7524d-106">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Directory table.</span></span>

<span data-ttu-id="7524d-107">Un élément configurable du type de répertoire doit uniquement modifier le répertoire de destination de l’installation et ne pas modifier l’image source.</span><span class="sxs-lookup"><span data-stu-id="7524d-107">A configurable item of the Directory type should only modify the destination directory of the installation and not modify the source image.</span></span> <span data-ttu-id="7524d-108">Un élément configurable de ce type doit donc uniquement modifier les clés étrangères de la table de répertoires et ne pas modifier directement la table de répertoires.</span><span class="sxs-lookup"><span data-stu-id="7524d-108">A configurable item of this type should therefore only modify foreign keys to the Directory table and not modify the Directory table directly.</span></span>

<span data-ttu-id="7524d-109">Étant donné que la \_ colonne de répertoire de la [table de composants](component-table.md) n’accepte pas les valeurs NULL, la valeur NULL n’est pas une valeur valide pour un élément configurable de ce type, même si le msmConfigItemNonNullable n’est pas défini dans la colonne attributs.</span><span class="sxs-lookup"><span data-stu-id="7524d-109">Because the Directory\_ column of the [Component table](component-table.md) is non-nullable, null is an invalid value for a configurable item of this type even if the msmConfigItemNonNullable is not set in the Attributes column.</span></span>

<span data-ttu-id="7524d-110">Le type de répertoire peut être utilisé avec deux types de ContextData.</span><span class="sxs-lookup"><span data-stu-id="7524d-110">The Directory type may be used with two kinds of ContextData.</span></span>

<span data-ttu-id="7524d-111">**IsolationDirectory ContextData**</span><span class="sxs-lookup"><span data-stu-id="7524d-111">**IsolationDirectory ContextData**</span></span>

<span data-ttu-id="7524d-112">Un module de fusion configurable peut utiliser ce type pour permettre à l’utilisateur de fournir un répertoire de destination pour les fichiers dans le module.</span><span class="sxs-lookup"><span data-stu-id="7524d-112">A configurable merge module may use this type to enable the user to provide a destination directory for files in the module.</span></span> <span data-ttu-id="7524d-113">L’outil Merge Tool remplace l’identificateur de l’annuaire dans les modèles de la colonne value de la [table ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="7524d-113">The merge tool substitutes the directory's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="7524d-114">Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom du répertoire dans la colonne nom, entrer « 1 » dans la colonne format, entrer « répertoire » dans la colonne type et entrer « IsolationDirectory » dans la colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="7524d-114">To specify a configurable item of this type, module authors should enter the name of the directory into the Name column, enter "1" into the Format column, enter "Directory" into the Type column, and enter "IsolationDirectory" into the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="7524d-115">**ShortcutLocation ContextData**</span><span class="sxs-lookup"><span data-stu-id="7524d-115">**ShortcutLocation ContextData**</span></span>

<span data-ttu-id="7524d-116">Un module de fusion configurable peut utiliser ce type pour permettre à l’utilisateur de fournir un répertoire de destination pour les raccourcis dans le module.</span><span class="sxs-lookup"><span data-stu-id="7524d-116">A configurable merge module may use this type to enable the user to provide a destination directory for shortcuts in the module.</span></span> <span data-ttu-id="7524d-117">L’outil Merge Tool remplace l’identificateur du raccourci dans les modèles de la colonne value de la [table ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="7524d-117">The merge tool substitutes the shortcut's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="7524d-118">Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom du répertoire dans la colonne nom, entrer « 1 » dans la colonne format, entrer « répertoire » dans la colonne type et entrer « ShortcutLocation » dans la colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="7524d-118">To specify a configurable item of this type, module authors should enter the name of the directory into the Name column, enter "1" into the Format column, enter "Directory" into the Type column, and enter "ShortcutLocation" into the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

 

 



