---
description: Instructions relatives à l’utilisation de l’API du gestionnaire d’autorisations pour créer un magasin de stratégies d’autorisation dans le script.
ms.assetid: bd9a995a-4195-4da4-a194-472448a0cb08
title: Création d’un magasin de stratégies d’autorisation dans le script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0cb35e8e998f95e99193d1dc5e8a74838b7efc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114539"
---
# <a name="creating-an-authorization-policy-store-in-script"></a><span data-ttu-id="f5771-103">Création d’un magasin de stratégies d’autorisation dans le script</span><span class="sxs-lookup"><span data-stu-id="f5771-103">Creating an Authorization Policy Store in Script</span></span>

<span data-ttu-id="f5771-104">Créer une stratégie d’autorisation avant ou pendant l’installation d’une application.</span><span class="sxs-lookup"><span data-stu-id="f5771-104">Create an authorization policy before or during the installation of an application.</span></span>

<span data-ttu-id="f5771-105">Lorsque vous utilisez l’API du gestionnaire d’autorisations pour créer une stratégie d’autorisation, suivez les instructions fournies dans les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="f5771-105">When you use the Authorization Manager API to create an authorization policy, follow the instructions provided in the following topics.</span></span>



| <span data-ttu-id="f5771-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="f5771-106">Topic</span></span>                                                                                                                  | <span data-ttu-id="f5771-107">Description</span><span class="sxs-lookup"><span data-stu-id="f5771-107">Description</span></span>                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5771-108">Création d’un objet du magasin de stratégies d’autorisation dans le script</span><span class="sxs-lookup"><span data-stu-id="f5771-108">Creating an Authorization Policy Store Object in Script</span></span>](creating-an-authorization-policy-store-object-in-script.md) | <span data-ttu-id="f5771-109">Un magasin de stratégies d’autorisation contient des informations sur la stratégie de sécurité d’une application ou d’un groupe d’applications.</span><span class="sxs-lookup"><span data-stu-id="f5771-109">An authorization policy store contains information about the security policy of an application or group of applications.</span></span>                                                                                                                                       |
| [<span data-ttu-id="f5771-110">Création d’un objet d’application dans un script</span><span class="sxs-lookup"><span data-stu-id="f5771-110">Creating an Application Object in Script</span></span>](creating-an-application-object-in-script.md)                               | <span data-ttu-id="f5771-111">Pour chaque application qui utilise un magasin de stratégies d’autorisation, vous devez créer un objet [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) et l’enregistrer dans un magasin de stratégies.</span><span class="sxs-lookup"><span data-stu-id="f5771-111">For each application that uses an authorization policy store, you must create an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object and save it to a policy store.</span></span>                                                                                                |
| [<span data-ttu-id="f5771-112">Définition des opérations dans le script</span><span class="sxs-lookup"><span data-stu-id="f5771-112">Defining Operations in Script</span></span>](defining-operations-in-script.md)                                                     | <span data-ttu-id="f5771-113">Une opération est une fonction ou une méthode de bas niveau d’une application.</span><span class="sxs-lookup"><span data-stu-id="f5771-113">An operation is a low-level function or method of an application.</span></span>                                                                                                                                                                                              |
| [<span data-ttu-id="f5771-114">Regroupement d’opérations en tâches dans un script</span><span class="sxs-lookup"><span data-stu-id="f5771-114">Grouping Operations into Tasks in Script</span></span>](grouping-operations-into-tasks-in-script.md)                               | <span data-ttu-id="f5771-115">Une tâche est une action de haut niveau que les utilisateurs d’une application doivent effectuer.</span><span class="sxs-lookup"><span data-stu-id="f5771-115">A task is a high-level action that users of an application need to complete.</span></span> <span data-ttu-id="f5771-116">Les tâches sont constituées d’opérations, qui sont des fonctions de bas niveau et des méthodes de l’application.</span><span class="sxs-lookup"><span data-stu-id="f5771-116">Tasks are made up of operations, which are low-level functions and methods of the application.</span></span>                                                                                    |
| [<span data-ttu-id="f5771-117">Regroupement de tâches en rôles dans le script</span><span class="sxs-lookup"><span data-stu-id="f5771-117">Grouping Tasks into Roles in Script</span></span>](grouping-tasks-into-roles-in-script.md)                                         | <span data-ttu-id="f5771-118">Un rôle représente une catégorie d’utilisateurs et les tâches que ces utilisateurs sont autorisés à effectuer.</span><span class="sxs-lookup"><span data-stu-id="f5771-118">A role represents a category of users and the tasks those users are authorized to perform.</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="f5771-119">Définition de groupes d’utilisateurs dans le script</span><span class="sxs-lookup"><span data-stu-id="f5771-119">Defining Groups of Users in Script</span></span>](defining-groups-of-users-in-script.md)                                           | <span data-ttu-id="f5771-120">Un objet [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) représente un groupe d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f5771-120">An [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object represents a group of users.</span></span> <span data-ttu-id="f5771-121">Les rôles peuvent ensuite être attribués à ce groupe d’utilisateurs de manière collective.</span><span class="sxs-lookup"><span data-stu-id="f5771-121">Roles can then be assigned to this group of users collectively.</span></span> <span data-ttu-id="f5771-122">Un objet **IAzApplicationGroup** peut également inclure d’autres objets **IAzApplicationGroup** en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="f5771-122">An **IAzApplicationGroup** object can also include other **IAzApplicationGroup** objects as members.</span></span> |
| [<span data-ttu-id="f5771-123">Ajout d’utilisateurs à un groupe d’applications dans le script</span><span class="sxs-lookup"><span data-stu-id="f5771-123">Adding Users to an Application Group in Script</span></span>](adding-users-to-an-application-group-in-script.md)                   | <span data-ttu-id="f5771-124">Un groupe d’applications est un groupe d’utilisateurs et de groupes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f5771-124">An application group is a group of users and user groups.</span></span> <span data-ttu-id="f5771-125">Comme un groupe d’applications peut contenir d’autres groupes d’applications, les groupes d’utilisateurs peuvent être imbriqués.</span><span class="sxs-lookup"><span data-stu-id="f5771-125">An application group can contain other application groups, so groups of users can be nested.</span></span> <span data-ttu-id="f5771-126">Un groupe d’applications est représenté par un objet [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .</span><span class="sxs-lookup"><span data-stu-id="f5771-126">An application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span>    |



 

 

 



