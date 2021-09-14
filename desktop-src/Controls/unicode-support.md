---
title: Prise en charge Unicode pour les contrôles communs
description: Cette rubrique décrit comment prendre en charge Unicode pour les notifications de contrôle courantes.
ms.assetid: 5020F638-261D-4D32-ACC4-F9572EDBE875
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb029d6e1c018f1793c749aefb2f88104559cae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115405"
---
# <a name="unicode-support-for-common-controls"></a>Prise en charge Unicode pour les contrôles communs

Cette rubrique décrit comment prendre en charge Unicode pour les notifications de contrôle courantes.


pour les versions 5,80 et ultérieures de comctl32.dll, les notifications de contrôles communs prennent en charge les formats ANSI et Unicode sur les systèmes Windows 95 ou version ultérieure. Le système détermine le format à utiliser en envoyant votre fenêtre à un message [**WM \_ NOTIFYFORMAT**](wm-notifyformat.md) . Pour spécifier un format, retournez NFR \_ ANSI pour les notifications ANSI ou NFR \_ Unicode pour les notifications Unicode. Si vous ne gérez pas ce message, le système appelle [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) pour déterminer le format. étant donné que Windows 95 et Windows 98 retournent toujours **false** pour cet appel de fonction, ils utilisent des notifications ANSI par défaut.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des contrôles communs](common-controls-intro.md)
</dt> </dl>

 

 