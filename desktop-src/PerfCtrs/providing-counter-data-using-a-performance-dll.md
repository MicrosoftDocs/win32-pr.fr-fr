---
description: Un service, un pilote ou une application qui souhaite fournir des données de compteur peut écrire une DLL de performance pour fournir les données.
ms.assetid: 030316e5-f9f3-4333-9bb4-7ad301bbe7bf
title: Fourniture de données de compteur à l’aide d’une DLL de performance
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: e14b8a0e59b1fc9af3d8cad6e895d4a0067b9ae6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218289"
---
# <a name="providing-counter-data-using-a-performance-dll"></a>Fourniture de données de compteur à l’aide d’une DLL de performance

> [!IMPORTANT]
> En raison des limitations de performances et de fiabilité significatives, la méthode permettant de fournir des données de compteurs de performances que cette rubrique décrit peut être modifiée ou non disponible à l’avenir. Au lieu de cela, Microsoft vous recommande d’utiliser la méthode décrite dans la rubrique [fourniture de données de compteur à l’aide de la Version 2,0](providing-counter-data-using-version-2-0.md) pour la création de nouveaux compteurs de performances et la migration des compteurs de performances existants pour utiliser également cette méthode.

Un service, un pilote ou une application qui souhaite fournir des données de compteur peut écrire une DLL de performance pour fournir les données. Lorsqu’un consommateur interroge des données de performances, le système charge la DLL du fournisseur dans le processus du consommateur et appelle le fournisseur pour collecter les données. Pour plus d’informations sur l’écriture de la DLL de performance, consultez [création d’une DLL d’extension de performance](creating-a-performance-extension-dll.md).

Le système utilise le registre pour déterminer le fournisseur à appeler. Pour plus d’informations sur l’inscription de votre fournisseur et les compteurs qu’il prend en charge, consultez [Ajout de compteurs de performances](adding-performance-counters.md).

> [!Note]
> Les dll de performance ne sont pas prises en charge sur Windows OneCore. si vous écrivez un composant qui doit s’exécuter sur Windows OneCore, utilisez la méthode décrite dans la rubrique [fourniture de données de compteur à l’aide de la Version 2,0](providing-counter-data-using-version-2-0.md).
