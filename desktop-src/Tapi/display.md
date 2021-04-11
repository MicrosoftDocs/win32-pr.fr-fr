---
description: L’interface TAPI permet d’accéder à un affichage de téléphones.
ms.assetid: f6017ecc-b2a0-4a92-8c28-ce7411f8dd84
title: Afficher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dd813297c1d4624bb37cea8d833f63bcebeeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113191"
---
# <a name="display"></a><span data-ttu-id="b9aa3-103">Afficher</span><span class="sxs-lookup"><span data-stu-id="b9aa3-103">Display</span></span>

<span data-ttu-id="b9aa3-104">L’interface TAPI permet d’accéder à l’affichage d’un téléphone.</span><span class="sxs-lookup"><span data-stu-id="b9aa3-104">TAPI provides access to a phone's display.</span></span> <span data-ttu-id="b9aa3-105">L’affichage est modélisé sous la forme d’une zone alphanumérique avec des lignes et des colonnes.</span><span class="sxs-lookup"><span data-stu-id="b9aa3-105">The display is modeled as an alphanumeric area with rows and columns.</span></span> <span data-ttu-id="b9aa3-106">Les fonctionnalités de l’appareil d’un téléphone indiquent la taille de l’affichage d’un téléphone en nombre de lignes et le nombre de colonnes.</span><span class="sxs-lookup"><span data-stu-id="b9aa3-106">A phone's device capabilities indicate the size of a phone's display as the number of rows and the number of columns.</span></span> <span data-ttu-id="b9aa3-107">Ces deux nombres sont nuls si l’appareil téléphonique n’a pas d’affichage.</span><span class="sxs-lookup"><span data-stu-id="b9aa3-107">Both these numbers are zero if the phone device does not have a display.</span></span> <span data-ttu-id="b9aa3-108">Utilisez [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) pour écrire des informations sur l’affichage d’un appareil téléphonique ouvert et [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) pour récupérer le contenu actuel de l’affichage d’un téléphone.</span><span class="sxs-lookup"><span data-stu-id="b9aa3-108">Use [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) to write information to the display of an open phone device, and [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) to retrieve the current contents of a phone's display.</span></span>

<span data-ttu-id="b9aa3-109">Lorsque l’affichage d’un appareil mobile est modifié, un message d' [**\_ État de téléphone**](phone-state.md) est envoyé à la fonction d’application pour notifier l’application du changement d’État.</span><span class="sxs-lookup"><span data-stu-id="b9aa3-109">When the display of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application function to notify the application about the state change.</span></span> <span data-ttu-id="b9aa3-110">Les paramètres de ce message fournissent une indication de la modification.</span><span class="sxs-lookup"><span data-stu-id="b9aa3-110">Parameters to this message provide an indication of the change.</span></span>

 

 



