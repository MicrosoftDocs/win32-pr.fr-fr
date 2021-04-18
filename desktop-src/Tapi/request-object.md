---
description: L’objet de requête est créé à l’aide de COM CoCreateInstance et expose une interface, ITRequest.
ms.assetid: 1e4c71ce-6846-4e64-9346-455ed82aa458
title: Objet Request
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51e81cae01f2624ba863b304c0a5f732b221199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533640"
---
# <a name="request-object"></a>Objet Request

L’objet de requête est créé à l’aide de COM **CoCreateInstance** et expose une interface, [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest). Cette interface expose la méthode [**MakeCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) , qui permet à une application TAPI 3 d’utiliser la téléphonie assistée. La téléphonie assistée fournit aux applications prenant en charge la téléphonie un mécanisme simple pour effectuer des appels téléphoniques sans que le développeur n’ait besoin d’être entièrement responsable de la téléphonie.

Par exemple, une application de feuille de calcul peut ajouter un bouton « téléphoner » à l’aide de la téléphonie assistée sans implémenter les contrôles plus élaborés disponibles dans une application TAPI complète.

Pour plus d’informations, consultez la [vue d’ensemble de la téléphonie assistée](assisted-telephony-overview.md) .

 

 



