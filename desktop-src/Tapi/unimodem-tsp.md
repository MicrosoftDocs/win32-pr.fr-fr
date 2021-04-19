---
description: Le pilote de modem Unimodem ou universel, TSP (unimdm. tsp) permet d’accéder à presque tous les modems standard.
ms.assetid: 1ea60477-f6c9-44ae-969c-515dfb0c607e
title: TSP Unimodem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115cc4fd159b2e62062171131f583bad19dc9b00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530199"
---
# <a name="unimodem-tsp"></a><span data-ttu-id="17638-103">TSP Unimodem</span><span class="sxs-lookup"><span data-stu-id="17638-103">Unimodem TSP</span></span>

<span data-ttu-id="17638-104">Le pilote de modem Unimodem ou universel, TSP (unimdm. tsp) permet d’accéder à presque tous les modems standard.</span><span class="sxs-lookup"><span data-stu-id="17638-104">The Unimodem, or Universal Modem Driver, TSP (Unimdm.tsp) provides access to nearly all standard modems.</span></span> <span data-ttu-id="17638-105">Il prend en charge les modems vocaux qui autorisent la diffusion en continu semi-duplex.</span><span class="sxs-lookup"><span data-stu-id="17638-105">It supports voice modems that allow half-duplex streaming.</span></span> <span data-ttu-id="17638-106">Ils sont pris en charge par le MSP Wave et le contrôle de flux est possible.</span><span class="sxs-lookup"><span data-stu-id="17638-106">They are supported by the Wave MSP and stream control is possible.</span></span> <span data-ttu-id="17638-107">(Notez que Unimodem sur Windows NT 4,0 ou version antérieure ne prend pas en charge les modems vocaux, si bien que le contrôle direct stream n’est pas possible.)</span><span class="sxs-lookup"><span data-stu-id="17638-107">(Note that Unimodem on Windows NT 4.0 or earlier does not support voice modems, so direct stream control is not possible.)</span></span>

<span data-ttu-id="17638-108">Ce TSP prend en charge une valeur de [**type d’adresse**](./lineaddresstype--constants.md) LINEADDRESSTYPE \_ PHONENUMBER.</span><span class="sxs-lookup"><span data-stu-id="17638-108">This TSP supports an [**address type**](./lineaddresstype--constants.md) value of LINEADDRESSTYPE\_PHONENUMBER.</span></span> <span data-ttu-id="17638-109">Si le programmeur souhaite utiliser les règles de numérotation, l’interface TAPI 3 [**ITAddressTranslation**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) ou la fonction [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) TAPI 2 doit être utilisée pour obtenir une chaîne de numérotation à partir d’un numéro de téléphone au format canonique.</span><span class="sxs-lookup"><span data-stu-id="17638-109">If the programmer wants to use the dialing rules, the TAPI 3 [**ITAddressTranslation**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) interface or the TAPI 2 [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) function must be used to obtain a dialable string from a phone number in canonical format.</span></span>

<span data-ttu-id="17638-110">Le TSP Unimodem est installé avec les systèmes d’exploitation Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Millennium Edition, Windows 98 et Windows 95.</span><span class="sxs-lookup"><span data-stu-id="17638-110">The Unimodem TSP is installed with Windows Server 2003 operating systems, Windows XP, Windows 2000, Windows NT, Windows Millennium Edition, Windows 98, and Windows 95.</span></span>

 

 
