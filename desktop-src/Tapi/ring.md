---
description: Un seul téléphone peut être en mesure d’sonner avec différents modes de sonnerie.
ms.assetid: c5ddcb3c-183c-4f97-9429-977d5cc32668
title: Anneau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671aac6ead1938ff5b35ecb4996e4bc072a66d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951959"
---
# <a name="ring"></a><span data-ttu-id="0198c-103">Anneau</span><span class="sxs-lookup"><span data-stu-id="0198c-103">Ring</span></span>

<span data-ttu-id="0198c-104">Un seul téléphone peut être en mesure d’sonner avec différents modes de sonnerie.</span><span class="sxs-lookup"><span data-stu-id="0198c-104">A single phone may be able to ring with different ring modes.</span></span> <span data-ttu-id="0198c-105">Étant donné la grande variété de modes de sonnerie disponibles, les modes Ring sont identifiés par le biais de leur numéro en mode Ring.</span><span class="sxs-lookup"><span data-stu-id="0198c-105">Given the wide variety of ring modes available, ring modes are identified by means of their ring mode number.</span></span> <span data-ttu-id="0198c-106">Un nombre en mode Ring est compris entre zéro et le nombre de modes Ring disponibles moins un.</span><span class="sxs-lookup"><span data-stu-id="0198c-106">A ring mode number ranges from zero to the number of available ring modes minus one.</span></span>

<span data-ttu-id="0198c-107">Les fonctions qu’une application utiliserait pour contrôler les modes ring d’un appareil téléphonique sont [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), qui sonne un appareil téléphonique ouvert en fonction d’un mode Ring donné et [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), qui retourne le mode Ring actuel d’un appareil téléphonique ouvert.</span><span class="sxs-lookup"><span data-stu-id="0198c-107">The functions an application would use to control a phone device's ring modes are [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), which rings an open phone device according to a given ring mode, and [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), which returns the current ring mode of an opened phone device.</span></span>

<span data-ttu-id="0198c-108">Lorsque le mode ring d’un appareil téléphonique est modifié, un message d' [**\_ État de téléphone**](phone-state.md) est envoyé à l’application pour notifier l’application du changement d’État.</span><span class="sxs-lookup"><span data-stu-id="0198c-108">When the ring mode of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application to notify the application about the state change.</span></span> <span data-ttu-id="0198c-109">Les paramètres de ce message fournissent une indication de la modification.</span><span class="sxs-lookup"><span data-stu-id="0198c-109">Parameters to this message provide an indication of the change.</span></span>

 

 



