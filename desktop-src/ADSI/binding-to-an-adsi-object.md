---
title: Liaison à un objet ADSI
description: La connexion à un objet dans un service d’annuaire est connue sous le nom de liaison.
ms.assetid: f3963019-9b3a-42d5-a978-484f294110e5
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, utilisation, liaison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c0fefcdb62d374d98e3007864168e2626ecc5d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671182"
---
# <a name="binding-to-an-adsi-object"></a><span data-ttu-id="7ea30-104">Liaison à un objet ADSI</span><span class="sxs-lookup"><span data-stu-id="7ea30-104">Binding to an ADSI Object</span></span>

<span data-ttu-id="7ea30-105">La connexion à un objet dans un service d’annuaire est connue sous le nom de liaison.</span><span class="sxs-lookup"><span data-stu-id="7ea30-105">Connecting to an object in a directory service is known as binding.</span></span> <span data-ttu-id="7ea30-106">La liaison à un objet ADSI est la première étape de la communication avec le système d’annuaire sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="7ea30-106">Binding to an ADSI object is the first step to communicating with the underlying directory system.</span></span> <span data-ttu-id="7ea30-107">Un objet doit être lié pour pouvoir naviguer dans son espace de noms, Rechercher des données, modifier des données ou emprunter l’identité d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7ea30-107">An object must be bound to in order to navigate its namespace, search for data, modify data, or impersonate a user.</span></span> <span data-ttu-id="7ea30-108">Il est également possible de fournir des caractéristiques de liaison supplémentaires, telles que le nom d’utilisateur, le mot de passe, le nom du serveur, les méthodes de chiffrement et l’authentification sécurisée.</span><span class="sxs-lookup"><span data-stu-id="7ea30-108">It is also possible to supply additional binding characteristics, such as user name, password, server name, encryption methods, and secured authentication.</span></span> <span data-ttu-id="7ea30-109">Les caractéristiques de liaison supplémentaires réelles qui peuvent être utilisées dépendent du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="7ea30-109">The actual additional binding characteristics that can be used will depend on the provider.</span></span>

<span data-ttu-id="7ea30-110">Pour plus d’informations sur la liaison ADSI, consultez :</span><span class="sxs-lookup"><span data-stu-id="7ea30-110">For more information about ADSI binding, see:</span></span>

-   [<span data-ttu-id="7ea30-111">Chaîne de liaison</span><span class="sxs-lookup"><span data-stu-id="7ea30-111">Binding String</span></span>](binding-string.md)
-   [<span data-ttu-id="7ea30-112">Types de liaison spécifiques à Active Directory</span><span class="sxs-lookup"><span data-stu-id="7ea30-112">Binding Types Specific to Active Directory</span></span>](binding-types-specific-to-active-directory.md)
-   [<span data-ttu-id="7ea30-113">Problèmes de liaison pour les environnements mixtes</span><span class="sxs-lookup"><span data-stu-id="7ea30-113">Binding Issues for Mixed Environments</span></span>](binding-issues-for-mixed-environments.md)
-   [<span data-ttu-id="7ea30-114">Liaison par programme à l’aide d’une interface ADSI</span><span class="sxs-lookup"><span data-stu-id="7ea30-114">Binding Programmatically Using an ADSI Interface</span></span>](binding-programmatically-using-an-adsi-interface.md)
-   [<span data-ttu-id="7ea30-115">Mise en cache des connexions</span><span class="sxs-lookup"><span data-stu-id="7ea30-115">Connection Caching</span></span>](connection-caching.md)
-   [<span data-ttu-id="7ea30-116">Lier à des objets enfants</span><span class="sxs-lookup"><span data-stu-id="7ea30-116">Binding to Child Objects</span></span>](binding-to-child-objects.md)
-   [<span data-ttu-id="7ea30-117">Liaison au parent d’un objet</span><span class="sxs-lookup"><span data-stu-id="7ea30-117">Binding to an Object's Parent</span></span>](binding-to-an-objectampaposs-parent.md)
-   [<span data-ttu-id="7ea30-118">Option de liaison rapide pour les opérations d’écriture/modification par lots</span><span class="sxs-lookup"><span data-stu-id="7ea30-118">Fast Binding Option for Batch Write/Modify Operations</span></span>](fast-binding-option-for-batch-writemodify-operations.md)
-   [<span data-ttu-id="7ea30-119">Choix d’une interface pour la liaison</span><span class="sxs-lookup"><span data-stu-id="7ea30-119">Choosing an Interface for Binding</span></span>](choosing-an-interface.md)

 

 




