---
description: MFTrace est un outil permettant de générer des journaux de suivi pour les applications Media Foundation.
ms.assetid: 55b421c8-e87c-4dd2-8649-93832c93f999
title: MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542ac9325b33fc8f1a76394d203dbf1d27919bd6
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885223"
---
# <a name="mftrace"></a>MFTrace

MFTrace est un outil permettant de générer des journaux de suivi pour les applications Media Foundation.

## <a name="in-this-section"></a>Dans cette section

-   [Utilisation de MFTrace](using-mftrace.md)
-   [Mots clés MFTrace](mftrace-keywords.md)
-   [Fichier de configuration MFTrace](mftrace-configuration-file.md)

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------------|---------------------------------------------------------------------------------------|
| Version minimale du kit de développement logiciel      | kit de développement logiciel (SDK) Microsoft Windows pour Windows 7 et .NET Framework 4,0 |
| Système d’exploitation minimal | Windows Vista                                                                         |



 

MFTrace requiert les dll suivantes, qui sont également fournies dans le kit de développement logiciel (SDK).

-   detoured.dll
-   mfdetours.dll

Le kit de développement logiciel (SDK) fournit des versions 32 bits et 64 bits de MFTrace. MFTrace ne prend pas en charge WOW64 ; pour suivre un processus 32 bits s’exécutant sur un Windows 64 bits, utilisez la version 32 bits de MFTrace.

sdk-root sur les systèmes 32 bits : \program files \ Windows Kits\10 sdk-root sur 64 bit system : \program files (x86) \ Windows Kits\10 vous trouverez mftrace à la &lt; racine du sdk-root &gt; \bin \<sdk-version> \<architecture>\mftrace.exe

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Outils de Media Foundation](media-foundation-tools.md)
</dt> </dl>

 

 



