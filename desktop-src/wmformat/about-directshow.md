---
title: À propos de DirectShow (SDK Windows Media format 11)
description: À propos de DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- DirectShow, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd77507643edb220bc71a029779c88fe56760eae
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032241"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="1c783-107">À propos de DirectShow (SDK Windows Media format 11)</span><span class="sxs-lookup"><span data-stu-id="1c783-107">About DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="1c783-108">DirectShow est une architecture de diffusion en continu modulaire, modulaire et de haut niveau pour la plate-forme Windows.</span><span class="sxs-lookup"><span data-stu-id="1c783-108">DirectShow is a high-level, modular, extensible, data-streaming architecture for the Windows platform.</span></span> <span data-ttu-id="1c783-109">Il fournit les composants logiciels sous-jacents et les interfaces de programmation d’application (API) pour un large éventail d’applications audio et vidéo numériques sur le marché dès aujourd’hui.</span><span class="sxs-lookup"><span data-stu-id="1c783-109">It provides the underlying software components and application programming interfaces (APIs) for a wide variety of digital audio and video applications on the market today.</span></span> <span data-ttu-id="1c783-110">DirectShow est disponible dans le cadre du kit de développement logiciel (SDK) Microsoft DirectX.</span><span class="sxs-lookup"><span data-stu-id="1c783-110">DirectShow is available as part of the Microsoft DirectX Software Development Kit.</span></span> <span data-ttu-id="1c783-111">Pour en savoir plus sur DirectShow, consultez le kit de développement logiciel (SDK) Microsoft Platform.</span><span class="sxs-lookup"><span data-stu-id="1c783-111">To learn more about DirectShow, see the Microsoft Platform SDK.</span></span>

<span data-ttu-id="1c783-112">Dans DirectShow, tous les composants de streaming de données sont appelés *filtres*.</span><span class="sxs-lookup"><span data-stu-id="1c783-112">In DirectShow, all data streaming components are called *filters*.</span></span> <span data-ttu-id="1c783-113">Un filtre peut représenter un périphérique matériel, un codeur logiciel ou un décodeur, un convertisseur audio ou vidéo, ou toute fonctionnalité de traitement audio/vidéo.</span><span class="sxs-lookup"><span data-stu-id="1c783-113">A filter may represent a hardware device, a software encoder or decoder, an audio or video renderer, or any audio-video processing capability.</span></span> <span data-ttu-id="1c783-114">Pour permettre aux applications DirectShow de lire et d’écrire du contenu au format Windows Media, y compris le contenu protégé par les Rights Management numériques (DRM), Microsoft fournit deux filtres qui encapsulent des portions du kit de développement logiciel (SDK) de format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1c783-114">To enable DirectShow–based applications to read and write Windows Media Format content, including content protected by Digital Rights Management (DRM), Microsoft provides two filters that encapsulate portions of the Windows Media Format SDK.</span></span> <span data-ttu-id="1c783-115">Il s’agit du [lecteur ASF WM](wm-asf-reader-filter.md) et de l' [enregistreur ASF WM](wm-asf-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="1c783-115">These are the [WM ASF Reader](wm-asf-reader-filter.md) and the [WM ASF Writer](wm-asf-writer-filter.md).</span></span> <span data-ttu-id="1c783-116">Ces filtres et les interfaces qu’ils exposent sont collectivement désignés sous le terme de composants QASF, après la DLL dans laquelle ils sont empaquetés.</span><span class="sxs-lookup"><span data-stu-id="1c783-116">These filters and the interfaces they expose are collectively referred to as the QASF components, after the DLL in which they are packaged.</span></span> <span data-ttu-id="1c783-117">(Q représente quartz, un nom de code précoce pour DirectShow.)</span><span class="sxs-lookup"><span data-stu-id="1c783-117">(The Q stands for Quartz, an early code name for DirectShow.)</span></span>

> [!Note]  
> <span data-ttu-id="1c783-118">L’utilisation des codecs de série Windows Media Audio et Video 9 par le biais des composants QASF DirectShow nécessite Microsoft Windows Millennium Edition ou version ultérieure, ou DirectX 8,0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1c783-118">The use of the Windows Media Audio and Video 9 Series codecs through the DirectShow QASF components requires Microsoft Windows Millennium Edition or later, or DirectX 8.0 or later.</span></span>

 

<span data-ttu-id="1c783-119">Le diagramme suivant montre un graphique de filtre DirectShow permettant de lire les fichiers Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="1c783-119">The following diagram shows a DirectShow filter graph for playing back Windows Media Video files.</span></span>

![graphique de lecture vidéo Windows Media](images/wmv-wmasfreader.png)

<span data-ttu-id="1c783-121">Le [lecteur ASF WM](wm-asf-reader-filter.md) est un composant qasf, les décodeurs sont des composants du kit de développement logiciel (SDK) de format Windows Media hébergés dans le filtre de wrappers DMO (un composant qasf) et les convertisseurs sont des composants DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1c783-121">The [WM ASF Reader](wm-asf-reader-filter.md) is a QASF component, the decoders are Windows Media Format SDK components hosted in the DMO Wrapper filter (a QASF component), and the renderers are DirectShow components.</span></span>

 

 




