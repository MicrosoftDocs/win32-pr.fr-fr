---
description: Certains ensembles de téléphones prennent en charge la notion de téléchargement de données à partir de ou de chargement des données sur le périphérique téléphonique, ce qui permet de programmer le jeu de téléphones à plusieurs égards.
ms.assetid: 5734107d-8104-4d8a-b3f7-3cc2a48f71ca
title: Zones de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed05d6233a8c8ed31a2d00d28970a517ef181f00689c7da34673d3044fffb4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117946142"
---
# <a name="data-areas"></a>Zones de données

Certains ensembles de téléphones prennent en charge la notion de téléchargement de données à partir de ou de chargement des données sur le périphérique téléphonique, ce qui permet de programmer le jeu de téléphones à plusieurs égards. Modèles TAPI ces jeux de téléphones ont une ou plusieurs zones de téléchargement ou de téléchargement. Chaque zone est identifiée par un nombre compris entre zéro et le nombre de zones de données disponibles sur le téléphone moins un. Les tailles de chaque zone peuvent varier. Le format des données elles-mêmes est spécifique à l’appareil.

La fonction TAPI [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) télécharge une mémoire tampon de données dans une zone de données donnée du périphérique téléphonique, et la fonction [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) charge le contenu d’une zone de données donnée dans le périphérique téléphonique dans une mémoire tampon.

Lorsqu’une zone de données d’un appareil mobile est modifiée, un message d' [**\_ État de téléphone**](phone-state.md) est envoyé à l’application pour notifier l’application du changement d’État. Les paramètres de ce message fournissent une indication de la modification.

 

 



