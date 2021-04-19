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
# <a name="buttons-telephony-api"></a>Boutons (API de téléphonie)

La téléphonie Microsoft modélise les boutons et les lampes d’un téléphone en tant que paires bouton-lampe. Un bouton sans lampe en regard, ou un feu sans bouton est spécifié à l’aide d’un indicateur factice pour le bouton ou la lampe manquant (e). Un bouton avec plusieurs lampes est modélisé à l’aide de plusieurs paires bouton-lampe.

Les informations associées à un bouton de téléphone peuvent être définies et récupérées. Quand vous appuyez sur un bouton, le fournisseur de services envoie un message de [**\_ bouton téléphone**](/previous-versions/windows/desktop/legacy/ms725254(v=vs.85)) à la fonction de rappel TAPI. Les paramètres de ce message sont un descripteur du périphérique téléphonique et l’identificateur de bouton/lampe du bouton sur lequel l’utilisateur a cliqué. Le bouton de pavé numérique « 0 » à « 9 », « \* » et « \# » se voient assigner des identificateurs de bouton/lampe fixes de 0 à 11.

La fonction [**TSPI \_ phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo) définit les informations associées à un bouton sur un appareil téléphonique. [**TSPI \_ phoneGetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetbuttoninfo) retourne les informations associées à un bouton sur un appareil téléphonique. Le fournisseur de services envoie un \_ message de bouton téléphone à la fonction de rappel TAPI lorsqu’un bouton sur le téléphone est enfoncé.

Les informations associées à un bouton n’ont aucune signification sémantique en ce qui concerne TSPI. Il est utile pour les applications spécifiques à l’appareil qui interprètent ces informations pour un appareil téléphonique donné, ou pour l’affichage à l’utilisateur, comme dans le système d’aide d’une application.

 

 
