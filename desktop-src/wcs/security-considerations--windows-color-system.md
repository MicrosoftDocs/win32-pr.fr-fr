---
title: Considérations sur la sécurité - Système de couleurs Windows
description: Considérations sur la sécurité - Système de couleurs Windows
ms.assetid: 9e8b7c38-3c4f-4537-a7e1-6ad0daa39497
keywords:
- Windows Système de couleurs (WCS), sécurité
- WCS (Windows Color System), sécurité
- gestion des couleurs des images, sécurité
- gestion des couleurs, sécurité
- sécurité pour le système de couleur Windows (WCS)
- Module de gestion des couleurs (CMM)
- CMM (module de gestion des couleurs)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e710a0224c10d4f7cd7aa1565e88d00da539370974719129a37d735f11a29fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118444666"
---
# <a name="security-considerations-windows-color-system"></a>considérations relatives à la sécurité : Windows système de couleurs

Ce document fournit des informations sur les considérations de sécurité liées à la gestion des couleurs des images. Ce document ne fournit pas tout ce que vous devez savoir sur les problèmes de sécurité. Utilisez-le plutôt comme point de départ et référence pour ce domaine technologique.

## <a name="non-microsoft-cmms-can-run-in-system-context"></a>Les CMMs non-Microsoft peuvent s’exécuter dans le contexte du système

Les modules de gestion des couleurs non-Microsoft (CMMs) doivent être traités comme des pilotes d’imprimante non-Microsoft, car ils peuvent s’exécuter dans un contexte système pour les opérations d’impression.
