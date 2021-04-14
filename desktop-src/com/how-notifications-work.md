---
title: Fonctionnement des notifications
description: Fonctionnement des notifications
ms.assetid: faf66654-8233-49ac-a0fa-6cae51df0bea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9665b327d164a4e105f8adba3328be284fbe1fa0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382991"
---
# <a name="how-notifications-work"></a><span data-ttu-id="53abe-103">Fonctionnement des notifications</span><span class="sxs-lookup"><span data-stu-id="53abe-103">How Notifications Work</span></span>

<span data-ttu-id="53abe-104">Les notifications proviennent de l’application d’objet et sont acheminées vers le conteneur par le biais du gestionnaire d’objets.</span><span class="sxs-lookup"><span data-stu-id="53abe-104">Notifications originate in the object application and flow to the container by way of the object handler.</span></span> <span data-ttu-id="53abe-105">Si l’objet est un objet lié, l’objet lié intercepte les notifications du gestionnaire d’objets et notifie le conteneur directement.</span><span class="sxs-lookup"><span data-stu-id="53abe-105">If the object is a linked object, the linked object intercepts the notifications from the object handler and notifies the container directly.</span></span>

<span data-ttu-id="53abe-106">Une application d’objet doit gérer les demandes d’inscription, en effectuant le suivi de l’emplacement des notifications et de l’envoi de ces notifications, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="53abe-106">An object application must manage registration requests, keeping track of where to send which notifications and sending those notifications when appropriate.</span></span> <span data-ttu-id="53abe-107">OLE fournit deux objets de composant pour simplifier cette tâche : OleAdviseHolder pour les notifications de document composé et DataAdviseHolder pour les notifications de données.</span><span class="sxs-lookup"><span data-stu-id="53abe-107">OLE provides two component objects to simplify this task: the OleAdviseHolder for compound document notifications and the DataAdviseHolder for data notifications.</span></span>

<span data-ttu-id="53abe-108">Les applications d’objet déterminent les conditions qui demandent à l’envoi de chaque notification spécifique et la fréquence à laquelle chaque notification doit être envoyée.</span><span class="sxs-lookup"><span data-stu-id="53abe-108">Object applications determine the conditions that prompt the sending of each specific notification and the frequency with which each notification should be sent.</span></span> <span data-ttu-id="53abe-109">Lorsqu’il convient d’envoyer plusieurs notifications, il n’est pas important que la notification soit envoyée en premier ; ils peuvent être envoyés dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="53abe-109">When it is appropriate for multiple notifications to be sent, it does not matter which notification is sent first; they can be sent in any order.</span></span>

<span data-ttu-id="53abe-110">Le minutage des notifications affecte les performances et la coordination entre une application d’objet et ses conteneurs.</span><span class="sxs-lookup"><span data-stu-id="53abe-110">The timing of notifications affects the performance and coordination between an object application and its containers.</span></span> <span data-ttu-id="53abe-111">Alors que les notifications envoyées sont trop lentes, les notifications envoyées trop rarement génèrent un conteneur hors synchronisation.</span><span class="sxs-lookup"><span data-stu-id="53abe-111">Whereas notifications sent too frequently slow processing, notifications sent too infrequently result in an out-of-sync container.</span></span> <span data-ttu-id="53abe-112">La fréquence de notification peut être comparée à la fréquence à laquelle une application est redessinée.</span><span class="sxs-lookup"><span data-stu-id="53abe-112">Notification frequency can be compared with the rate at which an application repaints.</span></span> <span data-ttu-id="53abe-113">Par conséquent, l’utilisation d’une logique similaire pour le minutage des notifications (comme utilisé pour le redessin) est judicieuse.</span><span class="sxs-lookup"><span data-stu-id="53abe-113">Therefore, using similar logic for the timing of notifications (as is used for repainting) is wise.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53abe-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="53abe-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53abe-115">**CreateDataAdviseHolder**</span><span class="sxs-lookup"><span data-stu-id="53abe-115">**CreateDataAdviseHolder**</span></span>](/windows/win32/api/ole2/nf-ole2-createdataadviseholder)
</dt> <dt>

[<span data-ttu-id="53abe-116">**CreateOleAdviseHolder**</span><span class="sxs-lookup"><span data-stu-id="53abe-116">**CreateOleAdviseHolder**</span></span>](/windows/desktop/api/Ole2/nf-ole2-createoleadviseholder)
</dt> <dt>

[<span data-ttu-id="53abe-117">Notifications</span><span class="sxs-lookup"><span data-stu-id="53abe-117">Notifications</span></span>](notifications.md)
</dt> </dl>

 

 