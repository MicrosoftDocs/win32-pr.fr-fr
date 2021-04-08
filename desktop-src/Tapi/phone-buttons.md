---
description: L’interface TAPI modélise les boutons et les lampes des téléphones en tant que paires bouton-lampe.
ms.assetid: e4c50bd6-a256-407f-af3b-b24383a30ea0
title: Boutons de téléphone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3e65c34096c0cf043b85d80c9c726c6bef982d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755109"
---
# <a name="phone-buttons"></a><span data-ttu-id="d16e1-103">Boutons de téléphone</span><span class="sxs-lookup"><span data-stu-id="d16e1-103">Phone Buttons</span></span>

<span data-ttu-id="d16e1-104">TAPI modélise les boutons et les lampes d’un téléphone en tant que paires bouton-lampe.</span><span class="sxs-lookup"><span data-stu-id="d16e1-104">TAPI models a phone's buttons and lamps as button-lamp pairs.</span></span> <span data-ttu-id="d16e1-105">Un bouton sans bouton est spécifié à l’aide d’un indicateur « factice » pour la lampe ou le bouton manquant.</span><span class="sxs-lookup"><span data-stu-id="d16e1-105">A button with no lamp next to it or a lamp with no button is specified using a "dummy" indicator for the missing lamp or button.</span></span> <span data-ttu-id="d16e1-106">Un bouton avec plusieurs lampes est modélisé à l’aide de plusieurs paires bouton-lampe.</span><span class="sxs-lookup"><span data-stu-id="d16e1-106">A button with multiple lamps is modeled by using multiple button-lamp pairs.</span></span>

<span data-ttu-id="d16e1-107">Les informations associées à un bouton de téléphone peuvent être définies et récupérées.</span><span class="sxs-lookup"><span data-stu-id="d16e1-107">Information associated with a phone button can be set and retrieved.</span></span> <span data-ttu-id="d16e1-108">Quand vous appuyez sur un bouton, un message de [**\_ bouton téléphone**](phone-button.md) est envoyé à la fonction d’application.</span><span class="sxs-lookup"><span data-stu-id="d16e1-108">When a button is pressed, a [**PHONE\_BUTTON**](phone-button.md) message is sent to the application function.</span></span> <span data-ttu-id="d16e1-109">Les paramètres de ce message sont un descripteur de l’appareil téléphonique et l’identificateur de lampe de bouton du bouton sur lequel l’utilisateur a cliqué.</span><span class="sxs-lookup"><span data-stu-id="d16e1-109">The parameters of this message are a handle to the phone device and the button-lamp identifier of the button that was pressed.</span></span> <span data-ttu-id="d16e1-110">Les boutons de clavier « 0 » à « 9 », « \* » et « \# » sont affectés aux identificateurs de lampe de bouton fixes de 0 à 11.</span><span class="sxs-lookup"><span data-stu-id="d16e1-110">The keypad buttons '0' through '9', '\*', and '\#' are assigned the fixed button-lamp identifiers 0 through 11.</span></span>

<span data-ttu-id="d16e1-111">Les fonctions associées aux boutons sont [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo), qui définit les informations associées à un bouton sur un appareil téléphonique, et [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), qui retourne les informations associées à un bouton sur un appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="d16e1-111">The functions associated with buttons are [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo), which sets the information associated with a button on a phone device, and [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), which returns information associated with a button on a phone device.</span></span> <span data-ttu-id="d16e1-112">Le \_ message du bouton téléphone est envoyé à une application quand vous appuyez sur un bouton du téléphone.</span><span class="sxs-lookup"><span data-stu-id="d16e1-112">The PHONE\_BUTTON message is sent to an application when a button on the phone is pressed.</span></span>

<span data-ttu-id="d16e1-113">Les informations associées à un bouton n’ont aucune signification sémantique en ce qui concerne TAPI.</span><span class="sxs-lookup"><span data-stu-id="d16e1-113">The information associated with a button does not carry any semantic meaning as far as TAPI is concerned.</span></span> <span data-ttu-id="d16e1-114">Il est utile pour les applications spécifiques à l’appareil qui comprennent la signification de ces informations pour un périphérique téléphonique donné, ou pour l’affichage à l’utilisateur, comme l’aide en ligne.</span><span class="sxs-lookup"><span data-stu-id="d16e1-114">It is useful for device-specific applications that understand the meaning of this information for a given phone device, or for display to the user, such as online help.</span></span>

 

 



