---
description: Flux audio et sous-image
ms.assetid: 8d361da3-a33a-401c-a750-f9b952022cf6
title: Flux audio et sous-image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f5c8c74f7507557f374d690a671b62e8b43343
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482536"
---
# <a name="audio-and-subpicture-streams"></a><span data-ttu-id="2f584-103">Flux audio et sous-image</span><span class="sxs-lookup"><span data-stu-id="2f584-103">Audio and Subpicture Streams</span></span>

<span data-ttu-id="2f584-104">Un disque DVD-Video peut avoir jusqu’à huit flux audio, numérotés de 0 à 7, chacun avec jusqu’à six canaux discrets.</span><span class="sxs-lookup"><span data-stu-id="2f584-104">A DVD-Video disc can have up to eight audio streams, numbered zero through seven, each with up to six discrete channels.</span></span> <span data-ttu-id="2f584-105">(Notez que les flux audio et de sous-image sont numérotés à partir de zéro, tandis que les titres, les angles et les niveaux parental sont numérotés à partir de un.) Vous ne pouvez sélectionner qu’un seul de ces flux à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="2f584-105">(Note that audio and subpicture streams are numbered from zero, whereas titles, angles, and parental levels are numbered from one.) Only one of these streams can be selected at any given time.</span></span> <span data-ttu-id="2f584-106">Pour les sous-images, jusqu’à 32 flux sont disponibles, bien qu’un seul flux puisse être activé à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="2f584-106">For subpictures, up to 32 streams are available, although only one stream can be activated at any given time.</span></span> <span data-ttu-id="2f584-107">Les disques sont généralement créés avec des flux audio et sous-images par défaut, mais une application peut permettre aux utilisateurs d’afficher la liste de tous les flux disponibles et de sélectionner celle-ci dans la langue de leur choix.</span><span class="sxs-lookup"><span data-stu-id="2f584-107">Discs are generally authored with default audio and subpicture streams, but an application can enable users to view a list of all the available streams, and select the one in the language they prefer.</span></span> <span data-ttu-id="2f584-108">Les étapes de base de ce processus sont les mêmes pour les flux audio et de sous-image.</span><span class="sxs-lookup"><span data-stu-id="2f584-108">The basic steps in this process are the same for both audio and subpicture streams.</span></span>

1.  <span data-ttu-id="2f584-109">Déterminez le nombre de flux disponibles pour un titre.</span><span class="sxs-lookup"><span data-stu-id="2f584-109">Determine the number of streams available for a title.</span></span>
2.  <span data-ttu-id="2f584-110">Itérez au sein des flux et récupérez les attributs de flux pour chacun.</span><span class="sxs-lookup"><span data-stu-id="2f584-110">Iterate through the streams and retrieve the stream attributes for each.</span></span>
3.  <span data-ttu-id="2f584-111">Récupérez le code de langue de l’identificateur de paramètres régionaux (LCID) retourné et créez une chaîne explicite.</span><span class="sxs-lookup"><span data-stu-id="2f584-111">Retrieve the language code from the returned locale identifier (LCID) and create a human-readable string.</span></span>
4.  <span data-ttu-id="2f584-112">Remplir une zone de liste ou un autre contrôle de l’interface utilisateur pour permettre à l’utilisateur de sélectionner un flux préféré.</span><span class="sxs-lookup"><span data-stu-id="2f584-112">Populate a list box or other user interface (UI) control to enable the user to select a preferred stream.</span></span>

<span data-ttu-id="2f584-113">Dans l’exemple d’application de DVD, la méthode CAudioLangDlg :: MakeAudioStreamList dans Dialogs. cpp illustre les étapes de base.</span><span class="sxs-lookup"><span data-stu-id="2f584-113">In the DVD sample application, the CAudioLangDlg::MakeAudioStreamList method in Dialogs.cpp demonstrates the basic steps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f584-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2f584-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f584-115">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="2f584-115">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



