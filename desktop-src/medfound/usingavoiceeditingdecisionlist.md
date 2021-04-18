---
description: Utilisation d’une liste de décisions de modification pour l’encodage vocal
ms.assetid: a3d88483-acc9-47cf-8735-f17bd3b4ad57
title: Utilisation d’une liste de décisions de modification pour l’encodage vocal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970cc40bc5749b9edc1017546020fa3806a9730b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536136"
---
# <a name="using-an-editing-decision-list-for-encoding-voice"></a><span data-ttu-id="f7e4a-103">Utilisation d’une liste de décisions de modification pour l’encodage vocal</span><span class="sxs-lookup"><span data-stu-id="f7e4a-103">Using an Editing Decision List for Encoding Voice</span></span>

<span data-ttu-id="f7e4a-104">Une liste de décisions de modification (EDL) est fournie à un codec qui fournit des informations sur la façon dont des parties spécifiques du contenu doivent être encodées.</span><span class="sxs-lookup"><span data-stu-id="f7e4a-104">An editing decision list (EDL), is data given to a codec that provides information about how specific portions of content should be encoded.</span></span> <span data-ttu-id="f7e4a-105">Le codec vocal Windows Media Audio 9 prend en charge un EDL simple dans lequel vous pouvez spécifier les portions de contenu qui contiennent de la musique.</span><span class="sxs-lookup"><span data-stu-id="f7e4a-105">The Windows Media Audio 9 Voice codec supports a simple EDL in which you can specify the portions of content that contain music.</span></span> <span data-ttu-id="f7e4a-106">Par défaut, le codec détecte les passages de musique lui-même lorsqu’il est configuré pour encoder du contenu mixte.</span><span class="sxs-lookup"><span data-stu-id="f7e4a-106">By default, the codec detects passages of music itself when configured to encode mixed content.</span></span> <span data-ttu-id="f7e4a-107">Vous devez utiliser un EDL uniquement si le codec ne détecte pas correctement les types de contenu.</span><span class="sxs-lookup"><span data-stu-id="f7e4a-107">You should use an EDL only if the codec is not detecting the content types correctly.</span></span>

<span data-ttu-id="f7e4a-108">Pour utiliser un EDL, l’encodeur vocal doit être défini pour encoder le contenu mixte.</span><span class="sxs-lookup"><span data-stu-id="f7e4a-108">To use an EDL, the voice encoder must be set to encode mixed content.</span></span> <span data-ttu-id="f7e4a-109">Configurez le mode du codec vocal sur « mixed » en affectant à la propriété [MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) la valeur 2.</span><span class="sxs-lookup"><span data-stu-id="f7e4a-109">Configure the mode of the voice codec to "mixed" by setting the [MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) property to 2.</span></span> <span data-ttu-id="f7e4a-110">Définissez l’EDL à l’aide de la propriété [ \_ \_ \_ EDL MFPKEY WMAVOICE enc](mfpkey-wmavoice-enc-edlproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="f7e4a-110">Set the EDL using the [MFPKEY\_WMAVOICE\_ENC\_EDL](mfpkey-wmavoice-enc-edlproperty.md) property.</span></span> <span data-ttu-id="f7e4a-111">La valeur de cette propriété est une chaîne contenant une liste délimitée par des virgules des plages de temps du contenu qui doivent être encodées en musique.</span><span class="sxs-lookup"><span data-stu-id="f7e4a-111">The value of this property is a string containing a comma-delimited list of the time ranges in the content that should be encoded as music.</span></span> <span data-ttu-id="f7e4a-112">Le premier élément de la liste est la version de l’EDL, qui est toujours 1.</span><span class="sxs-lookup"><span data-stu-id="f7e4a-112">The first item in the list is the version of the EDL, which is always 1.</span></span> <span data-ttu-id="f7e4a-113">Le deuxième élément est le nombre de sections de musique décrites dans la liste.</span><span class="sxs-lookup"><span data-stu-id="f7e4a-113">The second item is the number of music sections described in the list.</span></span> <span data-ttu-id="f7e4a-114">Après le deuxième élément, plusieurs paires de valeurs sont égales au deuxième élément ; chaque paire de valeurs décrit le point de départ et le point de fin d’un passage de musique dans le contenu, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="f7e4a-114">Following the second item are a number of pairs of values equal to the second item; each pair of values describes the starting and ending point of a music passage in the content, in milliseconds.</span></span>

<span data-ttu-id="f7e4a-115">Par exemple, la chaîne EDL « 1, 4, 1000, 2000, 5000, 6000, 9000, 10000, 13000, 14000 » spécifie quatre passages musicaux, chacun d’entre eux étant une seconde longue.</span><span class="sxs-lookup"><span data-stu-id="f7e4a-115">For example, the EDL string "1, 4, 1000, 2000, 5000, 6000, 9000, 10000, 13000, 14000" specifies four musical passages, each of which is one second long.</span></span> <span data-ttu-id="f7e4a-116">Si les informations de la chaîne EDL ne sont pas valides, elles sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="f7e4a-116">If the information in the EDL string is invalid, it is ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7e4a-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f7e4a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7e4a-118">Utilisation du codec vocal Windows Media Audio 9</span><span class="sxs-lookup"><span data-stu-id="f7e4a-118">Using the Windows Media Audio 9 Voice Codec</span></span>](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[<span data-ttu-id="f7e4a-119">Utilisation de l’audio</span><span class="sxs-lookup"><span data-stu-id="f7e4a-119">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



