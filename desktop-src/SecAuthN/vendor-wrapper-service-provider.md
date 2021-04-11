---
description: L’objectif du wrapper de fournisseur est d’encapsuler et d’utiliser les interfaces COM de bas niveau (fournies par les fabricants de cartes à puce) pour une carte à puce particulière. Ces interfaces ne sont pas fournies par Microsoft.
ms.assetid: 7bc26f7b-c355-448a-9f23-4ccfffea2fef
title: Fournisseur de services de wrappers de fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b7d22fea8e450111e1611f2ec069697c229a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112790"
---
# <a name="vendor-wrapper-service-provider"></a><span data-ttu-id="c944a-104">Fournisseur de services de wrappers de fournisseur</span><span class="sxs-lookup"><span data-stu-id="c944a-104">Vendor Wrapper Service Provider</span></span>

<span data-ttu-id="c944a-105">L’objectif du wrapper de fournisseur est d’encapsuler et d’utiliser les interfaces COM de bas niveau (fournies par les fabricants de cartes à puce) pour une carte à puce particulière.</span><span class="sxs-lookup"><span data-stu-id="c944a-105">The purpose of the vendor wrapper is to encapsulate and use the low-level COM interfaces (supplied by the smart card manufacturers) for a particular smart card.</span></span> <span data-ttu-id="c944a-106">Ces interfaces ne sont pas fournies par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c944a-106">These interfaces are not supplied by Microsoft.</span></span>

![Wrapper de fournisseur](images/scspart1.png)

<span data-ttu-id="c944a-108">Comme décrit dans la partie 6 de la *spécification d’interopérabilité pour les ICCS et les systèmes d’ordinateurs personnels* (consultez les spécifications à [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) l’adresse), la fonctionnalité exposée par ce wrapper est plus facile à utiliser que les fonctionnalités de quatre fournisseurs de services distincts.</span><span class="sxs-lookup"><span data-stu-id="c944a-108">As described in part 6 of the *Interoperability Specification for ICCs and Personal Computer Systems* (see specifications at [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/)), the functionality exposed by this wrapper is easier to use than the functionality of four separate service providers.</span></span> <span data-ttu-id="c944a-109">La fonctionnalité du wrapper peut être divisée en quatre zones principales :</span><span class="sxs-lookup"><span data-stu-id="c944a-109">The wrapper's functionality can be divided into four main areas:</span></span>

-   <span data-ttu-id="c944a-110">Services d’authentification par carte à puce, tels que l’authentification par stimulation et l’authentification par carte.</span><span class="sxs-lookup"><span data-stu-id="c944a-110">Smart card authentication services, such as get challenge and card authentication.</span></span>
-   <span data-ttu-id="c944a-111">Accès aux fichiers de carte à puce ou services de système de fichiers, tels que ouvrir, fermer, lire et écrire.</span><span class="sxs-lookup"><span data-stu-id="c944a-111">Smart card file access or file system services, such as open, close, read, and write.</span></span>
-   <span data-ttu-id="c944a-112">Gestion des cartes à puce, telle que l’attachement et le détachement.</span><span class="sxs-lookup"><span data-stu-id="c944a-112">Smart card management, such as attach and detach.</span></span>
-   <span data-ttu-id="c944a-113">Services de vérification de carte à puce, tels que vérifier et modifier le code.</span><span class="sxs-lookup"><span data-stu-id="c944a-113">Smart card verification services, such as verify and change code.</span></span>

> [!Note]  
> <span data-ttu-id="c944a-114">Cette spécification peut ne pas être disponible dans certains langages, pays ou régions.</span><span class="sxs-lookup"><span data-stu-id="c944a-114">This specification may not be available in some languages and countries or regions.</span></span>

 

<span data-ttu-id="c944a-115">La fonctionnalité est spécifique au type de carte utilisé (fonction prise en charge par la carte, protocoles, etc.) et sera différente pour chaque carte.</span><span class="sxs-lookup"><span data-stu-id="c944a-115">The functionality is specific to the type of card being used (which functions the card supports, protocols, and so on) and will be different for each card.</span></span>

<span data-ttu-id="c944a-116">L’exemple de wrapper Microsoft SCardCOM utilise la bibliothèque COM ATL pour implémenter un wrapper simple et définir un modèle pour d’autres wrappers.</span><span class="sxs-lookup"><span data-stu-id="c944a-116">The Microsoft SCardCOM example wrapper uses the ATL COM library to implement a simple wrapper and lay down a template for other wrappers.</span></span> <span data-ttu-id="c944a-117">Il implémente les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="c944a-117">It implements the following interfaces.</span></span>



| <span data-ttu-id="c944a-118">Interface ou objet</span><span class="sxs-lookup"><span data-stu-id="c944a-118">Interface or object</span></span>                                     | <span data-ttu-id="c944a-119">Description</span><span class="sxs-lookup"><span data-stu-id="c944a-119">Description</span></span>                         |
|---------------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="c944a-120">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="c944a-120">**ISCardAuth**</span></span>](iscardauth.md)<br/>             | <span data-ttu-id="c944a-121">Services d’authentification.</span><span class="sxs-lookup"><span data-stu-id="c944a-121">Authentication services.</span></span><br/> |
| [<span data-ttu-id="c944a-122">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="c944a-122">**ISCardFileAccess**</span></span>](iscardfileaccess.md)<br/> | <span data-ttu-id="c944a-123">Services du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c944a-123">File system services.</span></span><br/>    |
| [<span data-ttu-id="c944a-124">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="c944a-124">**ISCardManage**</span></span>](iscardmanage.md)<br/>         | <span data-ttu-id="c944a-125">Services de gestion.</span><span class="sxs-lookup"><span data-stu-id="c944a-125">Management services.</span></span><br/>     |
| [<span data-ttu-id="c944a-126">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="c944a-126">**ISCardVerify**</span></span>](iscardverify.md)<br/>         | <span data-ttu-id="c944a-127">Services de vérification.</span><span class="sxs-lookup"><span data-stu-id="c944a-127">Verification services.</span></span><br/>   |



 

> [!Note]  
> <span data-ttu-id="c944a-128">L’exemple SCardCOM est fourni uniquement comme exemple d’implémentation des interfaces de wrapper.</span><span class="sxs-lookup"><span data-stu-id="c944a-128">The SCardCOM example is provided only as an example of implementing the wrapper interfaces.</span></span> <span data-ttu-id="c944a-129">Pour éviter les conflits de noms de DLL avec d’autres fournisseurs, vous ne devez pas utiliser SCardCOM.dll comme nom des dll que vous créez.</span><span class="sxs-lookup"><span data-stu-id="c944a-129">To prevent DLL name collision with other vendors, you must not use SCardCOM.dll as the name of any DLLs you create.</span></span>

 

<span data-ttu-id="c944a-130">Voici une utilisation courante du wrapper du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c944a-130">Following is a typical use of the vendor wrapper.</span></span> <span data-ttu-id="c944a-131">Cet exemple utilise l’interface [**ISCardManage**](iscardmanage.md) pour créer des instances des interfaces qui seront encapsulées dans le fournisseur de services et l’interface [**ISCardVerify**](iscardverify.md) pour vérifier leur opération.</span><span class="sxs-lookup"><span data-stu-id="c944a-131">This example uses the [**ISCardManage**](iscardmanage.md) interface to create instances of the interfaces that will be wrapped into the service provider and the [**ISCardVerify**](iscardverify.md) interface to verify their operation.</span></span>

<span data-ttu-id="c944a-132">**Pour générer un fournisseur de services de wrapper**</span><span class="sxs-lookup"><span data-stu-id="c944a-132">**To build a wrapper service provider**</span></span>

1.  <span data-ttu-id="c944a-133">Créez une instance de l’interface [**ISCardManage**](iscardmanage.md) .</span><span class="sxs-lookup"><span data-stu-id="c944a-133">Create an instance of the [**ISCardManage**](iscardmanage.md) interface.</span></span> <span data-ttu-id="c944a-134">Utilisez cette interface pour créer une instance des interfaces requises (par exemple, [**ISCardFileAccess**](iscardfileaccess.md) ou [**ISCardVerify**](iscardverify.md)).</span><span class="sxs-lookup"><span data-stu-id="c944a-134">Use this interface to create an instance of required interfaces (for example, [**ISCardFileAccess**](iscardfileaccess.md) or [**ISCardVerify**](iscardverify.md)).</span></span> <span data-ttu-id="c944a-135">Lors de la création de ces interfaces, les interfaces COM de bas niveau correspondantes sont également créées.</span><span class="sxs-lookup"><span data-stu-id="c944a-135">When creating these interfaces, any corresponding low-level COM interfaces would also be created.</span></span>
2.  <span data-ttu-id="c944a-136">Connectez/Connectez-vous à une carte par le biais de la méthode [**ISCardManage**](iscardmanage.md) appropriée.</span><span class="sxs-lookup"><span data-stu-id="c944a-136">Attach/connect to a card through the appropriate [**ISCardManage**](iscardmanage.md) method.</span></span>
3.  <span data-ttu-id="c944a-137">Effectuez les opérations requises par le biais de la méthode [**ISCardVerify**](iscardverify.md) appropriée (qui peut appeler plusieurs méthodes et interfaces COM de bas niveau pour se terminer).</span><span class="sxs-lookup"><span data-stu-id="c944a-137">Perform required operations through the appropriate [**ISCardVerify**](iscardverify.md) method (which may call multiple low-level COM interfaces and methods to complete).</span></span>
4.  <span data-ttu-id="c944a-138">Répétez cette opération pour les autres opérations.</span><span class="sxs-lookup"><span data-stu-id="c944a-138">Repeat for other operations.</span></span>
5.  <span data-ttu-id="c944a-139">Mise en version terminée.</span><span class="sxs-lookup"><span data-stu-id="c944a-139">Release when complete.</span></span>

<span data-ttu-id="c944a-140">Le nom de l’interface COM et l’identificateur d’interface (GUID) ne doivent pas changer par rapport à ceux utilisés dans le wrapper de code ou d’exemple.</span><span class="sxs-lookup"><span data-stu-id="c944a-140">The COM interface name and interface identifier (GUID) should not change from those used in the code or example wrapper.</span></span> <span data-ttu-id="c944a-141">Toutefois, le GUID de la classe (autrement dit, où une implémentation réelle de l’interface réside) doit être modifié par rapport à ceux utilisés.</span><span class="sxs-lookup"><span data-stu-id="c944a-141">However, the class GUID (that is, where an actual implementation of an interface resides) must be changed from those used.</span></span> <span data-ttu-id="c944a-142">Cela est particulièrement important lors de l’implémentation d’un wrapper de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c944a-142">This is especially important when implementing a vendor wrapper.</span></span> <span data-ttu-id="c944a-143">Un exemple consiste à utiliser plusieurs wrappers de fournisseur sur un ordinateur particulier.</span><span class="sxs-lookup"><span data-stu-id="c944a-143">One example would be using multiple vendor wrappers on a particular computer.</span></span> <span data-ttu-id="c944a-144">Ces wrappers doivent implémenter les mêmes interfaces COM, mais utilisent toujours des stratégies d’implémentation différentes.</span><span class="sxs-lookup"><span data-stu-id="c944a-144">These wrappers should implement the same COM interfaces, but will always use different implementation strategies.</span></span> <span data-ttu-id="c944a-145">Par conséquent, des classes différentes (et des ID de classe) sont requises.</span><span class="sxs-lookup"><span data-stu-id="c944a-145">Therefore, different classes (and class IDs) are required.</span></span>

 

 




