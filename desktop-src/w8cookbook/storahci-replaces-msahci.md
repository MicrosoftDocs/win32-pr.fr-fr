---
title: StorAHCI remplace MSAHCI
description: StorAHCI remplace MSAHCI
ms.assetid: 9C6FAFA7-A6B3-4D3A-94EE-B53626DBF183
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6affffe41dd00c009ebb7bebf508dac1b63bec673c17783f594d22969822e542
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932139"
---
# <a name="storahci-replaces-msahci"></a>StorAHCI remplace MSAHCI

## <a name="platforms"></a>Plateformes

**Clients** – Windows 8  
**serveurs** – Windows Server 2012  


## <a name="description"></a>Description

StorAHCI, un miniport Storport, prend en charge les contrôleurs d’interface de contrôleur d’hôte (AHCI) avancés sata dans Windows, et remplace MSAHCI, un miniport ATAport.

## <a name="manifestation"></a>Manifestation

Il ne doit y avoir aucune modification de la fonctionnalité ou des performances. ce pilote prend en charge tous les appareils pris en charge par MSAHCI.

Cette modification est transparente pour l’utilisateur.

## <a name="mitigation"></a>Limitation des risques

Mettez à jour tous les utilitaires et scripts qui reposent sur des liaisons ATAport. Ne vous fiez pas au nom du lecteur. Utilisez plutôt la détection de disque standard.

 

 




