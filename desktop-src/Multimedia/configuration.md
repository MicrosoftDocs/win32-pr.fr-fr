---
title: Configuration (Windows Multimedia)
description: Découvrez comment un pilote multimédia Windows peut permettre aux utilisateurs de choisir des paramètres de configuration en affichant une boîte de dialogue de configuration.
ms.assetid: d61d6c8b-8dba-45c2-ba99-0b2111a2d624
keywords:
- pilotes installables, configuration
- pilotes installables, DRV_CONFIGURE message
- Message DRV_CONFIGURE
- Message DRV_QUERYCONFIGURE
- Message DRVCONFIGINFO
- Configuration des pilotes installables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7804e4d92d30d666d4d28c253a1a44572a707daa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403922"
---
# <a name="configuration-windows-multimedia"></a>Configuration (Windows Multimedia)

Un pilote pouvant être installé peut permettre aux utilisateurs de choisir des paramètres de configuration pour le pilote et le matériel associé en affichant une boîte de dialogue de configuration lors du traitement du message de configuration du [**DRV \_**](drv-configure.md) . Le pilote est responsable de la création et de la gestion de la boîte de dialogue, du traitement de toute entrée d’utilisateur à partir de la boîte de dialogue et de la modification de la configuration du pilote ou du matériel comme demandé par l’utilisateur. Le pilote doit fournir une procédure de boîte de dialogue distincte pour traiter les messages de fenêtre pour la boîte de dialogue et un modèle de boîte de dialogue pour définir l’apparence et le contenu de la boîte de dialogue.

Avant de recevoir le \_ message de configuration du DRV, un pilote reçoit le message [**\_ QUERYCONFIGURE du DRV**](drv-queryconfigure.md) . Le pilote doit retourner une valeur différente de zéro à la requête pour garantir la réception du message de configuration du DRV suivant \_ .

Lors de l’initialisation de la boîte de dialogue de configuration, le pilote récupère généralement les informations de configuration à partir du Registre. Pour faciliter la recherche de ces informations, le \_ message de configuration du DRV inclut généralement l’adresse d’une structure [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) qui contient les noms de la clé de Registre et la valeur associée au pilote. Si l’utilisateur demande des modifications à la configuration, le pilote doit mettre à jour les informations de configuration dans le registre.

 

 
