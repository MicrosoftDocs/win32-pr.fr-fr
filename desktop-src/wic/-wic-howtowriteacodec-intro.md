---
description: Le composant WIC (Windows Imaging Component) est une plateforme extensible pour l’imagerie numérique sur les systèmes d’exploitation Windows Vista et Windows 7.
ms.assetid: ffcd5239-ae2d-436f-9402-8c10a79256c3
title: Introduction (écriture d’un codec WIC-Enabled)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776bf9f2c0cb5df8b45ce04d55f20d40d05a12a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520993"
---
# <a name="introduction-how-to-write-a-wic-enabled-codec"></a><span data-ttu-id="5eb72-103">Introduction (écriture d’un codec WIC-Enabled)</span><span class="sxs-lookup"><span data-stu-id="5eb72-103">Introduction (How to Write a WIC-Enabled Codec)</span></span>

<span data-ttu-id="5eb72-104">Le composant WIC (Windows Imaging Component) est une plateforme extensible pour l’imagerie numérique sur les systèmes d’exploitation Windows Vista et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5eb72-104">The Windows Imaging Component (WIC) is an extensible platform for digital imaging on the Windows Vista and Windows 7 operating systems.</span></span> <span data-ttu-id="5eb72-105">WIC est également disponible sur Windows XP et Windows Server 2003, soit dans le cadre de Microsoft .NET Framework 3,0, soit en tant que composant distinct que vous pouvez redistribuer.</span><span class="sxs-lookup"><span data-stu-id="5eb72-105">WIC is also available on Windows XP and Windows Server 2003, either as part of Microsoft .NET Framework 3.0 or as a separate component that you can redistribute.</span></span> <span data-ttu-id="5eb72-106">Toute application utilisant le WIC peut accéder à des images, les afficher, les traiter et les imprimer dans n’importe quel format d’image qui fournit un codec WIC, à l’aide d’un ensemble unique d’interfaces cohérentes qui éliminent la nécessité d’une connaissance spécialisée de formats spécifiques.</span><span class="sxs-lookup"><span data-stu-id="5eb72-106">Any application using the WIC can access, display, process, and print images in any image format that provides a WIC-enabled codec, using a single set of consistent interfaces that eliminate the need for specialized knowledge of specific formats.</span></span>

<span data-ttu-id="5eb72-107">L’Explorateur Windows Vista, la Galerie de photos Windows Vista, la Galerie de photos en direct et la visionneuse de photos Windows 7 s’appuient sur WIC.</span><span class="sxs-lookup"><span data-stu-id="5eb72-107">The Windows Vista Explorer, Windows Vista Photo Gallery, Live Photo Gallery, and Windows 7 Photo Viewer are built on WIC.</span></span> <span data-ttu-id="5eb72-108">Après l’installation d’un codec WIC activé sur un système Windows Vista ou Windows 7, le système d’exploitation offre le même niveau de prise en charge pour le format d’image associé que pour les formats d’image standard fournis avec la plateforme.</span><span class="sxs-lookup"><span data-stu-id="5eb72-108">After a WIC-enabled codec is installed on a Windows Vista or Windows 7 system, the operating system provides the same level of support for the associated image format as for the standard image formats that ship with the platform.</span></span> <span data-ttu-id="5eb72-109">Étant donné que vous écrivez le codec pour votre propre format d’image, vous pouvez garantir une qualité cohérente partout où votre format d’image est utilisé et vous bénéficiez des avantages de la prise en charge complète des plateformes.</span><span class="sxs-lookup"><span data-stu-id="5eb72-109">Because you write the codec for your own image format, you can ensure consistent quality wherever your image format is used, and you get the benefits of full platform support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5eb72-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5eb72-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5eb72-111">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="5eb72-111">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5eb72-112">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="5eb72-112">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="5eb72-113">Fonctionnement du composant de création d’images Windows</span><span class="sxs-lookup"><span data-stu-id="5eb72-113">How The Windows Imaging Component Works</span></span>](-wic-howwicworks.md)
</dt> <dt>

<span data-ttu-id="5eb72-114">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="5eb72-114">How to Write a WIC-Enabled CODEC</span></span>
</dt> <dt>

[<span data-ttu-id="5eb72-115">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="5eb72-115">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



