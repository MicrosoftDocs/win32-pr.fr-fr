---
title: Type complexe networkSettingsType
description: Définit les éléments qui fournissent les paramètres utilisés par le service de Planificateur de tâches pour obtenir un profil réseau.
ms.assetid: e5df1dda-b691-47ff-a956-50ff1ce9c7cc
keywords:
- Planificateur de tâches de type complexe networkSettingsType
topic_type:
- apiref
api_name:
- networkSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2a8389b1e1f368bedf03fa38dce9c8e262a401
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942342"
---
# <a name="networksettingstype-complex-type"></a><span data-ttu-id="0316b-104">Type complexe networkSettingsType</span><span class="sxs-lookup"><span data-stu-id="0316b-104">networkSettingsType Complex Type</span></span>

<span data-ttu-id="0316b-105">Définit les éléments qui fournissent les paramètres utilisés par le service de Planificateur de tâches pour obtenir un profil réseau.</span><span class="sxs-lookup"><span data-stu-id="0316b-105">Defines the elements that provide the settings that the Task Scheduler service uses to obtain a network profile.</span></span>

``` syntax
<xs:complexType name="networkSettingsType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="Id"
            type="guidType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="0316b-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0316b-106">Child elements</span></span>



| <span data-ttu-id="0316b-107">Élément</span><span class="sxs-lookup"><span data-stu-id="0316b-107">Element</span></span>                                                              | <span data-ttu-id="0316b-108">Type</span><span class="sxs-lookup"><span data-stu-id="0316b-108">Type</span></span>                                                        | <span data-ttu-id="0316b-109">Description</span><span class="sxs-lookup"><span data-stu-id="0316b-109">Description</span></span>                                                                                 |
|----------------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0316b-110">**Identifi**</span><span class="sxs-lookup"><span data-stu-id="0316b-110">**Id**</span></span>](taskschedulerschema-id-networksettingstype-element.md)     | [<span data-ttu-id="0316b-111">**guidType**</span><span class="sxs-lookup"><span data-stu-id="0316b-111">**guidType**</span></span>](taskschedulerschema-guidtype-simpletype.md) | <span data-ttu-id="0316b-112">Spécifie une valeur GUID qui identifie un profil réseau.</span><span class="sxs-lookup"><span data-stu-id="0316b-112">Specifies a GUID value that identifies a network profile.</span></span> <br/>                       |
| [<span data-ttu-id="0316b-113">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0316b-113">**Name**</span></span>](taskschedulerschema-name-networksettingstype-element.md) | <span data-ttu-id="0316b-114">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="0316b-114">nonEmptyString</span></span>                                              | <span data-ttu-id="0316b-115">Spécifie le nom d’un profil réseau.</span><span class="sxs-lookup"><span data-stu-id="0316b-115">Specifies the name of a network profile.</span></span> <span data-ttu-id="0316b-116">Le nom est utilisé à des fins d’affichage.</span><span class="sxs-lookup"><span data-stu-id="0316b-116">The name is used for display purposes.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="0316b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0316b-117">Requirements</span></span>



| <span data-ttu-id="0316b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0316b-118">Requirement</span></span> | <span data-ttu-id="0316b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0316b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0316b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0316b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0316b-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0316b-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0316b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0316b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0316b-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0316b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





