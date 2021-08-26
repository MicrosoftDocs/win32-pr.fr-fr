---
title: MSAA n’est pas disponible pour les applications de Windows store
description: MSAA n’est pas disponible pour les applications de Windows store
ms.assetid: C3C12BC7-7A0B-4859-93D0-AA78BC06E90B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eabfd0f855cc4d3940a68fd18e69c4ca2a93774ccdbd0fb1868d2f8f489abea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935079"
---
# <a name="msaa-is-not-available-to-windows-store-apps"></a>MSAA n’est pas disponible pour les applications de Windows store

## <a name="platform"></a>Plateforme

**Clients** – Windows 8 


## <a name="description"></a>Description

Windows 8 ne prend pas en charge MSAA (Microsoft Active Accessibility) pour lire ou automatiser des données accessibles à partir d’applications Windows store. l’API UI Automation (UIA), disponible depuis Windows 7, doit être utilisée à la place. étant donné qu’il n’existe pas de fonctionnalités d’application Windows Store existantes, aucune implémentation existante n’est affectée par cette modification. Cela affecte uniquement les nouvelles applications et fonctionnalités écrites pour Windows 8. Les développeurs peuvent toujours utiliser MSAA pour exposer leurs données d’accessibilité. si les données MSAA sont fournies par Windows fournisseur d’applications du windows Store, les clients UIA pourront toujours lire et automatiser les données.

pour simplifier l’API pour les applications de Windows 8Windows Store, nous avons décidé de prendre en charge uniquement UI Automation en tant que client pour ces applications. Les clients UIA peuvent lire les fournisseurs UIA en mode natif, sans aucune traduction. Les clients UIA peuvent lire les fournisseurs MSAA tels qu’ils sont traduits par le proxy UIA-à-MSAA. cela permet de réduire la charge de test pour les développeurs d’applications Windows Store.

L’élimination de la prise en charge des fournisseurs MSAA réduirait davantage la matrice de test, mais il existe des applications majeures qui sont toujours basées sur MSAA et que nous ne souhaitons pas rendre inaccessibles.

## <a name="manifestation"></a>Manifestation

Windows Les développeurs d’applications du Store ne pourront pas accéder aux détails de MSAA dans le modèle d’application.

## <a name="solution"></a>Solution

aucun nouveau cas automatisé ne doit être créé dans MSAA pour les fonctionnalités des applications Windows store.

permutez les outils intégrés existants qui utilisent MSAA à UIA s’ils ont besoin d’interagir avec les applications Windows store. Windows Les développeurs d’applications du Store doivent utiliser l’API UI Automation.

## <a name="resources"></a>Ressources

-   [Notions de base d’UI Automation](../winauto/entry-uiauto-win32.md)

 

 