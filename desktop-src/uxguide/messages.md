---
title: Messages (concepts de base de la conception)
description: Les messages sont n’importe quel type de message dont les utilisateurs ont besoin ou souhaitent voir lorsqu’ils utilisent votre application. Découvrez comment présenter des erreurs, des avertissements, des confirmations et des notifications dans votre application.
ms.assetid: 700F1F1F-B41D-4C0A-B2EC-91C84E46E526
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dba3296c9824b2153184c45b6a021ea823b4d151
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106531444"
---
# <a name="messages-design-basics"></a><span data-ttu-id="3d89a-104">Messages (concepts de base de la conception)</span><span class="sxs-lookup"><span data-stu-id="3d89a-104">Messages (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="3d89a-105">Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="3d89a-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="3d89a-106">La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.</span><span class="sxs-lookup"><span data-stu-id="3d89a-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="3d89a-107">Les messages sont n’importe quel type de message dont les utilisateurs ont besoin ou souhaitent voir lorsqu’ils utilisent votre application.</span><span class="sxs-lookup"><span data-stu-id="3d89a-107">Messages are any kind of message users need or want to see as they use your app.</span></span> <span data-ttu-id="3d89a-108">Découvrez comment présenter des erreurs, des avertissements, des confirmations et des notifications dans votre application.</span><span class="sxs-lookup"><span data-stu-id="3d89a-108">Learn how to present errors, warning, confirmations, and notifications in your app.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3d89a-109">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="3d89a-109">In this section</span></span>



| <span data-ttu-id="3d89a-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="3d89a-110">Topic</span></span>                                        | <span data-ttu-id="3d89a-111">Description</span><span class="sxs-lookup"><span data-stu-id="3d89a-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d89a-112">Messages d’erreur</span><span class="sxs-lookup"><span data-stu-id="3d89a-112">Error Messages</span></span>](mess-error.md)<br/>  | <span data-ttu-id="3d89a-113">Un message d’erreur avertit les utilisateurs d’un problème qui s’est déjà produit.</span><span class="sxs-lookup"><span data-stu-id="3d89a-113">An error message alerts users of a problem that has already occurred.</span></span> <span data-ttu-id="3d89a-114">En revanche, un message d’avertissement avertit les utilisateurs d’une condition susceptible de provoquer un problème à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="3d89a-114">By contrast, a warning message alerts users of a condition that might cause a problem in the future.</span></span> <span data-ttu-id="3d89a-115">Des messages d’erreur peuvent être présentés à l’aide de boîtes de dialogue modales, de messages sur place, de notifications ou de bulles.</span><span class="sxs-lookup"><span data-stu-id="3d89a-115">Error messages can be presented using modal dialog boxes, in-place messages, notifications, or balloons.</span></span><br/>                                                  |
| [<span data-ttu-id="3d89a-116">Messages d’avertissement</span><span class="sxs-lookup"><span data-stu-id="3d89a-116">Warning Messages</span></span>](mess-warn.md)<br/> | <span data-ttu-id="3d89a-117">Un message d’avertissement est une boîte de dialogue modale, un message sur place, une notification ou une bulle qui avertit l’utilisateur d’une condition susceptible de provoquer un problème à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="3d89a-117">A warning message is a modal dialog box, in-place message, notification, or balloon that alerts the user of a condition that might cause a problem in the future.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="3d89a-118">Confirmations</span><span class="sxs-lookup"><span data-stu-id="3d89a-118">Confirmations</span></span>](mess-confirm.md)<br/> | <span data-ttu-id="3d89a-119">Une confirmation est une boîte de dialogue modale qui demande si l’utilisateur souhaite effectuer une action.</span><span class="sxs-lookup"><span data-stu-id="3d89a-119">A confirmation is a modal dialog box that asks if the user wants to proceed with an action.</span></span><br/>                                                                                                                                                                                                                                          |
| [<span data-ttu-id="3d89a-120">Notifications</span><span class="sxs-lookup"><span data-stu-id="3d89a-120">Notifications</span></span>](mess-notif.md)<br/>   | <span data-ttu-id="3d89a-121">Une notification informe les utilisateurs d’événements qui ne sont pas liés à l’activité de l’utilisateur actuel, en affichant brièvement une info-bulle à partir d’une icône dans la zone de notification.</span><span class="sxs-lookup"><span data-stu-id="3d89a-121">A notification informs users of events that are unrelated to the current user activity, by briefly displaying a balloon from an icon in the notification area.</span></span> <span data-ttu-id="3d89a-122">La notification peut être due à une action de l’utilisateur ou à un événement système significatif, ou peut fournir des informations potentiellement utiles à partir de Microsoft Windows ou d’une application.</span><span class="sxs-lookup"><span data-stu-id="3d89a-122">The notification could result from a user action or significant system event, or could offer potentially useful information from Microsoft Windows or an application.</span></span><br/> |



 

 

