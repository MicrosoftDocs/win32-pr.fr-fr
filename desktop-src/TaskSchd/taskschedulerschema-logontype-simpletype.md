---
title: Type simple logonType
description: Définit les valeurs possibles de l’élément LogonType.
ms.assetid: a08cd549-f45c-4278-a428-1ffe91b67564
keywords:
- Planificateur de tâches de type simple logonType
topic_type:
- apiref
api_name:
- logonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58d8c859502e81b5c5101adac3c8c26539870dd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105214"
---
# <a name="logontype-simple-type"></a><span data-ttu-id="52d4c-104">Type simple logonType</span><span class="sxs-lookup"><span data-stu-id="52d4c-104">logonType Simple Type</span></span>

<span data-ttu-id="52d4c-105">Définit les valeurs possibles de l’élément [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="52d4c-105">Defines the possible values of the [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="logonType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="S4U"
         />
        <xs:enumeration
            value="Password"
         />
        <xs:enumeration
            value="InteractiveToken"
         />
        <xs:enumeration
            value="InteractiveTokenOrPassword"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="52d4c-106">Valeurs d’énumération</span><span class="sxs-lookup"><span data-stu-id="52d4c-106">Enumeration values</span></span>

<span data-ttu-id="52d4c-107">Le type simple **LogonType** définit les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="52d4c-107">The **logonType** simple type defines the following values.</span></span>



| <span data-ttu-id="52d4c-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="52d4c-108">Value</span></span>                      | <span data-ttu-id="52d4c-109">Description</span><span class="sxs-lookup"><span data-stu-id="52d4c-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52d4c-110">S4U</span><span class="sxs-lookup"><span data-stu-id="52d4c-110">S4U</span></span>                        | <span data-ttu-id="52d4c-111">L’utilisateur doit se connecter à l’aide d’une connexion S4U (service for user).</span><span class="sxs-lookup"><span data-stu-id="52d4c-111">User must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="52d4c-112">Lorsqu’une ouverture de session S4U est utilisée, aucun mot de passe n’est stocké par le système et il n’y a aucun accès au réseau ou aux fichiers chiffrés.</span><span class="sxs-lookup"><span data-stu-id="52d4c-112">When an S4U logon is used, no password is stored by the system and there is no access to either the network or encrypted files.</span></span><br/>                                                                                                                                                          |
| <span data-ttu-id="52d4c-113">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="52d4c-113">Password</span></span>                   | <span data-ttu-id="52d4c-114">L’utilisateur doit se connecter à l’aide d’un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="52d4c-114">User must log on using a password.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="52d4c-115">InteractiveToken</span><span class="sxs-lookup"><span data-stu-id="52d4c-115">InteractiveToken</span></span>           | <span data-ttu-id="52d4c-116">L’utilisateur doit déjà avoir ouvert une session.</span><span class="sxs-lookup"><span data-stu-id="52d4c-116">User must already be logged on.</span></span> <span data-ttu-id="52d4c-117">La tâche est exécutée uniquement dans une session interactive existante.</span><span class="sxs-lookup"><span data-stu-id="52d4c-117">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="52d4c-118">InteractiveTokenOrPassword</span><span class="sxs-lookup"><span data-stu-id="52d4c-118">InteractiveTokenOrPassword</span></span> | <span data-ttu-id="52d4c-119">N’est plus utilisé ; actuellement identique au mot de passe.</span><span class="sxs-lookup"><span data-stu-id="52d4c-119">No longer in use; currently identical to Password.</span></span><br/> <span data-ttu-id="52d4c-120">**Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows Vista et Windows server 2008 :** La tâche est exécutée dans une session interactive existante ou l’utilisateur doit ouvrir une session à l’aide d’un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="52d4c-120">**Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows Vista and Windows Server 2008:** The task will be run in an existing interactive session or the user must log on using a password.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="52d4c-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52d4c-121">Requirements</span></span>



| <span data-ttu-id="52d4c-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52d4c-122">Requirement</span></span> | <span data-ttu-id="52d4c-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="52d4c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="52d4c-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52d4c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="52d4c-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52d4c-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="52d4c-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52d4c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="52d4c-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52d4c-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="52d4c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52d4c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52d4c-129">Types simples de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="52d4c-129">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="52d4c-130">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="52d4c-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





