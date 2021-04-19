---
title: Conditions requises pour la signature de la fonctionnalité de démarrage sécurisé pour les pilotes en mode noyau
description: Conditions requises pour la signature de la fonctionnalité de démarrage sécurisé pour les pilotes en mode noyau
ms.assetid: 7FF64BA2-89E3-4E6F-B542-7BC7BF7F4FB2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a63a8b1fca1677aa125bac96dfec290dcd736b5
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "106510911"
---
# <a name="secure-boot-feature-signing-requirements-for-kernel-mode-drivers"></a>Conditions requises pour la signature de la fonctionnalité de démarrage sécurisé pour les pilotes en mode noyau

## <a name="platforms"></a>Plateformes

**Clients** – Windows 8  
**Serveurs** – Windows Server 2012  


## <a name="description"></a>Description

Dans Windows 8 et Windows Server 2012, y compris WinPE, le noyau a été verrouillé pour empêcher les logiciels malveillants introduits par les kits de démarrage ou racine de contourner les exigences de sécurité du système d’exploitation Windows pour les pilotes signés.

Ce changement affecte tous les pilotes en mode noyau pour les appareils qui prennent en charge le démarrage sécurisé UEFI (Unified Extensible Firmware Interface). Le démarrage sécurisé UEFI est requis pour la certification Windows 8 pour les ordinateurs clients, et facultatif pour les serveurs. Elle n’affecte pas les pilotes en mode utilisateur.

Le développement standard pour les pilotes en mode noyau implique soit l’utilisation du débogage en mode noyau, soit le paramètre de données de configuration de démarrage (BCD) <testsigning> . Ces deux options sont désactivées lorsque le démarrage sécurisé est activé.

## <a name="manifestation"></a>Manifestation

Les pilotes en mode noyau ne sont pas exécutés s’ils ne sont pas correctement signés par une autorité de certification approuvée. Le système d’exploitation n’autorise pas l’exécution des pilotes non autorisés et les mécanismes standard tels que le débogage du noyau et testsigning ne sont pas autorisés.

## <a name="mitigation"></a>Limitation des risques

Pour tester des pilotes, vous devez désactiver le démarrage sécurisé dans le BIOS et répondre aux autres exigences de signature de test (voir ci-dessous).

Lorsque vous distribuez plus largement des pilotes, ceux-ci doivent être correctement signés par une autorité de certification approuvée.

## <a name="resources"></a>Ressources

-   [Signature des pilotes](/previous-versions/windows/hardware/design/dn653563(v=vs.85))

 

 