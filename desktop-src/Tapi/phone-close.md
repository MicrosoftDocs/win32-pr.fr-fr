---
description: Le message de fermeture du téléphone TAPI \_ est envoyé lorsqu’un appareil téléphonique ouvert a été fermé de force dans le cadre de la récupération des ressources. Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.
ms.assetid: 84650abf-235e-4792-a67d-2f0f08b85a32
title: Message PHONE_CLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9a7641b437a10098806fc7ad52aa64200ca015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523656"
---
# <a name="phone_close-message"></a><span data-ttu-id="82fb5-104">Message de fermeture du téléphone \_</span><span class="sxs-lookup"><span data-stu-id="82fb5-104">PHONE\_CLOSE message</span></span>

<span data-ttu-id="82fb5-105">Le message **de \_ fermeture du téléphone** TAPI est envoyé lorsqu’un appareil téléphonique ouvert a été fermé de force dans le cadre de la récupération des ressources.</span><span class="sxs-lookup"><span data-stu-id="82fb5-105">The TAPI **PHONE\_CLOSE** message is sent when an open phone device has been forcibly closed as part of resource reclamation.</span></span> <span data-ttu-id="82fb5-106">Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="82fb5-106">The device handle is no longer valid once this message has been sent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="82fb5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82fb5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82fb5-108">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="82fb5-108">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="82fb5-109">Handle vers l’appareil téléphonique ouvert qui a été fermé.</span><span class="sxs-lookup"><span data-stu-id="82fb5-109">A handle to the open phone device that was closed.</span></span> <span data-ttu-id="82fb5-110">Le descripteur n’est plus valide une fois que ce message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="82fb5-110">The handle is no longer valid after this message has been sent.</span></span>

</dd> <dt>

<span data-ttu-id="82fb5-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="82fb5-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="82fb5-112">Instance de rappel de l’application fournie lors de l’ouverture du périphérique téléphonique.</span><span class="sxs-lookup"><span data-stu-id="82fb5-112">The application's callback instance that provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="82fb5-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="82fb5-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="82fb5-114">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="82fb5-114">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="82fb5-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="82fb5-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="82fb5-116">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="82fb5-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="82fb5-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="82fb5-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="82fb5-118">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="82fb5-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82fb5-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="82fb5-119">Return value</span></span>

<span data-ttu-id="82fb5-120">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="82fb5-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82fb5-121">Notes</span><span class="sxs-lookup"><span data-stu-id="82fb5-121">Remarks</span></span>

<span data-ttu-id="82fb5-122">Le message de **\_ fermeture du téléphone** est envoyé à une application uniquement après la fermeture forcée d’un téléphone ouvert.</span><span class="sxs-lookup"><span data-stu-id="82fb5-122">The **PHONE\_CLOSE** message is only sent to an application after an open phone has been forcibly closed.</span></span> <span data-ttu-id="82fb5-123">Cela peut être fait pour empêcher une seule application de monopoliser un appareil téléphonique pendant trop longtemps.</span><span class="sxs-lookup"><span data-stu-id="82fb5-123">This can be done to prevent a single application from monopolizing a phone device for too long.</span></span> <span data-ttu-id="82fb5-124">Si le téléphone peut être rouvert immédiatement après une fermeture forcée est spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="82fb5-124">Whether the phone can be reopened immediately after a forced close is device specific.</span></span>

<span data-ttu-id="82fb5-125">Un appareil téléphonique ouvert peut également être fermé de force une fois que l’utilisateur a modifié la configuration de ce téléphone ou de son pilote.</span><span class="sxs-lookup"><span data-stu-id="82fb5-125">An open phone device can also be forcibly closed after the user has modified the configuration of that phone or its driver.</span></span> <span data-ttu-id="82fb5-126">Si l’utilisateur souhaite que les modifications de configuration soient effectives immédiatement (par opposition à après le redémarrage du système suivant), et que ces modifications affectent la vue actuelle de l’application de l’appareil (par exemple, une modification des fonctionnalités de l’appareil), un fournisseur de services peut forcer la fermeture de l’appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="82fb5-126">If the user wants the configuration changes to be effective immediately (as opposed to after the next system restart), and these changes affect the application's current view of the device (such as a change in device capabilities), then a service provider can forcibly close the phone device.</span></span>

## <a name="requirements"></a><span data-ttu-id="82fb5-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82fb5-127">Requirements</span></span>



| <span data-ttu-id="82fb5-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82fb5-128">Requirement</span></span> | <span data-ttu-id="82fb5-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="82fb5-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="82fb5-130">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="82fb5-130">TAPI version</span></span><br/> | <span data-ttu-id="82fb5-131">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="82fb5-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="82fb5-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="82fb5-132">Header</span></span><br/>       | <dl> <span data-ttu-id="82fb5-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="82fb5-133"><dt>Tapi.h</dt></span></span> </dl> |



 

 




