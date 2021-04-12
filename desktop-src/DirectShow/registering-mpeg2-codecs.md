---
description: Inscription des codecs MPEG2
ms.assetid: f730a7df-af8f-4dce-9bfe-6ee1eca8fd90
title: Inscription des codecs MPEG2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de007cebdd0a911f6b43f21003ed3ede0bc1723
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108923"
---
# <a name="registering-mpeg2-codecs"></a><span data-ttu-id="01218-103">Inscription des codecs MPEG2</span><span class="sxs-lookup"><span data-stu-id="01218-103">Registering MPEG2 Codecs</span></span>

<span data-ttu-id="01218-104">Cette rubrique s’applique uniquement à Windows XP Media Center Edition.</span><span class="sxs-lookup"><span data-stu-id="01218-104">This topic applies to Windows XP Media Center Edition only.</span></span>

<span data-ttu-id="01218-105">Windows XP Media Center Edition gère deux clés de registre qu’il utilise pour déterminer le codec à utiliser pour lire les fichiers audio et vidéo MPEG2.</span><span class="sxs-lookup"><span data-stu-id="01218-105">Windows XP Media Center Edition maintains two registry keys that it uses to determine which codec to use to play back MPEG2 video and audio files.</span></span> <span data-ttu-id="01218-106">La première clé de Registre spécifie le codec MPEG2 préféré du fabricant de l’ordinateur, et la seconde répertorie tous les codecs compatibles Media Center qui sont actuellement installés sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="01218-106">The first registry key specifies the computer manufacturer's preferred MPEG2 codec, and the second lists all of the Media Center compatible codecs that are currently installed on the computer.</span></span> <span data-ttu-id="01218-107">Quand Media Center doit lire un fichier MPEG2, il utilise le codec préféré du fabricant, si celui-ci est spécifié.</span><span class="sxs-lookup"><span data-stu-id="01218-107">When Media Center needs to play back an MPEG2 file, it uses the manufacturer's preferred codec, if one is specified.</span></span> <span data-ttu-id="01218-108">Si ce n’est pas le cas, il utilise le premier codec compatible Media Center listé dans le registre.</span><span class="sxs-lookup"><span data-stu-id="01218-108">If not, it uses the first Media Center compatible codec listed in the registry.</span></span> <span data-ttu-id="01218-109">Si le registre ne spécifie aucun codec préféré ou compatible, Media Center utilise la valeur de filtre DirectShow standard pour choisir un codec.</span><span class="sxs-lookup"><span data-stu-id="01218-109">If the registry specifies no preferred or compatible codecs, Media Center uses the standard DirectShow filter merit to choose a codec.</span></span>

<span data-ttu-id="01218-110">Pour vous assurer que Media Center utilise toujours un codec MPEG2 compatible, les fabricants d’ordinateurs Media Center doivent spécifier le codec MPEG2 préféré à l’emplacement de Registre suivant :</span><span class="sxs-lookup"><span data-stu-id="01218-110">To ensure that Media Center always uses a compatible MPEG2 codec, manufacturers of Media Center computers should specify the preferred MPEG2 codec at the following registry location:</span></span>


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Media Center\Service\Video
```



<span data-ttu-id="01218-111">Les données de la clé doivent être les suivantes :</span><span class="sxs-lookup"><span data-stu-id="01218-111">The key data should be as follows:</span></span>


```C++
PreferredMPEG2VideoDecoder=REG_SZ "{MPEG2 Video CLSID GUID}"
PreferredMPEG2AudioDecoder=REG_SZ "{MPEG2 Audio CLSID GUID}"
```



<span data-ttu-id="01218-112">Le programme d’installation d’un codec MPEG2 compatible avec Media Center doit inscrire le codec en créant deux instances de la clé de Registre suivante : une pour le codec vidéo et une pour le codec audio :</span><span class="sxs-lookup"><span data-stu-id="01218-112">The setup program for a Media Center compatible MPEG2 codec should register the codec by creating two instances of the following registry key—one for the video codec and one for the audio codec:</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\{083863F1-70DE-11d0-BD40-00A0C911CE86}\Instance\<Your Codec CLSID here>\Capabilities]
```



<span data-ttu-id="01218-113">Les données de la clé doivent être les suivantes :</span><span class="sxs-lookup"><span data-stu-id="01218-113">The key data should be as follows:</span></span>


```C++
"{374ac4df-7c98-4257-b13d-36087dbee458}"=dword:00000001
```



 

 



