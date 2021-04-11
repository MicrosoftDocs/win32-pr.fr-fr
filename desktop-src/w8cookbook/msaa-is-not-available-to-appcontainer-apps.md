---
title: MSAA n’est pas disponible pour les applications du Windows Store
description: MSAA n’est pas disponible pour les applications du Windows Store
ms.assetid: C3C12BC7-7A0B-4859-93D0-AA78BC06E90B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e9c1221850b1fa97a3a0d5fcef119c21277486
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104031993"
---
# <a name="msaa-is-not-available-to-windows-store-apps"></a>MSAA n’est pas disponible pour les applications du Windows Store

## <a name="platform"></a>Plateforme

**Clients** – Windows 8 


## <a name="description"></a>Description

Windows 8 ne prend pas en charge MSAA (Microsoft Active Accessibility) pour lire ou automatiser des données accessibles à partir d’applications du Windows Store. L’API UI Automation (UIA), disponible depuis Windows 7, doit être utilisée à la place. Étant donné qu’il n’existe pas de fonctionnalités d’application Windows Store existantes, aucune implémentation existante n’est affectée par cette modification. Cela affecte uniquement les nouvelles applications et fonctionnalités écrites pour Windows 8. Les développeurs peuvent toujours utiliser MSAA pour exposer leurs données d’accessibilité. Si les données MSAA sont fournies par le fournisseur d’applications du Windows Store, les clients UIA pourront toujours lire et automatiser les données.

Pour simplifier l’API pour les applications du Windows Store 8Windows, nous avons décidé de prendre en charge uniquement UI Automation en tant que client pour ces applications. Les clients UIA peuvent lire les fournisseurs UIA en mode natif, sans aucune traduction. Les clients UIA peuvent lire les fournisseurs MSAA tels qu’ils sont traduits par le proxy UIA-à-MSAA. Cela réduira la charge de test pour les développeurs d’applications du Windows Store.

L’élimination de la prise en charge des fournisseurs MSAA réduirait davantage la matrice de test, mais il existe des applications majeures qui sont toujours basées sur MSAA et que nous ne souhaitons pas rendre inaccessibles.

## <a name="manifestation"></a>Manifestation

Les développeurs d’applications du Windows Store ne seront pas en mesure d’accéder aux détails de MSAA dans le modèle d’application.

## <a name="solution"></a>Solution

Aucun nouveau cas automatisé ne doit être créé dans MSAA pour les fonctionnalités des applications du Windows Store.

Basculez tous les outils intégrés existants qui utilisent MSAA vers UIA s’ils ont besoin d’interagir avec les applications du Windows Store. Les développeurs d’applications du Windows Store doivent utiliser l’API UI Automation.

## <a name="resources"></a>Ressources

-   [Notions de base d’UI Automation](../winauto/entry-uiauto-win32.md)

 

 