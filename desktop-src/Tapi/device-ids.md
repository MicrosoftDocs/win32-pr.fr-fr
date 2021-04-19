---
description: D’autres fonctions de téléphone TAPI utilisent un handle vers un appareil téléphonique ouvert pour identifier l’appareil téléphonique ouvert.
ms.assetid: 3e8e18fc-d577-4406-8225-048813c4cb9e
title: ID des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8eb9d43b22ab6cd39a90ab8ed0776c4e043ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514830"
---
# <a name="device-ids"></a><span data-ttu-id="b62b9-103">ID des appareils</span><span class="sxs-lookup"><span data-stu-id="b62b9-103">Device IDs</span></span>

<span data-ttu-id="b62b9-104">D’autres fonctions de téléphone TAPI utilisent un handle vers un appareil téléphonique ouvert pour identifier l’appareil téléphonique ouvert.</span><span class="sxs-lookup"><span data-stu-id="b62b9-104">Other TAPI phone functions use a handle to an open phone device to identify the open phone device.</span></span> <span data-ttu-id="b62b9-105">Les seules fonctions des appareils téléphoniques qui prennent un paramètre d’identificateur de périphérique téléphonique (par opposition à un handle de téléphone) sont les fonctions [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) et [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) .</span><span class="sxs-lookup"><span data-stu-id="b62b9-105">The only functions for phone devices that take a phone device identifier parameter (as opposed to a phone handle) are the [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) and [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) functions.</span></span> <span data-ttu-id="b62b9-106">Une application peut récupérer l’identificateur d’appareil du téléphone à l’aide de la fonction [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) avec le descripteur de téléphone comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="b62b9-106">An application can retrieve the phone's device identifier by using the [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function with the phone handle as a parameter.</span></span>

<span data-ttu-id="b62b9-107">Une application peut également obtenir des identificateurs d’appareil pour différentes classes d’appareils associées à un téléphone ouvert en appelant [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span><span class="sxs-lookup"><span data-stu-id="b62b9-107">An application can also obtain device identifiers for various device classes associated with an opened phone by invoking [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span></span> <span data-ttu-id="b62b9-108">Consultez [classes d’appareils TAPI](tapi-device-classes.md) pour les noms de classes d’appareils.</span><span class="sxs-lookup"><span data-stu-id="b62b9-108">See [TAPI Device Classes](tapi-device-classes.md) for device class names.</span></span>

<span data-ttu-id="b62b9-109">Cette fonction prend un handle de téléphone et une description de classe d’appareil.</span><span class="sxs-lookup"><span data-stu-id="b62b9-109">This function takes a phone handle and a device class description.</span></span> <span data-ttu-id="b62b9-110">Elle retourne l’identificateur de l’appareil de la classe d’appareil donnée associée à l’appareil téléphonique ouvert.</span><span class="sxs-lookup"><span data-stu-id="b62b9-110">It returns the device identifier for the device of the given device class that is associated with the open phone device.</span></span> <span data-ttu-id="b62b9-111">Si la classe d’appareil est « TAPI/Phone », l’identificateur d’appareil de l’appareil téléphonique est retourné.</span><span class="sxs-lookup"><span data-stu-id="b62b9-111">If the device class is "tapi/phone", the device identifier of the phone device is returned.</span></span>

<span data-ttu-id="b62b9-112">Contrairement aux appareils en ligne, pour lesquels les services de base de ligne fournissent l’équivalent des POTS, aucun jeu de fonctions minimal garanti n’est défini pour les appareils téléphoniques.</span><span class="sxs-lookup"><span data-stu-id="b62b9-112">In contrast with line devices, for which the basic line services provide the equivalent of POTS, no minimum guaranteed set of functions is defined for phone devices.</span></span> <span data-ttu-id="b62b9-113">Bien que chaque appareil téléphonique fournisse au moins les fonctions et les messages décrits dans cette section, il n’offre pas d’opérations réelles sur l’appareil mobile physique.</span><span class="sxs-lookup"><span data-stu-id="b62b9-113">While each phone device provides at least the functions and messages described in this section, they do not offer any actual operations on the physical phone device.</span></span>

 

 



