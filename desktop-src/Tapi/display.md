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
# <a name="display"></a>Afficher

L’interface TAPI permet d’accéder à l’affichage d’un téléphone. L’affichage est modélisé sous la forme d’une zone alphanumérique avec des lignes et des colonnes. Les fonctionnalités de l’appareil d’un téléphone indiquent la taille de l’affichage d’un téléphone en nombre de lignes et le nombre de colonnes. Ces deux nombres sont nuls si l’appareil téléphonique n’a pas d’affichage. Utilisez [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) pour écrire des informations sur l’affichage d’un appareil téléphonique ouvert et [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) pour récupérer le contenu actuel de l’affichage d’un téléphone.

Lorsque l’affichage d’un appareil mobile est modifié, un message d' [**\_ État de téléphone**](phone-state.md) est envoyé à la fonction d’application pour notifier l’application du changement d’État. Les paramètres de ce message fournissent une indication de la modification.

 

 



