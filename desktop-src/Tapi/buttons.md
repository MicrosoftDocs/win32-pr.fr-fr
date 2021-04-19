---
description: La téléphonie Microsoft modélise les boutons et les lampes des téléphones en tant que paires bouton-lampe.
ms.assetid: 6ac912bb-8d2b-4aa3-a6e8-af86fbaabd58
title: Boutons (API de téléphonie)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd1fc18e02331f98f4dbb98cfea7d9df2ca7f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544777"
---
# <a name="buttons-telephony-api"></a><span data-ttu-id="d44b8-103">Boutons (API de téléphonie)</span><span class="sxs-lookup"><span data-stu-id="d44b8-103">Buttons (Telephony API)</span></span>

<span data-ttu-id="d44b8-104">La téléphonie Microsoft modélise les boutons et les lampes d’un téléphone en tant que paires bouton-lampe.</span><span class="sxs-lookup"><span data-stu-id="d44b8-104">Microsoft Telephony models a phone's buttons and lamps as button-lamp pairs.</span></span> <span data-ttu-id="d44b8-105">Un bouton sans lampe en regard, ou un feu sans bouton est spécifié à l’aide d’un indicateur factice pour le bouton ou la lampe manquant (e).</span><span class="sxs-lookup"><span data-stu-id="d44b8-105">A button with no lamp next to it, or a lamp with no button is specified using a dummy indicator for the missing lamp or button.</span></span> <span data-ttu-id="d44b8-106">Un bouton avec plusieurs lampes est modélisé à l’aide de plusieurs paires bouton-lampe.</span><span class="sxs-lookup"><span data-stu-id="d44b8-106">A button with multiple lamps is modeled by using multiple button-lamp pairs.</span></span>

<span data-ttu-id="d44b8-107">Les informations associées à un bouton de téléphone peuvent être définies et récupérées.</span><span class="sxs-lookup"><span data-stu-id="d44b8-107">Information associated with a phone button can be set and retrieved.</span></span> <span data-ttu-id="d44b8-108">Quand vous appuyez sur un bouton, le fournisseur de services envoie un message de [**\_ bouton téléphone**](/previous-versions/windows/desktop/legacy/ms725254(v=vs.85)) à la fonction de rappel TAPI.</span><span class="sxs-lookup"><span data-stu-id="d44b8-108">When a button is pressed, the service provider sends a [**PHONE\_BUTTON**](/previous-versions/windows/desktop/legacy/ms725254(v=vs.85)) message to the TAPI callback function.</span></span> <span data-ttu-id="d44b8-109">Les paramètres de ce message sont un descripteur du périphérique téléphonique et l’identificateur de bouton/lampe du bouton sur lequel l’utilisateur a cliqué.</span><span class="sxs-lookup"><span data-stu-id="d44b8-109">Parameters of this message are a handle to the phone device and the button/lamp identifier of the button that was pressed.</span></span> <span data-ttu-id="d44b8-110">Le bouton de pavé numérique « 0 » à « 9 », « \* » et « \# » se voient assigner des identificateurs de bouton/lampe fixes de 0 à 11.</span><span class="sxs-lookup"><span data-stu-id="d44b8-110">The keypad button '0' through '9', '\*', and '\#' are assigned fixed button/lamp identifiers 0 through 11.</span></span>

<span data-ttu-id="d44b8-111">La fonction [**TSPI \_ phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo) définit les informations associées à un bouton sur un appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="d44b8-111">The function [**TSPI\_phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo) sets the information associated with a button on a phone device.</span></span> <span data-ttu-id="d44b8-112">[**TSPI \_ phoneGetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetbuttoninfo) retourne les informations associées à un bouton sur un appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="d44b8-112">[**TSPI\_phoneGetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetbuttoninfo) returns information associated with a button on a phone device.</span></span> <span data-ttu-id="d44b8-113">Le fournisseur de services envoie un \_ message de bouton téléphone à la fonction de rappel TAPI lorsqu’un bouton sur le téléphone est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="d44b8-113">The service provider sends a PHONE\_BUTTON message to the TAPI callback function when a button on the phone is pressed.</span></span>

<span data-ttu-id="d44b8-114">Les informations associées à un bouton n’ont aucune signification sémantique en ce qui concerne TSPI.</span><span class="sxs-lookup"><span data-stu-id="d44b8-114">The information associated with a button does not carry any semantic meaning as far as TSPI is concerned.</span></span> <span data-ttu-id="d44b8-115">Il est utile pour les applications spécifiques à l’appareil qui interprètent ces informations pour un appareil téléphonique donné, ou pour l’affichage à l’utilisateur, comme dans le système d’aide d’une application.</span><span class="sxs-lookup"><span data-stu-id="d44b8-115">It is useful for device-specific applications that interpret this information for a given phone device, or for display to the user, such as in an application's help system.</span></span>

 

 
