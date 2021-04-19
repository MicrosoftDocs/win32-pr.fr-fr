---
description: Pour simplifier autant que possible la mise en œuvre des pilotes, l’acquisition d’images Windows (WIA) fournit une bibliothèque de service de minipilote qui effectue la plupart des tâches d’administration requises par l’architecture WIA.
ms.assetid: 074a53a3-20b0-4b25-991d-5d48f75c5d75
title: Bibliothèque du service WIA minipilote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45856fb795810e4e447a226f1b92a28698f08cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516474"
---
# <a name="wia-minidriver-service-library"></a>Bibliothèque du service WIA minipilote

Pour simplifier autant que possible la mise en œuvre des pilotes, l’acquisition d’images Windows (WIA) fournit une bibliothèque de service de minipilote qui effectue la plupart des tâches d’administration requises par l’architecture WIA. La bibliothèque de service fournit des fonctions d’assistance pour gérer l’arborescence des objets de l' [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) de l’appareil.

Les fonctions de base de la bibliothèque de services exécutent des fonctions d’assistance que la plupart des pilotes de périphérique doivent normalement implémenter. Ces fonctions lisent et écrivent des propriétés. Ils créent également des objets d’élément de pilote et copient les propriétés des informations de périphérique.

 

 



