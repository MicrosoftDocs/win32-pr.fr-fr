---
title: Exemples de modifications incompatibles
description: 'En ce qui concerne les modifications incompatibles, la règle de pouce en cause est la suivante : toute modification peut être incompatible en amont, sauf si elle est très bien comprise.'
ms.assetid: 5b893d79-b81d-4ede-8d49-71d85219c497
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9498e5c71c7ce9690da0969f234fbb9d094eca50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029365"
---
# <a name="examples-of-incompatible-changes"></a><span data-ttu-id="6e51b-103">Exemples de modifications incompatibles</span><span class="sxs-lookup"><span data-stu-id="6e51b-103">Examples of Incompatible Changes</span></span>

<span data-ttu-id="6e51b-104">En ce qui concerne les modifications incompatibles, la règle de pouce est la suivante : toute modification peut être incompatible en amont, sauf si elle est très bien comprise.</span><span class="sxs-lookup"><span data-stu-id="6e51b-104">When dealing with incompatible changes, the unfortunate rule of thumb is as follows: any change can be backward incompatible, unless it is very well understood.</span></span> <span data-ttu-id="6e51b-105">Cette règle requiert une connaissance des règles de NDR.</span><span class="sxs-lookup"><span data-stu-id="6e51b-105">This rule requires knowledge of NDR rules.</span></span> <span data-ttu-id="6e51b-106">Si vous ne connaissez pas le rapport de non-remise, n’apportez aucune modification.</span><span class="sxs-lookup"><span data-stu-id="6e51b-106">If you do not know what the NDR is, do not make modifications.</span></span> <span data-ttu-id="6e51b-107">Les exemples de modifications qui entraînent généralement une violation d’accès dans l’application, ou une exception de données de stub incorrecte \_ \_ \_ déclenchée par le moteur de marshaling, sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6e51b-107">Examples of changes that typically result in an access violation in the application, or a BAD\_STUB\_DATA\_EXCEPTION raised by the marshaling engine, are as follows:</span></span>

-   <span data-ttu-id="6e51b-108">Ajout d’une nouvelle méthode au milieu des anciennes méthodes.</span><span class="sxs-lookup"><span data-stu-id="6e51b-108">Adding a new method in the middle of old methods.</span></span>
-   <span data-ttu-id="6e51b-109">Ajout ou suppression de paramètres dans une méthode.</span><span class="sxs-lookup"><span data-stu-id="6e51b-109">Adding or removing parameters from a method.</span></span>
-   <span data-ttu-id="6e51b-110">Modification d’un attribut, par exemple un attribut de pointeur : remplacement \[ \] de Ref par \[ unique \] ou \[ ptr, \] ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="6e51b-110">Changing an attribute, for example a pointer attribute: changing \[ref\] to \[unique\] or \[ptr\] or vice versa.</span></span> <span data-ttu-id="6e51b-111">Chaque type de pointeur a une représentation filaire différente.</span><span class="sxs-lookup"><span data-stu-id="6e51b-111">Each pointer type has a different wire representation.</span></span>
-   <span data-ttu-id="6e51b-112">Modification de la taille des données : de Short à long, de char à WCHAR \_ t (Unicode), en ajoutant un champ à une structure, en modifiant la taille d’un tableau de taille fixe.</span><span class="sxs-lookup"><span data-stu-id="6e51b-112">Changing the size of the data: from short to long, from char to wchar\_t (unicode), adding a field to a structure, changing the size of a fixed size array.</span></span>
-   <span data-ttu-id="6e51b-113">Ajout de branches d’Union à une Union avec une clause default.</span><span class="sxs-lookup"><span data-stu-id="6e51b-113">Adding union arms to a union with a default clause.</span></span>

<span data-ttu-id="6e51b-114">Il se peut que des modifications insidieux ou des incompatibilités involontaires entre un client et un serveur se produisent comme suit :</span><span class="sxs-lookup"><span data-stu-id="6e51b-114">Some insidious changes or unintended mismatches between a client and a server may occur as follows:</span></span>

-   <span data-ttu-id="6e51b-115">Modification d’un membre d’un type composé, tel qu’une structure ou un tableau.</span><span class="sxs-lookup"><span data-stu-id="6e51b-115">Modifying a member of a compound type, like a structure or an array.</span></span> <span data-ttu-id="6e51b-116">Par exemple, si un \_ ID client passe d’un entier à un GUID, une \_ structure d’enregistrement client avec le \_ champ ID client devient incompatible.</span><span class="sxs-lookup"><span data-stu-id="6e51b-116">For example, if a CLIENT\_ID changes from an integral to a GUID, a CLIENT\_RECORD structure with the CLIENT\_ID field becomes incompatible.</span></span> <span data-ttu-id="6e51b-117">Il peut être difficile de détecter s’il est monté en cascade sur plusieurs niveaux d’incorporation à un type de paramètre distant réel.</span><span class="sxs-lookup"><span data-stu-id="6e51b-117">This may be difficult to detect if cascaded through several levels of embedding to an actual remote parameter type.</span></span>
-   <span data-ttu-id="6e51b-118">Modification d’un type importé.</span><span class="sxs-lookup"><span data-stu-id="6e51b-118">Modifying an imported type.</span></span> <span data-ttu-id="6e51b-119">Le type peut provenir d’un autre composant qui n’est pas directement distant, par conséquent, la modification a été jugée compatible.</span><span class="sxs-lookup"><span data-stu-id="6e51b-119">The type may be coming from a different component that does not remote directly, hence the change was thought to be compatible.</span></span>
-   <span data-ttu-id="6e51b-120">L’utilisation \# de ifdef dans un fichier IDL est une mauvaise idée pour les définitions de type ifdef dans un fichier IDL. il s’agit d’un incident qui se produit.</span><span class="sxs-lookup"><span data-stu-id="6e51b-120">Using \#ifdef in an IDL file is a bad idea to ifdef type definitions in an IDL file—it is disaster waiting to happen.</span></span> <span data-ttu-id="6e51b-121">Inévitablement, en raison de la génération ou d’autres problèmes, un client est compilé avec un ensemble différent de définitions que le serveur et il finit par être incompatible.</span><span class="sxs-lookup"><span data-stu-id="6e51b-121">Inevitably, due to build or other glitches, a client is compiled with a different set of defines than the server, and they end up being incompatible.</span></span>

 

 




