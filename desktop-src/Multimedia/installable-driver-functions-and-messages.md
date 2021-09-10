---
title: Fonctions et messages des pilotes installables
description: Fonctions et messages des pilotes installables
ms.assetid: f487705a-ae8e-4ea8-bfd5-9b0f6087ddbb
keywords:
- pilotes installables, fonctions
- pilotes installables, messages
- pilotes installables, fonction OpenDriver
- OpenDriver fonction)
- pilotes installables, messages personnalisés
- messages du pilote
- messages de pilote personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66e6ebaac73bf8eb779119750cb390481152c3f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369063"
---
# <a name="installable-driver-functions-and-messages"></a>Fonctions et messages des pilotes installables

Vous pouvez ouvrir un pilote installable à partir d’une application à l’aide de la fonction [**OpenDriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) . Cette fonction crée une instance du pilote, en chargeant le pilote en mémoire si aucune autre instance n’existe et retourne le handle de la nouvelle instance. Lors de l’ouverture d’un pilote installable, vous devez fournir le chemin d’accès complet du pilote ou les noms de la clé de Registre et la valeur associée au pilote.

Une fois qu’un pilote est ouvert, vous pouvez le diriger pour effectuer des tâches à l’aide de la fonction [**SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) pour envoyer des messages de pilote au pilote. Par exemple, vous pouvez indiquer au pilote d’afficher sa boîte de dialogue de configuration en envoyant le message de configuration du [**DRV \_**](drv-configure.md) . Avant d’envoyer ce message, vous devez déterminer si le pilote a une boîte de dialogue de configuration en envoyant le message [**\_ QUERYCONFIGURE du DRV**](drv-queryconfigure.md) et en vérifiant une valeur de retour différente de zéro. De nombreux pilotes fournissent un ensemble de messages personnalisés que vous pouvez envoyer pour diriger les opérations du pilote.

Si vous avez besoin d’un accès spécial à un pilote pouvant être installé, tel que l’accès à ses ressources, vous pouvez récupérer le descripteur de module du pilote à l’aide de la fonction [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) .

Lorsque vous n’avez plus besoin du pilote installable, vous pouvez le fermer à l’aide de la fonction [**CloseDriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-closedriver) .

Vous pouvez utiliser les fonctions et messages des pilotes installables pour ouvrir et gérer n’importe quel pilote pouvant être installé. Toutefois, il est recommandé d’utiliser d’abord des services standard (tels que [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen), [**waveOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)et [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) pour les périphériques de sortie Waveform), le cas échéant. S’il n’existe pas de services standard pour un pilote multimédia, ouvrez et gérez le pilote à l’aide des fonctions et des messages du pilote installable.

> [!Note]  
> Les fonctions [**SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) et [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) sont les fonctions préférées à utiliser pour envoyer des messages à un pilote et pour obtenir un descripteur d’une instance de module. toutefois, l’ancienne fonction [**DrvGetModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-drvgetmodulehandle) a été incluse pour assurer la compatibilité avec les versions précédentes du système d’exploitation Windows.

 

 

 