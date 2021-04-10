---
title: Écriture de scripts d’objets COM dans des applications personnalisées
description: Écriture de scripts d’objets COM dans des applications personnalisées
ms.assetid: 14e8cd53-e2b2-4393-8961-32efdf269f76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d16938747755dfb0c08907430837de5a1106ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196663"
---
# <a name="scripting-com-objects-in-custom-applications"></a><span data-ttu-id="8df04-103">Écriture de scripts d’objets COM dans des applications personnalisées</span><span class="sxs-lookup"><span data-stu-id="8df04-103">Scripting COM Objects in Custom Applications</span></span>

<span data-ttu-id="8df04-104">Microsoft fournit plusieurs environnements pour l’écriture de scripts d’objets COM : Active Server pages, Windows Script Host, etc.</span><span class="sxs-lookup"><span data-stu-id="8df04-104">Microsoft provides several environments for scripting COM objects: Active Server Pages, Windows Script Host, and so on.</span></span> <span data-ttu-id="8df04-105">Les éditeurs de logiciels indépendants (ISV) peuvent également accorder des licences aux moteurs de script Microsoft pour les utiliser dans leurs applications.</span><span class="sxs-lookup"><span data-stu-id="8df04-105">Independent software vendors (ISVs) can also license Microsoft scripting engines for use in their applications.</span></span> <span data-ttu-id="8df04-106">Par exemple, un ISV qui crée un traitement de texte peut vouloir ajouter un langage de macro à l’application afin que les utilisateurs puissent automatiser des tâches simples.</span><span class="sxs-lookup"><span data-stu-id="8df04-106">For example, an ISV creating a word processor might want to add a macro language to the application so users could automate simple tasks.</span></span> <span data-ttu-id="8df04-107">En accordant une licence à un moteur de script, l’ISV peut utiliser un langage tel que VBScript ou JScript comme langage de macro de l’application.</span><span class="sxs-lookup"><span data-stu-id="8df04-107">By licensing a scripting engine, the ISV can use a language such as VBScript or JScript as the application's macro language.</span></span>

<span data-ttu-id="8df04-108">Outre les moteurs de script VBScript et JScript, les éditeurs de logiciels indépendants peuvent écrire leurs propres moteurs de script ActiveX.</span><span class="sxs-lookup"><span data-stu-id="8df04-108">In addition to licensing VBScript and JScript scripting engines, ISVs can write their own ActiveX scripting engines.</span></span> <span data-ttu-id="8df04-109">Ces moteurs de script peuvent ensuite être connectés à n’importe quel environnement hôte qui prend en charge le moteur de script ActiveX standard.</span><span class="sxs-lookup"><span data-stu-id="8df04-109">These scripting engines can then be plugged into any host environment that supports the ActiveX scripting engine standard.</span></span> <span data-ttu-id="8df04-110">Par exemple, un éditeur de logiciels peut écrire un moteur de script PerlScript et l’installer sur un serveur ASP, ce qui permet au serveur ASP de traiter les scripts PerlScript.</span><span class="sxs-lookup"><span data-stu-id="8df04-110">For example, an ISV might write a PerlScript scripting engine and install it on an ASP server, thus enabling the ASP server to process PerlScript scripts.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8df04-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8df04-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8df04-112">Écriture de scripts avec des objets COM</span><span class="sxs-lookup"><span data-stu-id="8df04-112">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




