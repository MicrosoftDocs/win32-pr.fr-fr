---
description: L’interface IX509EndorsementKey expose les propriétés suivantes.
ms.assetid: 9E93622B-56E9-4F2F-9EFA-4F63D45EDCB6
title: Propriétés IX509EndorsementKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4bbdbc464803988f5b1100ac42fc0e3697fb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536482"
---
# <a name="ix509endorsementkey-properties"></a><span data-ttu-id="6678e-103">Propriétés IX509EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="6678e-103">IX509EndorsementKey Properties</span></span>

<span data-ttu-id="6678e-104">L’interface [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) expose les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6678e-104">The [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6678e-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="6678e-105">In this section</span></span>



| <span data-ttu-id="6678e-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="6678e-106">Topic</span></span>                                                                        | <span data-ttu-id="6678e-107">Description</span><span class="sxs-lookup"><span data-stu-id="6678e-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6678e-108">**Length, propriété**</span><span class="sxs-lookup"><span data-stu-id="6678e-108">**Length property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_length)<br/>             | <span data-ttu-id="6678e-109">Longueur en bits de la clé de type EK.</span><span class="sxs-lookup"><span data-stu-id="6678e-109">The bit length of the endorsement key.</span></span> <span data-ttu-id="6678e-110">Vous ne pouvez accéder à cette propriété qu’après l’appel de la méthode [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) .</span><span class="sxs-lookup"><span data-stu-id="6678e-110">You can only access this property after the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method has been called.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="6678e-111">**Propriété ouverte**</span><span class="sxs-lookup"><span data-stu-id="6678e-111">**Opened property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_opened)<br/>             | <span data-ttu-id="6678e-112">Indique si la méthode d' [**ouverture**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) a été appelée avec succès.</span><span class="sxs-lookup"><span data-stu-id="6678e-112">Indicates whether the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method has been successfully called.</span></span><br/>                                                                                                                                                                                                                                            |
| [<span data-ttu-id="6678e-113">**ProviderName, propriété**</span><span class="sxs-lookup"><span data-stu-id="6678e-113">**ProviderName property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername)<br/> | <span data-ttu-id="6678e-114">Nom du fournisseur de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="6678e-114">The name of the encryption provider.</span></span> <span data-ttu-id="6678e-115">La valeur par défaut est le fournisseur de chiffrement de la plateforme Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6678e-115">The default is the Microsoft Platform Crypto Provider.</span></span> <span data-ttu-id="6678e-116">Vous devez définir la propriété [**providerName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) avant d’appeler la méthode [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) .</span><span class="sxs-lookup"><span data-stu-id="6678e-116">You must set the [**ProviderName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) property before you call the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method.</span></span> <span data-ttu-id="6678e-117">Vous ne pouvez pas modifier la propriété **providerName** après avoir appelé la méthode **Open** .</span><span class="sxs-lookup"><span data-stu-id="6678e-117">You cannot change the **ProviderName** property after you have called the **Open** method.</span></span><br/> |



 

 

 




