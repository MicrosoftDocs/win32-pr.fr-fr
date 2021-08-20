---
title: Installation (Windows multimédia)
description: en savoir plus sur Windows installation multimédia, y compris le traitement des messages de DRV_INSTALL et de DRV_REMOVE.
ms.assetid: 1f0e23ad-4db7-4f32-98d9-e672370db559
keywords:
- pilotes installables, installation
- pilotes installables, DRV_INSTALL message
- pilotes installables, DRV_REMOVE message
- Message DRV_INSTALL
- Message DRV_REMOVE
- Message DRVCONFIGINFO
- installation des pilotes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01ef47952f3d5a62c0dce246bf24689d37f11326f0f3ec251f7afc19c822fa9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140677"
---
# <a name="installation-windows-multimedia"></a>Installation (Windows multimédia)

Un pilote pouvant être installé peut effectuer des tâches d’installation spécifiques au pilote lors du traitement des messages de [**\_ suppression**](drv-remove.md) de [**DRV \_ install**](drv-install.md) et DRV. Une application d’installation, telle qu’une application de panneau de configuration, envoie les messages au pilote lors de l’installation ou de la suppression du pilote, respectivement.

Lors du traitement du \_ message d’installation de DRV, le pilote vérifie généralement que le matériel requis est présent, puis affiche la boîte de dialogue de configuration pour permettre à l’utilisateur de choisir les paramètres de configuration initiaux pour le pilote et le matériel associé. Le message inclut l’adresse d’une structure [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) qui contient les noms de la clé de Registre et la valeur associée au pilote. le pilote vérifie la valeur de Registre pour les informations de configuration par défaut. Enfin, le pilote crée également des clés de Registre et des valeurs supplémentaires nécessaires pour réussir l’opération.

Lors du traitement du \_ message de suppression du DRV, le pilote supprime toutes les clés de Registre et les valeurs que vous avez créées.

 

 
