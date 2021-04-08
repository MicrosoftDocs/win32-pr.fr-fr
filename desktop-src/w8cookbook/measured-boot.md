---
title: Démarrage mesuré
description: Démarrage mesuré
ms.assetid: D7ED02FA-6D0F-4753-AC07-BD7DCE55B3FD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccbba6e5f96fd91c00c295c4b15cab8849f11dc
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730740"
---
# <a name="measured-boot"></a>Démarrage mesuré

## <a name="platforms"></a>Plateformes

 **Clients** -Windows 8  
**Serveurs** -Windows Server 2012  



## <a name="description"></a>Description

Comme le logiciel anti-programme malveillant est devenu mieux et mieux adapté à la détection des programmes malveillants du runtime, les attaquants deviennent également mieux adaptés à la création de rootkits qui peuvent masquer la détection. La détection de programmes malveillants qui démarrent tôt au cours du cycle de démarrage est un défi que la plupart des fournisseurs sont tenus de faire face à la diligence. En règle générale, ils créent des piratages système qui ne sont pas pris en charge par le système d’exploitation hôte et qui peuvent entraîner le placement de l’ordinateur dans un état instable. Jusqu’à présent, Windows n’a pas fourni un bon moyen de détecter et de résoudre ces menaces de démarrage anticipé. Windows 8 introduit une nouvelle fonctionnalité appelée démarrage mesuré, qui mesure chaque composant, du microprogramme au-dessus des pilotes de démarrage de démarrage, stocke ces mesures dans le Module de plateforme sécurisée (TPM) (TPM) sur l’ordinateur, puis met à disposition un journal qui peut être testé à distance pour vérifier l’état de démarrage du client.

## <a name="manifestation"></a>Manifestation

La fonctionnalité de démarrage mesurée fournit aux logiciels un journal approuvé (résistant aux usurpations et falsifications) de tous les composants de démarrage qui ont démarré avant le logiciel. AM Software peut utiliser le journal pour déterminer si les composants qui ont été exécutés avant d’être dignes de confiance ou s’ils sont infectés par des logiciels malveillants. Le logiciel AM sur l’ordinateur local peut envoyer le journal à un serveur distant à des fins d’évaluation. Le serveur distant peut initier des actions de correction en interagissant avec le logiciel sur le client ou par le biais de mécanismes hors bande, le cas échéant.

## <a name="mitigation"></a>Limitation des risques

Dans les scénarios d’entreprise, l’administrateur système contrôle le mode d’utilisation des informations de démarrage mesurées. Dans les scénarios d’utilisateur final (par exemple, les banques en ligne), le consommateur doit s’inscrire pour utiliser le démarrage mesuré pour le service spécifique.

## <a name="solution"></a>Solution

Un livre blanc est préparé pour détailler les API et les appels de fonction qui doivent être faits pour différents scénarios de démarrage mesurés.

 

 




