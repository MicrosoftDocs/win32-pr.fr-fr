---
description: Les \_ constantes d’indicateur de bit LINEDEVSTATUSFLAGS décrivent une collection d’éléments de l’état du périphérique de ligne booléenne.
ms.assetid: 5fa754d3-07b2-4b75-91ef-1bf961d9fef4
title: Constantes LINEDEVSTATUSFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70745b1a84119af2305cadabd0a39ab5954e5b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537376"
---
# <a name="linedevstatusflags_-constants"></a><span data-ttu-id="c8743-103">\_Constantes LINEDEVSTATUSFLAGS</span><span class="sxs-lookup"><span data-stu-id="c8743-103">LINEDEVSTATUSFLAGS\_ Constants</span></span>

<span data-ttu-id="c8743-104">Les constantes d’indicateur de bit **LINEDEVSTATUSFLAGS \_** décrivent une collection d’éléments de l’état du périphérique de ligne booléenne.</span><span class="sxs-lookup"><span data-stu-id="c8743-104">The **LINEDEVSTATUSFLAGS\_** bit-flag constants describe a collection of Boolean line device status items.</span></span>

<dl> <dt>

<span data-ttu-id="c8743-105"><span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**LINEDEVSTATUSFLAGS \_ connecté**</span><span class="sxs-lookup"><span data-stu-id="c8743-105"><span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**LINEDEVSTATUSFLAGS\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c8743-106">Spécifie si la ligne est connectée à l’interface TAPI.</span><span class="sxs-lookup"><span data-stu-id="c8743-106">Specifies whether the line is connected to TAPI.</span></span> <span data-ttu-id="c8743-107">Si la **valeur est true**, la ligne est connectée et l’interface TAPI peut fonctionner sur le périphérique de ligne.</span><span class="sxs-lookup"><span data-stu-id="c8743-107">If **TRUE**, the line is connected and TAPI is able to operate on the line device.</span></span> <span data-ttu-id="c8743-108">Si la **valeur est false**, la ligne est déconnectée et l’application ne peut pas contrôler l’appareil de ligne via TAPI.</span><span class="sxs-lookup"><span data-stu-id="c8743-108">If **FALSE**, the line is disconnected and the application is unable to control the line device through TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c8743-109"><span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**InService LINEDEVSTATUSFLAGS \_**</span><span class="sxs-lookup"><span data-stu-id="c8743-109"><span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**LINEDEVSTATUSFLAGS\_INSERVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c8743-110">Indique si la ligne est en service.</span><span class="sxs-lookup"><span data-stu-id="c8743-110">Indicates whether the line is in service.</span></span> <span data-ttu-id="c8743-111">Si la **valeur est true**, la ligne est en service ; Si la **valeur est false**, la ligne est hors service.</span><span class="sxs-lookup"><span data-stu-id="c8743-111">If **TRUE**, the line is in service; if **FALSE**, the line is out of service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c8743-112"><span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**LINEDEVSTATUSFLAGS \_ verrouillé**</span><span class="sxs-lookup"><span data-stu-id="c8743-112"><span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**LINEDEVSTATUSFLAGS\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c8743-113">Indique si la ligne est verrouillée ou déverrouillée.</span><span class="sxs-lookup"><span data-stu-id="c8743-113">Indicates whether the line is locked or unlocked.</span></span> <span data-ttu-id="c8743-114">Ce bit est le plus souvent utilisé avec des appareils de ligne associés à des téléphones cellulaires.</span><span class="sxs-lookup"><span data-stu-id="c8743-114">This bit is most often used with line devices associated with cellular phones.</span></span> <span data-ttu-id="c8743-115">De nombreux téléphones cellulaires disposent d’un mécanisme de sécurité qui nécessite l’entrée d’un mot de passe pour permettre au téléphone de passer des appels.</span><span class="sxs-lookup"><span data-stu-id="c8743-115">Many cellular phones have a security mechanism that requires the entry of a password to enable the phone to place calls.</span></span> <span data-ttu-id="c8743-116">Ce bit peut être utilisé pour indiquer aux applications que le téléphone est verrouillé et ne peut pas effectuer d’appels jusqu’à ce que le mot de passe soit entré sur l’interface utilisateur du téléphone afin que l’application puisse présenter une alerte appropriée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c8743-116">This bit can be used to indicate to applications that the phone is locked and cannot place calls until the password is entered on the user interface of the phone so that the application can present an appropriate alert to the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c8743-117"><span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**LINEDEVSTATUSFLAGS \_ MSGWAIT**</span><span class="sxs-lookup"><span data-stu-id="c8743-117"><span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**LINEDEVSTATUSFLAGS\_MSGWAIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c8743-118">Indique si la ligne a un message en attente.</span><span class="sxs-lookup"><span data-stu-id="c8743-118">Indicates whether the line has a message waiting.</span></span> <span data-ttu-id="c8743-119">Si la **valeur est true**, un message est en attente ; Si la **valeur est false**, aucun message n’est en attente.</span><span class="sxs-lookup"><span data-stu-id="c8743-119">If **TRUE**, a message is waiting; if **FALSE**, no message is waiting.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8743-120">Notes</span><span class="sxs-lookup"><span data-stu-id="c8743-120">Remarks</span></span>

<span data-ttu-id="c8743-121">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="c8743-121">No extensibility.</span></span> <span data-ttu-id="c8743-122">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="c8743-122">All 32 bits are reserved.</span></span>

<span data-ttu-id="c8743-123">\_Les constantes LINEDEVSTATUSFLAGS sont utilisées dans le membre **dwDevStatusFlags** de la structure de données [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) .</span><span class="sxs-lookup"><span data-stu-id="c8743-123">LINEDEVSTATUSFLAGS\_ constants are used within the **dwDevStatusFlags** member of the [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) data structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8743-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8743-124">Requirements</span></span>



| <span data-ttu-id="c8743-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8743-125">Requirement</span></span> | <span data-ttu-id="c8743-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8743-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c8743-127">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="c8743-127">TAPI version</span></span><br/> | <span data-ttu-id="c8743-128">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c8743-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c8743-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8743-129">Header</span></span><br/>       | <dl> <span data-ttu-id="c8743-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8743-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




