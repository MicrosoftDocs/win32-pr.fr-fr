---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3e8b9c48-9d2d-4055-b78d-c4a22d780764
title: L (Service VSS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a568ed662019cbc0f3c0a242faf884df72acb015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201456"
---
# <a name="l-volume-shadow-copy-service"></a><span data-ttu-id="a2bcc-103">L (Service VSS)</span><span class="sxs-lookup"><span data-stu-id="a2bcc-103">L (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="a2bcc-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [e](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K L M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="a2bcc-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K L M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="a2bcc-105"><span id="base.vssgloss_logical_path"></span><span id="BASE.VSSGLOSS_LOGICAL_PATH"></span>**chemin logique**</span><span class="sxs-lookup"><span data-stu-id="a2bcc-105"><span id="base.vssgloss_logical_path"></span><span id="BASE.VSSGLOSS_LOGICAL_PATH"></span>**logical path**</span></span>
</dt> <dd>

<span data-ttu-id="a2bcc-106">Mécanisme permettant de décrire les composants d’un enregistreur.</span><span class="sxs-lookup"><span data-stu-id="a2bcc-106">A mechanism for describing a writer's components.</span></span> <span data-ttu-id="a2bcc-107">Il est utilisé pour exprimer des relations entre les composants, en particulier leur hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="a2bcc-107">It is used to express relationships between components, in particularly their hierarchy.</span></span> <span data-ttu-id="a2bcc-108">Par exemple, si un writer gérait plusieurs livres électroniques, il peut affecter des chemins logiques « \\ ebook \\ Classeur1 » et « \\ ebook \\ book2 » aux composants de groupe de fichiers contenant chaque livre.</span><span class="sxs-lookup"><span data-stu-id="a2bcc-108">For instance, if a writer managed several electronic books, it might assign logical paths of "\\ebook\\book1" and "\\ebook\\book2" to file group components containing each book.</span></span> <span data-ttu-id="a2bcc-109">Les chemins d’accès logiques sont requis lors de la spécification des sous-composants.</span><span class="sxs-lookup"><span data-stu-id="a2bcc-109">Logical paths are required when specifying subcomponents.</span></span>

<span data-ttu-id="a2bcc-110">Par Convention, la barre oblique inverse « \\ » est utilisée pour séparer les éléments d’un chemin d’accès logique.</span><span class="sxs-lookup"><span data-stu-id="a2bcc-110">By convention the backslash "\\" is used to separate elements of a logical path.</span></span> <span data-ttu-id="a2bcc-111">En outre, il n’existe aucune restriction sur les caractères qui peuvent apparaître dans un chemin logique non **null** .</span><span class="sxs-lookup"><span data-stu-id="a2bcc-111">Beyond that, there are no restrictions on the characters that can appear in a non-**NULL** logical path.</span></span>

<span data-ttu-id="a2bcc-112">Un chemin d’accès logique peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="a2bcc-112">A logical path can be **NULL**.</span></span> <span data-ttu-id="a2bcc-113">Par Convention, les composants avec des chemins logiques **null** sont considérés comme étant au niveau supérieur de la hiérarchie des chemins d’accès logiques d’un writer.</span><span class="sxs-lookup"><span data-stu-id="a2bcc-113">By convention, components with **NULL** logical paths are said to be at the top level of a writer's logical path hierarchy.</span></span>

<span data-ttu-id="a2bcc-114">Voir aussi [*composant*](vssgloss-c.md), sous- [*composant*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="a2bcc-114">See also [*component*](vssgloss-c.md), [*subcomponent*](vssgloss-s.md).</span></span>

</dd> </dl>

 

 



