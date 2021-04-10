---
title: Prise en charge Unicode pour les contrôles communs
description: Cette rubrique décrit comment prendre en charge Unicode pour les notifications de contrôle courantes.
ms.assetid: 5020F638-261D-4D32-ACC4-F9572EDBE875
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb029d6e1c018f1793c749aefb2f88104559cae
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941488"
---
# <a name="unicode-support-for-common-controls"></a><span data-ttu-id="44f3b-103">Prise en charge Unicode pour les contrôles communs</span><span class="sxs-lookup"><span data-stu-id="44f3b-103">Unicode Support for Common Controls</span></span>

<span data-ttu-id="44f3b-104">Cette rubrique décrit comment prendre en charge Unicode pour les notifications de contrôle courantes.</span><span class="sxs-lookup"><span data-stu-id="44f3b-104">This topic describes how to support Unicode for common control notifications.</span></span>


<span data-ttu-id="44f3b-105">Pour les versions 5,80 et ultérieures de comctl32.dll, les notifications de contrôles communs prennent en charge les formats ANSI et Unicode sur les systèmes Windows 95 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="44f3b-105">For versions 5.80 and later of comctl32.dll, common controls notifications support both ANSI and Unicode formats on Windows 95 systems or later.</span></span> <span data-ttu-id="44f3b-106">Le système détermine le format à utiliser en envoyant votre fenêtre à un message [**WM \_ NOTIFYFORMAT**](wm-notifyformat.md) .</span><span class="sxs-lookup"><span data-stu-id="44f3b-106">The system determines which format to use by sending your window a [**WM\_NOTIFYFORMAT**](wm-notifyformat.md) message.</span></span> <span data-ttu-id="44f3b-107">Pour spécifier un format, retournez NFR \_ ANSI pour les notifications ANSI ou NFR \_ Unicode pour les notifications Unicode.</span><span class="sxs-lookup"><span data-stu-id="44f3b-107">To specify a format, return NFR\_ANSI for ANSI notifications or NFR\_UNICODE for Unicode notifications.</span></span> <span data-ttu-id="44f3b-108">Si vous ne gérez pas ce message, le système appelle [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) pour déterminer le format.</span><span class="sxs-lookup"><span data-stu-id="44f3b-108">If you do not handle this message, the system calls [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) to determine the format.</span></span> <span data-ttu-id="44f3b-109">Étant donné que Windows 95 et Windows 98 retournent toujours **false** pour cet appel de fonction, ils utilisent des notifications ANSI par défaut.</span><span class="sxs-lookup"><span data-stu-id="44f3b-109">Since Windows 95 and Windows 98 always return **FALSE** to this function call, they use ANSI notifications by default.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44f3b-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="44f3b-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44f3b-111">À propos des contrôles communs</span><span class="sxs-lookup"><span data-stu-id="44f3b-111">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 