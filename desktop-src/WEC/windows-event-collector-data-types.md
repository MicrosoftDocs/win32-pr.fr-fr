---
title: Types de données du collecteur d’événements Windows (Evcoll. h)
description: Les types de données du collecteur d’événements Windows sont utilisés en tant que types de variables objet d’abonnement d’événement, types de paramètres de fonction et types de retour de fonction.
ms.assetid: b78bdaf8-e034-40fe-acf8-632313e4fd94
ms.tgt_platform: multiple
keywords:
- EC_HANDLE
- EC_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ccec141317644aa091eac44033b87b9e4495ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513760"
---
# <a name="windows-event-collector-data-types"></a><span data-ttu-id="61702-105">Types de données du collecteur d’événements Windows</span><span class="sxs-lookup"><span data-stu-id="61702-105">Windows Event Collector Data Types</span></span>

<span data-ttu-id="61702-106">Les types de données du collecteur d’événements Windows sont utilisés en tant que types de variables objet d’abonnement d’événement, types de paramètres de fonction et types de retour de fonction.</span><span class="sxs-lookup"><span data-stu-id="61702-106">The data types for the Windows Event Collector are used as event subscription object variable types, function parameter types, and function return types.</span></span>


```C++
typedef HANDLE EC_HANDLE;
typedef HANDLE EC_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

<span data-ttu-id="61702-107">**\_handle EC**</span><span class="sxs-lookup"><span data-stu-id="61702-107">**EC\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="61702-108">Handle vers un objet d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="61702-108">Handle to a subscription object.</span></span> <span data-ttu-id="61702-109">Utilisé pour représenter un abonnement au collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="61702-109">Used to represent an event collector subscription.</span></span>

</dd> <dt>

<span data-ttu-id="61702-110">**\_handle de \_ propriété du tableau d’objets EC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61702-110">**EC\_OBJECT\_ARRAY\_PROPERTY\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="61702-111">Handle vers un tableau de valeurs de propriété pour les sources d’événements d’un abonnement.</span><span class="sxs-lookup"><span data-stu-id="61702-111">Handle to an array of property values for the event sources of a subscription.</span></span> <span data-ttu-id="61702-112">Le descripteur de tableau est retourné par la méthode [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) lorsque la valeur **EcSubscriptionEventSources** est passée dans le paramètre *PropertyId* .</span><span class="sxs-lookup"><span data-stu-id="61702-112">The array handle is returned by the [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) method when the **EcSubscriptionEventSources** value is passed into the *PropertyId* parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61702-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61702-113">Requirements</span></span>



| <span data-ttu-id="61702-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61702-114">Requirement</span></span> | <span data-ttu-id="61702-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="61702-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="61702-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61702-116">Minimum supported client</span></span><br/> | <span data-ttu-id="61702-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61702-117">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="61702-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61702-118">Minimum supported server</span></span><br/> | <span data-ttu-id="61702-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61702-119">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="61702-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="61702-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="61702-121"><dt>Evcoll. h</dt></span><span class="sxs-lookup"><span data-stu-id="61702-121"><dt>Evcoll.h</dt></span></span> </dl> |



 

 





