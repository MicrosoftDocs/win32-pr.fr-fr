---
title: Types complexes de schéma d’événement
description: Voici les types complexes définis par le schéma d’événement.
ms.assetid: bc995483-7e54-4224-a372-4e63b0dd764c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2844fef209aedf6819aeaa5a5b6b8a2d698b39a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511038"
---
# <a name="event-schema-complex-types"></a><span data-ttu-id="897e7-103">Types complexes de schéma d’événement</span><span class="sxs-lookup"><span data-stu-id="897e7-103">Event Schema Complex Types</span></span>

<span data-ttu-id="897e7-104">Voici les types complexes définis par le schéma d’événement.</span><span class="sxs-lookup"><span data-stu-id="897e7-104">The following are the complex types that the Event schema defines.</span></span>



| <span data-ttu-id="897e7-105">Type complexe</span><span class="sxs-lookup"><span data-stu-id="897e7-105">Complex type</span></span>                                                                       | <span data-ttu-id="897e7-106">Description</span><span class="sxs-lookup"><span data-stu-id="897e7-106">Description</span></span>                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="897e7-107">**ComplexDataType**</span><span class="sxs-lookup"><span data-stu-id="897e7-107">**ComplexDataType**</span></span>](eventschema-complexdatatype-complextype.md)                 | <span data-ttu-id="897e7-108">Définit une structure qui contient un ou plusieurs éléments de données.</span><span class="sxs-lookup"><span data-stu-id="897e7-108">Defines a structure that contains one or more data items.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="897e7-109">**DataType**</span><span class="sxs-lookup"><span data-stu-id="897e7-109">**DataType**</span></span>](eventschema-datafieldtype-complextype.md)                          | <span data-ttu-id="897e7-110">Définit un élément de données.</span><span class="sxs-lookup"><span data-stu-id="897e7-110">Defines a data item.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="897e7-111">**DebugDataType**</span><span class="sxs-lookup"><span data-stu-id="897e7-111">**DebugDataType**</span></span>](eventschema-debugdatatype-complextype.md)                     | <span data-ttu-id="897e7-112">Définit les données qui peuvent être journalisées pour les événements du préprocesseur de trace logiciel Windows (WPP).</span><span class="sxs-lookup"><span data-stu-id="897e7-112">Defines the data that can be logged for Windows software trace preprocessor (WPP) events.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="897e7-113">**EventDataType**</span><span class="sxs-lookup"><span data-stu-id="897e7-113">**EventDataType**</span></span>](eventschema-eventdatatype-complextype.md)                     | <span data-ttu-id="897e7-114">Définit les éléments de données d’événement et les structures qui contiennent les données d’événement.</span><span class="sxs-lookup"><span data-stu-id="897e7-114">Defines the event data items and structures that contains the event data.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="897e7-115">**Type d’événement**</span><span class="sxs-lookup"><span data-stu-id="897e7-115">**EventType**</span></span>](eventschema-eventtype-complextype.md)                             | <span data-ttu-id="897e7-116">Définit le nœud racine du schéma d’événement.</span><span class="sxs-lookup"><span data-stu-id="897e7-116">Defines the root node of the Event schema.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="897e7-117">**ProcessingErrorDataType**</span><span class="sxs-lookup"><span data-stu-id="897e7-117">**ProcessingErrorDataType**</span></span>](eventschema-processingerrordatatype-complextype.md) | <span data-ttu-id="897e7-118">Définit une erreur qui s’est produite lors du rendu des données d’événement pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="897e7-118">Defines an error that occurred while rendering the event data for the event.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="897e7-119">**RenderingInfoType**</span><span class="sxs-lookup"><span data-stu-id="897e7-119">**RenderingInfoType**</span></span>](eventschema-renderingtype-complextype.md)                 | <span data-ttu-id="897e7-120">Définit les messages rendus pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="897e7-120">Defines the rendered messages for the event.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="897e7-121">**SystemPropertiesType**</span><span class="sxs-lookup"><span data-stu-id="897e7-121">**SystemPropertiesType**</span></span>](eventschema-systempropertiestype-complextype.md)       | <span data-ttu-id="897e7-122">Définit les informations qui identifient le fournisseur et comment il a été activé, l’événement, le canal vers lequel l’événement a été écrit et les informations système telles que les ID de processus et de thread.</span><span class="sxs-lookup"><span data-stu-id="897e7-122">Defines the information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span><br/> |
| [<span data-ttu-id="897e7-123">**UserDataType**</span><span class="sxs-lookup"><span data-stu-id="897e7-123">**UserDataType**</span></span>](eventschema-userdatatype-complextype.md)                       | <span data-ttu-id="897e7-124">Définit un fragment XML qui spécifie la disposition des données d’événement.</span><span class="sxs-lookup"><span data-stu-id="897e7-124">Defines an XML fragment that specifies the layout of the event data.</span></span><br/>                                                                                                                           |



 

 

 





