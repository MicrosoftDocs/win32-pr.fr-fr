---
description: Le type de dialogue de type sémantique est l’un des types de format de clé. Ce type se compose d’une clé étrangère dans la table de boîtes de dialogue fournie par l’utilisateur.
ms.assetid: 3656684a-de95-45e1-9c78-5c1cc8ca879a
title: Type de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ed04dece5702d232f252caa7c0ee02e7576246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534346"
---
# <a name="dialog-type"></a><span data-ttu-id="2b897-104">Type de dialogue</span><span class="sxs-lookup"><span data-stu-id="2b897-104">Dialog Type</span></span>

<span data-ttu-id="2b897-105">Le type de dialogue de [type sémantique](semantic-types.md) est l’un des [types de format de clé](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="2b897-105">The Dialog Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="2b897-106">Ce type se compose d’une clé étrangère dans la [table de boîtes de dialogue](dialog-table.md) fournie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2b897-106">This type consists of a foreign key into the [Dialog table](dialog-table.md) provided by the user.</span></span>

<span data-ttu-id="2b897-107">L’outil de fusion doit substituer un [identificateur](identifier.md) de Windows Installer valide pour les éléments de ce type.</span><span class="sxs-lookup"><span data-stu-id="2b897-107">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="2b897-108">Mergemod.dll n’applique pas cette restriction et c’est à l’outil de fusion de s’assurer que l’utilisateur fournit une clé valide dans la table de dialogue.</span><span class="sxs-lookup"><span data-stu-id="2b897-108">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Dialog table.</span></span>

<span data-ttu-id="2b897-109">NULL est une valeur valide pour ce type, sauf si msmConfigItemNonNullable a été inclus dans le champ Attributes de la [table ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="2b897-109">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="2b897-110">Le type de dialogue peut être utilisé avec les types de ContextData suivants.</span><span class="sxs-lookup"><span data-stu-id="2b897-110">The Dialog type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="2b897-111">**DialogNext ContextData**</span><span class="sxs-lookup"><span data-stu-id="2b897-111">**DialogNext ContextData**</span></span>

<span data-ttu-id="2b897-112">Un module de fusion configurable peut utiliser ce type pour permettre à l’utilisateur de fournir une clé étrangère dans la table de boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="2b897-112">A configurable merge module may use this type to enable the user to provide a foreign key into the Dialog Table.</span></span> <span data-ttu-id="2b897-113">Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de l’élément configurable dans la colonne nom, entrer « 1 » dans la colonne format, entrer « boîte de dialogue » dans la colonne type et entrer « DialogNext » dans la colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="2b897-113">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Dialog" into the Type column, and enter "DialogNext" into the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="2b897-114">**DialogPrev ContextData**</span><span class="sxs-lookup"><span data-stu-id="2b897-114">**DialogPrev ContextData**</span></span>

<span data-ttu-id="2b897-115">Un module de fusion configurable peut utiliser ce type pour permettre à l’utilisateur de fournir une clé étrangère dans la table de boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="2b897-115">A configurable merge module may use this type to enable the user to provide a foreign key into the Dialog Table.</span></span> <span data-ttu-id="2b897-116">Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de l’élément configurable dans la colonne nom, entrer « 1 » dans la colonne format, entrer « boîte de dialogue » dans la colonne type et entrer « DialogPrev » dans la colonne ContextData de la table ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2b897-116">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Dialog" into the Type column, and enter "DialogPrev" into the ContextData column of the ModuleConfiguration table.</span></span>

 

 



