---
title: DirectWrite (DWrite)
description: Les applications actuelles doivent prendre en charge le rendu de texte de haute qualité, les polices de contour indépendantes de la résolution et la prise en charge complète du texte Unicode et de la disposition. DirectWrite, une API [DirectX](../directx.md) , fournit ces fonctionnalités et bien plus encore.
ms.assetid: 62a8d723-ae1c-4cbc-a9da-3177e80d4a3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b1e2ff44083a56a7202847fc07ad9daaa67b7ba
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2020
ms.locfileid: "104464174"
---
# <a name="directwrite-dwrite"></a>DirectWrite (DWrite)

## <a name="purpose"></a>Objectif

Les applications actuelles doivent prendre en charge le rendu de texte de haute qualité, les polices de contour indépendantes de la résolution et la prise en charge complète du texte Unicode et de la disposition. DirectWrite, une API [DirectX](../directx.md) , fournit ces fonctionnalités et bien plus encore.

- Système de disposition de texte indépendant du périphérique qui améliore la lisibilité du texte dans les documents et dans l’interface utilisateur.
- Rendu de texte [Microsoft ClearType](/typography/cleartype/) de haute qualité, sous-pixel, qui peut utiliser [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md)ou la technologie de rendu propre à l’application.
- Texte avec accélération matérielle, lorsqu’il est utilisé avec [Direct2D](rendering-by-using-direct2d.md).
- Prise en charge du texte à plusieurs formats.
- Prise en charge des fonctionnalités typographiques avancées des polices OpenType.
- Prise en charge de la disposition et du rendu du texte dans toutes les langues prises en charge.
- Mise en page et rendu compatibles [GDI](interoperating-with-gdi.md).

L’API prend en charge la mesure, le dessin et le test d’atteinte du texte à plusieurs formats. DirectWrite gère le texte dans toutes les langues prises en charge pour les applications globales et localisées, en se basant sur l’infrastructure de langage clé qui se trouve dans Windows 7. DirectWrite fournit également une API de rendu de glyphe de bas niveau pour les développeurs désireux de réaliser leurs propres disposition et traitement d’Unicode à glyphe.

> [!NOTE]
> [Project REUNION](/windows/apps/project-reunion/) introduit une nouvelle version de DirectWrite &mdash; appelée DWriteCore &mdash; qui s’exécute sur des versions de Windows vers Windows 8, et qui ouvre la porte pour que vous l’utilisiez sur plusieurs plateformes. Pour plus d’informations, consultez [vue d’ensemble de DWriteCore](dwritecore-overview.md).

## <a name="run-time-requirements"></a>Conditions d’exécution

- Windows 7 ou Windows Vista avec Service Pack 2 (SP2) et mise à jour de la plateforme pour Windows Vista
- Windows Server 2008 R2 ou Windows Server 2008 avec Service Pack 2 (SP2) et mise à jour de plateforme pour Windows Server 2008

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [Nouveautés de DirectWrite](what-s-new-in-directwrite-for-windows-8-consumer-preview.md)<br/> | Voici quelques-uns des nouveaux ajouts à DirectWrite. <br/> |
| [Guide de programmation](programming-guide.md)<br/> | Les rubriques suivantes fournissent une vue d’ensemble de l’API DirectWrite.<br/> |
| [Référence sur l’API](reference.md)<br/> | Décrit l’API DirectWrite.<br/> |
| [Exemple de Code](samples.md)<br/> | Cette section contient des informations sur les exemples de programmes pour DirectWrite.<br/> |
