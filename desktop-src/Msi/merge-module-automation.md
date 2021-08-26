---
description: Mergemod.dll fournit un objet COM qui implémente les opérations de fusion et la génération d’image source pour les modules de fusion. l’objet principal implémente des interfaces pour les programmes C/C++ et les clients automation, y compris Visual Basic et VBScript.
ms.assetid: 877d3691-948f-4aea-89d8-0ff008126ccc
title: Automatisation des modules de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e592429b77671e154b932f3d79f6f57bb39a65ee2058aafd2164428234458acf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043049"
---
# <a name="merge-module-automation"></a>Automatisation des modules de fusion

Mergemod.dll fournit un objet COM qui implémente les opérations de fusion et la génération d’image source pour les modules de fusion. l’objet principal implémente des interfaces pour les programmes C/C++ et les clients automation, y compris Visual Basic et VBScript.

la méthode recommandée pour installer Mergemod.dll consiste à utiliser l’Windows Installer. L’ID du composant contenant l’interface COM Mergemod.dll est {FD153241-37EC-11D2-8892-00A0C981B015}. le même binaire peut être utilisé sur tous les systèmes de Windows et la dll s’inscrit automatiquement par le biais de regsvr32 sur les systèmes antérieurs.

Notez que Mergemod.dll exige que le Msvcrt.dll soit installé sur le système.

Notez que Mergemod.dll 2,0 est requis pour créer des [modules de fusion configurables](configurable-merge-modules.md). Mergemod.dll version 2,0 fournit des fonctionnalités étendues au moment de la génération par le biais de l’interface [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) . Ce CLSID prend en charge toutes les fonctionnalités existantes de l’interface [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) fournie par Mergemod.dll version 1,0. L’interface par défaut sur l’objet [**Merge**](merge-object.md) de Mergemod.dll 2,0 est l’interface **IMsmMerge2** au lieu de l’interface **IMsmMerge** .

[Modèle objet pour Mergemod.dll version 1,0](object-model-for-mergemod-dll-version-1-0.md)

[Modèle objet pour Mergemod.dll version 2,0](object-model-for-mergemod-dll-version-2-0.md)

 

 
