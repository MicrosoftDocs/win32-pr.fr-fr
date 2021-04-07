---
title: Dessin personnalisé
description: Le dessin personnalisé n’est pas un contrôle courant ; Il s’agit d’un service que de nombreux contrôles communs fournissent.
ms.assetid: vs|controls|~\controls\custdraw\custdraw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5184d06dbb8e04185bf12a43c6c71dd96b933a6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939765"
---
# <a name="custom-draw"></a><span data-ttu-id="bd7d1-103">Dessin personnalisé</span><span class="sxs-lookup"><span data-stu-id="bd7d1-103">Custom Draw</span></span>

<span data-ttu-id="bd7d1-104">Le dessin personnalisé n’est pas un contrôle courant ; Il s’agit d’un service que de nombreux contrôles communs fournissent.</span><span class="sxs-lookup"><span data-stu-id="bd7d1-104">Custom draw is not a common control; it is a service that many common controls provide.</span></span> <span data-ttu-id="bd7d1-105">Le service de dessin personnalisé permet à une application de bénéficier d’une plus grande souplesse dans la personnalisation de l’apparence d’un contrôle.</span><span class="sxs-lookup"><span data-stu-id="bd7d1-105">The custom draw service allows an application greater flexibility in customizing a control's appearance.</span></span> <span data-ttu-id="bd7d1-106">Votre application peut exploiter des notifications de dessin personnalisées pour modifier facilement la police utilisée pour afficher des éléments ou dessiner manuellement un élément sans avoir à effectuer une Owner Draw complète.</span><span class="sxs-lookup"><span data-stu-id="bd7d1-106">Your application can harness custom draw notifications to easily change the font used to display items or manually draw an item without having to do a full owner draw.</span></span>

<span data-ttu-id="bd7d1-107">Cette section contient des informations sur les éléments de programmation utilisés avec le dessin personnalisé.</span><span class="sxs-lookup"><span data-stu-id="bd7d1-107">This section contains information about the programming elements used with custom draw.</span></span>

## <a name="overviews"></a><span data-ttu-id="bd7d1-108">Vues d'ensemble</span><span class="sxs-lookup"><span data-stu-id="bd7d1-108">Overviews</span></span>



| <span data-ttu-id="bd7d1-109">Rubrique</span><span class="sxs-lookup"><span data-stu-id="bd7d1-109">Topic</span></span>                                      | <span data-ttu-id="bd7d1-110">Contenu</span><span class="sxs-lookup"><span data-stu-id="bd7d1-110">Contents</span></span>                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd7d1-111">À propos du dessin personnalisé</span><span class="sxs-lookup"><span data-stu-id="bd7d1-111">About Custom Draw</span></span>](about-custom-draw.md) | <span data-ttu-id="bd7d1-112">Cette section contient des informations générales sur la fonctionnalité de dessin personnalisée et fournit une vue d’ensemble conceptuelle de la façon dont une application peut prendre en charge le dessin personnalisé.</span><span class="sxs-lookup"><span data-stu-id="bd7d1-112">This section contains general information about custom draw functionality and provides a conceptual overview of how an application can support custom draw.</span></span><br/> |
| [<span data-ttu-id="bd7d1-113">Utilisation d’un dessin personnalisé</span><span class="sxs-lookup"><span data-stu-id="bd7d1-113">Using Custom Draw</span></span>](using-custom-draw.md) | <span data-ttu-id="bd7d1-114">Cette section contient des exemples qui montrent comment implémenter un dessin personnalisé.</span><span class="sxs-lookup"><span data-stu-id="bd7d1-114">This section contains examples that demonstrate how to implement custom draw.</span></span> <br/>                                                                              |



 

## <a name="notifications"></a><span data-ttu-id="bd7d1-115">Notifications</span><span class="sxs-lookup"><span data-stu-id="bd7d1-115">Notifications</span></span>



| <span data-ttu-id="bd7d1-116">Rubrique</span><span class="sxs-lookup"><span data-stu-id="bd7d1-116">Topic</span></span>                               | <span data-ttu-id="bd7d1-117">Contenu</span><span class="sxs-lookup"><span data-stu-id="bd7d1-117">Contents</span></span>                                                                                                                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd7d1-118">\_CUSTOMDRAW nm</span><span class="sxs-lookup"><span data-stu-id="bd7d1-118">NM\_CUSTOMDRAW</span></span>](nm-customdraw.md) | <span data-ttu-id="bd7d1-119">Avertit la fenêtre parente d’un contrôle des opérations de dessin personnalisées.</span><span class="sxs-lookup"><span data-stu-id="bd7d1-119">Notifies a control's parent window about custom drawing operations.</span></span> <span data-ttu-id="bd7d1-120">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bd7d1-120">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/> |



 

## <a name="structures"></a><span data-ttu-id="bd7d1-121">Structures</span><span class="sxs-lookup"><span data-stu-id="bd7d1-121">Structures</span></span>



| <span data-ttu-id="bd7d1-122">Rubrique</span><span class="sxs-lookup"><span data-stu-id="bd7d1-122">Topic</span></span>                                | <span data-ttu-id="bd7d1-123">Contenu</span><span class="sxs-lookup"><span data-stu-id="bd7d1-123">Contents</span></span>                                                                                              |
|--------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd7d1-124">**NMCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="bd7d1-124">**NMCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) | <span data-ttu-id="bd7d1-125">Contient des informations spécifiques à un code de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) .</span><span class="sxs-lookup"><span data-stu-id="bd7d1-125">Contains information specific to an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code.</span></span><br/> |



 

 

 





