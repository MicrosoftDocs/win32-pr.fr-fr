---
title: Type simple sessionStateChangeType
description: Définit des valeurs pour le type de Terminal Server changement d’état de session que vous pouvez utiliser pour déclencher le démarrage d’une tâche.
ms.assetid: 56e19ec0-ea6c-4434-ab9d-a1069108920f
keywords:
- Planificateur de tâches de type simple sessionStateChangeType
topic_type:
- apiref
api_name:
- sessionStateChangeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a77fb563b59ccd8d63d38c6c85f16ff74ac404b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466415"
---
# <a name="sessionstatechangetype-simple-type"></a><span data-ttu-id="3d662-104">Type simple sessionStateChangeType</span><span class="sxs-lookup"><span data-stu-id="3d662-104">sessionStateChangeType Simple Type</span></span>

<span data-ttu-id="3d662-105">Définit des valeurs pour le type de Terminal Server changement d’état de session que vous pouvez utiliser pour déclencher le démarrage d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="3d662-105">Defines values for the kind of Terminal Server session state change you can use to trigger a task to start.</span></span>

``` syntax
<xs:simpleType name="sessionStateChangeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="ConsoleConnect"
         />
        <xs:enumeration
            value="ConsoleDisconnect"
         />
        <xs:enumeration
            value="RemoteConnect"
         />
        <xs:enumeration
            value="RemoteDisconnect"
         />
        <xs:enumeration
            value="SessionLock"
         />
        <xs:enumeration
            value="SessionUnlock"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="3d662-106">Valeurs d’énumération</span><span class="sxs-lookup"><span data-stu-id="3d662-106">Enumeration values</span></span>

<span data-ttu-id="3d662-107">Le type simple **sessionStateChangeType** définit les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="3d662-107">The **sessionStateChangeType** simple type defines the following values.</span></span>



| <span data-ttu-id="3d662-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d662-108">Value</span></span>             | <span data-ttu-id="3d662-109">Description</span><span class="sxs-lookup"><span data-stu-id="3d662-109">Description</span></span>                                                                                                                                                                                       |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d662-110">ConsoleConnect</span><span class="sxs-lookup"><span data-stu-id="3d662-110">ConsoleConnect</span></span>    | <span data-ttu-id="3d662-111">Modification de l’état de la connexion à la console Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="3d662-111">Terminal Server console connection state change.</span></span> <span data-ttu-id="3d662-112">Par exemple, lorsque vous vous connectez à une session utilisateur sur l’ordinateur local en basculant les utilisateurs sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3d662-112">For example, when you connect to a user session on the local computer by switching users on the computer.</span></span> <br/>                            |
| <span data-ttu-id="3d662-113">ConsoleDisconnect</span><span class="sxs-lookup"><span data-stu-id="3d662-113">ConsoleDisconnect</span></span> | <span data-ttu-id="3d662-114">Modification de l’état de déconnexion de la console Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="3d662-114">Terminal Server console disconnection state change.</span></span> <span data-ttu-id="3d662-115">Par exemple, lorsque vous vous déconnectez à une session utilisateur sur l’ordinateur local en basculant les utilisateurs sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3d662-115">For example, when you disconnect to a user session on the local computer by switching users on the computer.</span></span> <br/>                      |
| <span data-ttu-id="3d662-116">RemoteConnect</span><span class="sxs-lookup"><span data-stu-id="3d662-116">RemoteConnect</span></span>     | <span data-ttu-id="3d662-117">Terminal Server modification de l’état de la connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="3d662-117">Terminal Server remote connection state change.</span></span> <span data-ttu-id="3d662-118">Par exemple, lorsqu’un utilisateur se connecte à une session utilisateur à l’aide du programme Connexion Bureau à distance à partir d’un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="3d662-118">For example, when a user connects to a user session by using the Remote Desktop Connection program from a remote computer.</span></span> <br/>            |
| <span data-ttu-id="3d662-119">RemoteDisconnect</span><span class="sxs-lookup"><span data-stu-id="3d662-119">RemoteDisconnect</span></span>  | <span data-ttu-id="3d662-120">Terminal Server modification de l’état de la déconnexion distante.</span><span class="sxs-lookup"><span data-stu-id="3d662-120">Terminal Server remote disconnection state change.</span></span> <span data-ttu-id="3d662-121">Par exemple, lorsqu’un utilisateur se déconnecte d’une session utilisateur lors de l’utilisation du programme Connexion Bureau à distance à partir d’un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="3d662-121">For example, when a user disconnects from a user session while using the Remote Desktop Connection program from a remote computer.</span></span> <br/> |
| <span data-ttu-id="3d662-122">SessionLock</span><span class="sxs-lookup"><span data-stu-id="3d662-122">SessionLock</span></span>       | <span data-ttu-id="3d662-123">Terminal Server modification de l’état verrouillé de la session.</span><span class="sxs-lookup"><span data-stu-id="3d662-123">Terminal Server session locked state change.</span></span> <span data-ttu-id="3d662-124">Par exemple, ce changement d’État provoque l’exécution de la tâche lorsque l’ordinateur est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="3d662-124">For example, this state change causes the task to run when the computer is locked.</span></span> <br/>                                                       |
| <span data-ttu-id="3d662-125">SessionUnlock</span><span class="sxs-lookup"><span data-stu-id="3d662-125">SessionUnlock</span></span>     | <span data-ttu-id="3d662-126">Modification de l’état de déverrouillage de la session Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="3d662-126">Terminal Server session unlocked state change.</span></span> <span data-ttu-id="3d662-127">Par exemple, ce changement d’État provoque l’exécution de la tâche lorsque l’ordinateur est déverrouillé.</span><span class="sxs-lookup"><span data-stu-id="3d662-127">For example, this state change causes the task to run when the computer is unlocked.</span></span><br/>                                                    |



## <a name="requirements"></a><span data-ttu-id="3d662-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d662-128">Requirements</span></span>



| <span data-ttu-id="3d662-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d662-129">Requirement</span></span> | <span data-ttu-id="3d662-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d662-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3d662-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d662-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3d662-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d662-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3d662-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d662-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3d662-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d662-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





