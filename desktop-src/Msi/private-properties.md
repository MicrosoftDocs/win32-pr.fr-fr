---
description: Les propriétés privées sont utilisées en interne par le programme d’installation et leurs valeurs doivent être entrées dans la base de données par l’auteur du package d’installation ou définies par le programme d’installation lors de l’installation sur les valeurs déterminées par l’environnement d’exploitation.
ms.assetid: 7d574bf0-bcb3-4e19-9659-fe741ace9f21
title: Propriétés privées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab7b0196be016fecb625e139f308219582620d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528250"
---
# <a name="private-properties"></a><span data-ttu-id="d6242-103">Propriétés privées</span><span class="sxs-lookup"><span data-stu-id="d6242-103">Private Properties</span></span>

<span data-ttu-id="d6242-104">Les propriétés privées sont utilisées en interne par le programme d’installation et leurs valeurs doivent être entrées dans la base de données par l’auteur du package d’installation ou définies par le programme d’installation lors de l’installation sur les valeurs déterminées par l’environnement d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d6242-104">Private properties are used internally by the installer and their values must be entered into the database by the author of the installation package or set by the installer during the installation to values determined by the operating environment.</span></span> <span data-ttu-id="d6242-105">La seule façon dont un utilisateur peut interagir avec les propriétés privées consiste à utiliser des [événements de contrôle](control-events.md) dans l’interface utilisateur créée du package.</span><span class="sxs-lookup"><span data-stu-id="d6242-105">The only way a user can interact with private properties is through [Control Events](control-events.md) in the package's authored user interface.</span></span> <span data-ttu-id="d6242-106">Les noms de propriétés privées doivent inclure des lettres minuscules.</span><span class="sxs-lookup"><span data-stu-id="d6242-106">Private property names must include lowercase letters.</span></span> <span data-ttu-id="d6242-107">Consultez [restrictions sur les noms de propriété](restrictions-on-property-names.md).</span><span class="sxs-lookup"><span data-stu-id="d6242-107">See [Restrictions on Property Names](restrictions-on-property-names.md).</span></span>

<span data-ttu-id="d6242-108">Les propriétés privées décrivent généralement l’environnement d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d6242-108">Private properties commonly describe the operating environment.</span></span> <span data-ttu-id="d6242-109">Par exemple, si l’installation est exécutée sur une plate-forme Windows, le programme d’installation définit la propriété [**WindowsFolder**](windowsfolder.md) sur la valeur spécifiée dans la table de propriétés.</span><span class="sxs-lookup"><span data-stu-id="d6242-109">For example, if the installation is run on a Windows platform, the installer sets the [**WindowsFolder**](windowsfolder.md) property to the value specified in the Property table.</span></span>

<span data-ttu-id="d6242-110">Les valeurs de propriété privées ne peuvent pas être substituées sur une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="d6242-110">Private property values cannot be overridden at a command line.</span></span> <span data-ttu-id="d6242-111">Pour effacer une propriété privée d’une installation, ne la laissez pas dans la [table des propriétés](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="d6242-111">To clear a private property from an installation, leave it out of the [Property table](property-table.md).</span></span> <span data-ttu-id="d6242-112">Sur Windows XP et Windows 2000, vous ne pouvez pas définir une propriété privée dans la phase de l’interface utilisateur de l’installation, puis passer la valeur à la phase d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d6242-112">On Windows XP, and Windows 2000 you cannot set a private property in the user interface phase of the installation and then pass the value to the execution phase.</span></span>

<span data-ttu-id="d6242-113">Pour obtenir la liste de toutes les propriétés privées standard utilisées par le programme d’installation, consultez Référence de la [propriété](property-reference.md).</span><span class="sxs-lookup"><span data-stu-id="d6242-113">For a list of all the standard private properties used by the installer, see [Property Reference](property-reference.md).</span></span> <span data-ttu-id="d6242-114">Vous pouvez définir une propriété privée personnalisée en entrant le nom et la valeur initiale de la propriété dans la table de propriétés.</span><span class="sxs-lookup"><span data-stu-id="d6242-114">You can define a custom private property by entering the property's name and initial value in the Property table.</span></span> <span data-ttu-id="d6242-115">Les noms de propriétés privées doivent toujours inclure des lettres minuscules.</span><span class="sxs-lookup"><span data-stu-id="d6242-115">Private property names must always include lowercase letters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6242-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d6242-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6242-117">Propri&amp;#233;t&amp;#233;s publiques</span><span class="sxs-lookup"><span data-stu-id="d6242-117">Public Properties</span></span>](public-properties.md)
</dt> </dl>

 

 



