---
title: Opérations d’Access Control et d’écriture
description: Les modifications de propriété échouent si l’appelant ne dispose pas de droits suffisants.
ms.assetid: eb5b97fb-4654-444e-9f5a-9a4be27ef1a3
ms.tgt_platform: multiple
keywords:
- Opérations de Access Control et d’écriture AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b8ecab475cd5696a98c985f92ccc24b1dd6072
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842010"
---
# <a name="access-control-and-write-operations"></a><span data-ttu-id="30900-104">Opérations d’Access Control et d’écriture</span><span class="sxs-lookup"><span data-stu-id="30900-104">Access Control and Write Operations</span></span>

<span data-ttu-id="30900-105">Les modifications de propriété échouent si l’appelant ne dispose pas de droits suffisants.</span><span class="sxs-lookup"><span data-stu-id="30900-105">Property modifications fail if the caller does not have sufficient rights.</span></span> <span data-ttu-id="30900-106">Pour les opérations d’écriture effectuées par lot sur plusieurs propriétés, la totalité de l’opération échoue si l’appelant n’a pas les droits nécessaires sur une seule des propriétés modifiées.</span><span class="sxs-lookup"><span data-stu-id="30900-106">For write operations that batch modifications to multiple properties, the entire operation fails if the caller does not have the necessary rights to a single one of the modified properties.</span></span> <span data-ttu-id="30900-107">Par exemple, vous pouvez effectuer plusieurs [**IAD : les appels :P ut**](/windows/desktop/api/iads/nf-iads-iads-put) pour définir plusieurs propriétés sur un objet.</span><span class="sxs-lookup"><span data-stu-id="30900-107">For example, you can make multiple [**IADs::Put**](/windows/desktop/api/iads/nf-iads-iads-put) calls to set multiple properties on an object.</span></span> <span data-ttu-id="30900-108">Toutefois, lorsque vous appelez [**IADs :: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) pour écrire les nouvelles données du cache local dans le répertoire, **setinfo** échoue si l’appelant ne dispose pas d’un accès en écriture à toutes les propriétés modifiées.</span><span class="sxs-lookup"><span data-stu-id="30900-108">However, when you call [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to write the new data from the local cache to the directory, **SetInfo** will fail if the caller does not have write access to all the modified properties.</span></span> <span data-ttu-id="30900-109">De même, la méthode [**IDirectoryObject :: SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) ne peut définir aucune propriété si l’appelant n’a pas accès à toutes les propriétés définies.</span><span class="sxs-lookup"><span data-stu-id="30900-109">Similarly, the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) method fails to set any properties if the caller does not have access to all the properties being set.</span></span> <span data-ttu-id="30900-110">Par conséquent, vous devez regrouper plusieurs opérations de modification uniquement si vous savez que toutes les modifications ont été effectuées.</span><span class="sxs-lookup"><span data-stu-id="30900-110">So you should batch multiple modify operations only if you know that all modifications will succeed.</span></span> <span data-ttu-id="30900-111">Pour déterminer les attributs d’un objet d’annuaire que l’appelant a la possibilité de modifier, lisez l’attribut **allowedAttributesEffective** de l’objet.</span><span class="sxs-lookup"><span data-stu-id="30900-111">To determine the attributes of a directory object that the caller has the ability to modify, read the object's **allowedAttributesEffective** attribute.</span></span>

<span data-ttu-id="30900-112">Si l’appelant ne dispose pas des droits suffisants pour modifier une propriété, les codes de retour suivants peuvent être retournés :</span><span class="sxs-lookup"><span data-stu-id="30900-112">If the caller does not have sufficient rights to modify a property, the following return codes may be returned:</span></span>

<span data-ttu-id="30900-113">\_propriété e ADS \_ non définie sur la \_ \_ \_ \_ propriété ADS \_ non \_ modifiée</span><span class="sxs-lookup"><span data-stu-id="30900-113">E\_ADS\_PROPERTY\_NOT\_SET E\_ADS\_PROPERTY\_NOT\_MODIFIED</span></span>

 

 