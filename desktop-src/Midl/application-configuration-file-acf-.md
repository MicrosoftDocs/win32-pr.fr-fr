---
title: Fichier de configuration de l’application (ACF)
description: Il peut y avoir des aspects de votre application distribuée qui affectent un composant, mais qui n’ont rien à faire avec un autre.
ms.assetid: 017d93fd-1701-4713-a786-752a7695b5a6
keywords:
- MIDL DE ACF
- Microsoft Interface Definition Language MIDL, décrit, fichier de configuration de l’application
- fichier de configuration de l’application MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9066e5641d6b71e68ba670984765661f1b9f6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510222"
---
# <a name="application-configuration-file-acf"></a><span data-ttu-id="b8fbd-106">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="b8fbd-106">Application Configuration File (ACF)</span></span>

<span data-ttu-id="b8fbd-107">Il peut y avoir des aspects de votre application distribuée qui affectent un composant, mais qui n’ont rien à faire avec un autre.</span><span class="sxs-lookup"><span data-stu-id="b8fbd-107">There may be aspects of your distributed application that affect one component, but have nothing to do with another.</span></span> <span data-ttu-id="b8fbd-108">Par exemple, un objet peut contenir une structure de données complexe de grande taille et passer le contenu de cette structure de données à un autre objet.</span><span class="sxs-lookup"><span data-stu-id="b8fbd-108">For example, an object may contain a large, complex data structure and pass the contents of this data structure to another object.</span></span> <span data-ttu-id="b8fbd-109">La disposition exacte de cette structure de données peut ne pas avoir de sens pour l’application réceptrice.</span><span class="sxs-lookup"><span data-stu-id="b8fbd-109">The exact layout of this data structure may be meaningless to the receiving application.</span></span> <span data-ttu-id="b8fbd-110">En outre, la structure peut contenir des types de données que le compilateur MIDL ne reconnaît pas et ne peut pas générer de code de marshaling et de démarshaling.</span><span class="sxs-lookup"><span data-stu-id="b8fbd-110">Also, the structure may contain data types that the MIDL compiler does not recognize and cannot generate marshaling and unmarshaling code.</span></span>

<span data-ttu-id="b8fbd-111">Les applications clientes peuvent partager la même interface, mais elles s’exécutent sur des plateformes différentes ; ils peuvent avoir besoin de leur propre ensemble de routines de marshaling.</span><span class="sxs-lookup"><span data-stu-id="b8fbd-111">Client applications may share the same interface but run on different platforms; they may each need their own set of marshaling routines.</span></span> <span data-ttu-id="b8fbd-112">Enfin, les clients individuels n’ont pas forcément besoin du même ensemble de fonctions.</span><span class="sxs-lookup"><span data-stu-id="b8fbd-112">Finally, individual clients may not always need the same set of functions.</span></span> <span data-ttu-id="b8fbd-113">Il est inefficace de générer du code stub pour les fonctions qui ne seront jamais implémentées dans une application cliente particulière.</span><span class="sxs-lookup"><span data-stu-id="b8fbd-113">It is inefficient to generate stub code for functions that will never be implemented in a particular client application.</span></span>

<span data-ttu-id="b8fbd-114">En définissant ces aspects locaux de votre interface dans un fichier de configuration d’application (ACF), vous pouvez séparer les différences entre les interfaces client de leur représentation réseau, ce qui permet au serveur d’envoyer et de recevoir des données dans un format cohérent, et de rendre votre code stub plus compact et efficace.</span><span class="sxs-lookup"><span data-stu-id="b8fbd-114">By defining these local aspects of your interface in an application configuration file (ACF), you can separate the differences between the client interfaces from their network representation, allowing the server to send and receive data in a consistent format, and making your stub code more compact and efficient.</span></span>

<span data-ttu-id="b8fbd-115">La structure et la syntaxe d’une définition d’interface ACF sont identiques à la définition IDL :</span><span class="sxs-lookup"><span data-stu-id="b8fbd-115">The structure and syntax of an ACF interface definition are identical to the IDL definition:</span></span>

``` syntax
[ interface-attribute-list] interface interface-name {. . .}
```

<span data-ttu-id="b8fbd-116">Par défaut, le nom de l’interface ACF doit correspondre à son nom dans la définition IDL.</span><span class="sxs-lookup"><span data-stu-id="b8fbd-116">By default, the ACF interface name must match its name in the IDL definition.</span></span> <span data-ttu-id="b8fbd-117">Toutefois, lorsque vous utilisez l’option/ [**ACF**](-acf.md) du compilateur MIDL pour spécifier explicitement un nom de fichier ACF, il n’est pas nécessaire que les noms d’interface correspondent.</span><span class="sxs-lookup"><span data-stu-id="b8fbd-117">However, when you use the MIDL compiler option / [**acf**](-acf.md) to explicitly specify an ACF file name, the interface names do not have to match.</span></span> <span data-ttu-id="b8fbd-118">Cette fonctionnalité permet à plusieurs interfaces de partager une seule spécification ACF.</span><span class="sxs-lookup"><span data-stu-id="b8fbd-118">This feature allows several interfaces to share a single ACF specification.</span></span>

 

 




