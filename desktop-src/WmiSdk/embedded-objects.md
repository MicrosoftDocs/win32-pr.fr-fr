---
description: Un objet incorporé est un objet d’une classe qui existe dans une déclaration de classe ou d’instance d’une autre classe.
ms.assetid: 11a4556b-f682-4850-aedc-793602c5745b
ms.tgt_platform: multiple
title: Incorporation d’objets dans une classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39b94296a6869dddca7fd3df08739615a4a0c501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518821"
---
# <a name="embedding-objects-in-a-class"></a><span data-ttu-id="14042-103">Incorporation d’objets dans une classe</span><span class="sxs-lookup"><span data-stu-id="14042-103">Embedding Objects in a Class</span></span>

<span data-ttu-id="14042-104">Un objet incorporé est un objet d’une classe qui existe dans une déclaration de classe ou d’instance d’une autre classe.</span><span class="sxs-lookup"><span data-stu-id="14042-104">An embedded object is an object of a class that exists within a class or instance declaration of another class.</span></span> <span data-ttu-id="14042-105">Par exemple, la classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) contient des objets incorporés [**Win32 \_ Trusted**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) .</span><span class="sxs-lookup"><span data-stu-id="14042-105">For example, the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class contains [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) embedded objects.</span></span> <span data-ttu-id="14042-106">Chacun des objets **de \_ confiance Win32** contient un [**objet \_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .</span><span class="sxs-lookup"><span data-stu-id="14042-106">Each of the **Win32\_Trustee** objects contains a [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) object.</span></span> <span data-ttu-id="14042-107">WMI ne limite pas la profondeur à laquelle une classe peut avoir des objets incorporés.</span><span class="sxs-lookup"><span data-stu-id="14042-107">WMI does not limit the depth to which a class can have embedded objects.</span></span> <span data-ttu-id="14042-108">Toutefois, l’utilisation d’une autre conception, telle que la création d’une classe d’association, peut rendre un schéma plus gérable.</span><span class="sxs-lookup"><span data-stu-id="14042-108">However, using another design, such as creating an association class, may make a more manageable schema.</span></span>

<span data-ttu-id="14042-109">Pour plus d’informations sur les objets incorporés, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="14042-109">For more information about embedded objects, see the following topics:</span></span>

-   [<span data-ttu-id="14042-110">Création d’objets incorporés</span><span class="sxs-lookup"><span data-stu-id="14042-110">Creating Embedded Objects</span></span>](creating-embedded-objects.md)
-   [<span data-ttu-id="14042-111">Interrogation d’objets incorporés</span><span class="sxs-lookup"><span data-stu-id="14042-111">Querying Embedded Objects</span></span>](querying-embedded-objects.md)

## <a name="related-topics"></a><span data-ttu-id="14042-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="14042-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14042-113">Conception de classes format MOF (MOF)</span><span class="sxs-lookup"><span data-stu-id="14042-113">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
