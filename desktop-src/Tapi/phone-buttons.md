---
description: L’interface TAPI modélise les boutons et les lampes des téléphones en tant que paires bouton-lampe.
ms.assetid: e4c50bd6-a256-407f-af3b-b24383a30ea0
title: Téléphone Boutons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e72288133615b19e622434b8727608aaec9a9136dd58eaa03e339708c42a13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774159"
---
# <a name="phone-buttons"></a>Téléphone Boutons

TAPI modélise les boutons et les lampes d’un téléphone en tant que paires bouton-lampe. Un bouton sans bouton est spécifié à l’aide d’un indicateur « factice » pour la lampe ou le bouton manquant. Un bouton avec plusieurs lampes est modélisé à l’aide de plusieurs paires bouton-lampe.

Les informations associées à un bouton de téléphone peuvent être définies et récupérées. Quand vous appuyez sur un bouton, un message de [**\_ bouton téléphone**](phone-button.md) est envoyé à la fonction d’application. Les paramètres de ce message sont un descripteur de l’appareil téléphonique et l’identificateur de lampe de bouton du bouton sur lequel l’utilisateur a cliqué. Les boutons de clavier « 0 » à « 9 », « \* » et « \# » sont affectés aux identificateurs de lampe de bouton fixes de 0 à 11.

Les fonctions associées aux boutons sont [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo), qui définit les informations associées à un bouton sur un appareil téléphonique, et [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), qui retourne les informations associées à un bouton sur un appareil téléphonique. Le \_ message du bouton téléphone est envoyé à une application quand vous appuyez sur un bouton du téléphone.

Les informations associées à un bouton n’ont aucune signification sémantique en ce qui concerne TAPI. Il est utile pour les applications spécifiques à l’appareil qui comprennent la signification de ces informations pour un périphérique téléphonique donné, ou pour l’affichage à l’utilisateur, comme l’aide en ligne.

 

 



