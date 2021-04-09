---
description: Les fonctions suivantes sont utilisées avec les Security Center Windows.
ms.assetid: FC28ACD2-A3C6-42A9-AE59-61892A139FB7
title: Fonctions Windows Security Center
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250d5b3dd7213d9d7f9363ce6b1a83a1e170e01a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846981"
---
# <a name="windows-security-center-functions"></a><span data-ttu-id="9d163-103">Fonctions Windows Security Center</span><span class="sxs-lookup"><span data-stu-id="9d163-103">Windows Security Center Functions</span></span>

<span data-ttu-id="9d163-104">Les fonctions suivantes sont utilisées avec les Security Center Windows.</span><span class="sxs-lookup"><span data-stu-id="9d163-104">The following functions are used with Windows Security Center.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9d163-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="9d163-105">In this section</span></span>



| <span data-ttu-id="9d163-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="9d163-106">Topic</span></span>                                                                           | <span data-ttu-id="9d163-107">Description</span><span class="sxs-lookup"><span data-stu-id="9d163-107">Description</span></span>                                                                                                                                                                              |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9d163-108">**WscGetSecurityProviderHealth**</span><span class="sxs-lookup"><span data-stu-id="9d163-108">**WscGetSecurityProviderHealth**</span></span>](/windows/desktop/api/Wscapi/nf-wscapi-wscgetsecurityproviderhealth)<br/> | <span data-ttu-id="9d163-109">Obtient l’état d’intégrité global des catégories de fournisseurs de sécurité représentées par les valeurs d’énumération du [**\_ \_ fournisseur de sécurité WSC**](/windows/desktop/api/Wscapi/ne-wscapi-wsc_security_provider) spécifiées.</span><span class="sxs-lookup"><span data-stu-id="9d163-109">Gets the aggregate health state of the security provider categories represented by the specified [**WSC\_SECURITY\_PROVIDER**](/windows/desktop/api/Wscapi/ne-wscapi-wsc_security_provider) enumeration values.</span></span><br/> |
| [<span data-ttu-id="9d163-110">**WscRegisterForChanges**</span><span class="sxs-lookup"><span data-stu-id="9d163-110">**WscRegisterForChanges**</span></span>](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges)<br/>               | <span data-ttu-id="9d163-111">Inscrit une fonction de rappel à exécuter lorsque Windows Security Center (WSC) détecte une modification susceptible d’affecter l’intégrité de l’un des fournisseurs de sécurité.</span><span class="sxs-lookup"><span data-stu-id="9d163-111">Registers a callback function to be run when Windows Security Center (WSC) detects a change that could affect the health of one of the security providers.</span></span><br/>                    |
| [<span data-ttu-id="9d163-112">**WscUnRegisterChanges**</span><span class="sxs-lookup"><span data-stu-id="9d163-112">**WscUnRegisterChanges**</span></span>](/windows/desktop/api/Wscapi/nf-wscapi-wscunregisterchanges)<br/>                 | <span data-ttu-id="9d163-113">Annule une inscription de rappel effectuée par un appel à la fonction [**WscRegisterForChanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges) .</span><span class="sxs-lookup"><span data-stu-id="9d163-113">Cancels a callback registration that was made by a call to the [**WscRegisterForChanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges) function.</span></span><br/>                                               |



 

 

 




