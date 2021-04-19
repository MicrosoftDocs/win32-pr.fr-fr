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
# <a name="wia-minidriver-service-library"></a><span data-ttu-id="b417c-103">Bibliothèque du service WIA minipilote</span><span class="sxs-lookup"><span data-stu-id="b417c-103">WIA Minidriver Service Library</span></span>

<span data-ttu-id="b417c-104">Pour simplifier autant que possible la mise en œuvre des pilotes, l’acquisition d’images Windows (WIA) fournit une bibliothèque de service de minipilote qui effectue la plupart des tâches d’administration requises par l’architecture WIA.</span><span class="sxs-lookup"><span data-stu-id="b417c-104">To simplify driver implementation as much as possible, Windows Image Acquisition (WIA) provides a Minidriver Service Library that performs many of the administrative tasks required by the WIA architecture.</span></span> <span data-ttu-id="b417c-105">La bibliothèque de service fournit des fonctions d’assistance pour gérer l’arborescence des objets de l' [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b417c-105">The service library provides helper functions to maintain the device's tree of [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) objects.</span></span>

<span data-ttu-id="b417c-106">Les fonctions de base de la bibliothèque de services exécutent des fonctions d’assistance que la plupart des pilotes de périphérique doivent normalement implémenter.</span><span class="sxs-lookup"><span data-stu-id="b417c-106">The basic service library functions perform helper functions that most device drivers would otherwise need to implement.</span></span> <span data-ttu-id="b417c-107">Ces fonctions lisent et écrivent des propriétés.</span><span class="sxs-lookup"><span data-stu-id="b417c-107">These functions read and write properties.</span></span> <span data-ttu-id="b417c-108">Ils créent également des objets d’élément de pilote et copient les propriétés des informations de périphérique.</span><span class="sxs-lookup"><span data-stu-id="b417c-108">They also create driver item objects and copy device information properties.</span></span>

 

 



