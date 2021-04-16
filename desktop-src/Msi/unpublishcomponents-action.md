---
description: L’action UnpublishComponents gère la désannonce des composants listés dans la table PublishComponent.
ms.assetid: 3e50f668-6d08-405e-a5a4-f422041ef0b1
title: Action UnpublishComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f58d9fff862295bcc06e61e1b35c05cdddb58daa
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104394039"
---
# <a name="unpublishcomponents-action"></a><span data-ttu-id="2196f-103">Action UnpublishComponents</span><span class="sxs-lookup"><span data-stu-id="2196f-103">UnpublishComponents Action</span></span>

<span data-ttu-id="2196f-104">L’action UnpublishComponents gère la désannonce des composants listés dans la table PublishComponent.</span><span class="sxs-lookup"><span data-stu-id="2196f-104">The UnpublishComponents action manages the unadvertisement of components listed in the PublishComponent table.</span></span> <span data-ttu-id="2196f-105">Il s’agit de composants pouvant être en panne dans d’autres produits.</span><span class="sxs-lookup"><span data-stu-id="2196f-105">These are components that may be faulted in by other products.</span></span> <span data-ttu-id="2196f-106">Cette action supprime les informations sur les composants publiés de la [table PublishComponent](publishcomponent-table.md) pour laquelle la fonctionnalité correspondante est actuellement sélectionnée pour être désinstallée.</span><span class="sxs-lookup"><span data-stu-id="2196f-106">This action removes information about published components from the [PublishComponent table](publishcomponent-table.md) for which the corresponding feature is currently selected to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="2196f-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="2196f-107">Sequence Restrictions</span></span>

<span data-ttu-id="2196f-108">Il n’existe aucune restriction de séquence.</span><span class="sxs-lookup"><span data-stu-id="2196f-108">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="2196f-109">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="2196f-109">ActionData Messages</span></span>



| <span data-ttu-id="2196f-110">Champ</span><span class="sxs-lookup"><span data-stu-id="2196f-110">Field</span></span> | <span data-ttu-id="2196f-111">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="2196f-111">Description of action data</span></span>                                   |
|-------|--------------------------------------------------------------|
| <span data-ttu-id="2196f-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="2196f-112">\[1\]</span></span> | <span data-ttu-id="2196f-113">GUID représentant l’ID de composant d’une fonctionnalité publiée.</span><span class="sxs-lookup"><span data-stu-id="2196f-113">GUID representing the component ID of an advertised feature.</span></span> |
| <span data-ttu-id="2196f-114">\[2\]</span><span class="sxs-lookup"><span data-stu-id="2196f-114">\[2\]</span></span> | <span data-ttu-id="2196f-115">Qualificateur de l’ID du composant.</span><span class="sxs-lookup"><span data-stu-id="2196f-115">Qualifier of the component ID.</span></span>                               |



 

