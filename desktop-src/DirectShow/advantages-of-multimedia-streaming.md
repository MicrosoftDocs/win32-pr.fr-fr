---
description: Avantages de la diffusion multimédia en continu
ms.assetid: 01020ad5-430d-4b4d-8de3-bcc81270e132
title: Avantages de la diffusion multimédia en continu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd907d9b8e91cb61709479a2d600323d6d420958
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104116042"
---
# <a name="advantages-of-multimedia-streaming"></a><span data-ttu-id="d729e-103">Avantages de la diffusion multimédia en continu</span><span class="sxs-lookup"><span data-stu-id="d729e-103">Advantages of Multimedia Streaming</span></span>

> [!Note]  
> <span data-ttu-id="d729e-104">Ces API sont déconseillées.</span><span class="sxs-lookup"><span data-stu-id="d729e-104">These APIs are deprecated.</span></span> <span data-ttu-id="d729e-105">Les applications doivent utiliser le filtre d' [**accrochage d’exemple**](sample-grabber-filter.md) ou implémenter un filtre personnalisé pour obtenir des données à partir d’un graphique de filtre DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d729e-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="d729e-106">Lorsque les développeurs utilisent la diffusion multimédia en continu dans leurs applications, cela réduit considérablement la quantité de programmation spécifique au format nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d729e-106">When developers use multimedia streaming in their applications, it greatly reduces the amount of format-specific programming needed.</span></span> <span data-ttu-id="d729e-107">En règle générale, une application qui doit obtenir des données multimédias à partir d’une source de fichier ou matérielle doit tout savoir sur le format des données et sur le périphérique matériel.</span><span class="sxs-lookup"><span data-stu-id="d729e-107">Typically, an application that must obtain media data from a file or hardware source must know everything about the data format and the hardware device.</span></span> <span data-ttu-id="d729e-108">L’application doit gérer la connexion, le transfert de données, toute conversion de données nécessaire et le rendu de données ou le stockage de fichiers réel.</span><span class="sxs-lookup"><span data-stu-id="d729e-108">The application must handle the connection, transfer of data, any necessary data conversion, and the actual data rendering or file storage.</span></span> <span data-ttu-id="d729e-109">Étant donné que chaque format et appareil est légèrement différent, ce processus est souvent complexe et fastidieux.</span><span class="sxs-lookup"><span data-stu-id="d729e-109">Because each format and device is slightly different, this process is often complex and cumbersome.</span></span> <span data-ttu-id="d729e-110">La diffusion multimédia en continu, en revanche, négocie automatiquement le transfert et la conversion des données de la source vers l’application.</span><span class="sxs-lookup"><span data-stu-id="d729e-110">Multimedia streaming, on the other hand, automatically negotiates the transfer and conversion of data from the source to the application.</span></span> <span data-ttu-id="d729e-111">Les interfaces de streaming fournissent une méthode uniforme et prévisible d’accès et de contrôle des données, ce qui permet à une application de lire facilement les données, quelle que soit leur source ou leur format d’origine.</span><span class="sxs-lookup"><span data-stu-id="d729e-111">The streaming interfaces provide a uniform and predictable method of data access and control, which makes it easy for an application to play back the data, regardless of its original source or format.</span></span>

<span data-ttu-id="d729e-112">Les étapes suivantes montrent comment implémenter la diffusion en continu, d’un périphérique matériel à un rendu de lecture.</span><span class="sxs-lookup"><span data-stu-id="d729e-112">The following steps show how to implement streaming, from hardware device to rendered playback.</span></span>

1.  <span data-ttu-id="d729e-113">Une source de données vidéo, telle que DirectShow, expose les interfaces de streaming.</span><span class="sxs-lookup"><span data-stu-id="d729e-113">A source of video data, such as DirectShow, exposes the streaming interfaces.</span></span>
2.  <span data-ttu-id="d729e-114">Le développeur d’applications utilise les interfaces de diffusion multimédia en continu pour gérer la conversion de format de données.</span><span class="sxs-lookup"><span data-stu-id="d729e-114">The application developer uses the multimedia streaming interfaces to handle data format conversion.</span></span>
3.  <span data-ttu-id="d729e-115">Le développeur d’applications utilise les interfaces DirectDraw pour afficher les données résultantes.</span><span class="sxs-lookup"><span data-stu-id="d729e-115">The application developer uses the DirectDraw interfaces to render the resulting data.</span></span>

<span data-ttu-id="d729e-116">La spécification des flux multimédias comprend plusieurs interfaces. chaque interface comprend des méthodes qui contrôlent un certain aspect du processus de diffusion en continu ou gèrent un certain type de données.</span><span class="sxs-lookup"><span data-stu-id="d729e-116">The specification for multimedia streams comprises several interfaces; each interface includes methods that control a certain aspect of the streaming process or handle a certain type of data.</span></span> <span data-ttu-id="d729e-117">Pour plus d’informations, consultez la [liste des interfaces de diffusion multimédia en continu](list-of-multimedia-streaming-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="d729e-117">See [List of Multimedia Streaming Interfaces](list-of-multimedia-streaming-interfaces.md) for additional information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d729e-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d729e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d729e-119">À propos de l’architecture de diffusion multimédia en continu</span><span class="sxs-lookup"><span data-stu-id="d729e-119">About the Multimedia Streaming Architecture</span></span>](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



