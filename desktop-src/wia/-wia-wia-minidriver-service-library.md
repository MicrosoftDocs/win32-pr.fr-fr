---
description: pour simplifier autant que possible la mise en œuvre des pilotes, Windows acquisition d’images (WIA) fournit une bibliothèque de Service de minipilote qui effectue la plupart des tâches d’administration requises par l’architecture wia.
ms.assetid: 074a53a3-20b0-4b25-991d-5d48f75c5d75
title: Bibliothèque du service WIA minipilote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0008e19fbbdb31000535fa10f34bfacebfd6c6180964fa3e3fb18502f22a28d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207929"
---
# <a name="wia-minidriver-service-library"></a>Bibliothèque du service WIA minipilote

pour simplifier autant que possible la mise en œuvre des pilotes, Windows acquisition d’images (WIA) fournit une bibliothèque de Service de minipilote qui effectue la plupart des tâches d’administration requises par l’architecture wia. La bibliothèque de service fournit des fonctions d’assistance pour gérer l’arborescence des objets de l' [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) de l’appareil.

Les fonctions de base de la bibliothèque de services exécutent des fonctions d’assistance que la plupart des pilotes de périphérique doivent normalement implémenter. Ces fonctions lisent et écrivent des propriétés. Ils créent également des objets d’élément de pilote et copient les propriétés des informations de périphérique.

 

 



