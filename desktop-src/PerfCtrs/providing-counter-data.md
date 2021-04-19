---
description: Dans Windows Vista, les compteurs de performances implémentaient une nouvelle architecture (version 2,0) pour fournir des données de compteur.
ms.assetid: c17eda2f-3cf8-40d6-8be6-c1ce190d1a26
title: Fourniture de données de compteur
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: ed5aa4cc505baab9e15d3f69c3fb466712eddbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529834"
---
# <a name="providing-counter-data"></a>Fourniture de données de compteur

Les composants logiciels qui publient des données par le biais des compteurs de performances Windows sont appelés fournisseurs de données de performances.

Windows prend en charge deux types de fournisseurs de données de performances. Les fournisseurs de données de performance hérités (**fournisseurs v1**) sont implémentés à l’aide d’un. Fichier INI et une DLL de performance. Les fournisseurs de données de performances modernes (**fournisseurs v2**) utilisent un. MAN (manifeste XML) et les API du fournisseur de compteurs de performances.

## <a name="manifests"></a>Manifestes

Les fournisseurs de données de performances modernes utilisent un. MAN (manifeste XML) pour définir les données de compteur et utiliser les API du fournisseur de compteurs de performance pour gérer les données dans le contexte du fournisseur.

Les fournisseurs implémentés à l’aide d’un manifeste et des API du fournisseur de compteurs de performances sont souvent appelés **fournisseurs v2**.

Windows prend en charge les fournisseurs V2 en mode utilisateur sur Windows Vista ou version ultérieure. Pour plus d’informations sur le mode utilisateur, consultez [fourniture de données de compteurs à l’aide de la Version 2,0](providing-counter-data-using-version-2-0.md).

Windows prend en charge les fournisseurs V2 en mode noyau sur Windows 7 ou version ultérieure. Pour plus d’informations sur le mode noyau, consultez [surveillance des performances en mode noyau](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).

## <a name="performance-dll-deprecated"></a>DLL de performance (déconseillée)

Dans l’architecture du compteur de performances hérité, les fournisseurs ont implémenté une DLL de performance dans qui s’exécutait dans le processus du consommateur pour collecter et fournir les données de compteur lorsqu’un consommateur l’a demandé. Le fournisseur a utilisé une initialisation (. INI) et les entrées de Registre pour définir les compteurs et configurer la DLL de performance.

Fournisseurs implémentés à l’aide d’un. Les fichiers INI et les DLL de performance sont souvent appelés **fournisseurs v1**.

> [!CAUTION]
> Bien que vous puissiez toujours utiliser une DLL de performance pour fournir des données de compteur, cette architecture est dépréciée en raison de limitations de performances et de fiabilité significatives. En outre, les fournisseurs v1 sont souvent plus difficiles à implémenter, car ils requièrent l’expédition d’une DLL distincte qui doit s’exécuter dans le processus du consommateur.

Pour plus d’informations, consultez [fourniture de données de compteur à l’aide d’une dll de performance](providing-counter-data-using-a-performance-dll.md).
