---
title: Enregistrement et restauration de jeux de variables d’État
description: Vous pouvez enregistrer et restaurer les valeurs d’une collection de variables d’État sur une pile d’attributs avec les fonctions glPushAttrib et glPopAttrib.
ms.assetid: 339de633-4158-4907-b985-2d75b465fb2a
keywords:
- Variables d’État OpenGL
- enregistrement des variables d’État OpenGL
- restauration des variables d’État OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b3192c228ea35005c5755802d3cd1b873f7b7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510617"
---
# <a name="saving-and-restoring-sets-of-state-variables"></a><span data-ttu-id="b37da-106">Enregistrement et restauration de jeux de variables d’État</span><span class="sxs-lookup"><span data-stu-id="b37da-106">Saving and Restoring Sets of State Variables</span></span>

<span data-ttu-id="b37da-107">Vous pouvez enregistrer et restaurer les valeurs d’une collection de variables d’État sur une pile d’attributs avec les fonctions [**glPushAttrib**](glpushattrib.md) et [**glPopAttrib**](glpopattrib.md) .</span><span class="sxs-lookup"><span data-stu-id="b37da-107">You can save and restore the values of a collection of state variables on an attribute stack with the [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) functions.</span></span> <span data-ttu-id="b37da-108">La profondeur de la pile d’attributs est au moins égale à 16.</span><span class="sxs-lookup"><span data-stu-id="b37da-108">The attribute stack has a depth of at least 16.</span></span> <span data-ttu-id="b37da-109">Pour obtenir la profondeur réelle, utilisez la \_ profondeur de la \_ pile Max \_ . d’attrib GL \_ avec [**glGetIntegerv**](glgetintegerv.md).</span><span class="sxs-lookup"><span data-stu-id="b37da-109">To obtain the actual depth, use GL\_MAX\_ATTRIB\_STACK\_DEPTH with [**glGetIntegerv**](glgetintegerv.md).</span></span> <span data-ttu-id="b37da-110">Le push d’une pile complète ou le dépilament d’une pile vide génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="b37da-110">Pushing a full stack or popping an empty one generates an error.</span></span>

<span data-ttu-id="b37da-111">Il est généralement plus rapide d’utiliser **glPushAttrib** et **glPopAttrib** que pour récupérer et restaurer les valeurs vous-même.</span><span class="sxs-lookup"><span data-stu-id="b37da-111">It is generally faster to use **glPushAttrib** and **glPopAttrib** than to get and restore the values yourself.</span></span> <span data-ttu-id="b37da-112">Certaines valeurs peuvent être envoyées et dépilées dans le matériel, et l’enregistrement et la restauration peuvent nécessiter beaucoup de ressources.</span><span class="sxs-lookup"><span data-stu-id="b37da-112">Some values might be pushed and popped in the hardware, and saving and restoring them can be resource-intensive.</span></span> <span data-ttu-id="b37da-113">En outre, si vous utilisez un client distant, toutes les données d’attribut doivent être transférées via la connexion réseau, puis à nouveau enregistrées et restaurées.</span><span class="sxs-lookup"><span data-stu-id="b37da-113">Also, if you're operating on a remote client, all of the attribute data must be transferred across the network connection and back as it is saved and restored.</span></span> <span data-ttu-id="b37da-114">Toutefois, votre implémentation OpenGL conserve la pile d’attributs sur le serveur, ce qui évite les retards de réseau inutiles.</span><span class="sxs-lookup"><span data-stu-id="b37da-114">However, your OpenGL implementation keeps the attribute stack on the server, avoiding unnecessary network delays.</span></span>

<span data-ttu-id="b37da-115">Le prototype de **glPushAttrib** est le suivant :</span><span class="sxs-lookup"><span data-stu-id="b37da-115">The prototype of **glPushAttrib** is:</span></span>

<span data-ttu-id="b37da-116">**void** **glPushAttrib**( *masque* GLbitfield);</span><span class="sxs-lookup"><span data-stu-id="b37da-116">**void** **glPushAttrib**(**GLbitfield** *mask* );</span></span>

<span data-ttu-id="b37da-117">L’utilisation de [**glPushAttrib**](glpushattrib.md) enregistre tous les attributs indiqués par bits dans *Mask* en les envoyant sur la pile d’attributs.</span><span class="sxs-lookup"><span data-stu-id="b37da-117">Using [**glPushAttrib**](glpushattrib.md) saves all the attributes indicated by bits in *mask* by pushing them onto the attribute stack.</span></span> <span data-ttu-id="b37da-118">Pour obtenir la liste des bits de masque possibles que vous pouvez logiquement ou ensemble pour enregistrer n’importe quelle combinaison d’attributs, consultez [groupes](attribute-groups.md)d’attributs.</span><span class="sxs-lookup"><span data-stu-id="b37da-118">For a list of the possible mask bits you can logically OR together to save any combination of attributes, see [Attribute Groups](attribute-groups.md).</span></span> <span data-ttu-id="b37da-119">Chaque bit correspond à une collection de variables d’État individuelles.</span><span class="sxs-lookup"><span data-stu-id="b37da-119">Each bit corresponds to a collection of individual state variables.</span></span> <span data-ttu-id="b37da-120">Par exemple, le \_ bit d’éclairage GL \_ fait référence à toutes les variables d’état associées à l’éclairage, y compris la couleur de matériau actuelle, la lumière ambiante, diffuse, spéculaire et émise, une liste des lumières activées et les directions des lumières.</span><span class="sxs-lookup"><span data-stu-id="b37da-120">For example, GL\_LIGHTING\_BIT refers to all the state variables related to lighting, which include the current material color; the ambient, diffuse, specular, and emitted light; a list of the lights that are enabled; and the directions of the spotlights.</span></span> <span data-ttu-id="b37da-121">Lorsque vous appelez [**glPopAttrib**](glpopattrib.md), toutes ces variables sont restaurées.</span><span class="sxs-lookup"><span data-stu-id="b37da-121">When you call [**glPopAttrib**](glpopattrib.md), all those variables are restored.</span></span> <span data-ttu-id="b37da-122">Pour savoir exactement quels attributs sont enregistrés pour des valeurs de masque particulières, consultez la page [variables d’État OpenGL](opengl-state-variables.md).</span><span class="sxs-lookup"><span data-stu-id="b37da-122">To find out exactly which attributes are saved for particular mask values, see [OpenGL State Variables](opengl-state-variables.md).</span></span>

 

 




