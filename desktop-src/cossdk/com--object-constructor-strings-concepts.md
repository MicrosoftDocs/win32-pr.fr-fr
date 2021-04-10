---
description: Les chaînes de constructeur d’objet COM+ sont des chaînes d’initialisation qui sont spécifiées de manière administrative pour un composant.
ms.assetid: b4915dae-c97c-4d36-95ee-bb10dcb40845
title: Concepts des chaînes du constructeur d’objet COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32bffd35ad230efe1f22b52da10e1b4910d71da
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950524"
---
# <a name="com-object-constructor-strings-concepts"></a><span data-ttu-id="15232-103">Concepts des chaînes du constructeur d’objet COM+</span><span class="sxs-lookup"><span data-stu-id="15232-103">COM+ Object Constructor Strings Concepts</span></span>

<span data-ttu-id="15232-104">Les chaînes de constructeur d’objet COM+ sont des chaînes d’initialisation qui sont spécifiées de manière administrative pour un composant.</span><span class="sxs-lookup"><span data-stu-id="15232-104">COM+ object constructor strings are initialization strings that are administratively specified for a component.</span></span> <span data-ttu-id="15232-105">Vous pouvez utiliser des chaînes de constructeur d’objet pour écrire un composant unique avec un degré de généralisation qui lui permet d’être personnalisé par la suite pour une tâche particulière. autrement dit, vous pouvez effectuer la construction d’objets paramétrables.</span><span class="sxs-lookup"><span data-stu-id="15232-105">You can use object constructor strings to write a single component with a degree of generality that allows it to be later customized for a particular task; that is, you can perform parameterized object construction.</span></span>

<span data-ttu-id="15232-106">Par exemple, vous pouvez utiliser cette fonctionnalité pour écrire un composant qui détient une connexion ODBC générique et spécifier ultérieurement un DSN exact pour le composant de manière administrative.</span><span class="sxs-lookup"><span data-stu-id="15232-106">For example, you might use this feature to write a component that holds a generic ODBC connection and later specify an exact DSN for the component administratively.</span></span> <span data-ttu-id="15232-107">Si la configuration du système change, vous pouvez modifier la chaîne du constructeur en conséquence.</span><span class="sxs-lookup"><span data-stu-id="15232-107">If the system configuration changes, you can change the constructor string accordingly.</span></span>

> [!Note]  
> <span data-ttu-id="15232-108">Les chaînes de constructeur d’objet ne doivent pas être utilisées pour stocker des informations sensibles à la sécurité.</span><span class="sxs-lookup"><span data-stu-id="15232-108">Object constructor strings should not be used to store security-sensitive information.</span></span>

 

<span data-ttu-id="15232-109">Vous pouvez utiliser des chaînes de constructeur d’objet conjointement avec le [regroupement d’objets](com--object-pooling.md) pour obtenir un degré de granularité plus élevé de la façon dont vous regroupez et réutilisez les ressources.</span><span class="sxs-lookup"><span data-stu-id="15232-109">You can use object constructor strings in conjunction with [object pooling](com--object-pooling.md) to achieve a greater degree of granularity in how you pool and reuse resources.</span></span> <span data-ttu-id="15232-110">Par exemple, vous pouvez créer plusieurs composants distincts, identiques à l’exception des chaînes de constructeur et des CLSID, pour gérer des pools distincts d’objets contenant des connexions utilisables par des groupes de clients distincts.</span><span class="sxs-lookup"><span data-stu-id="15232-110">For example, you might create several distinct components, identical except for constructor strings and CLSIDs, to maintain distinct pools of objects holding connections usable by distinct groups of clients.</span></span> <span data-ttu-id="15232-111">Cela peut être utile si les connexions sont ouvertes d’une manière qui les lie à des rôles de sécurité particuliers, par exemple quand les connexions sont ouvertes avec une authentification spécifique au niveau de la base de données, ce qui les rend non réutilisables dans le cas général.</span><span class="sxs-lookup"><span data-stu-id="15232-111">This would be useful if connections are opened in a manner that binds them to particular security roles—such as when the connections are opened with some specific authentication at the database—rendering them non-reusable in the general case.</span></span>

<span data-ttu-id="15232-112">Pour ce faire, vous pouvez écrire un composant générique unique qui s’appuie sur les chaînes du constructeur de l’objet, à l’aide de [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct), puis le recompiler pour produire plusieurs composants personnalisables, chacun avec un CLSID distinct.</span><span class="sxs-lookup"><span data-stu-id="15232-112">To do this, you can write a single generic component that relies on object constructor strings, using [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct), and recompile it to produce several customizable components each with a distinct CLSID.</span></span> <span data-ttu-id="15232-113">Vous pouvez ensuite personnaliser de manière administrative chaque composant pour ouvrir une connexion appropriée avec une chaîne de constructeur, les configurer pour qu’ils soient regroupés, et ils seront conservés dans des pools distincts par CLSID.</span><span class="sxs-lookup"><span data-stu-id="15232-113">You can then administratively tailor each component to open an appropriate connection with a constructor string, configure them to be pooled, and they will be maintained in distinct pools per CLSID.</span></span>

<span data-ttu-id="15232-114">Vous pouvez spécifier une chaîne de constructeur lorsqu’un composant a été écrit spécifiquement pour reconnaître la chaîne que vous entrez.</span><span class="sxs-lookup"><span data-stu-id="15232-114">You can specify a constructor string when a component has been written specifically to recognize the string that you enter.</span></span> <span data-ttu-id="15232-115">Les composants peuvent accéder à ces chaînes par programmation à l’aide de [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct).</span><span class="sxs-lookup"><span data-stu-id="15232-115">Components can access these strings programmatically by using [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct).</span></span>

<span data-ttu-id="15232-116">Les chaînes de constructeur sont passées au moment de la création de l’objet uniquement lorsque la construction d’objet est activée administrativement.</span><span class="sxs-lookup"><span data-stu-id="15232-116">Constructor strings are passed in at object creation time only when object construction is administratively enabled.</span></span> <span data-ttu-id="15232-117">COM+ appelle la méthode [**IObjectConstruct :: Construct**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) qu’il implémente.</span><span class="sxs-lookup"><span data-stu-id="15232-117">COM+ calls the [**IObjectConstruct::Construct**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) method that it implements.</span></span> <span data-ttu-id="15232-118">Dans cette méthode, vous pouvez accéder à la chaîne du constructeur à l’aide de [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring).</span><span class="sxs-lookup"><span data-stu-id="15232-118">Within that method, you can access the constructor string by using [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring).</span></span> <span data-ttu-id="15232-119">Les chaînes vides peuvent être des entrées valides.</span><span class="sxs-lookup"><span data-stu-id="15232-119">Empty strings can be valid entries.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15232-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="15232-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15232-121">Mise en pool d’objets COM+</span><span class="sxs-lookup"><span data-stu-id="15232-121">COM+ Object Pooling</span></span>](com--object-pooling.md)
</dt> <dt>

[<span data-ttu-id="15232-122">Spécification d’une chaîne de constructeur d’objet pour un composant</span><span class="sxs-lookup"><span data-stu-id="15232-122">Specifying an Object Constructor String for a Component</span></span>](specifying-an-object-constructor-string-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="15232-123">Utilisation d’une chaîne de constructeur d’objet pour construire un composant</span><span class="sxs-lookup"><span data-stu-id="15232-123">Using an Object Constructor String to Construct a Component</span></span>](using-an-object-constructor-string-to-construct-a-component.md)
</dt> </dl>

 

 



