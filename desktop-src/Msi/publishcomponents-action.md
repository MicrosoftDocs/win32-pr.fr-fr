---
description: L’action PublishComponents gère la publication des composants à partir de la table PublishComponent.
ms.assetid: 58d945d7-7dfb-4752-ae19-7e41caca1de7
title: Action PublishComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9c8967e737193922a9dbc3d9e03bc95131d5a63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864853"
---
# <a name="publishcomponents-action"></a><span data-ttu-id="ae125-103">Action PublishComponents</span><span class="sxs-lookup"><span data-stu-id="ae125-103">PublishComponents Action</span></span>

<span data-ttu-id="ae125-104">L’action PublishComponents gère la publication des composants à partir de la table [PublishComponent](publishcomponent-table.md) .</span><span class="sxs-lookup"><span data-stu-id="ae125-104">The PublishComponents action manages the advertisement of the components from the [PublishComponent](publishcomponent-table.md) table.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="ae125-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="ae125-105">Sequence Restrictions</span></span>

<span data-ttu-id="ae125-106">Il n’existe aucune restriction de séquence.</span><span class="sxs-lookup"><span data-stu-id="ae125-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="ae125-107">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="ae125-107">ActionData Messages</span></span>



| <span data-ttu-id="ae125-108">Champ</span><span class="sxs-lookup"><span data-stu-id="ae125-108">Field</span></span> | <span data-ttu-id="ae125-109">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="ae125-109">Description of action data</span></span>                                   |
|-------|--------------------------------------------------------------|
| <span data-ttu-id="ae125-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="ae125-110">\[1\]</span></span> | <span data-ttu-id="ae125-111">GUID représentant l’ID de composant d’une fonctionnalité publiée.</span><span class="sxs-lookup"><span data-stu-id="ae125-111">GUID representing the component ID of an advertised feature.</span></span> |
| <span data-ttu-id="ae125-112">\[2\]</span><span class="sxs-lookup"><span data-stu-id="ae125-112">\[2\]</span></span> | <span data-ttu-id="ae125-113">Qualificateur de l’ID du composant.</span><span class="sxs-lookup"><span data-stu-id="ae125-113">Qualifier of component ID.</span></span>                                   |



 

## <a name="remarks"></a><span data-ttu-id="ae125-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ae125-114">Remarks</span></span>

<span data-ttu-id="ae125-115">L’action PublishComponents publie tous les composants de la table PublishComponents qui appartiennent aux fonctionnalités sélectionnées pour la publication ou l’installation.</span><span class="sxs-lookup"><span data-stu-id="ae125-115">The PublishComponents action publishes all of the components from the PublishComponents table that belong to features that have been selected for advertisement or installation.</span></span>

 

 



