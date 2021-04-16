---
description: Une application compatible avec l’encre communique avec le système de reconnaissance via les API de la plateforme Tablet PC.
ms.assetid: 0ea6881f-d2d7-4646-9c41-53d1c03ea55b
title: Architecture de l’API de reconnaissance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72838b77e11092cacd4adb998c669167940ecad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104567149"
---
# <a name="recognition-api-architecture"></a><span data-ttu-id="c9427-103">Architecture de l’API de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="c9427-103">Recognition API Architecture</span></span>

<span data-ttu-id="c9427-104">Une application compatible avec l’encre communique avec le système de reconnaissance via les API de la plateforme Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="c9427-104">An ink-enabled application communicates with the recognition system through the Tablet PC Platform APIs.</span></span> <span data-ttu-id="c9427-105">Les applications utilisent l’objet [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) pour y parvenir.</span><span class="sxs-lookup"><span data-stu-id="c9427-105">Applications use the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object to accomplish this.</span></span> <span data-ttu-id="c9427-106">La plateforme Tablet PC interagit avec votre module de reconnaissance à l’aide des interfaces de style C documentées dans cette section.</span><span class="sxs-lookup"><span data-stu-id="c9427-106">The Tablet PC Platform interacts with your recognizer by using the C-style interfaces that are documented in this section.</span></span> <span data-ttu-id="c9427-107">Dans l’illustration suivante, la zone à l’intérieur de la ligne en pointillés indique ce qui est documenté dans cette section.</span><span class="sxs-lookup"><span data-stu-id="c9427-107">In the following illustration, the area inside the dashed line shows what is documented in this section.</span></span>

![illustration de l’architecture de reconnaissance avec reconnaissance en surbrillance](images/96ee7367-7b8a-4794-99c1-bcac9daed645.gif)

<span data-ttu-id="c9427-109">Un module de reconnaissance personnalisé doit inclure Récapitulatifis. h (installé par défaut dans C : \\ Program Files \\ Microsoft Tablet PC Platform SDK \\ include).</span><span class="sxs-lookup"><span data-stu-id="c9427-109">A custom recognizer must include Recapis.h (installed by default in C:\\Program Files\\Microsoft Tablet PC Platform SDK\\Include).</span></span> <span data-ttu-id="c9427-110">Sauf indication contraire, votre bibliothèque de liens dynamiques (DLL) doit exporter toutes les fonctions d’API, même si vous choisissez d’en faire une, vous devez retourner E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="c9427-110">Except where noted, your dynamic-link library (DLL) must export all of the API functions, even if you choose to have some of them return E\_NOTIMPL.</span></span>

<span data-ttu-id="c9427-111">En aucun cas, votre module de reconnaissance sera appelé directement par une application compatible avec l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="c9427-111">Under no circumstances will your recognizer be called directly by an ink-enabled application.</span></span> <span data-ttu-id="c9427-112">Au lieu de cela, les applications appellent les API d’automatisation ou les API gérées pour obtenir les résultats de votre module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="c9427-112">Instead, applications will call either the Automation APIs or the Managed APIs to get results from your recognizer.</span></span>

 

 



