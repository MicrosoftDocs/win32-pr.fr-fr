---
title: Extensions de schéma
description: L’architecture du schéma ADSI fournit que de nouvelles classes de schéma peuvent être ajoutées au conteneur de classe de schéma et de nouvelles propriétés à un objet de classe de schéma existant au moment de l’exécution.
ms.assetid: 935d39ca-cfb9-4aa3-aa0e-b614f7b359f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b86491966e2bfddbef72d68d7a96869448c38188
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100557"
---
# <a name="schema-extensions"></a><span data-ttu-id="df03f-103">Extensions de schéma</span><span class="sxs-lookup"><span data-stu-id="df03f-103">Schema Extensions</span></span>

<span data-ttu-id="df03f-104">L’architecture du schéma ADSI fournit que de nouvelles classes de schéma peuvent être ajoutées au conteneur de classe de schéma et de nouvelles propriétés à un objet de classe de schéma existant au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="df03f-104">The architecture of the ADSI schema provides that new schema classes can be added to the schema class container and new properties to an existing schema class object at run time.</span></span> <span data-ttu-id="df03f-105">La dernière possibilité ne requiert pas de nouveau code.</span><span class="sxs-lookup"><span data-stu-id="df03f-105">The latter ability requires no new code.</span></span> <span data-ttu-id="df03f-106">Il s’agit d’une fonctionnalité importante pour les espaces de noms qui autorisent les services d’annuaire extensibles.</span><span class="sxs-lookup"><span data-stu-id="df03f-106">This is an important feature for namespaces that allow extensible directory services.</span></span> <span data-ttu-id="df03f-107">Le composant fournisseur doit autoriser cette extensibilité et savoir où accéder et stocker l’instance de classe et les valeurs de ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="df03f-107">The provider component must allow for this extensibility and know where to access and store the class instance and the values of its properties.</span></span> <span data-ttu-id="df03f-108">Dans un service d’annuaire extensible classique, ces informations sont stockées dans la base de données du service d’annuaire de la même manière que toute autre classe de schéma et définition de propriété.</span><span class="sxs-lookup"><span data-stu-id="df03f-108">In a typical extensible directory service, this information is stored in the directory service database in the same manner as any other schema class and property definitions.</span></span>

> [!Note]  
> <span data-ttu-id="df03f-109">Dans la terminologie de l’interface COM, seules les propriétés peuvent être ajoutées à une classe de schéma existante, et non à des méthodes.</span><span class="sxs-lookup"><span data-stu-id="df03f-109">In COM interface terminology, only properties can be added to an existing schema class, not methods.</span></span> <span data-ttu-id="df03f-110">L’ajout d’une nouvelle méthode nécessite l’ajout d’une nouvelle implémentation de cette méthode et nécessite donc du code supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="df03f-110">Adding a new method would require adding a new implementation of that method and thus require additional code.</span></span>

 

<span data-ttu-id="df03f-111">Pour obtenir un exemple de schéma de fournisseur spécifique, consultez [gestion des schémas](schema-management.md).</span><span class="sxs-lookup"><span data-stu-id="df03f-111">For an example of a specific provider schema, see [Schema Management](schema-management.md).</span></span>

 

 




