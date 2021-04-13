---
description: Les applications COM+ comportent un ou plusieurs composants COM.
ms.assetid: e7ed2844-276e-4726-952d-e4d3be2eb6e8
title: Parties d’une application COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f75aba454689e25e8706d4a7e3f059d498891f9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483032"
---
# <a name="parts-of-a-com-application"></a><span data-ttu-id="99e12-103">Parties d’une application COM+</span><span class="sxs-lookup"><span data-stu-id="99e12-103">Parts of a COM+ Application</span></span>

<span data-ttu-id="99e12-104">Les applications COM+ comportent un ou plusieurs composants COM.</span><span class="sxs-lookup"><span data-stu-id="99e12-104">COM+ applications consist of one or more COM components.</span></span>

<span data-ttu-id="99e12-105">Les termes suivants sont utilisés dans la documentation COM+ :</span><span class="sxs-lookup"><span data-stu-id="99e12-105">The following terms are used throughout the COM+ documentation:</span></span>

<dl> <dt>

<span data-ttu-id="99e12-106"><span id="COM_component"></span><span id="com_component"></span><span id="COM_COMPONENT"></span>*Composant COM*</span><span class="sxs-lookup"><span data-stu-id="99e12-106"><span id="COM_component"></span><span id="com_component"></span><span id="COM_COMPONENT"></span>*COM component*</span></span>
</dt> <dd>

<span data-ttu-id="99e12-107">Unité binaire de code qui crée des objets COM (y compris le code d’empaquetage et d’inscription).</span><span class="sxs-lookup"><span data-stu-id="99e12-107">A binary unit of code that creates COM objects (includes packaging and registration code).</span></span>

</dd> <dt>

<span data-ttu-id="99e12-108"><span id="COM_object"></span><span id="com_object"></span><span id="COM_OBJECT"></span>*Objet COM*</span><span class="sxs-lookup"><span data-stu-id="99e12-108"><span id="COM_object"></span><span id="com_object"></span><span id="COM_OBJECT"></span>*COM object*</span></span>
</dt> <dd>

<span data-ttu-id="99e12-109">Instance d’une classe COM.</span><span class="sxs-lookup"><span data-stu-id="99e12-109">An instance of a COM class.</span></span>

</dd> <dt>

<span data-ttu-id="99e12-110"><span id="COM_class"></span><span id="com_class"></span><span id="COM_CLASS"></span>*Classe COM*</span><span class="sxs-lookup"><span data-stu-id="99e12-110"><span id="COM_class"></span><span id="com_class"></span><span id="COM_CLASS"></span>*COM class*</span></span>
</dt> <dd>

<span data-ttu-id="99e12-111">Implémentation concrète nommée d’une ou de plusieurs interfaces.</span><span class="sxs-lookup"><span data-stu-id="99e12-111">A named, concrete implementation of one or more interfaces.</span></span> <span data-ttu-id="99e12-112">Une classe COM est identifiée par un CLSID (parfois par un ProgID également).</span><span class="sxs-lookup"><span data-stu-id="99e12-112">A COM class is identified by a CLSID (sometimes by a ProgID also).</span></span>

</dd> <dt>

<span data-ttu-id="99e12-113"><span id="COM_interface"></span><span id="com_interface"></span><span id="COM_INTERFACE"></span>*Interface COM*</span><span class="sxs-lookup"><span data-stu-id="99e12-113"><span id="COM_interface"></span><span id="com_interface"></span><span id="COM_INTERFACE"></span>*COM interface*</span></span>
</dt> <dd>

<span data-ttu-id="99e12-114">Groupe de fonctions de méthode associées exposées par une classe COM qui spécifient un contrat.</span><span class="sxs-lookup"><span data-stu-id="99e12-114">A group of related method functions exposed by a COM class that specify a contract.</span></span> <span data-ttu-id="99e12-115">Cela comprend le nom, la signature d’interface, la sémantique d’interface et le format de mémoire tampon de marshaling.</span><span class="sxs-lookup"><span data-stu-id="99e12-115">This includes the name, interface signature, interface semantics, and marshaling buffer format.</span></span> <span data-ttu-id="99e12-116">Une interface est identifiée par un IID.</span><span class="sxs-lookup"><span data-stu-id="99e12-116">An interface is identified by an IID.</span></span> <span data-ttu-id="99e12-117">La syntaxe de l’interface est définie dans les bibliothèques de types et/ou IDL.</span><span class="sxs-lookup"><span data-stu-id="99e12-117">The interface syntax is defined in IDL and/or type libraries.</span></span> <span data-ttu-id="99e12-118">Les interfaces d’une classe COM doivent être divisées en ensembles de méthodes gérables et cohésifs.</span><span class="sxs-lookup"><span data-stu-id="99e12-118">The interfaces of a COM class should be divided into manageable, cohesive sets of methods.</span></span>

<span data-ttu-id="99e12-119">Les interfaces COM sont immuables ; le contrat COM stipule qu’ils ne peuvent pas être modifiés.</span><span class="sxs-lookup"><span data-stu-id="99e12-119">COM interfaces are immutable; the COM contract states that they cannot be modified.</span></span> <span data-ttu-id="99e12-120">Toute modification (telle que l’ajout de méthodes) requiert la définition d’une nouvelle interface.</span><span class="sxs-lookup"><span data-stu-id="99e12-120">Any modification (such as adding methods) requires defining a new interface.</span></span>

</dd> <dt>

<span data-ttu-id="99e12-121"><span id="COM_method"></span><span id="com_method"></span><span id="COM_METHOD"></span>*Méthode COM*</span><span class="sxs-lookup"><span data-stu-id="99e12-121"><span id="COM_method"></span><span id="com_method"></span><span id="COM_METHOD"></span>*COM method*</span></span>
</dt> <dd>

<span data-ttu-id="99e12-122">Un des ensembles de fonctions connexes fournies par une interface COM.</span><span class="sxs-lookup"><span data-stu-id="99e12-122">One of a set of related functions provided by a COM interface.</span></span>

</dd> </dl>

## <a name="configured-and-unconfigured-components"></a><span data-ttu-id="99e12-123">Composants configurés et non configurés</span><span class="sxs-lookup"><span data-stu-id="99e12-123">Configured and Unconfigured Components</span></span>

<span data-ttu-id="99e12-124">Pour tirer parti des services pris en charge par les applications COM+, l’environnement COM+ impose des exigences spécifiques sur les composants COM créés pour les applications COM+.</span><span class="sxs-lookup"><span data-stu-id="99e12-124">To take advantage of the services that COM+ applications support, the COM+ environment imposes specific requirements on COM components built for COM+ applications.</span></span> <span data-ttu-id="99e12-125">Lorsqu’il est ajouté à une application COM+, un composant COM est appelé *composant configuré*.</span><span class="sxs-lookup"><span data-stu-id="99e12-125">When added to a COM+ application, a COM component is known as a *configured component*.</span></span>

<span data-ttu-id="99e12-126">Les composants COM générés pour les applications COM+ sont des composants serveur in-process.</span><span class="sxs-lookup"><span data-stu-id="99e12-126">COM components built for COM+ applications are in-process server components.</span></span> <span data-ttu-id="99e12-127">Le composant doit contenir une bibliothèque de types (fichier. tlb) pour décrire toutes les classes implémentées dans le composant et déclarer les interfaces sur toutes les classes du composant.</span><span class="sxs-lookup"><span data-stu-id="99e12-127">The component must contain a type library (.tlb file) to describe all classes implemented in the component and declare the interfaces on all classes in the component.</span></span> <span data-ttu-id="99e12-128">Vous pouvez créer et implémenter ces composants avec Microsoft Visual Basic, Microsoft Visual C++ ou n’importe quel outil de développement compatible COM.</span><span class="sxs-lookup"><span data-stu-id="99e12-128">You can create and implement these components with Microsoft Visual Basic, Microsoft Visual C++, or any COM-compatible development tool.</span></span>

<span data-ttu-id="99e12-129">Un *composant non configuré* est un composant qui n’est pas installé dans une application com+.</span><span class="sxs-lookup"><span data-stu-id="99e12-129">An *unconfigured component* is a component that isn't installed in a COM+ application.</span></span> <span data-ttu-id="99e12-130">Vous pouvez transformer les composants non configurés en composants configurés simplement en les intégrant dans une application COM+.</span><span class="sxs-lookup"><span data-stu-id="99e12-130">You can transform most unconfigured components into configured components simply by integrating them into a COM+ application.</span></span>

> [!Note]  
> <span data-ttu-id="99e12-131">N’utilisez pas la même AppID pour une application COM+ et dans le registre pour un composant non configuré.</span><span class="sxs-lookup"><span data-stu-id="99e12-131">Do not use the same AppID for both a COM+ application and in the registry for an unconfigured component.</span></span> <span data-ttu-id="99e12-132">Lorsque le composant non configuré est activé, l’activation peut récupérer les informations de l’application COM+ à partir du Registre qui ne contient pas les informations requises pour l’activation COM.</span><span class="sxs-lookup"><span data-stu-id="99e12-132">When the unconfigured component is activated , as activation may retrieve the COM+ application information from the registry that does not contain the information required for COM activation.</span></span> <span data-ttu-id="99e12-133">Des problèmes similaires peuvent survenir si un appel est passé à [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) à partir de Dllhost qui héberge une application serveur com+.</span><span class="sxs-lookup"><span data-stu-id="99e12-133">Similar problems could arise if a call is made to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) from DllHost that hosts COM+ Server application.</span></span>

 

 

 
