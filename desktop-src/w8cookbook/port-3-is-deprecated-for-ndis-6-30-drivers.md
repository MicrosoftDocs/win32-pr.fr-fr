---
title: Le port 3 est déconseillé pour les pilotes NDIS 6,30
description: Le port 3 est déconseillé pour les pilotes NDIS 6,30
ms.assetid: 900BD08D-3EAF-43F3-A74A-359815474FAD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0b4c7f6a33b179a14d3d7f8151d3850e16dd44
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104463834"
---
# <a name="port-3-is-deprecated-for-ndis-630-drivers"></a>Le port 3 est déconseillé pour les pilotes NDIS 6,30

## <a name="platforms"></a>Plateformes

**Clients** – Windows 8  
**Serveurs** – Windows Server 2012  


## <a name="description"></a>Description

Windows 8 supprime la prise en charge de la plateforme pour les pilotes WLAN miniport NDIS pour créer ou démarrer le port d’extensibilité IHV (également appelé troisième port). Cette fonctionnalité a été introduite dans Windows 7 en tant que mesure dépannage, tandis que l’Alliance d' Wi-Fi (WFA) a développé la spécification Wi-Fi directe. La spécification est maintenant terminée, les produits qui utilisent Wi-Fi direct sont certifiés et Windows 8 introduit une pile Native Wi-Fi direct.

## <a name="manifestation"></a>Manifestation

Rien, car le troisième port est une fonctionnalité de plateforme que les pilotes de miniport WLAN démarrent s’ils ont besoin de cette fonctionnalité.

## <a name="solution"></a>Solution

Nous conservons la fonctionnalité de port d’extensibilité disponible pour les pilotes existants qui ne signalent pas NDIS 6,30 pour assurer la compatibilité des appareils. Toutefois, les nouveaux pilotes WLAN qui signalent NDIS 6,30 ne pourront pas démarrer ce port. au lieu de cela, les développeurs de ces pilotes doivent utiliser Wi-Fi direct.

 

 




