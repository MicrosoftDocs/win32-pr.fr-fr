---
title: Access Control et création d’objets
description: Le serveur Active Directory ne parvient pas à créer un objet enfant si l’appelant ne dispose pas de l' \_ enfant ad droit \_ créer un \_ \_ enfant pour ce type d’objet sur le conteneur parent.
ms.assetid: 52f56e2a-580c-44b5-ba97-21388f6258bc
ms.tgt_platform: multiple
keywords:
- PUBLICITÉ pour la création de Access Control et d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ac54c1fe71a1821d3a02db383ca95606ae360d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101400"
---
# <a name="access-control-and-object-creation"></a><span data-ttu-id="489e5-104">Access Control et création d’objets</span><span class="sxs-lookup"><span data-stu-id="489e5-104">Access Control and Object Creation</span></span>

<span data-ttu-id="489e5-105">Le serveur Active Directory ne parvient pas à créer un objet enfant si l’appelant ne dispose pas de l' **\_ enfant ad droit \_ créer un \_ \_ enfant** pour ce type d’objet sur le conteneur parent.</span><span class="sxs-lookup"><span data-stu-id="489e5-105">The Active Directory server will fail to create a child object if the caller does not have the **ADS\_RIGHT\_DS\_CREATE\_CHILD** for that object type on the parent container.</span></span> <span data-ttu-id="489e5-106">Pour déterminer les types d’objets enfants que l’appelant peut créer dans un objet d’annuaire, lisez l’attribut **allowedChildClassesEffective** de l’objet.</span><span class="sxs-lookup"><span data-stu-id="489e5-106">To determine the types of child objects that the caller can create in a directory object, read the object's **allowedChildClassesEffective** attribute.</span></span>

<span data-ttu-id="489e5-107">Quand vous utilisez la méthode [**IADsContainer :: Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) pour créer un objet enfant, l’objet n’est pas rendu persistant tant que [**IADs :: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) n’est pas appelé sur le nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="489e5-107">When you use the [**IADsContainer::Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) method to create a child object, the object is not made persistent until [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) is called on the new object.</span></span> <span data-ttu-id="489e5-108">Entre les appels **Create** et **setinfo** , le thread de création peut placer des valeurs dans n’importe laquelle des propriétés de l’objet.</span><span class="sxs-lookup"><span data-stu-id="489e5-108">Between the **Create** and **SetInfo** calls, the creating thread can put values into any of the new object's properties.</span></span> <span data-ttu-id="489e5-109">Après l’appel de **setinfo** , le thread de création ne dispose pas nécessairement des droits d’accès nécessaires pour définir les propriétés du nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="489e5-109">After the **SetInfo** call, the creating thread does not necessarily have the access rights to set the new object's properties.</span></span> <span data-ttu-id="489e5-110">Pour vous assurer que l’appelant dispose de ces droits, spécifiez un descripteur de sécurité explicite lors de la création.</span><span class="sxs-lookup"><span data-stu-id="489e5-110">To ensure that the caller has these rights, specify an explicit security descriptor during creation.</span></span> <span data-ttu-id="489e5-111">La liste DACL doit avoir un ACE qui donne à l’appelant les droits d’accès nécessaires sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="489e5-111">The DACL should have an ACE that gives the caller the necessary access rights on the object.</span></span>

<span data-ttu-id="489e5-112">Pour plus d’informations sur le contrôle d’accès et la création d’objets, consultez [Comment les descripteurs de sécurité sont définis sur les nouveaux objets d’annuaire](how-security-descriptors-are-set-on-new-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="489e5-112">For more information about access control and object creation, see [How Security Descriptors are Set on New Directory Objects](how-security-descriptors-are-set-on-new-directory-objects.md).</span></span>

 

 