---
description: Certains ensembles de téléphones prennent en charge la notion de téléchargement de données à partir de ou de chargement des données sur le périphérique téléphonique, ce qui permet de programmer le jeu de téléphones à plusieurs égards.
ms.assetid: 5734107d-8104-4d8a-b3f7-3cc2a48f71ca
title: Zones de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81376549c63b4fcea92f705246cd58161faeac94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519889"
---
# <a name="data-areas"></a><span data-ttu-id="0c4ee-103">Zones de données</span><span class="sxs-lookup"><span data-stu-id="0c4ee-103">Data Areas</span></span>

<span data-ttu-id="0c4ee-104">Certains ensembles de téléphones prennent en charge la notion de téléchargement de données à partir de ou de chargement des données sur le périphérique téléphonique, ce qui permet de programmer le jeu de téléphones à plusieurs égards.</span><span class="sxs-lookup"><span data-stu-id="0c4ee-104">Some phone sets support the notion of downloading data from or uploading data to the phone device, which allows the phone set to be programmed in a variety of ways.</span></span> <span data-ttu-id="0c4ee-105">Modèles TAPI ces jeux de téléphones ont une ou plusieurs zones de téléchargement ou de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="0c4ee-105">TAPI models these phone sets as having one or more download or upload areas.</span></span> <span data-ttu-id="0c4ee-106">Chaque zone est identifiée par un nombre compris entre zéro et le nombre de zones de données disponibles sur le téléphone moins un.</span><span class="sxs-lookup"><span data-stu-id="0c4ee-106">Each area is identified by a number that ranges from zero to the number of data areas available on the phone minus one.</span></span> <span data-ttu-id="0c4ee-107">Les tailles de chaque zone peuvent varier.</span><span class="sxs-lookup"><span data-stu-id="0c4ee-107">Sizes of each area can vary.</span></span> <span data-ttu-id="0c4ee-108">Le format des données elles-mêmes est spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0c4ee-108">The format of the data itself is device-specific.</span></span>

<span data-ttu-id="0c4ee-109">La fonction TAPI [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) télécharge une mémoire tampon de données dans une zone de données donnée du périphérique téléphonique, et la fonction [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) charge le contenu d’une zone de données donnée dans le périphérique téléphonique dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="0c4ee-109">The TAPI [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) function downloads a buffer of data to a given data area in the phone device, and the [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) function uploads the contents of a given data area in the phone device to a buffer.</span></span>

<span data-ttu-id="0c4ee-110">Lorsqu’une zone de données d’un appareil mobile est modifiée, un message d' [**\_ État de téléphone**](phone-state.md) est envoyé à l’application pour notifier l’application du changement d’État.</span><span class="sxs-lookup"><span data-stu-id="0c4ee-110">When a data area of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application to notify the application about the state change.</span></span> <span data-ttu-id="0c4ee-111">Les paramètres de ce message fournissent une indication de la modification.</span><span class="sxs-lookup"><span data-stu-id="0c4ee-111">Parameters to this message provide an indication of the change.</span></span>

 

 



