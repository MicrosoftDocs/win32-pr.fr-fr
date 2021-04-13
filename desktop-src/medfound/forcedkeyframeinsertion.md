---
description: Insertion d’une image clé forcée
ms.assetid: 844e5a01-96db-4a69-9704-f0fdbfee3957
title: Insertion d’une image clé forcée (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d053f97c7aff08f61fa56d07db0a28b20c797d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484073"
---
# <a name="forced-key-frame-insertion-microsoft-media-foundation"></a><span data-ttu-id="4ef31-103">Insertion d’une image clé forcée (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="4ef31-103">Forced Key Frame Insertion (Microsoft Media Foundation)</span></span>

<span data-ttu-id="4ef31-104">Quand vous configurez un objet d’encodeur vidéo, vous pouvez définir un intervalle maximal pour les images clés dans le contenu encodé.</span><span class="sxs-lookup"><span data-stu-id="4ef31-104">When you configure a video encoder object, you can set a maximum interval for key frames in the encoded content.</span></span> <span data-ttu-id="4ef31-105">Toutefois, le codec place les images clés dans cet intervalle comme indiqué par le contenu. l’intervalle d’image clé n’est pas constant.</span><span class="sxs-lookup"><span data-stu-id="4ef31-105">However, the codec will place key frames within that interval as dictated by the content; the key frame interval is not constant.</span></span> <span data-ttu-id="4ef31-106">Pour certaines applications, la distance d’image clé est très importante.</span><span class="sxs-lookup"><span data-stu-id="4ef31-106">For some applications, the key frame distance is very important.</span></span> <span data-ttu-id="4ef31-107">Par exemple, une application de modification vidéo a besoin d’images clés à des emplacements logiques à un éditeur, tels que des arrêts de scène et des transitions de capture.</span><span class="sxs-lookup"><span data-stu-id="4ef31-107">For example, a video editing application needs key frames at locations that are logical to an editor, like at scene breaks and shot transitions.</span></span>

<span data-ttu-id="4ef31-108">L’insertion d’une image clé forcée est une fonctionnalité qui vous permet de demander qu’une trame d’entrée soit encodée sous la forme d’une image clé.</span><span class="sxs-lookup"><span data-stu-id="4ef31-108">Forced key frame insertion is a feature that enables you to request that an input frame be encoded as a key frame.</span></span> <span data-ttu-id="4ef31-109">L’encodeur essaiera d’honorer ces requêtes, mais les paramètres de mémoire tampon (vitesse de transmission et fenêtre de mémoire tampon) configurés pour la session d’encodage sont toujours prioritaires.</span><span class="sxs-lookup"><span data-stu-id="4ef31-109">The encoder will try to honor these requests, but the buffer settings (bit rate and buffer window) configured for the encoding session always take precedence.</span></span>

<span data-ttu-id="4ef31-110">Les objets d’encodeur vidéo implémentent l’insertion d’une image clé forcée en réponse à une extension d’unité de données jointe à l’exemple d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4ef31-110">The video encoder objects implement forced key frame insertion as a response to a data unit extension attached to the input sample.</span></span> <span data-ttu-id="4ef31-111">Pour plus d’informations sur les extensions d’unité de données, consultez [utilisation des extensions d’unité de données](usingdataunitextensions.md).</span><span class="sxs-lookup"><span data-stu-id="4ef31-111">For more information about data unit extensions, see [Using Data Unit Extensions](usingdataunitextensions.md).</span></span>

<span data-ttu-id="4ef31-112">Les données d’extension pour l’insertion d’une image clé forcée sont identifiées par la valeur GUID suivante : **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**.</span><span class="sxs-lookup"><span data-stu-id="4ef31-112">The extension data for forced key frame insertion is identified by the following GUID value: **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**.</span></span> <span data-ttu-id="4ef31-113">Les extensions individuelles sont des valeurs **bool** .</span><span class="sxs-lookup"><span data-stu-id="4ef31-113">The individual extensions are **BOOL** values.</span></span> <span data-ttu-id="4ef31-114">Définissez la valeur sur **true** pour indiquer une demande d’image clé.</span><span class="sxs-lookup"><span data-stu-id="4ef31-114">Set the value to **TRUE** to indicate a key frame request.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ef31-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4ef31-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ef31-116">Utilisation des extensions d’unité de données</span><span class="sxs-lookup"><span data-stu-id="4ef31-116">Using Data Unit Extensions</span></span>](usingdataunitextensions.md)
</dt> <dt>

[<span data-ttu-id="4ef31-117">Utilisation de la vidéo</span><span class="sxs-lookup"><span data-stu-id="4ef31-117">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



