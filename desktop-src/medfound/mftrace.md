---
description: MFTrace est un outil permettant de générer des journaux de suivi pour les applications Media Foundation.
ms.assetid: 55b421c8-e87c-4dd2-8649-93832c93f999
title: MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4a216f225141ceccf3f1357025dd069afa494d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540945"
---
# <a name="mftrace"></a>MFTrace

MFTrace est un outil permettant de générer des journaux de suivi pour les applications Media Foundation.

## <a name="in-this-section"></a>Dans cette section

-   [Utilisation de MFTrace](using-mftrace.md)
-   [Mots clés MFTrace](mftrace-keywords.md)
-   [Fichier de configuration MFTrace](mftrace-configuration-file.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------------|---------------------------------------------------------------------------------------|
| Version minimale du kit de développement logiciel      | Kit de développement logiciel (SDK) Microsoft Windows pour Windows 7 et .NET Framework 4,0 |
| Système d’exploitation minimal | Windows Vista                                                                         |



 

MFTrace requiert les dll suivantes, qui sont également fournies dans le kit de développement logiciel (SDK).

-   detoured.dll
-   mfdetours.dll

Le kit de développement logiciel (SDK) fournit des versions 32 bits et 64 bits de MFTrace. MFTrace ne prend pas en charge WOW64 ; pour suivre un processus 32 bits s’exécutant sur Windows 64 bits, utilisez la version 32 bits de MFTrace.

SDK-root sur les systèmes 32 bits : \Program Files\Windows Kits\10 SDK-root on 64 bit System : \Program Files (x86) \Windows Kits\10 vous trouverez mftrace <à la racine> \bin du kit de développement logiciel (SDK) \<sdk-version> \<architecture>\mftrace.exe

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Outils de Media Foundation](media-foundation-tools.md)
</dt> </dl>

 

 



