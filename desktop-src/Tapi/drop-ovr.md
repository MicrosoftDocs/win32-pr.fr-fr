---
description: La suppression ou la déconnexion d’une session met fin à la communication. L’application a la possibilité d’envoyer des informations utilisateur-utilisateur au moment de la déconnexion, si le fournisseur de services la prend en charge.
ms.assetid: dc348bb2-d564-40f8-afe3-5473c5769fa4
title: Supprimer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9bf3705d9b104b8816ce4b493ec6b188c5fe1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951064"
---
# <a name="drop"></a><span data-ttu-id="e0bc3-104">Supprimer</span><span class="sxs-lookup"><span data-stu-id="e0bc3-104">Drop</span></span>

<span data-ttu-id="e0bc3-105">La suppression ou la déconnexion d’une session met fin à la communication.</span><span class="sxs-lookup"><span data-stu-id="e0bc3-105">Dropping or disconnecting a session terminates communication.</span></span> <span data-ttu-id="e0bc3-106">L’application a la possibilité d’envoyer des informations utilisateur-utilisateur au moment de la déconnexion, si le fournisseur de services la prend en charge.</span><span class="sxs-lookup"><span data-stu-id="e0bc3-106">The application has the option of sending user-user information at the time of the disconnect, if the service provider supports it.</span></span>

<span data-ttu-id="e0bc3-107">Les raisons habituelles de la suppression d’une session sont qu’un utilisateur a demandé une déconnexion ou que l’autre extrémité de la session a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="e0bc3-107">The usual reasons for dropping a session is a user has requested a disconnect or the other end of the session has dropped.</span></span> <span data-ttu-id="e0bc3-108">Une opération Drop peut également être appelée lorsque l’interface TAPI offre une session à l’application.</span><span class="sxs-lookup"><span data-stu-id="e0bc3-108">A drop operation may also be called when TAPI offers a session to the application.</span></span> <span data-ttu-id="e0bc3-109">Si le fournisseur de services prend cela en charge, l’effet est que l’application rejette l’appel.</span><span class="sxs-lookup"><span data-stu-id="e0bc3-109">If the service provider supports this, the effect is that the application rejects the call.</span></span>

<span data-ttu-id="e0bc3-110">Lors de l’appel d’une opération de déplacement, les sessions associées peuvent parfois être affectées.</span><span class="sxs-lookup"><span data-stu-id="e0bc3-110">When invoking a drop operation, related sessions can sometimes be affected as well.</span></span> <span data-ttu-id="e0bc3-111">Par exemple, la suppression d’un appel de conférence peut supprimer tous les participants individuels.</span><span class="sxs-lookup"><span data-stu-id="e0bc3-111">For example, dropping a conference call can drop all individual participants.</span></span> <span data-ttu-id="e0bc3-112">Les messages de changement d’État sont envoyés à l’application pour tous les appels dont l’État est affecté.</span><span class="sxs-lookup"><span data-stu-id="e0bc3-112">State change messages are sent to the application for all calls whose state is affected.</span></span>

<span data-ttu-id="e0bc3-113">Dans les configurations par pont ou par ligne de tiers lorsque plusieurs tiers sont sur l’appel, une opération de suppression peut ne pas réellement effacer l’appel.</span><span class="sxs-lookup"><span data-stu-id="e0bc3-113">In various bridged or party-line configurations when multiple parties are on the call, a drop operation may not actually clear the call.</span></span> <span data-ttu-id="e0bc3-114">Par exemple, dans une situation de pont, l’appel ne peut pas être supprimé car l’état des autres stations sur l’appel peut être régi.</span><span class="sxs-lookup"><span data-stu-id="e0bc3-114">For example, in a bridged situation, the call may not be dropped because the status of other stations on the call may govern.</span></span> <span data-ttu-id="e0bc3-115">Au lieu de cela, l’appel peut simplement être remplacé par l’état inactif tout en restant connecté sur d’autres stations.</span><span class="sxs-lookup"><span data-stu-id="e0bc3-115">Instead, the call may simply be changed to the inactive state while remaining connected at other stations.</span></span>

<span data-ttu-id="e0bc3-116">Après une opération Drop, l’identificateur de session et la plupart des ressources associées à la session restent utilisables pour la plupart des opérations de requête.</span><span class="sxs-lookup"><span data-stu-id="e0bc3-116">Following a drop operation, the session identifier and most resources associated with the session will remain usable for most query operations.</span></span> <span data-ttu-id="e0bc3-117">Quand une application n’a plus besoin de ces ressources, elle doit [mettre fin à la session](terminate-a-session-ovr.md) afin d’éviter les fuites de mémoire.</span><span class="sxs-lookup"><span data-stu-id="e0bc3-117">When an application no longer requires these resources, it must [terminate the session](terminate-a-session-ovr.md) in order to avoid memory leaks.</span></span>

<span data-ttu-id="e0bc3-118">**TAPI 2. x :** Consultez [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop).</span><span class="sxs-lookup"><span data-stu-id="e0bc3-118">**TAPI 2.x:** See [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop).</span></span>

<span data-ttu-id="e0bc3-119">**TAPI 3. x :** Consultez [**ITBasicCallControl ::D éconnecter**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span><span class="sxs-lookup"><span data-stu-id="e0bc3-119">**TAPI 3.x:** See [**ITBasicCallControl::Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span></span>

 

 
