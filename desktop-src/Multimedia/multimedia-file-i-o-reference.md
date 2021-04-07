---
title: Référence d’e/s de fichier multimédia
description: Référence d’e/s de fichier multimédia
ms.assetid: 1f24432e-7407-4b97-80ab-0a0c40c09253
keywords:
- Windows Multimedia, informations de référence sur les e/s de fichier
- multimédia, référence d’e/s de fichier
- entrée multimédia, référence d’e/s de fichier
- e/s de fichier multimédia, référence
- e/s de fichier, référence
- entrée et sortie (e/s), référence
- E/s (entrée et sortie), référence
- référence pour les e/s de fichier multimédia, à propos de
- informations de référence sur les e/s de fichier multimédia, à propos de
- Référence des e/s de fichier, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0f833b7fb6677e064c19897e276d3961038cfc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724820"
---
# <a name="multimedia-file-io-reference"></a>Référence d’e/s de fichier multimédia

Cette section décrit les fonctions, les macros, les messages et les structures associés à l’entrée et à la sortie d’un fichier multimédia. Ces éléments sont regroupés comme suit.

## <a name="basic-io"></a>E/s de base

-   [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)
-   [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)
-   [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)
-   [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)
-   [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)
-   [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)

## <a name="buffered-io"></a>E/s mises en mémoire tampon

-   [**mmioAdvance**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance)
-   [**mmioFlush**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush)
-   [**mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)
-   [**MMIOINFO**](/previous-versions//dd757322(v=vs.85))
-   [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)
-   [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)

## <a name="riff-io"></a>E/S RIFF

-   [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo)
-   [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc)
-   [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)

## <a name="custom-io-procedures"></a>Procédures d’e/s personnalisées

-   [**IOProc**](/previous-versions//dd757098(v=vs.85))
-   [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [**MMIOM \_ Fermer**](mmiom-close.md)
-   [**MMIOM \_ ouvrir**](mmiom-open.md)
-   [**\_lecture MMIOM**](mmiom-read.md)
-   [**MMIOM \_ REnommer**](mmiom-rename.md)
-   [**MMIOM \_ Seek**](mmiom-seek.md)
-   [**\_écriture MMIOM**](mmiom-write.md)
-   [**MMIOM \_ WRITEFLUSH**](mmiom-writeflush.md)
-   [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[E/s de fichier multimédia](multimedia-file-i-o.md)
</dt> </dl>

 

 