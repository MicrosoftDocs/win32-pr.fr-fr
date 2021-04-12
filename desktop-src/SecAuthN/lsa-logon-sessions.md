---
description: Une session de connexion est une session de calcul qui commence lorsque l’authentification d’un utilisateur est réussie et se termine lorsque l’utilisateur se déconnecte du système.
ms.assetid: 14f0f9e7-90ba-47d7-a8d5-06f9d2f1a7a1
title: Sessions LSA Logon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32a4912218b68c25c5c23334f7b34ef875fa318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204167"
---
# <a name="lsa-logon-sessions"></a><span data-ttu-id="2f089-103">Sessions LSA Logon</span><span class="sxs-lookup"><span data-stu-id="2f089-103">LSA Logon Sessions</span></span>

<span data-ttu-id="2f089-104">Une [*session de connexion*](../secgloss/l-gly.md) est une session de calcul qui commence lorsque l’authentification d’un utilisateur est réussie et se termine lorsque l’utilisateur se déconnecte du système.</span><span class="sxs-lookup"><span data-stu-id="2f089-104">A [*logon session*](../secgloss/l-gly.md) is a computing session that begins when a user authentication is successful and ends when the user logs off of the system.</span></span>

<span data-ttu-id="2f089-105">Lorsqu’un utilisateur est authentifié avec succès, le package d’authentification crée une session de connexion et retourne des informations à l' [*autorité de sécurité locale*](../secgloss/l-gly.md) (LSA) qui est utilisée pour créer un [*jeton*](../secgloss/t-gly.md) pour le nouvel utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2f089-105">When a user is successfully authenticated, the authentication package creates a logon session and returns information to the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) that is used to create a [*token*](../secgloss/t-gly.md) for the new user.</span></span> <span data-ttu-id="2f089-106">Ce jeton comprend, entre autres choses, un [*identificateur unique local*](../secgloss/l-gly.md) (LUID) pour la session d’ouverture de session, appelé [*ID d’ouverture*](../secgloss/l-gly.md)de session.</span><span class="sxs-lookup"><span data-stu-id="2f089-106">This token includes, among other things, a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) for the logon session, called the [*logon Id*](../secgloss/l-gly.md).</span></span>

<span data-ttu-id="2f089-107">Lorsqu’un jeton est créé, le [*nombre de références*](../secgloss/r-gly.md) pour la session d’ouverture de session est incrémenté.</span><span class="sxs-lookup"><span data-stu-id="2f089-107">When a token is created, the [*reference count*](../secgloss/r-gly.md) for the logon session is incremented.</span></span> <span data-ttu-id="2f089-108">Le décompte de références est également incrémenté chaque fois que des copies du jeton sont créées pour la création du processus, l’emprunt d’identité ou d’autres utilisations.</span><span class="sxs-lookup"><span data-stu-id="2f089-108">The reference count is also incremented whenever copies of the token are created for process creation, impersonation, or other uses.</span></span> <span data-ttu-id="2f089-109">À mesure que les utilisations des jetons sont terminées et que des copies du jeton sont supprimées, le nombre de références pour la session d’ouverture de session est décrémenté.</span><span class="sxs-lookup"><span data-stu-id="2f089-109">As token uses are completed and copies of the token are deleted, the reference count for the logon session is decremented.</span></span> <span data-ttu-id="2f089-110">Lorsque le nombre de références atteint zéro, la session de connexion est supprimée.</span><span class="sxs-lookup"><span data-stu-id="2f089-110">When the reference count reaches zero, the logon session is deleted.</span></span>

> [!Note]  
> <span data-ttu-id="2f089-111">Si l’authentification échoue, le [*package d’authentification*](../secgloss/a-gly.md) ne doit pas créer de session de connexion.</span><span class="sxs-lookup"><span data-stu-id="2f089-111">If authentication is not successful, the [*authentication package*](../secgloss/a-gly.md) should not create a logon session.</span></span> <span data-ttu-id="2f089-112">Si le package d’authentification doit créer une session de connexion avant de procéder à une détermination finale de la validité de l’utilisateur, et si l’authentification échoue, le package d’authentification doit supprimer la session.</span><span class="sxs-lookup"><span data-stu-id="2f089-112">If the authentication package must create a logon session before making a final determination about the validity of the user, and if authentication fails, the authentication package must delete the session.</span></span>

 

 

 
