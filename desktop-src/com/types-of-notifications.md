---
title: Types de notifications
description: Types de notifications
ms.assetid: 1e7f44ea-f4ac-457e-96a3-94036508d7b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21216ca99e1a606aaba793371ad6b8619d13f2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380215"
---
# <a name="types-of-notifications"></a><span data-ttu-id="3b166-103">Types de notifications</span><span class="sxs-lookup"><span data-stu-id="3b166-103">Types of Notifications</span></span>

<span data-ttu-id="3b166-104">Les notifications sont classées en trois groupes : document composé, données et vue.</span><span class="sxs-lookup"><span data-stu-id="3b166-104">Notifications fall into three groups: compound document, data, and view.</span></span> <span data-ttu-id="3b166-105">Un objet envoie des notifications de document composé en réponse à un changement de nom, d’enregistrement, de fermeture ou, dans le cas d’un lien, dont la source de lien est renommée.</span><span class="sxs-lookup"><span data-stu-id="3b166-105">An object sends compound document notifications in response to being renamed, saved, closed or, in the case of a link, having its link source renamed.</span></span> <span data-ttu-id="3b166-106">Comme vous pouvez vous y attendre, les objets envoient des notifications de données en réponse à des modifications de leurs données et envoient des notifications d’affichage en réponse aux modifications apportées à leur présentation.</span><span class="sxs-lookup"><span data-stu-id="3b166-106">As you would expect, objects send data notifications in response to changes in their data and send view notifications in response to changes in their presentation.</span></span> <span data-ttu-id="3b166-107">Les applications de conteneur doivent s’inscrire séparément pour chacun de ces types de notification, mais elles peuvent toutes être gérées par un seul récepteur de notifications.</span><span class="sxs-lookup"><span data-stu-id="3b166-107">Container applications must register separately for each of these notification types, but all can be handled by a single advisory sink.</span></span>

<span data-ttu-id="3b166-108">Tous les conteneurs, le gestionnaire d’objets et l’objet lié s’inscrivent pour les notifications de document composé.</span><span class="sxs-lookup"><span data-stu-id="3b166-108">All containers, the object handler, and the linked object register for compound document notifications.</span></span> <span data-ttu-id="3b166-109">Le conteneur standard s’inscrit également pour les notifications d’affichage.</span><span class="sxs-lookup"><span data-stu-id="3b166-109">The typical container also registers for view notifications.</span></span> <span data-ttu-id="3b166-110">Les notifications de données sont généralement envoyées à l’objet lié et au gestionnaire d’objets.</span><span class="sxs-lookup"><span data-stu-id="3b166-110">Data notifications are usually sent to both the linked object and object handler.</span></span> <span data-ttu-id="3b166-111">Un conteneur à usage spécial, tel qu’un conteneur qui restitue les données lui-même, peut tirer parti de la réception de notifications de données au lieu de notifications d’affichage.</span><span class="sxs-lookup"><span data-stu-id="3b166-111">A special purpose container, such as one that renders the data itself, might benefit from receiving data notifications instead of view notifications.</span></span> <span data-ttu-id="3b166-112">Par exemple, un conteneur de graphique incorporé avec un lien vers une table peut s’inscrire aux notifications de données.</span><span class="sxs-lookup"><span data-stu-id="3b166-112">For example, an embedded chart container with a link to a table can register for data notifications.</span></span> <span data-ttu-id="3b166-113">Comme une modification apportée à la table affecte le graphique, la réception d’une notification de données dirigerait le conteneur pour obtenir les nouvelles données tabulaires.</span><span class="sxs-lookup"><span data-stu-id="3b166-113">Because a change to the table affects the chart, the receipt of a data notification would direct the container to get the new tabular data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b166-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3b166-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b166-115">Notifications</span><span class="sxs-lookup"><span data-stu-id="3b166-115">Notifications</span></span>](notifications.md)
</dt> </dl>

 

 




