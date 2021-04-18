---
description: L’interface ITAttributeList fournit des méthodes pour obtenir et définir des attributs non interprétés.
ms.assetid: 12806c2e-615c-4d78-a4bb-5cc35ea21175
title: Interface ITAttributeList (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2afbc7ab447188943c0f02e6c5a664bbcc4c6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526659"
---
# <a name="itattributelist-interface"></a><span data-ttu-id="8d013-103">Interface ITAttributeList</span><span class="sxs-lookup"><span data-stu-id="8d013-103">ITAttributeList interface</span></span>

<span data-ttu-id="8d013-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8d013-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8d013-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="8d013-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8d013-106">L’interface **ITAttributeList** fournit des méthodes pour obtenir et définir des attributs non interprétés.</span><span class="sxs-lookup"><span data-stu-id="8d013-106">The **ITAttributeList** interface supplies methods for getting and setting of uninterpreted attributes.</span></span> <span data-ttu-id="8d013-107">En ce qui concerne la position des chaînes d’attributs dans un protocole SDP (session descripteur), consultez le paquet RFC 2327), les méthodes supposent que toutes les chaînes d’attribut existent juste avant que les attributs de média soient spécifiés et après tous les attributs communs.</span><span class="sxs-lookup"><span data-stu-id="8d013-107">Regarding the position of the attribute strings in a Session Descriptor Protocol (SDP, see RFC 2327) packet, the methods assume that all attribute strings exist just before the media attributes are specified and after all the common attributes.</span></span> <span data-ttu-id="8d013-108">L’interface **ITAttributeList** est créée en appelant **QueryInterface** sur [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span><span class="sxs-lookup"><span data-stu-id="8d013-108">The **ITAttributeList** interface is created by calling **QueryInterface** on [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span></span>

## <a name="members"></a><span data-ttu-id="8d013-109">Membres</span><span class="sxs-lookup"><span data-stu-id="8d013-109">Members</span></span>

<span data-ttu-id="8d013-110">L’interface **ITAttributeList** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="8d013-110">The **ITAttributeList** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="8d013-111">**ITAttributeList** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8d013-111">**ITAttributeList** also has these types of members:</span></span>

-   [<span data-ttu-id="8d013-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8d013-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8d013-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8d013-113">Methods</span></span>

<span data-ttu-id="8d013-114">L’interface **ITAttributeList** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8d013-114">The **ITAttributeList** interface has these methods.</span></span>



| <span data-ttu-id="8d013-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="8d013-115">Method</span></span>                                                          | <span data-ttu-id="8d013-116">Description</span><span class="sxs-lookup"><span data-stu-id="8d013-116">Description</span></span>                                             |
|:----------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="8d013-117">**Complémentaires**</span><span class="sxs-lookup"><span data-stu-id="8d013-117">**Add**</span></span>](itattributelist-add.md)                              | <span data-ttu-id="8d013-118">Ajoute l’attribut à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="8d013-118">Adds the attribute at the specified index.</span></span><br/>   |
| [<span data-ttu-id="8d013-119">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="8d013-119">**Delete**</span></span>](itattributelist-delete.md)                        | <span data-ttu-id="8d013-120">Supprime l’attribut à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="8d013-120">Deletes the attribute at the specified index</span></span><br/> |
| [<span data-ttu-id="8d013-121">**Obtient \_ AttributeList**</span><span class="sxs-lookup"><span data-stu-id="8d013-121">**get\_AttributeList**</span></span>](itattributelist-get-attributelist.md) | <span data-ttu-id="8d013-122">Obtient la liste des attributs.</span><span class="sxs-lookup"><span data-stu-id="8d013-122">Gets the list of attributes.</span></span><br/>                 |
| [<span data-ttu-id="8d013-123">**nombre d’extractions \_**</span><span class="sxs-lookup"><span data-stu-id="8d013-123">**get\_Count**</span></span>](itattributelist-get-count.md)                 | <span data-ttu-id="8d013-124">Obtient le nombre d'attributs.</span><span class="sxs-lookup"><span data-stu-id="8d013-124">Gets the number of attributes.</span></span><br/>               |
| [<span data-ttu-id="8d013-125">**recevoir un \_ élément**</span><span class="sxs-lookup"><span data-stu-id="8d013-125">**get\_Item**</span></span>](itattributelist-get-item.md)                   | <span data-ttu-id="8d013-126">Obtient l’attribut spécifié par l’index.</span><span class="sxs-lookup"><span data-stu-id="8d013-126">Gets the attribute specified by the index.</span></span><br/>   |
| [<span data-ttu-id="8d013-127">**put \_ AttributeList**</span><span class="sxs-lookup"><span data-stu-id="8d013-127">**put\_AttributeList**</span></span>](itattributelist-put-attributelist.md) | <span data-ttu-id="8d013-128">Définit la liste des attributs.</span><span class="sxs-lookup"><span data-stu-id="8d013-128">Sets the list of attributes.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="8d013-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d013-129">Requirements</span></span>



| <span data-ttu-id="8d013-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d013-130">Requirement</span></span> | <span data-ttu-id="8d013-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d013-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d013-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="8d013-132">TAPI version</span></span><br/> | <span data-ttu-id="8d013-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8d013-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8d013-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="8d013-134">Header</span></span><br/>       | <dl> <span data-ttu-id="8d013-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d013-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8d013-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8d013-136">Library</span></span><br/>      | <dl> <span data-ttu-id="8d013-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d013-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8d013-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8d013-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="8d013-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d013-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

