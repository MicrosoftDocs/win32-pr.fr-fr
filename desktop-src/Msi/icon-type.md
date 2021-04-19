---
description: Le type d’icône du type sémantique est l’un des types de format de clé. Ce type est constitué d’une clé dans la table d’icônes fournie par l’utilisateur.
ms.assetid: 8e155846-cc29-43f4-b1f7-9880320edbec
title: Type d’icône
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a7c90de925ff34977e7ff192dffe0b8614e5734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527755"
---
# <a name="icon-type"></a><span data-ttu-id="2d79a-104">Type d’icône</span><span class="sxs-lookup"><span data-stu-id="2d79a-104">Icon Type</span></span>

<span data-ttu-id="2d79a-105">Le type d’icône du [type sémantique](semantic-types.md) est l’un des [types de format de clé](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="2d79a-105">The Icon Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="2d79a-106">Ce type est constitué d’une clé dans la [table d’icônes](icon-table.md) fournie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2d79a-106">This type consists of a key into the [Icon table](icon-table.md) provided by the user.</span></span>

<span data-ttu-id="2d79a-107">L’outil de fusion doit substituer un [identificateur](identifier.md) de Windows Installer valide pour les éléments de ce type.</span><span class="sxs-lookup"><span data-stu-id="2d79a-107">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="2d79a-108">Mergemod.dll n’applique pas cette restriction et c’est à l’outil de fusion de s’assurer que l’utilisateur fournit une clé valide dans la table d’icônes.</span><span class="sxs-lookup"><span data-stu-id="2d79a-108">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Icon table.</span></span>

<span data-ttu-id="2d79a-109">NULL est une valeur valide pour ce type, sauf si msmConfigItemNonNullable a été inclus dans le champ Attributes de la [table ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="2d79a-109">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="2d79a-110">Le type binaire peut être utilisé avec les types de ContextData suivants.</span><span class="sxs-lookup"><span data-stu-id="2d79a-110">The Binary type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="2d79a-111">**ShortcutIcon ContextData**</span><span class="sxs-lookup"><span data-stu-id="2d79a-111">**ShortcutIcon ContextData**</span></span>

<span data-ttu-id="2d79a-112">Un module de fusion configurable peut utiliser ce type pour permettre à l’utilisateur de fournir une clé étrangère à une ligne dans la [table d’icônes](icon-table.md) qui contient une image pouvant être utilisée comme icône de raccourci.</span><span class="sxs-lookup"><span data-stu-id="2d79a-112">A configurable merge module may use this type to enable the user to provide a foreign key to a row in the [Icon Table](icon-table.md) that contains an image suitable for use as a shortcut icon.</span></span> <span data-ttu-id="2d79a-113">Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de l’élément configurable dans la colonne nom, entrer « 1 » dans la colonne format, entrer « Icon » dans la colonne de type et entrer « ShorcutIcon » dans la colonne ContextData de la table ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d79a-113">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Icon" into the Type column, and enter "ShorcutIcon" into the ContextData column of the ModuleConfiguration table.</span></span> <span data-ttu-id="2d79a-114">Ce type n’est pas approprié pour une utilisation dans une table d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2d79a-114">This type is not appropriate for use in a user interface table.</span></span> <span data-ttu-id="2d79a-115">Pour modifier une clé de la table d’icônes de ces tables, consultez icône ContextData sous [type binaire](binary-type.md).</span><span class="sxs-lookup"><span data-stu-id="2d79a-115">To modify a key to the Icon table in these tables see Icon ContextData under [Binary Type](binary-type.md).</span></span>

 

 



