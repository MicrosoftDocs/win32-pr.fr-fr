---
title: API de grossissement
description: L’API d’agrandissement permet aux applications d’agrandir la totalité de l’écran ou des parties de l’écran, et d’appliquer des effets de couleur.
ms.assetid: 644af100-82ec-4450-b809-cede9b388cb4
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 7e6c652c2cca8e3c5675b390e93b70ad0b522a44
ms.sourcegitcommit: 541c08d5d36109b754f39bf89e57404f007c5f63
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/08/2020
ms.locfileid: "103841861"
---
# <a name="magnification-api"></a>API de grossissement

## <a name="purpose"></a>Objectif

L’API d’agrandissement permet aux applications d’agrandir la totalité de l’écran ou des parties de l’écran, et d’appliquer des effets de couleur.

## <a name="where-applicable"></a>Le cas échéant

Grâce à l’API d’agrandissement, les développeurs peuvent créer des applications de technologie d’assistance Windows qui agrandissent l’écran et appliquent des effets de couleur au contenu de l’écran agrandi. Pour les utilisateurs dont la vision est faible, la taille de l’image agrandie et les effets de couleur peuvent faciliter l’utilisation et l’utilisation de l’ordinateur.

## <a name="developer-audience"></a>Développeurs concernés

L’API d’agrandissement est conçue principalement pour les développeurs C et C++ qui comprennent la programmation Windows et qui sont familiarisés avec les concepts de la programmation graphique.

## <a name="run-time-requirements"></a>Conditions d’exécution

La version initiale de l’API d’agrandissement est prise en charge sur Windows Vista et les systèmes d’exploitation ultérieurs. Une deuxième version ajoute des fonctionnalités d’agrandissement plein écran et est prise en charge sur Windows 8 et versions ultérieures.

L’API est prise en charge par Magnification.dll. Pour compiler votre application, incluez grossissement. h et un lien vers grossissement. lib.

> [!Note]  
> L’API d’agrandissement n’est pas prise en charge sous WOW64 ; autrement dit, une application de loupe 32 bits ne s’exécutera pas correctement sous Windows 64 bits.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|:---|:---|
| [Vue d’ensemble de l’API zoom](magapi-intro.md)<br/> | Cette rubrique décrit l’API d’agrandissement et explique comment l’utiliser dans une application.<br/> |
| [Référence](entry-magapi-ref.md)<br/>  | Cette section contient des informations de référence sur l’API d’agrandissement.<br/>|
| [Exemples](magapi-samples-entry.md)<br/> | L’exemple d’application suivant montre comment utiliser l’API de grossissement pour créer une loupe plein écran qui agrandit la totalité de l’écran et une loupe avec fenêtres qui agrandit et affiche une partie de l’écran dans une fenêtre.<br/> |

## <a name="related-topics"></a>Rubriques connexes

[Site Web Microsoft Accessibility](https://www.microsoft.com/accessibility/), [accessibilité dans Windows 10](/windows/apps/accessibility)
