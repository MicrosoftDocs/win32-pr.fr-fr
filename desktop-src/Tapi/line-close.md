---
description: Le message de fermeture de la ligne TAPI \_ est envoyé lorsque l’appareil de ligne spécifié a été fermé de force. Le handle de périphérique de ligne ou les handles d’appel des appels sur la ligne ne sont plus valides une fois que ce message a été envoyé.
ms.assetid: f254e331-d574-4fa7-8447-6e4535d3d773
title: Message LINE_CLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7f4fde53d1017b2dcd9fe4ea833803055d9f2dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532606"
---
# <a name="line_close-message"></a><span data-ttu-id="49580-104">Message de fermeture de ligne \_</span><span class="sxs-lookup"><span data-stu-id="49580-104">LINE\_CLOSE message</span></span>

<span data-ttu-id="49580-105">Le message **de \_ fermeture** de la ligne TAPI est envoyé lorsque l’appareil de ligne spécifié a été fermé de force.</span><span class="sxs-lookup"><span data-stu-id="49580-105">The TAPI **LINE\_CLOSE** message is sent when the specified line device has been forcibly closed.</span></span> <span data-ttu-id="49580-106">Le handle de périphérique de ligne ou les handles d’appel des appels sur la ligne ne sont plus valides une fois que ce message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="49580-106">The line device handle or any call handles for calls on the line are no longer valid once this message has been sent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="49580-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49580-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49580-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="49580-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="49580-109">Handle vers le périphérique de ligne qui a été fermé.</span><span class="sxs-lookup"><span data-stu-id="49580-109">A handle to the line device that was closed.</span></span> <span data-ttu-id="49580-110">Ce descripteur n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="49580-110">This handle is no longer valid.</span></span>

</dd> <dt>

<span data-ttu-id="49580-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="49580-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="49580-112">Instance de rappel fournie lors de l’ouverture de la ligne.</span><span class="sxs-lookup"><span data-stu-id="49580-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="49580-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="49580-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="49580-114">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="49580-114">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="49580-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="49580-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="49580-116">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="49580-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="49580-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="49580-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="49580-118">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="49580-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49580-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49580-119">Return value</span></span>

<span data-ttu-id="49580-120">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="49580-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="49580-121">Notes</span><span class="sxs-lookup"><span data-stu-id="49580-121">Remarks</span></span>

<span data-ttu-id="49580-122">Le message de **\_ fermeture de ligne** est envoyé à toute application uniquement après que le fournisseur de services TAPI (TSP) a fermé de force une ligne ouverte.</span><span class="sxs-lookup"><span data-stu-id="49580-122">The **LINE\_CLOSE** message is sent to any application only after the TAPI service provider (TSP) has forcibly closed an open line.</span></span> <span data-ttu-id="49580-123">Si la ligne peut ou non être rouverte immédiatement après une fermeture forcée, elle est spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="49580-123">Whether or not the line can be reopened immediately after a forced close is device-specific.</span></span>

<span data-ttu-id="49580-124">La condition à l’origine du problème peut être un changement important de l’État, une erreur matérielle, une perte de connexion à un serveur, ou même potentiellement empêcher une application de monopoliser un appareil de ligne trop longtemps.</span><span class="sxs-lookup"><span data-stu-id="49580-124">The causing condition can be a significant change of state, a hardware error, a loss of connection to a server, or even potentially to prevent a single application from monopolizing a line device for too long.</span></span> <span data-ttu-id="49580-125">Un périphérique de ligne peut également être fermé de force une fois que l’utilisateur a modifié la configuration de cette ligne ou de son pilote.</span><span class="sxs-lookup"><span data-stu-id="49580-125">A line device can also be forcibly closed after the user has modified the configuration of that line or its driver.</span></span> <span data-ttu-id="49580-126">Si l’utilisateur souhaite que les modifications de configuration soient effectives immédiatement (par opposition à après le redémarrage du système suivant), et qu’elles affectent la vue actuelle de l’application de l’appareil (par exemple, une modification des fonctionnalités de l’appareil), un fournisseur de services peut fermer l’appareil de ligne de force.</span><span class="sxs-lookup"><span data-stu-id="49580-126">If the user wants the configuration changes to be effective immediately (as opposed to after the next system restart), and they affect the application's current view of the device (such as a change in device capabilities), then a service provider can forcibly close the line device.</span></span>

## <a name="requirements"></a><span data-ttu-id="49580-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49580-127">Requirements</span></span>



| <span data-ttu-id="49580-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49580-128">Requirement</span></span> | <span data-ttu-id="49580-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="49580-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="49580-130">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="49580-130">TAPI version</span></span><br/> | <span data-ttu-id="49580-131">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="49580-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="49580-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="49580-132">Header</span></span><br/>       | <dl> <span data-ttu-id="49580-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="49580-133"><dt>Tapi.h</dt></span></span> </dl> |



 

 




