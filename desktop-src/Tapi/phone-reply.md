---
description: Le \_ message de réponse du téléphone TAPI est envoyé à une application pour signaler les résultats de l’appel de fonction qui s’est terminé de façon asynchrone.
ms.assetid: 434f37d6-f385-4cc9-9658-2b683cab532c
title: Message PHONE_REPLY (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091920c631bf56d58959d60288a1af039495d2d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540936"
---
# <a name="phone_reply-message"></a><span data-ttu-id="5d6dc-103">\_Message de réponse téléphonique</span><span class="sxs-lookup"><span data-stu-id="5d6dc-103">PHONE\_REPLY message</span></span>

<span data-ttu-id="5d6dc-104">Le message **de \_ réponse du téléphone** TAPI est envoyé à une application pour signaler les résultats de l’appel de fonction qui s’est terminé de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="5d6dc-104">The TAPI **PHONE\_REPLY** message is sent to an application to report the results of function call that completed asynchronously.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="5d6dc-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d6dc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d6dc-106">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="5d6dc-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="5d6dc-107">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="5d6dc-107">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="5d6dc-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="5d6dc-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="5d6dc-109">Retourne l’instance de rappel de l’application.</span><span class="sxs-lookup"><span data-stu-id="5d6dc-109">Returns the application's callback instance.</span></span>

</dd> <dt>

<span data-ttu-id="5d6dc-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="5d6dc-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="5d6dc-111">Identificateur de demande pour lequel il s’agit de la réponse.</span><span class="sxs-lookup"><span data-stu-id="5d6dc-111">The request identifier for which this is the reply.</span></span>

</dd> <dt>

<span data-ttu-id="5d6dc-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="5d6dc-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="5d6dc-113">Indication de réussite ou d’erreur.</span><span class="sxs-lookup"><span data-stu-id="5d6dc-113">The success or error indication.</span></span> <span data-ttu-id="5d6dc-114">L’application doit effectuer un cast de ce paramètre en LONG.</span><span class="sxs-lookup"><span data-stu-id="5d6dc-114">The application should cast this parameter into a LONG.</span></span> <span data-ttu-id="5d6dc-115">Zéro indique une réussite ; un nombre négatif indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="5d6dc-115">Zero indicates success; a negative number indicates an error.</span></span>

</dd> <dt>

<span data-ttu-id="5d6dc-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="5d6dc-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="5d6dc-117">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="5d6dc-117">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d6dc-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d6dc-118">Return value</span></span>

<span data-ttu-id="5d6dc-119">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="5d6dc-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d6dc-120">Notes</span><span class="sxs-lookup"><span data-stu-id="5d6dc-120">Remarks</span></span>

<span data-ttu-id="5d6dc-121">Les fonctions qui exécutent de façon asynchrone renvoient une valeur d’identificateur de demande positive à l’application.</span><span class="sxs-lookup"><span data-stu-id="5d6dc-121">Functions that operate asynchronously return a positive request identifier value to the application.</span></span> <span data-ttu-id="5d6dc-122">Cet identificateur de demande est retourné avec le message de réponse pour identifier la demande qui a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="5d6dc-122">This request identifier is returned with the reply message to identify the request that was completed.</span></span> <span data-ttu-id="5d6dc-123">L’autre paramètre du message **de \_ réponse téléphonique** porte l’indication de réussite ou d’échec.</span><span class="sxs-lookup"><span data-stu-id="5d6dc-123">The other parameter for the **PHONE\_REPLY** message carries the success or failure indication.</span></span> <span data-ttu-id="5d6dc-124">Les erreurs possibles sont les mêmes que celles définies par la fonction correspondante.</span><span class="sxs-lookup"><span data-stu-id="5d6dc-124">Possible errors are the same as those defined by the corresponding function.</span></span> <span data-ttu-id="5d6dc-125">Ce message ne peut pas être désactivé.</span><span class="sxs-lookup"><span data-stu-id="5d6dc-125">This message cannot be disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d6dc-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d6dc-126">Requirements</span></span>



| <span data-ttu-id="5d6dc-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d6dc-127">Requirement</span></span> | <span data-ttu-id="5d6dc-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d6dc-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5d6dc-129">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="5d6dc-129">TAPI version</span></span><br/> | <span data-ttu-id="5d6dc-130">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5d6dc-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5d6dc-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d6dc-131">Header</span></span><br/>       | <dl> <span data-ttu-id="5d6dc-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d6dc-132"><dt>Tapi.h</dt></span></span> </dl> |



 

 




