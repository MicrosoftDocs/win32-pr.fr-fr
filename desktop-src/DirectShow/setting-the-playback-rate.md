---
description: Définition de la vitesse de lecture
ms.assetid: 74ae45d3-4fea-491c-af1f-46768df41c5f
title: Définition de la vitesse de lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8a3297ca376b0cc55e4df4884b22d1cb2df81b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106543065"
---
# <a name="setting-the-playback-rate"></a><span data-ttu-id="ab304-103">Définition de la vitesse de lecture</span><span class="sxs-lookup"><span data-stu-id="ab304-103">Setting the Playback Rate</span></span>

<span data-ttu-id="ab304-104">Pour modifier la vitesse de lecture, appelez la méthode [**IMediaSeeking ::**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) se.</span><span class="sxs-lookup"><span data-stu-id="ab304-104">To change the playback rate, call the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span> <span data-ttu-id="ab304-105">Spécifiez le nouveau taux comme une fraction du taux d’origine.</span><span class="sxs-lookup"><span data-stu-id="ab304-105">Specify the new rate as a fraction of the original rate.</span></span> <span data-ttu-id="ab304-106">Par exemple, pour jouer à deux fois la vitesse normale, utilisez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="ab304-106">For example, to play at twice-normal speed, use the following:</span></span>


```C++
pSeek->SetRate(2.0)
```



<span data-ttu-id="ab304-107">Les taux supérieurs à un sont plus rapides que le débit normal.</span><span class="sxs-lookup"><span data-stu-id="ab304-107">Rates greater than one are faster than normal.</span></span> <span data-ttu-id="ab304-108">Les taux entre zéro et un sont plus lents que la normale.</span><span class="sxs-lookup"><span data-stu-id="ab304-108">Rates between zero and one are slower than normal.</span></span> <span data-ttu-id="ab304-109">Les taux négatifs sont définis en tant que lecture descendante, mais dans la pratique, la plupart des filtres ne le prennent pas en charge.</span><span class="sxs-lookup"><span data-stu-id="ab304-109">Negative rates are defined as backward playback, but in practice most filters do not support it.</span></span> <span data-ttu-id="ab304-110">Actuellement, aucun des filtres DirectShow standard ne prend en charge la lecture inversée.</span><span class="sxs-lookup"><span data-stu-id="ab304-110">Currently none of the standard DirectShow filters support reverse playback.</span></span>

<span data-ttu-id="ab304-111">Quelle que soit la vitesse de lecture, la position actuelle et la position d’arrêt sont toujours exprimées par rapport à la source d’origine.</span><span class="sxs-lookup"><span data-stu-id="ab304-111">Regardless of the playback rate, the current position and the stop position are always expressed relative to the original source.</span></span> <span data-ttu-id="ab304-112">Par exemple, si un fichier source a une durée de lecture normale de 20 secondes, le fait de définir la position actuelle sur 10 secondes recherche le milieu du fichier.</span><span class="sxs-lookup"><span data-stu-id="ab304-112">For example, if a source file is 20 seconds long at normal playback rate, setting the current position to 10 seconds will seek to the middle of the file.</span></span> <span data-ttu-id="ab304-113">Si la vitesse de lecture est de 2,0, la position d’arrêt est de 20 secondes et vous recherchez la position à 10 secondes, le fichier est lu pendant 5 secondes de temps réel : 10 secondes, à deux fois la vitesse de lecture normale.</span><span class="sxs-lookup"><span data-stu-id="ab304-113">If the playback rate is 2.0, the stop position is 20 seconds, and you seek to the 10-second position, the file will play for 5 seconds of real time: 10 seconds' worth, at twice the normal playback speed.</span></span> <span data-ttu-id="ab304-114">À une vitesse de lecture de 2,0, la position actuelle augmente à deux fois le taux de l’horloge de référence.</span><span class="sxs-lookup"><span data-stu-id="ab304-114">At a playback rate of 2.0, the current position increases at twice the rate of the reference clock.</span></span>

 

 



